
---
title: "EventHubConnection"
title_tag: "azure-native.kusto.EventHubConnection"
meta_desc: "Documentation for the azure-native.kusto.EventHubConnection resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Class representing an event hub connection.
API Version: 2018-09-07-preview.

{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}


### KustoEventHubConnectionsCreateOrUpdate


{{< example csharp >}}

```csharp
using Pulumi;
using AzureNative = Pulumi.AzureNative;

class MyStack : Stack
{
    public MyStack()
    {
        var eventHubConnection = new AzureNative.Kusto.EventHubConnection("eventHubConnection", new AzureNative.Kusto.EventHubConnectionArgs
        {
            ClusterName = "KustoClusterRPTest4",
            ConsumerGroup = "testConsumerGroup1",
            DatabaseName = "KustoDatabase8",
            EventHubConnectionName = "kustoeventhubconnection1",
            EventHubResourceId = "/subscriptions/12345678-1234-1234-1234-123456789098/resourceGroups/kustorptest/providers/Microsoft.EventHub/namespaces/eventhubTestns1/eventhubs/eventhubTest1",
            Location = "westus",
            ResourceGroupName = "kustorptest",
        });
    }

}

```


{{< /example >}}


{{< example go >}}


```go
package main

import (
	kusto "github.com/pulumi/pulumi-azure-native/sdk/go/azure/kusto"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := kusto.NewEventHubConnection(ctx, "eventHubConnection", &kusto.EventHubConnectionArgs{
			ClusterName:            pulumi.String("KustoClusterRPTest4"),
			ConsumerGroup:          pulumi.String("testConsumerGroup1"),
			DatabaseName:           pulumi.String("KustoDatabase8"),
			EventHubConnectionName: pulumi.String("kustoeventhubconnection1"),
			EventHubResourceId:     pulumi.String("/subscriptions/12345678-1234-1234-1234-123456789098/resourceGroups/kustorptest/providers/Microsoft.EventHub/namespaces/eventhubTestns1/eventhubs/eventhubTest1"),
			Location:               pulumi.String("westus"),
			ResourceGroupName:      pulumi.String("kustorptest"),
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

event_hub_connection = azure_native.kusto.EventHubConnection("eventHubConnection",
    cluster_name="KustoClusterRPTest4",
    consumer_group="testConsumerGroup1",
    database_name="KustoDatabase8",
    event_hub_connection_name="kustoeventhubconnection1",
    event_hub_resource_id="/subscriptions/12345678-1234-1234-1234-123456789098/resourceGroups/kustorptest/providers/Microsoft.EventHub/namespaces/eventhubTestns1/eventhubs/eventhubTest1",
    location="westus",
    resource_group_name="kustorptest")

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure_native from "@pulumi/azure-native";

const eventHubConnection = new azure_native.kusto.EventHubConnection("eventHubConnection", {
    clusterName: "KustoClusterRPTest4",
    consumerGroup: "testConsumerGroup1",
    databaseName: "KustoDatabase8",
    eventHubConnectionName: "kustoeventhubconnection1",
    eventHubResourceId: "/subscriptions/12345678-1234-1234-1234-123456789098/resourceGroups/kustorptest/providers/Microsoft.EventHub/namespaces/eventhubTestns1/eventhubs/eventhubTest1",
    location: "westus",
    resourceGroupName: "kustorptest",
});

```


{{< /example >}}





{{% /examples %}}




## Create a EventHubConnection Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">EventHubConnection</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">EventHubConnectionArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">EventHubConnection</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                       <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                       <span class="nx">cluster_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                       <span class="nx">consumer_group</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                       <span class="nx">data_format</span><span class="p">:</span> <span class="nx">Optional[Union[str, DataFormat]]</span> = None<span class="p">,</span>
                       <span class="nx">database_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                       <span class="nx">event_hub_connection_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                       <span class="nx">event_hub_resource_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                       <span class="nx">location</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                       <span class="nx">mapping_rule_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                       <span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                       <span class="nx">table_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">EventHubConnection</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                       <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">EventHubConnectionArgs</a></span><span class="p">,</span>
                       <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewEventHubConnection</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">EventHubConnectionArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">EventHubConnection</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">EventHubConnection</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">EventHubConnectionArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">EventHubConnectionArgs</a></span>
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
        <span class="property-type"><a href="#inputs">EventHubConnectionArgs</a></span>
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
        <span class="property-type"><a href="#inputs">EventHubConnectionArgs</a></span>
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
        <span class="property-type"><a href="#inputs">EventHubConnectionArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## EventHubConnection Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The EventHubConnection resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="clustername_csharp">
<a href="#clustername_csharp" style="color: inherit; text-decoration: inherit;">Cluster<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Kusto cluster.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="consumergroup_csharp">
<a href="#consumergroup_csharp" style="color: inherit; text-decoration: inherit;">Consumer<wbr>Group</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The event hub consumer group.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="databasename_csharp">
<a href="#databasename_csharp" style="color: inherit; text-decoration: inherit;">Database<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the database in the Kusto cluster.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="eventhubresourceid_csharp">
<a href="#eventhubresourceid_csharp" style="color: inherit; text-decoration: inherit;">Event<wbr>Hub<wbr>Resource<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource ID of the event hub to be used to create a data connection.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group containing the Kusto cluster.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="dataformat_csharp">
<a href="#dataformat_csharp" style="color: inherit; text-decoration: inherit;">Data<wbr>Format</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string | <a href="#dataformat">Pulumi.<wbr>Azure<wbr>Native.<wbr>Kusto.<wbr>Data<wbr>Format</a></span>
    </dt>
    <dd>{{% md %}}The data format of the message. Optionally the data format can be added to each message.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="eventhubconnectionname_csharp">
<a href="#eventhubconnectionname_csharp" style="color: inherit; text-decoration: inherit;">Event<wbr>Hub<wbr>Connection<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the event hub connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="location_csharp">
<a href="#location_csharp" style="color: inherit; text-decoration: inherit;">Location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource location.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="mappingrulename_csharp">
<a href="#mappingrulename_csharp" style="color: inherit; text-decoration: inherit;">Mapping<wbr>Rule<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The mapping rule to be used to ingest the data. Optionally the mapping information can be added to each message.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tablename_csharp">
<a href="#tablename_csharp" style="color: inherit; text-decoration: inherit;">Table<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The table where the data should be ingested. Optionally the table information can be added to each message.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="clustername_go">
<a href="#clustername_go" style="color: inherit; text-decoration: inherit;">Cluster<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Kusto cluster.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="consumergroup_go">
<a href="#consumergroup_go" style="color: inherit; text-decoration: inherit;">Consumer<wbr>Group</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The event hub consumer group.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="databasename_go">
<a href="#databasename_go" style="color: inherit; text-decoration: inherit;">Database<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the database in the Kusto cluster.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="eventhubresourceid_go">
<a href="#eventhubresourceid_go" style="color: inherit; text-decoration: inherit;">Event<wbr>Hub<wbr>Resource<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource ID of the event hub to be used to create a data connection.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group containing the Kusto cluster.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="dataformat_go">
<a href="#dataformat_go" style="color: inherit; text-decoration: inherit;">Data<wbr>Format</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string | <a href="#dataformat">Data<wbr>Format</a></span>
    </dt>
    <dd>{{% md %}}The data format of the message. Optionally the data format can be added to each message.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="eventhubconnectionname_go">
<a href="#eventhubconnectionname_go" style="color: inherit; text-decoration: inherit;">Event<wbr>Hub<wbr>Connection<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the event hub connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="location_go">
<a href="#location_go" style="color: inherit; text-decoration: inherit;">Location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource location.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="mappingrulename_go">
<a href="#mappingrulename_go" style="color: inherit; text-decoration: inherit;">Mapping<wbr>Rule<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The mapping rule to be used to ingest the data. Optionally the mapping information can be added to each message.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tablename_go">
<a href="#tablename_go" style="color: inherit; text-decoration: inherit;">Table<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The table where the data should be ingested. Optionally the table information can be added to each message.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="clustername_nodejs">
<a href="#clustername_nodejs" style="color: inherit; text-decoration: inherit;">cluster<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Kusto cluster.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="consumergroup_nodejs">
<a href="#consumergroup_nodejs" style="color: inherit; text-decoration: inherit;">consumer<wbr>Group</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The event hub consumer group.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="databasename_nodejs">
<a href="#databasename_nodejs" style="color: inherit; text-decoration: inherit;">database<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the database in the Kusto cluster.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="eventhubresourceid_nodejs">
<a href="#eventhubresourceid_nodejs" style="color: inherit; text-decoration: inherit;">event<wbr>Hub<wbr>Resource<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource ID of the event hub to be used to create a data connection.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group containing the Kusto cluster.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="dataformat_nodejs">
<a href="#dataformat_nodejs" style="color: inherit; text-decoration: inherit;">data<wbr>Format</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string | <a href="#dataformat">Data<wbr>Format</a></span>
    </dt>
    <dd>{{% md %}}The data format of the message. Optionally the data format can be added to each message.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="eventhubconnectionname_nodejs">
<a href="#eventhubconnectionname_nodejs" style="color: inherit; text-decoration: inherit;">event<wbr>Hub<wbr>Connection<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the event hub connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="location_nodejs">
<a href="#location_nodejs" style="color: inherit; text-decoration: inherit;">location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Resource location.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="mappingrulename_nodejs">
<a href="#mappingrulename_nodejs" style="color: inherit; text-decoration: inherit;">mapping<wbr>Rule<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The mapping rule to be used to ingest the data. Optionally the mapping information can be added to each message.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tablename_nodejs">
<a href="#tablename_nodejs" style="color: inherit; text-decoration: inherit;">table<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The table where the data should be ingested. Optionally the table information can be added to each message.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="cluster_name_python">
<a href="#cluster_name_python" style="color: inherit; text-decoration: inherit;">cluster_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the Kusto cluster.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="consumer_group_python">
<a href="#consumer_group_python" style="color: inherit; text-decoration: inherit;">consumer_<wbr>group</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The event hub consumer group.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="database_name_python">
<a href="#database_name_python" style="color: inherit; text-decoration: inherit;">database_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the database in the Kusto cluster.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="event_hub_resource_id_python">
<a href="#event_hub_resource_id_python" style="color: inherit; text-decoration: inherit;">event_<wbr>hub_<wbr>resource_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The resource ID of the event hub to be used to create a data connection.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource group containing the Kusto cluster.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="data_format_python">
<a href="#data_format_python" style="color: inherit; text-decoration: inherit;">data_<wbr>format</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str | <a href="#dataformat">Data<wbr>Format</a></span>
    </dt>
    <dd>{{% md %}}The data format of the message. Optionally the data format can be added to each message.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="event_hub_connection_name_python">
<a href="#event_hub_connection_name_python" style="color: inherit; text-decoration: inherit;">event_<wbr>hub_<wbr>connection_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the event hub connection.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="location_python">
<a href="#location_python" style="color: inherit; text-decoration: inherit;">location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Resource location.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="mapping_rule_name_python">
<a href="#mapping_rule_name_python" style="color: inherit; text-decoration: inherit;">mapping_<wbr>rule_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The mapping rule to be used to ingest the data. Optionally the mapping information can be added to each message.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="table_name_python">
<a href="#table_name_python" style="color: inherit; text-decoration: inherit;">table_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The table where the data should be ingested. Optionally the table information can be added to each message.{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the EventHubConnection resource produces the following output properties:



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
    <dd>{{% md %}}The name of the resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The name of the resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The name of the resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The name of the resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"{{% /md %}}</dd></dl>
{{% /choosable %}}







## Supporting Types



<h4 id="dataformat">Data<wbr>Format</h4>

{{% choosable language csharp %}}
<dl class="tabular"><dt>MULTIJSON</dt>
    <dd>MULTIJSON</dd><dt>JSON</dt>
    <dd>JSON</dd><dt>CSV</dt>
    <dd>CSV</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="tabular"><dt>Data<wbr>Format<wbr>MULTIJSON</dt>
    <dd>MULTIJSON</dd><dt>Data<wbr>Format<wbr>JSON</dt>
    <dd>JSON</dd><dt>Data<wbr>Format<wbr>CSV</dt>
    <dd>CSV</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="tabular"><dt>MULTIJSON</dt>
    <dd>MULTIJSON</dd><dt>JSON</dt>
    <dd>JSON</dd><dt>CSV</dt>
    <dd>CSV</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="tabular"><dt>MULTIJSON</dt>
    <dd>MULTIJSON</dd><dt>JSON</dt>
    <dd>JSON</dd><dt>CSV</dt>
    <dd>CSV</dd></dl>
{{% /choosable %}}
## Import


An existing resource can be imported using its type token, name, and identifier, e.g.

```sh
$ pulumi import azure-native:kusto:EventHubConnection KustoClusterRPTest4/KustoDatabase8 /subscriptions/12345678-1234-1234-1234-123456789098/resourceGroups/kustorptest/providers/Microsoft.Kusto/clusters/KustoClusterRPTest4/Databases/KustoDatabase8 
```




<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-native">https://github.com/pulumi/pulumi-azure-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>

