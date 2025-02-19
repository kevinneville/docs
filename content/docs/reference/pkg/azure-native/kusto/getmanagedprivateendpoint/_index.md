
---
title: "getManagedPrivateEndpoint"
title_tag: "azure-native.kusto.getManagedPrivateEndpoint"
meta_desc: "Documentation for the azure-native.kusto.getManagedPrivateEndpoint function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Class representing a managed private endpoint.
API Version: 2021-08-27.




## Using getManagedPrivateEndpoint {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getManagedPrivateEndpoint<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetManagedPrivateEndpointArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetManagedPrivateEndpointResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_managed_private_endpoint(</span><span class="nx">cluster_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                 <span class="nx">managed_private_endpoint_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                 <span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                 <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetManagedPrivateEndpointResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupManagedPrivateEndpoint<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupManagedPrivateEndpointArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupManagedPrivateEndpointResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupManagedPrivateEndpoint` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetManagedPrivateEndpoint </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetManagedPrivateEndpointResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetManagedPrivateEndpointArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


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
        <span id="managedprivateendpointname_csharp">
<a href="#managedprivateendpointname_csharp" style="color: inherit; text-decoration: inherit;">Managed<wbr>Private<wbr>Endpoint<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the managed private endpoint.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group containing the Kusto cluster.{{% /md %}}</dd></dl>
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
        <span id="managedprivateendpointname_go">
<a href="#managedprivateendpointname_go" style="color: inherit; text-decoration: inherit;">Managed<wbr>Private<wbr>Endpoint<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the managed private endpoint.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group containing the Kusto cluster.{{% /md %}}</dd></dl>
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
        <span id="managedprivateendpointname_nodejs">
<a href="#managedprivateendpointname_nodejs" style="color: inherit; text-decoration: inherit;">managed<wbr>Private<wbr>Endpoint<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the managed private endpoint.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group containing the Kusto cluster.{{% /md %}}</dd></dl>
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
        <span id="managed_private_endpoint_name_python">
<a href="#managed_private_endpoint_name_python" style="color: inherit; text-decoration: inherit;">managed_<wbr>private_<wbr>endpoint_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the managed private endpoint.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource group containing the Kusto cluster.{{% /md %}}</dd></dl>
{{% /choosable %}}




## getManagedPrivateEndpoint Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="groupid_csharp">
<a href="#groupid_csharp" style="color: inherit; text-decoration: inherit;">Group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The groupId in which the managed private endpoint is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privatelinkresourceid_csharp">
<a href="#privatelinkresourceid_csharp" style="color: inherit; text-decoration: inherit;">Private<wbr>Link<wbr>Resource<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARM resource ID of the resource for which the managed private endpoint is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioningstate_csharp">
<a href="#provisioningstate_csharp" style="color: inherit; text-decoration: inherit;">Provisioning<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provisioned state of the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="systemdata_csharp">
<a href="#systemdata_csharp" style="color: inherit; text-decoration: inherit;">System<wbr>Data</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#systemdataresponse">Pulumi.<wbr>Azure<wbr>Native.<wbr>Kusto.<wbr>Outputs.<wbr>System<wbr>Data<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Metadata pertaining to creation and last modification of the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privatelinkresourceregion_csharp">
<a href="#privatelinkresourceregion_csharp" style="color: inherit; text-decoration: inherit;">Private<wbr>Link<wbr>Resource<wbr>Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region of the resource to which the managed private endpoint is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="requestmessage_csharp">
<a href="#requestmessage_csharp" style="color: inherit; text-decoration: inherit;">Request<wbr>Message</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The user request message.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="groupid_go">
<a href="#groupid_go" style="color: inherit; text-decoration: inherit;">Group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The groupId in which the managed private endpoint is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privatelinkresourceid_go">
<a href="#privatelinkresourceid_go" style="color: inherit; text-decoration: inherit;">Private<wbr>Link<wbr>Resource<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARM resource ID of the resource for which the managed private endpoint is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioningstate_go">
<a href="#provisioningstate_go" style="color: inherit; text-decoration: inherit;">Provisioning<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provisioned state of the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="systemdata_go">
<a href="#systemdata_go" style="color: inherit; text-decoration: inherit;">System<wbr>Data</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#systemdataresponse">System<wbr>Data<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Metadata pertaining to creation and last modification of the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privatelinkresourceregion_go">
<a href="#privatelinkresourceregion_go" style="color: inherit; text-decoration: inherit;">Private<wbr>Link<wbr>Resource<wbr>Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region of the resource to which the managed private endpoint is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="requestmessage_go">
<a href="#requestmessage_go" style="color: inherit; text-decoration: inherit;">Request<wbr>Message</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The user request message.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="groupid_nodejs">
<a href="#groupid_nodejs" style="color: inherit; text-decoration: inherit;">group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The groupId in which the managed private endpoint is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privatelinkresourceid_nodejs">
<a href="#privatelinkresourceid_nodejs" style="color: inherit; text-decoration: inherit;">private<wbr>Link<wbr>Resource<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARM resource ID of the resource for which the managed private endpoint is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioningstate_nodejs">
<a href="#provisioningstate_nodejs" style="color: inherit; text-decoration: inherit;">provisioning<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provisioned state of the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="systemdata_nodejs">
<a href="#systemdata_nodejs" style="color: inherit; text-decoration: inherit;">system<wbr>Data</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#systemdataresponse">System<wbr>Data<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Metadata pertaining to creation and last modification of the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privatelinkresourceregion_nodejs">
<a href="#privatelinkresourceregion_nodejs" style="color: inherit; text-decoration: inherit;">private<wbr>Link<wbr>Resource<wbr>Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The region of the resource to which the managed private endpoint is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="requestmessage_nodejs">
<a href="#requestmessage_nodejs" style="color: inherit; text-decoration: inherit;">request<wbr>Message</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The user request message.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="group_id_python">
<a href="#group_id_python" style="color: inherit; text-decoration: inherit;">group_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The groupId in which the managed private endpoint is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Fully qualified resource ID for the resource. Ex - /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/{resourceProviderNamespace}/{resourceType}/{resourceName}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="private_link_resource_id_python">
<a href="#private_link_resource_id_python" style="color: inherit; text-decoration: inherit;">private_<wbr>link_<wbr>resource_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARM resource ID of the resource for which the managed private endpoint is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioning_state_python">
<a href="#provisioning_state_python" style="color: inherit; text-decoration: inherit;">provisioning_<wbr>state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provisioned state of the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="system_data_python">
<a href="#system_data_python" style="color: inherit; text-decoration: inherit;">system_<wbr>data</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#systemdataresponse">System<wbr>Data<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Metadata pertaining to creation and last modification of the resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of the resource. E.g. "Microsoft.Compute/virtualMachines" or "Microsoft.Storage/storageAccounts"{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="private_link_resource_region_python">
<a href="#private_link_resource_region_python" style="color: inherit; text-decoration: inherit;">private_<wbr>link_<wbr>resource_<wbr>region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The region of the resource to which the managed private endpoint is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="request_message_python">
<a href="#request_message_python" style="color: inherit; text-decoration: inherit;">request_<wbr>message</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The user request message.{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="systemdataresponse">System<wbr>Data<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="createdat_csharp">
<a href="#createdat_csharp" style="color: inherit; text-decoration: inherit;">Created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The timestamp of resource creation (UTC).{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="createdby_csharp">
<a href="#createdby_csharp" style="color: inherit; text-decoration: inherit;">Created<wbr>By</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The identity that created the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="createdbytype_csharp">
<a href="#createdbytype_csharp" style="color: inherit; text-decoration: inherit;">Created<wbr>By<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of identity that created the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="lastmodifiedat_csharp">
<a href="#lastmodifiedat_csharp" style="color: inherit; text-decoration: inherit;">Last<wbr>Modified<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The timestamp of resource last modification (UTC){{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="lastmodifiedby_csharp">
<a href="#lastmodifiedby_csharp" style="color: inherit; text-decoration: inherit;">Last<wbr>Modified<wbr>By</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The identity that last modified the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="lastmodifiedbytype_csharp">
<a href="#lastmodifiedbytype_csharp" style="color: inherit; text-decoration: inherit;">Last<wbr>Modified<wbr>By<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of identity that last modified the resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="createdat_go">
<a href="#createdat_go" style="color: inherit; text-decoration: inherit;">Created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The timestamp of resource creation (UTC).{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="createdby_go">
<a href="#createdby_go" style="color: inherit; text-decoration: inherit;">Created<wbr>By</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The identity that created the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="createdbytype_go">
<a href="#createdbytype_go" style="color: inherit; text-decoration: inherit;">Created<wbr>By<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of identity that created the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="lastmodifiedat_go">
<a href="#lastmodifiedat_go" style="color: inherit; text-decoration: inherit;">Last<wbr>Modified<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The timestamp of resource last modification (UTC){{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="lastmodifiedby_go">
<a href="#lastmodifiedby_go" style="color: inherit; text-decoration: inherit;">Last<wbr>Modified<wbr>By</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The identity that last modified the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="lastmodifiedbytype_go">
<a href="#lastmodifiedbytype_go" style="color: inherit; text-decoration: inherit;">Last<wbr>Modified<wbr>By<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of identity that last modified the resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="createdat_nodejs">
<a href="#createdat_nodejs" style="color: inherit; text-decoration: inherit;">created<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The timestamp of resource creation (UTC).{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="createdby_nodejs">
<a href="#createdby_nodejs" style="color: inherit; text-decoration: inherit;">created<wbr>By</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The identity that created the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="createdbytype_nodejs">
<a href="#createdbytype_nodejs" style="color: inherit; text-decoration: inherit;">created<wbr>By<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of identity that created the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="lastmodifiedat_nodejs">
<a href="#lastmodifiedat_nodejs" style="color: inherit; text-decoration: inherit;">last<wbr>Modified<wbr>At</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The timestamp of resource last modification (UTC){{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="lastmodifiedby_nodejs">
<a href="#lastmodifiedby_nodejs" style="color: inherit; text-decoration: inherit;">last<wbr>Modified<wbr>By</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The identity that last modified the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="lastmodifiedbytype_nodejs">
<a href="#lastmodifiedbytype_nodejs" style="color: inherit; text-decoration: inherit;">last<wbr>Modified<wbr>By<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of identity that last modified the resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="created_at_python">
<a href="#created_at_python" style="color: inherit; text-decoration: inherit;">created_<wbr>at</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The timestamp of resource creation (UTC).{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="created_by_python">
<a href="#created_by_python" style="color: inherit; text-decoration: inherit;">created_<wbr>by</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The identity that created the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="created_by_type_python">
<a href="#created_by_type_python" style="color: inherit; text-decoration: inherit;">created_<wbr>by_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of identity that created the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="last_modified_at_python">
<a href="#last_modified_at_python" style="color: inherit; text-decoration: inherit;">last_<wbr>modified_<wbr>at</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The timestamp of resource last modification (UTC){{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="last_modified_by_python">
<a href="#last_modified_by_python" style="color: inherit; text-decoration: inherit;">last_<wbr>modified_<wbr>by</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The identity that last modified the resource.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="last_modified_by_type_python">
<a href="#last_modified_by_type_python" style="color: inherit; text-decoration: inherit;">last_<wbr>modified_<wbr>by_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of identity that last modified the resource.{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-native">https://github.com/pulumi/pulumi-azure-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>

