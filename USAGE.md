<!-- Start SDK Example Usage [usage] -->
```typescript
import { Gr4vy, withToken } from "@gr4vy/sdk";
import fs from "fs";

const gr4vy = new Gr4vy({
  id: "example",
  server: "sandbox",
  merchantAccountId: "default",
  bearerAuth: withToken({
    privateKey: fs.readFileSync("private_key.pem", "utf8"),
  }),
});

async function run() {
  const result = await gr4vy.accountUpdater.jobs.create({
    paymentMethodIds: [
      "ef9496d8-53a5-4aad-8ca2-00eb68334389",
      "f29e886e-93cc-4714-b4a3-12b7a718e595",
    ],
  });

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->