
---
title: "Webhook"
title_tag: "azure-native.containerregistry.Webhook"
meta_desc: "Documentation for the azure-native.containerregistry.Webhook resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

An object that represents a webhook for a container registry.
API Version: 2019-05-01.

{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}


### WebhookCreate


{{< example csharp >}}

```csharp
using Pulumi;
using AzureNative = Pulumi.AzureNative;

class MyStack : Stack
{
    public MyStack()
    {
        var webhook = new AzureNative.ContainerRegistry.Webhook("webhook", new AzureNative.ContainerRegistry.WebhookArgs
        {
            Actions = 
            {
                "push",
            },
            CustomHeaders = 
            {
                { "Authorization", "Basic 000000000000000000000000000000000000000000000000000" },
            },
            Location = "westus",
            RegistryName = "myRegistry",
            ResourceGroupName = "myResourceGroup",
            Scope = "myRepository",
            ServiceUri = "http://myservice.com",
            Status = "enabled",
            Tags = 
            {
                { "key", "value" },
            },
            WebhookName = "myWebhook",
        });
    }

}

```


{{< /example >}}


{{< example go >}}


```go
package main

import (
	containerregistry "github.com/pulumi/pulumi-azure-native/sdk/go/azure/containerregistry"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := containerregistry.NewWebhook(ctx, "webhook", &containerregistry.WebhookArgs{
			Actions: pulumi.StringArray{
				pulumi.String("push"),
			},
			CustomHeaders: pulumi.StringMap{
				"Authorization": pulumi.String("Basic 000000000000000000000000000000000000000000000000000"),
			},
			Location:          pulumi.String("westus"),
			RegistryName:      pulumi.String("myRegistry"),
			ResourceGroupName: pulumi.String("myResourceGroup"),
			Scope:             pulumi.String("myRepository"),
			ServiceUri:        pulumi.String("http://myservice.com"),
			Status:            pulumi.String("enabled"),
			Tags: pulumi.StringMap{
				"key": pulumi.String("value"),
			},
			WebhookName: pulumi.String("myWebhook"),
		})
		if err != nil {
			return err
		}
		return nil
	})
}

```


{{< /example >}}


{{< example python >}}


```python
import pulumi
import pulumi_azure_native as azure_native

webhook = azure_native.containerregistry.Webhook("webhook",
    actions=["push"],
    custom_headers={
        "Authorization": "Basic 000000000000000000000000000000000000000000000000000",
    },
    location="westus",
    registry_name="myRegistry",
    resource_group_name="myResourceGroup",
    scope="myRepository",
    service_uri="http://myservice.com",
    status="enabled",
    tags={
        "key": "value",
    },
    webhook_name="myWebhook")

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure_native from "@pulumi/azure-native";

const webhook = new azure_native.containerregistry.Webhook("webhook", {
    actions: ["push"],
    customHeaders: {
        Authorization: "Basic 000000000000000000000000000000000000000000000000000",
    },
    location: "westus",
    registryName: "myRegistry",
    resourceGroupName: "myResourceGroup",
    scope: "myRepository",
    serviceUri: "http://myservice.com",
    status: "enabled",
    tags: {
        key: "value",
    },
    webhookName: "myWebhook",
});

```


{{< /example >}}





{{% /examples %}}




## Create a Webhook Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">Webhook</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">WebhookArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Webhook</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
            <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
            <span class="nx">actions</span><span class="p">:</span> <span class="nx">Optional[Sequence[Union[str, WebhookAction]]]</span> = None<span class="p">,</span>
            <span class="nx">custom_headers</span><span class="p">:</span> <span class="nx">Optional[Mapping[str, str]]</span> = None<span class="p">,</span>
            <span class="nx">location</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
            <span class="nx">registry_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
            <span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
            <span class="nx">scope</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
            <span class="nx">service_uri</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
            <span class="nx">status</span><span class="p">:</span> <span class="nx">Optional[Union[str, WebhookStatus]]</span> = None<span class="p">,</span>
            <span class="nx">tags</span><span class="p">:</span> <span class="nx">Optional[Mapping[str, str]]</span> = None<span class="p">,</span>
            <span class="nx">webhook_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Webhook</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
            <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">WebhookArgs</a></span><span class="p">,</span>
            <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewWebhook</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">WebhookArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">Webhook</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">Webhook</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">WebhookArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">WebhookArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

{{% choosable language python %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">WebhookArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">ResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties"><dt
        class="property-optional" title="Optional">
        <span>ctx</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span>
    </dt>
    <dd>Context object for the current deployment.</dd><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">WebhookArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">WebhookArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## Webhook Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The Webhook resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="actions_csharp">
<a href="#actions_csharp" style="color: inherit; text-decoration: inherit;">Actions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;Union&lt;string, Pulumi.<wbr>Azure<wbr>Native.<wbr>Container<wbr>Registry.<wbr>Webhook<wbr>Action&gt;&gt;</span>
    </dt>
    <dd>{{% md %}}The list of actions that trigger the webhook to post notifications.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="registryname_csharp">
<a href="#registryname_csharp" style="color: inherit; text-decoration: inherit;">Registry<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the container registry.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group to which the container registry belongs.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="serviceuri_csharp">
<a href="#serviceuri_csharp" style="color: inherit; text-decoration: inherit;">Service<wbr>Uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The service URI for the webhook to post notifications.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="customheaders_csharp">
<a href="#customheaders_csharp" style="color: inherit; text-decoration: inherit;">Custom<wbr>Headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}Custom headers that will be added to the webhook notifications.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="location_csharp">
<a href="#location_csharp" style="color: inherit; text-decoration: inherit;">Location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The location of the webhook. This cannot be changed after the resource is created.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="scope_csharp">
<a href="#scope_csharp" style="color: inherit; text-decoration: inherit;">Scope</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The scope of repositories where the event can be triggered. For example, 'foo:*' means events for all tags under repository 'foo'. 'foo:bar' means events for 'foo:bar' only. 'foo' is equivalent to 'foo:latest'. Empty means all events.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="status_csharp">
<a href="#status_csharp" style="color: inherit; text-decoration: inherit;">Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string | <a href="#webhookstatus">Pulumi.<wbr>Azure<wbr>Native.<wbr>Container<wbr>Registry.<wbr>Webhook<wbr>Status</a></span>
    </dt>
    <dd>{{% md %}}The status of the webhook at the time the operation was called.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}The tags for the webhook.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="webhookname_csharp">
<a href="#webhookname_csharp" style="color: inherit; text-decoration: inherit;">Webhook<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the webhook.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="actions_go">
<a href="#actions_go" style="color: inherit; text-decoration: inherit;">Actions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The list of actions that trigger the webhook to post notifications.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="registryname_go">
<a href="#registryname_go" style="color: inherit; text-decoration: inherit;">Registry<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the container registry.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group to which the container registry belongs.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="serviceuri_go">
<a href="#serviceuri_go" style="color: inherit; text-decoration: inherit;">Service<wbr>Uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The service URI for the webhook to post notifications.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="customheaders_go">
<a href="#customheaders_go" style="color: inherit; text-decoration: inherit;">Custom<wbr>Headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}Custom headers that will be added to the webhook notifications.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="location_go">
<a href="#location_go" style="color: inherit; text-decoration: inherit;">Location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The location of the webhook. This cannot be changed after the resource is created.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="scope_go">
<a href="#scope_go" style="color: inherit; text-decoration: inherit;">Scope</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The scope of repositories where the event can be triggered. For example, 'foo:*' means events for all tags under repository 'foo'. 'foo:bar' means events for 'foo:bar' only. 'foo' is equivalent to 'foo:latest'. Empty means all events.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="status_go">
<a href="#status_go" style="color: inherit; text-decoration: inherit;">Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string | <a href="#webhookstatus">Webhook<wbr>Status</a></span>
    </dt>
    <dd>{{% md %}}The status of the webhook at the time the operation was called.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}The tags for the webhook.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="webhookname_go">
<a href="#webhookname_go" style="color: inherit; text-decoration: inherit;">Webhook<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the webhook.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="actions_nodejs">
<a href="#actions_nodejs" style="color: inherit; text-decoration: inherit;">actions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">(string | Webhook<wbr>Action)[]</span>
    </dt>
    <dd>{{% md %}}The list of actions that trigger the webhook to post notifications.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="registryname_nodejs">
<a href="#registryname_nodejs" style="color: inherit; text-decoration: inherit;">registry<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the container registry.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group to which the container registry belongs.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="serviceuri_nodejs">
<a href="#serviceuri_nodejs" style="color: inherit; text-decoration: inherit;">service<wbr>Uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The service URI for the webhook to post notifications.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="customheaders_nodejs">
<a href="#customheaders_nodejs" style="color: inherit; text-decoration: inherit;">custom<wbr>Headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}Custom headers that will be added to the webhook notifications.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="location_nodejs">
<a href="#location_nodejs" style="color: inherit; text-decoration: inherit;">location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The location of the webhook. This cannot be changed after the resource is created.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="scope_nodejs">
<a href="#scope_nodejs" style="color: inherit; text-decoration: inherit;">scope</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The scope of repositories where the event can be triggered. For example, 'foo:*' means events for all tags under repository 'foo'. 'foo:bar' means events for 'foo:bar' only. 'foo' is equivalent to 'foo:latest'. Empty means all events.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="status_nodejs">
<a href="#status_nodejs" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string | <a href="#webhookstatus">Webhook<wbr>Status</a></span>
    </dt>
    <dd>{{% md %}}The status of the webhook at the time the operation was called.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}The tags for the webhook.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="webhookname_nodejs">
<a href="#webhookname_nodejs" style="color: inherit; text-decoration: inherit;">webhook<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the webhook.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="actions_python">
<a href="#actions_python" style="color: inherit; text-decoration: inherit;">actions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[Union[str, Webhook<wbr>Action]]</span>
    </dt>
    <dd>{{% md %}}The list of actions that trigger the webhook to post notifications.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="registry_name_python">
<a href="#registry_name_python" style="color: inherit; text-decoration: inherit;">registry_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the container registry.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource group to which the container registry belongs.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="service_uri_python">
<a href="#service_uri_python" style="color: inherit; text-decoration: inherit;">service_<wbr>uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The service URI for the webhook to post notifications.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="custom_headers_python">
<a href="#custom_headers_python" style="color: inherit; text-decoration: inherit;">custom_<wbr>headers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}Custom headers that will be added to the webhook notifications.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="location_python">
<a href="#location_python" style="color: inherit; text-decoration: inherit;">location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The location of the webhook. This cannot be changed after the resource is created.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="scope_python">
<a href="#scope_python" style="color: inherit; text-decoration: inherit;">scope</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The scope of repositories where the event can be triggered. For example, 'foo:*' means events for all tags under repository 'foo'. 'foo:bar' means events for 'foo:bar' only. 'foo' is equivalent to 'foo:latest'. Empty means all events.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="status_python">
<a href="#status_python" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str | <a href="#webhookstatus">Webhook<wbr>Status</a></span>
    </dt>
    <dd>{{% md %}}The status of the webhook at the time the operation was called.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}The tags for the webhook.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="webhook_name_python">
<a href="#webhook_name_python" style="color: inherit; text-decoration: inherit;">webhook_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the webhook.{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the Webhook resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioningstate_csharp">
<a href="#provisioningstate_csharp" style="color: inherit; text-decoration: inherit;">Provisioning<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provisioning state of the webhook at the time the operation was called.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the resource.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioningstate_go">
<a href="#provisioningstate_go" style="color: inherit; text-decoration: inherit;">Provisioning<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provisioning state of the webhook at the time the operation was called.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the resource.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioningstate_nodejs">
<a href="#provisioningstate_nodejs" style="color: inherit; text-decoration: inherit;">provisioning<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provisioning state of the webhook at the time the operation was called.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the resource.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioning_state_python">
<a href="#provisioning_state_python" style="color: inherit; text-decoration: inherit;">provisioning_<wbr>state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provisioning state of the webhook at the time the operation was called.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of the resource.{{% /md %}}</dd></dl>
{{% /choosable %}}







## Supporting Types



<h4 id="webhookaction">Webhook<wbr>Action</h4>

{{% choosable language csharp %}}
<dl class="tabular"><dt>Push</dt>
    <dd>push</dd><dt>Delete</dt>
    <dd>delete</dd><dt>Quarantine</dt>
    <dd>quarantine</dd><dt>Chart_<wbr>push</dt>
    <dd>chart_push</dd><dt>Chart_<wbr>delete</dt>
    <dd>chart_delete</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="tabular"><dt>Webhook<wbr>Action<wbr>Push</dt>
    <dd>push</dd><dt>Webhook<wbr>Action<wbr>Delete</dt>
    <dd>delete</dd><dt>Webhook<wbr>Action<wbr>Quarantine</dt>
    <dd>quarantine</dd><dt>Webhook<wbr>Action_Chart_<wbr>push</dt>
    <dd>chart_push</dd><dt>Webhook<wbr>Action_Chart_<wbr>delete</dt>
    <dd>chart_delete</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="tabular"><dt>Push</dt>
    <dd>push</dd><dt>Delete</dt>
    <dd>delete</dd><dt>Quarantine</dt>
    <dd>quarantine</dd><dt>Chart_<wbr>push</dt>
    <dd>chart_push</dd><dt>Chart_<wbr>delete</dt>
    <dd>chart_delete</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="tabular"><dt>PUSH</dt>
    <dd>push</dd><dt>DELETE</dt>
    <dd>delete</dd><dt>QUARANTINE</dt>
    <dd>quarantine</dd><dt>CHART_PUSH</dt>
    <dd>chart_push</dd><dt>CHART_DELETE</dt>
    <dd>chart_delete</dd></dl>
{{% /choosable %}}

<h4 id="webhookstatus">Webhook<wbr>Status</h4>

{{% choosable language csharp %}}
<dl class="tabular"><dt>Enabled</dt>
    <dd>enabled</dd><dt>Disabled</dt>
    <dd>disabled</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="tabular"><dt>Webhook<wbr>Status<wbr>Enabled</dt>
    <dd>enabled</dd><dt>Webhook<wbr>Status<wbr>Disabled</dt>
    <dd>disabled</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="tabular"><dt>Enabled</dt>
    <dd>enabled</dd><dt>Disabled</dt>
    <dd>disabled</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="tabular"><dt>ENABLED</dt>
    <dd>enabled</dd><dt>DISABLED</dt>
    <dd>disabled</dd></dl>
{{% /choosable %}}
## Import


An existing resource can be imported using its type token, name, and identifier, e.g.

```sh
$ pulumi import azure-native:containerregistry:Webhook myWebhook /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.ContainerRegistry/registries/myRegistry/webhooks/myWebhook 
```




<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-native">https://github.com/pulumi/pulumi-azure-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>

