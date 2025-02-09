
---
title: "OrganizationConformancePack"
title_tag: "aws-native.configuration.OrganizationConformancePack"
meta_desc: "Documentation for the aws-native.configuration.OrganizationConformancePack resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Resource schema for AWS::Config::OrganizationConformancePack.




## Create a OrganizationConformancePack Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">OrganizationConformancePack</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">OrganizationConformancePackArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">OrganizationConformancePack</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                                <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                                <span class="nx">conformance_pack_input_parameters</span><span class="p">:</span> <span class="nx">Optional[Sequence[OrganizationConformancePackConformancePackInputParameterArgs]]</span> = None<span class="p">,</span>
                                <span class="nx">delivery_s3_bucket</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                <span class="nx">delivery_s3_key_prefix</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                <span class="nx">excluded_accounts</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">,</span>
                                <span class="nx">organization_conformance_pack_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                <span class="nx">template_body</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                <span class="nx">template_s3_uri</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">OrganizationConformancePack</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                                <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">OrganizationConformancePackArgs</a></span><span class="p">,</span>
                                <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewOrganizationConformancePack</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">OrganizationConformancePackArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">OrganizationConformancePack</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">OrganizationConformancePack</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">OrganizationConformancePackArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">OrganizationConformancePackArgs</a></span>
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
        <span class="property-type"><a href="#inputs">OrganizationConformancePackArgs</a></span>
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
        <span class="property-type"><a href="#inputs">OrganizationConformancePackArgs</a></span>
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
        <span class="property-type"><a href="#inputs">OrganizationConformancePackArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## OrganizationConformancePack Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The OrganizationConformancePack resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="organizationconformancepackname_csharp">
<a href="#organizationconformancepackname_csharp" style="color: inherit; text-decoration: inherit;">Organization<wbr>Conformance<wbr>Pack<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the organization conformance pack.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="conformancepackinputparameters_csharp">
<a href="#conformancepackinputparameters_csharp" style="color: inherit; text-decoration: inherit;">Conformance<wbr>Pack<wbr>Input<wbr>Parameters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#organizationconformancepackconformancepackinputparameter">List&lt;Pulumi.<wbr>Aws<wbr>Native.<wbr>Configuration.<wbr>Inputs.<wbr>Organization<wbr>Conformance<wbr>Pack<wbr>Conformance<wbr>Pack<wbr>Input<wbr>Parameter<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}A list of ConformancePackInputParameter objects.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="deliverys3bucket_csharp">
<a href="#deliverys3bucket_csharp" style="color: inherit; text-decoration: inherit;">Delivery<wbr>S3Bucket</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}AWS Config stores intermediate files while processing conformance pack template.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="deliverys3keyprefix_csharp">
<a href="#deliverys3keyprefix_csharp" style="color: inherit; text-decoration: inherit;">Delivery<wbr>S3Key<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The prefix for the delivery S3 bucket.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="excludedaccounts_csharp">
<a href="#excludedaccounts_csharp" style="color: inherit; text-decoration: inherit;">Excluded<wbr>Accounts</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of AWS accounts to be excluded from an organization conformance pack while deploying a conformance pack.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="templatebody_csharp">
<a href="#templatebody_csharp" style="color: inherit; text-decoration: inherit;">Template<wbr>Body</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string containing full conformance pack template body.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="templates3uri_csharp">
<a href="#templates3uri_csharp" style="color: inherit; text-decoration: inherit;">Template<wbr>S3Uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Location of file containing the template body.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="organizationconformancepackname_go">
<a href="#organizationconformancepackname_go" style="color: inherit; text-decoration: inherit;">Organization<wbr>Conformance<wbr>Pack<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the organization conformance pack.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="conformancepackinputparameters_go">
<a href="#conformancepackinputparameters_go" style="color: inherit; text-decoration: inherit;">Conformance<wbr>Pack<wbr>Input<wbr>Parameters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#organizationconformancepackconformancepackinputparameter">[]Organization<wbr>Conformance<wbr>Pack<wbr>Conformance<wbr>Pack<wbr>Input<wbr>Parameter<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}A list of ConformancePackInputParameter objects.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="deliverys3bucket_go">
<a href="#deliverys3bucket_go" style="color: inherit; text-decoration: inherit;">Delivery<wbr>S3Bucket</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}AWS Config stores intermediate files while processing conformance pack template.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="deliverys3keyprefix_go">
<a href="#deliverys3keyprefix_go" style="color: inherit; text-decoration: inherit;">Delivery<wbr>S3Key<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The prefix for the delivery S3 bucket.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="excludedaccounts_go">
<a href="#excludedaccounts_go" style="color: inherit; text-decoration: inherit;">Excluded<wbr>Accounts</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of AWS accounts to be excluded from an organization conformance pack while deploying a conformance pack.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="templatebody_go">
<a href="#templatebody_go" style="color: inherit; text-decoration: inherit;">Template<wbr>Body</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string containing full conformance pack template body.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="templates3uri_go">
<a href="#templates3uri_go" style="color: inherit; text-decoration: inherit;">Template<wbr>S3Uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Location of file containing the template body.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="organizationconformancepackname_nodejs">
<a href="#organizationconformancepackname_nodejs" style="color: inherit; text-decoration: inherit;">organization<wbr>Conformance<wbr>Pack<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the organization conformance pack.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="conformancepackinputparameters_nodejs">
<a href="#conformancepackinputparameters_nodejs" style="color: inherit; text-decoration: inherit;">conformance<wbr>Pack<wbr>Input<wbr>Parameters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#organizationconformancepackconformancepackinputparameter">Organization<wbr>Conformance<wbr>Pack<wbr>Conformance<wbr>Pack<wbr>Input<wbr>Parameter<wbr>Args[]</a></span>
    </dt>
    <dd>{{% md %}}A list of ConformancePackInputParameter objects.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="deliverys3bucket_nodejs">
<a href="#deliverys3bucket_nodejs" style="color: inherit; text-decoration: inherit;">delivery<wbr>S3Bucket</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}AWS Config stores intermediate files while processing conformance pack template.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="deliverys3keyprefix_nodejs">
<a href="#deliverys3keyprefix_nodejs" style="color: inherit; text-decoration: inherit;">delivery<wbr>S3Key<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The prefix for the delivery S3 bucket.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="excludedaccounts_nodejs">
<a href="#excludedaccounts_nodejs" style="color: inherit; text-decoration: inherit;">excluded<wbr>Accounts</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of AWS accounts to be excluded from an organization conformance pack while deploying a conformance pack.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="templatebody_nodejs">
<a href="#templatebody_nodejs" style="color: inherit; text-decoration: inherit;">template<wbr>Body</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string containing full conformance pack template body.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="templates3uri_nodejs">
<a href="#templates3uri_nodejs" style="color: inherit; text-decoration: inherit;">template<wbr>S3Uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Location of file containing the template body.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="organization_conformance_pack_name_python">
<a href="#organization_conformance_pack_name_python" style="color: inherit; text-decoration: inherit;">organization_<wbr>conformance_<wbr>pack_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the organization conformance pack.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="conformance_pack_input_parameters_python">
<a href="#conformance_pack_input_parameters_python" style="color: inherit; text-decoration: inherit;">conformance_<wbr>pack_<wbr>input_<wbr>parameters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#organizationconformancepackconformancepackinputparameter">Sequence[Organization<wbr>Conformance<wbr>Pack<wbr>Conformance<wbr>Pack<wbr>Input<wbr>Parameter<wbr>Args]</a></span>
    </dt>
    <dd>{{% md %}}A list of ConformancePackInputParameter objects.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="delivery_s3_bucket_python">
<a href="#delivery_s3_bucket_python" style="color: inherit; text-decoration: inherit;">delivery_<wbr>s3_<wbr>bucket</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}AWS Config stores intermediate files while processing conformance pack template.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="delivery_s3_key_prefix_python">
<a href="#delivery_s3_key_prefix_python" style="color: inherit; text-decoration: inherit;">delivery_<wbr>s3_<wbr>key_<wbr>prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The prefix for the delivery S3 bucket.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="excluded_accounts_python">
<a href="#excluded_accounts_python" style="color: inherit; text-decoration: inherit;">excluded_<wbr>accounts</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of AWS accounts to be excluded from an organization conformance pack while deploying a conformance pack.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="template_body_python">
<a href="#template_body_python" style="color: inherit; text-decoration: inherit;">template_<wbr>body</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A string containing full conformance pack template body.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="template_s3_uri_python">
<a href="#template_s3_uri_python" style="color: inherit; text-decoration: inherit;">template_<wbr>s3_<wbr>uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Location of file containing the template body.{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the OrganizationConformancePack resource produces the following output properties:



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



<h4 id="organizationconformancepackconformancepackinputparameter">Organization<wbr>Conformance<wbr>Pack<wbr>Conformance<wbr>Pack<wbr>Input<wbr>Parameter</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="parametername_csharp">
<a href="#parametername_csharp" style="color: inherit; text-decoration: inherit;">Parameter<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="parametervalue_csharp">
<a href="#parametervalue_csharp" style="color: inherit; text-decoration: inherit;">Parameter<wbr>Value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="parametername_go">
<a href="#parametername_go" style="color: inherit; text-decoration: inherit;">Parameter<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="parametervalue_go">
<a href="#parametervalue_go" style="color: inherit; text-decoration: inherit;">Parameter<wbr>Value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="parametername_nodejs">
<a href="#parametername_nodejs" style="color: inherit; text-decoration: inherit;">parameter<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="parametervalue_nodejs">
<a href="#parametervalue_nodejs" style="color: inherit; text-decoration: inherit;">parameter<wbr>Value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="parameter_name_python">
<a href="#parameter_name_python" style="color: inherit; text-decoration: inherit;">parameter_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="parameter_value_python">
<a href="#parameter_value_python" style="color: inherit; text-decoration: inherit;">parameter_<wbr>value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
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

