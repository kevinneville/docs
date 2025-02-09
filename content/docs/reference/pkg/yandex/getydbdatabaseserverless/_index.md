
---
title: "getYdbDatabaseServerless"
title_tag: "yandex.getYdbDatabaseServerless"
meta_desc: "Documentation for the yandex.getYdbDatabaseServerless function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Get information about a Yandex Database serverless cluster.
For more information, see [the official documentation](https://cloud.yandex.com/en/docs/ydb/concepts/serverless_and_dedicated).


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Yandex = Pulumi.Yandex;

class MyStack : Stack
{
    public MyStack()
    {
        var myDatabase = Output.Create(Yandex.GetYdbDatabaseServerless.InvokeAsync(new Yandex.GetYdbDatabaseServerlessArgs
        {
            DatabaseId = "some_ydb_serverless_database_id",
        }));
        this.YdbApiEndpoint = myDatabase.Apply(myDatabase => myDatabase.YdbApiEndpoint);
    }

    [Output("ydbApiEndpoint")]
    public Output<string> YdbApiEndpoint { get; set; }
}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-yandex/sdk/go/yandex"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		opt0 := "some_ydb_serverless_database_id"
		myDatabase, err := yandex.LookupYdbDatabaseServerless(ctx, &yandex.LookupYdbDatabaseServerlessArgs{
			DatabaseId: &opt0,
		}, nil)
		if err != nil {
			return err
		}
		ctx.Export("ydbApiEndpoint", myDatabase.YdbApiEndpoint)
		return nil
	})
}
```


{{< /example >}}


{{< example python >}}

```python
import pulumi
import pulumi_yandex as yandex

my_database = yandex.get_ydb_database_serverless(database_id="some_ydb_serverless_database_id")
pulumi.export("ydbApiEndpoint", my_database.ydb_api_endpoint)
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as yandex from "@pulumi/yandex";

const myDatabase = pulumi.output(yandex.getYdbDatabaseServerless({
    databaseId: "some_ydb_serverless_database_id",
}, { async: true }));

export const ydbApiEndpoint = myDatabase.ydbApiEndpoint;
```


{{< /example >}}





{{% /examples %}}




## Using getYdbDatabaseServerless {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getYdbDatabaseServerless<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetYdbDatabaseServerlessArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetYdbDatabaseServerlessResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_ydb_database_serverless(</span><span class="nx">database_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                <span class="nx">folder_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                <span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetYdbDatabaseServerlessResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupYdbDatabaseServerless<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupYdbDatabaseServerlessArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupYdbDatabaseServerlessResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupYdbDatabaseServerless` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetYdbDatabaseServerless </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetYdbDatabaseServerlessResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetYdbDatabaseServerlessArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="databaseid_csharp">
<a href="#databaseid_csharp" style="color: inherit; text-decoration: inherit;">Database<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="folderid_csharp">
<a href="#folderid_csharp" style="color: inherit; text-decoration: inherit;">Folder<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the folder that the Yandex Database serverless cluster belongs to.
It will be deduced from provider configuration if not set explicitly.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the Yandex Database serverless cluster.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="databaseid_go">
<a href="#databaseid_go" style="color: inherit; text-decoration: inherit;">Database<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="folderid_go">
<a href="#folderid_go" style="color: inherit; text-decoration: inherit;">Folder<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the folder that the Yandex Database serverless cluster belongs to.
It will be deduced from provider configuration if not set explicitly.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the Yandex Database serverless cluster.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="databaseid_nodejs">
<a href="#databaseid_nodejs" style="color: inherit; text-decoration: inherit;">database<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="folderid_nodejs">
<a href="#folderid_nodejs" style="color: inherit; text-decoration: inherit;">folder<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the folder that the Yandex Database serverless cluster belongs to.
It will be deduced from provider configuration if not set explicitly.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the Yandex Database serverless cluster.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="database_id_python">
<a href="#database_id_python" style="color: inherit; text-decoration: inherit;">database_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="folder_id_python">
<a href="#folder_id_python" style="color: inherit; text-decoration: inherit;">folder_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the folder that the Yandex Database serverless cluster belongs to.
It will be deduced from provider configuration if not set explicitly.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the Yandex Database serverless cluster.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getYdbDatabaseServerless Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createdat_csharp">
<a href="#createdat_csharp" style="color: inherit; text-decoration: inherit;">Created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Yandex Database serverless cluster creation timestamp.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="databasepath_csharp">
<a href="#databasepath_csharp" style="color: inherit; text-decoration: inherit;">Database<wbr>Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Full database path of the Yandex Database serverless cluster.
Useful for SDK configuration.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_csharp">
<a href="#description_csharp" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A description of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="documentapiendpoint_csharp">
<a href="#documentapiendpoint_csharp" style="color: inherit; text-decoration: inherit;">Document<wbr>Api<wbr>Endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Document API endpoint of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="labels_csharp">
<a href="#labels_csharp" style="color: inherit; text-decoration: inherit;">Labels</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}A set of key/value label pairs assigned to the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="locationid_csharp">
<a href="#locationid_csharp" style="color: inherit; text-decoration: inherit;">Location<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Location ID of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="status_csharp">
<a href="#status_csharp" style="color: inherit; text-decoration: inherit;">Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Status of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tlsenabled_csharp">
<a href="#tlsenabled_csharp" style="color: inherit; text-decoration: inherit;">Tls<wbr>Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether TLS is enabled for the Yandex Database serverless cluster.
Useful for SDK configuration.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ydbapiendpoint_csharp">
<a href="#ydbapiendpoint_csharp" style="color: inherit; text-decoration: inherit;">Ydb<wbr>Api<wbr>Endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}API endpoint of the Yandex Database serverless cluster.
Useful for SDK configuration.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ydbfullendpoint_csharp">
<a href="#ydbfullendpoint_csharp" style="color: inherit; text-decoration: inherit;">Ydb<wbr>Full<wbr>Endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Full endpoint of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="databaseid_csharp">
<a href="#databaseid_csharp" style="color: inherit; text-decoration: inherit;">Database<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="folderid_csharp">
<a href="#folderid_csharp" style="color: inherit; text-decoration: inherit;">Folder<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createdat_go">
<a href="#createdat_go" style="color: inherit; text-decoration: inherit;">Created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Yandex Database serverless cluster creation timestamp.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="databasepath_go">
<a href="#databasepath_go" style="color: inherit; text-decoration: inherit;">Database<wbr>Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Full database path of the Yandex Database serverless cluster.
Useful for SDK configuration.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_go">
<a href="#description_go" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A description of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="documentapiendpoint_go">
<a href="#documentapiendpoint_go" style="color: inherit; text-decoration: inherit;">Document<wbr>Api<wbr>Endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Document API endpoint of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="labels_go">
<a href="#labels_go" style="color: inherit; text-decoration: inherit;">Labels</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}A set of key/value label pairs assigned to the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="locationid_go">
<a href="#locationid_go" style="color: inherit; text-decoration: inherit;">Location<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Location ID of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="status_go">
<a href="#status_go" style="color: inherit; text-decoration: inherit;">Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Status of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tlsenabled_go">
<a href="#tlsenabled_go" style="color: inherit; text-decoration: inherit;">Tls<wbr>Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether TLS is enabled for the Yandex Database serverless cluster.
Useful for SDK configuration.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ydbapiendpoint_go">
<a href="#ydbapiendpoint_go" style="color: inherit; text-decoration: inherit;">Ydb<wbr>Api<wbr>Endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}API endpoint of the Yandex Database serverless cluster.
Useful for SDK configuration.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ydbfullendpoint_go">
<a href="#ydbfullendpoint_go" style="color: inherit; text-decoration: inherit;">Ydb<wbr>Full<wbr>Endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Full endpoint of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="databaseid_go">
<a href="#databaseid_go" style="color: inherit; text-decoration: inherit;">Database<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="folderid_go">
<a href="#folderid_go" style="color: inherit; text-decoration: inherit;">Folder<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createdat_nodejs">
<a href="#createdat_nodejs" style="color: inherit; text-decoration: inherit;">created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Yandex Database serverless cluster creation timestamp.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="databasepath_nodejs">
<a href="#databasepath_nodejs" style="color: inherit; text-decoration: inherit;">database<wbr>Path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Full database path of the Yandex Database serverless cluster.
Useful for SDK configuration.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_nodejs">
<a href="#description_nodejs" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A description of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="documentapiendpoint_nodejs">
<a href="#documentapiendpoint_nodejs" style="color: inherit; text-decoration: inherit;">document<wbr>Api<wbr>Endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Document API endpoint of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="labels_nodejs">
<a href="#labels_nodejs" style="color: inherit; text-decoration: inherit;">labels</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}A set of key/value label pairs assigned to the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="locationid_nodejs">
<a href="#locationid_nodejs" style="color: inherit; text-decoration: inherit;">location<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Location ID of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="status_nodejs">
<a href="#status_nodejs" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Status of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tlsenabled_nodejs">
<a href="#tlsenabled_nodejs" style="color: inherit; text-decoration: inherit;">tls<wbr>Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Whether TLS is enabled for the Yandex Database serverless cluster.
Useful for SDK configuration.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ydbapiendpoint_nodejs">
<a href="#ydbapiendpoint_nodejs" style="color: inherit; text-decoration: inherit;">ydb<wbr>Api<wbr>Endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}API endpoint of the Yandex Database serverless cluster.
Useful for SDK configuration.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ydbfullendpoint_nodejs">
<a href="#ydbfullendpoint_nodejs" style="color: inherit; text-decoration: inherit;">ydb<wbr>Full<wbr>Endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Full endpoint of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="databaseid_nodejs">
<a href="#databaseid_nodejs" style="color: inherit; text-decoration: inherit;">database<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="folderid_nodejs">
<a href="#folderid_nodejs" style="color: inherit; text-decoration: inherit;">folder<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="created_at_python">
<a href="#created_at_python" style="color: inherit; text-decoration: inherit;">created_<wbr>at</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Yandex Database serverless cluster creation timestamp.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="database_path_python">
<a href="#database_path_python" style="color: inherit; text-decoration: inherit;">database_<wbr>path</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Full database path of the Yandex Database serverless cluster.
Useful for SDK configuration.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_python">
<a href="#description_python" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A description of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="document_api_endpoint_python">
<a href="#document_api_endpoint_python" style="color: inherit; text-decoration: inherit;">document_<wbr>api_<wbr>endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Document API endpoint of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="labels_python">
<a href="#labels_python" style="color: inherit; text-decoration: inherit;">labels</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}A set of key/value label pairs assigned to the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="location_id_python">
<a href="#location_id_python" style="color: inherit; text-decoration: inherit;">location_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Location ID of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="status_python">
<a href="#status_python" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Status of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tls_enabled_python">
<a href="#tls_enabled_python" style="color: inherit; text-decoration: inherit;">tls_<wbr>enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether TLS is enabled for the Yandex Database serverless cluster.
Useful for SDK configuration.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ydb_api_endpoint_python">
<a href="#ydb_api_endpoint_python" style="color: inherit; text-decoration: inherit;">ydb_<wbr>api_<wbr>endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}API endpoint of the Yandex Database serverless cluster.
Useful for SDK configuration.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ydb_full_endpoint_python">
<a href="#ydb_full_endpoint_python" style="color: inherit; text-decoration: inherit;">ydb_<wbr>full_<wbr>endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Full endpoint of the Yandex Database serverless cluster.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="database_id_python">
<a href="#database_id_python" style="color: inherit; text-decoration: inherit;">database_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="folder_id_python">
<a href="#folder_id_python" style="color: inherit; text-decoration: inherit;">folder_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-yandex">https://github.com/pulumi/pulumi-yandex</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`yandex` Terraform Provider](https://github.com/yandex-cloud/terraform-provider-yandex).{{% /md %}}</dd>
</dl>

