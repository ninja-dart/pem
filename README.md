# ninja_pem

Dart library that provides simple and elegant way to decode and encode PEM.

## Usage

A simple usage example:

```dart
import 'package:ninja_pem/ninja_pem.dart';

final pemString = '''-----BEGIN KEY1-----
TG9yZW0gaXBzdW0gZG9sb3Igc2l0IGFtZXQsIGNvbnNlY3RldHVyIGFkaXBpc2Np
bmcgZWxpdC4uLkxvcmVtIGlwc3VtIGRvbG9yIHNpdCBhbWV0LCBjb25zZWN0ZXR1
ciBhZGlwaXNjaW5nIGVsaXQuLi5Mb3JlbSBpcHN1bSBkb2xvciBzaXQgYW1ldCwg
Y29uc2VjdGV0dXIgYWRpcGlzY2luZyBlbGl0Li4uTG9yZW0gaXBzdW0gZG9sb3Ig
c2l0IGFtZXQsIGNvbnNlY3RldHVyIGFkaXBpc2NpbmcgZWxpdC4uLkxvcmVtIGlw
c3VtIGRvbG9yIHNpdCBhbWV0LCBjb25zZWN0ZXR1ciBhZGlwaXNjaW5nIGVsaXQu
Li4K
-----END KEY1-----''';

void main() {
  // Decode PEM
  final part = PemPart.decodeLabelled(pemString, ['KEY1']);
  // Encode PEM
  print(part.toString());
}
```
