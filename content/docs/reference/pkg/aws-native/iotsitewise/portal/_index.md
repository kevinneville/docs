
---
title: "Portal"
title_tag: "aws-native.iotsitewise.Portal"
meta_desc: "Documentation for the aws-native.iotsitewise.Portal resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Resource schema for AWS::IoTSiteWise::Portal




## Create a Portal Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">Portal</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">PortalArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Portal</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
           <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
           <span class="nx">alarms</span><span class="p">:</span> <span class="nx">Optional[Any]</span> = None<span class="p">,</span>
           <span class="nx">notification_sender_email</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
           <span class="nx">portal_auth_mode</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
           <span class="nx">portal_contact_email</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
           <span class="nx">portal_description</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
           <span class="nx">portal_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
           <span class="nx">role_arn</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
           <span class="nx">tags</span><span class="p">:</span> <span class="nx">Optional[Sequence[PortalTagArgs]]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Portal</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
           <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">PortalArgs</a></span><span class="p">,</span>
           <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewPortal</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">PortalArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">Portal</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">Portal</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">PortalArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">PortalArgs</a></span>
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
        <span class="property-type"><a href="#inputs">PortalArgs</a></span>
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
        <span class="property-type"><a href="#inputs">PortalArgs</a></span>
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
        <span class="property-type"><a href="#inputs">PortalArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## Portal Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The Portal resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="portalcontactemail_csharp">
<a href="#portalcontactemail_csharp" style="color: inherit; text-decoration: inherit;">Portal<wbr>Contact<wbr>Email</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The AWS administrator's contact email address.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="portalname_csharp">
<a href="#portalname_csharp" style="color: inherit; text-decoration: inherit;">Portal<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A friendly name for the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rolearn_csharp">
<a href="#rolearn_csharp" style="color: inherit; text-decoration: inherit;">Role<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of a service role that allows the portal's users to access your AWS IoT SiteWise resources on your behalf.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="alarms_csharp">
<a href="#alarms_csharp" style="color: inherit; text-decoration: inherit;">Alarms</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">object</span>
    </dt>
    <dd>{{% md %}}Contains the configuration information of an alarm created in an AWS IoT SiteWise Monitor portal. You can use the alarm to monitor an asset property and get notified when the asset property value is outside a specified range.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="notificationsenderemail_csharp">
<a href="#notificationsenderemail_csharp" style="color: inherit; text-decoration: inherit;">Notification<wbr>Sender<wbr>Email</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The email address that sends alarm notifications.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="portalauthmode_csharp">
<a href="#portalauthmode_csharp" style="color: inherit; text-decoration: inherit;">Portal<wbr>Auth<wbr>Mode</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The service to use to authenticate users to the portal. Choose from SSO or IAM. You can't change this value after you create a portal.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="portaldescription_csharp">
<a href="#portaldescription_csharp" style="color: inherit; text-decoration: inherit;">Portal<wbr>Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A description for the portal.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portaltag">List&lt;Pulumi.<wbr>Aws<wbr>Native.<wbr>Io<wbr>TSite<wbr>Wise.<wbr>Inputs.<wbr>Portal<wbr>Tag<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}A list of key-value pairs that contain metadata for the portal.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="portalcontactemail_go">
<a href="#portalcontactemail_go" style="color: inherit; text-decoration: inherit;">Portal<wbr>Contact<wbr>Email</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The AWS administrator's contact email address.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="portalname_go">
<a href="#portalname_go" style="color: inherit; text-decoration: inherit;">Portal<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A friendly name for the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rolearn_go">
<a href="#rolearn_go" style="color: inherit; text-decoration: inherit;">Role<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of a service role that allows the portal's users to access your AWS IoT SiteWise resources on your behalf.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="alarms_go">
<a href="#alarms_go" style="color: inherit; text-decoration: inherit;">Alarms</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">interface{}</span>
    </dt>
    <dd>{{% md %}}Contains the configuration information of an alarm created in an AWS IoT SiteWise Monitor portal. You can use the alarm to monitor an asset property and get notified when the asset property value is outside a specified range.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="notificationsenderemail_go">
<a href="#notificationsenderemail_go" style="color: inherit; text-decoration: inherit;">Notification<wbr>Sender<wbr>Email</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The email address that sends alarm notifications.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="portalauthmode_go">
<a href="#portalauthmode_go" style="color: inherit; text-decoration: inherit;">Portal<wbr>Auth<wbr>Mode</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The service to use to authenticate users to the portal. Choose from SSO or IAM. You can't change this value after you create a portal.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="portaldescription_go">
<a href="#portaldescription_go" style="color: inherit; text-decoration: inherit;">Portal<wbr>Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A description for the portal.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portaltag">[]Portal<wbr>Tag<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}A list of key-value pairs that contain metadata for the portal.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="portalcontactemail_nodejs">
<a href="#portalcontactemail_nodejs" style="color: inherit; text-decoration: inherit;">portal<wbr>Contact<wbr>Email</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The AWS administrator's contact email address.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="portalname_nodejs">
<a href="#portalname_nodejs" style="color: inherit; text-decoration: inherit;">portal<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A friendly name for the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rolearn_nodejs">
<a href="#rolearn_nodejs" style="color: inherit; text-decoration: inherit;">role<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of a service role that allows the portal's users to access your AWS IoT SiteWise resources on your behalf.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="alarms_nodejs">
<a href="#alarms_nodejs" style="color: inherit; text-decoration: inherit;">alarms</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">any</span>
    </dt>
    <dd>{{% md %}}Contains the configuration information of an alarm created in an AWS IoT SiteWise Monitor portal. You can use the alarm to monitor an asset property and get notified when the asset property value is outside a specified range.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="notificationsenderemail_nodejs">
<a href="#notificationsenderemail_nodejs" style="color: inherit; text-decoration: inherit;">notification<wbr>Sender<wbr>Email</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The email address that sends alarm notifications.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="portalauthmode_nodejs">
<a href="#portalauthmode_nodejs" style="color: inherit; text-decoration: inherit;">portal<wbr>Auth<wbr>Mode</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The service to use to authenticate users to the portal. Choose from SSO or IAM. You can't change this value after you create a portal.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="portaldescription_nodejs">
<a href="#portaldescription_nodejs" style="color: inherit; text-decoration: inherit;">portal<wbr>Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A description for the portal.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portaltag">Portal<wbr>Tag<wbr>Args[]</a></span>
    </dt>
    <dd>{{% md %}}A list of key-value pairs that contain metadata for the portal.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="portal_contact_email_python">
<a href="#portal_contact_email_python" style="color: inherit; text-decoration: inherit;">portal_<wbr>contact_<wbr>email</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The AWS administrator's contact email address.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="portal_name_python">
<a href="#portal_name_python" style="color: inherit; text-decoration: inherit;">portal_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A friendly name for the portal.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="role_arn_python">
<a href="#role_arn_python" style="color: inherit; text-decoration: inherit;">role_<wbr>arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of a service role that allows the portal's users to access your AWS IoT SiteWise resources on your behalf.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="alarms_python">
<a href="#alarms_python" style="color: inherit; text-decoration: inherit;">alarms</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Any</span>
    </dt>
    <dd>{{% md %}}Contains the configuration information of an alarm created in an AWS IoT SiteWise Monitor portal. You can use the alarm to monitor an asset property and get notified when the asset property value is outside a specified range.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="notification_sender_email_python">
<a href="#notification_sender_email_python" style="color: inherit; text-decoration: inherit;">notification_<wbr>sender_<wbr>email</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The email address that sends alarm notifications.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="portal_auth_mode_python">
<a href="#portal_auth_mode_python" style="color: inherit; text-decoration: inherit;">portal_<wbr>auth_<wbr>mode</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The service to use to authenticate users to the portal. Choose from SSO or IAM. You can't change this value after you create a portal.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="portal_description_python">
<a href="#portal_description_python" style="color: inherit; text-decoration: inherit;">portal_<wbr>description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A description for the portal.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#portaltag">Sequence[Portal<wbr>Tag<wbr>Args]</a></span>
    </dt>
    <dd>{{% md %}}A list of key-value pairs that contain metadata for the portal.{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the Portal resource produces the following output properties:



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
        <span id="portalarn_csharp">
<a href="#portalarn_csharp" style="color: inherit; text-decoration: inherit;">Portal<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the portal, which has the following format.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="portalclientid_csharp">
<a href="#portalclientid_csharp" style="color: inherit; text-decoration: inherit;">Portal<wbr>Client<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The AWS SSO application generated client ID (used with AWS SSO APIs).{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="portalid_csharp">
<a href="#portalid_csharp" style="color: inherit; text-decoration: inherit;">Portal<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the portal.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="portalstarturl_csharp">
<a href="#portalstarturl_csharp" style="color: inherit; text-decoration: inherit;">Portal<wbr>Start<wbr>Url</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The public root URL for the AWS IoT AWS IoT SiteWise Monitor application portal.{{% /md %}}</dd></dl>
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
        <span id="portalarn_go">
<a href="#portalarn_go" style="color: inherit; text-decoration: inherit;">Portal<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the portal, which has the following format.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="portalclientid_go">
<a href="#portalclientid_go" style="color: inherit; text-decoration: inherit;">Portal<wbr>Client<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The AWS SSO application generated client ID (used with AWS SSO APIs).{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="portalid_go">
<a href="#portalid_go" style="color: inherit; text-decoration: inherit;">Portal<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the portal.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="portalstarturl_go">
<a href="#portalstarturl_go" style="color: inherit; text-decoration: inherit;">Portal<wbr>Start<wbr>Url</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The public root URL for the AWS IoT AWS IoT SiteWise Monitor application portal.{{% /md %}}</dd></dl>
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
        <span id="portalarn_nodejs">
<a href="#portalarn_nodejs" style="color: inherit; text-decoration: inherit;">portal<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ARN of the portal, which has the following format.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="portalclientid_nodejs">
<a href="#portalclientid_nodejs" style="color: inherit; text-decoration: inherit;">portal<wbr>Client<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The AWS SSO application generated client ID (used with AWS SSO APIs).{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="portalid_nodejs">
<a href="#portalid_nodejs" style="color: inherit; text-decoration: inherit;">portal<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the portal.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="portalstarturl_nodejs">
<a href="#portalstarturl_nodejs" style="color: inherit; text-decoration: inherit;">portal<wbr>Start<wbr>Url</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The public root URL for the AWS IoT AWS IoT SiteWise Monitor application portal.{{% /md %}}</dd></dl>
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
        <span id="portal_arn_python">
<a href="#portal_arn_python" style="color: inherit; text-decoration: inherit;">portal_<wbr>arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ARN of the portal, which has the following format.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="portal_client_id_python">
<a href="#portal_client_id_python" style="color: inherit; text-decoration: inherit;">portal_<wbr>client_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The AWS SSO application generated client ID (used with AWS SSO APIs).{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="portal_id_python">
<a href="#portal_id_python" style="color: inherit; text-decoration: inherit;">portal_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the portal.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="portal_start_url_python">
<a href="#portal_start_url_python" style="color: inherit; text-decoration: inherit;">portal_<wbr>start_<wbr>url</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The public root URL for the AWS IoT AWS IoT SiteWise Monitor application portal.{{% /md %}}</dd></dl>
{{% /choosable %}}







## Supporting Types



<h4 id="portaltag">Portal<wbr>Tag</h4>

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
        <span class="property-type">string</span>
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
        <span class="property-type">string</span>
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
        <span class="property-type">string</span>
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

