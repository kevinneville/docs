
---
title: "getConversation"
title_tag: "google-native.dialogflow/v2beta1.getConversation"
meta_desc: "Documentation for the google-native.dialogflow/v2beta1.getConversation function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Retrieves the specific conversation.




## Using getConversation {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getConversation<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetConversationArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetConversationResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_conversation(</span><span class="nx">conversation_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                     <span class="nx">location</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                     <span class="nx">project</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                     <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetConversationResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupConversation<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupConversationArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupConversationResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupConversation` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetConversation </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetConversationResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetConversationArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="conversationid_csharp">
<a href="#conversationid_csharp" style="color: inherit; text-decoration: inherit;">Conversation<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="location_csharp">
<a href="#location_csharp" style="color: inherit; text-decoration: inherit;">Location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_csharp">
<a href="#project_csharp" style="color: inherit; text-decoration: inherit;">Project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="conversationid_go">
<a href="#conversationid_go" style="color: inherit; text-decoration: inherit;">Conversation<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="location_go">
<a href="#location_go" style="color: inherit; text-decoration: inherit;">Location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_go">
<a href="#project_go" style="color: inherit; text-decoration: inherit;">Project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="conversationid_nodejs">
<a href="#conversationid_nodejs" style="color: inherit; text-decoration: inherit;">conversation<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="location_nodejs">
<a href="#location_nodejs" style="color: inherit; text-decoration: inherit;">location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_nodejs">
<a href="#project_nodejs" style="color: inherit; text-decoration: inherit;">project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="conversation_id_python">
<a href="#conversation_id_python" style="color: inherit; text-decoration: inherit;">conversation_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="location_python">
<a href="#location_python" style="color: inherit; text-decoration: inherit;">location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_python">
<a href="#project_python" style="color: inherit; text-decoration: inherit;">project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## getConversation Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="conversationprofile_csharp">
<a href="#conversationprofile_csharp" style="color: inherit; text-decoration: inherit;">Conversation<wbr>Profile</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Conversation Profile to be used to configure this Conversation. This field cannot be updated. Format: `projects//locations//conversationProfiles/`.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="conversationstage_csharp">
<a href="#conversationstage_csharp" style="color: inherit; text-decoration: inherit;">Conversation<wbr>Stage</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The stage of a conversation. It indicates whether the virtual agent or a human agent is handling the conversation. If the conversation is created with the conversation profile that has Dialogflow config set, defaults to ConversationStage.VIRTUAL_AGENT_STAGE; Otherwise, defaults to ConversationStage.HUMAN_ASSIST_STAGE. If the conversation is created with the conversation profile that has Dialogflow config set but explicitly sets conversation_stage to ConversationStage.HUMAN_ASSIST_STAGE, it skips ConversationStage.VIRTUAL_AGENT_STAGE stage and directly goes to ConversationStage.HUMAN_ASSIST_STAGE.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="endtime_csharp">
<a href="#endtime_csharp" style="color: inherit; text-decoration: inherit;">End<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time the conversation was finished.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lifecyclestate_csharp">
<a href="#lifecyclestate_csharp" style="color: inherit; text-decoration: inherit;">Lifecycle<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The current state of the Conversation.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique identifier of this conversation. Format: `projects//locations//conversations/`.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="phonenumber_csharp">
<a href="#phonenumber_csharp" style="color: inherit; text-decoration: inherit;">Phone<wbr>Number</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#googleclouddialogflowv2beta1conversationphonenumberresponse">Pulumi.<wbr>Google<wbr>Native.<wbr>Dialogflow.<wbr>V2Beta1.<wbr>Outputs.<wbr>Google<wbr>Cloud<wbr>Dialogflow<wbr>V2beta1Conversation<wbr>Phone<wbr>Number<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Required if the conversation is to be connected over telephony.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="starttime_csharp">
<a href="#starttime_csharp" style="color: inherit; text-decoration: inherit;">Start<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time the conversation was started.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="conversationprofile_go">
<a href="#conversationprofile_go" style="color: inherit; text-decoration: inherit;">Conversation<wbr>Profile</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Conversation Profile to be used to configure this Conversation. This field cannot be updated. Format: `projects//locations//conversationProfiles/`.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="conversationstage_go">
<a href="#conversationstage_go" style="color: inherit; text-decoration: inherit;">Conversation<wbr>Stage</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The stage of a conversation. It indicates whether the virtual agent or a human agent is handling the conversation. If the conversation is created with the conversation profile that has Dialogflow config set, defaults to ConversationStage.VIRTUAL_AGENT_STAGE; Otherwise, defaults to ConversationStage.HUMAN_ASSIST_STAGE. If the conversation is created with the conversation profile that has Dialogflow config set but explicitly sets conversation_stage to ConversationStage.HUMAN_ASSIST_STAGE, it skips ConversationStage.VIRTUAL_AGENT_STAGE stage and directly goes to ConversationStage.HUMAN_ASSIST_STAGE.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="endtime_go">
<a href="#endtime_go" style="color: inherit; text-decoration: inherit;">End<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time the conversation was finished.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lifecyclestate_go">
<a href="#lifecyclestate_go" style="color: inherit; text-decoration: inherit;">Lifecycle<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The current state of the Conversation.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique identifier of this conversation. Format: `projects//locations//conversations/`.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="phonenumber_go">
<a href="#phonenumber_go" style="color: inherit; text-decoration: inherit;">Phone<wbr>Number</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#googleclouddialogflowv2beta1conversationphonenumberresponse">Google<wbr>Cloud<wbr>Dialogflow<wbr>V2beta1Conversation<wbr>Phone<wbr>Number<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Required if the conversation is to be connected over telephony.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="starttime_go">
<a href="#starttime_go" style="color: inherit; text-decoration: inherit;">Start<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time the conversation was started.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="conversationprofile_nodejs">
<a href="#conversationprofile_nodejs" style="color: inherit; text-decoration: inherit;">conversation<wbr>Profile</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Conversation Profile to be used to configure this Conversation. This field cannot be updated. Format: `projects//locations//conversationProfiles/`.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="conversationstage_nodejs">
<a href="#conversationstage_nodejs" style="color: inherit; text-decoration: inherit;">conversation<wbr>Stage</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The stage of a conversation. It indicates whether the virtual agent or a human agent is handling the conversation. If the conversation is created with the conversation profile that has Dialogflow config set, defaults to ConversationStage.VIRTUAL_AGENT_STAGE; Otherwise, defaults to ConversationStage.HUMAN_ASSIST_STAGE. If the conversation is created with the conversation profile that has Dialogflow config set but explicitly sets conversation_stage to ConversationStage.HUMAN_ASSIST_STAGE, it skips ConversationStage.VIRTUAL_AGENT_STAGE stage and directly goes to ConversationStage.HUMAN_ASSIST_STAGE.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="endtime_nodejs">
<a href="#endtime_nodejs" style="color: inherit; text-decoration: inherit;">end<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time the conversation was finished.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lifecyclestate_nodejs">
<a href="#lifecyclestate_nodejs" style="color: inherit; text-decoration: inherit;">lifecycle<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The current state of the Conversation.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The unique identifier of this conversation. Format: `projects//locations//conversations/`.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="phonenumber_nodejs">
<a href="#phonenumber_nodejs" style="color: inherit; text-decoration: inherit;">phone<wbr>Number</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#googleclouddialogflowv2beta1conversationphonenumberresponse">Google<wbr>Cloud<wbr>Dialogflow<wbr>V2beta1Conversation<wbr>Phone<wbr>Number<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Required if the conversation is to be connected over telephony.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="starttime_nodejs">
<a href="#starttime_nodejs" style="color: inherit; text-decoration: inherit;">start<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time the conversation was started.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="conversation_profile_python">
<a href="#conversation_profile_python" style="color: inherit; text-decoration: inherit;">conversation_<wbr>profile</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Conversation Profile to be used to configure this Conversation. This field cannot be updated. Format: `projects//locations//conversationProfiles/`.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="conversation_stage_python">
<a href="#conversation_stage_python" style="color: inherit; text-decoration: inherit;">conversation_<wbr>stage</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The stage of a conversation. It indicates whether the virtual agent or a human agent is handling the conversation. If the conversation is created with the conversation profile that has Dialogflow config set, defaults to ConversationStage.VIRTUAL_AGENT_STAGE; Otherwise, defaults to ConversationStage.HUMAN_ASSIST_STAGE. If the conversation is created with the conversation profile that has Dialogflow config set but explicitly sets conversation_stage to ConversationStage.HUMAN_ASSIST_STAGE, it skips ConversationStage.VIRTUAL_AGENT_STAGE stage and directly goes to ConversationStage.HUMAN_ASSIST_STAGE.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="end_time_python">
<a href="#end_time_python" style="color: inherit; text-decoration: inherit;">end_<wbr>time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The time the conversation was finished.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lifecycle_state_python">
<a href="#lifecycle_state_python" style="color: inherit; text-decoration: inherit;">lifecycle_<wbr>state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The current state of the Conversation.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The unique identifier of this conversation. Format: `projects//locations//conversations/`.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="phone_number_python">
<a href="#phone_number_python" style="color: inherit; text-decoration: inherit;">phone_<wbr>number</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#googleclouddialogflowv2beta1conversationphonenumberresponse">Google<wbr>Cloud<wbr>Dialogflow<wbr>V2beta1Conversation<wbr>Phone<wbr>Number<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Required if the conversation is to be connected over telephony.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="start_time_python">
<a href="#start_time_python" style="color: inherit; text-decoration: inherit;">start_<wbr>time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The time the conversation was started.{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="googleclouddialogflowv2beta1conversationphonenumberresponse">Google<wbr>Cloud<wbr>Dialogflow<wbr>V2beta1Conversation<wbr>Phone<wbr>Number<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="phonenumber_csharp">
<a href="#phonenumber_csharp" style="color: inherit; text-decoration: inherit;">Phone<wbr>Number</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The phone number to connect to this conversation.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="phonenumber_go">
<a href="#phonenumber_go" style="color: inherit; text-decoration: inherit;">Phone<wbr>Number</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The phone number to connect to this conversation.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="phonenumber_nodejs">
<a href="#phonenumber_nodejs" style="color: inherit; text-decoration: inherit;">phone<wbr>Number</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The phone number to connect to this conversation.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="phone_number_python">
<a href="#phone_number_python" style="color: inherit; text-decoration: inherit;">phone_<wbr>number</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The phone number to connect to this conversation.{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-google-native">https://github.com/pulumi/pulumi-google-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>

