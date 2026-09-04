# claude-website-full-clone-made-qith-glm-5.3-f112<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Prompt Library — 52 Copy-Paste Prompts for Claude Code</title>
<meta name="description" content="A searchable library of 52 copy-paste prompts for Claude Code, tagged by task and role. Fill in the highlighted fields, copy, and send.">
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'%3E%3Crect width='24' height='24' fill='%23FAFAF7' rx='5'/%3E%3Cpath d='M6 18 L18 6 M8 6 h10 v10' stroke='%23D97757' stroke-width='2.4' fill='none' stroke-linecap='round' stroke-linejoin='round'/%3E%3C/svg%3E">
<style>
/* ═══════════ BASE ═══════════ */
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --bg:#FAFAF7; --surface:#F0EEE6; --card:#FFFFFF;
  --border:#E8E6DC; --border-subtle:rgba(31,30,29,.09);
  --text:#141413; --text-2:#5E5D59; --text-3:#73726C; --text-4:#9C9A92;
  --accent:#D97757; --accent-bg:rgba(217,119,87,.09);
  --term-bg:#141413; --term-fg:#F0EEE6; --mark:rgba(217,119,87,.22);
  --sans:-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,sans-serif;
  --mono:ui-monospace,SFMono-Regular,Menlo,Consolas,'Liberation Mono',monospace;
}
@media (prefers-color-scheme: dark){
  :root{
    --bg:#1B1A18; --surface:#232220; --card:#201F1D;
    --border:#3D3C38; --border-subtle:rgba(240,238,230,.09);
    --text:#F0EEE6; --text-2:#BFBDB4; --text-3:#91908A; --text-4:#767468;
    --mark:rgba(217,119,87,.32);
  }
}
html{overflow-x:hidden}
body{background:var(--bg);color:var(--text);font:16px/1.6 var(--sans);-webkit-font-smoothing:antialiased}
:focus-visible{outline:2px solid var(--accent);outline-offset:2px}
::selection{background:var(--accent);color:#fff}
a{color:var(--accent);text-decoration:none}
a:hover{text-decoration:underline}
button{font-family:inherit;cursor:pointer;touch-action:manipulation}
.pl{max-width:880px;margin:0 auto;padding:36px 20px 72px}

/* ═══════════ PAGE HEAD ═══════════ */
.pl-pagehead h1{font-size:clamp(26px,5vw,34px);font-weight:600;letter-spacing:-.02em}
.pl-pagehead p{margin-top:10px;max-width:62ch;color:var(--text-2);font-size:15px;line-height:1.7}
.pl-pagehead{margin-bottom:26px;animation:fadeUp .4s ease both}
@keyframes fadeUp{from{opacity:0;transform:translateY(10px)}to{opacity:1;transform:none}}
@media (prefers-reduced-motion:reduce){*{animation:none!important;transition:none!important}}

/* ═══════════ SEARCH ═══════════ */
.pl-search{display:flex;align-items:center;gap:10px;padding:14px 18px;background:var(--surface);border:1px solid var(--border);border-radius:12px;margin-bottom:14px}
.pl-search svg{color:var(--text-4);flex:none}
.pl-search input{flex:1;border:none;outline:none;background:transparent;font:16px var(--sans);color:var(--text);min-width:0}
.pl-search input::placeholder{color:var(--text-4)}
.pl-search kbd{font:600 10px var(--mono);color:var(--text-4);border:1px solid var(--border);border-bottom-width:2px;border-radius:4px;padding:2px 6px;flex:none}

/* ═══════════ TAG ROW ═══════════ */
.pl-tags{display:flex;gap:8px;flex-wrap:wrap;align-items:center;margin-bottom:20px}
.pl-tag{padding:7px 14px;border:1px solid var(--border);background:var(--card);font-size:14px;color:var(--text-2);border-radius:999px;transition:background .12s,color .12s,border-color .12s}
.pl-tag:hover{background:var(--surface);color:var(--text)}
.pl-tag.on{background:var(--text);border-color:var(--text);color:var(--bg)}
.pl-tag--start{color:var(--accent);font-weight:500}
.pl-tag--start.on{background:var(--accent);border-color:var(--accent);color:#fff}
.pl-tags.dim .pl-tag{opacity:.45}
.pl-tags.dim .pl-tag:hover{opacity:1}
.pl-sep{width:1px;height:22px;background:var(--border);margin:0 4px;flex:none}
.pl-clear{border:none;background:none;font-size:13px;color:var(--text-4);padding:4px 6px}
.pl-clear:hover{color:var(--text-2)}
.pl-count{margin-left:auto;font-size:14px;color:var(--text-4)}

/* ═══════════ GROUPS / CARDS ═══════════ */
.pl-group-h{font-size:12px;letter-spacing:.09em;text-transform:uppercase;color:var(--text-4);margin:26px 0 12px}
.pl-group-h .pl-phase{color:var(--text-3)}
.pl-card{border:1px solid var(--border-subtle);border-radius:10px;margin-bottom:12px;background:var(--card);padding:14px 18px}
.pl-card.open{border-color:var(--border);background:var(--surface)}
.pl-head{width:100%;display:flex;align-items:baseline;gap:12px;border:none;background:transparent;text-align:left;padding:0}
.pl-title{flex:1;font-size:17px;font-weight:500;color:var(--text);min-width:0;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.pl-chip{font-size:11px;letter-spacing:.05em;text-transform:uppercase;padding:3px 9px;border-radius:999px;flex:none;background:var(--accent-bg);color:var(--accent)}
.pl-preview{display:block;font-family:var(--mono);font-size:13.5px;color:var(--text-3);margin-top:6px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
.pl-match{font-size:13.5px;color:var(--text-3);margin-top:6px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
.pl-match mark{background:var(--mark);color:var(--text);padding:1px 2px;border-radius:3px}

/* ═══════════ CARD BODY ═══════════ */
.pl-body{margin-top:14px;padding-top:14px;border-top:1px solid var(--border-subtle)}
.pl-label{font-size:11.5px;letter-spacing:.09em;text-transform:uppercase;color:var(--text-4);margin:12px 0 8px}
.pl-hint{font-size:14px;color:var(--text-3);margin:0 0 10px}
.pl-hint .pl-mini{display:inline-block;font-size:10.5px;letter-spacing:.06em;text-transform:uppercase;padding:2px 8px;margin-right:6px;border-radius:4px;background:var(--accent-bg);color:var(--accent)}
.pl-hint-chip{font-family:var(--mono);font-size:.92em;background:var(--accent-bg);color:var(--accent);border-bottom:1.5px dashed var(--accent);border-radius:3px 3px 0 0;padding:1px 5px}

/* terminal-style prompt box with inline fill slots */
.pl-box{display:flex;align-items:center;gap:10px;flex-wrap:wrap;padding:14px 16px;background:var(--term-bg);color:var(--term-fg);border-radius:10px;font-family:var(--mono);font-size:14.5px}
.pl-caret{color:var(--accent);flex:none}
.pl-box code{flex:1;min-width:0;background:none;padding:0;color:inherit;white-space:pre-wrap;line-height:2;overflow-wrap:break-word}
.pl-slot{font:inherit;background:rgba(217,119,87,.16);color:var(--term-fg);border:none;border-bottom:1.5px dashed var(--accent);border-radius:4px 4px 0 0;padding:2px 6px;margin:0 1px;outline:none;min-width:6ch;max-width:100%;box-sizing:content-box;cursor:text}
.pl-slot:hover{background:rgba(217,119,87,.24)}
.pl-slot:focus{background:rgba(217,119,87,.3);border-bottom-style:solid}
.pl-slot::placeholder{color:rgba(240,238,230,.42);font-style:italic}
.pl-copy{font-size:12.5px;padding:7px 14px;border-radius:6px;background:var(--accent);color:#fff;border:none;flex:none}
.pl-copy:hover{filter:brightness(1.07)}
.pl-copy:active{transform:translateY(1px)}

.pl-teaches{font-size:15.5px;color:var(--text-2);line-height:1.6}
.pl-next{display:flex;gap:10px;align-items:baseline;margin-top:14px;padding:10px 12px;background:var(--accent-bg);border-radius:8px;font-size:14.5px;color:var(--text-2)}
.pl-next b{font-size:11px;letter-spacing:.06em;text-transform:uppercase;color:var(--accent);flex:none}
.pl-src{font-size:14px;color:var(--text-4);margin-top:14px}

.pl-showall{display:block;width:100%;padding:14px;margin-top:6px;border:1px dashed var(--border);border-radius:10px;background:transparent;font-size:15px;color:var(--accent);text-align:center}
.pl-showall:hover{background:var(--accent-bg);border-style:solid}
.pl-empty{padding:36px;text-align:center;color:var(--text-4);border:1px dashed var(--border);border-radius:10px}
.pl-empty code{font-family:var(--mono)}

.pl-toast{position:fixed;left:50%;bottom:24px;transform:translate(-50%,10px);background:var(--term-bg);color:var(--term-fg);font:600 12px var(--mono);padding:11px 18px;border-radius:8px;opacity:0;pointer-events:none;transition:.2s;z-index:50}
.pl-toast.show{opacity:1;transform:translate(-50%,0)}

/* ═══════════ MOBILE ═══════════ */
@media(max-width:640px){
  .pl{padding:24px 14px 56px}
  .pl-card{padding:12px 14px}
  .pl-title{font-size:15.5px}
  .pl-box{font-size:13.5px;padding:12px}
  .pl-copy{flex-basis:100%}
  .pl-count{margin-left:0;flex-basis:100%}
}
</style>
</head>
<body>
<main class="pl">
  <header class="pl-pagehead">
    <h1>Prompt library</h1>
    <p>Copy-paste prompts for Claude Code, tagged by task and role. Search or filter by tag, open a card, fill in the highlighted fields, and copy the finished prompt. Open any card's <strong>Why this works</strong> to learn the pattern behind it.</p>
  </header>

  <div class="pl-search">
    <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true"><circle cx="11" cy="11" r="7"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>
    <input id="pl-q" type="text" placeholder="Search 52 prompts…" aria-label="Search prompts">
    <kbd>/</kbd>
  </div>

  <div class="pl-tags" id="pl-tags" role="toolbar" aria-label="Filters"></div>
  <div id="pl-results"></div>
</main>

<div class="pl-toast" id="pl-toast" role="status"></div>

<script>
/* ═════════════════════════════════════════════════════════════
   Standalone rebuild of the Prompt Library — no dependencies.
   All 52 prompts preserved from the pasted data; titles and
   "why this works" notes written for this build.
   ═════════════════════════════════════════════════════════════ */
(function(){
'use strict';

/* ── helpers ── */
function $(s,c){ return (c||document).querySelector(s); }
function esc(s){ return String(s).replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;').replace(/"/g,'&quot;'); }

/* ── vocabulary ── */
var TAGS = ['understand','plan','prototype','build','test','refactor','review','steer','debug','git','release','data','automate','pm','design','docs','marketing','security','ops'];
var TAG_LABEL = { understand:'Understand', plan:'Plan', prototype:'Prototype', build:'Build', test:'Test', refactor:'Refactor', review:'Review', steer:'Steer', debug:'Debug', git:'Git', release:'Release', data:'Data', automate:'Automate', pm:'Product', design:'Design', docs:'Docs', marketing:'Marketing', security:'Security', ops:'On-call' };
var CAT_TAG = { Onboard:'understand', Understand:'understand', Plan:'plan', Prototype:'prototype', Implement:'build', Test:'test', Refactor:'refactor', Review:'review', Steer:'steer', Git:'git', Release:'release', Debug:'debug', Incident:'debug', Data:'data', Automate:'automate' };
var PHASE_LABEL = { discover:'Discover', design:'Design', build:'Build', ship:'Ship', operate:'Operate' };
var CAT_LABEL = { Onboard:'Onboard', Understand:'Understand', Plan:'Plan', Prototype:'Prototype', Implement:'Implement', Test:'Test', Refactor:'Refactor', Review:'Review', Steer:'Steer', Git:'Git', Release:'Release', Debug:'Debug', Incident:'Incident', Data:'Data', Automate:'Automate' };
var SOURCES = {
  workflows:      { label:'Common workflows', href:'https://code.claude.com/docs/en/common-workflows' },
  teams:          { label:'How Anthropic teams use Claude Code', href:'https://claude.com/blog/how-anthropic-teams-use-claude-code' },
  legal:          { label:'Anthropic Legal guide', href:'https://claude.com/blog/how-anthropic-uses-claude-legal' },
  cybersecurity:  { label:'Anthropic Cybersecurity guide', href:'https://claude.com/blog/how-anthropic-uses-claude-cybersecurity' },
  'best-practices': { label:'Best practices', href:'https://code.claude.com/docs/en/best-practices' },
  ebook:          { label:'Scaling agentic coding guide', href:'https://resources.anthropic.com/hubfs/Scaling%20agentic%20coding%20across%20your%20organization.pdf' }
};
var NEEDS_HINT = {
  tracker: 'your issue tracker connected as an MCP server or claude.ai connector.',
  gh:      'the GitHub CLI authenticated, or GitHub connected as an MCP server.',
  browser: 'a way to render and screenshot — the Desktop app, a browser extension, or a Playwright MCP server.',
  db:      'your data warehouse or log store connected as an MCP server.'
};
var PASTE_HINT = {
  mockup:    'Paste, drag, or @-mention your mockup image, then send this:',
  design:    'Paste, drag, or @-mention your design image, then send this:',
  screenshot:'Paste, drag, or @-mention your screenshot, then send this:',
  plan:      'Paste the plan output into the prompt first, then send this:',
  error:     'Paste the error output into the prompt first, then send this:',
  csv:       'Drag your file into the prompt, or replace the path with an @-mention of your own:'
};

/* ── the 52 prompts ── */
var P = [
{ id:'get-oriented-in-a', sdlc:'discover', cat:'Onboard', startN:1, roles:[], src:'workflows',
  prompt:'give me an overview of this codebase: architecture, key directories, and how the pieces connect',
  title:'Get oriented in a new repository',
  teaches:'Describe what you want to know, not which files to open — the exploration is done for you.',
  next:'Run /init to write a CLAUDE.md so this context sticks next session.' },
{ id:'explain-unfamiliar-code', sdlc:'discover', cat:'Understand', roles:[], src:'workflows',
  prompt:'explain what {path} does and how data flows through it. write it up as {format}',
  slots:{ path:'src/scheduler/queue.ts', format:'an HTML page with a diagram, then open it in my browser' },
  title:'Explain unfamiliar code',
  teaches:'Name the file and the output format you want; swap formats to fit how you learn.' },
{ id:'find-where-something-happens', sdlc:'discover', cat:'Understand', startN:2, roles:[], src:'workflows',
  prompt:'where do we {behavior}?',
  slots:{ behavior:'validate uploaded file types' },
  title:'Find where something happens',
  teaches:'Search by behavior when you don\'t know the file name or which directory it lives in.' },
{ id:'see-what-depends-on', sdlc:'discover', cat:'Understand', roles:[], src:'workflows',
  prompt:'what would break if I deleted {target}?',
  slots:{ target:'the retryWithBackoff helper' },
  title:'Check what breaks before deleting',
  teaches:'Get the list of dependents first, so nothing is removed silently.' },
{ id:'trace-how-code-evolved', sdlc:'discover', cat:'Understand', roles:[], src:'best-practices',
  prompt:'look through the commit history of {path} and summarize how it evolved and why',
  slots:{ path:'internal/auth/session.go' },
  title:'Trace how code evolved',
  teaches:'Point at history when the question is why the code looks like this, not what it does.' },
{ id:'scope-a-change-before', sdlc:'discover', cat:'Understand', roles:['pm','design'], src:'teams',
  prompt:'which files would I need to touch to {change}?',
  slots:{ change:'add a dark mode toggle to settings' },
  title:'Scope a change before starting',
  teaches:'Size the work across files before it goes on a roadmap.' },
{ id:'ask-the-codebase-a', sdlc:'discover', cat:'Understand', roles:['pm'], src:'teams',
  prompt:'I am a {role}. walk me through what happens when a user {action}, from the UI down to the result',
  slots:{ role:'PM', action:'clicks Export to PDF' },
  title:'Ask the codebase a product question',
  teaches:'State your role so the answer is pitched at the right altitude.' },
{ id:'plan-a-multi-file', sdlc:'design', cat:'Plan', roles:['pm','design'], src:'workflows',
  prompt:'plan how to refactor the {target} to {goal}. list the files you would change, but don\'t edit anything yet',
  slots:{ target:'payment module', goal:'support multiple currencies' },
  title:'Plan a multi-file change first',
  teaches:'Explicitly forbidding edits separates planning from doing — you review the approach before code moves.',
  next:'Use plan mode (Shift+Tab) to make plan-first the default.' },
{ id:'draft-a-spec-by', sdlc:'design', cat:'Plan', roles:['pm'], src:'best-practices',
  prompt:'I want to build {feature}. interview me about implementation, UX, edge cases, and tradeoffs until we have covered everything, then write the spec to SPEC.md',
  slots:{ feature:'per-workspace rate limits' },
  title:'Draft a spec by interview',
  teaches:'Being interviewed surfaces requirements you would forget to write down yourself.' },
{ id:'turn-a-meeting-into', sdlc:'design', cat:'Plan', roles:['pm'], src:'teams', needs:'tracker',
  prompt:'read {input} and write up the action items, then create a {tracker} ticket for each with acceptance criteria',
  slots:{ input:'@meeting-notes.md', tracker:'Linear' },
  title:'Turn a meeting into tickets',
  teaches:'Unstructured notes become tracker tickets with acceptance criteria in one step.' },
{ id:'map-edge-cases-before', sdlc:'design', cat:'Plan', roles:['design','pm'], src:'teams',
  prompt:'list the error states, empty states, and edge cases for {feature} that the design needs to cover',
  slots:{ feature:'the file upload flow' },
  title:'Map edge cases before building',
  teaches:'Ask for what\'s missing — error and empty states — rather than the happy path.' },
{ id:'turn-a-mockup-into', sdlc:'design', cat:'Prototype', roles:['design','pm','marketing'], src:'teams', paste:'mockup',
  prompt:'here is a mockup. build a working prototype I can click through, matching the layout and states shown',
  title:'Mockup to working prototype',
  teaches:'A clickable prototype answers interaction questions a static mock cannot.' },
{ id:'implement-from-a-screenshot', sdlc:'design', cat:'Prototype', roles:['design'], src:'best-practices', needs:'browser',
  prompt:'implement this design, then take a screenshot of the result, compare it to the original, and fix any differences',
  title:'Implement a design and self-check',
  teaches:'Render, screenshot, compare, fix — a verification loop that runs without you pointing out each gap.' },
{ id:'follow-an-existing-pattern', sdlc:'build', cat:'Implement', roles:[], src:'best-practices',
  prompt:'look at how {example} is implemented to understand the pattern, then build {new} the same way',
  slots:{ example:'the GitHub webhook handler', new:'a Stripe webhook handler' },
  title:'Follow an existing pattern',
  teaches:'Point at code you already like so new code matches your conventions, not generic ones.',
  next:'Record the pattern in CLAUDE.md so future sessions match it without the reference.' },
{ id:'generate-docs-for-code', sdlc:'build', cat:'Implement', roles:['docs'], src:'workflows',
  prompt:'find {scope} without {format} comments and add them, matching the style already used in the file',
  slots:{ scope:'the public functions in src/auth/', format:'JSDoc' },
  title:'Generate docs for existing code',
  teaches:'Name the scope and format; the comment style is matched to what the file already uses.' },
{ id:'add-a-small-well', sdlc:'build', cat:'Implement', roles:[], src:'workflows',
  prompt:'add a {endpoint} endpoint that returns {payload}',
  slots:{ endpoint:'/health', payload:'the app version and uptime' },
  title:'Add a small well-defined feature',
  teaches:'State inputs and outputs, not the implementation — placement follows the existing code.' },
{ id:'build-a-small-internal', sdlc:'build', cat:'Implement', roles:['pm','design','marketing','docs'], src:'teams',
  prompt:'create a {tool} using HTML, CSS, and vanilla JavaScript, then open it in my browser',
  slots:{ tool:'drag-and-drop Kanban board with three columns' },
  title:'Build a small internal tool',
  teaches:'No project, framework, or build step needed — describe the tool and see it running immediately.' },
{ id:'work-an-issue-end', sdlc:'build', cat:'Implement', roles:[], src:'workflows', needs:'gh',
  prompt:'read issue #{issue}, implement the fix, and run the tests',
  slots:{ issue:'312' },
  title:'Work an issue end to end',
  teaches:'Give the issue number so the full ticket — not your summary — drives the work.' },
{ id:'find-and-update-copy', sdlc:'build', cat:'Implement', roles:['design','docs','marketing'], src:'teams',
  prompt:'find every place we say "{copy}" or a close variant, show me each one in context, then update them all to "{new}". leave tests and the changelog alone',
  slots:{ copy:'Sign up free', new:'Start free trial' },
  title:'Find and update copy everywhere',
  teaches:'Variant-aware search catches reworded copy a literal search would miss, and skips fixtures.' },
{ id:'draft-from-past-examples', sdlc:'build', cat:'Implement', roles:['docs','marketing','pm'], src:'legal',
  prompt:'read the {examples} in {folder} to learn the structure and voice, then draft a new one for {topic}',
  slots:{ examples:'privacy impact assessments', folder:'legal/pia/', topic:'the new analytics integration' },
  title:'Draft from past examples',
  teaches:'Point at a folder of finished work instead of describing your style.' },
{ id:'write-tests-run-them', sdlc:'build', cat:'Test', startN:4, roles:[], src:'workflows',
  prompt:'write tests for {path}, run them, and fix any failures',
  slots:{ path:'app/parsers/feed.py' },
  title:'Write tests, run, fix failures',
  teaches:'Write, run, and fix in one instruction so iteration never stalls waiting for you.',
  next:'Run /init so your test command is discovered automatically.' },
{ id:'drive-implementation-from-tests', sdlc:'build', cat:'Test', roles:[], src:'ebook',
  prompt:'write tests for {feature} first, then implement it until they pass',
  slots:{ feature:'the password reset flow' },
  title:'Drive implementation from tests',
  teaches:'The tests define when the work is complete; the implementation iterates until they pass.' },
{ id:'fill-gaps-from-a', sdlc:'build', cat:'Test', roles:[], src:'workflows',
  prompt:'read {report} and add tests for the lowest-covered files until each is above {target}%',
  slots:{ report:'coverage/coverage-summary.json', target:'80' },
  title:'Fill gaps from a coverage report',
  teaches:'Read the actual coverage numbers instead of guessing what is untested.' },
{ id:'migrate-a-pattern-across', sdlc:'build', cat:'Refactor', roles:[], src:'workflows',
  prompt:'migrate everything from {from} to {to}: identify every place that needs to change, then make the changes',
  slots:{ from:'the old logging API', to:'the structured logger' },
  title:'Migrate a pattern codebase-wide',
  teaches:'Inventory every call site in the response first, so you can check none were missed.' },
{ id:'port-code-between-languages', sdlc:'build', cat:'Refactor', roles:[], src:'teams',
  prompt:'port {source} to {target}, keeping the same {keep}',
  slots:{ source:'this Python module', target:'Rust', keep:'public API and test behavior' },
  title:'Port code between languages',
  teaches:'Naming what must be preserved gives the port a contract to satisfy.' },
{ id:'optimize-against-a-measurable', sdlc:'build', cat:'Refactor', roles:['data'], src:'ebook',
  prompt:'optimize {target} to bring {metric} from {current} down to under {goal}',
  slots:{ target:'the search query', metric:'p95 latency', current:'2s', goal:'500ms' },
  title:'Optimize to a measurable target',
  teaches:'A named metric and target make "done" objective instead of a feeling.' },
{ id:'fix-a-precise-visual', sdlc:'build', cat:'Refactor', roles:['design'], src:'ebook',
  prompt:'the {element} extends {amount} beyond the {container} on {viewport}. fix it.',
  slots:{ element:'login button', amount:'20px', container:'card border', viewport:'mobile' },
  title:'Fix a precise visual bug',
  teaches:'Exact element, measurement, and viewport gets an exact fix.' },
{ id:'review-your-changes-before', sdlc:'build', cat:'Review', startN:5, roles:[], src:'workflows',
  prompt:'review my uncommitted changes and flag anything that looks risky before I commit',
  title:'Review changes before committing',
  teaches:'Catch risk while it is still uncommitted and cheap to drop.',
  next:'/code-review runs the same check in one command.' },
{ id:'review-a-pull-request', sdlc:'build', cat:'Review', roles:[], src:'workflows', needs:'gh',
  prompt:'review PR #{pr} and summarize what changed, then list any concerns',
  slots:{ pr:'247' },
  title:'Review a pull request',
  teaches:'Review with the whole codebase in context, not just the diff lines.' },
{ id:'review-infrastructure-changes-before', sdlc:'build', cat:'Review', roles:['security','ops'], src:'teams', paste:'plan',
  prompt:'here is my Terraform plan output. what is this going to do, and is anything here going to cause problems?',
  title:'Review infra changes before applying',
  teaches:'A plain-language read of dense plan output before anything touches production.' },
{ id:'run-a-security-review', sdlc:'build', cat:'Review', roles:['security'], src:'best-practices',
  prompt:'use a subagent to review {path} for security issues and report what it finds',
  slots:{ path:'src/api/' },
  title:'Run a security review',
  teaches:'A subagent runs the audit in its own context and reports back a summary.' },
{ id:'review-content-before-sending', sdlc:'build', cat:'Review', roles:['marketing','docs'], src:'legal',
  prompt:'review {file} for {concerns} and list anything I should fix before it goes to {reviewer}',
  slots:{ file:'launch-post.md', concerns:'unsupported claims, missing attributions, and brand-guideline issues', reviewer:'legal' },
  title:'Review content before it ships',
  teaches:'A focused first pass, named by concern, before a human spends time on it.' },
{ id:'course-correct-a-wrong', sdlc:'build', cat:'Steer', roles:[], src:'best-practices',
  prompt:'that is not right: {feedback}. try a different approach',
  slots:{ feedback:'the function signature needs to stay backward-compatible' },
  title:'Course-correct a wrong approach',
  teaches:'Give the reason it is wrong so the retry has a real constraint to satisfy.',
  next:'Press Esc twice to rewind and retry from a clean state.' },
{ id:'narrow-the-scope-of', sdlc:'build', cat:'Steer', roles:[], src:'best-practices',
  prompt:'that is too much. keep only the changes to {scope} and undo your other edits',
  slots:{ scope:'the validation logic in src/forms/' },
  title:'Narrow the scope of a change',
  teaches:'A stated boundary keeps a small fix from becoming a refactor.' },
{ id:'turn-a-correction-into', sdlc:'build', cat:'Steer', roles:[], src:'best-practices',
  prompt:'you keep {mistake}. add a rule to CLAUDE.md so this stops happening',
  slots:{ mistake:'using default exports when this project uses named exports' },
  title:'Turn a correction into a rule',
  teaches:'Chat corrections vanish; a rule in CLAUDE.md persists across sessions.',
  next:'Open /memory to review what was written.' },
{ id:'resolve-merge-conflicts', sdlc:'ship', cat:'Git', roles:[], src:'workflows',
  prompt:'resolve the merge conflicts in this branch and explain what you kept from each side',
  title:'Resolve merge conflicts',
  teaches:'Say the desired end state, not which conflict markers to keep — the reasoning makes the merge reviewable.' },
{ id:'commit-with-a-generated', sdlc:'ship', cat:'Git', roles:[], src:'workflows',
  prompt:'commit these changes with a message that summarizes what I did',
  title:'Commit with a generated message',
  teaches:'Let the message be derived from the diff, matched to your repo\'s existing style.' },
{ id:'open-a-pull-request', sdlc:'ship', cat:'Git', roles:[], src:'workflows', needs:'tracker',
  prompt:'find the {tracker} ticket about {topic} and open a PR that implements it',
  slots:{ tracker:'Linear', topic:'the login timeout' },
  title:'Open a PR from a ticket',
  teaches:'One prompt reads the spec, makes the change, and opens the PR.' },
{ id:'draft-release-notes-from', sdlc:'ship', cat:'Release', roles:['pm','docs','marketing'], src:'workflows',
  prompt:'compare {from} to {to} and draft release notes grouped by feature, fix, and breaking change',
  slots:{ from:'v2.3.0', to:'v2.4.0' },
  title:'Draft release notes from history',
  teaches:'Two tags plus a structure gives a changelog you only have to edit.' },
{ id:'write-a-ci-workflow', sdlc:'ship', cat:'Release', roles:['ops'], src:'workflows',
  prompt:'write a GitHub Actions workflow that {steps} on every push to {branch}',
  slots:{ steps:'runs the tests and deploys to staging', branch:'main' },
  title:'Write a CI workflow',
  teaches:'Describe when it runs and what it does; the YAML is matched to your project.' },
{ id:'find-and-fix-a', sdlc:'operate', cat:'Debug', startN:3, roles:[], src:'workflows',
  prompt:'the {test} test is failing, find out why and fix it',
  slots:{ test:'UserAuth' },
  title:'Find and fix a failing test',
  teaches:'Describe the symptom — the failure is reproduced and traced into source.' },
{ id:'investigate-a-reported-error', sdlc:'operate', cat:'Debug', roles:['ops'], src:'workflows',
  prompt:'users are seeing {symptom} on {where}. investigate and tell me what is going on',
  slots:{ symptom:'500 errors', where:'/api/settings' },
  title:'Investigate a reported error',
  teaches:'Symptom and location are enough to start; paste stack traces if you have them.' },
{ id:'fix-a-build-error', sdlc:'operate', cat:'Debug', roles:['ops'], src:'best-practices', paste:'error',
  prompt:'here is a build error. fix the root cause and verify the build succeeds',
  title:'Fix a build error',
  teaches:'The pasted error carries the context needed for a root-cause fix, then the build is verified.' },
{ id:'investigate-a-production-incident', sdlc:'operate', cat:'Incident', roles:['ops','security'], src:'workflows',
  prompt:'{symptom}. check the logs, recent deploys, and config changes, then tell me the most likely cause',
  slots:{ symptom:'the checkout endpoint started returning 500s an hour ago' },
  title:'Investigate a production incident',
  teaches:'Correlate logs, deploys, and config changes to find the most likely cause fast.' },
{ id:'diagnose-from-a-console', sdlc:'operate', cat:'Incident', roles:['ops','data'], src:'teams', paste:'screenshot',
  prompt:'here is a screenshot of {console}. walk me through why {resource} is failing and give me the exact commands to fix it',
  slots:{ console:'the GCP Kubernetes dashboard', resource:'this pod' },
  title:'Diagnose from a console screenshot',
  teaches:'A screenshot plus the resource name gets you exact fix commands, not guesses.' },
{ id:'query-logs-in-plain', sdlc:'operate', cat:'Incident', roles:['security','ops','data'], src:'cybersecurity', needs:'db',
  prompt:'show me all {events} for {scope} over {timeframe}. write the query, run it, and tell me what stands out',
  slots:{ events:'failed logins', scope:'the auth service', timeframe:'the past 24 hours' },
  title:'Query logs in plain language',
  teaches:'Plain-language requests become real queries against your connected log store.' },
{ id:'analyze-a-data-file', sdlc:'operate', cat:'Data', roles:['data','pm','marketing'], src:'teams', paste:'csv',
  prompt:'read {file}, summarize the key patterns, and write the results to {output}',
  slots:{ file:'@reports/q1-signups.csv', output:'an HTML page with charts, then open it in my browser' },
  title:'Analyze a data file',
  teaches:'The file is read, patterns summarized, and results written wherever you say.' },
{ id:'generate-variations-from-performance', sdlc:'operate', cat:'Data', roles:['marketing','data'], src:'teams', paste:'csv',
  prompt:'read {file}, find the underperforming {items}, and generate {n} new variations that stay under {limit} characters',
  slots:{ file:'@ads-performance.csv', items:'headlines', n:'20', limit:'90' },
  title:'Generate variations from performance data',
  teaches:'Underperformers are found from the data, and new variations respect your character limit.' },
{ id:'turn-a-recurring-task', sdlc:'operate', cat:'Automate', roles:[], src:'workflows',
  prompt:'create a /{name} skill for this project that {steps}',
  slots:{ name:'ship', steps:'runs the linter and tests, then drafts a commit message' },
  title:'Turn a task into a skill',
  teaches:'Recurring work becomes one command you can rerun forever.' },
{ id:'add-a-hook-for', sdlc:'operate', cat:'Automate', roles:[], src:'best-practices',
  prompt:'write a hook that {action} after every {event}',
  slots:{ action:'runs prettier', event:'edit to a .ts or .tsx file' },
  title:'Add a hook for automation',
  teaches:'Formatting and checks run automatically after the events you name.' },
{ id:'connect-a-tool-with', sdlc:'operate', cat:'Automate', roles:[], src:'workflows',
  prompt:'set up the {server} MCP server so you can read my {data} directly',
  slots:{ server:'Sentry', data:'error reports' },
  title:'Connect a tool with MCP',
  teaches:'Connected tools let Claude read the source of truth instead of pasted copies.' },
{ id:'capture-what-to-remember', sdlc:'operate', cat:'Automate', roles:['pm','docs'], src:'teams',
  prompt:'summarize what we did this session and suggest what to add to CLAUDE.md',
  title:'Capture what to remember',
  teaches:'End-of-session summaries become memory rules for the next one.' }
];

/* ── state ── */
var state = { q:'', start:true, sel:null, openId:null, fills:{} };
var results = [];

/* ── prompt string helpers ── */
function byId(id){ for (var i=0;i<P.length;i++) if (P[i].id===id) return P[i]; return null; }
function fillOf(p,k){
  var v = state.fills[p.id+'.'+k];
  if (v !== undefined) return v;
  return (p.slots && p.slots[k] !== undefined) ? p.slots[k] : '';
}
function assemble(p){
  return p.prompt.replace(/\{(\w+)\}/g, function(_,k){
    var v = fillOf(p,k);
    if (v) return v;
    return (p.slots && p.slots[k]) || k;
  });
}
function preview(p){
  return p.prompt.replace(/\{(\w+)\}/g, function(_,k){ return (p.slots && p.slots[k]) || k; });
}
function bodyText(p){ return preview(p) + ' ' + p.teaches + ' ' + (p.next || ''); }
function tagsOf(p){ return [CAT_TAG[p.cat]].concat(p.roles || []); }

/* ── filtering + sorting (mirrors the original logic) ── */
function computeResults(){
  var ql = state.q.trim().toLowerCase();
  var list = P.filter(function(p){
    if (ql) return p.title.toLowerCase().indexOf(ql) !== -1 || bodyText(p).toLowerCase().indexOf(ql) !== -1;
    if (state.start) return !!p.startN;
    if (state.sel) return tagsOf(p).indexOf(state.sel) !== -1;
    return true;
  });
  if (ql) return list;
  if (state.start) return list.slice().sort(function(a,b){ return (a.startN||99) - (b.startN||99); });
  if (state.sel) return list.slice().sort(function(a,b){
    return (a.roles||[]).length - (b.roles||[]).length ||
      ((b.sdlc==='operate')?1:0) - ((a.sdlc==='operate')?1:0);
  });
  return list;
}

/* ── snippet with <mark> for search matches in body text ── */
function snippetHtml(p, ql){
  if (!ql || p.title.toLowerCase().indexOf(ql) !== -1) return null;
  var txt = bodyText(p);
  var at = txt.toLowerCase().indexOf(ql);
  if (at < 0) return null;
  var lo = Math.max(0, at - 30), hi = Math.min(txt.length, at + ql.length + 50);
  return (lo>0?'…':'') + esc(txt.slice(lo,at)) +
         '<mark>' + esc(txt.slice(at, at+ql.length)) + '</mark>' +
         esc(txt.slice(at+ql.length, hi)) + (hi<txt.length?'…':'');
}

/* ── prompt body with inline fill-in inputs ── */
function promptCodeHtml(p){
  if (!p.slots) return esc(p.prompt);
  var parts = p.prompt.split(/(\{\w+\})/g);
  var h = '';
  for (var i=0;i<parts.length;i++){
    var m = /^\{(\w+)\}$/.exec(parts[i]);
    if (!m){ h += '<span>' + esc(parts[i]) + '</span>'; continue; }
    var k = m[1];
    var val = fillOf(p,k);
    var ph = (p.slots[k] !== undefined) ? p.slots[k] : k;
    h += '<input type="text" class="pl-slot" data-fill-id="' + p.id + '" data-fill-key="' + k +
         '" value="' + esc(val) + '" placeholder="' + esc(ph) + '" aria-label="' + esc(k) +
         '" style="width:' + ((val || ph).length + 3) + 'ch" spellcheck="false">';
  }
  return h;
}

function bodyHtml(p){
  var h = '<div class="pl-body">';
  h += '<div class="pl-label">' + (p.slots ? 'Fill in and copy' : 'Copy this prompt') + '</div>';
  if (p.needs && NEEDS_HINT[p.needs])
    h += '<div class="pl-hint"><span class="pl-mini">Needs</span>' + esc(NEEDS_HINT[p.needs]) + '</div>';
  if (p.paste && PASTE_HINT[p.paste])
    h += '<div class="pl-hint">' + esc(PASTE_HINT[p.paste]) + '</div>';
  if (p.slots)
    h += '<div class="pl-hint">Type in the <span class="pl-hint-chip">highlighted</span> fields to customize, then copy.</div>';
  h += '<div class="pl-box"><span class="pl-caret">❯</span><code>' + promptCodeHtml(p) + '</code>' +
       '<button type="button" class="pl-copy" data-copy="' + p.id + '">Copy</button></div>';
  h += '<div class="pl-label">Why this works</div>';
  h += '<div class="pl-teaches">' + esc(p.teaches) + '</div>';
  if (p.next)
    h += '<div class="pl-next"><b>Make it stick</b><span>' + esc(p.next) + '</span></div>';
  var s = SOURCES[p.src];
  if (s)
    h += '<div class="pl-src">From <a href="' + s.href + '" target="_blank" rel="noopener">' + esc(s.label) + '</a></div>';
  h += '</div>';
  return h;
}

function cardHtml(p, ql){
  var open = state.openId === p.id;
  var snip = snippetHtml(p, ql);
  var h = '<div class="pl-card' + (open ? ' open' : '') + '">';
  h += '<button type="button" class="pl-head" data-open="' + p.id + '" aria-expanded="' + open + '">';
  h += '<span class="pl-title">' + esc(p.title) + '</span>';
  if (p.startN) h += '<span class="pl-chip">Start here · ' + p.startN + '</span>';
  h += '</button>';
  if (snip) h += '<div class="pl-match">' + snip + '</div>';
  else h += '<code class="pl-preview">' + esc(preview(p)) + '</code>';
  if (open) h += bodyHtml(p);
  h += '</div>';
  return h;
}

/* ── render ── */
function renderTags(){
  var ql = state.q.trim().toLowerCase();
  var el = $('#pl-tags');
  var h = '<button type="button" class="pl-tag pl-tag--start' + (!ql && state.start ? ' on' : '') + '" id="pl-start">★ Start here</button>';
  h += '<span class="pl-sep"></span>';
  for (var i=0;i<TAGS.length;i++){
    var k = TAGS[i];
    h += '<button type="button" class="pl-tag' + (!ql && state.sel===k ? ' on' : '') + '" data-tag="' + k + '" aria-pressed="' + (!ql && state.sel===k) + '">' + TAG_LABEL[k] + '</button>';
  }
  if (state.start || state.sel || state.q) h += '<button type="button" class="pl-clear" id="pl-clear">Clear</button>';
  h += '<span class="pl-count">' + results.length + (results.length===1 ? ' prompt' : ' prompts') + '</span>';
  el.innerHTML = h;
  el.classList.toggle('dim', !!ql);
}

function renderResults(){
  var ql = state.q.trim().toLowerCase();
  var el = $('#pl-results');
  if (!results.length){
    el.innerHTML = '<div class="pl-empty">No prompts match ' + (ql ? '<code>' + esc(state.q) + '</code>' : '') +
      ' <button type="button" class="pl-clear" data-act="clear">Clear</button></div>';
    return;
  }
  if (!ql && state.start){
    var h = '<div class="pl-group-h">Five prompts to try first</div>';
    for (var i=0;i<results.length;i++) h += cardHtml(results[i], ql);
    h += '<button type="button" class="pl-showall" data-act="clear">Show all ' + P.length + ' prompts →</button>';
    el.innerHTML = h;
    return;
  }
  var groups = [], index = {};
  results.forEach(function(p){
    var key = p.sdlc + '|' + p.cat;
    if (!index[key]){ index[key] = { sdlc:p.sdlc, cat:p.cat, items:[] }; groups.push(index[key]); }
    index[key].items.push(p);
  });
  var out = '';
  groups.forEach(function(g){
    out += '<div class="pl-group-h"><span class="pl-phase">' + PHASE_LABEL[g.sdlc] + '</span> · ' + CAT_LABEL[g.cat] + '</div>';
    g.items.forEach(function(p){ out += cardHtml(p, ql); });
  });
  el.innerHTML = out;
}

function render(){
  results = computeResults();
  renderTags();
  renderResults();
}

/* ── copy with honest feedback ── */
var toastTimer;
function toast(msg){
  var t = $('#pl-toast'); t.textContent = msg; t.classList.add('show');
  clearTimeout(toastTimer); toastTimer = setTimeout(function(){ t.classList.remove('show'); }, 1900);
}
function copyPrompt(p, btn){
  var str = assemble(p);
  function done(){ btn.textContent = 'Copied'; setTimeout(function(){ btn.textContent = 'Copy'; }, 1600); }
  function fallback(){
    var ta = document.createElement('textarea');
    ta.value = str; ta.setAttribute('readonly','');
    ta.style.cssText = 'position:fixed;left:-9999px;top:0;opacity:0';
    document.body.appendChild(ta); ta.select();
    var ok = false;
    try { ok = document.execCommand('copy'); } catch (e) {}
    ta.remove();
    if (ok) done(); else toast('Copy blocked — select the prompt text manually');
  }
  if (navigator.clipboard && navigator.clipboard.writeText){
    navigator.clipboard.writeText(str).then(done, fallback);
  } else fallback();
}

/* ── events ── */
 $('#pl-q').addEventListener('input', function(e){
  state.q = e.target.value;
  if (state.q) state.start = false;
  render();
});

 $('#pl-tags').addEventListener('click', function(e){
  if (e.target.id === 'pl-start'){
    var turningOn = !state.start;
    state.q = ''; $('#pl-q').value = '';
    state.start = !state.start;
    if (turningOn) state.sel = null;
    render(); return;
  }
  if (e.target.id === 'pl-clear'){
    state.q = ''; state.start = false; state.sel = null;
    $('#pl-q').value = '';
    render(); return;
  }
  var t = e.target.closest('[data-tag]');
  if (t){
    state.q = ''; $('#pl-q').value = '';
    state.start = false;
    var k = t.getAttribute('data-tag');
    state.sel = (state.sel === k) ? null : k;
    render();
  }
});

 $('#pl-results').addEventListener('click', function(e){
  var act = e.target.closest('[data-act]');
  if (act && act.getAttribute('data-act') === 'clear'){
    state.q = ''; state.start = false; state.sel = null;
    $('#pl-q').value = '';
    render(); return;
  }
  var openBtn = e.target.closest('[data-open]');
  if (openBtn){
    var id = openBtn.getAttribute('data-open');
    state.openId = (state.openId === id) ? null : id;
    render(); return;
  }
  var copyBtn = e.target.closest('[data-copy]');
  if (copyBtn){
    var p = byId(copyBtn.getAttribute('data-copy'));
    if (p) copyPrompt(p, copyBtn);
  }
});

/* fill-in slot inputs: update state + width without re-render (keeps focus) */
 $('#pl-results').addEventListener('input', function(e){
  var el = e.target;
  if (!el.classList || !el.classList.contains('pl-slot')) return;
  var key = el.getAttribute('data-fill-id') + '.' + el.getAttribute('data-fill-key');
  state.fills[key] = el.value;
  var ph = el.getAttribute('placeholder') || '';
  el.style.width = ((el.value || ph).length + 3) + 'ch';
});

/* "/" focuses search; Escape leaves it */
document.addEventListener('keydown', function(e){
  if (e.key === '/' && document.activeElement !== $('#pl-q') &&
      !/INPUT|TEXTAREA|SELECT/.test(document.activeElement ? document.activeElement.tagName : '')){
    e.preventDefault(); $('#pl-q').focus();
  }
  if (e.key === 'Escape' && document.activeElement === $('#pl-q')) $('#pl-q').blur();
});

render();
})();
</script>
</body>
</html>