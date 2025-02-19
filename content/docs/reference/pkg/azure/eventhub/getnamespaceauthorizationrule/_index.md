
---
title: "getNamespaceAuthorizationRule"
title_tag: "azure.eventhub.getNamespaceAuthorizationRule"
meta_desc: "Documentation for the azure.eventhub.getNamespaceAuthorizationRule function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use this data source to access information about an Authorization Rule for an Event Hub Namespace.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Azure = Pulumi.Azure;

class MyStack : Stack
{
    public MyStack()
    {
        var example = Output.Create(Azure.EventHub.GetNamespaceAuthorizationRule.InvokeAsync(new Azure.EventHub.GetNamespaceAuthorizationRuleArgs
        {
            Name = "navi",
            ResourceGroupName = "example-resources",
            NamespaceName = "example-ns",
        }));
        this.EventhubAuthorizationRuleId = data.Azurem_eventhub_namespace_authorization_rule.Example.Id;
    }

    [Output("eventhubAuthorizationRuleId")]
    public Output<string> EventhubAuthorizationRuleId { get; set; }
}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-azure/sdk/v4/go/azure/eventhub"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := eventhub.LookupNamespaceAuthorizationRule(ctx, &eventhub.LookupNamespaceAuthorizationRuleArgs{
			Name:              "navi",
			ResourceGroupName: "example-resources",
			NamespaceName:     "example-ns",
		}, nil)
		if err != nil {
			return err
		}
		ctx.Export("eventhubAuthorizationRuleId", data.Azurem_eventhub_namespace_authorization_rule.Example.Id)
		return nil
	})
}
```


{{< /example >}}


{{< example python >}}

```python
import pulumi
import pulumi_azure as azure

example = azure.eventhub.get_namespace_authorization_rule(name="navi",
    resource_group_name="example-resources",
    namespace_name="example-ns")
pulumi.export("eventhubAuthorizationRuleId", data["azurem_eventhub_namespace_authorization_rule"]["example"]["id"])
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure from "@pulumi/azure";

const example = azure.eventhub.getNamespaceAuthorizationRule({
    name: "navi",
    resourceGroupName: "example-resources",
    namespaceName: "example-ns",
});
export const eventhubAuthorizationRuleId = data.azurem_eventhub_namespace_authorization_rule.example.id;
```


{{< /example >}}





{{% /examples %}}




## Using getNamespaceAuthorizationRule {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getNamespaceAuthorizationRule<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetNamespaceAuthorizationRuleArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetNamespaceAuthorizationRuleResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_namespace_authorization_rule(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                     <span class="nx">namespace_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                     <span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                     <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetNamespaceAuthorizationRuleResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupNamespaceAuthorizationRule<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupNamespaceAuthorizationRuleArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupNamespaceAuthorizationRuleResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupNamespaceAuthorizationRule` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetNamespaceAuthorizationRule </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetNamespaceAuthorizationRuleResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetNamespaceAuthorizationRuleArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the EventHub Authorization Rule resource.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="namespacename_csharp">
<a href="#namespacename_csharp" style="color: inherit; text-decoration: inherit;">Namespace<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the EventHub Namespace.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group in which the EventHub Namespace exists.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the EventHub Authorization Rule resource.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="namespacename_go">
<a href="#namespacename_go" style="color: inherit; text-decoration: inherit;">Namespace<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the EventHub Namespace.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group in which the EventHub Namespace exists.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the EventHub Authorization Rule resource.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="namespacename_nodejs">
<a href="#namespacename_nodejs" style="color: inherit; text-decoration: inherit;">namespace<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the EventHub Namespace.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group in which the EventHub Namespace exists.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the EventHub Authorization Rule resource.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="namespace_name_python">
<a href="#namespace_name_python" style="color: inherit; text-decoration: inherit;">namespace_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the name of the EventHub Namespace.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource group in which the EventHub Namespace exists.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getNamespaceAuthorizationRule Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
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
        <span id="listen_csharp">
<a href="#listen_csharp" style="color: inherit; text-decoration: inherit;">Listen</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Does this Authorization Rule have permissions to Listen to the Event Hub?
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="manage_csharp">
<a href="#manage_csharp" style="color: inherit; text-decoration: inherit;">Manage</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Does this Authorization Rule have permissions to Manage to the Event Hub?
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="namespacename_csharp">
<a href="#namespacename_csharp" style="color: inherit; text-decoration: inherit;">Namespace<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="primaryconnectionstring_csharp">
<a href="#primaryconnectionstring_csharp" style="color: inherit; text-decoration: inherit;">Primary<wbr>Connection<wbr>String</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Primary Connection String for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="primaryconnectionstringalias_csharp">
<a href="#primaryconnectionstringalias_csharp" style="color: inherit; text-decoration: inherit;">Primary<wbr>Connection<wbr>String<wbr>Alias</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The alias of the Primary Connection String for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="primarykey_csharp">
<a href="#primarykey_csharp" style="color: inherit; text-decoration: inherit;">Primary<wbr>Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Primary Key for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secondaryconnectionstring_csharp">
<a href="#secondaryconnectionstring_csharp" style="color: inherit; text-decoration: inherit;">Secondary<wbr>Connection<wbr>String</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Secondary Connection String for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secondaryconnectionstringalias_csharp">
<a href="#secondaryconnectionstringalias_csharp" style="color: inherit; text-decoration: inherit;">Secondary<wbr>Connection<wbr>String<wbr>Alias</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The alias of the Secondary Connection String for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secondarykey_csharp">
<a href="#secondarykey_csharp" style="color: inherit; text-decoration: inherit;">Secondary<wbr>Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Secondary Key for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="send_csharp">
<a href="#send_csharp" style="color: inherit; text-decoration: inherit;">Send</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Does this Authorization Rule have permissions to Send to the Event Hub?
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
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
        <span id="listen_go">
<a href="#listen_go" style="color: inherit; text-decoration: inherit;">Listen</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Does this Authorization Rule have permissions to Listen to the Event Hub?
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="manage_go">
<a href="#manage_go" style="color: inherit; text-decoration: inherit;">Manage</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Does this Authorization Rule have permissions to Manage to the Event Hub?
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="namespacename_go">
<a href="#namespacename_go" style="color: inherit; text-decoration: inherit;">Namespace<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="primaryconnectionstring_go">
<a href="#primaryconnectionstring_go" style="color: inherit; text-decoration: inherit;">Primary<wbr>Connection<wbr>String</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Primary Connection String for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="primaryconnectionstringalias_go">
<a href="#primaryconnectionstringalias_go" style="color: inherit; text-decoration: inherit;">Primary<wbr>Connection<wbr>String<wbr>Alias</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The alias of the Primary Connection String for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="primarykey_go">
<a href="#primarykey_go" style="color: inherit; text-decoration: inherit;">Primary<wbr>Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Primary Key for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secondaryconnectionstring_go">
<a href="#secondaryconnectionstring_go" style="color: inherit; text-decoration: inherit;">Secondary<wbr>Connection<wbr>String</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Secondary Connection String for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secondaryconnectionstringalias_go">
<a href="#secondaryconnectionstringalias_go" style="color: inherit; text-decoration: inherit;">Secondary<wbr>Connection<wbr>String<wbr>Alias</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The alias of the Secondary Connection String for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secondarykey_go">
<a href="#secondarykey_go" style="color: inherit; text-decoration: inherit;">Secondary<wbr>Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Secondary Key for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="send_go">
<a href="#send_go" style="color: inherit; text-decoration: inherit;">Send</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Does this Authorization Rule have permissions to Send to the Event Hub?
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
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
        <span id="listen_nodejs">
<a href="#listen_nodejs" style="color: inherit; text-decoration: inherit;">listen</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Does this Authorization Rule have permissions to Listen to the Event Hub?
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="manage_nodejs">
<a href="#manage_nodejs" style="color: inherit; text-decoration: inherit;">manage</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Does this Authorization Rule have permissions to Manage to the Event Hub?
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="namespacename_nodejs">
<a href="#namespacename_nodejs" style="color: inherit; text-decoration: inherit;">namespace<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="primaryconnectionstring_nodejs">
<a href="#primaryconnectionstring_nodejs" style="color: inherit; text-decoration: inherit;">primary<wbr>Connection<wbr>String</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Primary Connection String for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="primaryconnectionstringalias_nodejs">
<a href="#primaryconnectionstringalias_nodejs" style="color: inherit; text-decoration: inherit;">primary<wbr>Connection<wbr>String<wbr>Alias</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The alias of the Primary Connection String for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="primarykey_nodejs">
<a href="#primarykey_nodejs" style="color: inherit; text-decoration: inherit;">primary<wbr>Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Primary Key for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secondaryconnectionstring_nodejs">
<a href="#secondaryconnectionstring_nodejs" style="color: inherit; text-decoration: inherit;">secondary<wbr>Connection<wbr>String</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Secondary Connection String for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secondaryconnectionstringalias_nodejs">
<a href="#secondaryconnectionstringalias_nodejs" style="color: inherit; text-decoration: inherit;">secondary<wbr>Connection<wbr>String<wbr>Alias</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The alias of the Secondary Connection String for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secondarykey_nodejs">
<a href="#secondarykey_nodejs" style="color: inherit; text-decoration: inherit;">secondary<wbr>Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Secondary Key for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="send_nodejs">
<a href="#send_nodejs" style="color: inherit; text-decoration: inherit;">send</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Does this Authorization Rule have permissions to Send to the Event Hub?
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
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
        <span id="listen_python">
<a href="#listen_python" style="color: inherit; text-decoration: inherit;">listen</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Does this Authorization Rule have permissions to Listen to the Event Hub?
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="manage_python">
<a href="#manage_python" style="color: inherit; text-decoration: inherit;">manage</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Does this Authorization Rule have permissions to Manage to the Event Hub?
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="namespace_name_python">
<a href="#namespace_name_python" style="color: inherit; text-decoration: inherit;">namespace_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="primary_connection_string_python">
<a href="#primary_connection_string_python" style="color: inherit; text-decoration: inherit;">primary_<wbr>connection_<wbr>string</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Primary Connection String for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="primary_connection_string_alias_python">
<a href="#primary_connection_string_alias_python" style="color: inherit; text-decoration: inherit;">primary_<wbr>connection_<wbr>string_<wbr>alias</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The alias of the Primary Connection String for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="primary_key_python">
<a href="#primary_key_python" style="color: inherit; text-decoration: inherit;">primary_<wbr>key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Primary Key for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secondary_connection_string_python">
<a href="#secondary_connection_string_python" style="color: inherit; text-decoration: inherit;">secondary_<wbr>connection_<wbr>string</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Secondary Connection String for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secondary_connection_string_alias_python">
<a href="#secondary_connection_string_alias_python" style="color: inherit; text-decoration: inherit;">secondary_<wbr>connection_<wbr>string_<wbr>alias</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The alias of the Secondary Connection String for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="secondary_key_python">
<a href="#secondary_key_python" style="color: inherit; text-decoration: inherit;">secondary_<wbr>key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Secondary Key for the Event Hubs authorization Rule.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="send_python">
<a href="#send_python" style="color: inherit; text-decoration: inherit;">send</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Does this Authorization Rule have permissions to Send to the Event Hub?
{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure">https://github.com/pulumi/pulumi-azure</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`azurerm` Terraform Provider](https://github.com/hashicorp/terraform-provider-azurerm).{{% /md %}}</dd>
</dl>

