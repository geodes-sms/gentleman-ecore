# Ecore integration with Gentleman

## Approach

The transformation is two-fold.

1. We apply a M2M transformation with the ATLAS Transformation Language (ATL).  
   To apply the ATL transformation, an input and output metamodel are required.
The input metamodel will be Ecore and the output will be Gentleman Ecore model, Gentleman metamodel deﬁned with Ecore.
1. With the generated model, we apply an M2T transformation with the Epsilon Generation Language (EGL).  
   The EGL Generator main generates the JSON file, which can be loaded in Gentleman.

## Mapping

The mapping of concepts between Ecore and Gentleman is shown in the table below.

> Some elements supported by Gentleman, such as properties, are not presented in the table as they have no equivalence in Ecore.

| Ecore               | Gentleman
|:---------------------:|:------------------------------:|
| EPackage         | Model |
| EClass (abstract or interface) | Prototype |
| EClass (concrete) | Concrete |
| EEnum | Derivative |
| EDataType | Primitive |
| EAttribute (many) | Set |
| EAttribute | Attribute |
| EReference | Attribute |
