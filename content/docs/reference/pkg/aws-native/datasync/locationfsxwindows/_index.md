
---
title: "LocationFSxWindows"
title_tag: "aws-native.datasync.LocationFSxWindows"
meta_desc: "Documentation for the aws-native.datasync.LocationFSxWindows resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Resource schema for AWS::DataSync::LocationFSxWindows.




## Create a LocationFSxWindows Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">LocationFSxWindows</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">LocationFSxWindowsArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">LocationFSxWindows</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                       <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                       <span class="nx">domain</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                       <span class="nx">fsx_filesystem_arn</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                       <span class="nx">password</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                       <span class="nx">security_group_arns</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">,</span>
                       <span class="nx">subdirectory</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                       <span class="nx">tags</span><span class="p">:</span> <span class="nx">Optional[Sequence[LocationFSxWindowsTagArgs]]</span> = None<span class="p">,</span>
                       <span class="nx">user</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">LocationFSxWindows</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                       <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">LocationFSxWindowsArgs</a></span><span class="p">,</span>
                       <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewLocationFSxWindows</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">LocationFSxWindowsArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">LocationFSxWindows</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">LocationFSxWindows</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">LocationFSxWindowsArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">LocationFSxWindowsArgs</a></span>
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
        <span class="property-type"><a href="#inputs">LocationFSxWindowsArgs</a></span>
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
        <span class="property-type"><a href="#inputs">LocationFSxWindowsArgs</a></span>
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
        <span class="property-type"><a href="#inputs">LocationFSxWindowsArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## LocationFSxWindows Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The LocationFSxWindows resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="fsxfilesystemarn_csharp">
<a href="#fsxfilesystemarn_csharp" style="color: inherit; text-decoration: inherit;">Fsx<wbr>Filesystem<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) for the FSx for Windows file system.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="password_csharp">
<a href="#password_csharp" style="color: inherit; text-decoration: inherit;">Password</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of the user who has the permissions to access files and folders in the FSx for Windows file system.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="securitygrouparns_csharp">
<a href="#securitygrouparns_csharp" style="color: inherit; text-decoration: inherit;">Security<wbr>Group<wbr>Arns</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}The ARNs of the security groups that are to use to configure the FSx for Windows file system.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="user_csharp">
<a href="#user_csharp" style="color: inherit; text-decoration: inherit;">User</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The user who has the permissions to access files and folders in the FSx for Windows file system.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="domain_csharp">
<a href="#domain_csharp" style="color: inherit; text-decoration: inherit;">Domain</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Windows domain that the FSx for Windows server belongs to.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="subdirectory_csharp">
<a href="#subdirectory_csharp" style="color: inherit; text-decoration: inherit;">Subdirectory</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A subdirectory in the location's path.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#locationfsxwindowstag">List&lt;Pulumi.<wbr>Aws<wbr>Native.<wbr>Data<wbr>Sync.<wbr>Inputs.<wbr>Location<wbr>FSx<wbr>Windows<wbr>Tag<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}An array of key-value pairs to apply to this resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="fsxfilesystemarn_go">
<a href="#fsxfilesystemarn_go" style="color: inherit; text-decoration: inherit;">Fsx<wbr>Filesystem<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) for the FSx for Windows file system.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="password_go">
<a href="#password_go" style="color: inherit; text-decoration: inherit;">Password</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of the user who has the permissions to access files and folders in the FSx for Windows file system.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="securitygrouparns_go">
<a href="#securitygrouparns_go" style="color: inherit; text-decoration: inherit;">Security<wbr>Group<wbr>Arns</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The ARNs of the security groups that are to use to configure the FSx for Windows file system.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="user_go">
<a href="#user_go" style="color: inherit; text-decoration: inherit;">User</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The user who has the permissions to access files and folders in the FSx for Windows file system.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="domain_go">
<a href="#domain_go" style="color: inherit; text-decoration: inherit;">Domain</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Windows domain that the FSx for Windows server belongs to.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="subdirectory_go">
<a href="#subdirectory_go" style="color: inherit; text-decoration: inherit;">Subdirectory</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A subdirectory in the location's path.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#locationfsxwindowstag">[]Location<wbr>FSx<wbr>Windows<wbr>Tag<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}An array of key-value pairs to apply to this resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="fsxfilesystemarn_nodejs">
<a href="#fsxfilesystemarn_nodejs" style="color: inherit; text-decoration: inherit;">fsx<wbr>Filesystem<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) for the FSx for Windows file system.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="password_nodejs">
<a href="#password_nodejs" style="color: inherit; text-decoration: inherit;">password</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The password of the user who has the permissions to access files and folders in the FSx for Windows file system.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="securitygrouparns_nodejs">
<a href="#securitygrouparns_nodejs" style="color: inherit; text-decoration: inherit;">security<wbr>Group<wbr>Arns</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The ARNs of the security groups that are to use to configure the FSx for Windows file system.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="user_nodejs">
<a href="#user_nodejs" style="color: inherit; text-decoration: inherit;">user</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The user who has the permissions to access files and folders in the FSx for Windows file system.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="domain_nodejs">
<a href="#domain_nodejs" style="color: inherit; text-decoration: inherit;">domain</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Windows domain that the FSx for Windows server belongs to.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="subdirectory_nodejs">
<a href="#subdirectory_nodejs" style="color: inherit; text-decoration: inherit;">subdirectory</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A subdirectory in the location's path.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#locationfsxwindowstag">Location<wbr>FSx<wbr>Windows<wbr>Tag<wbr>Args[]</a></span>
    </dt>
    <dd>{{% md %}}An array of key-value pairs to apply to this resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="fsx_filesystem_arn_python">
<a href="#fsx_filesystem_arn_python" style="color: inherit; text-decoration: inherit;">fsx_<wbr>filesystem_<wbr>arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) for the FSx for Windows file system.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="password_python">
<a href="#password_python" style="color: inherit; text-decoration: inherit;">password</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The password of the user who has the permissions to access files and folders in the FSx for Windows file system.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="security_group_arns_python">
<a href="#security_group_arns_python" style="color: inherit; text-decoration: inherit;">security_<wbr>group_<wbr>arns</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}The ARNs of the security groups that are to use to configure the FSx for Windows file system.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="user_python">
<a href="#user_python" style="color: inherit; text-decoration: inherit;">user</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The user who has the permissions to access files and folders in the FSx for Windows file system.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="domain_python">
<a href="#domain_python" style="color: inherit; text-decoration: inherit;">domain</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the Windows domain that the FSx for Windows server belongs to.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="subdirectory_python">
<a href="#subdirectory_python" style="color: inherit; text-decoration: inherit;">subdirectory</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A subdirectory in the location's path.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#locationfsxwindowstag">Sequence[Location<wbr>FSx<wbr>Windows<wbr>Tag<wbr>Args]</a></span>
    </dt>
    <dd>{{% md %}}An array of key-value pairs to apply to this resource.{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the LocationFSxWindows resource produces the following output properties:



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
        <span id="locationarn_csharp">
<a href="#locationarn_csharp" style="color: inherit; text-decoration: inherit;">Location<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the Amazon FSx for Windows file system location that is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="locationuri_csharp">
<a href="#locationuri_csharp" style="color: inherit; text-decoration: inherit;">Location<wbr>Uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URL of the FSx for Windows location that was described.{{% /md %}}</dd></dl>
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
        <span id="locationarn_go">
<a href="#locationarn_go" style="color: inherit; text-decoration: inherit;">Location<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the Amazon FSx for Windows file system location that is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="locationuri_go">
<a href="#locationuri_go" style="color: inherit; text-decoration: inherit;">Location<wbr>Uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URL of the FSx for Windows location that was described.{{% /md %}}</dd></dl>
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
        <span id="locationarn_nodejs">
<a href="#locationarn_nodejs" style="color: inherit; text-decoration: inherit;">location<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the Amazon FSx for Windows file system location that is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="locationuri_nodejs">
<a href="#locationuri_nodejs" style="color: inherit; text-decoration: inherit;">location<wbr>Uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The URL of the FSx for Windows location that was described.{{% /md %}}</dd></dl>
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
        <span id="location_arn_python">
<a href="#location_arn_python" style="color: inherit; text-decoration: inherit;">location_<wbr>arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the Amazon FSx for Windows file system location that is created.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="location_uri_python">
<a href="#location_uri_python" style="color: inherit; text-decoration: inherit;">location_<wbr>uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The URL of the FSx for Windows location that was described.{{% /md %}}</dd></dl>
{{% /choosable %}}







## Supporting Types



<h4 id="locationfsxwindowstag">Location<wbr>FSx<wbr>Windows<wbr>Tag</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_csharp">
<a href="#key_csharp" style="color: inherit; text-decoration: inherit;">Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The key for an AWS resource tag.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_csharp">
<a href="#value_csharp" style="color: inherit; text-decoration: inherit;">Value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value for an AWS resource tag.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_go">
<a href="#key_go" style="color: inherit; text-decoration: inherit;">Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The key for an AWS resource tag.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_go">
<a href="#value_go" style="color: inherit; text-decoration: inherit;">Value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value for an AWS resource tag.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_nodejs">
<a href="#key_nodejs" style="color: inherit; text-decoration: inherit;">key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The key for an AWS resource tag.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_nodejs">
<a href="#value_nodejs" style="color: inherit; text-decoration: inherit;">value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value for an AWS resource tag.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_python">
<a href="#key_python" style="color: inherit; text-decoration: inherit;">key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The key for an AWS resource tag.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_python">
<a href="#value_python" style="color: inherit; text-decoration: inherit;">value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The value for an AWS resource tag.{{% /md %}}</dd></dl>
{{% /choosable %}}


<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-aws-native">https://github.com/pulumi/pulumi-aws-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>

