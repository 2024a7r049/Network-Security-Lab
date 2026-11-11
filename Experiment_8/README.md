# Experiment 8: Protected Email Exchange with OpenPGP and Thunderbird

## 1. Objective

To implement secure email communication using OpenPGP in Mozilla Thunderbird by exchanging encrypted and digitally signed emails between two participants. The experiment demonstrates confidentiality, integrity, sender authentication, and successful message decryption.

## 2. Account and Key Details

| Participant | Email Address | OpenPGP Key ID |
|---|---|---|
| Suksham Kalyan | 2024a7r049@mietjammu.in | `0x090241A542C44F23` |
| Krish Sharma | 2024a7r012@mietjammu.in | `0x41A23AAE89FC29BB` |

Both participants generated their own OpenPGP key pairs consisting of a public key and a private key.

- Public keys were exchanged between participants.
- Private keys were retained by their respective owners.
- Public keys were imported into the correspondent's Thunderbird account.

## 3. Message Exchange Architecture

The following diagram illustrates the two-way secure email communication process.

```text
        Suksham Kalyan                    Krish Sharma
        (Sender)                          (Recipient)
        
        Private Key                       Public Key
             |                                 |
             |                                 |
        Sign Email                             |
             |                                 |
        Encrypt Message ---------------------->
                                               |
                                          Decrypt Email
                                               |
                                          Verify Signature
                                               |
                                               |
        Public Key                        Private Key
             |                                 |
             |                                 |
        Verify Signature <---------------- Sign Email
             |                           Encrypt Message
        Decrypt Email
             |
        Message Received
```

## 4. Tools and Technologies Used

1. Mozilla Thunderbird – Email client supporting OpenPGP encryption.
2. OpenPGP – Standard for public-key encryption and digital signatures.
3. Public and Private Key Pairs – Used for encryption, decryption, and signing.
4. ASCII-armored public key files (.asc) – Used for exchanging public keys.

## 5. Experimental Procedure

### Step 1: OpenPGP Key Generation

Both participants configured OpenPGP in Mozilla Thunderbird and generated or selected their respective key pairs.

**Suksham Kalyan:**
- Email: `2024a7r049@mietjammu.in`
- Key ID: `0x090241A542C44F23`

**Krish Sharma:**
- Email: `2024a7r012@mietjammu.in`
- Key ID: `0x41A23AAE89FC29BB`

### Step 2: Public Key Exchange

Both participants exported their public keys and exchanged them.

The public keys were imported into the respective Thunderbird accounts to enable encrypted communication.

The private keys remained confidential and were never shared.

### Step 3: Sending an Encrypted and Digitally Signed Email

Suksham composed an email addressed to Krish Sharma.

Before sending the email:
1. The recipient's public key was selected for encryption.
2. Digital signing was enabled using Suksham's private key.
3. Message encryption was enabled.
4. The email was sent to Krish.

### Step 4: Receiving and Verifying the Email

Krish received the encrypted email in Thunderbird.

He used his private key to decrypt the message.

Thunderbird used Suksham's imported public key to verify the digital signature.

The message was successfully decrypted, and the signature was reported as valid.

### Step 5: Sending the Encrypted Reply

Krish composed a reply addressed to Suksham.

The following security settings were enabled:
1. Encryption using Suksham's public key.
2. Digital signing using Krish's private key.

The encrypted and digitally signed email was sent to Suksham.

### Step 6: Receiving and Verifying the Reply

Suksham received the encrypted reply from Krish.

He decrypted the message using his private key.

Thunderbird verified the digital signature using Krish's imported public key.

The reply was successfully decrypted, and the signature was reported as valid.

## 6. Results and Observations

The experiment was successfully performed in both communication directions.

| Parameter | Suksham → Krish | Krish → Suksham |
|---|---|---|
| Email transmission | Successful | Successful |
| Message encryption | Successful | Successful |
| Message decryption | Successful | Successful |
| Digital signature | Enabled | Enabled |
| Signature verification | Valid | Valid |
| Communication | Successful | Successful |

### Associated OpenPGP Key IDs

| Participant | Key ID |
|---|---|
| Suksham Kalyan | `0x090241A542C44F23` |
| Krish Sharma | `0x41A23AAE89FC29BB` |

## 7. Security Analysis

### Confidentiality
OpenPGP encryption ensures that only the intended recipient possessing the corresponding private key can decrypt and read the protected message.

### Integrity
Digital signatures help detect modifications made to a signed message after it was created.

### Authentication
A valid digital signature demonstrates that the message corresponds to a signature generated by the private key associated with the imported public key.

### Non-Repudiation
Digital signatures provide evidence that a particular private key was used to sign a message. However, they do not independently establish the real-world identity of the person controlling that key.

### Key Verification
Full OpenPGP fingerprints should be verified through a trusted independent communication channel. Short key IDs are useful for identifying keys but are not sufficient for establishing identity.

## 8. Evidence and Screenshots

The following screenshots should be included in the experiment documentation:

1. OpenPGP key details of Suksham Kalyan.
2. OpenPGP key details of Krish Sharma.
3. Public key exchange and import.
4. Suksham's sent email showing encryption and digital signing.
5. Krish's received email showing successful decryption and valid signature.
6. Krish's sent reply showing encryption and digital signing.
7. Suksham's received reply showing successful decryption and valid signature.

**Note:** Full fingerprints should also be documented if required by the experiment instructions. They should be copied from Thunderbird's key properties rather than inferred from the short key IDs.

## 9. Conclusion

The experiment successfully demonstrated secure two-way email communication using OpenPGP in Mozilla Thunderbird.

Suksham Kalyan and Krish Sharma exchanged public keys and communicated using encrypted and digitally signed emails. Both participants successfully decrypted their received messages and Thunderbird reported valid digital signatures in both directions.

The experiment demonstrated the practical implementation of confidentiality, integrity, and signature-based authentication through public-key cryptography.

Thus, the objective of implementing protected email exchange using OpenPGP and Thunderbird was achieved.
