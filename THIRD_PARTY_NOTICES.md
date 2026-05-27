# Third-party notices

`interpose` and `interpose-fido-bridge` binaries published under this repo statically link or vendor third-party code. The notices below satisfy the attribution obligations of those licenses.

For the source-side dependency tree, see `go.mod` in the source repository.

---

## go-libfido2 (vendored fork) — MIT

The `interpose-fido-bridge` binary statically links a vendored fork of [`github.com/keys-pub/go-libfido2`](https://github.com/keys-pub/go-libfido2). The fork lives at `third_party/go-libfido2/` in the source tree; the only modification is updating darwin/arm64 link paths from the discontinued `openssl@1.1` to the current `openssl@3`. License unchanged.

```
MIT License

Copyright (c) 2019 Gabriel Handford

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## libfido2 (Yubico) — BSD-2-Clause

The `interpose-fido-bridge` darwin/arm64 binary statically links [Yubico's `libfido2`](https://github.com/Yubico/libfido2) (installed at build time via Homebrew). License text reproduced from the `libfido2` source distribution:

```
Copyright (c) 2018, Yubico AB
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this
   list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice,
   this list of conditions and the following disclaimer in the documentation
   and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
```

YubiKey® is a registered trademark of Yubico AB. interposed is not affiliated with or endorsed by Yubico.

---

## OpenSSL 3 — Apache-2.0

The `interpose-fido-bridge` darwin/arm64 binary statically links [OpenSSL 3](https://www.openssl.org) (installed at build time via Homebrew). OpenSSL 3 is distributed under the Apache License 2.0. Full license text at <https://www.apache.org/licenses/LICENSE-2.0>.

---

## libcbor — MIT

`go-libfido2`'s vendored darwin/arm64 build statically links [`libcbor`](https://github.com/PJK/libcbor). License: MIT. Full notice ships in the vendored `third_party/go-libfido2/darwin/arm64/lib/` tree of the source repository.
