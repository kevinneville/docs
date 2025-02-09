
---
title: "getProjectSshKey"
title_tag: "equinix-metal.getProjectSshKey"
meta_desc: "Documentation for the equinix-metal.getProjectSshKey function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use this datasource to retrieve attributes of a Project SSH Key API resource.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using EquinixMetal = Pulumi.EquinixMetal;

class MyStack : Stack
{
    public MyStack()
    {
        var myKey = Output.Create(EquinixMetal.GetProjectSshKey.InvokeAsync(new EquinixMetal.GetProjectSshKeyArgs
        {
            Search = "username@hostname",
            ProjectId = local.Project_id,
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-equinix-metal/sdk/v3/go/equinix-metal"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		opt0 := "username@hostname"
		_, err := equinix - metal.LookupProjectSshKey(ctx, &equinix-metal.LookupProjectSshKeyArgs{
			Search:    &opt0,
			ProjectId: local.Project_id,
		}, nil)
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
import pulumi_equinix_metal as equinix_metal

my_key = equinix_metal.get_project_ssh_key(search="username@hostname",
    project_id=local["project_id"])
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as equinix_metal from "@pulumi/equinix-metal";

const myKey = equinix_metal.getProjectSshKey({
    search: "username@hostname",
    projectId: local.project_id,
});
```


{{< /example >}}





{{% /examples %}}




## Using getProjectSshKey {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getProjectSshKey<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetProjectSshKeyArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetProjectSshKeyResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_project_ssh_key(</span><span class="nx">id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                        <span class="nx">project_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                        <span class="nx">search</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetProjectSshKeyResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupProjectSshKey<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupProjectSshKeyArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupProjectSshKeyResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupProjectSshKey` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetProjectSshKey </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetProjectSshKeyResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetProjectSshKeyArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="projectid_csharp">
<a href="#projectid_csharp" style="color: inherit; text-decoration: inherit;">Project<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Equinix Metal project id of the Equinix Metal SSH Key
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The id of the SSH Key to search for in the Equinix Metal project
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="search_csharp">
<a href="#search_csharp" style="color: inherit; text-decoration: inherit;">Search</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name, fingerprint, or public_key of the SSH Key to search for
in the Equinix Metal project
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="projectid_go">
<a href="#projectid_go" style="color: inherit; text-decoration: inherit;">Project<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Equinix Metal project id of the Equinix Metal SSH Key
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The id of the SSH Key to search for in the Equinix Metal project
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="search_go">
<a href="#search_go" style="color: inherit; text-decoration: inherit;">Search</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name, fingerprint, or public_key of the SSH Key to search for
in the Equinix Metal project
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="projectid_nodejs">
<a href="#projectid_nodejs" style="color: inherit; text-decoration: inherit;">project<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Equinix Metal project id of the Equinix Metal SSH Key
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The id of the SSH Key to search for in the Equinix Metal project
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="search_nodejs">
<a href="#search_nodejs" style="color: inherit; text-decoration: inherit;">search</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name, fingerprint, or public_key of the SSH Key to search for
in the Equinix Metal project
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="project_id_python">
<a href="#project_id_python" style="color: inherit; text-decoration: inherit;">project_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Equinix Metal project id of the Equinix Metal SSH Key
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The id of the SSH Key to search for in the Equinix Metal project
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="search_python">
<a href="#search_python" style="color: inherit; text-decoration: inherit;">search</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name, fingerprint, or public_key of the SSH Key to search for
in the Equinix Metal project
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getProjectSshKey Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="created_csharp">
<a href="#created_csharp" style="color: inherit; text-decoration: inherit;">Created</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The timestamp for when the SSH key was created
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="fingerprint_csharp">
<a href="#fingerprint_csharp" style="color: inherit; text-decoration: inherit;">Fingerprint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The fingerprint of the SSH key
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique ID of the key
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the SSH key
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ownerid_csharp">
<a href="#ownerid_csharp" style="color: inherit; text-decoration: inherit;">Owner<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of parent project (same as project_id)
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="projectid_csharp">
<a href="#projectid_csharp" style="color: inherit; text-decoration: inherit;">Project<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of parent project
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="publickey_csharp">
<a href="#publickey_csharp" style="color: inherit; text-decoration: inherit;">Public<wbr>Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The text of the public key
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="updated_csharp">
<a href="#updated_csharp" style="color: inherit; text-decoration: inherit;">Updated</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The timestamp for the last time the SSH key was updated
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="search_csharp">
<a href="#search_csharp" style="color: inherit; text-decoration: inherit;">Search</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="created_go">
<a href="#created_go" style="color: inherit; text-decoration: inherit;">Created</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The timestamp for when the SSH key was created
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="fingerprint_go">
<a href="#fingerprint_go" style="color: inherit; text-decoration: inherit;">Fingerprint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The fingerprint of the SSH key
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique ID of the key
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the SSH key
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ownerid_go">
<a href="#ownerid_go" style="color: inherit; text-decoration: inherit;">Owner<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of parent project (same as project_id)
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="projectid_go">
<a href="#projectid_go" style="color: inherit; text-decoration: inherit;">Project<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of parent project
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="publickey_go">
<a href="#publickey_go" style="color: inherit; text-decoration: inherit;">Public<wbr>Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The text of the public key
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="updated_go">
<a href="#updated_go" style="color: inherit; text-decoration: inherit;">Updated</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The timestamp for the last time the SSH key was updated
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="search_go">
<a href="#search_go" style="color: inherit; text-decoration: inherit;">Search</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="created_nodejs">
<a href="#created_nodejs" style="color: inherit; text-decoration: inherit;">created</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The timestamp for when the SSH key was created
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="fingerprint_nodejs">
<a href="#fingerprint_nodejs" style="color: inherit; text-decoration: inherit;">fingerprint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The fingerprint of the SSH key
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique ID of the key
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the SSH key
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="ownerid_nodejs">
<a href="#ownerid_nodejs" style="color: inherit; text-decoration: inherit;">owner<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of parent project (same as project_id)
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="projectid_nodejs">
<a href="#projectid_nodejs" style="color: inherit; text-decoration: inherit;">project<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of parent project
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="publickey_nodejs">
<a href="#publickey_nodejs" style="color: inherit; text-decoration: inherit;">public<wbr>Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The text of the public key
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="updated_nodejs">
<a href="#updated_nodejs" style="color: inherit; text-decoration: inherit;">updated</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The timestamp for the last time the SSH key was updated
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="search_nodejs">
<a href="#search_nodejs" style="color: inherit; text-decoration: inherit;">search</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="created_python">
<a href="#created_python" style="color: inherit; text-decoration: inherit;">created</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The timestamp for when the SSH key was created
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="fingerprint_python">
<a href="#fingerprint_python" style="color: inherit; text-decoration: inherit;">fingerprint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The fingerprint of the SSH key
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The unique ID of the key
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the SSH key
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="owner_id_python">
<a href="#owner_id_python" style="color: inherit; text-decoration: inherit;">owner_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of parent project (same as project_id)
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="project_id_python">
<a href="#project_id_python" style="color: inherit; text-decoration: inherit;">project_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of parent project
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="public_key_python">
<a href="#public_key_python" style="color: inherit; text-decoration: inherit;">public_<wbr>key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The text of the public key
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="updated_python">
<a href="#updated_python" style="color: inherit; text-decoration: inherit;">updated</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The timestamp for the last time the SSH key was updated
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="search_python">
<a href="#search_python" style="color: inherit; text-decoration: inherit;">search</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-equinix-metal">https://github.com/pulumi/pulumi-equinix-metal</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`metal` Terraform Provider](https://github.com/equinix/terraform-provider-metal).{{% /md %}}</dd>
</dl>

