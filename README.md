# Web lndconnect
Simple web tool to connect Zap Mobile to an Lnd node.
This tool was based on the Go code in https://github.com/LN-Zap/lndconnect

# How to use

- Download the repository as a ZIP archive.
- Unpack the ZIP archive.
- Go into the unpacked folder and open the `weblndconnect.html` file.

- The host field is automatically filled with your local network IP address if the code can grab it. You can also use a public IP address or a host name.
- The port defaults to `10009`. Change it if your Lnd node is serving on another one.
- Select your `tls.cert` path.
  - For Windows you can usually find it in `C:\Users\<youruser>\AppData\Local\Lnd`.
  - For Linux and MacOS it should be at a similar folder.
- Select your `admin.macaroon` file.
  - For Windows you can usually find it in `C:\Users\<youruser>\AppData\Local\Lnd\data\chain\bitcoin\<mainnet/testnet>`.
- Select a scale for the generated QRCode. Leave it at the default value, if the generated QRCode is too big or too small, you can adjust it there and generate again.

# For developers

If you want to check that the code is not doing anything wrong, all of the custom relevant code is inline in the `weblndconnect.html` file and fully commented.
In the `js/` folder you'll find the QRCode helper library. It's a complete copy of https://github.com/nayuki/QR-Code-generator/blob/master/javascript/qrcodegen.js with no changes.
