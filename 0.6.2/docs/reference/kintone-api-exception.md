# kintoneAPIException

Handle error responses from kintone Rest API

## Methods

### get()

**Parameters**

(none)

**Return**

[Kintone Error Response](https://developer.kintone.io/hc/en-us/articles/212495188#responses)

**Sample code**

<details class="tab-container" open>
<Summary>Get app with error response</Summary>

<strong class="tab-name">Javascript</strong>

<pre class="inline-code">

    var id = YOUR_APP_ID;
    kintoneApp.getApp({id}).then((rsp) => {
        console.log(rsp);
    }).catch((err) => {
        // This SDK return err with KintoneAPIException
        console.log(err.get());
    });

</pre>

<strong class="tab-name">Nodejs</strong>

<pre class="inline-code">

    let id = YOUR_APP_ID;
    kintoneApp.getApp({id}).then((rsp) => {
        console.log(rsp);
    }).catch((err) => {
        // This SDK return err with KintoneAPIException
        console.log(err.get());
    });
    
</pre>

<strong class="tab-name">Response</strong>

<pre class="inline-code">
    {
        "id":"KINTONE_ERROR_ID",
        "code":"KINTONE_ERROR_CODE",
        "message":"KINTONE_ERROR_MESSAGE",
        "errors": [
            /*errors items here*/
        ]

    }

</pre>

</details>

### getAll()

**Parameters**

(none)

**Return**

The result of Promise.Reject()

**Sample code**

<details class="tab-container" open>
<Summary>Get apps with error response</Summary>

<strong class="tab-name">Javascript</strong>

<pre class="inline-code">

    var id = YOUR_APP_ID;
    kintoneApp.getApp({id}).then((rsp) => {
        console.log(rsp);
    }).catch((err) => {
        // This SDK return err with KintoneAPIException
        console.log(err.getAll());
    });

</pre>

<strong class="tab-name">Nodejs</strong>

<pre class="inline-code">

    let id = YOUR_APP_ID;
    kintoneApp.getApp({id}).then((rsp) => {
        console.log(rsp);
    }).catch((err) => {
        // This SDK return err with KintoneAPIException
        console.log(err.getAll());
    });

</pre>

<strong class="tab-name">Response</strong>

<pre class="inline-code">
    // Response error object

</pre>

</details>

### throw()

> This function will throw result of [get()](#get) function

<strong class="tab-name">Parameter</strong>

(none)

**Return**

(none)

### throwAll()

> This function will throw result of [getAll()](#getall) function

**Parameters**

(none)

**Return**

(none)

## Reference

- [kintone REST API Overview](https://developer.kintone.io/hc/en-us/articles/212495188)`on developer network`
- [axios](https://www.npmjs.com/package/axios)`on npmjs`