
---
title: "InstanceAccessControlAttributeConfiguration"
title_tag: "aws-native.sso.InstanceAccessControlAttributeConfiguration"
meta_desc: "Documentation for the aws-native.sso.InstanceAccessControlAttributeConfiguration resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Resource Type definition for SSO InstanceAccessControlAttributeConfiguration




## Create a InstanceAccessControlAttributeConfiguration Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">InstanceAccessControlAttributeConfiguration</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">InstanceAccessControlAttributeConfigurationArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">InstanceAccessControlAttributeConfiguration</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                                                <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                                                <span class="nx">access_control_attributes</span><span class="p">:</span> <span class="nx">Optional[Sequence[InstanceAccessControlAttributeConfigurationAccessControlAttributeArgs]]</span> = None<span class="p">,</span>
                                                <span class="nx">instance_access_control_attribute_configuration</span><span class="p">:</span> <span class="nx">Optional[Any]</span> = None<span class="p">,</span>
                                                <span class="nx">instance_arn</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">InstanceAccessControlAttributeConfiguration</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                                                <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">InstanceAccessControlAttributeConfigurationArgs</a></span><span class="p">,</span>
                                                <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewInstanceAccessControlAttributeConfiguration</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">InstanceAccessControlAttributeConfigurationArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">InstanceAccessControlAttributeConfiguration</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">InstanceAccessControlAttributeConfiguration</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">InstanceAccessControlAttributeConfigurationArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">InstanceAccessControlAttributeConfigurationArgs</a></span>
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
        <span class="property-type"><a href="#inputs">InstanceAccessControlAttributeConfigurationArgs</a></span>
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
        <span class="property-type"><a href="#inputs">InstanceAccessControlAttributeConfigurationArgs</a></span>
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
        <span class="property-type"><a href="#inputs">InstanceAccessControlAttributeConfigurationArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## InstanceAccessControlAttributeConfiguration Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The InstanceAccessControlAttributeConfiguration resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="instancearn_csharp">
<a href="#instancearn_csharp" style="color: inherit; text-decoration: inherit;">Instance<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the AWS SSO instance under which the operation will be executed.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="accesscontrolattributes_csharp">
<a href="#accesscontrolattributes_csharp" style="color: inherit; text-decoration: inherit;">Access<wbr>Control<wbr>Attributes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instanceaccesscontrolattributeconfigurationaccesscontrolattribute">List&lt;Pulumi.<wbr>Aws<wbr>Native.<wbr>SSO.<wbr>Inputs.<wbr>Instance<wbr>Access<wbr>Control<wbr>Attribute<wbr>Configuration<wbr>Access<wbr>Control<wbr>Attribute<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="instanceaccesscontrolattributeconfigurationvalue_csharp">
<a href="#instanceaccesscontrolattributeconfigurationvalue_csharp" style="color: inherit; text-decoration: inherit;">Instance<wbr>Access<wbr>Control<wbr>Attribute<wbr>Configuration<wbr>Value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">object</span>
    </dt>
    <dd>{{% md %}}The InstanceAccessControlAttributeConfiguration property has been deprecated but is still supported for backwards compatibility purposes. We recomend that you use  AccessControlAttributes property instead.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="instancearn_go">
<a href="#instancearn_go" style="color: inherit; text-decoration: inherit;">Instance<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the AWS SSO instance under which the operation will be executed.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="accesscontrolattributes_go">
<a href="#accesscontrolattributes_go" style="color: inherit; text-decoration: inherit;">Access<wbr>Control<wbr>Attributes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instanceaccesscontrolattributeconfigurationaccesscontrolattribute">[]Instance<wbr>Access<wbr>Control<wbr>Attribute<wbr>Configuration<wbr>Access<wbr>Control<wbr>Attribute<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="instanceaccesscontrolattributeconfiguration_go">
<a href="#instanceaccesscontrolattributeconfiguration_go" style="color: inherit; text-decoration: inherit;">Instance<wbr>Access<wbr>Control<wbr>Attribute<wbr>Configuration</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">interface{}</span>
    </dt>
    <dd>{{% md %}}The InstanceAccessControlAttributeConfiguration property has been deprecated but is still supported for backwards compatibility purposes. We recomend that you use  AccessControlAttributes property instead.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="instancearn_nodejs">
<a href="#instancearn_nodejs" style="color: inherit; text-decoration: inherit;">instance<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the AWS SSO instance under which the operation will be executed.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="accesscontrolattributes_nodejs">
<a href="#accesscontrolattributes_nodejs" style="color: inherit; text-decoration: inherit;">access<wbr>Control<wbr>Attributes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instanceaccesscontrolattributeconfigurationaccesscontrolattribute">Instance<wbr>Access<wbr>Control<wbr>Attribute<wbr>Configuration<wbr>Access<wbr>Control<wbr>Attribute<wbr>Args[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="instanceaccesscontrolattributeconfiguration_nodejs">
<a href="#instanceaccesscontrolattributeconfiguration_nodejs" style="color: inherit; text-decoration: inherit;">instance<wbr>Access<wbr>Control<wbr>Attribute<wbr>Configuration</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">any</span>
    </dt>
    <dd>{{% md %}}The InstanceAccessControlAttributeConfiguration property has been deprecated but is still supported for backwards compatibility purposes. We recomend that you use  AccessControlAttributes property instead.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="instance_arn_python">
<a href="#instance_arn_python" style="color: inherit; text-decoration: inherit;">instance_<wbr>arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the AWS SSO instance under which the operation will be executed.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="access_control_attributes_python">
<a href="#access_control_attributes_python" style="color: inherit; text-decoration: inherit;">access_<wbr>control_<wbr>attributes</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instanceaccesscontrolattributeconfigurationaccesscontrolattribute">Sequence[Instance<wbr>Access<wbr>Control<wbr>Attribute<wbr>Configuration<wbr>Access<wbr>Control<wbr>Attribute<wbr>Args]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="instance_access_control_attribute_configuration_python">
<a href="#instance_access_control_attribute_configuration_python" style="color: inherit; text-decoration: inherit;">instance_<wbr>access_<wbr>control_<wbr>attribute_<wbr>configuration</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Any</span>
    </dt>
    <dd>{{% md %}}The InstanceAccessControlAttributeConfiguration property has been deprecated but is still supported for backwards compatibility purposes. We recomend that you use  AccessControlAttributes property instead.{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the InstanceAccessControlAttributeConfiguration resource produces the following output properties:



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







## Supporting Types



<h4 id="instanceaccesscontrolattributeconfigurationaccesscontrolattribute">Instance<wbr>Access<wbr>Control<wbr>Attribute<wbr>Configuration<wbr>Access<wbr>Control<wbr>Attribute</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_csharp">
<a href="#key_csharp" style="color: inherit; text-decoration: inherit;">Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_csharp">
<a href="#value_csharp" style="color: inherit; text-decoration: inherit;">Value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instanceaccesscontrolattributeconfigurationaccesscontrolattributevalue">Pulumi.<wbr>Aws<wbr>Native.<wbr>SSO.<wbr>Inputs.<wbr>Instance<wbr>Access<wbr>Control<wbr>Attribute<wbr>Configuration<wbr>Access<wbr>Control<wbr>Attribute<wbr>Value</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_go">
<a href="#value_go" style="color: inherit; text-decoration: inherit;">Value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instanceaccesscontrolattributeconfigurationaccesscontrolattributevalue">Instance<wbr>Access<wbr>Control<wbr>Attribute<wbr>Configuration<wbr>Access<wbr>Control<wbr>Attribute<wbr>Value</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_nodejs">
<a href="#value_nodejs" style="color: inherit; text-decoration: inherit;">value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instanceaccesscontrolattributeconfigurationaccesscontrolattributevalue">Instance<wbr>Access<wbr>Control<wbr>Attribute<wbr>Configuration<wbr>Access<wbr>Control<wbr>Attribute<wbr>Value</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_python">
<a href="#value_python" style="color: inherit; text-decoration: inherit;">value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#instanceaccesscontrolattributeconfigurationaccesscontrolattributevalue">Instance<wbr>Access<wbr>Control<wbr>Attribute<wbr>Configuration<wbr>Access<wbr>Control<wbr>Attribute<wbr>Value</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="instanceaccesscontrolattributeconfigurationaccesscontrolattributevalue">Instance<wbr>Access<wbr>Control<wbr>Attribute<wbr>Configuration<wbr>Access<wbr>Control<wbr>Attribute<wbr>Value</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="source_csharp">
<a href="#source_csharp" style="color: inherit; text-decoration: inherit;">Source</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="source_go">
<a href="#source_go" style="color: inherit; text-decoration: inherit;">Source</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="source_nodejs">
<a href="#source_nodejs" style="color: inherit; text-decoration: inherit;">source</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="source_python">
<a href="#source_python" style="color: inherit; text-decoration: inherit;">source</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}


<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-aws-native">https://github.com/pulumi/pulumi-aws-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>

