
---
title: "WorkspaceApplicationGroupAssociation"
title_tag: "azure.desktopvirtualization.WorkspaceApplicationGroupAssociation"
meta_desc: "Documentation for the azure.desktopvirtualization.WorkspaceApplicationGroupAssociation resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Manages a Virtual Desktop Workspace Application Group Association.

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
        var example = new Azure.Core.ResourceGroup("example", new Azure.Core.ResourceGroupArgs
        {
            Location = "West Europe",
        });
        var pooledbreadthfirst = new Azure.DesktopVirtualization.HostPool("pooledbreadthfirst", new Azure.DesktopVirtualization.HostPoolArgs
        {
            Location = example.Location,
            ResourceGroupName = example.Name,
            Type = "Pooled",
            LoadBalancerType = "BreadthFirst",
        });
        var remoteapp = new Azure.DesktopVirtualization.ApplicationGroup("remoteapp", new Azure.DesktopVirtualization.ApplicationGroupArgs
        {
            Location = example.Location,
            ResourceGroupName = example.Name,
            Type = "RemoteApp",
            HostPoolId = pooledbreadthfirst.Id,
        });
        var workspace = new Azure.DesktopVirtualization.Workspace("workspace", new Azure.DesktopVirtualization.WorkspaceArgs
        {
            Location = example.Location,
            ResourceGroupName = example.Name,
        });
        var workspaceremoteapp = new Azure.DesktopVirtualization.WorkspaceApplicationGroupAssociation("workspaceremoteapp", new Azure.DesktopVirtualization.WorkspaceApplicationGroupAssociationArgs
        {
            WorkspaceId = workspace.Id,
            ApplicationGroupId = remoteapp.Id,
        });
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-azure/sdk/v4/go/azure/core"
	"github.com/pulumi/pulumi-azure/sdk/v4/go/azure/desktopvirtualization"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		example, err := core.NewResourceGroup(ctx, "example", &core.ResourceGroupArgs{
			Location: pulumi.String("West Europe"),
		})
		if err != nil {
			return err
		}
		pooledbreadthfirst, err := desktopvirtualization.NewHostPool(ctx, "pooledbreadthfirst", &desktopvirtualization.HostPoolArgs{
			Location:          example.Location,
			ResourceGroupName: example.Name,
			Type:              pulumi.String("Pooled"),
			LoadBalancerType:  pulumi.String("BreadthFirst"),
		})
		if err != nil {
			return err
		}
		remoteapp, err := desktopvirtualization.NewApplicationGroup(ctx, "remoteapp", &desktopvirtualization.ApplicationGroupArgs{
			Location:          example.Location,
			ResourceGroupName: example.Name,
			Type:              pulumi.String("RemoteApp"),
			HostPoolId:        pooledbreadthfirst.ID(),
		})
		if err != nil {
			return err
		}
		workspace, err := desktopvirtualization.NewWorkspace(ctx, "workspace", &desktopvirtualization.WorkspaceArgs{
			Location:          example.Location,
			ResourceGroupName: example.Name,
		})
		if err != nil {
			return err
		}
		_, err = desktopvirtualization.NewWorkspaceApplicationGroupAssociation(ctx, "workspaceremoteapp", &desktopvirtualization.WorkspaceApplicationGroupAssociationArgs{
			WorkspaceId:        workspace.ID(),
			ApplicationGroupId: remoteapp.ID(),
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
import pulumi_azure as azure

example = azure.core.ResourceGroup("example", location="West Europe")
pooledbreadthfirst = azure.desktopvirtualization.HostPool("pooledbreadthfirst",
    location=example.location,
    resource_group_name=example.name,
    type="Pooled",
    load_balancer_type="BreadthFirst")
remoteapp = azure.desktopvirtualization.ApplicationGroup("remoteapp",
    location=example.location,
    resource_group_name=example.name,
    type="RemoteApp",
    host_pool_id=pooledbreadthfirst.id)
workspace = azure.desktopvirtualization.Workspace("workspace",
    location=example.location,
    resource_group_name=example.name)
workspaceremoteapp = azure.desktopvirtualization.WorkspaceApplicationGroupAssociation("workspaceremoteapp",
    workspace_id=workspace.id,
    application_group_id=remoteapp.id)
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure from "@pulumi/azure";

const example = new azure.core.ResourceGroup("example", {location: "West Europe"});
const pooledbreadthfirst = new azure.desktopvirtualization.HostPool("pooledbreadthfirst", {
    location: example.location,
    resourceGroupName: example.name,
    type: "Pooled",
    loadBalancerType: "BreadthFirst",
});
const remoteapp = new azure.desktopvirtualization.ApplicationGroup("remoteapp", {
    location: example.location,
    resourceGroupName: example.name,
    type: "RemoteApp",
    hostPoolId: pooledbreadthfirst.id,
});
const workspace = new azure.desktopvirtualization.Workspace("workspace", {
    location: example.location,
    resourceGroupName: example.name,
});
const workspaceremoteapp = new azure.desktopvirtualization.WorkspaceApplicationGroupAssociation("workspaceremoteapp", {
    workspaceId: workspace.id,
    applicationGroupId: remoteapp.id,
});
```


{{< /example >}}





{{% /examples %}}




## Create a WorkspaceApplicationGroupAssociation Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">WorkspaceApplicationGroupAssociation</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">WorkspaceApplicationGroupAssociationArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">WorkspaceApplicationGroupAssociation</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                                         <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                                         <span class="nx">application_group_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                         <span class="nx">workspace_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">WorkspaceApplicationGroupAssociation</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                                         <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">WorkspaceApplicationGroupAssociationArgs</a></span><span class="p">,</span>
                                         <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewWorkspaceApplicationGroupAssociation</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">WorkspaceApplicationGroupAssociationArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">WorkspaceApplicationGroupAssociation</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">WorkspaceApplicationGroupAssociation</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">WorkspaceApplicationGroupAssociationArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">WorkspaceApplicationGroupAssociationArgs</a></span>
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
        <span class="property-type"><a href="#inputs">WorkspaceApplicationGroupAssociationArgs</a></span>
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
        <span class="property-type"><a href="#inputs">WorkspaceApplicationGroupAssociationArgs</a></span>
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
        <span class="property-type"><a href="#inputs">WorkspaceApplicationGroupAssociationArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## WorkspaceApplicationGroupAssociation Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The WorkspaceApplicationGroupAssociation resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="applicationgroupid_csharp">
<a href="#applicationgroupid_csharp" style="color: inherit; text-decoration: inherit;">Application<wbr>Group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource ID for the Virtual Desktop Application Group.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="workspaceid_csharp">
<a href="#workspaceid_csharp" style="color: inherit; text-decoration: inherit;">Workspace<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource ID for the Virtual Desktop Workspace.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="applicationgroupid_go">
<a href="#applicationgroupid_go" style="color: inherit; text-decoration: inherit;">Application<wbr>Group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource ID for the Virtual Desktop Application Group.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="workspaceid_go">
<a href="#workspaceid_go" style="color: inherit; text-decoration: inherit;">Workspace<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource ID for the Virtual Desktop Workspace.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="applicationgroupid_nodejs">
<a href="#applicationgroupid_nodejs" style="color: inherit; text-decoration: inherit;">application<wbr>Group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource ID for the Virtual Desktop Application Group.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="workspaceid_nodejs">
<a href="#workspaceid_nodejs" style="color: inherit; text-decoration: inherit;">workspace<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource ID for the Virtual Desktop Workspace.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="application_group_id_python">
<a href="#application_group_id_python" style="color: inherit; text-decoration: inherit;">application_<wbr>group_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The resource ID for the Virtual Desktop Application Group.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="workspace_id_python">
<a href="#workspace_id_python" style="color: inherit; text-decoration: inherit;">workspace_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The resource ID for the Virtual Desktop Workspace.
{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the WorkspaceApplicationGroupAssociation resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}



## Look up an Existing WorkspaceApplicationGroupAssociation Resource {#look-up}

Get an existing WorkspaceApplicationGroupAssociation resource's state with the given name, ID, and optional extra properties used to qualify the lookup.
{{< chooser language "typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">,</span> <span class="nx">state</span><span class="p">?:</span> <span class="nx">WorkspaceApplicationGroupAssociationState</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx">WorkspaceApplicationGroupAssociation</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@staticmethod</span>
<span class="k">def </span><span class="nf">get</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">id</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
        <span class="nx">application_group_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">workspace_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">) -&gt;</span> WorkspaceApplicationGroupAssociation</code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetWorkspaceApplicationGroupAssociation<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p"> </span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">,</span> <span class="nx">state</span><span class="p"> *</span><span class="nx">WorkspaceApplicationGroupAssociationState</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">WorkspaceApplicationGroupAssociation</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx">WorkspaceApplicationGroupAssociation</span><span class="nf"> Get</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input-1.html">Input&lt;string&gt;</a></span><span class="p"> </span><span class="nx">id<span class="p">,</span> <span class="nx">WorkspaceApplicationGroupAssociationState</span><span class="p">? </span><span class="nx">state<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

The following state arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_applicationgroupid_csharp">
<a href="#state_applicationgroupid_csharp" style="color: inherit; text-decoration: inherit;">Application<wbr>Group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource ID for the Virtual Desktop Application Group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_workspaceid_csharp">
<a href="#state_workspaceid_csharp" style="color: inherit; text-decoration: inherit;">Workspace<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource ID for the Virtual Desktop Workspace.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_applicationgroupid_go">
<a href="#state_applicationgroupid_go" style="color: inherit; text-decoration: inherit;">Application<wbr>Group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource ID for the Virtual Desktop Application Group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_workspaceid_go">
<a href="#state_workspaceid_go" style="color: inherit; text-decoration: inherit;">Workspace<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource ID for the Virtual Desktop Workspace.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_applicationgroupid_nodejs">
<a href="#state_applicationgroupid_nodejs" style="color: inherit; text-decoration: inherit;">application<wbr>Group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource ID for the Virtual Desktop Application Group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_workspaceid_nodejs">
<a href="#state_workspaceid_nodejs" style="color: inherit; text-decoration: inherit;">workspace<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The resource ID for the Virtual Desktop Workspace.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_application_group_id_python">
<a href="#state_application_group_id_python" style="color: inherit; text-decoration: inherit;">application_<wbr>group_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The resource ID for the Virtual Desktop Application Group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_workspace_id_python">
<a href="#state_workspace_id_python" style="color: inherit; text-decoration: inherit;">workspace_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The resource ID for the Virtual Desktop Workspace.
{{% /md %}}</dd></dl>
{{% /choosable %}}





## Import


Associations between Virtual Desktop Workspaces and Virtual Desktop Application Groups can be imported using the `resource id`, e.g.

```sh
 $ pulumi import azure:desktopvirtualization/workspaceApplicationGroupAssociation:WorkspaceApplicationGroupAssociation association1 "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myGroup1/providers/Microsoft.DesktopVirtualization/workspaces/myworkspace|/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myGroup1/providers/Microsoft.DesktopVirtualization/applicationGroups/myapplicationgroup"
```




<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure">https://github.com/pulumi/pulumi-azure</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`azurerm` Terraform Provider](https://github.com/hashicorp/terraform-provider-azurerm).{{% /md %}}</dd>
</dl>

