## `rust:1-slim`

```console
$ docker pull rust@sha256:31ee7fc65186be7e0e0ccb3f2ca305f14e4739e7642a1ae65753aa5d7b874523
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rust:1-slim` - linux; amd64

```console
$ docker pull rust@sha256:d8f0d5c09580253ecdd6d6894ff112b2b760683ff2a74585e5189f2578728ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.5 MB (320462817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7774afa8fa5ea5aedfbfdfd3684d130a9c824508cfc0d373e7c3eaa8b546af`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Tue, 30 Jun 2026 23:43:04 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:43:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:43:04 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5169cf74e23b4eb5efada4feddccfe1372ad72000179e789555e16a4739b3cfa`  
		Last Modified: Tue, 30 Jun 2026 23:43:47 GMT  
		Size: 290.7 MB (290677398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:cb3cc9dca8bb10018f9053aabc7314ee70b8044349044bb0f1a93feeb7d01690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4180813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd95d495aff47b22e1b29309b7dea7fa7b32f1d4ab805b8985e4060643a34e80`

```dockerfile
```

-	Layers:
	-	`sha256:1d3e799027176ce724c193484b07272e9e43fcd07143f6a96e137783a89ff441`  
		Last Modified: Tue, 30 Jun 2026 23:43:41 GMT  
		Size: 4.2 MB (4165181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b332e57a057c6fbd37127e9e26a17e45504d8e6a42b91304fab1f0187744128f`  
		Last Modified: Tue, 30 Jun 2026 23:43:40 GMT  
		Size: 15.6 KB (15632 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:d8bbece1bbb94edc50dd3aaebd6db6906a8708406cae246336a2a6d5d982d5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334306918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a44f63b86e6d2df4306e3c141aca74d706a09cd362fcaaee6056f1bcb440374`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Tue, 30 Jun 2026 23:36:17 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:36:17 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:36:17 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbed8fc27cc2e57aa37e54edccbeca68ab0064fdb2e220aa86d6539f843f6dca`  
		Last Modified: Tue, 30 Jun 2026 23:37:00 GMT  
		Size: 308.1 MB (308095867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:31288bbc0bd624f9ef9a075839e6b56bfc962b85df14158d642867a25409aa1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7235ade987dfe21348a579741ba48e27e3c87b39218e0ae1a249c710a22287f`

```dockerfile
```

-	Layers:
	-	`sha256:0b08f54c46e1bb018fa82f3bed76118b02519ca2abf88b8fee7cdc9109613a96`  
		Last Modified: Tue, 30 Jun 2026 23:36:54 GMT  
		Size: 4.0 MB (3970057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9c2d74cdbb5e81c47df6fcdcf0506dc3e529cf120768dbd5a739223bfddda24`  
		Last Modified: Tue, 30 Jun 2026 23:36:53 GMT  
		Size: 15.7 KB (15745 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:bfa306c18b2e778a21782d0ac2f1ae7442c6261409bfff086867a736396cafe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (280037021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d0599a9e72e980be6e5e2c8f5b7bd4527ee7cae3dc9cb856b6f3bcb78fe5bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Tue, 30 Jun 2026 23:41:00 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:41:00 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:41:00 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06f4d21cd23f8b3b2051580f857db82c3ecc0344a1dd61937b45c6e0136596a`  
		Last Modified: Tue, 30 Jun 2026 23:41:40 GMT  
		Size: 249.9 MB (249888470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:580c5e9ae884d53f62947e73dccbe2755d928ce5015b17ed6058f32051eeaed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4272174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28ca1537d64fbb42b753bbca060bd3af72d8a8ea79e215639fb408ea14a80ec`

```dockerfile
```

-	Layers:
	-	`sha256:ad14d04f4f25022fb981e732a582a7bea9db76ca62a17f8cc280d829acb283f5`  
		Last Modified: Tue, 30 Jun 2026 23:41:35 GMT  
		Size: 4.3 MB (4256389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfbeb26bafa5a931c4a905890c97fc5e2af63c967676d1544be8ef0ac611c843`  
		Last Modified: Tue, 30 Jun 2026 23:41:34 GMT  
		Size: 15.8 KB (15785 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:2e9387cd3957094ac433d5195fa8b3303a927b776c55a5616556ade166126666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.3 MB (345268333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5695d4ee44f7c9e67d9aedd34783f715caaa68496705cd22e0f1dc970a240e8b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Tue, 30 Jun 2026 23:36:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:36:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:36:21 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e39aa2cb81cc9de4f8e8a62a93e0424a9cf059df3a61fe8c6997709aafe8c8`  
		Last Modified: Tue, 30 Jun 2026 23:37:10 GMT  
		Size: 314.0 MB (313967123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:f411c5f9ae123b68e5900939df2f83f8ea2f6a66092e64ed170a7bebd31549e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4154275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652dcff9f53175950374a6cf80cdc09a14c6d2cee0fbc374b9c787ad54c40e4e`

```dockerfile
```

-	Layers:
	-	`sha256:68c0104fc98af4a0baa5a7886a29adef44730b841731045adb6654933d1ec1ef`  
		Last Modified: Tue, 30 Jun 2026 23:37:03 GMT  
		Size: 4.1 MB (4138694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1ffa2f2236a1926b38bfccc2311a4f3c1e6ec7fa80c4b09b937e1e5a935a7b5`  
		Last Modified: Tue, 30 Jun 2026 23:37:03 GMT  
		Size: 15.6 KB (15581 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:6cccfaff8b5e435353bdd1584bb779cc3462a7e6ebf0310f9e3a91f511516cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.8 MB (394794662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9808328e9d7a7086a80ad49829787737640cd8f9c6a5b027f8471db9f8c39e0b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Tue, 30 Jun 2026 23:45:08 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:45:08 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:45:08 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a1b9586b8df8c7b48a10cb239c8dc121612c6b2334ede9029441341a3a1aeb`  
		Last Modified: Tue, 30 Jun 2026 23:46:42 GMT  
		Size: 361.2 MB (361188274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:7b3da06d488d047d5f5ccf6310847d0cb4cc3e74c30264da20feeb30af356a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4177343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27a004bd43a0b0db613494e459ae5ad050b9cdd7f74b088f8d9ec7005e09cdf`

```dockerfile
```

-	Layers:
	-	`sha256:871b5e01a06417652ce71f8fc2e4801fcf5e89353dfbbfa8de5309f4e86c7f0c`  
		Last Modified: Tue, 30 Jun 2026 23:46:34 GMT  
		Size: 4.2 MB (4161642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e425d7e83750e5382336978b8f35be6d832a2217ff61a8e1c0279ed4ffab833`  
		Last Modified: Tue, 30 Jun 2026 23:46:34 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; riscv64

```console
$ docker pull rust@sha256:6de76d48bfa215d4acfafe83b3a995c541169c07e58f0875df3011be1654907a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.6 MB (390622308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2aa4ab7fac655f70dbabe7b479a77fc1422e1d7ec52f5b7ecb9da60d08ffdd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1782172800'
# Wed, 01 Jul 2026 00:08:50 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 01 Jul 2026 00:08:50 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Wed, 01 Jul 2026 00:08:50 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:58bface994ba631e609596a2ca5032d9d75de27f1b6476034b581e226205adab`  
		Last Modified: Wed, 24 Jun 2026 03:41:42 GMT  
		Size: 28.3 MB (28282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741b3e17a86e6fc7485362d4b2330dd099ace7baef05c6ee938ab23b69df819d`  
		Last Modified: Wed, 01 Jul 2026 00:20:19 GMT  
		Size: 362.3 MB (362339930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:86d7753e8cfc6e83ce8cda22a09ba52bd57d667dc289be1f0f2151b92bfd3fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154d9138453eb7cf2ddc62d93359648e55e7e0b00b346f50ab392f7e2ccc35a9`

```dockerfile
```

-	Layers:
	-	`sha256:1f775781ebbe44e5272f2cd49401babaee6f32315b81861d38525d178127b35e`  
		Last Modified: Wed, 01 Jul 2026 00:19:15 GMT  
		Size: 4.2 MB (4239598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65854b22ee921bfff704d344af5be5b90a6df3af462e8793572ad096ab3555b0`  
		Last Modified: Wed, 01 Jul 2026 00:19:13 GMT  
		Size: 15.7 KB (15701 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:6d030b3966486a507584fe3ca14771a3671616a56b00d579d5c4ae174168c719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.5 MB (377522130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa078bd7e0a1077a2ef029e95ad87a41169ca69d70e54a22ed7fdedb248a4427`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Tue, 30 Jun 2026 23:33:02 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 30 Jun 2026 23:33:02 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.96.1
# Tue, 30 Jun 2026 23:33:02 GMT
RUN set -eux;         apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;         arch="$(dpkg --print-architecture)";     case "$arch" in         'amd64')             rustArch='x86_64-unknown-linux-gnu';             rustupSha256='4acc9acc76d5079515b46346a485974457b5a79893cfb01112423c89aeb5aa10';             ;;         'armhf')             rustArch='armv7-unknown-linux-gnueabihf';             rustupSha256='124e02253af9128f9e27ea1ac929cbb73cf44cf35469d0f594a1b62f7b71fea1';             ;;         'arm64')             rustArch='aarch64-unknown-linux-gnu';             rustupSha256='9732d6c5e2a098d3521fca8145d826ae0aaa067ef2385ead08e6feac88fa5792';             ;;         'i386')             rustArch='i686-unknown-linux-gnu';             rustupSha256='5140e82096f96d1d8077f00eb312648e0e5106d101c9918d086f72cbc69bb3a1';             ;;         'ppc64el')             rustArch='powerpc64le-unknown-linux-gnu';             rustupSha256='4bfff85bd3967d988e14567aa9cc6ab0ea386f0ffeff0f9f14d23f0103bf1f97';             ;;         's390x')             rustArch='s390x-unknown-linux-gnu';             rustupSha256='66c2c132428b6b77803facb02cbdf33b89d20c00bd20da142be8cb651f2e7cd8';             ;;         'riscv64')             rustArch='riscv64gc-unknown-linux-gnu';             rustupSha256='7e43f2b2e6307d61da17a4dff61e6bceef408b8189822df64e1094590d2a70f9';             ;;         *)             echo >&2 "unsupported architecture: $arch";             exit 1;             ;;     esac;         url="https://static.rust-lang.org/rustup/archive/1.29.0/${rustArch}/rustup-init";     wget --progress=dot:giga "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;         chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;         apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;         rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a217a5960c58b3cfbf8274a06f1dd8394cdac82fe111339631190c625224dc`  
		Last Modified: Tue, 30 Jun 2026 23:34:11 GMT  
		Size: 347.7 MB (347670749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:e321d4f9eeef3ee561a68964bbaaef56f138e78113ec6715cae03d768a156d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3998562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ac54263bcb8c912f1564455b0d90250a6f53da98b84ce1afd13de0e51b25a5`

```dockerfile
```

-	Layers:
	-	`sha256:98c8714b9945a7008c62559d08ecb9f78776eb2c5cb86f3e92620295c54bf7b1`  
		Last Modified: Tue, 30 Jun 2026 23:34:05 GMT  
		Size: 4.0 MB (3982929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a10e0ec21d242417fdb7ead873cb4e93ddcd432584200c2d1b148868c1463b6`  
		Last Modified: Tue, 30 Jun 2026 23:34:04 GMT  
		Size: 15.6 KB (15633 bytes)  
		MIME: application/vnd.in-toto+json
