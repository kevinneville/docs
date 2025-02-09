
---
title: "getGateway"
title_tag: "equinix-metal.getGateway"
meta_desc: "Documentation for the equinix-metal.getGateway function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use this datasource to retrieve Metal Gateway resources in Equinix Metal.


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
        // Create Metal Gateway for a VLAN with a private IPv4 block with 8 IP addresses
        var testVlan = new EquinixMetal.Vlan("testVlan", new EquinixMetal.VlanArgs
        {
            Description = "test VLAN in SV",
            Metro = "sv",
            ProjectId = local.Project_id,
        });
        var testGateway = Output.Create(EquinixMetal.GetGateway.InvokeAsync(new EquinixMetal.GetGatewayArgs
        {
            GatewayId = local.Gateway_id,
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
		_, err := equinix - metal.NewVlan(ctx, "testVlan", &equinix-metal.VlanArgs{
			Description: pulumi.String("test VLAN in SV"),
			Metro:       pulumi.String("sv"),
			ProjectId:   pulumi.Any(local.Project_id),
		})
		if err != nil {
			return err
		}
		_, err = equinix - metal.LookupGateway(ctx, &equinix-metal.LookupGatewayArgs{
			GatewayId: local.Gateway_id,
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

# Create Metal Gateway for a VLAN with a private IPv4 block with 8 IP addresses
test_vlan = equinix_metal.Vlan("testVlan",
    description="test VLAN in SV",
    metro="sv",
    project_id=local["project_id"])
test_gateway = equinix_metal.get_gateway(gateway_id=local["gateway_id"])
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as equinix_metal from "@pulumi/equinix-metal";

// Create Metal Gateway for a VLAN with a private IPv4 block with 8 IP addresses
const testVlan = new equinix_metal.Vlan("testVlan", {
    description: "test VLAN in SV",
    metro: "sv",
    projectId: local.project_id,
});
const testGateway = equinix_metal.getGateway({
    gatewayId: local.gateway_id,
});
```


{{< /example >}}





{{% /examples %}}




## Using getGateway {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getGateway<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetGatewayArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetGatewayResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_gateway(</span><span class="nx">gateway_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetGatewayResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupGateway<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupGatewayArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupGatewayResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupGateway` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetGateway </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetGatewayResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetGatewayArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="gatewayid_csharp">
<a href="#gatewayid_csharp" style="color: inherit; text-decoration: inherit;">Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}UUID of the metal gateway resource to retrieve
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="gatewayid_go">
<a href="#gatewayid_go" style="color: inherit; text-decoration: inherit;">Gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}UUID of the metal gateway resource to retrieve
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="gatewayid_nodejs">
<a href="#gatewayid_nodejs" style="color: inherit; text-decoration: inherit;">gateway<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}UUID of the metal gateway resource to retrieve
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="gateway_id_python">
<a href="#gateway_id_python" style="color: inherit; text-decoration: inherit;">gateway_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}UUID of the metal gateway resource to retrieve
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getGateway Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="gatewayid_csharp">
<a href="#gatewayid_csharp" style="color: inherit; text-decoration: inherit;">Gateway<wbr>Id</a>
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
        <span id="ipreservationid_csharp">
<a href="#ipreservationid_csharp" style="color: inherit; text-decoration: inherit;">Ip<wbr>Reservation<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}UUID of IP reservation block bound to the gateway
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privateipv4subnetsize_csharp">
<a href="#privateipv4subnetsize_csharp" style="color: inherit; text-decoration: inherit;">Private<wbr>Ipv4Subnet<wbr>Size</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Size of the private IPv4 subnet bound to this metal gateway, one of (8, 16, 32, 64, 128)`
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="projectid_csharp">
<a href="#projectid_csharp" style="color: inherit; text-decoration: inherit;">Project<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}UUID of the project where the gateway is scoped to
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="state_csharp">
<a href="#state_csharp" style="color: inherit; text-decoration: inherit;">State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Status of the gateway resource
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="vlanid_csharp">
<a href="#vlanid_csharp" style="color: inherit; text-decoration: inherit;">Vlan<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}UUID of the VLAN where the gateway is scoped to
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="gatewayid_go">
<a href="#gatewayid_go" style="color: inherit; text-decoration: inherit;">Gateway<wbr>Id</a>
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
        <span id="ipreservationid_go">
<a href="#ipreservationid_go" style="color: inherit; text-decoration: inherit;">Ip<wbr>Reservation<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}UUID of IP reservation block bound to the gateway
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privateipv4subnetsize_go">
<a href="#privateipv4subnetsize_go" style="color: inherit; text-decoration: inherit;">Private<wbr>Ipv4Subnet<wbr>Size</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Size of the private IPv4 subnet bound to this metal gateway, one of (8, 16, 32, 64, 128)`
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="projectid_go">
<a href="#projectid_go" style="color: inherit; text-decoration: inherit;">Project<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}UUID of the project where the gateway is scoped to
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="state_go">
<a href="#state_go" style="color: inherit; text-decoration: inherit;">State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Status of the gateway resource
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="vlanid_go">
<a href="#vlanid_go" style="color: inherit; text-decoration: inherit;">Vlan<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}UUID of the VLAN where the gateway is scoped to
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="gatewayid_nodejs">
<a href="#gatewayid_nodejs" style="color: inherit; text-decoration: inherit;">gateway<wbr>Id</a>
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
        <span id="ipreservationid_nodejs">
<a href="#ipreservationid_nodejs" style="color: inherit; text-decoration: inherit;">ip<wbr>Reservation<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}UUID of IP reservation block bound to the gateway
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="privateipv4subnetsize_nodejs">
<a href="#privateipv4subnetsize_nodejs" style="color: inherit; text-decoration: inherit;">private<wbr>Ipv4Subnet<wbr>Size</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}Size of the private IPv4 subnet bound to this metal gateway, one of (8, 16, 32, 64, 128)`
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="projectid_nodejs">
<a href="#projectid_nodejs" style="color: inherit; text-decoration: inherit;">project<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}UUID of the project where the gateway is scoped to
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="state_nodejs">
<a href="#state_nodejs" style="color: inherit; text-decoration: inherit;">state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Status of the gateway resource
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="vlanid_nodejs">
<a href="#vlanid_nodejs" style="color: inherit; text-decoration: inherit;">vlan<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}UUID of the VLAN where the gateway is scoped to
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="gateway_id_python">
<a href="#gateway_id_python" style="color: inherit; text-decoration: inherit;">gateway_<wbr>id</a>
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
        <span id="ip_reservation_id_python">
<a href="#ip_reservation_id_python" style="color: inherit; text-decoration: inherit;">ip_<wbr>reservation_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}UUID of IP reservation block bound to the gateway
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="private_ipv4_subnet_size_python">
<a href="#private_ipv4_subnet_size_python" style="color: inherit; text-decoration: inherit;">private_<wbr>ipv4_<wbr>subnet_<wbr>size</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}Size of the private IPv4 subnet bound to this metal gateway, one of (8, 16, 32, 64, 128)`
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="project_id_python">
<a href="#project_id_python" style="color: inherit; text-decoration: inherit;">project_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}UUID of the project where the gateway is scoped to
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="state_python">
<a href="#state_python" style="color: inherit; text-decoration: inherit;">state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Status of the gateway resource
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="vlan_id_python">
<a href="#vlan_id_python" style="color: inherit; text-decoration: inherit;">vlan_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}UUID of the VLAN where the gateway is scoped to
{{% /md %}}</dd></dl>
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

