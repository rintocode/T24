# Temenos Connectors

We are going to learn how to cnfigure TC Server and TC Client

## TC Server
`./conf/TCServer/tcserver.xml`

```xml
<?xml version="1.0" ?>
<TCSERVER>
   <JMXRmiPort>1099</JMXRmiPort>
   <MONITOR_PORT> 9500 </MONITOR_PORT>
   <TELNETD_PORT> 9501 </TELNETD_PORT>
   <DEBUGGER_PORT> 9502 </DEBUGGER_PORT>
   <SPY_PORT> 9503 </SPY_PORT>
   <MESSAGEFORMATTERS>  
      <!--================================================
           Add formatters
      =================================================-->
   </MESSAGEFORMATTERS>

   <ADAPTERS>
      <!--================================================
         T24 Adapters
      =================================================-->
      <ADAPTER id="T24"> 
         <MAX_SESSION> 5 </MAX_SESSION>
         <MIN_SESSION> 1 </MIN_SESSION>
         <TIMEOUT>30</TIMEOUT>
         <LOGIN_CONTEXT></LOGIN_CONTEXT>
         <STARTIN>[GLOBUS_PATH]</STARTIN>
         <JBASEPATH>[JBASE_PATH]</JBASEPATH>
         <PROGRAM>tSS</PROGRAM>
         <PARAMETER>[OFS_SOURCE]</PARAMETER>
      </ADAPTER>
      <ADAPTER id="TEST">
         <MAX_SESSION> 5 </MAX_SESSION>
         <MIN_SESSION> 1 </MIN_SESSION>
         <TIMEOUT>30</TIMEOUT>
         <LOGIN_CONTEXT></LOGIN_CONTEXT>
         <STARTIN>[GLOBUS_PATH]</STARTIN>
         <JBASEPATH>[JBASE_PATH]</JBASEPATH>
         <PROGRAM>tSS</PROGRAM>
         <PARAMETER>[OFS_SOURCE]</PARAMETER>
         <ENVIRONMENT>test.vars</ENVIRONMENT>
      </ADAPTER>
   </ADAPTERS>

    <LISTENERS>
      <!--================================================
           Default Listeners for Temenos Browser
      =================================================-->
      <LISTENER Name="browser.1" type="tcp" active="true">
         <ADAPTERID>T24</ADAPTERID>
         <PORT> 10001 </PORT>
      </LISTENER>

      <LISTENER Name="browser.2" type="tcp" active="true">
         <ADAPTERID>T24</ADAPTERID>
         <PORT> 10002 </PORT>
      </LISTENER>

      <LISTENER Name="tcp.secured" type="tcp" active="true">
         <ADAPTERID>TEST</ADAPTERID>
         <PORT> 10003 </PORT>
      </LISTENER>
      <LISTENER Name="raw.tcp" type="raw-tcp" active="true">
         <ADAPTERID>TEST</ADAPTERID>
         <PORT> 7023 </PORT>
      </LISTENER>
   <LISTENERS>
</TCSERVER>
```

## TC Client
Configuration file: `./conf/channels.xml`

```xml
<?xml version="1.0" ?>
<!-- T24 Connector communications channels definitions -->

<CHANNELS>
   <SECURITY_CONFIG>jaas.config</SECURITY_CONFIG>
   
   <CHANNEL>
		<NAME> browser.1 </NAME>
		<TIMEOUT> 120 </TIMEOUT>
		<ADAPTER>
			<TYPE> tcp </TYPE>
			<PORT> 10001 </PORT>
			<SUPPLIER>
				<INITIATOR>
					<HOSTNAME> localhost </HOSTNAME>
				</INITIATOR>
			</SUPPLIER>
		</ADAPTER>
	</CHANNEL>

	<CHANNEL>
		<NAME> browser.2 </NAME>
		<TIMEOUT> 120 </TIMEOUT>
		<ADAPTER>
			<TYPE> tcp </TYPE>
			<PORT> 10002 </PORT>
			<SUPPLIER>
				<INITIATOR>
					<HOSTNAME> 127.0.0.1 </HOSTNAME>
				</INITIATOR>
			</SUPPLIER>
		</ADAPTER>
	</CHANNEL>

   <CHANNEL>
		<NAME> tcp.sample </NAME>
		<TIMEOUT> 120 </TIMEOUT>
		<ADAPTER>
			<TYPE> tcp </TYPE>
			<PORT> 10003 </PORT>
			<SUPPLIER>
				<INITIATOR>
					<HOSTNAME> 127.0.0.1 </HOSTNAME>
				</INITIATOR>
			</SUPPLIER>
		</ADAPTER>
   </CHANNEL>
</CHANNELS>
```