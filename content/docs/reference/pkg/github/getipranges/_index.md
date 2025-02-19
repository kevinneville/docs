
---
title: "getIpRanges"
title_tag: "github.getIpRanges"
meta_desc: "Documentation for the github.getIpRanges function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use this data source to retrieve information about GitHub's IP addresses.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Github = Pulumi.Github;

class MyStack : Stack
{
    public MyStack()
    {
        var test = Output.Create(Github.GetIpRanges.InvokeAsync());
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-github/sdk/v4/go/github"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := github.GetIpRanges(ctx, nil, nil)
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
import pulumi_github as github

test = github.get_ip_ranges()
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as github from "@pulumi/github";

const test = pulumi.output(github.getIpRanges());
```


{{< /example >}}





{{% /examples %}}




## Using getIpRanges {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getIpRanges<span class="p">(</span><span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetIpRangesResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_ip_ranges(</span><span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetIpRangesResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetIpRanges<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetIpRangesResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `GetIpRanges` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetIpRanges </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetIpRangesResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}




## getIpRanges Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="actions_csharp">
<a href="#actions_csharp" style="color: inherit; text-decoration: inherit;">Actions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}An array of IP addresses in CIDR format specifying the addresses that incoming requests from GitHub actions will originate from.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="actionsipv4s_csharp">
<a href="#actionsipv4s_csharp" style="color: inherit; text-decoration: inherit;">Actions<wbr>Ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A subset of the `actions` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="actionsipv6s_csharp">
<a href="#actionsipv6s_csharp" style="color: inherit; text-decoration: inherit;">Actions<wbr>Ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A subset of the `actions` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dependabotipv4s_csharp">
<a href="#dependabotipv4s_csharp" style="color: inherit; text-decoration: inherit;">Dependabot<wbr>Ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A subset of the `dependabot` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dependabotipv6s_csharp">
<a href="#dependabotipv6s_csharp" style="color: inherit; text-decoration: inherit;">Dependabot<wbr>Ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A subset of the `dependabot` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dependabots_csharp">
<a href="#dependabots_csharp" style="color: inherit; text-decoration: inherit;">Dependabots</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}An array of IP addresses in CIDR format specifying the A records for dependabot.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="gitipv4s_csharp">
<a href="#gitipv4s_csharp" style="color: inherit; text-decoration: inherit;">Git<wbr>Ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A subset of the `git` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="gitipv6s_csharp">
<a href="#gitipv6s_csharp" style="color: inherit; text-decoration: inherit;">Git<wbr>Ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A subset of the `git` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="gits_csharp">
<a href="#gits_csharp" style="color: inherit; text-decoration: inherit;">Gits</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}An Array of IP addresses in CIDR format specifying the Git servers.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hooks_csharp">
<a href="#hooks_csharp" style="color: inherit; text-decoration: inherit;">Hooks</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}An Array of IP addresses in CIDR format specifying the addresses that incoming service hooks will originate from.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hooksipv4s_csharp">
<a href="#hooksipv4s_csharp" style="color: inherit; text-decoration: inherit;">Hooks<wbr>Ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A subset of the `hooks` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hooksipv6s_csharp">
<a href="#hooksipv6s_csharp" style="color: inherit; text-decoration: inherit;">Hooks<wbr>Ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A subset of the `hooks` array that contains IP addresses in IPv6 CIDR format.
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
        <span id="importeripv4s_csharp">
<a href="#importeripv4s_csharp" style="color: inherit; text-decoration: inherit;">Importer<wbr>Ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A subset of the `importer` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="importeripv6s_csharp">
<a href="#importeripv6s_csharp" style="color: inherit; text-decoration: inherit;">Importer<wbr>Ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A subset of the `importer` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="importers_csharp">
<a href="#importers_csharp" style="color: inherit; text-decoration: inherit;">Importers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}An Array of IP addresses in CIDR format specifying the A records for GitHub Importer.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="pages_csharp">
<a href="#pages_csharp" style="color: inherit; text-decoration: inherit;">Pages</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}An Array of IP addresses in CIDR format specifying the A records for GitHub Pages.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="pagesipv4s_csharp">
<a href="#pagesipv4s_csharp" style="color: inherit; text-decoration: inherit;">Pages<wbr>Ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A subset of the `pages` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="pagesipv6s_csharp">
<a href="#pagesipv6s_csharp" style="color: inherit; text-decoration: inherit;">Pages<wbr>Ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A subset of the `pages` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="actions_go">
<a href="#actions_go" style="color: inherit; text-decoration: inherit;">Actions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}An array of IP addresses in CIDR format specifying the addresses that incoming requests from GitHub actions will originate from.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="actionsipv4s_go">
<a href="#actionsipv4s_go" style="color: inherit; text-decoration: inherit;">Actions<wbr>Ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A subset of the `actions` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="actionsipv6s_go">
<a href="#actionsipv6s_go" style="color: inherit; text-decoration: inherit;">Actions<wbr>Ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A subset of the `actions` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dependabotipv4s_go">
<a href="#dependabotipv4s_go" style="color: inherit; text-decoration: inherit;">Dependabot<wbr>Ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A subset of the `dependabot` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dependabotipv6s_go">
<a href="#dependabotipv6s_go" style="color: inherit; text-decoration: inherit;">Dependabot<wbr>Ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A subset of the `dependabot` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dependabots_go">
<a href="#dependabots_go" style="color: inherit; text-decoration: inherit;">Dependabots</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}An array of IP addresses in CIDR format specifying the A records for dependabot.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="gitipv4s_go">
<a href="#gitipv4s_go" style="color: inherit; text-decoration: inherit;">Git<wbr>Ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A subset of the `git` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="gitipv6s_go">
<a href="#gitipv6s_go" style="color: inherit; text-decoration: inherit;">Git<wbr>Ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A subset of the `git` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="gits_go">
<a href="#gits_go" style="color: inherit; text-decoration: inherit;">Gits</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}An Array of IP addresses in CIDR format specifying the Git servers.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hooks_go">
<a href="#hooks_go" style="color: inherit; text-decoration: inherit;">Hooks</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}An Array of IP addresses in CIDR format specifying the addresses that incoming service hooks will originate from.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hooksipv4s_go">
<a href="#hooksipv4s_go" style="color: inherit; text-decoration: inherit;">Hooks<wbr>Ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A subset of the `hooks` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hooksipv6s_go">
<a href="#hooksipv6s_go" style="color: inherit; text-decoration: inherit;">Hooks<wbr>Ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A subset of the `hooks` array that contains IP addresses in IPv6 CIDR format.
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
        <span id="importeripv4s_go">
<a href="#importeripv4s_go" style="color: inherit; text-decoration: inherit;">Importer<wbr>Ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A subset of the `importer` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="importeripv6s_go">
<a href="#importeripv6s_go" style="color: inherit; text-decoration: inherit;">Importer<wbr>Ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A subset of the `importer` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="importers_go">
<a href="#importers_go" style="color: inherit; text-decoration: inherit;">Importers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}An Array of IP addresses in CIDR format specifying the A records for GitHub Importer.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="pages_go">
<a href="#pages_go" style="color: inherit; text-decoration: inherit;">Pages</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}An Array of IP addresses in CIDR format specifying the A records for GitHub Pages.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="pagesipv4s_go">
<a href="#pagesipv4s_go" style="color: inherit; text-decoration: inherit;">Pages<wbr>Ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A subset of the `pages` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="pagesipv6s_go">
<a href="#pagesipv6s_go" style="color: inherit; text-decoration: inherit;">Pages<wbr>Ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A subset of the `pages` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="actions_nodejs">
<a href="#actions_nodejs" style="color: inherit; text-decoration: inherit;">actions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}An array of IP addresses in CIDR format specifying the addresses that incoming requests from GitHub actions will originate from.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="actionsipv4s_nodejs">
<a href="#actionsipv4s_nodejs" style="color: inherit; text-decoration: inherit;">actions<wbr>Ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A subset of the `actions` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="actionsipv6s_nodejs">
<a href="#actionsipv6s_nodejs" style="color: inherit; text-decoration: inherit;">actions<wbr>Ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A subset of the `actions` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dependabotipv4s_nodejs">
<a href="#dependabotipv4s_nodejs" style="color: inherit; text-decoration: inherit;">dependabot<wbr>Ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A subset of the `dependabot` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dependabotipv6s_nodejs">
<a href="#dependabotipv6s_nodejs" style="color: inherit; text-decoration: inherit;">dependabot<wbr>Ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A subset of the `dependabot` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dependabots_nodejs">
<a href="#dependabots_nodejs" style="color: inherit; text-decoration: inherit;">dependabots</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}An array of IP addresses in CIDR format specifying the A records for dependabot.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="gitipv4s_nodejs">
<a href="#gitipv4s_nodejs" style="color: inherit; text-decoration: inherit;">git<wbr>Ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A subset of the `git` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="gitipv6s_nodejs">
<a href="#gitipv6s_nodejs" style="color: inherit; text-decoration: inherit;">git<wbr>Ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A subset of the `git` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="gits_nodejs">
<a href="#gits_nodejs" style="color: inherit; text-decoration: inherit;">gits</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}An Array of IP addresses in CIDR format specifying the Git servers.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hooks_nodejs">
<a href="#hooks_nodejs" style="color: inherit; text-decoration: inherit;">hooks</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}An Array of IP addresses in CIDR format specifying the addresses that incoming service hooks will originate from.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hooksipv4s_nodejs">
<a href="#hooksipv4s_nodejs" style="color: inherit; text-decoration: inherit;">hooks<wbr>Ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A subset of the `hooks` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hooksipv6s_nodejs">
<a href="#hooksipv6s_nodejs" style="color: inherit; text-decoration: inherit;">hooks<wbr>Ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A subset of the `hooks` array that contains IP addresses in IPv6 CIDR format.
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
        <span id="importeripv4s_nodejs">
<a href="#importeripv4s_nodejs" style="color: inherit; text-decoration: inherit;">importer<wbr>Ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A subset of the `importer` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="importeripv6s_nodejs">
<a href="#importeripv6s_nodejs" style="color: inherit; text-decoration: inherit;">importer<wbr>Ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A subset of the `importer` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="importers_nodejs">
<a href="#importers_nodejs" style="color: inherit; text-decoration: inherit;">importers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}An Array of IP addresses in CIDR format specifying the A records for GitHub Importer.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="pages_nodejs">
<a href="#pages_nodejs" style="color: inherit; text-decoration: inherit;">pages</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}An Array of IP addresses in CIDR format specifying the A records for GitHub Pages.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="pagesipv4s_nodejs">
<a href="#pagesipv4s_nodejs" style="color: inherit; text-decoration: inherit;">pages<wbr>Ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A subset of the `pages` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="pagesipv6s_nodejs">
<a href="#pagesipv6s_nodejs" style="color: inherit; text-decoration: inherit;">pages<wbr>Ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A subset of the `pages` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="actions_python">
<a href="#actions_python" style="color: inherit; text-decoration: inherit;">actions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}An array of IP addresses in CIDR format specifying the addresses that incoming requests from GitHub actions will originate from.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="actions_ipv4s_python">
<a href="#actions_ipv4s_python" style="color: inherit; text-decoration: inherit;">actions_<wbr>ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A subset of the `actions` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="actions_ipv6s_python">
<a href="#actions_ipv6s_python" style="color: inherit; text-decoration: inherit;">actions_<wbr>ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A subset of the `actions` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dependabot_ipv4s_python">
<a href="#dependabot_ipv4s_python" style="color: inherit; text-decoration: inherit;">dependabot_<wbr>ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A subset of the `dependabot` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dependabot_ipv6s_python">
<a href="#dependabot_ipv6s_python" style="color: inherit; text-decoration: inherit;">dependabot_<wbr>ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A subset of the `dependabot` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dependabots_python">
<a href="#dependabots_python" style="color: inherit; text-decoration: inherit;">dependabots</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}An array of IP addresses in CIDR format specifying the A records for dependabot.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="git_ipv4s_python">
<a href="#git_ipv4s_python" style="color: inherit; text-decoration: inherit;">git_<wbr>ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A subset of the `git` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="git_ipv6s_python">
<a href="#git_ipv6s_python" style="color: inherit; text-decoration: inherit;">git_<wbr>ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A subset of the `git` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="gits_python">
<a href="#gits_python" style="color: inherit; text-decoration: inherit;">gits</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}An Array of IP addresses in CIDR format specifying the Git servers.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hooks_python">
<a href="#hooks_python" style="color: inherit; text-decoration: inherit;">hooks</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}An Array of IP addresses in CIDR format specifying the addresses that incoming service hooks will originate from.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hooks_ipv4s_python">
<a href="#hooks_ipv4s_python" style="color: inherit; text-decoration: inherit;">hooks_<wbr>ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A subset of the `hooks` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hooks_ipv6s_python">
<a href="#hooks_ipv6s_python" style="color: inherit; text-decoration: inherit;">hooks_<wbr>ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A subset of the `hooks` array that contains IP addresses in IPv6 CIDR format.
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
        <span id="importer_ipv4s_python">
<a href="#importer_ipv4s_python" style="color: inherit; text-decoration: inherit;">importer_<wbr>ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A subset of the `importer` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="importer_ipv6s_python">
<a href="#importer_ipv6s_python" style="color: inherit; text-decoration: inherit;">importer_<wbr>ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A subset of the `importer` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="importers_python">
<a href="#importers_python" style="color: inherit; text-decoration: inherit;">importers</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}An Array of IP addresses in CIDR format specifying the A records for GitHub Importer.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="pages_python">
<a href="#pages_python" style="color: inherit; text-decoration: inherit;">pages</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}An Array of IP addresses in CIDR format specifying the A records for GitHub Pages.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="pages_ipv4s_python">
<a href="#pages_ipv4s_python" style="color: inherit; text-decoration: inherit;">pages_<wbr>ipv4s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A subset of the `pages` array that contains IP addresses in IPv4 CIDR format.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="pages_ipv6s_python">
<a href="#pages_ipv6s_python" style="color: inherit; text-decoration: inherit;">pages_<wbr>ipv6s</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A subset of the `pages` array that contains IP addresses in IPv6 CIDR format.
{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-github">https://github.com/pulumi/pulumi-github</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`github` Terraform Provider](https://github.com/terraform-providers/terraform-provider-github).{{% /md %}}</dd>
</dl>

