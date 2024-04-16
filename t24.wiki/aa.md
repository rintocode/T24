# Temenos T24 AA - Arrangement Architecture

## Objectives

1. Fundamentals of T24 Arrangement Architecture
2. Product life-cycle in AA
3. Create new Products or amend existing ones using AA Product Builder

## Product Lines and Property Classes

`Product Lines` (AA.PRODUCT.LINE) and `Property Classes` (AA.PROPERTY.CLASS) are the fundamental building blocks. They are defined by Temenos.<br>
A Product line is made of different property classes. <br>
A property class has a number of Property class `ATTRIBUTES` and `ACTIONS`. <br><br>

## Product groups and Properties

`Product groups` (AA.PRODUCT.GROUP) are subset of Product Lines and `Properties` (AA.PROPERTY) are named types of property classes. They can be created and modified by the bank. <br>
A product group has a number of properties associated with it.<br><br>

## Products and Product Conditions

`Product` is the lowest level. At this level we create `PRODUCT CONDITIONS` to define default values for the arrangement and if they can negotiated and with which restrictions. Each Property must have a Product condition.

## Arrangements and Arrangement conditions

## Activity Classes

Activity class relates to the Property class (@ID: PRODUCT.LINE-PROCESS-PROPERTY.CLASS) eg: LENDING-APPLY.RATE-INTEREST, LENDING-CAPITALISE-INTEREST <br>
It defines the system behavior when an activity is run.<br>

## Product life-cycle:

1. Design
2. Proof
3. Publish
