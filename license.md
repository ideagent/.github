IDEAgent End User License Agreement (Developer EULA)
Last updated: [DATE]

This End User License Agreement ("Agreement") is a legal agreement between you, either an individual or a single entity ("You" or "Licensee"), and IDEAgent [PLACEHOLDER: legal entity/trade description, e.g. "Einzelunternehmen" — to be inserted once trade registration (Gewerbeanmeldung) is complete], registered at [ADDRESS], Germany ("Licensor", "we", "us") governing your use of the IDEAgent plugin(s) for JetBrains IDEs, the associated backend components (including but not limited to the gateway, MCP server, RAG server, and any other containers distributed alongside the plugin), and any related documentation (collectively, the "Software").

By downloading, installing, or using the Software, you agree to be bound by this Agreement. If you do not agree, do not install or use the Software.

1. Definitions
* "Software" means the IDEAgent JetBrains plugin(s), the RAG File Watcher plugin, and any Docker container images or backend services distributed or made available by Licensor for self-hosted operation with the plugin(s), including updates.
* "Agent" means any autonomous or semi-autonomous AI coding agent, tool-calling process, or automated code-modification feature operating within the Software, whether powered by a third-party LLM provider (e.g. Anthropic) or a locally-hosted model (e.g. via Ollama).
* "Modification" means any change to the Software's source code, configuration, container images, deployment environment, or runtime behavior made by You or on Your behalf, other than through an official update released by Licensor.
* "Output" means any code, file change, command, suggestion, or other content generated, executed, or applied by an Agent.

2. License Grant
Subject to Your compliance with this Agreement, Licensor grants You a limited, non-exclusive, non-transferable, revocable license to install and use the Software for Your own internal development purposes, in accordance with the Documentation and any applicable pricing tier.

2.1 Beta Release. The Software is currently distributed as a beta release. Licensor may add, remove, or change features, APIs, and licensing terms prior to a final release. During the beta period, Licensor grants You the license described in Section 2 free of charge. Licensor may introduce a commercial license for the final release, under which continued use of the Software may require a paid subscription. Licensor may, at its sole discretion, offer preferential pricing or other benefits to users who used the Software during the beta period. Nothing in this Section obligates Licensor to offer any specific price, benefit, or continued free access, and Licensor may discontinue the beta or the Software at any time.

3. Self-Hosted Nature of the Software
You acknowledge that the Software is designed to be self-hosted, comprising a plugin (installed in Your JetBrains IDE) and backend components — the gateway, MCP server, and RAG server — that You deploy as containers on infrastructure of Your choosing. You are responsible for provisioning, configuring, securing, and maintaining that infrastructure (including containers, networks, API keys, and credentials). Licensor has no visibility into, and no control over, Your deployment environment once the Software has been installed or the container images have been pulled.

3.1 Deployment topology. The plugin stores API keys and tokens in the operating system keychain of the machine on which it runs, and communicates with the gateway over the network to relay them. Licensor recommends running the gateway on the same local machine or local network as the plugin. Deploying the gateway on a remote host or cloud infrastructure is not recommended, as it causes keys and credentials to travel over that connection and increases exposure to interception or misconfiguration. If You choose to deploy the gateway remotely against this recommendation, You do so entirely at Your own risk, and Licensor assumes no responsibility or liability for any resulting compromise of Your keys, credentials, or data.

4. Modifications
4.1 You may configure the Software as permitted by the Documentation. Any modification to the Software's source code, container images, configuration beyond documented settings, or integration with third-party systems not officially supported ("Unauthorized Modification") is done entirely at Your own risk.

4.2 Licensor makes no warranty and assumes no responsibility or liability whatsoever for the Software's behavior, security, output quality, or fitness for purpose following any Unauthorized Modification, including modifications that:
* alter Agent permissions, tool access, or safety/redaction mechanisms;
* change how the Software interacts with source code, file systems, credentials, or external services;
* remove, disable, or bypass any built-in safeguard, confirmation step, or human-in-the-loop control.

4.3 Licensor is not obligated to provide support, updates, or bug fixes for a Modified instance of the Software, and reserves the right to refuse support requests where an Unauthorized Modification is the identified or suspected cause of the issue.

5. Use of Agents and Generated Output
5.1 Human oversight required. The Software includes Agents capable of reading, generating, and — where explicitly configured to do so — modifying or executing code and commands. You acknowledge that You are solely responsible for reviewing, testing, and validating all Output before relying on it, merging it, deploying it, or executing it in any environment, including production systems.

5.2 No warranty on Output. Licensor does not warrant that Output will be correct, secure, complete, non-infringing, or fit for any particular purpose. AI-generated Output may contain errors, insecure patterns, or unintended side effects.

5.3 Improper use. Licensor assumes no responsibility or liability for any damage, data loss, security incident, financial loss, or other harm arising from:
* Your use of an Agent to act on production systems, sensitive data, or third-party systems without adequate review or safeguards;
* disabling, ignoring, or overriding confirmation prompts, redaction, or other safety controls provided by the Software;
* granting an Agent broader tool access, file-system access, or network access than reasonably necessary for its task;
* reliance on Output without independent verification.

5.4 You are responsible for ensuring Your use of the Software and any Agents complies with applicable law, Your employer's or client's policies, and any third-party terms (including those of any LLM provider You configure, such as Anthropic or a self-hosted model provider).

6. Third-Party Services
The Software may be configured to send data to third-party LLM providers (e.g. Anthropic's API) at Your direction and using Your own API credentials ("BYOK"). Licensor is not a party to, and assumes no liability arising from, Your relationship or agreement with any such third-party provider, including their pricing, availability, data handling, or output.

7. Data Handling
7.1 The Software does not collect or transmit telemetry to Licensor. All data processed by the Software (source code, file contents, terminal output, and any data sent to a configured LLM provider) remains within Your self-hosted deployment and, where applicable, is sent only to the third-party provider You have configured, using Your own credentials.

7.2 API keys and tokens are stored in the operating system keychain of the machine running the plugin, rather than in plaintext configuration files. As set out in Section 3.1, keys travel over the network between the plugin and the gateway; Licensor recommends a local deployment topology to minimize this exposure and disclaims liability for risks arising from remote or cloud deployment of the gateway against that recommendation.

7.3 The Software provides redaction of read and terminal tool results (e.g. IP addresses, emails, secrets) before such data is shown to an LLM. Redaction is provided as a configurable safeguard, not a guarantee: You may disable it, and Licensor does not warrant that redaction will catch every instance of sensitive data. You remain responsible for what data You expose to any LLM provider.

7.4 Because the Software does not collect personal data on Licensor's behalf, this Agreement does not include a separate Privacy Policy. If a future version of the Software introduces data collection, Licensor will update this Agreement and provide a Privacy Policy accordingly. This section does not cover data JetBrains itself collects as Merchant of Record (e.g. purchase and license-check information), which is governed by JetBrains' own privacy documentation.

8. Disclaimer of Warranties
TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, THE SOFTWARE IS PROVIDED "AS IS" AND "AS AVAILABLE", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, NON-INFRINGEMENT, ACCURACY, OR UNINTERRUPTED OR ERROR-FREE OPERATION.

9. Limitation of Liability
9.1 TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, LICENSOR SHALL NOT BE LIABLE FOR ANY INDIRECT, INCIDENTAL, SPECIAL, CONSEQUENTIAL, OR PUNITIVE DAMAGES, OR ANY LOSS OF DATA, PROFITS, REVENUE, OR BUSINESS, ARISING OUT OF OR RELATED TO YOUR USE OF THE SOFTWARE, WHETHER IN CONTRACT, TORT, OR OTHERWISE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

9.2 WITHOUT LIMITING THE FOREGOING, LICENSOR'S TOTAL LIABILITY ARISING OUT OF OR RELATED TO THIS AGREEMENT SHALL NOT EXCEED THE AMOUNT PAID BY YOU FOR THE SOFTWARE IN THE TWELVE (12) MONTHS PRECEDING THE EVENT GIVING RISE TO LIABILITY.

9.3 Nothing in this Agreement excludes or limits liability that cannot be excluded or limited under applicable mandatory law, including liability for intent (Vorsatz) or gross negligence (grobe Fahrlässigkeit), or for injury to life, body, or health, in accordance with §§ 276, 309 No. 7 BGB.

9.4 The limitations in this Section do not apply to damage arising from Unauthorized Modification (Section 4) or improper Agent use (Section 5), for which Licensor's liability is excluded to the fullest extent permitted by law, as such damage falls outside the intended and documented use of the Software.

10. Indemnification
You agree to indemnify and hold Licensor harmless from any claims, damages, or expenses (including reasonable legal fees) arising from Your Unauthorized Modification of the Software, improper use of an Agent, or violation of this Agreement.

11. Term and Termination
This Agreement is effective until terminated. Licensor may terminate this Agreement if You breach any of its terms. Upon termination, You must cease all use of the Software and delete all copies of it and associated container images in Your possession.

12. Governing Law
This Agreement is governed by the laws of the Federal Republic of Germany, excluding its conflict-of-law rules and the UN Convention on Contracts for the International Sale of Goods (CISG). If You qualify as a consumer under EEA law, mandatory consumer-protection provisions of Your country of residence remain unaffected.

13. Miscellaneous
If any provision of this Agreement is found unenforceable, the remaining provisions remain in full force. This Agreement, together with the Documentation, constitutes the entire agreement between You and Licensor regarding the Software.

Contact: [SUPPORT EMAIL] · [LEGAL ENTITY NAME] · [ADDRESS]
