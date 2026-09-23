IDEAgent End User License Agreement (Developer EULA)

Last updated: 22.10.2026

This End User License Agreement ("Agreement") is a legal agreement between you, either an individual or a single entity ("You" or "Licensee"), and IDEAgent Gewerbeanmeldung, registered at Bahnhofstraße 11 85375 Neufahrn b. Freising, Germany ("Licensor", "we", "us") governing your use of the IDEAgent plugin(s) for JetBrains IDEs, the associated backend components (including but not limited to the gateway, MCP server, RAG server, and any other containers distributed alongside the plugin), and any related documentation (collectively, the "Software").

By downloading, installing, or using the Software, you agree to be bound by this Agreement. If you do not agree, do not install or use the Software.

IMPORTANT: The Software is proprietary software intended primarily for professional, commercial, educational, governmental, and software-development use. If You use the Software on behalf of an organization, You represent and warrant that You have authority to bind that organization to this Agreement.

1. Definitions
- "Software" means the IDEAgent JetBrains plugin(s), the RAG File Watcher plugin, and any Docker container images or backend services distributed or made available by Licensor for self-hosted operation with the plugin(s), including updates.
- "Agent" means any autonomous or semi-autonomous AI coding agent, tool-calling process, or automated code-modification feature operating within the Software, whether powered by a third-party LLM provider (e.g. Anthropic) or a locally-hosted model (e.g. via Ollama).
- "Modification" means any change to the Software's source code, configuration, container images, deployment environment, or runtime behavior made by You or on Your behalf, other than through an official update released by Licensor.
- "Output" means any code, file change, command, suggestion, or other content generated, executed, or applied by an Agent.
- "Confidential Technical Information" means any non-public information regarding the Software's design, source code, prompts, workflows, orchestration logic, infrastructure architecture, security controls, deployment mechanisms, communication protocols, encryption methods, authentication systems, credential-handling mechanisms, container communication patterns, and any other technical implementation details not expressly published by Licensor.

2. License Grant
Subject to Your compliance with this Agreement, Licensor grants You a limited, non-exclusive, non-transferable, non-sublicensable license to install and use the Software for Your own internal development purposes, in accordance with the Documentation and any applicable pricing tier.
The Software is licensed, not sold. All rights not expressly granted under this Agreement are reserved by Licensor.

2.1 Beta Release
The Software is currently distributed as a beta release. Licensor may add, remove, or change features, APIs, and licensing terms prior to a final release. During the beta period, Licensor grants You the license described in Section 2 free of charge.
Licensor may introduce a commercial license for the final release, under which continued use of the Software may require a paid subscription. Licensor may, at its sole discretion, offer preferential pricing or other benefits to users who used the Software during the beta period.

Nothing in this Section obligates Licensor to offer any specific price, benefit, or continued free access, and Licensor may discontinue the beta or the Software at any time.

3. Self-Hosted Nature of the Software

You acknowledge that the Software is designed to be self-hosted, comprising a plugin (installed in Your JetBrains IDE) and backend components, including but not limited to the gateway, MCP server, and RAG server, that You deploy as containers on infrastructure of Your choosing.
You are responsible for provisioning, configuring, securing, and maintaining that infrastructure, including containers, networks, API keys, credentials, backups, monitoring, and compliance obligations.
Licensor has no visibility into, and no control over, Your deployment environment once the Software has been installed or the container images have been pulled.

3.1 Deployment Topology
The plugin stores API keys and tokens in the operating system keychain of the machine on which it runs, and communicates with the gateway over the network to relay them.
Licensor recommends running the gateway on the same local machine or local network as the plugin.
Deploying the gateway on a remote host or cloud infrastructure is not recommended, as it causes keys and credentials to travel over that connection and increases exposure to interception or misconfiguration.
If You choose to deploy the gateway remotely against this recommendation, You do so entirely at Your own risk, and Licensor assumes no responsibility or liability for any resulting compromise of Your keys, credentials, or data.

3.2 Proprietary Nature of the Software
The Software is proprietary software owned by Licensor and is licensed, not sold.
Except for third-party components that Licensor explicitly identifies as being subject to a separate open-source license, the Software is not open source and no rights associated with open-source software licenses are granted under this Agreement.
Nothing in this Agreement grants You any right to:

- access source code;
- create derivative works;
- redistribute the Software;
- sublicense the Software;
- publicly disclose non-public implementation details;
- publish internal prompts;
- publish orchestration logic; or
- otherwise exercise rights commonly associated with open-source software.

All rights not expressly granted under this Agreement are reserved by Licensor.

3.3 Confidential Technical Information
You acknowledge that the Software contains Confidential Technical Information, trade secrets, and proprietary know-how belonging to Licensor.
Confidential Technical Information remains the exclusive property of Licensor and shall not be disclosed, published, distributed, or otherwise made available to any third party without Licensor's prior written consent.
Nothing in this Agreement obligates Licensor to disclose Confidential Technical Information beyond what Licensor reasonably considers necessary for the intended operation and use of the Software.

3.4 Security-Sensitive Implementation Details
The Software operates in customer-hosted environments, and certain implementation details are intentionally withheld for security reasons.
This may include, without limitation:

- system prompts and agent instructions;
- prompt-engineering methodologies;
- orchestration and workflow logic;
- infrastructure topology and deployment architecture;
- encryption, authentication, and credential-handling mechanisms;
- inter-container communication patterns and protocols;
- internal security controls, detection mechanisms, and abuse-prevention systems; and
- other non-public technical information that could reasonably increase security risks if disclosed.

Licensor may provide high-level architectural information, deployment guidance, APIs, and operational documentation where appropriate.
However, Licensor reserves the right to withhold implementation details that could reasonably compromise the security, integrity, reliability, or resilience of customer deployments.
The withholding of such information shall not constitute incomplete documentation, lack of functionality, a defect, failure to provide support, or breach of this Agreement.

4. Modifications

4.1 You may configure the Software as permitted by the Documentation.
Any modification to the Software's source code, container images, configuration beyond documented settings, or integration with third-party systems not officially supported ("Unauthorized Modification") is done entirely at Your own risk.
4.2 Licensor makes no warranty and assumes no responsibility or liability whatsoever for the Software's behavior, security, output quality, or fitness for purpose following any Unauthorized Modification, including modifications that:
- alter Agent permissions, tool access, or safety/redaction mechanisms;
- change how the Software interacts with source code, file systems, credentials, or external services;
- remove, disable, or bypass any built-in safeguard, confirmation step, or human-in-the-loop control.
4.3 Licensor is not obligated to provide support, updates, or bug fixes for a Modified instance of the Software and reserves the right to refuse support requests where an Unauthorized Modification is the identified or suspected cause of the issue.
For the avoidance of doubt, modifications made by Licensee do not create any obligation on Licensor to disclose source code, prompts, internal architecture, container build processes, or other Confidential Technical Information.

5. Use of Agents and Generated Output

5.1 Human Oversight Required
The Software includes Agents capable of reading, generating, and, where explicitly configured to do so, modifying or executing code and commands.
You acknowledge that You are solely responsible for reviewing, testing, and validating all Output before relying on it, merging it, deploying it, or executing it in any environment, including production systems.
5.2 No Warranty on Output
Licensor does not warrant that Output will be correct, secure, complete, non-infringing, or fit for any particular purpose.
AI-generated Output may contain errors, insecure patterns, or unintended side effects.
5.3 Improper Use
Licensor assumes no responsibility or liability for any damage, data loss, security incident, financial loss, or other harm arising from:

- Your use of an Agent to act on production systems, sensitive data, or third-party systems without adequate review or safeguards;
- disabling, ignoring, or overriding confirmation prompts, redaction, or other safety controls provided by the Software;
- granting an Agent broader tool access, file-system access, or network access than reasonably necessary for its task;
- reliance on Output without independent verification.
5.4 You are responsible for ensuring Your use of the Software and any Agents complies with applicable law, Your employer's or client's policies, and any third-party terms, including those of any LLM provider You configure.

6. Third-Party Services
The Software may be configured to send data to third-party LLM providers at Your direction and using Your own API credentials ("BYOK").
Licensor is not a party to, and assumes no liability arising from, Your relationship or agreement with any such third-party provider, including their pricing, availability, data handling, security practices, or output.

7. Data Handling
7.1 The Software does not collect or transmit telemetry to Licensor.
All data processed by the Software remains within Your self-hosted deployment and, where applicable, is sent only to the third-party provider You have configured using Your own credentials.
7.2 API keys and tokens are stored in the operating system keychain of the machine running the plugin, rather than in plaintext configuration files.
As set out in Section 3.1, keys travel over the network between the plugin and the gateway. Licensor recommends a local deployment topology and disclaims liability for risks arising from remote or cloud deployment of the gateway against that recommendation.
7.3 The Software provides redaction of read and terminal tool results before such data is shown to an LLM.
Redaction is provided as a configurable safeguard, not a guarantee. You remain responsible for what data You expose to any LLM provider.
7.4 Because the Software does not collect personal data on Licensor's behalf, this Agreement does not include a separate Privacy Policy.

If a future version introduces data collection by Licensor, Licensor will update this Agreement and provide appropriate privacy documentation.
This Section does not cover data collected by JetBrains or other third parties acting independently of Licensor.

8. Disclaimer of Warranties
TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, THE SOFTWARE IS PROVIDED "AS IS" AND "AS AVAILABLE", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, NON-INFRINGEMENT, ACCURACY, OR UNINTERRUPTED OR ERROR-FREE OPERATION.

9. Limitation of Liability
9.1 TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, LICENSOR SHALL NOT BE LIABLE FOR ANY INDIRECT, INCIDENTAL, SPECIAL, CONSEQUENTIAL, OR PUNITIVE DAMAGES, OR ANY LOSS OF DATA, PROFITS, REVENUE, OR BUSINESS ARISING OUT OF OR RELATED TO YOUR USE OF THE SOFTWARE.
9.2 WITHOUT LIMITING THE FOREGOING, LICENSOR'S TOTAL LIABILITY ARISING OUT OF OR RELATED TO THIS AGREEMENT SHALL NOT EXCEED THE AMOUNT PAID BY YOU FOR THE SOFTWARE IN THE TWELVE (12) MONTHS PRECEDING THE EVENT GIVING RISE TO LIABILITY.
IF NO FEES WERE PAID FOR THE SOFTWARE, LICENSOR'S TOTAL LIABILITY SHALL NOT EXCEED EUR 100 TO THE EXTENT PERMITTED BY APPLICABLE LAW.
9.3 Nothing in this Agreement excludes or limits liability that cannot be excluded or limited under applicable mandatory law, including liability for intent (Vorsatz), gross negligence (grobe Fahrlässigkeit), or injury to life, body, or health.
9.4 The limitations in this Section do not apply to damage arising from Unauthorized Modification (Section 4) or improper Agent use (Section 5), for which Licensor's liability is excluded to the fullest extent permitted by law.

10. Indemnification
You agree to indemnify and hold Licensor harmless from any claims, damages, liabilities, costs, or expenses (including reasonable legal fees) arising from:
- Your Unauthorized Modification of the Software;
- improper use of an Agent;
- Your violation of this Agreement; or
- Your violation of applicable law or third-party rights.

11. Term and Termination
This Agreement is effective until terminated.
Licensor may terminate this Agreement if You materially breach any of its terms.
Upon termination, You must cease all use of the Software and delete all copies of it and associated container images in Your possession or control.

12. Governing Law
This Agreement is governed by the laws of the Federal Republic of Germany, excluding its conflict-of-law rules and the United Nations Convention on Contracts for the International Sale of Goods (CISG).
If You qualify as a consumer under EEA law, mandatory consumer-protection provisions of Your country of residence remain unaffected.
For merchants (Kaufleute), legal entities under public law, and special funds under public law, the exclusive place of jurisdiction shall be Munich, Germany.

13. Miscellaneous
All Confidential Technical Information, trade secrets, and proprietary know-how relating to the Software shall remain the exclusive property of Licensor both during and after termination of this Agreement.
If any provision of this Agreement is found unenforceable, the remaining provisions remain in full force and effect.
This Agreement, together with the Documentation, constitutes the entire agreement between You and Licensor regarding the Software.

Contact:
gsca075@gmail.com
Sandro Cantarella
Bahnhofstraße 11
85375 Neufahrn b. Freising
Germany
