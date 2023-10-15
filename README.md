# SAP UI5 Demo JSON Model

JSON Model in SAP UI5 is a client-side model and supports two-way data binding. It holds the data and provides methods to retrieve the data and to set and update data.

---

### Code Explaination:

Refer to [/webapp/view/App.view.xml](https://github.com/VaibhavMojidra/SAP-UI5---Demo-JSON-Model/blob/master/webapp/view/App.view.xml "App.view.xml")

`<Input value="{/name}" description="Hello {/name}" valueLiveUpdate="true" width="30%"/>`: This is an `Input` UI element. The `value` attribute binds the input's value to the `/name` path in the model. The `description` attribute sets a description that includes the input's current value. The `valueLiveUpdate` attribute enables live update for the input's value, meaning it updates as soon as you type. The `width` attribute sets the input's width to 30% of its container's width.

In this code, `{/name}` refers to the `name` property in the JSON model. When you change the value in the input field, it will automatically update the `name` property in the model because of two-way data binding. The description "Hello {/name}" will also update automatically to reflect the current value of `name`.

The curly brackets {…} indicate that data is taken from the value of the name property. This is called "data binding"



Refer to [/webapp/controller/App.controller.js](https://github.com/VaibhavMojidra/SAP-UI5---Demo-JSON-Model/blob/master/webapp/controller/App.controller.js "App.controller.js")

`onInit` is one of SAPUI5’s lifecycle methods that is invoked by the framework when the controller is created, similar to a constructor function of a control.

`sap.ui.model.json.JSONModel`: This is the JSON Model class from the SAP UI5 framework. A JSON Model is a client-side model and, as the name suggests, it supports JSON data.

`var oData={name:"Vaibhav Mojidra"};`: Here, a JavaScript object `oData` is being created with a single property `name` that has the value "Vaibhav Mojidra".

`var oModel=new JSONModel(oData);`: A new instance of the JSON Model is being created with `oData` as its data.

`this.getView().setModel(oModel);`: The model instance `oModel` is then set to the current view. This allows data binding between the view and the model in SAP UI5, meaning any UI elements in the view can now access and display the data from this model.

---

[![Vaibhav Mojidra - 1.jpeg](https://raw.githubusercontent.com/VaibhavMojidra/SAP-UI5---Demo-JSON-Model/master/screenshots/1.jpeg "Vaibhav Mojidra")](https://vaibhavmojidra.github.io/site/)

[![Vaibhav Mojidra - 2.jpeg](https://raw.githubusercontent.com/VaibhavMojidra/SAP-UI5---Demo-JSON-Model/master/screenshots/2.jpeg "Vaibhav Mojidra")](https://vaibhavmojidra.github.io/site/)