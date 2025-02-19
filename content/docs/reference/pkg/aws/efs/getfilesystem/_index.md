
---
title: "getFileSystem"
title_tag: "aws.efs.getFileSystem"
meta_desc: "Documentation for the aws.efs.getFileSystem function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Provides information about an Elastic File System (EFS) File System.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Aws = Pulumi.Aws;

class MyStack : Stack
{
    public MyStack()
    {
        var config = new Config();
        var fileSystemId = config.Get("fileSystemId") ?? "";
        var byId = Output.Create(Aws.Efs.GetFileSystem.InvokeAsync(new Aws.Efs.GetFileSystemArgs
        {
            FileSystemId = fileSystemId,
        }));
        var byTag = Output.Create(Aws.Efs.GetFileSystem.InvokeAsync(new Aws.Efs.GetFileSystemArgs
        {
            Tags = 
            {
                { "Environment", "dev" },
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
	"github.com/pulumi/pulumi-aws/sdk/v4/go/aws/efs"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi/config"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		cfg := config.New(ctx, "")
		fileSystemId := ""
		if param := cfg.Get("fileSystemId"); param != "" {
			fileSystemId = param
		}
		opt0 := fileSystemId
		_, err := efs.LookupFileSystem(ctx, &efs.LookupFileSystemArgs{
			FileSystemId: &opt0,
		}, nil)
		if err != nil {
			return err
		}
		_, err = efs.LookupFileSystem(ctx, &efs.LookupFileSystemArgs{
			Tags: map[string]interface{}{
				"Environment": "dev",
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
import pulumi_aws as aws

config = pulumi.Config()
file_system_id = config.get("fileSystemId")
if file_system_id is None:
    file_system_id = ""
by_id = aws.efs.get_file_system(file_system_id=file_system_id)
by_tag = aws.efs.get_file_system(tags={
    "Environment": "dev",
})
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const config = new pulumi.Config();
const fileSystemId = config.get("fileSystemId") || "";
const byId = aws.efs.getFileSystem({
    fileSystemId: fileSystemId,
});
const byTag = aws.efs.getFileSystem({
    tags: {
        Environment: "dev",
    },
});
```


{{< /example >}}





{{% /examples %}}




## Using getFileSystem {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getFileSystem<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetFileSystemArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetFileSystemResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_file_system(</span><span class="nx">creation_token</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">file_system_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">tags</span><span class="p">:</span> <span class="nx">Optional[Mapping[str, str]]</span> = None<span class="p">,</span>
                    <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetFileSystemResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupFileSystem<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupFileSystemArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupFileSystemResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupFileSystem` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetFileSystem </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetFileSystemResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetFileSystemArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="creationtoken_csharp">
<a href="#creationtoken_csharp" style="color: inherit; text-decoration: inherit;">Creation<wbr>Token</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Restricts the list to the file system with this creation token.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="filesystemid_csharp">
<a href="#filesystemid_csharp" style="color: inherit; text-decoration: inherit;">File<wbr>System<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID that identifies the file system (e.g. fs-ccfc0d65).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}Restricts the list to the file system with these tags.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="creationtoken_go">
<a href="#creationtoken_go" style="color: inherit; text-decoration: inherit;">Creation<wbr>Token</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Restricts the list to the file system with this creation token.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="filesystemid_go">
<a href="#filesystemid_go" style="color: inherit; text-decoration: inherit;">File<wbr>System<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID that identifies the file system (e.g. fs-ccfc0d65).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}Restricts the list to the file system with these tags.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="creationtoken_nodejs">
<a href="#creationtoken_nodejs" style="color: inherit; text-decoration: inherit;">creation<wbr>Token</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Restricts the list to the file system with this creation token.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="filesystemid_nodejs">
<a href="#filesystemid_nodejs" style="color: inherit; text-decoration: inherit;">file<wbr>System<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID that identifies the file system (e.g. fs-ccfc0d65).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}Restricts the list to the file system with these tags.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="creation_token_python">
<a href="#creation_token_python" style="color: inherit; text-decoration: inherit;">creation_<wbr>token</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Restricts the list to the file system with this creation token.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="file_system_id_python">
<a href="#file_system_id_python" style="color: inherit; text-decoration: inherit;">file_<wbr>system_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID that identifies the file system (e.g. fs-ccfc0d65).
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}Restricts the list to the file system with these tags.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getFileSystem Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="arn_csharp">
<a href="#arn_csharp" style="color: inherit; text-decoration: inherit;">Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Amazon Resource Name of the file system.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availabilityzoneid_csharp">
<a href="#availabilityzoneid_csharp" style="color: inherit; text-decoration: inherit;">Availability<wbr>Zone<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The identifier of the Availability Zone in which the file system's One Zone storage classes exist.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availabilityzonename_csharp">
<a href="#availabilityzonename_csharp" style="color: inherit; text-decoration: inherit;">Availability<wbr>Zone<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Availability Zone name in which the file system's One Zone storage classes exist.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="creationtoken_csharp">
<a href="#creationtoken_csharp" style="color: inherit; text-decoration: inherit;">Creation<wbr>Token</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dnsname_csharp">
<a href="#dnsname_csharp" style="color: inherit; text-decoration: inherit;">Dns<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The DNS name for the filesystem per [documented convention](http://docs.aws.amazon.com/efs/latest/ug/mounting-fs-mount-cmd-dns-name.html).
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="encrypted_csharp">
<a href="#encrypted_csharp" style="color: inherit; text-decoration: inherit;">Encrypted</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether EFS is encrypted.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filesystemid_csharp">
<a href="#filesystemid_csharp" style="color: inherit; text-decoration: inherit;">File<wbr>System<wbr>Id</a>
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
        <span id="kmskeyid_csharp">
<a href="#kmskeyid_csharp" style="color: inherit; text-decoration: inherit;">Kms<wbr>Key<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN for the KMS encryption key.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lifecyclepolicy_csharp">
<a href="#lifecyclepolicy_csharp" style="color: inherit; text-decoration: inherit;">Lifecycle<wbr>Policy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getfilesystemlifecyclepolicy">Get<wbr>File<wbr>System<wbr>Lifecycle<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}A file system [lifecycle policy](https://docs.aws.amazon.com/efs/latest/ug/API_LifecyclePolicy.html) object.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="performancemode_csharp">
<a href="#performancemode_csharp" style="color: inherit; text-decoration: inherit;">Performance<wbr>Mode</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The file system performance mode.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisionedthroughputinmibps_csharp">
<a href="#provisionedthroughputinmibps_csharp" style="color: inherit; text-decoration: inherit;">Provisioned<wbr>Throughput<wbr>In<wbr>Mibps</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">double</span>
    </dt>
    <dd>{{% md %}}The throughput, measured in MiB/s, that you want to provision for the file system.
* `tags` -A map of tags to assign to the file system.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="sizeinbytes_csharp">
<a href="#sizeinbytes_csharp" style="color: inherit; text-decoration: inherit;">Size<wbr>In<wbr>Bytes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The current byte count used by the file system.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Dictionary&lt;string, string&gt;</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="throughputmode_csharp">
<a href="#throughputmode_csharp" style="color: inherit; text-decoration: inherit;">Throughput<wbr>Mode</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Throughput mode for the file system.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="arn_go">
<a href="#arn_go" style="color: inherit; text-decoration: inherit;">Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Amazon Resource Name of the file system.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availabilityzoneid_go">
<a href="#availabilityzoneid_go" style="color: inherit; text-decoration: inherit;">Availability<wbr>Zone<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The identifier of the Availability Zone in which the file system's One Zone storage classes exist.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availabilityzonename_go">
<a href="#availabilityzonename_go" style="color: inherit; text-decoration: inherit;">Availability<wbr>Zone<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Availability Zone name in which the file system's One Zone storage classes exist.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="creationtoken_go">
<a href="#creationtoken_go" style="color: inherit; text-decoration: inherit;">Creation<wbr>Token</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dnsname_go">
<a href="#dnsname_go" style="color: inherit; text-decoration: inherit;">Dns<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The DNS name for the filesystem per [documented convention](http://docs.aws.amazon.com/efs/latest/ug/mounting-fs-mount-cmd-dns-name.html).
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="encrypted_go">
<a href="#encrypted_go" style="color: inherit; text-decoration: inherit;">Encrypted</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether EFS is encrypted.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filesystemid_go">
<a href="#filesystemid_go" style="color: inherit; text-decoration: inherit;">File<wbr>System<wbr>Id</a>
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
        <span id="kmskeyid_go">
<a href="#kmskeyid_go" style="color: inherit; text-decoration: inherit;">Kms<wbr>Key<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN for the KMS encryption key.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lifecyclepolicy_go">
<a href="#lifecyclepolicy_go" style="color: inherit; text-decoration: inherit;">Lifecycle<wbr>Policy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getfilesystemlifecyclepolicy">Get<wbr>File<wbr>System<wbr>Lifecycle<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}A file system [lifecycle policy](https://docs.aws.amazon.com/efs/latest/ug/API_LifecyclePolicy.html) object.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="performancemode_go">
<a href="#performancemode_go" style="color: inherit; text-decoration: inherit;">Performance<wbr>Mode</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The file system performance mode.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisionedthroughputinmibps_go">
<a href="#provisionedthroughputinmibps_go" style="color: inherit; text-decoration: inherit;">Provisioned<wbr>Throughput<wbr>In<wbr>Mibps</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">float64</span>
    </dt>
    <dd>{{% md %}}The throughput, measured in MiB/s, that you want to provision for the file system.
* `tags` -A map of tags to assign to the file system.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="sizeinbytes_go">
<a href="#sizeinbytes_go" style="color: inherit; text-decoration: inherit;">Size<wbr>In<wbr>Bytes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The current byte count used by the file system.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">map[string]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="throughputmode_go">
<a href="#throughputmode_go" style="color: inherit; text-decoration: inherit;">Throughput<wbr>Mode</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Throughput mode for the file system.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="arn_nodejs">
<a href="#arn_nodejs" style="color: inherit; text-decoration: inherit;">arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Amazon Resource Name of the file system.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availabilityzoneid_nodejs">
<a href="#availabilityzoneid_nodejs" style="color: inherit; text-decoration: inherit;">availability<wbr>Zone<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The identifier of the Availability Zone in which the file system's One Zone storage classes exist.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availabilityzonename_nodejs">
<a href="#availabilityzonename_nodejs" style="color: inherit; text-decoration: inherit;">availability<wbr>Zone<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Availability Zone name in which the file system's One Zone storage classes exist.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="creationtoken_nodejs">
<a href="#creationtoken_nodejs" style="color: inherit; text-decoration: inherit;">creation<wbr>Token</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dnsname_nodejs">
<a href="#dnsname_nodejs" style="color: inherit; text-decoration: inherit;">dns<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The DNS name for the filesystem per [documented convention](http://docs.aws.amazon.com/efs/latest/ug/mounting-fs-mount-cmd-dns-name.html).
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="encrypted_nodejs">
<a href="#encrypted_nodejs" style="color: inherit; text-decoration: inherit;">encrypted</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Whether EFS is encrypted.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filesystemid_nodejs">
<a href="#filesystemid_nodejs" style="color: inherit; text-decoration: inherit;">file<wbr>System<wbr>Id</a>
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
        <span id="kmskeyid_nodejs">
<a href="#kmskeyid_nodejs" style="color: inherit; text-decoration: inherit;">kms<wbr>Key<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN for the KMS encryption key.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lifecyclepolicy_nodejs">
<a href="#lifecyclepolicy_nodejs" style="color: inherit; text-decoration: inherit;">lifecycle<wbr>Policy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getfilesystemlifecyclepolicy">Get<wbr>File<wbr>System<wbr>Lifecycle<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}A file system [lifecycle policy](https://docs.aws.amazon.com/efs/latest/ug/API_LifecyclePolicy.html) object.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="performancemode_nodejs">
<a href="#performancemode_nodejs" style="color: inherit; text-decoration: inherit;">performance<wbr>Mode</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The file system performance mode.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisionedthroughputinmibps_nodejs">
<a href="#provisionedthroughputinmibps_nodejs" style="color: inherit; text-decoration: inherit;">provisioned<wbr>Throughput<wbr>In<wbr>Mibps</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The throughput, measured in MiB/s, that you want to provision for the file system.
* `tags` -A map of tags to assign to the file system.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="sizeinbytes_nodejs">
<a href="#sizeinbytes_nodejs" style="color: inherit; text-decoration: inherit;">size<wbr>In<wbr>Bytes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The current byte count used by the file system.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">{[key: string]: string}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="throughputmode_nodejs">
<a href="#throughputmode_nodejs" style="color: inherit; text-decoration: inherit;">throughput<wbr>Mode</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Throughput mode for the file system.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="arn_python">
<a href="#arn_python" style="color: inherit; text-decoration: inherit;">arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Amazon Resource Name of the file system.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availability_zone_id_python">
<a href="#availability_zone_id_python" style="color: inherit; text-decoration: inherit;">availability_<wbr>zone_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The identifier of the Availability Zone in which the file system's One Zone storage classes exist.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="availability_zone_name_python">
<a href="#availability_zone_name_python" style="color: inherit; text-decoration: inherit;">availability_<wbr>zone_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Availability Zone name in which the file system's One Zone storage classes exist.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="creation_token_python">
<a href="#creation_token_python" style="color: inherit; text-decoration: inherit;">creation_<wbr>token</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="dns_name_python">
<a href="#dns_name_python" style="color: inherit; text-decoration: inherit;">dns_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The DNS name for the filesystem per [documented convention](http://docs.aws.amazon.com/efs/latest/ug/mounting-fs-mount-cmd-dns-name.html).
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="encrypted_python">
<a href="#encrypted_python" style="color: inherit; text-decoration: inherit;">encrypted</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Whether EFS is encrypted.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="file_system_id_python">
<a href="#file_system_id_python" style="color: inherit; text-decoration: inherit;">file_<wbr>system_<wbr>id</a>
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
        <span id="kms_key_id_python">
<a href="#kms_key_id_python" style="color: inherit; text-decoration: inherit;">kms_<wbr>key_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN for the KMS encryption key.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lifecycle_policy_python">
<a href="#lifecycle_policy_python" style="color: inherit; text-decoration: inherit;">lifecycle_<wbr>policy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getfilesystemlifecyclepolicy">Get<wbr>File<wbr>System<wbr>Lifecycle<wbr>Policy</a></span>
    </dt>
    <dd>{{% md %}}A file system [lifecycle policy](https://docs.aws.amazon.com/efs/latest/ug/API_LifecyclePolicy.html) object.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="performance_mode_python">
<a href="#performance_mode_python" style="color: inherit; text-decoration: inherit;">performance_<wbr>mode</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The file system performance mode.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="provisioned_throughput_in_mibps_python">
<a href="#provisioned_throughput_in_mibps_python" style="color: inherit; text-decoration: inherit;">provisioned_<wbr>throughput_<wbr>in_<wbr>mibps</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">float</span>
    </dt>
    <dd>{{% md %}}The throughput, measured in MiB/s, that you want to provision for the file system.
* `tags` -A map of tags to assign to the file system.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="size_in_bytes_python">
<a href="#size_in_bytes_python" style="color: inherit; text-decoration: inherit;">size_<wbr>in_<wbr>bytes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The current byte count used by the file system.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Mapping[str, str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="throughput_mode_python">
<a href="#throughput_mode_python" style="color: inherit; text-decoration: inherit;">throughput_<wbr>mode</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Throughput mode for the file system.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="getfilesystemlifecyclepolicy">Get<wbr>File<wbr>System<wbr>Lifecycle<wbr>Policy</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="transitiontoia_csharp">
<a href="#transitiontoia_csharp" style="color: inherit; text-decoration: inherit;">Transition<wbr>To<wbr>Ia</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="transitiontoprimarystorageclass_csharp">
<a href="#transitiontoprimarystorageclass_csharp" style="color: inherit; text-decoration: inherit;">Transition<wbr>To<wbr>Primary<wbr>Storage<wbr>Class</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="transitiontoia_go">
<a href="#transitiontoia_go" style="color: inherit; text-decoration: inherit;">Transition<wbr>To<wbr>Ia</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="transitiontoprimarystorageclass_go">
<a href="#transitiontoprimarystorageclass_go" style="color: inherit; text-decoration: inherit;">Transition<wbr>To<wbr>Primary<wbr>Storage<wbr>Class</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="transitiontoia_nodejs">
<a href="#transitiontoia_nodejs" style="color: inherit; text-decoration: inherit;">transition<wbr>To<wbr>Ia</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="transitiontoprimarystorageclass_nodejs">
<a href="#transitiontoprimarystorageclass_nodejs" style="color: inherit; text-decoration: inherit;">transition<wbr>To<wbr>Primary<wbr>Storage<wbr>Class</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="transition_to_ia_python">
<a href="#transition_to_ia_python" style="color: inherit; text-decoration: inherit;">transition_<wbr>to_<wbr>ia</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="transition_to_primary_storage_class_python">
<a href="#transition_to_primary_storage_class_python" style="color: inherit; text-decoration: inherit;">transition_<wbr>to_<wbr>primary_<wbr>storage_<wbr>class</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-aws">https://github.com/pulumi/pulumi-aws</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`aws` Terraform Provider](https://github.com/terraform-providers/terraform-provider-aws).{{% /md %}}</dd>
</dl>

