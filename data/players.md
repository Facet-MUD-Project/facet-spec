# Player Save Files

Player save files MUST be stored in the [TOML] format, containing the following
variables:

| Key | Data type | Optional | Notes |
| --- | --------- | -------- | ----- |
| username | string | No | |
| creation_state | integer | No | See [player creation state] |
| display_name | string | Yes | |
| password | string | No | See [password format](#password-format) |
| level | integer | No | |

## Password Format

Passwords MUST be stored in the format:

```txt
<algorithm>$<iterations>$<salt>$<hash>
```

For example, a password generated from the following:

| Key | Value |
| --------- | ----------------------- |
| Algorithm | PBKDF2 w/SHA512 hashing |
| Iterations | 100,000 |
| Salt | this_is_my_salt |
| Password | super_secret_password |

Would be stored as the following:

```txt
pbkdf2_sha512$100000$this_is_my_salt$5e9fcfd9910423912540cda961793794dca41c926cbd6e577b43a2b80cb81978ab880a17ff50711eff7b0718457692c72d4c5f713d073e16ad9a99ab3bde0ef6
```

### Supported Algorithms

#### PBKDF2

At this time, only the [PBKDF2] algorithm is supported. This algorithm MUST be
noted in the format `pbkdf2_<hashing algorithm>`. For example, `pbkdf2_sha512`.

At this time, the only supported hashing algorithm is `SHA512`.

The key length of the resulting password MUST be 64 bytes.

[PBKDF2]: https://en.wikipedia.org/wiki/PBKDF2
[player creation state]: ./enums.md#player-creation-state
[TOML]: https://toml.io/
