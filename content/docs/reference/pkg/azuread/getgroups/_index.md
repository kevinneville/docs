
---
title: "getGroups"
title_tag: "azuread.getGroups"
meta_desc: "Documentation for the azuread.getGroups function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Gets Object IDs or Display Names for multiple Azure Active Directory groups.

## API Permissions

The following API permissions are required in order to use this data source.

When authenticated with a service principal, this data source requires one of the following application roles: `Group.Read.All` or `Directory.Read.All`

When authenticated with a user principal, this data source does not require any additional roles.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using AzureAD = Pulumi.AzureAD;

class MyStack : Stack
{
    public MyStack()
    {
        var example = Output.Create(AzureAD.GetGroups.InvokeAsync(new AzureAD.GetGroupsArgs
        {
            DisplayNames = 
            {
                "group-a",
                "group-b",
            },
        }));
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-azuread/sdk/v5/go/azuread"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := azuread.GetGroups(ctx, &GetGroupsArgs{
			DisplayNames: []string{
				"group-a",
				"group-b",
			},
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
import pulumi_azuread as azuread

example = azuread.get_groups(display_names=[
    "group-a",
    "group-b",
])
```


{{< /example >}}


{{< example typescript >}}

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azuread from "@pulumi/azuread";

const example = pulumi.output(azuread.getGroups({
    displayNames: [
        "group-a",
        "group-b",
    ],
}));
```


{{< /example >}}





{{% /examples %}}




## Using getGroups {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getGroups<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetGroupsArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetGroupsResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_groups(</span><span class="nx">display_names</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">,</span>
               <span class="nx">mail_enabled</span><span class="p">:</span> <span class="nx">Optional[bool]</span> = None<span class="p">,</span>
               <span class="nx">object_ids</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">,</span>
               <span class="nx">return_all</span><span class="p">:</span> <span class="nx">Optional[bool]</span> = None<span class="p">,</span>
               <span class="nx">security_enabled</span><span class="p">:</span> <span class="nx">Optional[bool]</span> = None<span class="p">,</span>
               <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetGroupsResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetGroups<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">GetGroupsArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetGroupsResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `GetGroups` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetGroups </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetGroupsResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetGroupsArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="displaynames_csharp">
<a href="#displaynames_csharp" style="color: inherit; text-decoration: inherit;">Display<wbr>Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}The display names of the groups.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="mailenabled_csharp">
<a href="#mailenabled_csharp" style="color: inherit; text-decoration: inherit;">Mail<wbr>Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the returned groups should be mail-enabled. By itself this does not exclude security-enabled groups. Setting this to `true` ensures all groups are mail-enabled, and setting to `false` ensures that all groups are _not_ mail-enabled. To ignore this filter, omit the property or set it to null. Cannot be specified together with `object_ids`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="objectids_csharp">
<a href="#objectids_csharp" style="color: inherit; text-decoration: inherit;">Object<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}The object IDs of the groups.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="returnall_csharp">
<a href="#returnall_csharp" style="color: inherit; text-decoration: inherit;">Return<wbr>All</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}A flag to denote if all groups should be fetched and returned.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="securityenabled_csharp">
<a href="#securityenabled_csharp" style="color: inherit; text-decoration: inherit;">Security<wbr>Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the returned groups should be security-enabled. By itself this does not exclude mail-enabled groups. Setting this to `true` ensures all groups are security-enabled, and setting to `false` ensures that all groups are _not_ security-enabled. To ignore this filter, omit the property or set it to null. Cannot be specified together with `object_ids`.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="displaynames_go">
<a href="#displaynames_go" style="color: inherit; text-decoration: inherit;">Display<wbr>Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The display names of the groups.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="mailenabled_go">
<a href="#mailenabled_go" style="color: inherit; text-decoration: inherit;">Mail<wbr>Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the returned groups should be mail-enabled. By itself this does not exclude security-enabled groups. Setting this to `true` ensures all groups are mail-enabled, and setting to `false` ensures that all groups are _not_ mail-enabled. To ignore this filter, omit the property or set it to null. Cannot be specified together with `object_ids`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="objectids_go">
<a href="#objectids_go" style="color: inherit; text-decoration: inherit;">Object<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The object IDs of the groups.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="returnall_go">
<a href="#returnall_go" style="color: inherit; text-decoration: inherit;">Return<wbr>All</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}A flag to denote if all groups should be fetched and returned.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="securityenabled_go">
<a href="#securityenabled_go" style="color: inherit; text-decoration: inherit;">Security<wbr>Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the returned groups should be security-enabled. By itself this does not exclude mail-enabled groups. Setting this to `true` ensures all groups are security-enabled, and setting to `false` ensures that all groups are _not_ security-enabled. To ignore this filter, omit the property or set it to null. Cannot be specified together with `object_ids`.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="displaynames_nodejs">
<a href="#displaynames_nodejs" style="color: inherit; text-decoration: inherit;">display<wbr>Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The display names of the groups.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="mailenabled_nodejs">
<a href="#mailenabled_nodejs" style="color: inherit; text-decoration: inherit;">mail<wbr>Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Whether the returned groups should be mail-enabled. By itself this does not exclude security-enabled groups. Setting this to `true` ensures all groups are mail-enabled, and setting to `false` ensures that all groups are _not_ mail-enabled. To ignore this filter, omit the property or set it to null. Cannot be specified together with `object_ids`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="objectids_nodejs">
<a href="#objectids_nodejs" style="color: inherit; text-decoration: inherit;">object<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The object IDs of the groups.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="returnall_nodejs">
<a href="#returnall_nodejs" style="color: inherit; text-decoration: inherit;">return<wbr>All</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}A flag to denote if all groups should be fetched and returned.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="securityenabled_nodejs">
<a href="#securityenabled_nodejs" style="color: inherit; text-decoration: inherit;">security<wbr>Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Whether the returned groups should be security-enabled. By itself this does not exclude mail-enabled groups. Setting this to `true` ensures all groups are security-enabled, and setting to `false` ensures that all groups are _not_ security-enabled. To ignore this filter, omit the property or set it to null. Cannot be specified together with `object_ids`.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="display_names_python">
<a href="#display_names_python" style="color: inherit; text-decoration: inherit;">display_<wbr>names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}The display names of the groups.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="mail_enabled_python">
<a href="#mail_enabled_python" style="color: inherit; text-decoration: inherit;">mail_<wbr>enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the returned groups should be mail-enabled. By itself this does not exclude security-enabled groups. Setting this to `true` ensures all groups are mail-enabled, and setting to `false` ensures that all groups are _not_ mail-enabled. To ignore this filter, omit the property or set it to null. Cannot be specified together with `object_ids`.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="object_ids_python">
<a href="#object_ids_python" style="color: inherit; text-decoration: inherit;">object_<wbr>ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}The object IDs of the groups.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="return_all_python">
<a href="#return_all_python" style="color: inherit; text-decoration: inherit;">return_<wbr>all</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}A flag to denote if all groups should be fetched and returned.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="security_enabled_python">
<a href="#security_enabled_python" style="color: inherit; text-decoration: inherit;">security_<wbr>enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether the returned groups should be security-enabled. By itself this does not exclude mail-enabled groups. Setting this to `true` ensures all groups are security-enabled, and setting to `false` ensures that all groups are _not_ security-enabled. To ignore this filter, omit the property or set it to null. Cannot be specified together with `object_ids`.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getGroups Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="displaynames_csharp">
<a href="#displaynames_csharp" style="color: inherit; text-decoration: inherit;">Display<wbr>Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}The display names of the groups.
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
        <span id="mailenabled_csharp">
<a href="#mailenabled_csharp" style="color: inherit; text-decoration: inherit;">Mail<wbr>Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="objectids_csharp">
<a href="#objectids_csharp" style="color: inherit; text-decoration: inherit;">Object<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}The object IDs of the groups.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="securityenabled_csharp">
<a href="#securityenabled_csharp" style="color: inherit; text-decoration: inherit;">Security<wbr>Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="returnall_csharp">
<a href="#returnall_csharp" style="color: inherit; text-decoration: inherit;">Return<wbr>All</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="displaynames_go">
<a href="#displaynames_go" style="color: inherit; text-decoration: inherit;">Display<wbr>Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The display names of the groups.
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
        <span id="mailenabled_go">
<a href="#mailenabled_go" style="color: inherit; text-decoration: inherit;">Mail<wbr>Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="objectids_go">
<a href="#objectids_go" style="color: inherit; text-decoration: inherit;">Object<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The object IDs of the groups.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="securityenabled_go">
<a href="#securityenabled_go" style="color: inherit; text-decoration: inherit;">Security<wbr>Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="returnall_go">
<a href="#returnall_go" style="color: inherit; text-decoration: inherit;">Return<wbr>All</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="displaynames_nodejs">
<a href="#displaynames_nodejs" style="color: inherit; text-decoration: inherit;">display<wbr>Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The display names of the groups.
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
        <span id="mailenabled_nodejs">
<a href="#mailenabled_nodejs" style="color: inherit; text-decoration: inherit;">mail<wbr>Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="objectids_nodejs">
<a href="#objectids_nodejs" style="color: inherit; text-decoration: inherit;">object<wbr>Ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The object IDs of the groups.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="securityenabled_nodejs">
<a href="#securityenabled_nodejs" style="color: inherit; text-decoration: inherit;">security<wbr>Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="returnall_nodejs">
<a href="#returnall_nodejs" style="color: inherit; text-decoration: inherit;">return<wbr>All</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="display_names_python">
<a href="#display_names_python" style="color: inherit; text-decoration: inherit;">display_<wbr>names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}The display names of the groups.
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
        <span id="mail_enabled_python">
<a href="#mail_enabled_python" style="color: inherit; text-decoration: inherit;">mail_<wbr>enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="object_ids_python">
<a href="#object_ids_python" style="color: inherit; text-decoration: inherit;">object_<wbr>ids</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}The object IDs of the groups.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="security_enabled_python">
<a href="#security_enabled_python" style="color: inherit; text-decoration: inherit;">security_<wbr>enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="return_all_python">
<a href="#return_all_python" style="color: inherit; text-decoration: inherit;">return_<wbr>all</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azuread">https://github.com/pulumi/pulumi-azuread</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`azuread` Terraform Provider](https://github.com/hashicorp/terraform-provider-azuread).{{% /md %}}</dd>
</dl>

