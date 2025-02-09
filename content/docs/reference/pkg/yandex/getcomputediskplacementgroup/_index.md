
---
title: "getComputeDiskPlacementGroup"
title_tag: "yandex.getComputeDiskPlacementGroup"
meta_desc: "Documentation for the yandex.getComputeDiskPlacementGroup function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Get information about a Yandex Compute Disk Placement group. For more information, see
[the official documentation](https://cloud.yandex.com/docs/compute/concepts/disk#nr-disks).


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
        var myGroup = Output.Create(Yandex.GetComputeDiskPlacementGroup.InvokeAsync(new Yandex.GetComputeDiskPlacementGroupArgs
        {
            GroupId = "some_group_id",
        }));
        this.PlacementGroupName = myGroup.Apply(myGroup => myGroup.Name);
    }

    [Output("placementGroupName")]
    public Output<string> PlacementGroupName { get; set; }
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
		opt0 := "some_group_id"
		myGroup, err := yandex.LookupComputeDiskPlacementGroup(ctx, &yandex.LookupComputeDiskPlacementGroupArgs{
			GroupId: &opt0,
		}, nil)
		if err != nil {
			return err
		}
		ctx.Export("placementGroupName", myGroup.Name)
		return nil
	})
}
```


{{< /example >}}


{{< example python >}}

```python
import pulumi
import pulumi_yandex as yandex

my_group = yandex.get_compute_disk_placement_group(group_id="some_group_id")
pulumi.export("placementGroupName", my_group.name)
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as yandex from "@pulumi/yandex";

const myGroup = pulumi.output(yandex.getComputeDiskPlacementGroup({
    groupId: "some_group_id",
}, { async: true }));

export const placementGroupName = myGroup.name!;
```


{{< /example >}}





{{% /examples %}}




## Using getComputeDiskPlacementGroup {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getComputeDiskPlacementGroup<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetComputeDiskPlacementGroupArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetComputeDiskPlacementGroupResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_compute_disk_placement_group(</span><span class="nx">description</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                     <span class="nx">folder_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                     <span class="nx">group_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                     <span class="nx">labels</span><span class="p">:</span> <span class="nx">Optional[Mapping[str, str]]</span> = None<span class="p">,</span>
                                     <span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                     <span class="nx">zone</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                     <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetComputeDiskPlacementGroupResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupComputeDiskPlacementGroup<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupComputeDiskPlacementGroupArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupComputeDiskPlacementGroupResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupComputeDiskPlacementGroup` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetComputeDiskPlacementGroup </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetComputeDiskPlacementGroupResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetComputeDiskPlacementGroupArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="description_csharp">
<a href="#description_csharp" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Description of the Disk Placement Group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="folderid_csharp">
<a href="#folderid_csharp" style="color: inherit; text-decoration: inherit;">Folder<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Folder that the resource belongs to. If value is omitted, the default provider folder is used.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="groupid_csharp">
<a href="#groupid_csharp" style="color: inherit; text-decoration: inherit;">Group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of a specific group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="labels_csharp">
<a href="#labels_csharp" style="color: inherit; text-decoration: inherit;">Labels</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}A set of key/value label pairs assigned to the Disk Placement Group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="zone_csharp">
<a href="#zone_csharp" style="color: inherit; text-decoration: inherit;">Zone</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the zone where the Disk Placement Group resides.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="description_go">
<a href="#description_go" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Description of the Disk Placement Group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="folderid_go">
<a href="#folderid_go" style="color: inherit; text-decoration: inherit;">Folder<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Folder that the resource belongs to. If value is omitted, the default provider folder is used.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="groupid_go">
<a href="#groupid_go" style="color: inherit; text-decoration: inherit;">Group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of a specific group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="labels_go">
<a href="#labels_go" style="color: inherit; text-decoration: inherit;">Labels</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}A set of key/value label pairs assigned to the Disk Placement Group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="zone_go">
<a href="#zone_go" style="color: inherit; text-decoration: inherit;">Zone</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the zone where the Disk Placement Group resides.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="description_nodejs">
<a href="#description_nodejs" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Description of the Disk Placement Group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="folderid_nodejs">
<a href="#folderid_nodejs" style="color: inherit; text-decoration: inherit;">folder<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Folder that the resource belongs to. If value is omitted, the default provider folder is used.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="groupid_nodejs">
<a href="#groupid_nodejs" style="color: inherit; text-decoration: inherit;">group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of a specific group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="labels_nodejs">
<a href="#labels_nodejs" style="color: inherit; text-decoration: inherit;">labels</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}A set of key/value label pairs assigned to the Disk Placement Group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Name of the group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="zone_nodejs">
<a href="#zone_nodejs" style="color: inherit; text-decoration: inherit;">zone</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the zone where the Disk Placement Group resides.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="description_python">
<a href="#description_python" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Description of the Disk Placement Group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="folder_id_python">
<a href="#folder_id_python" style="color: inherit; text-decoration: inherit;">folder_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Folder that the resource belongs to. If value is omitted, the default provider folder is used.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="group_id_python">
<a href="#group_id_python" style="color: inherit; text-decoration: inherit;">group_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of a specific group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="labels_python">
<a href="#labels_python" style="color: inherit; text-decoration: inherit;">labels</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}A set of key/value label pairs assigned to the Disk Placement Group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Name of the group.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="zone_python">
<a href="#zone_python" style="color: inherit; text-decoration: inherit;">zone</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the zone where the Disk Placement Group resides.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getComputeDiskPlacementGroup Result {#result}

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
    <dd>{{% md %}}The creation timestamp of the Disk Placement Group.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="folderid_csharp">
<a href="#folderid_csharp" style="color: inherit; text-decoration: inherit;">Folder<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="groupid_csharp">
<a href="#groupid_csharp" style="color: inherit; text-decoration: inherit;">Group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
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
        <span id="status_csharp">
<a href="#status_csharp" style="color: inherit; text-decoration: inherit;">Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Status of the Disk Placement Group.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_csharp">
<a href="#description_csharp" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Description of the Disk Placement Group.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="labels_csharp">
<a href="#labels_csharp" style="color: inherit; text-decoration: inherit;">Labels</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}A set of key/value label pairs assigned to the Disk Placement Group.
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
        <span id="zone_csharp">
<a href="#zone_csharp" style="color: inherit; text-decoration: inherit;">Zone</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the zone where the Disk Placement Group resides.
{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The creation timestamp of the Disk Placement Group.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="folderid_go">
<a href="#folderid_go" style="color: inherit; text-decoration: inherit;">Folder<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="groupid_go">
<a href="#groupid_go" style="color: inherit; text-decoration: inherit;">Group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
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
        <span id="status_go">
<a href="#status_go" style="color: inherit; text-decoration: inherit;">Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Status of the Disk Placement Group.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_go">
<a href="#description_go" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Description of the Disk Placement Group.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="labels_go">
<a href="#labels_go" style="color: inherit; text-decoration: inherit;">Labels</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}A set of key/value label pairs assigned to the Disk Placement Group.
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
        <span id="zone_go">
<a href="#zone_go" style="color: inherit; text-decoration: inherit;">Zone</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the zone where the Disk Placement Group resides.
{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The creation timestamp of the Disk Placement Group.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="folderid_nodejs">
<a href="#folderid_nodejs" style="color: inherit; text-decoration: inherit;">folder<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="groupid_nodejs">
<a href="#groupid_nodejs" style="color: inherit; text-decoration: inherit;">group<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
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
        <span id="status_nodejs">
<a href="#status_nodejs" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Status of the Disk Placement Group.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_nodejs">
<a href="#description_nodejs" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Description of the Disk Placement Group.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="labels_nodejs">
<a href="#labels_nodejs" style="color: inherit; text-decoration: inherit;">labels</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}A set of key/value label pairs assigned to the Disk Placement Group.
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
        <span id="zone_nodejs">
<a href="#zone_nodejs" style="color: inherit; text-decoration: inherit;">zone</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the zone where the Disk Placement Group resides.
{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The creation timestamp of the Disk Placement Group.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="folder_id_python">
<a href="#folder_id_python" style="color: inherit; text-decoration: inherit;">folder_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="group_id_python">
<a href="#group_id_python" style="color: inherit; text-decoration: inherit;">group_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
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
        <span id="status_python">
<a href="#status_python" style="color: inherit; text-decoration: inherit;">status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Status of the Disk Placement Group.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_python">
<a href="#description_python" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Description of the Disk Placement Group.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="labels_python">
<a href="#labels_python" style="color: inherit; text-decoration: inherit;">labels</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}A set of key/value label pairs assigned to the Disk Placement Group.
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
        <span id="zone_python">
<a href="#zone_python" style="color: inherit; text-decoration: inherit;">zone</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the zone where the Disk Placement Group resides.
{{% /md %}}</dd></dl>
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

