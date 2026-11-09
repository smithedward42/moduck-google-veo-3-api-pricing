# Google Veo 3 API Pricing: Turn Published Rates Into a Clip Budget

A developer planning a short generated video can find a $0.05 Veo rate and still have no reliable price for the clip. The practical question is what the number buys: a particular Veo generation, audio setting, resolution, purchasing route and billable unit. Those details change the calculation before any prompt is sent.

For a Google Veo 3 API pricing decision, start with Google's public rate table and read its labels intact. Then a per-second rate can become a budget *if the route actually bills that unit*. The example below is a planning scenario, not a charge observed in an account.

![Film strip passing through three translucent frames: layered plates, a dial and stacked cubes.](cover.png)

## Read the Google rate before pricing a clip

[Google Cloud's Agent Platform pricing page](https://cloud.google.com/model-garden/pricing), checked November 9, 2026, lists Veo 3.1 Standard, Fast and Lite as separate models. Its Veo table labels the following prices **USD / 1 count**. The rows below are a selection of the published text-to-video, video-with-audio configurations; they are not a universal “Veo 3” price.

| Google Cloud model | Output | Resolution | Published price |
|---|---|---|---|
| Veo 3.1 Lite | Video + audio | 720p | $0.05 / 1 count |
| Veo 3.1 Lite | Video + audio | 1080p | $0.08 / 1 count |
| Veo 3.1 Fast | Video + audio | 720p | $0.10 / 1 count |
| Veo 3.1 Fast | Video + audio | 1080p | $0.12 / 1 count |
| Veo 3.1 Standard | Video + audio | 720p or 1080p | $0.40 / 1 count |
| Veo 3.1 Lite | Video, no generated audio | 720p | $0.03 / 1 count |

All six rows come from that same [Google Cloud](https://cloud.google.com/model-garden/pricing) page and its displayed USD unit on November 9, 2026. The page also has other resolutions and no-audio rows; consult the exact row for the planned output. It lists **Veo 3** separately from **Veo 3.1**. A generic “Veo 3 API” search therefore does not identify the model that will be billed.

There is a second, easily missed source distinction. Search-indexed copies of Google's [Gemini Developer API pricing documentation](https://ai.google.dev/gemini-api/docs/pricing) describe Veo 3.1 paid pricing **per second** and show the same $0.05 for Lite with audio at 720p. But the current page reached in the browser redirected to [Google AI Studio pricing](https://aistudio.google.com/docs/pricing), where Veo rows were not visible in the rendered view checked for this article. The indexed wording is useful context, but it is not proof that the live Google Cloud label “1 count” means one second for every route or that a particular account will be charged identically. Keep the route and source attached to the quote. Otherwise, a clip estimate can appear precise while pricing a different product.

## What an eight-second estimate can and cannot say

Suppose a developer wants **one eight-second, 720p Veo 3.1 Lite video with generated audio**. If the applicable route confirms **$0.05 per generated second**, the arithmetic is simple:

> 8 seconds × $0.05 per second = **$0.40 for one successfully billed output**.

That $0.05 per-second premise comes from search-indexed [Gemini Developer API pricing](https://ai.google.dev/gemini-api/docs/pricing?frmapp=yes) wording, **not** from treating Google Cloud's “/ 1 count” label as a proven second. If the account uses the Cloud route, first establish what its billable count represents and whether the same settings and pricing mode apply. The $0.40 above is a conditional conversion, not a Google Cloud invoice or a promise of a fixed clip price.

Now add the production reality. If a team plans **20 accepted clips**, each eight seconds, and allows **two billable outputs per accepted clip**, the same assumed per-second rate yields 20 × 2 × 8 × $0.05 = **$16**. If all 20 succeed on the first billable attempt, the modeled generation amount would instead be **$8**. The assumed second output is an editorial scenario, not a measured retry rate. The difference tells you which operational question to resolve: are failed requests, discarded but successfully generated clips, or extended outputs billable on your route? The public Cloud table does not specify here whether a discarded successful output or a failed request is billable under every account and route. Budget from the number of *billable outputs*, then verify that definition in the applicable terms.

This is also why a “per video” claim can mislead. An eight-second clip at $0.05 **per second** is $0.40 under the stated premise, not $0.05. The observed [MindStudio tier comparison](https://www.mindstudio.ai/blog/veo-3-1-vs-veo-3-1-fast-vs-veo-3-1-light-comparison) uses “per video” language for its minimum; that cannot be substituted for Google's per-second indexed wording or Cloud's per-count display without checking the service and unit behind it.

## Choose the purchasing route and verify its terms

The rate only becomes a purchasing decision when the route is fixed. A Google Cloud or Gemini API project has its own model ID, billing terms and account access. A consumer Flow subscription uses credits and plan conditions. An independent provider such as [Kie.ai](https://kie.ai/features/v3-api) sets its own offer and API terms. A calculation on [CostGoat](https://costgoat.com/pricing/google-veo) can help explore scenarios, but its modeled result is not evidence of your account bill. These are different contracts, even when all of them say “Veo.”

Before choosing, verify four things in the current listing and documentation: the **exact model generation and endpoint**; whether audio, resolution and any processing mode match your intended output; the **billable unit and the treatment of failed or discarded jobs**; and the access, region and account conditions that apply to your project. The Google Cloud table supports a tier comparison for named settings. It does not establish that Lite is the right creative choice for every job, or that a vendor's similarly named model is operationally equivalent. No output-quality or latency tests were performed here.

## Where Moduck fits in the decision

[Moduck](https://moduck.ai/models) is another API route a developer may evaluate. Its product facts describe a unified model-access platform, but the public catalog view checked for this article did **not** confirm a Veo 3.1 listing, matching audio/resolution settings, availability or a Veo-specific price. It would be unfair to put a Moduck number beside the Google rows without that evidence.

If Moduck is on your route list, [Read the documentation](https://docs.moduck.ai/) and confirm the exact model listing, API method and current pricing terms before requesting a key. For any route, carry the same clip specification and billable-unit question into the decision. That is what turns a published number into a budget you can defend.


