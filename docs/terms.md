# MACsec Terminology

## SecY (MAC Security Entity)
The entity that operates the MACsec protocol on a port, handling frame protection and validation.

## SC (Secure Channel)
A unidirectional channel for transmitting protected frames. Each SecY has one transmit SC and one or more receive SCs.

## SA (Secure Association)
A security relationship within an SC, identified by an AN. Contains the cryptographic keys (SAK) used for frame protection.

## SCI (Secure Channel Identifier)
A globally unique identifier for an SC, composed of a MAC address and port identifier.

## AN (Association Number)
A 2-bit number (0-3) identifying an SA within an SC. Allows key rotation without traffic interruption.

## PN (Packet Number)
A 32-bit counter incremented for each frame, used to prevent replay attacks.

## XPN (Extended Packet Number)
A 64-bit packet number for high-bandwidth links, avoiding frequent key rotation due to PN exhaustion.

## KaY (Key Agreement Entity)
The entity responsible for MKA protocol operation, managing key distribution and SA establishment.

## MKA (MACsec Key Agreement)
The protocol used by KaY entities to discover peers, negotiate keys, and manage secure associations.
