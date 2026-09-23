# NWO Open Competition ENW-M 2026-2027 — Progress Log

Last updated: 2026-09-23

## Fresh start

The proposal will be rewritten from scratch for the same NWO Open Competition
ENW-M 2026-2027 call. All previous research directions, drafting decisions, and
planned next steps are discarded. The new direction is On-TRAQ, described below.

## Working convention

Alexios requested that this file be maintained throughout our discussions. Keep
decisions, ideas, open questions, and changes to the proposal up to date. Distinguish
confirmed decisions from suggestions and claims that still need verification.

## New proposal: On-TRAQ

- **Confirmed title:** On-TRAQ: Transparently Retrofitting Applications for the Quantum Era
- **Target:** the same NWO Open Competition ENW-M 2026-2027 call, using the M-1
  application file. The idea was originally considered for Vidi; the pasted Vidi
  budget discussion is background, not the budget basis for this application.
- **Core idea from Alexios:** use system-call interposition and shared-memory-access
  interposition to transparently enable an end-to-end security/encryption layer for
  existing applications.
- **Confirmed scope:** communication both between processes on the same machine
  and across machines.
- **Current priority:** how to write the proposal; detailed mechanism design is
  deferred for now.

## Motivation and positioning to develop

The discussion supplied by Alexios positions the idea between application-integrated
TLS and network-level IPsec: transparent retrofitting with process/socket-level
granularity. IPsec should not be portrayed as unused; the relevant comparison is
its use for host-to-host protection of individual applications, alongside TLS
proxies and other transparent encryption approaches. Deployment and novelty claims
still require literature verification.

The title makes the quantum transition central to the proposal. The exact
post-quantum security goals, cryptographic mechanisms, and contribution have not
yet been specified. Do not treat any particular algorithm or architecture as agreed.

## Open questions for later development

- Define the endpoints, trust boundary, permitted plaintext locations, and peer
  authentication/identity model.
- Explain how shared-memory accesses are mediated beyond the system calls that
  establish mappings, and how communication/data boundaries are identified.
- Establish the contribution relative to existing transparent encryption approaches.
- Specify how the interposition layer enables the transition to quantum-resistant
  security, including compatibility and performance goals.

These are discussion points raised by the assistant, not settled design decisions.

## Changes made

- **2026-09-12:** reset this progress log at Alexios's request, discarding the old
  proposal direction and decisions.
- **2026-09-12:** updated the title in
  `LaTeX_application_forms/application-form-oc-enw-M-1-2026.tex` to the confirmed
  On-TRAQ title. Only the title was changed; the old abstract, summary, and other
  draft content still need replacement as the new proposal is developed.

## Page planning (2026-09-12)

Checked the local M-1 LaTeX template. Its limits are A.1: 1 page; A.2: 6 pages;
A.3: 1 page. Figures and tables count within A.2/A.3; A.4 references do not count
toward those limits. A.1 parts have no individual length restrictions. The
template specifies no individual page quotas for A.2 subsections. Part B public
summaries have a maximum of 100 words each (Dutch and English); no Part B page
cap is stated in the template.

Allocation revised and approved by Alexios on 2026-09-12:
- A.1: title/keywords/headings 0.15 page; abstract 0.40; non-specialist summary 0.45.
- A.2 Research topic: 2.00 pages.
- A.2 Approach: 2.50 pages, including methods, evaluation, and work plan/timeline.
- A.2 Justification: 0.25 page.
- A.2 Embedding/expertise: 0.75 page (expertise 0.40, collaborators 0.20,
  infrastructure 0.15, adjusted according to relevance).
- A.2 Risk assessment: 0.50 page.
- A.3 Impact: 1.00 page.

Allocations include headings and any figures/tables, and are flexible within each
section's limit. Total limited scientific narrative: 8 pages, plus references and
Part B. Budget is a separate deliverable.

## A.1 drafting (2026-09-12)

Alexios requested that drafting begin with the abstract. A first discussion draft
was presented in the conversation and written into the M-1 LaTeX file at Alexios's
request on 2026-09-12, replacing the old ACCESS abstract. The draft frames quantum-resistant communication retrofitting
through system-call and shared-memory-access interposition as the research goal,
with security, compatibility, and performance as evaluation dimensions. These
details remain subject to discussion; no algorithms or specific trust model have
been selected.

The title and abstract now reflect On-TRAQ. The Summary and keywords still need
revision for the new direction. The updated A.1 page fit has not yet been checked
by compiling the document.

## Existing files

- `Call-for-proposals-OC-ENW-M-round-26-27_EN.pdf` — call document.
- `LaTeX_application_forms/` — application templates and previous draft material.

Apart from the updated title, existing proposal files have not yet been reset.
Their previous content is not an approved basis for the new proposal.

## Abstract revision (2026-09-12)

- Adopted capitalization **On-TRAQ** in the LaTeX title and abstract.
- Replaced the abstract with the revised single-paragraph version at Alexios's
  request. It now introduces the deployment constraints of application-integrated
  cryptography, proxies, and network-layer protection before presenting the approach.
- Detailed comparisons and supporting citations remain work for A.2.
- The Summary and keywords still need updating; PDF page fit remains unchecked.

## Wording refinement (2026-09-12)

- Alexios prefers **system call**, without a hyphen; use this wording going forward.
- Updated the LaTeX abstract to name virtual machines, gateways, and proxies as
  existing solutions providing partial answers, replacing the explanation of
  individual limitations. The sentence now reads: "Existing solutions, such as
  virtual machines, gateways, and proxies, provide only partial answers to the
  challenge of transparently protecting application communication both within and
  across machines."
- Specific comparisons and evidence for this positioning remain to be developed
  in A.2; the abstract does not establish those comparisons by itself.

## Existing-solutions wording (2026-09-12)

- At Alexios's request, simplified the abstract's list to **virtual machines and
  security gateways**, removing the overlapping gateway/proxy enumeration.
- Current sentence: "Existing solutions, such as virtual machines and security
  gateways, provide only partial answers to the challenge of transparently
  protecting application communication both within and across machines."
- Alexios confirmed that the specific VM-based solutions will be identified and
  discussed later in A.2.

## Interposition terminology (2026-09-12)

- Alexios approved replacing "shared-memory-access interposition" with
  **interposition on shared memory accesses**.
- Updated both relevant abstract sentences in LaTeX. The joint mechanism is now
  phrased as **interposition on system calls and shared memory accesses**.
- Preserve this terminology in subsequent drafting.

## Summary and keywords draft (2026-09-12)

- Replaced the old ACCESS summary and keywords in the M-1 LaTeX file with a
  first On-TRAQ draft at Alexios's request; awaiting review of the wording.
- Summary is one paragraph for non-specialists: explains the quantum threat,
  the difficulty of updating existing software, communication within/across
  computers, the proposed security layer, and security/behaviour/performance
  evaluation. Avoids requiring readers to understand system call interposition.
- Five keywords: post-quantum cryptography; system call interposition; shared
  memory; transparent application retrofitting; end-to-end communication security.
- Title, abstract, summary, and keywords now all reflect On-TRAQ. Earlier notes
  saying the summary/keywords still need replacement are superseded.
- The combined A.1 page fit still needs verification in a compiled PDF.

## Existing-solutions mapping (2026-09-12)

Alexios requested establishing existing solutions before drafting A.2. Initial
primary-source check identified these comparison families (not a completed
literature review):
- TLS wrappers/proxies and security gateways: stunnel wraps existing services.
  https://www.stunnel.org/manual.html
- Service meshes: Istio supports workload communication protection through
  mutual TLS; ambient mode uses per-node ztunnel proxies. This is a key comparator
  for transparent, identity-aware communication protection.
  https://istio.io/latest/docs/ambient/overview/
- Network encryption: IPsec and WireGuard, including managed deployment through
  Cilium. Gateways and IPsec overlap: one is a deployment role, the other a protocol
  suite that can also run on hosts.
  https://www.rfc-editor.org/info/rfc4301/
  https://docs.cilium.io/en/stable/security/network/encryption-wireguard/
- Transparent transport encryption: tcpcrypt (RFC 8548), to inspect further for
  authentication and application-integration assumptions.
  https://www.rfc-editor.org/info/rfc8548/
- Cryptographic library upgrades/providers: already TLS-enabled applications may
  gain hybrid post-quantum key exchange through library upgrades; source changes
  are not invariably necessary. Distinguish key exchange from authentication.
  https://www.openssl-corporation.org/post-quantum.html
- Confidential VMs: AMD SEV protects data in use within the VM boundary. This is
  not automatically end-to-end communication encryption. VM-based network
  appliances instead belong with gateways/tunnels. Specific VM work still needed.
  https://www.amd.com/en/developer/sev.html
  https://docs.amd.com/api/khub/documents/~uAtQszeypAVVEk_B91Ojg/content
- Kernel TLS is an adjacent implementation/offload mechanism, not a complete
  transparent retrofit: the documented interface requires TLS handshake setup.
  https://kernel.org/doc/html/latest/networking/tls.html

Implication for positioning: transparency alone is not a novelty claim. Compare
communication coverage, endpoint identity/trust boundaries, application changes,
post-quantum integration, and costs. Shared-memory protection needs an explicit
attacker model. No abstract changes made during this mapping.

## Limitations of existing approaches (2026-09-12)

User requested disadvantages of each comparison family. Treat these as scoped
trade-offs, not proof that On-TRAQ is superior:
- TLS wrappers/gateways: protection terminates at wrapper/gateway endpoints;
  application-to-wrapper segments need separate protection or trust. Service routing,
  credentials, and proxy operation remain deployment work; direct shared memory
  is outside the socket-wrapper path.
- Service meshes: deployment/control-plane/proxy dependencies and associated trust;
  network traffic mediation does not cover direct shared-memory accesses. Istio's
  security model documents proxy/node compromise implications and traffic capture
  limitations. Do not claim meshes lack workload identity.
  https://istio.io/latest/docs/ops/deployment/security-model/
- IPsec/WireGuard: IP traffic scope, tunnel/host endpoint trust, policy/key/routing
  administration; process identity requires additional integration. Cilium's
  WireGuard documentation explicitly excludes same-node packet encryption under
  its trusted-node model; this is implementation-specific, not a universal IPsec limit.
  https://docs.cilium.io/en/stable/security/network/encryption-wireguard/
- tcpcrypt: TCP-only scope, peer support, and separate endpoint authentication
  considerations; consult RFC 8548 for opportunistic-mode limitations.
  https://www.rfc-editor.org/rfc/rfc8548.html
- Library upgrades: help existing compatible TLS paths, not arbitrary plaintext
  or shared-memory communication; deployment compatibility and negotiated security
  still matter. Do not say application changes are always required.
- Confidential VMs: hardware/platform requirements; VM rather than per-process
  protection boundary; memory encryption alone does not secure outgoing channels.

For On-TRAQ, lower overhead, reduced configuration, complete mediation, and protection
against a compromised host remain unproven. Shared-memory encryption needs a defined
attacker who can access the shared region but not endpoints' plaintext/keys. Maintain
this distinction when using the comparison in the proposal. No LaTeX edits made.

## Simplified comparison table (2026-09-12)

- Alexios requested a simpler comparison and agreed to omit confidential VMs:
  they address a different protection problem and are not a direct communication
  retrofitting baseline. Library upgrades were already omitted as a separate row;
  they should not be characterized as unencrypted or improperly encrypted.
- Current table scope: TLS wrappers/security gateways; service meshes;
  IPsec/network tunnels.
- Proposed compact columns: approach; what it protects; main limitation for our
  scope. Focus on coverage and endpoints, avoiding an elaborate deployment matrix.
- The shared-memory gap is a scope distinction, not proof these solutions fail
  within their own threat models. On-TRAQ's threat model remains to be established.
- No LaTeX changes made. The abstract still names virtual machines and security
  gateways; this should be reconciled with the revised comparison when requested.

## IPsec deployment limitation (2026-09-12)

Alexios raised non-universal IPsec support. More precise framing: deployment
requires a compatible IPsec implementation and sufficient configuration privileges;
platform support does not mean every application operator can deploy it. strongSwan
explicitly documents host-stack and CAP_NET_ADMIN requirements for kernel IPsec
inside Docker. User-space IPsec implementations exist, so do not claim kernel
support is universally required. Suggested table wording: "Requires compatible
IPsec support and network configuration privileges; excludes shared-memory exchanges."
Sources:
- https://docs2.strongswan.org/docs/5.9/howtos/cloudPlatforms.html
- https://docs.strongswan.org/docs/latest/plugins/plugins.html
On-TRAQ's own privilege and portability requirements remain to be established.

## Research topic table added (2026-09-12)

- At Alexios's request, inserted the agreed three-row comparison table into A.2
  Research topic in the M-1 LaTeX file, with label `tab:existing-approaches`.
- Columns: approach; what it protects; main limitations for On-TRAQ's scope.
  Rows: TLS wrappers/security gateways, service meshes, and IPsec.
- Caption frames the comparison as coverage and deployment constraints.
- Used standard LaTeX tabular with wrapping columns and existing font size;
  no additional packages or template-style changes.
- References to representative systems still need adding when developing A.2;
  a LaTeX comment records this. PDF layout has not yet been verified.

## EU and Dutch motivation sources (2026-09-12)

User asked for EU/Netherlands articles on the quantum need; interpreted in project
context as the need for quantum-resistant security/migration. Primary sources found:

1. European Commission / NIS Cooperation Group, A Coordinated Implementation
   Roadmap for the Transition to Post-Quantum Cryptography, 23 June 2025.
   https://digital-strategy.ec.europa.eu/en/library/coordinated-implementation-roadmap-transition-post-quantum-cryptography
   News explanation:
   https://digital-strategy.ec.europa.eu/en/news/eu-reinforces-its-cybersecurity-post-quantum-cryptography
   Use for European urgency and coordinated migration targets. Describe roadmap
   targets as recommendations, not blanket legally binding deadlines.
2. ENISA, Post-Quantum Cryptography - Integration study, 18 October 2022.
   https://www.enisa.europa.eu/publications/post-quantum-cryptography-integration-study
   Introduction explains why algorithm standardization alone is insufficient:
   message sizes, performance, and interface differences complicate integration.
   Useful A.2 source; its historical standardization status is not current.
3. AIVD, Bescherm je nu tegen de dreiging van quantumcomputers, April 2026
   (date printed in PDF; URL contains a March date).
   https://www.aivd.nl/site/binaries/site-content/collections/documents/2026/03/27/bescherm-je-nu-tegen-de-dreiging-van-quantumcomputer-2026/bescherm-je-nu-tegen-de-dreiging-van-quantumcomputers-2026.pdf
   Printed p.4: store-now/decrypt-later threat, long-lived systems difficult or
   impossible to update, complex dependencies, and multi-year migration.
   Printed pp.6-7: recommends hybrid PQC; p.8 migration obstacles;
   pp.10-11 additional symmetric protection when timely PQC migration is infeasible.
   Strongest direct Dutch motivation for legacy retrofitting. Does not endorse
   On-TRAQ's specific mechanism or prove novelty.
4. AIVD/CWI/TNO, The PQC Migration Handbook, second edition, late 2024.
   https://english.aivd.nl/documents/2024/12/3/the-pqc-migration-handbook
   Announcement 3 December 2024:
   https://english.aivd.nl/latest/news/2024/12/03/aivd-cwi-and-tno-publish-renewed-handbook-for-quantum-safe-cryptography
   Practical Dutch migration reference; handbook not read in full in this search.
5. NCSC-NL, Wat is quantumveilige cryptografie? (current guidance page).
   https://www.ncsc.nl/quantumveilige-cryptografie/wat-is-quantumveilige-cryptografie
   Describes EU targets: end-2026 national roadmaps/stakeholder engagement;
   end-2030 high-risk cryptographic applications migrated, plans for others;
   end-2035 normal-risk and most low-risk applications migrated.
6. Commission Recommendation (EU) 2024/1101, 11 April 2024.
   https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ:L_202401101
   Foundational EU recommendation; 2025 roadmap is the more concrete follow-up.

Suggested use: A.2 motivate technical migration problem with AIVD 2026 + ENISA
2022; A.3 use EU roadmap and Dutch guidance for societal/policy relevance. No
LaTeX or bibliography changes requested/made. Avoid presenting any Q-Day year as
certain. Older NCSC 'Maak je organisatie quantumveilig' page flags itself as under
revision and contains stale pre-2024 standardization wording; prefer sources above.

## Cited motivation added to Research topic (2026-09-12)

- Inserted the two discussed motivation sentences before the comparison table:
  EU transition targets, followed by AIVD's legacy-system/multi-year migration
  concern and its relevance to practical retrofitting.
- Added bibliography entries `EC2025PQCTransition` (Commission news, 23 June 2025)
  and `AIVD2026QuantumThreat` (AIVD brochure, April 2026), with source URLs.
- Added corresponding LaTeX citations. Bibliography/PDF compilation has not yet
  been checked. Existing unused template bibliography entries remain.

## Confidential VMs with network protection (2026-09-12)

User requested checking integrated CVM solutions that also encrypt network traffic.
Found concrete examples, qualifying the earlier dismissal of CVMs as comparators:

- Contrast (Edgeless Systems): runs containers in confidential micro-VMs using a
  Kata/CoCo-based runtime; Coordinator attests workloads and issues certificates.
  Optional per-workload service mesh transparently wraps configured traffic in
  mTLS using an Envoy sidecar and iptables. Deployment annotations/configuration
  are needed; application TLS implementation is not needed for wrapped traffic.
  https://docs.edgeless.systems/contrast/architecture/overview
  https://docs.edgeless.systems/contrast/architecture/components/service-mesh
  https://www.edgeless.systems/products/contrast
- Constellation (Edgeless Systems): confidential Kubernetes nodes combined with
  Cilium/WireGuard network encryption. Historical comparator; current docs state
  no longer actively maintained, with development continuing in Contrast.
  https://docs.edgeless.systems/constellation/2.23/overview/confidential-kubernetes
  https://docs.edgeless.systems/constellation/next/architecture/networking
  Version-specific network coverage limitations must not be generalized.

Implication: bare CVM memory encryption does not encrypt the network, but complete
CVM-based systems do combine both. Contrast is a relevant concrete comparator,
possibly under service meshes rather than adding a generic CVM row. Platform
requirements (SEV-SNP/TDX, Kubernetes/runtime, attestation and mesh configuration)
are a defensible distinction; On-TRAQ's own requirements are still unsettled.
Shared memory within a CVM may be protected from an external host through the VM
boundary, even without per-access interposition; do not claim no memory protection.
No verified PQC guarantee found in reviewed docs; mTLS/attestation alone does not
establish quantum resistance. No LaTeX changes made for this lookup.

## VM-based comparison row restored (2026-09-12)

- Alexios requested including VM-based solutions in the Research topic table,
  following the identification of Contrast and Constellation.
- Added row: "VM-based solutions" / "Potentially both memory and network traffic"
  / "Potential performance overhead; hardware and runtime compatibility
  requirements; deployment complexity."
- This supersedes the earlier decision to omit VMs. Performance is phrased as a
  potential cost, not a measured universal disadvantage. Concrete supporting
  system references and comparisons still need integrating into the table/discussion.

## Expanded opening citations (2026-09-12)

- At Alexios's request, expanded the Research topic opening to explicitly name
  Dutch NCSC guidance and the joint AIVD/CWI/TNO migration handbook alongside
  the EU roadmap. Retained the AIVD 2026 legacy-system motivation and added
  ENISA's protocol-integration motivation.
- Added bibliography entries NCSCQuantumSafeGuidance (undated page, access date),
  AIVDCWITNO2024Handbook (second edition), and ENISA2022PQCIntegration.
- Opening now comprises three sentences; no PDF compilation performed.

## Dutch requirements versus recommendations (2026-09-12)

User asked whether Dutch government demands quantum resistance. Primary-source
check found government cryptographic-policy requirements and migration targets,
but did not establish a blanket Dutch law requiring every system to use PQC by 2030.

- Algemene Rekenkamer, Focus op quantum bij de rijksoverheid (2026), section 5.2.2,
  printed pp.33-34: government organizations are obliged to implement BIO, including
  cryptography/key-management policy; NIS2 does not explicitly require PQC. Section
  5.3.1 says QvC NL supports migration, with organizations determining when/how.
  https://www.tweedekamer.nl/downloads/document?id=2026D05382
- Rijksbreed beleidskader cryptografie, March 2025: mandatory government policy
  context; preparing for quantum-safe cryptography is explicitly a future development
  to address. Scope is central government, not a blanket private-sector PQC mandate.
  https://www.digitaleoverheid.nl/wp-content/uploads/sites/8/2025/03/Rijksbreed-Beleidskader-Cryptografie.pdf
  https://www.digitaleoverheid.nl/overzicht-van-alle-onderwerpen/quantumveilige-cryptografie/handige-hulpmiddelen/
- Dutch government speech delivered 2 December 2025, published 4 February 2026,
  points to 2030 for most important systems; this is policy direction, not itself law.
  https://www.rijksoverheid.nl/documenten/2026/02/04/toespraak-staatssecretaris-van-marum-tijdens-het-symposium-post-quantum-cryptography
- Staatscourant 2026, 24023 discusses quantum threat/crypto agility in draft Cbb
  Article 13 explanatory text. It is an advisory/draft publication, not sufficient
  evidence of enacted/in-force obligations; do not cite as a final PQC mandate.
  https://zoek.officielebekendmakingen.nl/stcrt-2026-24023.html

Proposal wording should distinguish existing cryptography/risk-management duties
from quantum migration guidance and targets. No LaTeX changes for this lookup.

## Bart Preneel talks on PQC migration (2026-09-12)

Alexios recalled a major talk by Bart Preneel (KU Leuven, Belgium). Found candidates,
but the particular remembered talk is not yet identified:
- Quantum Safe Migration: Technology and Policy Overview, PQCSA Workshop on
  Tackling the Quantum Threat, 12 September 2025. Public KU Leuven slides:
  https://www.esat.kuleuven.be/cosic/events/standardization-pqc-fundamentals/wp-content/uploads/sites/13/2025/09/BP_postquantum_12sep_2025_v1.pdf
- Post-Quantum Cryptography (PQC): The Risk of Being Late, SecAppDev,
  1 June 2026, 11:00-12:30. Organizer abstract covers standards, agency migration
  timelines, performance, and crypto agility. Published takeaway urges creating a
  migration strategy within six months if one is missing.
  https://secappdev.org/2026/sessions/post-quantum-cryptography-pqc-the-risk-of-being-late/
- Found ACM PQQS invited talk, Post-Quantum Cryptography: A Migration and Policy
  Perspective, 2-4 November 2026; FUTURE relative to this session, so cannot be the
  past talk recalled by Alexios.
  https://acm-pqqs.github.io/pqqs2026/team/invited-speaker.html
No proposal or bibliography changes made. Talks can supplement technical migration
motivation; official policy documents remain preferable for government targets.

## Preneel references accepted (2026-09-12)

- Alexios agreed to use both Preneel talks (September 2025 PQCSA and June 2026
  SecAppDev). Added bibliography entries Preneel2025QuantumSafeMigration and
  Preneel2026RiskOfBeingLate, with source URLs.
- Added a sentence in the Research topic opening citing both for the need to
  begin migration early. Government targets remain attributed to policy sources.
- Citation keys checked against bibliography entries; PDF not compiled.

## Impersonal expert-motivation wording (2026-09-12)

- Alexios requested avoiding naming Preneel directly in the motivation prose.
- Reworded the sentence to: "Expert discussions of post-quantum security also
  emphasize the need to begin migration early and the risks of delayed adoption",
  retaining both talk citations.
- Avoided claiming multiple scientists or scientific consensus on the basis of
  two talks by one speaker.

## Author comment command (2026-09-12)

- Added `\av{Your comment here}` to the M-1 LaTeX preamble at Alexios's request.
- Comments appear inline in dark green (`green!50!black`) for readability.
- Reuses xcolor already loaded by application.sty; color is scoped to the comment.

## Table reorganized by comparison criteria (2026-09-12)

- Alexios proposed columns for shared memory traffic, network traffic, deployment
  issues, and performance issues. Updated the LaTeX table accordingly, retaining
  Approach as the first column and all four approach families.
- Coverage qualifiers distinguish selected/enrolled network paths and VM-boundary
  memory protection. VM network protection requires an additional mechanism.
- Performance cells identify potential cost sources, not demonstrated slowdowns;
  caption makes this explicit. References/measurements remain to be added.
- Preserved Alexios's inline `\av{...}` comment above the table.
- Column widths account for inter-column padding; compiled layout remains unchecked.

## Coverage cell simplification (2026-09-12)

- At Alexios's request, VM-based solutions now show "Yes" for shared memory
  traffic. Explain in the surrounding text that this refers to protection within
  the VM boundary against external observers, not isolation among guest processes.
- TLS wrappers/gateways now show "Yes (except app-to-endpoint)" for network
  traffic. Other cells are unchanged.

## Service-mesh network coverage clarification (2026-09-12)

- Alexios asked whether service meshes provide total network protection. Answer:
  no universal guarantee; proxy-based mTLS protects the proxy-to-proxy segment,
  while app-to-proxy segments are normally inside a trusted local boundary and
  may remain plaintext. Enrollment, supported protocols, exemptions, and external
  traffic configuration affect coverage.
- Istio documents outgoing traffic capture limitations; its protocol-selection
  documentation distinguishes supported TCP traffic from non-proxied non-TCP traffic.
  https://istio.io/latest/docs/ops/deployment/security-model/
  https://istio.io/latest/docs/ops/configuration/traffic-management/protocol-selection/
- Proposed table wording: "Yes (except app-to-proxy)" with scope/configuration
  qualifications in surrounding text. No table edit made pending wording decision.

## Service meshes grouped with TLS wrappers/gateways (2026-09-12)

- Alexios proposed treating service meshes under the TLS tunnel/gateway umbrella.
  Removed the separate service-mesh table row and grouped proxy-based meshes with
  TLS wrappers/gateways. Added a LaTeX comment making this scope explicit.
- Updated deployment cell to "Proxy deployment, routing, and credentials".
- Current rows: TLS wrappers/gateways, IPsec, VM-based solutions.
- This groups the network-encryption mechanism, not all service-mesh functionality:
  workload identity, certificate automation, policy, and management still deserve
  mention when citing representative meshes. Integrated CVM+mesh systems remain
  relevant to the VM-based row; categories can overlap.

## Table row renamed to "Security gateways" (2026-09-12)

- Alexios requested renaming the "TLS wrappers / gateways" table row to
  "Security gateways" (settling on "security", not "secure", gateways).
- Updated the table row label only. The abstract already used "security
  gateways"; the summary does not name this approach, so no change was needed
  there.

## Network traffic column simplified for IPsec and VM-based rows (2026-09-12)

- Alexios requested changing the Network traffic cell to plain "Yes" for both
  IPsec (was "Yes, selected IP traffic") and VM-based solutions (was "With
  added network protection").
- The earlier qualifiers (selected-traffic scope for IPsec; added-mechanism
  dependency for VM-based network protection) are dropped from the table;
  Security gateways' cell still reads "Yes (except app-to-endpoint)".

## Deployment and Performance columns merged into Outstanding issues (2026-09-12)

- Alexios requested merging the Deployment issues and Performance issues
  columns into a single Outstanding issues column, and adjusted column widths
  accordingly (4 columns now, widths 0.18/0.15/0.15/remaining linewidth).
- Security gateways: Network traffic cell simplified to plain "Yes" (the
  app-to-endpoint qualifier moved out); Outstanding issues now reads "No
  coverage of app-to-endpoint and endpoint-to-app traffic". Deployment
  proxy/routing/credentials wording was dropped, per Alexios's specified
  replacement text.
- IPsec: Outstanding issues replaced with "Not supported everywhere",
  replacing the previous compatible-support/network-privileges and
  packet-processing/encryption wording.
- VM-based solutions: Outstanding issues replaced with "Virtualization cost,
  platform-specific hardware and runtime requirements", combining the former
  deployment and performance cells into Alexios's specified wording.
- Table caption still references "deployment requirements" and "performance
  costs" separately; may need reconciling with the merged column if requested.

## io_uring scoping decision (2026-09-12)

- Discussed whether two applications can communicate through io_uring: yes,
  chiefly via `IORING_OP_MSG_RING` (ring-to-ring messaging/fd passing) and by
  sharing/attaching io_uring instances across processes, both of which operate
  over the shared-memory submission/completion rings rather than one syscall
  per operation (especially under SQPOLL, where no syscall is needed at all).
- Alexios decided not to treat this as a separate case: io_uring-mediated
  app-to-app communication will be counted under "shared memory accesses" in
  On-TRAQ's scope, not as a third category alongside system calls and shared
  memory. Keep this framing when defining the interposition boundary in the
  Approach section.
- No LaTeX changes made for this decision.

## Table commented out; pipes/files added to abstract (2026-09-12)

- Alexios requested commenting out the comparison table rather than deleting
  it. Wrapped `tab:existing-approaches` in `\iffalse ... \fi` in the Research
  topic section, so it no longer renders but stays in the source for reference.
  This resolves Alexios's own `\av{Remove table ... pipes, files}` note, which
  was removed since it is now actioned.
- Alexios's other `\av{Applications can change but we need more
  straightforward ways to do it ...}` note is left untouched/unresolved.
- Added "such as sockets, files, and pipes" as concrete examples in the
  abstract's system-call-interposition sentence, per Alexios's request
  (sockets added in a follow-up correction). These are mediated through OS
  interfaces, so they fall under the system-call interposition mechanism, not
  shared memory.

## Scarlet/Mystes prior work reviewed; not to be cited (2026-09-12)

- Read `scarlet.pdf`: Alexios's own anonymous work-under-submission paper
  "Mystes: Practical, Secure, and Fast System Call Interposition" — a Linux
  binary-rewriting-based syscall interposer (zpoline-style redirection) with
  PKU-based in-process isolation/sandboxing, achieving near-native performance
  with strong security guarantees and no application/OS modifications.
- Alexios confirmed this should NOT be cited in the On-TRAQ proposal.
- Alexios plans to close the Research topic subsection with a paragraph on
  challenges of system call interposition, deliberately avoiding language that
  makes it sound like a solved/plug-and-play problem. Specific wording not
  yet drafted.
- Discussion also concluded (in the prior turn) that Approach, not Research
  topic, is where any mechanism specifics (e.g., binary rewriting) belong, and
  that Research topic figures illustrating syscall-mediated vs shared-memory
  communication are still an open idea, not yet drafted.

## Research topic structure agreed (2026-09-12)

- Alexios agreed on a five-part flow for Research topic: (1) opening
  motivation paragraph (kept similar to current), (2) simple figures on how
  applications communicate, (3) why existing solutions fail, (4) system call +
  memory interposition as the proposed direction, (5) why this is not trivial
  (challenges paragraph). Not yet drafted; existing-solutions content will
  likely need to stay compact prose given the 2-page budget.

## Communication diagrams drafted (2026-09-12)

- Created `LaTeX_application_forms/figures/communication-diagrams.drawio`, a
  two-page draw.io file per Alexios's requested layout:
  - Page 1 "Syscall-mediated communication": App -- syscall --> Channel
    <-- syscall -- App, labeled "Socket / Pipe / File" above the channel box.
  - Page 2 "Shared-memory communication": App -- memory access (read/write)
    --> Shared Memory <-- memory access (read/write) -- App.
- Rendered PNG previews via the draw.io desktop app's CLI
  (`/Applications/draw.io.app/Contents/MacOS/draw.io --export`) for review;
  Alexios has not yet confirmed the layout or approved embedding into the
  LaTeX Research topic section.
- Not yet embedded in the .tex file; would need export to PDF and
  `\includegraphics` once approved.
- Alexios reported the draw.io desktop app only showed the syscall page (tab
  visibility issue, not a broken file — the CLI export confirmed both pages
  render correctly). Per Alexios's request, split into two standalone files
  instead: `figures/syscall-communication.drawio` and
  `figures/shared-memory-communication.drawio`; the combined two-page
  `communication-diagrams.drawio` was deleted.
- Alexios then redesigned the figure directly in the draw.io app into a single
  combined diagram (`figures/communication.drawio`, exported to
  `figures/communication.drawio.svg`), with app icons, "system call"/"memory
  access" edge labels, and a "Socket File Pipe" cylinder plus a "Shared
  Memory" box — superseding the separate diagrams described above.
- Installed `resvg` via Homebrew (Alexios's request) to rasterize the SVG.
  draw.io's SVG export uses the CSS `light-dark()` color function and a
  `var(--ge-adaptive-bg, ...)` fallback for dark/light theme adaptivity, which
  resvg's CSS engine does not support, causing black fallback fills. Stripped
  these to their light-mode values directly in `communication.drawio.svg`
  before rendering with resvg to `figures/communication.png`. Alexios fixed a
  "Socker" -> "Socket" typo and re-exported the SVG from draw.io, which
  reintroduced the same `light-dark()`/`var()` CSS; repeated the same strip
  step and re-rendered successfully.
- Note for future re-exports from draw.io: any new export of
  `communication.drawio.svg` will need the same light-dark()/var() stripping
  before resvg can render it correctly.

## Figure embedded in Scientific proposal (2026-09-12)

- Inserted `\includegraphics{figures/communication.png}` as a figure
  (`fig:communication`) immediately before `\subsection{Research topic}`, per
  Alexios's request. Caption: "Applications can communicate through
  operating-system interfaces, such as sockets, files, and pipes, or through
  shared memory."
- Compiled the document with pdflatex to verify: builds successfully (5
  pages), figure renders correctly at full width on page 2, right before A.2.1
  Research topic. Pre-existing warnings (overfull hbox in Part B tables,
  duplicate section-name destinations, fancyhdr headheight) are unrelated to
  this change and were not addressed.

## Switched figure to vector PDF (2026-09-12)

- Alexios reported the embedded PNG looked blurry (raster scaled up to
  0.85\linewidth). resvg's CLI (0.48.1) only outputs PNG, no PDF, so used
  `rsvg-convert` (already installed) to convert the cleaned
  `communication.drawio.svg` (light-dark()/var() already stripped) to a
  vector `figures/communication.pdf` instead.
- Updated `\includegraphics{figures/communication.png}` to
  `figures/communication.pdf`. Recompiled successfully; text and lines are now
  sharp/vector instead of raster.
- Any future SVG re-export from draw.io will need the same light-dark/var
  stripping before rsvg-convert (not just resvg) can render it correctly.

## Terminology and caption changes; bibliography now shows URLs (2026-09-12)

- Alexios preferred "OS interfaces" over "operating-system interfaces";
  updated the abstract's system-call-interposition sentence accordingly.
- Rewrote the figure caption for non-expert readers: "Applications can
  communicate through OS interfaces using system calls, or through shared
  memory using memory accesses. Pipes, files, and shared memory can only be
  used for communication on the same machine, while sockets can be used for
  communication both on the same machine and across different machines."
- Alexios asked how to get the EC digital-strategy URL (and others) to show up
  in the reference list. Root cause: `\bibliographystyle{unsrt}` (plain
  unsrt.bst) silently drops the `url` field even though every .bib entry
  already had one. Fixed by switching to `unsrtnat` (natbib-compatible unsrt
  variant that prints "URL \url{...}"), adding `\usepackage{url}`, and adding
  the `numbers` option to `\usepackage{natbib}` (required — unsrtnat's .bbl
  looks like author-year format to natbib, which otherwise throws a
  "Bibliography not compatible with author-year citations" error).
- Recompiled with the full pdflatex/bibtex/pdflatex/pdflatex cycle (required
  after a bibliography style change): builds cleanly, all 7 references now
  show their full URL, and in-text citations remain plain numeric [1]-[7].

## Blue hyperlinks; removed "URL" label prefix (2026-09-12)

- Alexios asked for the URLs to be colored (e.g., blue). hyperref is already
  loaded by `application.sty` (with `pdfborder={0 0 0}`, no color), so added
  `\hypersetup{colorlinks=true, linkcolor=blue, citecolor=blue,
  urlcolor=blue}` in the main .tex preamble, scoped to this file only (did not
  touch the shared application.sty, which other form variants also use).
  Removed the separate `\usepackage{url}` line added earlier — redundant and
  loaded in the wrong order relative to hyperref (hyperref already provides
  its own `\url`).
- Alexios then found the literal "URL " text label before each link (from
  unsrtnat.bst's `format.url` function) ugly. unsrtnat.bst hardcodes this
  prefix, so copied it locally to
  `LaTeX_application_forms/unsrtnat-nolabel.bst` with that one line changed
  from `"URL \url{" url * "}" *` to `"\url{" url * "}" *`, and pointed
  `\bibliographystyle{}` at it instead of touching the system-installed style.
- Recompiled full cycle: URLs are now blue, clickable, and shown without the
  "URL" prefix; citation numbers are also blue via `citecolor`.

## Fixed stretched word spacing in bibliography (2026-09-12)

- Alexios noticed large gaps between words in the reference list. Cause:
  fully-justified text combined with long unbreakable URL strings forces
  LaTeX to stretch interword spaces on the same line to fill the column width.
- Fixed by wrapping `\bibliography{application}` in
  `\begingroup\raggedright ... \endgroup`, scoped to just the bibliography
  section (rest of the document remains fully justified). Recompiled
  successfully; text is now left-aligned/ragged-right with normal, even word
  spacing.

## Fixed orphaned "https:" URL line break (2026-09-12)

- Alexios noticed entry [5]'s URL broke as "https:" alone on one line, with
  "//secappdev.org/..." starting the next. Root cause took two attempts to
  find: `\url` typesets in math mode, where the colon character already has
  "Rel" (relation) math class by TeX's own plain default — independent of
  url.sty's `\UrlBreaks`/`\UrlBigBreaks` lists (removing `:` from
  `\UrlBigBreaks` alone, and separately trying `xurl`, both had no effect;
  `xurl` also introduced worse mid-word breaks in other entries and was
  reverted).
- Fix required BOTH: adding `:` to `\UrlOrds` (explicitly reclassifies it as
  ordinary/non-breaking) AND removing it from `\UrlBigBreaks` (processed
  later in url.sty's `\Url@MathSetup`, so it would otherwise override the
  `\UrlOrds` change back to breakable). Added in the preamble via
  `\makeatletter`/`\makeatother`, followed by `\urlstyle{tt}`.
- Recompiled successfully: entry [5]'s URL now wraps as a whole unit onto its
  own line instead of leaving "https:" orphaned; other entries unaffected.
- Alexios reported most other entries then looked worse (the earlier,
  narrower fix only touched ':'). Reverted, then Alexios asked to reinstate
  it with a broader goal: URLs should not break at all except when a full
  segment truly doesn't fit at the end of a line.
- Implemented by restricting URL breaking to "/" only: redefined
  `\UrlBreaks` to just `\do\/`, emptied `\UrlBigBreaks`, and moved every other
  previously-breakable character (`. @ \ ! _ | ; > ] :`) into `\UrlOrds`
  (ordinary/non-breaking), alongside the pre-existing ordinary set
  (`* - ~ ' "`). `\UrlNoBreaks` (`( [ { <`) left untouched (already
  non-breaking by "Open" math class). Followed by `\urlstyle{tt}` to force
  recomputation.
- Recompiled successfully: every reference now wraps only at "/" boundaries
  (path segments stay intact, e.g. entry [5]'s URL moves as a whole unit);
  no orphaned fragments or mid-word breaks anywhere in the list.

## Underlined acronym letters in the title (2026-09-12)

- Underlined the initial letters spelling TRAQ in the A.1 title:
  "On-TRAQ: \underline{T}ransparently \underline{R}etrofitting
  \underline{A}pplications for the \underline{Q}uantum Era". Recompiled
  successfully.

## Second Research topic paragraph drafted (2026-09-13)

- Added a new paragraph after the EU/Dutch motivation paragraph, per
  Alexios's content spec: briefly defines what a system call is, references
  Figure~\ref{fig:communication}, states that cross-machine communication
  uses sockets (system calls), that shared memory is the dominant local
  mechanism (efficient, no system calls needed), that files/pipes serve as a
  fallback (e.g. when shared memory is exhausted, or in legacy applications)
  and also require system calls, and that sockets can additionally be used
  locally.
- Added `\av{Need citation(s) for sockets, pipes, files, and shared memory as
  OS communication mechanisms.}` as a reminder note (no citation sourced yet).
- Recompiled successfully; paragraph renders on page 2 right after the figure.
  The two pre-existing `\av{}` planning notes below it were left in place
  (not yet fully resolved: "why existing solutions fail" and "why this is not
  trivial" still need drafting).

## Communication paragraph restructured (2026-09-13)

- Alexios rewrote the flow: open by listing all four mechanisms (sockets,
  shared memory, pipes, files) with the figure reference, then cross-machine
  communication (sockets create a channel between hosts; system calls defined
  inline at that point, not as a leading sentence), then same-machine
  communication (sockets/pipes/files as system-call-based options), ending
  with shared memory as the dominant/efficient local default and system-call
  techniques relegated to backup/legacy use.
  Replaced the previous version of this paragraph with this structure.
- Added `\cite{here}` as a literal inline placeholder (per Alexios's
  request) right after "backup or by legacy applications" — an intentionally
  undefined citation key that produces a harmless "Citation `here' undefined"
  warning and renders as "[?]" in the compiled PDF, marking exactly where a
  real reference is still needed. This replaces the earlier general `\av{}`
  reminder note about needing a citation, which was removed as superseded.
- Recompiled successfully (5 pages, one expected undefined-citation warning).

## Paragraph spacing fixed (2026-09-13)

- Alexios noticed paragraphs ran together with no visible gap. Cause:
  `application.sty` sets `\parindent=0pt` and `\parskip=0pt` for the whole
  template (likely deliberate, for precise page-limit control across the
  document), so consecutive paragraphs have neither indentation nor spacing.
- Rather than changing `\parskip` globally (risk of shifting page counts
  against the A.1/A.2/A.3 page limits), added an explicit `\medskip` between
  the motivation paragraph and the new communication paragraph in Research
  topic, consistent with the template's own use of explicit `\vspace`/skip
  commands elsewhere (e.g. after each `\section`).
- Recompiled successfully; visible gap now separates the two paragraphs. Will
  need the same explicit `\medskip` treatment between future paragraphs added
  elsewhere in A.2/A.3.

## Placeholder citation resolved: ReMon (USENIX ATC 2016) (2026-09-13)

- Alexios requested citing "Secure and Efficient Application Monitoring and
  Replication" (ReMon) to fill the `\cite{here}` placeholder in the
  communication paragraph. Confirmed via web search: Stijn Volckaert, Bart
  Coppens, Alexios Voulimeneas, Andrei Homescu, Per Larsen, Bjorn De Sutter,
  Michael Franz; USENIX ATC 2016, Denver, CO, pages 167-179. Alexios
  Voulimeneas (a co-author) is the applicant, so this is also a track-record
  reference, not just a topical one.
- Added bibliography entry `Volckaert2016ReMon` to application.bib and
  replaced `\cite{here}` with `\cite{Volckaert2016ReMon}` in the .tex file.
- Recompiled the full pdflatex/bibtex/pdflatex/pdflatex cycle: no undefined
  citations remain; reference [8] renders with full author list, venue,
  pages, and URL.
- Alexios then pasted the official ACM-exported BibTeX entry for this paper
  (Lastname-First author format, ISBN 9781931971300, exact booktitle/series
  wording, numpages). Merged those fields into the existing
  `Volckaert2016ReMon` entry (kept our own readable key rather than the
  numeric ACM key so `\cite{}` calls elsewhere need no change; omitted the
  long `abstract` field since unsrtnat-nolabel.bst never renders it and it
  would only bloat the .bib file). Recompiled successfully; entry [8] now
  also shows the ISBN and official proceedings title/series.

## Summary wording: avoid naming shared memory specifically (2026-09-12)

- Alexios requested phrasing the non-specialist Summary's communication-scope
  sentence as "between different machines, or even on the same machine"
  instead of naming shared memory explicitly.
- Updated sentence: "Applications also exchange information in different
  ways: between different machines, or even on the same machine."
- Note: the Abstract (peer-facing) still explicitly names shared memory
  accesses; this change applies only to the non-specialist Summary.
- Page fit for A.1 and A.2 (now shorter without the rendered table) has not
  been checked by compiling the document.

## Existing-solutions paragraphs drafted (2026-09-13)

- Added two new paragraphs to Research topic, per Alexios's content spec,
  replacing the resolved `\av{Applications can change...}` note:
  1. Rewriting-infeasibility paragraph: rewriting is an option but not always
     feasible — legacy software may only be available as a compiled
     executable (no source access), and even with source access, modifying
     it is error-prone; motivates migration-facilitating solutions instead.
  2. Existing-solutions paragraph: briefly describes and critiques security
     gateways (don't encrypt app-to-gateway/gateway-to-app segments; don't
     cover local communication — shared memory, pipes, files), IPsec (not
     deployed everywhere, adoption challenge; also doesn't cover local
     communication), and VM-based solutions (can in principle cover both
     local and network communication, but need extra hardware/application
     changes and add significant overhead).
- Added `\av{Need citations for security gateways, IPsec, and VM-based
  solutions when developing this discussion further.}` as a reminder (no
  citations sourced yet — earlier research from 2026-09-12 already identified
  candidates: stunnel, IPsec RFC 4301, Contrast/Constellation for VM-based).
- Recompiled successfully (6 pages total). Research topic content still fits
  on page 2 alone, well within its 2-page budget; the extra page in the
  overall document is unrelated to this section.
- The remaining `\av{ok then maybe the following...}` planning note still has
  two unresolved parts: "system call + memory interposition to the rescue"
  and "why that is not trivial" (closing challenges paragraph).

## Citations sourced for existing-solutions paragraphs (2026-09-13)

- Web-verified and added five bibliography entries:
  - `Stunnel2026Manual` (stunnel manual page) for the security-gateway
    description.
  - `Kent2005RFC4301` (RFC 4301, Kent & Seo, Dec 2005) for the IPsec
    description.
  - `EdgelessContrast2026` (Contrast architecture overview docs) for the
    VM-based-solutions description; also checked the service-mesh docs page,
    which confirms mTLS wrapping via Kubernetes annotations (application-side
    configuration) but does not itself state hardware requirements.
  - `GAO2025LegacySystems` (US GAO-25-107795, 2025) and `AcICT2025Legacy`
    (Dutch Adviescollege ICT-toetsing, "Problematische Legacy," 19 March
    2025) for the legacy-software/no-source-code claim, per Alexios's request
    for US + NL sources. Note: these establish that legacy systems (some on
    outdated languages/unsupported hardware) are hard/costly to
    replace/modify, which is adjacent to but not a verbatim match for "no
    source code access" specifically — worth flagging if Alexios wants a more
    literal source later.
  - A direct fetch of the AcICT PDF and its Next.js-rendered landing page both
    failed (404s / JS-rendered content not scrapable); relied on search-result
    snippets and secondary news coverage (Computable.nl, AgConnect, iBestuur)
    to confirm title, date, and substance instead.
- Rewrote both paragraphs to be more verbose per Alexios's request, weaving
  in the five citations at the relevant claims.
- Recompiled the full pdflatex/bibtex/pdflatex/pdflatex cycle: no undefined
  citations, all five render correctly ([9]-[13]). Research topic now spills
  a few lines onto page 3 — getting close to its 2-page budget as more
  content (the closing "why not trivial" paragraph) is still to be added.

## Page allocation revised (2026-09-13)

- Alexios reviewed actual page fit: Research topic currently runs a bit more
  than one page (confirmed: prose spills ~2 lines onto page 3, before the
  still-unwritten closing paragraph). Adding 1-2 more paragraphs for "why
  this is not trivial" is expected to bring Research topic to ~1.5-1.8 pages,
  down from the originally planned 2.00.
- Alexios is fine with this and will let Approach use "a bit more than 2.5"
  pages instead of exactly 2.50, since the two shifts roughly offset within
  the fixed 6-page A.2 total (Research topic + Approach + Justification +
  Embedding/expertise + Risk assessment). No hard numbers finalized for
  Approach yet.
- No LaTeX changes made for this planning note.

## Removed specific product names from text (2026-09-13)

- Alexios didn't want specific programs (stunnel, Contrast) named in the
  running text. Removed "such as stunnel" and "such as Contrast" from the
  security-gateway and VM-based-solutions sentences, keeping the general
  descriptions and retaining the `Stunnel2026Manual`/`EdgelessContrast2026`
  citations as supporting evidence (not named inline, but still cited).
- Recompiled successfully; text now reads generically for all three
  approaches (security gateways, IPsec, VM-based solutions).

## IPsec adoption citations added (2026-09-13)

- Found two sources for the IPsec adoption-challenge claim:
  - Ivan Pepelnjak (network-engineering expert), "Why is IPsec So Complex?"
    (ipSpace.net blog, Oct 2013) — argues standards-committee dynamics
    (optional SHOULDs/MAYs, vendor-driven features) produced an
    over-complex, poorly interoperable protocol.
  - strongSwan's own "Cloud Platforms" documentation, confirming concretely
    that kernel IPsec in Docker/cloud containers requires both a working
    host IPsec stack and CAP_NET_ADMIN privilege — direct support for the
    "sufficient configuration privileges... not available everywhere" claim.
    Flagged to Alexios: this strongSwan docs site currently serves an
    EXPIRED TLS certificate (content itself still legitimate, fetched via
    curl -k after WebFetch refused it).
- Added bibliography entries `Pepelnjak2013IPsecComplexity` and
  `StrongSwanCloud2026`; split the IPsec sentence to cite RFC 4301 (what it
  is), Pepelnjak (why interoperability/complexity limits adoption), and
  strongSwan docs (concrete privilege requirement) at their respective claims.
- Recompiled the full pdflatex/bibtex/pdflatex/pdflatex cycle: no undefined
  citations; both new citations ([13], [14]) render correctly.

## StrongSwan citation removed; general security-gateway citation added (2026-09-13)

- Alexios asked to remove the strongSwan citation (likely due to its expired
  TLS certificate, flagged earlier). Removed `\cite{StrongSwanCloud2026}`
  from the IPsec sentence and deleted the bib entry; kept the surrounding
  claim text (configuration-privilege requirement is a generally accepted
  technical fact, not solely dependent on that one source).
- Alexios then asked for a more general article about security gateways
  (rather than a single product's manual). Found "The Security Impact of
  HTTPS Interception" (Durumeric et al., NDSS 2017) — a highly-cited academic
  paper whose background section describes exactly the general TLS-proxy
  mechanism (terminate client TLS session, inspect, re-establish a new TLS
  connection to the destination) that our sentence describes.
- Alexios then clarified: keep both the general NDSS paper AND the specific
  stunnel manual as two citations, not a replacement. Final citation:
  `~\cite{Durumeric2017HTTPSInterception,Stunnel2026Manual}`.
- Recompiled the full pdflatex/bibtex/pdflatex/pdflatex cycle: no undefined
  citations; both citations render ([11], [12]) at the security-gateway
  sentence, IPsec now cites only RFC 4301 and Pepelnjak's complexity blog
  post ([13], [14] after renumbering).

## General citation added for VM-based solutions (2026-09-13)

- Alexios asked for a more general citation for the VM-based-solutions claim
  (previously only cited Contrast's own docs). Found "Confidential VMs
  Explained: An Empirical Analysis of AMD SEV-SNP and Intel TDX" (Misono,
  Stavrakakis, Santos, Bhatotia; POMACS Vol. 8, No. 3, Article 36, 2024) — a
  vendor-neutral empirical study covering both major confidential-computing
  hardware platforms, directly supporting the hardware-requirement and
  performance-overhead claims.
- Added bibliography entry `Misono2024ConfidentialVMs` and cited it alongside
  the existing `EdgelessContrast2026`, matching the two-citation
  (general + specific) pattern already used for security gateways.
- Recompiled the full pdflatex/bibtex/pdflatex/pdflatex cycle: no undefined
  citations; all three existing-solutions paragraphs now each cite one
  general academic/standards source plus one concrete system example
  (security gateways: NDSS 2017 + stunnel; IPsec: RFC 4301 + Pepelnjak;
  VM-based: Misono et al. 2024 + Contrast).

## Approach-direction paragraph drafted (2026-09-14)

- Added the "system call + memory interposition to the rescue" paragraph,
  based on Alexios's dictated content (deliberately kept at Research-topic
  altitude, no mechanism specifics like binary rewriting/PKU, consistent with
  the earlier decision that those belong in Approach):
  central idea = one security layer interposing ALL application
  communication, same-machine or cross-machine; unifying observation that
  every communication method ultimately passes through memory (system calls
  use application-supplied memory buffers; shared memory is accessed
  directly); therefore interpose both system calls and shared-memory
  accesses, inserting a post-quantum protection layer there so data is
  transparently encrypted/decrypted at each end without application changes.
- This resolves the "system call + memory interposition to the rescue" part
  of the long-standing `\av{}` planning note; replaced it with a shorter
  `\av{why that is that not trivial}` reminder for the one remaining
  unwritten piece (the closing challenges paragraph).
- Recompiled successfully (7 pages total). Research topic content now runs
  to roughly 1.15 pages, well within the (already relaxed) budget, even
  before the closing paragraph is added.

## Closing challenges paragraph drafted — Research topic complete (2026-09-14)

- Alexios asked to draft the final "why this is not trivial" paragraph,
  explicitly drawing on the reasoning in scarlet.pdf's (Mystes) Background
  section (cross-process designs are slow; in-process/binary-rewriting
  designs have compatibility and security issues) while NOT citing Mystes
  itself (standing decision from earlier). Instead, traced the reasoning back
  to the actual published sources Mystes itself relies on:
  - Jacobs, G\"ulmez, Andries, Volckaert, Voulimeneas, "System Call
    Interposition Without Compromise" (DSN 2024) — another of Alexios's own
    published papers (lazypoline) — cited for both the cross-process
    (ptrace-style) context-switch overhead claim and the binary-rewriting
    compatibility/dynamically-generated-code limitation claim (verified by
    reading the actual paper PDF).
  - Vahldiek-Oberwagner et al., "ERIM: Secure, Efficient In-Process Isolation
    with Protection Keys (MPK)" (USENIX Security 2019) — cited for the
    in-process security/tampering concern that motivates hardware-based
    isolation.
- Added bibliography entries `Jacobs2024LazypolineSyscall` and
  `Vahldiek2019ERIM`. Wrote the paragraph at Research-topic altitude (states
  the tension/challenge, not a mechanism design), ending on a sentence tying
  it back to On-TRAQ's own goal (resolve this tension for both system calls
  and shared memory, plus PQC computational cost).
- Fixed a missed `\medskip` before this paragraph (first compile ran it into
  the previous paragraph with no gap).
- Recompiled the full pdflatex/bibtex/pdflatex/pdflatex cycle: no undefined
  citations (new citations render as [17], [18]); Research topic is now
  fully drafted end-to-end (motivation, communication paths,
  rewriting-infeasibility, existing-solutions, approach-direction, closing
  challenges) at roughly 1.4 pages — within the revised 1.5-1.8 page target.
  No `\av{}` planning notes remain in this subsection.

## Generalized closing paragraph beyond system calls (2026-09-14)

- Alexios pointed out the closing challenges paragraph was framed only
  around system calls, but the same cross-process/in-process tension
  (overhead vs. compatibility/security) applies to memory-access
  interposition too. Reworded to speak generally about "interposition
  techniques, whether applied to system calls or to memory accesses,"
  keeping the concrete binary-rewriting example phrased to cover both
  ("the relevant instructions, whether system calls or memory accesses").
  Citations unchanged (still anchored to the syscall-specific illustration
  they were verified against).
- Recompiled successfully.

## Clarified final sentence: PQC cost accepted, interposition cost is the concern (2026-09-14)

- Alexios clarified that the additional computational cost of post-quantum
  cryptography itself is accepted/expected; the actual concern is that the
  interposition mechanism must not add further overhead on top of that
  unavoidable crypto cost.
- Reworded the closing sentence from "...while additionally accommodating
  the computational cost of post-quantum cryptographic operations" to
  "...so that the interposition layer itself does not introduce overhead
  beyond the unavoidable cost of the post-quantum cryptographic operations
  it performs."
- Recompiled successfully.

## Made PQC-degradation acceptance explicit (2026-09-14)

- Alexios wanted it stated explicitly that some performance degradation from
  PQC itself is inevitable/expected and accepted; the actual goal is that the
  interposition mechanism adds no cost beyond that. Split into two sentences:
  "On-TRAQ must resolve this same tension for both system calls and shared
  memory accesses. Some performance degradation from the post-quantum
  cryptographic operations themselves is inevitable and expected; On-TRAQ's
  goal is to ensure that the interposition mechanism does not introduce
  additional overhead beyond this unavoidable cost."
- Recompiled successfully; Research topic still ~1.5 pages.

## Closed Research topic with two explicit research questions (2026-09-14)

- Alexios suggested closing Research topic with two central research
  questions. Drafted and added as a final capstone paragraph:
  - RQ1 (feasibility/transparency): can interposition on system calls and
    shared memory accesses provide a transparent, general mechanism for
    retrofitting quantum-resistant communication security without source
    changes?
  - RQ2 (security vs. overhead): what security guarantees can such a
    mechanism provide against a compromised application, achievable without
    overhead beyond the unavoidable PQC cost?
  Formatted inline with bold "RQ1:"/"RQ2:" labels rather than a bulleted
  list, to save vertical space under the page budget.
- Recompiled successfully; Research topic now ends with this capstone,
  running to roughly 1.6 pages total — still within the revised 1.5-1.8 page
  target. Research topic subsection is now considered complete pending
  Alexios's review.

## Research questions made more abstract, one per line (2026-09-14)

- Alexios wanted the two research questions more abstract and each starting
  on its own line. Reformatted as a numbered list (`enumerate`) instead of
  inline bold RQ1/RQ2 labels:
  1. Can quantum-resistant communication security be retrofitted into
     existing applications through interposition on system calls and shared
     memory accesses?
  2. Can this be achieved efficiently, securely, and transparently, without
     requiring changes to the applications themselves?
- Recompiled successfully; renders as a clean two-item numbered list. Research
  topic still ~1.6 pages total.

## Research questions shortened further (2026-09-14)

- Alexios asked to shorten the two RQs. Final wording:
  1. "Can an interposition layer retrofit quantum-resistant communication
     security into existing applications?"
  2. "Can such an interposition layer be built transparently, securely, and
     efficiently?"
- Each question now fits on a single line. Recompiled successfully; Research
  topic subsection is complete, ~1.55 pages total.

## Closing paragraph restructured around transparency (2026-09-14)

- Alexios asked to restructure the closing challenges paragraph similar to
  scarlet.pdf's (Mystes) framing (title: "Practical, Secure, and Fast"), but
  built around "transparently" as the single throughline property rather
  than opening with all three (transparent/efficient/secure) at once.
- Re-checked scarlet.pdf's Introduction per Alexios's request, specifically
  the sentence on intrusive alternatives: "several prior systems rely on
  application or platform modifications, such as kernel or hardware changes,
  or custom libOS and libc environments... at the cost of increased
  development and deployment complexity, reduced portability, higher
  maintenance overhead, and an expanded trusted computing base (TCB)." Not
  cited (Mystes remains uncited); reused only the general idea, independently
  phrased.
- Restructured the paragraph: opens with "Achieving this transparently is
  not trivial"; cross-process designs are explicitly framed as transparent
  but slow; in-process/binary-rewriting designs are explicitly framed as
  transparent but fragile/insecure; added a new closing clause on approaches
  that abandon transparency altogether via intrusive OS/hardware
  modifications or custom libOS environments, trading it for
  performance/security at the cost of deployment complexity, portability,
  and TCB size. On-TRAQ's sentence updated to add "without resorting to such
  intrusive modifications."
- Per Alexios's explicit instruction, the two research questions were left
  unchanged for now (may need revision later to match this reframing, but
  deferred).
- Recompiled successfully; Research topic still ~1.6 pages total.

## Split closing paragraph into two (2026-09-14)

- Alexios noted the restructured closing paragraph was too big. Split it
  after the intrusive-modifications sentence (end of the "landscape of
  approaches" content) and before "On-TRAQ must resolve this same tension...",
  with a `\medskip` between them. First paragraph now covers cross-process,
  in-process/binary-rewriting, and intrusive-modification approaches and
  their trade-offs; second paragraph ties this back to On-TRAQ's own goal and
  the accepted PQC overhead.
- Recompiled successfully; Research topic still ~1.65 pages total.

## Removed binary-rewriting mechanism detail from Research topic (2026-09-14)

- Alexios asked to drop the binary-rewriting-specific detail (variable-length
  instructions, dynamically generated/loaded code discovery limits) from the
  in-process designs sentence, keeping only the general description
  (executes in the application's address space) and the security
  consequence (compromised application can tamper with/bypass it without
  hardware-based isolation). Consistent with the standing rule that
  mechanism-level detail belongs in Approach, not Research topic.
- `Jacobs2024LazypolineSyscall` is now cited only once (for the cross-process
  overhead claim); `Vahldiek2019ERIM` citation for the in-process security
  claim is unchanged.
- Recompiled successfully; Research topic slightly shorter now.

## Alexios manually simplified the closing paragraph (2026-09-14)

- Alexios edited the .tex file directly to simplify the closing challenges
  paragraph further: removed the opening "Achieving this transparently is
  not trivial" topic sentence and the repeated "transparent"/"give up
  transparency" callouts for each approach category, leaving a more direct
  statement of each approach's trade-off (cross-process: no app changes but
  slow; in-process: avoids overhead but security risk without hardware
  isolation; intrusive modifications: better performance/security at the
  cost of deployment complexity, portability, and TCB size).
- Verified: recompiles cleanly, both citations ([17], [18]) still resolve
  correctly, Research topic still ~1.55-1.6 pages total.

## Swapped citations: zpoline + ReMon, and added "You Shall Not (by)Pass!" (2026-09-14)

- Alexios asked to replace the `Jacobs2024LazypolineSyscall` citation (used
  for the cross-process context-switch-overhead claim) with zpoline and
  ReMon instead, and to additionally cite "You Shall Not (by)Pass!" alongside
  ERIM for the in-process security claim.
- Per Alexios's request, re-checked scarlet.pdf's (Mystes) full reference
  list (all 136 entries, pages 12-15) to verify these papers are legitimate.
  Confirmed present exactly as expected: [131] zpoline (Yasukata et al., ATC
  2023) and [119] "You shall not (by)pass!" (Voulimeneas, Vinck, Mechelinck,
  Volckaert; EuroSys 2022). Flagged one honest discrepancy to Alexios: ReMon
  ("Secure and Efficient Application Monitoring and Replication," Volckaert
  et al., ATC 2016) is NOT in Mystes' reference list (a different 2016
  Volckaert paper, "Cloning your gadgets," is [117] instead) — proceeded to
  cite it anyway since it's a real, already-used paper in our own bibliography
  and Alexios confirmed the intent regardless.
- Added bibliography entries `Yasukata2023Zpoline` (pages 293-300) and
  `Voulimeneas2022YouShallNotBypass` (DOI 10.1145/3492321.3519560). Removed
  the now-unused `Jacobs2024LazypolineSyscall` entry entirely (was replaced,
  not supplemented, per "instead").
- Updated citations: cross-process overhead sentence now cites
  `{Yasukata2023Zpoline,Volckaert2016ReMon}`; in-process security sentence
  now cites `{Vahldiek2019ERIM,Voulimeneas2022YouShallNotBypass}`.
- Recompiled the full pdflatex/bibtex/pdflatex/pdflatex cycle: no undefined
  citations. ReMon correctly reuses its earlier citation number [8] (already
  cited once in the communication paragraph); new entries render as [17] and
  [19] respectively. Verified all 19 entries in the compiled reference list.

## Full citation restructure per scarlet.pdf's related-work grouping (2026-09-14)

- Alexios asked to move zpoline to the in-process sentence (it was misplaced
  on the cross-process one) and add lazypoline and K23 there too; add Jenny,
  Donky, and Hodor for the OS/hardware-modification clause; and add
  Endokernel for the "custom libOS/libc environments" clause. Verified all
  against scarlet.pdf's (Mystes) actual related-work text and reference list
  (re-read pages 11, 13, 14, 15):
  - Page 11 Discussion: "recent work [59] discovered multiple issues in both
    approaches [64, 131]" confirms zpoline [131], lazypoline/Jacobs et al.
    [64], and K23/Clair Obscur [59] are literally grouped together in Mystes
    for exactly this in-process/binary-rewriting point.
  - Page 11: "intrusive techniques that rely on hardware or OS modifications
    [3, 32, 34, 38, 52, 60, 74, 85, 95, 115, 119, 122, 136]" confirms Hodor
    [60] is in that bucket (Jenny/Donky are not explicitly in that exact
    bracket in Mystes, but Alexios asked for them there regardless — both are
    PKU/RISC-V-hardware-dependent isolation systems, a reasonable fit).
  - Exact citations transcribed directly from the reference list images:
    Jenny [105] (Schrammel et al., USENIX Security 2022), Donky [106]
    (Schrammel et al., USENIX Security 2020), Hodor [60] (Hedayati et al.,
    ATC 2019), Endokernel [130] (Yang et al., ATC 2024), K23/Clair Obscur
    [59] (G\'omez et al., ACM/IFIP Middleware 2025).
- Re-added `Jacobs2024LazypolineSyscall` (deleted in a previous turn) and
  added `Gomez2025ClairObscur`, `Schrammel2022Jenny`, `Schrammel2020Donky`,
  `Hedayati2019Hodor`, `Yang2024Endokernel` to application.bib.
- Reworded the intrusive-modifications sentence to split OS/hardware
  citations from a new libOS/libc clause, using Mystes' own phrase "custom
  libOS and libc environments" adapted to "custom library operating system
  (libOS) or libc environments" (Alexios asked how to phrase this).
- Final citation layout: cross-process overhead -> ReMon only; in-process
  design -> zpoline + lazypoline + K23; in-process security -> ERIM + You
  Shall Not (by)Pass!; OS/hardware modifications -> Jenny + Donky + Hodor;
  libOS/libc environments -> Endokernel.
- Recompiled the full pdflatex/bibtex/pdflatex/pdflatex cycle: no undefined
  citations; all render correctly ([8], [17]-[25]).

## Added GHUMVEE, strace, gdb to cross-process citation (2026-09-14)

- Alexios asked to add GHUMVEE, strace, and gdb as citations for the
  cross-process designs sentence, and to check scarlet.pdf for them.
- Important correction: searched scarlet.pdf's full extracted text
  thoroughly and found NO mention of "GHUMVEE" or "ReMon" anywhere in the
  paper — an earlier claim in this session that Mystes discusses "a hybrid
  MVEE design—ReMon—that uses an existing, isolated CP monitor (GHUMVEE)"
  was a false memory and did not come from this paper. Flagged this
  correction to Alexios. `strace` [22] and `gdb` [4] ARE genuinely in
  Mystes' reference list, cited exactly as bare manual-page URLs (no
  authors), matching the style used here.
- Verified GHUMVEE independently as a real, separate paper: "GHUMVEE:
  Efficient, Effective, and Flexible Replication" (Volckaert, De Sutter, De
  Baets, De Bosschere; FPS 2012/2013, pp. 261-277) — not from Mystes'
  bibliography, but legitimate and added per Alexios's explicit request
  (same pattern as ReMon earlier).
- Added bibliography entries `Volckaert2013GHUMVEE`, `GdbManual2026`, and
  `StraceManual2026`. Updated the cross-process sentence to cite
  `{Volckaert2016ReMon,Volckaert2013GHUMVEE,StraceManual2026,GdbManual2026}`.
- Recompiled the full pdflatex/bibtex/pdflatex/pdflatex cycle: no undefined
  citations; cross-process sentence now cites [8, 17, 18, 19].

## Removed specific access-day from all citations (2026-09-14)

- Alexios asked for all "accessed" dates in the bibliography to show only
  month/year (September 2026), not a specific day. Updated 5 entries via
  sed: NCSCQuantumSafeGuidance, Stunnel2026Manual, GdbManual2026,
  StraceManual2026, EdgelessContrast2026 — all now read "Accessed September
  2026" / "accessed September 2026" instead of a specific date (12th, 13th,
  or 14th).
- Recompiled the full pdflatex/bibtex/pdflatex/pdflatex cycle: no errors;
  verified via pdftotext that all 5 access notes render as month-only.

## Cross-process sentence reworded; added PKU Pitfalls citation (2026-09-14)

- Alexios asked to drop the "requires no changes to the application" claim
  from the cross-process sentence, and instead explain that cross-process
  designs are secure because of process isolation. Reworded: "Such designs
  are secure, since process isolation prevents a potentially compromised
  application from tampering with the interposition logic; however, the
  frequent context switches required to hand control to the tracer on every
  intercepted operation introduce substantial performance overhead."
- Alexios also asked to cite "PKU Pitfalls" (Connor, McDaniel, Smith,
  Schuchard; USENIX Security 2020 — ref [43] in scarlet.pdf) alongside ReMon
  for the ptrace/context-switch overhead claim, noting that paper also shows
  the cost of ptrace. Added bibliography entry `Connor2020PKUPitfalls` and
  updated the citation to `{Volckaert2016ReMon,Connor2020PKUPitfalls}`.
- Recompiled the full pdflatex/bibtex/pdflatex/pdflatex cycle: no undefined
  citations; overhead claim now cites [8, 20].

## Closing paragraph rewritten; RQ2 simplified to transparency only (2026-09-14)

- Alexios rewrote the final paragraph's message: On-TRAQ's aim is a
  practical approach for secure and efficient retrofitting, with close
  attention to usability/security/performance side-effects since these
  typically hinder adoption; kept the existing point that PQC's own
  performance degradation is inevitable/accepted and the interposition
  mechanism itself must not add to it.
- RQ1 unchanged. RQ2 simplified per Alexios's request from "Can such an
  interposition layer be built transparently, securely, and efficiently?"
  to just "Can such an interposition layer be built transparently?" —
  security/efficiency goals now live in the prose paragraph above instead of
  the RQ itself.
- Recompiled successfully.

## Merged the two research questions into one (2026-09-14)

- Alexios asked to merge the two research questions into a single one,
  folding "transparently" in as a modifier. Replaced the two-item enumerate
  list with one inline sentence: "On-TRAQ is therefore guided by a central
  research question: can an interposition layer transparently retrofit
  quantum-resistant communication security into existing applications?"
- Recompiled successfully; Research topic subsection is complete, ~1.5 pages.

## Research question visually emphasized (2026-09-14)

- Alexios asked for the research question to stand on its own line, centered,
  and emphasized. Wrapped it in `\begin{center}\textit{...}\end{center}`,
  separated from the "On-TRAQ is therefore guided by a central research
  question:" lead-in sentence.
- Recompiled successfully; renders as an italicized, centered statement.
  Research topic still ~1.55 pages total; subsection is complete.

## Added quotes and rebalanced line break in research question (2026-09-14)

- Alexios wanted quotation marks around the research question and a more
  balanced line wrap (previously only "applications?" sat alone on the
  second line). Added LaTeX curly quotes (``...'') and a manual `\\` break
  after "quantum-resistant", giving two evenly balanced lines.
- Recompiled successfully.

## In-process paragraph restructured: heuristics vs. representative inputs (2026-09-14)

- Alexios asked to remove the zpoline/lazypoline/K23 citations from the
  general "in-process designs avoid this overhead" sentence, and instead add
  a new sentence naming the practical problems these binary-rewriting
  approaches face: depending on brittle heuristics to identify/rewrite
  instructions (cite zpoline + lazypoline), or requiring representative
  inputs to discover them ahead of time (cite K23), per scarlet.pdf's own
  distinction between these approaches.
- New text: "State-of-the-art approaches leverage binary rewriting to
  redirect the relevant instructions directly to the interposition logic
  without incurring additional mode switches. However, such approaches face
  practical problems: they typically depend on brittle heuristics to
  correctly identify and rewrite the relevant instructions
  [zpoline, lazypoline], or require representative inputs to discover them
  ahead of time [K23]." Changed the following sentence's "However" to
  "Moreover" to avoid repetition.
- Recompiled successfully; citations render as [21, 22] and [23]. Research
  topic still ~1.6 pages.

## Trimmed in-process/binary-rewriting explanation for brevity (2026-09-14)

- Alexios asked to be less verbose here since Approach will cover
  binary-rewriting mechanism detail more fully. Condensed three sentences
  into one: "In-process designs avoid this overhead by executing the
  interposition logic within the application's own address space, typically
  using binary rewriting. However, such approaches depend on brittle
  heuristics [zpoline, lazypoline] or representative inputs [K23] to
  correctly identify the relevant instructions, and, because the
  interposition logic runs in the same address space as the application, a
  compromised application can, in principle, tamper with or bypass it
  entirely unless additional hardware-based isolation is introduced [ERIM,
  You Shall Not (by)Pass!]." All citations preserved, just fewer words.
- Recompiled successfully; Research topic back down to ~1.5 pages.

## Added scarlet-style opening sentence to the challenges paragraph (2026-09-14)

- Alexios asked for an opening similar to scarlet.pdf's own framing (existing
  approaches struggle to jointly achieve strong security and performance).
  Added: "Existing interposition solutions come with limitations. In this
  paragraph, we discuss the main approaches and their trade-offs." right
  before "Interposition techniques, whether applied to system calls...".
- Noted Alexios's own manual edits since the last check: removed the
  `\cite{Vahldiek2019ERIM,Voulimeneas2022YouShallNotBypass}` citation from
  the tampering clause (now uncited), shortened "custom library operating
  system (libOS) or libc environments" to "custom libOS/libc environments",
  and added "(TCB)" spelled out. Also noticed a new `\av{Hardware and binary
  rewriting agnostic ...}` note started under Approach — left untouched as
  Alexios's own in-progress marker for that section.
- Recompiled successfully.

## Research question reworded (2026-09-14)

- Alexios rephrased the research question to lead with "Can we transparently
  retrofit..." rather than making "interposition layer" the subject.
  Final wording: "Can we transparently retrofit quantum-resistant
  communication security into existing applications using an
  interposition-based approach?" Recompiled successfully; renders as two
  balanced centered lines.

## Abstract opening question reworded (2026-09-23)

- Alexios proposed rewording the abstract's embedded opening question to
  "How can existing applications gain quantum-resistant communication with
  minimal changes?" — more direct than the previous "acquire quantum-resistant
  communication without extensive changes to their implementation".
- Updated in place, keeping the lead-in clause ("The transition to
  post-quantum cryptography presents a challenge that extends beyond
  replacing cryptographic algorithms:"), which was not discussed for removal.
- Recompiled successfully (7 pages, unchanged).

## Abstract: assertive "We propose On-TRAQ" opener (2026-09-23)

- Alexios flagged two abstract weaknesses: no plain "On-TRAQ is..." statement,
  and "investigates whether ... can provide" hedges on the core mechanism.
- Replaced the two sentences "On-TRAQ investigates whether interposition on
  system calls and shared memory accesses can provide a transparent
  foundation for this transition. The project will develop a layer that
  mediates application communication and applies quantum-resistant
  protection without requiring application source-code modifications." with
  one declarative sentence: "We propose On-TRAQ, a systems approach to
  retrofitting quantum-resistant communication security into existing
  applications through interposition on system calls and shared memory
  accesses, without requiring application source-code modifications."
- This is the abstract's first first-person ("we") usage; rest of the
  abstract remains third-person ("the project will...", "On-TRAQ aims to...").
  Flagged to Alexios as a deliberate, common grant-abstract pattern, not
  reconciled further since he confirmed this wording.
- Recompiled successfully (7 pages, unchanged).

## Summary opening sentence strengthened (2026-09-23)

- Alexios's cryptographer friend suggested changing "could" to "will" and
  strengthening "some of" toward crucial/critical framing in the Summary's
  first sentence.
- Changed "Future quantum computers could break some of the cryptographic
  methods used today to protect digital communication." to "Future quantum
  computers will break critical cryptographic methods used today to protect
  digital communication." — dropped "some of" entirely rather than inserting
  "critical" alongside it, since keeping "some of" would still read as
  softened. Defensible: the algorithmic result (quantum computers breaking
  RSA/ECC via Shor's algorithm) is settled, so the uncertainty is about
  timeline, not outcome, matching the "will break" framing.
- Recompiled successfully (7 pages, unchanged).

## Summary closing sentence strengthened (2026-09-23)

- Alexios flagged the Summary's closing sentence as weak. Changed "The aim
  is to help organizations prepare their existing software for the quantum
  era while reducing the need to rewrite applications." to "On-TRAQ will
  help organizations prepare their existing software for the quantum era
  without rewriting their applications." — dropped the "The aim is to"
  framing, made On-TRAQ the subject again (bookending the paragraph), and
  switched "reducing the need to rewrite" to "without rewriting", matching
  the stronger "without requiring changes to the applications' source code"
  claim already stated mid-paragraph.
- Recompiled successfully (7 pages, unchanged). Summary subsection is now
  fully strengthened per Alexios's and his cryptographer friend's feedback.

## Summary closing sentence mirrored to abstract's ending (2026-09-23)

- Alexios asked for the Summary's closing sentence to mirror the abstract's
  ending structure ("By separating communication security from application
  implementation, On-TRAQ aims to provide a practical migration path for
  existing software into the quantum era.").
- Replaced the previous closing sentence ("On-TRAQ will help organizations
  prepare their existing software for the quantum era without rewriting
  their applications.") with "By adding this protection separately from the
  applications themselves, On-TRAQ will give organizations a practical way
  to move their existing software into the quantum era." — non-specialist
  translation of the same "separating X" + "practical migration path"
  structure, kept assertive ("will give", not "aims to give"). The dropped
  "without rewriting" claim is already covered earlier in the same paragraph.
- Flagged to Alexios (not yet actioned): the abstract's own closing still
  reads "On-TRAQ aims to provide a practical migration path...", the same
  hedge word ("aims to") stripped from the Summary twice this session —
  worth reconciling for consistency if he wants the abstract's ending
  tightened too.
- Recompiled successfully (7 pages, unchanged).

## Summary: "partial answers" replaced with "partial protection" (2026-09-23)

- Alexios's feedback flagged "Existing solutions provide only partial
  answers to protecting these different exchanges without changing the
  applications themselves." as unclear ("answers" is vague, and "answers to
  protecting" is awkward grammar); Alexios agreed.
- Changed "partial answers to protecting these different exchanges" to
  "partial protection for these different exchanges". Fixes both the vague
  wording and the awkward grammar in one swap.
- Recompiled successfully (7 pages, unchanged). Note: the abstract has a
  similarly-worded but grammatically cleaner sentence ("provide only
  partial answers to the challenge of transparently protecting application
  communication..."), left unchanged since feedback was specific to the
  Summary and the abstract's phrasing is not grammatically awkward.

## Summary: "protection" ambiguity fixed by separating coverage from protection (2026-09-23)

- Alexios clarified the earlier feedback: the real issue is "protection" is
  used for two different things — the new quantum-resistant layer On-TRAQ
  adds (introduced in "bring new protection to existing software") and,
  confusingly, the same word for existing solutions' partial coverage in the
  next-but-one sentence, making "protection" read as if existing solutions
  already provide the new quantum-resistant layer, just partially.
- Changed "Existing solutions provide only partial protection for these
  different exchanges without changing the applications themselves." to
  "Existing solutions cover only some of these exchanges, without changing
  the applications themselves." — drops "protection" from this sentence,
  using "cover"/"exchanges" instead (a coverage-gap point, not a
  protection-strength point). "Protection" now consistently refers only to
  On-TRAQ's new layer throughout the rest of the paragraph; "this
  protection" in the following sentence still refers back cleanly to
  "bring new protection to existing software" two sentences earlier.
- Recompiled successfully (7 pages, unchanged).

## Summary: "protection" replaced with "cryptographic methods" as the driving noun (2026-09-23)

- Alexios asked to change "bring new protection to existing software" to
  "bring new cryptographic methods to existing software" — echoing sentence
  1's "cryptographic methods used today" (old methods break -> need new
  ones).
- Updated sentence 2 accordingly. Also updated the downstream reference in
  sentence 5 ("On-TRAQ will investigate a way to add this protection by
  placing a security layer...") to "add these methods", so it still points
  to a real antecedent (the new cryptographic methods) rather than reusing
  "protection" before that word is properly introduced. "Protection" is now
  first introduced fresh in sentence 6 ("This layer will apply protection
  designed to resist attacks by quantum computers...") as the layer's
  effect, and stays consistent through sentences 7-8.
- Recompiled successfully (7 pages, unchanged).

## Summary restructured: rewriting-infeasibility and existing-solutions-limitations added and reordered (2026-09-23)

- Alexios dictated a new flow for the Summary paragraph: motivation ->
  new cryptographic methods needed -> how applications exchange information
  -> applying these new methods via a security layer -> (new) rewriting
  applications directly is often difficult/costly and sometimes infeasible
  (e.g., no source-code access) -> (moved/reworded) existing solutions that
  retrofit this protection have several known limitations -> project's
  evaluation goals -> closing practical-migration-path sentence.
- Trimmed the ", which may be difficult or costly to modify" tail from the
  "new cryptographic methods" sentence (now developed into its own fuller
  sentence later).
- Moved and reworded the old "Existing solutions cover only some of these
  exchanges..." sentence to after the new rewriting-infeasibility sentence,
  now: "Existing solutions to retrofit this protection into existing
  software have several known limitations." -- introduces "retrofit" in the
  Summary for the first time, echoing the abstract's "retrofitting" and the
  title. Kept generic/non-specialist altitude (no enumerated limitations),
  consistent with the Summary's established simpler register vs. the peer-
  level Research topic section.
- Added new sentence: "Rewriting applications directly to add this
  protection is often difficult or costly, and sometimes not even feasible
  -- for example, when there is no access to the original source code."
- Recompiled successfully (7 pages, unchanged). Summary subsection is
  considered complete again pending Alexios's review.

## "Transparently" added before "retrofit" in Summary (2026-09-23)

- Alexios asked to add "transparently" before "retrofit" in "Existing
  solutions to retrofit this protection into existing software have
  several known limitations." Now reads "Existing solutions to
  transparently retrofit this protection into existing software have
  several known limitations." -- echoes the title's throughline term.
- Recompiled successfully (7 pages, unchanged).

## Summary: "On-TRAQ is an approach that..." added (2026-09-23)

- Alexios noted the Summary still never states what On-TRAQ is (same gap
  fixed in the abstract earlier), and that "approach" alone is enough here
  (no need for "systems approach" or further qualifiers, unlike the abstract).
- Changed "On-TRAQ will investigate a way to add these methods by placing a
  security layer at the points where applications exchange information." to
  "On-TRAQ is an approach that will add these methods by placing a security
  layer at the points where applications exchange information." Kept "will
  add" (future) rather than "adds" (present) to stay consistent with the
  rest of the paragraph's future tense; only the definitional "is an
  approach" clause is present tense.
- Recompiled successfully (7 pages, unchanged).

## Summary trimmed by Alexios; "protection" antecedent fixed again (2026-09-23)

- Alexios manually edited the .tex file directly, trimming the Summary down
  to its first five sentences (motivation, need for new cryptographic
  methods, how applications exchange information, rewriting-infeasibility,
  existing-solutions-limitations) -- removed the "On-TRAQ is an approach
  that will add these methods..." sentence, the security-layer description,
  the evaluation-goals sentence, and the closing practical-migration-path
  sentence. Treated as the current intentional baseline, not reverted.
- Alexios then flagged that within this trimmed version, "this protection"
  (used twice: rewriting-infeasibility and existing-solutions-limitations
  sentences) has no antecedent anymore, since the sentence that used to
  introduce "protection" via the security layer was removed. The only
  established noun at that point is "new cryptographic methods" (sentence 2).
- Fixed by replacing both instances of "this protection" with "these
  methods", matching the actual antecedent present in the paragraph.
- Recompiled successfully (7 pages, unchanged). Current full Summary text:
  motivation -> new cryptographic methods needed -> how applications
  exchange information -> rewriting-infeasibility (no source-code access
  example) -> existing-solutions-limitations (transparently retrofit).
  Summary subsection is shorter now and likely still being reworked/rebuilt
  by Alexios; not yet marked complete.

## Summary continued: rewriting vs. transparent retrofitting (2026-09-23)

- Alexios manually trimmed the Summary further on disk: removed the
  "Applications also exchange information..." sentence (per his note "do
  not care about local and remote communication" -- this detail is dropped
  from the Summary going forward) and changed "cryptographic methods" to
  "cryptographic techniques" in the second sentence.
- Alexios then dictated the next two sentences: "one way is to rewrite
  applications which is not always possible" and "transparently retrofitting
  is challenging and current solutions have several known limitations."
  Drafted and added: "One way to add these techniques is to rewrite the
  applications directly, but this is not always possible or practical:
  existing software is not always available with its original source code,
  and even when it is, rewriting can be difficult and costly. Transparently
  retrofitting these techniques into existing software is challenging, and
  current solutions have several known limitations." The "One way..."
  framing sets up an implicit contrast with On-TRAQ's own transparent-
  retrofit approach, to be introduced in a later sentence.
- Recompiled successfully (7 pages, unchanged). Current full Summary:
  motivation -> new cryptographic techniques needed -> rewriting directly is
  one way but often infeasible/costly -> transparent retrofitting is
  challenging and current solutions have limitations. Still missing:
  On-TRAQ's own approach/definition, evaluation goals, and closing sentence
  (all removed in Alexios's earlier trim); Summary not yet complete.

## "On the other hand" added before transparent retrofitting (2026-09-23)

- Alexios asked to add "on the other hand" before the transparent-
  retrofitting sentence, making the contrast with "One way is to rewrite
  the applications directly..." explicit rather than implicit.
- Now reads: "On the other hand, transparently retrofitting these
  techniques into existing software is challenging, and current solutions
  have several known limitations."
- Recompiled successfully (7 pages, unchanged).

## Summary: On-TRAQ description rewritten without "layer"/"protection" (2026-09-23)

- Alexios manually added back "On-TRAQ is an approach that will add these
  methods by placing a security layer at the points where applications
  exchange information. This layer will apply protection designed to
  resist attacks by quantum computers, covering communication both within
  and across computers without requiring changes to the applications'
  source code." as a separate paragraph, then asked to merge it into the
  same paragraph and rewrite avoiding the words "layer" and "protection",
  as two explicit steps: (1) identify all the points where applications
  exchange information, (2) apply the required cryptographic operations
  on the fly.
- Replaced with: "On-TRAQ is an approach that will first identify all the
  points where applications exchange information, whether within or across
  computers. It will then apply, on the fly, the cryptographic operations
  needed to secure this information against attacks by quantum computers,
  without requiring changes to the applications' source code." Merged into
  a single paragraph (removed the blank line/paragraph break).
- Recompiled successfully (7 pages, unchanged). Current full Summary:
  motivation -> new cryptographic techniques needed -> rewriting is one way
  but often infeasible/costly -> transparent retrofitting is challenging and
  current solutions have limitations -> On-TRAQ's two-step approach (identify
  exchange points, then apply crypto operations on the fly). Still missing:
  evaluation goals and closing sentence (removed in Alexios's earlier trim).

## Summary: closing sentence on usability/performance goal added (2026-09-23)

- Alexios asked for a closing sentence stating the project's goal is
  usability and performance, aiming to provide a viable migration solution
  for organizations.
- Added: "The project will focus on usability and performance, aiming to
  provide organizations with a viable solution for migrating their software
  into the quantum era." Kept future tense to match the two preceding
  sentences; ended with "into the quantum era" to match phrasing used
  elsewhere in the abstract/summary.
- Recompiled successfully (7 pages, unchanged). Summary subsection is now
  considered complete again: motivation -> new cryptographic techniques
  needed -> rewriting is one way but often infeasible/costly -> transparent
  retrofitting is challenging and current solutions have limitations ->
  On-TRAQ's two-step approach (identify exchange points, apply crypto
  operations on the fly) -> closing usability/performance/migration goal.
  Pending Alexios's final review.

## Summary: closing sentence expanded (security guarantees + adoption barriers) (2026-09-23)

- Alexios asked to expand the closing sentence: mention security guarantees
  alongside usability/performance, explain usability/performance as typical
  adoption barriers, and close with "All in all, On-TRAQ aims to provide a
  viable solution for organizations...".
- Replaced "The project will focus on usability and performance, aiming to
  provide organizations with a viable solution for migrating their software
  into the quantum era." with "In addition to the security guarantees of
  the solution, this project will also focus on usability and performance,
  since both are typically barriers to adoption. All in all, On-TRAQ aims
  to provide a viable solution for organizations that want to migrate their
  software into the quantum era." Fixed Alexios's "Except for" (reads as
  excluding) to "In addition to" (the intended meaning); fixed "On-Traw"/
  "biable" typos from his dictation.
- Note: this reintroduces "aims to provide" (present tense), matching the
  abstract's own still-unchanged closing wording -- Alexios's own dictation
  used this phrasing, so the earlier "will give"/"will focus" strengthening
  is superseded here by his explicit preference.
- Recompiled successfully (7 pages, unchanged). Summary subsection complete
  again pending final review.

## Research topic: smoother transition between paragraph 1 and 2 (2026-09-23)

- Alexios flagged feedback that the transition from the EU/Dutch motivation
  paragraph (ending "...motivating practical ways to retrofit
  quantum-resistant protection.") to the communication-methods paragraph
  (starting "Applications can communicate using various methods...") was
  abrupt.
- Added a bridging sentence at the start of paragraph 2: "Retrofitting this
  protection requires identifying every point at which applications
  exchange information." -- ties back to paragraph 1's closing "retrofit"
  language and motivates why communication methods/paths are discussed next.
- Recompiled the full pdflatex/bibtex/pdflatex/pdflatex cycle: no undefined
  citations; builds cleanly (7 pages).

## Figure PDF regenerated from re-exported SVG (2026-09-23)

- Alexios asked how to create a PDF from an SVG in figures/. Found
  `figures/communication.drawio.svg` had been freshly re-exported from
  draw.io today (14:08), newer than the existing `communication.pdf`
  (from the 12th) -- so the PDF was stale.
- Reused the established workflow: stripped draw.io's `light-dark()` and
  `var(--ge-adaptive-bg, ...)` CSS to their light-mode values (removed the
  dead `@supports` feature-detection block, replaced `var(--ge-adaptive-bg,
  X)` with `X`, and `light-dark(A, B)` with `A`, via a small Python script
  handling nested parens for `rgb(...)` args), then ran `rsvg-convert -f pdf
  -o communication.pdf communication.drawio.svg`.
- Recompiled the main document: builds cleanly (7 pages), figure renders
  correctly.
- Recipe for future re-exports, restated for reference: any new SVG export
  from draw.io needs the same light-dark()/var() stripping before
  rsvg-convert can render it correctly (resvg has the same limitation).
