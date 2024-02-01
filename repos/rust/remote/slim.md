## `rust:slim`

```console
$ docker pull rust@sha256:be99e92155c29874991cdbf3300ffa0e73f8fccc314901bc8e202c9f7ca8c84b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:slim` - linux; amd64

```console
$ docker pull rust@sha256:5c1e06035893f39822ad7ae131dc5e2e0d7b77bb7194e2974f587cd1c28b7b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277187127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3728bc1f336339e50945c341e14711c083d883c63bbe320b7ec0ac1b53b309`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jan 2024 18:59:53 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Wed, 10 Jan 2024 18:59:53 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 18:59:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.75.0
# Wed, 10 Jan 2024 18:59:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b3665875896e9830e494b58e529dd8d5f8fc520e17ac3e19f0623acbdd9b4e`  
		Last Modified: Tue, 16 Jan 2024 18:56:08 GMT  
		Size: 248.1 MB (248061206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:6ad4136564eefe265678e3df6ec5d7ed7fc522578e92cd3a4cb5e47fe1761cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3425040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4793b1dfa64d0155be3c646d2807fd16c08964986d2926895dd4780eff66b10c`

```dockerfile
```

-	Layers:
	-	`sha256:0721175f7569a80b17e738ff2797d42a9d11b32ee75fafa6868a321c7039e980`  
		Last Modified: Tue, 16 Jan 2024 18:56:01 GMT  
		Size: 3.4 MB (3412338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd19833723889d37cd2266aed3ef5223f9dd834c373a7e64c61f1f92ca126fb9`  
		Last Modified: Tue, 16 Jan 2024 18:56:01 GMT  
		Size: 12.7 KB (12702 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:0e7aa33cb4591717e8dc29fd58dcf347886d13659dd259cd1eabbb731770a6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287473350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2309ecf77551d101d34621cfb40006e7d77f8f329e2ba31caa87860b0c185784`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jan 2024 18:59:53 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Wed, 10 Jan 2024 18:59:53 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 18:59:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.75.0
# Wed, 10 Jan 2024 18:59:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa115848144f3843b6776260b7bb81a3bc17e082bab8d15c2ee094b9edd77f0`  
		Last Modified: Tue, 16 Jan 2024 19:54:52 GMT  
		Size: 262.8 MB (262755224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:92bcaa0e0c462bde0019a69fb762e781ff0f3294dea75d5ec11e6f281a7f388d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3265361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7a01838fb9626d1a80f913fb5a07f218c63acb1eaf2a9aede40c9ae63e65a9`

```dockerfile
```

-	Layers:
	-	`sha256:7e50cc419f580881218c81bac0f32e7e61aa7db1056a50cdda18f72fcadded5a`  
		Last Modified: Tue, 16 Jan 2024 19:54:45 GMT  
		Size: 3.3 MB (3252724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54108e16595a5825b90c0aa28bc40dfda19f9ddb8f6111d060c5b81ea4bae515`  
		Last Modified: Tue, 16 Jan 2024 19:54:45 GMT  
		Size: 12.6 KB (12637 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:eb511b285cf57e6ca056303f12ba5b4b36ddf53a89a66ad85958c02941417c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.9 MB (342929938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c4e715c650784d823c430eaadfbf22042b2d640447321f7b342c4c74b87d7c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jan 2024 18:59:53 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Wed, 10 Jan 2024 18:59:53 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 18:59:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.75.0
# Wed, 10 Jan 2024 18:59:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361b817749e2b0cc8c775520ae1766cd7e24e31525ad65da31f142acc818a7a4`  
		Last Modified: Tue, 16 Jan 2024 19:37:51 GMT  
		Size: 313.8 MB (313772603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:3f4e462120c8710f3b01b43af26c584bd8f699dcc2b05734fd4a1b5269469d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3444525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836de70694572673d8e47375e21c846dc3740567fa13c7ea46043c11c37803cf`

```dockerfile
```

-	Layers:
	-	`sha256:6a48e6c4e70e06df3ce4ffd1866ead41c77259dd559d5b2593468899ed26d73d`  
		Last Modified: Tue, 16 Jan 2024 19:37:44 GMT  
		Size: 3.4 MB (3431972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097a1e2fc7071ee500f9998e8195dae27dcbe701a7f432eba5ebbde2f806e40f`  
		Last Modified: Tue, 16 Jan 2024 19:37:43 GMT  
		Size: 12.6 KB (12553 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:c54648f21e14a54b15c0f31a4592f64b2b14737fb4525b4a198080aa9683ad2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288418588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3251eb8dc58831447eeab1587b5b500290926f43048e6eb7e2ac9a3c2ba38f64`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jan 2024 18:59:53 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
# Wed, 10 Jan 2024 18:59:53 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 18:59:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.75.0
# Wed, 10 Jan 2024 18:59:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b83920280cc776bb731fa9a63b3950acb8c0f67e8d6c16491f99adf3f4aff55`  
		Last Modified: Thu, 01 Feb 2024 00:09:17 GMT  
		Size: 258.3 MB (258253570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:76d5a8b8ffde1795ccebf4bbfeafc9eb0738fedbae956e63ca3de67f40e18665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3408067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7238f932167879b43ebaf511050606eecf7affd846beeee597c1eeb18c4ef3c`

```dockerfile
```

-	Layers:
	-	`sha256:c5b1c815fb3ec8b8c631167f93fab1c0e96744094bc28cb2e032194d41414f80`  
		Last Modified: Thu, 01 Feb 2024 00:09:08 GMT  
		Size: 3.4 MB (3395415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae56cbe4f2021a93eec8cf2b47ecbb509f0f585747e6cff56a30512ea09519b9`  
		Last Modified: Thu, 01 Feb 2024 00:09:07 GMT  
		Size: 12.7 KB (12652 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:4b1e1de90bf00c19a3b14d59a6cca268f114f46bdd007461629ce929bc0d9e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292863937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4847baf2984a9d4405f6654f29e6f373662228e1c7693ba6ce90cc3ac1ec2eaf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jan 2024 18:59:53 GMT
ADD file:fcbdad385ae78401c4f5aebfeed9ba8edc6adcc9870a328a756cef32458e50ca in / 
# Wed, 10 Jan 2024 18:59:53 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 18:59:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.75.0
# Wed, 10 Jan 2024 18:59:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:5d34c3dd8c95d308ec07fd694f24411653403413305af18811f2d53cc052f152`  
		Last Modified: Thu, 11 Jan 2024 02:39:25 GMT  
		Size: 33.1 MB (33120536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8442a04ba51120f902bde9098a254275caf3744fb2b2001eeb9e2604b705ecb9`  
		Last Modified: Tue, 16 Jan 2024 19:25:36 GMT  
		Size: 259.7 MB (259743401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:40bc525015b113109f9ac5ba7fc42219e341529a9f6589349a63e8adab699aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3401516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dab651bae9e16da51ef282e173ad0b0f9bedfb361cf1f1525cb91c4c315de9f`

```dockerfile
```

-	Layers:
	-	`sha256:443f7dcc31660a5e5b7b310c72264637b461d393acc1ad1f075ff14eabe6e7db`  
		Last Modified: Tue, 16 Jan 2024 19:25:27 GMT  
		Size: 3.4 MB (3388920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27b85cdb3d64fac0f06a150278cab6949ec82f653f43873b50aff6148e568567`  
		Last Modified: Tue, 16 Jan 2024 19:25:27 GMT  
		Size: 12.6 KB (12596 bytes)  
		MIME: application/vnd.in-toto+json
