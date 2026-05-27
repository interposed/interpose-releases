# interpose — Binary Distribution License (v1)

**Copyright © 2026 interposed.** All rights reserved.

> **NOTE:** This license is drafted by the maintainer, not by a lawyer, and has not been reviewed by counsel. Use it as a starting point. Before relying on its terms for serious commercial decisions (yours or anyone else's), consult an attorney licensed in your jurisdiction. Maintainer intent is described in [§ Spirit of this license](#spirit-of-this-license) below; if the wording and the spirit ever conflict, the spirit wins and that's a bug to be reported and fixed.

---

## Grant

Subject to the terms and conditions of this License, the copyright holder ("Licensor") grants you ("Licensee") a worldwide, royalty-free, non-exclusive, non-transferable, revocable license to:

1. **Download, install, and use** the pre-compiled binaries published in this repository (the "Binaries") for any of the following purposes without further permission or fee:
   - **Personal use** on a machine you own or are authorized to administer.
   - **Educational use** in academic settings (research, teaching, classroom demonstrations).
   - **Non-commercial use**, including open-source projects, individual experimentation, and personal demos.
   - **Internal commercial evaluation** for a period of up to ninety (90) days from first use within a given organization.

2. **Make copies of the Binaries** strictly for the purposes above, including backup copies and copies installed across multiple personal devices belonging to the same individual.

## What requires a separate commercial license

Use of the Binaries in any of the following contexts requires a separate written commercial license from the Licensor:

- **Production deployment** within a commercial organization (beyond the 90-day evaluation period).
- **Multi-user deployment** within a commercial organization (more than one human operator using the same installation, or installations across more than one machine for business purposes).
- **Embedding, bundling, or redistribution** of the Binaries within or alongside another commercial product or service.
- **Offering the Binaries as a service** (managed hosting, "interpose-as-a-service" SaaS offerings, etc.).
- **Government or defense use** beyond individual evaluation, regardless of whether the user is a public or private entity.

To request a commercial license, contact: **contact@stateful.art**.

The Licensor reserves the right to grant such licenses on terms the parties mutually agree upon, and is under no obligation to grant any particular request.

## Restrictions

You may not:

- **Reverse engineer, decompile, or disassemble** the Binaries, except to the extent that such activity is expressly permitted by applicable law notwithstanding this restriction (e.g. for interoperability under EU Directive 2009/24/EC or similar).
- **Redistribute the Binaries** through any channel other than this official `interposed/interpose-releases` repository — direct linking to the official releases is encouraged; copying tarballs to your own server, mirror, or package index is not.
- **Remove, alter, or obscure** any copyright notice, license notice, attribution, or version identifier embedded in the Binaries or their accompanying documentation.
- **Use the Binaries to develop a competing product** intended to replace interpose in the same or similar use cases, where the development meaningfully relies on knowledge of interpose's behavior gained from using the Binaries.
- **Misrepresent the origin of the Binaries** or imply endorsement by the Licensor where none exists.

## Trademarks

The names "interpose," "interposed," and any associated logos are trademarks of the Licensor. This License does not grant rights to use those marks beyond the minimum necessary to reasonably describe the origin of the Binaries (e.g., "powered by interpose" is acceptable; "interpose Pro" implying official endorsement is not).

## No warranty

THE BINARIES ARE PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND NONINFRINGEMENT. THE LICENSOR MAKES NO WARRANTY THAT THE BINARIES WILL BE ERROR-FREE, WILL FUNCTION UNINTERRUPTED, OR WILL MEET YOUR REQUIREMENTS.

## Limitation of liability

IN NO EVENT SHALL THE LICENSOR, ITS AFFILIATES, OR CONTRIBUTORS BE LIABLE FOR ANY CLAIM, DAMAGES, OR OTHER LIABILITY — WHETHER IN AN ACTION OF CONTRACT, TORT, OR OTHERWISE — ARISING FROM, OUT OF, OR IN CONNECTION WITH THE BINARIES OR THE USE OR OTHER DEALINGS IN THE BINARIES, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

This limitation applies to the maximum extent permitted by applicable law. Some jurisdictions do not allow the exclusion or limitation of certain warranties or liability; in those jurisdictions, the Licensor's liability is limited to the greatest extent allowed by law.

## Termination

This License terminates automatically if you breach any of its terms. Upon termination, you must cease all use of the Binaries and destroy all copies in your possession. Sections [Restrictions](#restrictions), [Trademarks](#trademarks), [No warranty](#no-warranty), and [Limitation of liability](#limitation-of-liability) survive termination.

The Licensor may also terminate this License with respect to specific Licensees or in general by publishing a notice in this repository. Termination does not affect rights validly exercised before the termination date.

## Spirit of this license

The maintainer's intent is:

- **Hobbyists, students, researchers, and individual developers can use this freely**, indefinitely, without paying or asking permission, including for their own commercial product development at the experimental stage.
- **Organizations that derive ongoing operational value from interpose pay for that value**, on terms that are fair to both sides.
- **Reverse engineering is restricted** to discourage clone competitors, not to prevent debugging your own setup — interoperability work (writing your own MCP integration, your own agent SDK, etc.) is welcome and explicitly does not require disassembly.
- **Redistribution is restricted** so that the official Binaries remain the authoritative artifact — partly for security (you should be able to trust what you install), partly for support (we can't help you debug something we didn't ship).

If you are unsure whether your use case falls inside this license or requires a commercial conversation, **just ask** — contact@stateful.art. The conversation is free; the answer is usually "fine, no commercial license needed yet."

## Governing law

This License is governed by the laws of Turkey, without regard to its conflict-of-laws principles. Any disputes arising from this License shall be resolved in the courts of Istanbul, Turkey.

---

*Last updated: 2026-05-26. Version: 1.0. License changes (when they happen) will increment the version and remain backward-compatible for binaries released under earlier versions.*
