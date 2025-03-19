## `rust:1-slim`

```console
$ docker pull rust@sha256:23d764637de186c9042df48a9c73e32babcca0a965260af3162a017e486a6fb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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
	-	linux; s390x
	-	unknown; unknown

### `rust:1-slim` - linux; amd64

```console
$ docker pull rust@sha256:3490aa77d179a59d67e94239cca96dd84030b564470859200f535b942bdffedf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292677821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8573a005bfcb44d5f462a33f6ad6e85d231f51e759b60c8061777422becfcb94`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Tue, 18 Mar 2025 20:40:17 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Mar 2025 20:40:17 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.1
# Tue, 18 Mar 2025 20:40:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ceaeef95ce1795f2816135a0ffe7f89ef389cbc075611930bbd36e992de061`  
		Last Modified: Tue, 18 Mar 2025 21:25:29 GMT  
		Size: 264.5 MB (264472956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3800e7f8330e51f1b04f284ac23e6a94536295727200c260c59d96f3945e4f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3968599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8263a7d48fb3c411316a3316b70eea98315359d13227829051158dcaaf84dfc`

```dockerfile
```

-	Layers:
	-	`sha256:d6da186db7bd4aeeb7395f2a1422e0a73923ab0ce6ab551b7914586117adbfe8`  
		Last Modified: Tue, 18 Mar 2025 21:25:23 GMT  
		Size: 4.0 MB (3955327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0a2617ba1c0f55b6772cbcce7f0a35ed41f8143bbbc4897ec6409383c6a3f92`  
		Last Modified: Tue, 18 Mar 2025 21:25:22 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:55bb7604a8633b5518d87322a9938cfbb4aa13d3b071606b7f3faba972611eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302053077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0073b0549e9cee60c38957e3f732d374be65dbe4f52c012f9c0237817764e850`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Mar 2025 18:46:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Wed, 05 Mar 2025 18:46:45 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 05 Mar 2025 18:46:45 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Wed, 05 Mar 2025 18:46:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15096ad914e9a55f497400ae1eec7c09e5a8b04c84bff7fef25ac76844d02f9`  
		Last Modified: Mon, 17 Mar 2025 23:35:10 GMT  
		Size: 278.1 MB (278137989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b73f417aba7b5a892fcb9b1f607b50fb9d754fd2431c1876d47ef2b0a35a1569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b061928e559e26235762108ea9b6052d914fba9bf638813860795701445f5002`

```dockerfile
```

-	Layers:
	-	`sha256:02c531b321effa156e90eb5becb9f4c7883632527bf894d7ae2648875d802b6c`  
		Last Modified: Mon, 17 Mar 2025 23:35:04 GMT  
		Size: 3.8 MB (3771390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e7ff68ad0284ca60514dabe1d953191f2c09ef2e124e4253ebe71187815284a`  
		Last Modified: Mon, 17 Mar 2025 23:35:04 GMT  
		Size: 13.4 KB (13380 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:05d21de3f51ad9713705faf9cdcbc14932e714db9cb6e419d69fa697ddf1e842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.7 MB (352695522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cbb1ed086d71df687ef372f5fa00f8aa04c23efb6f3de376a38e03c708bdc8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Mar 2025 18:46:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 05 Mar 2025 18:46:45 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 05 Mar 2025 18:46:45 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.0
# Wed, 05 Mar 2025 18:46:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d16d767bdc3b511bf4b1a0e9cea25f23f6aab04ed159f85f0283a0abc8254d`  
		Last Modified: Tue, 18 Mar 2025 01:08:33 GMT  
		Size: 324.7 MB (324651485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:2a51b164879bfb7341a05b953f255c248b5c153892936aa8a862e40f1f4b8dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3991094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569af3122c5d09662177ab07c9237165605cc870ae29ced193d9101b496a9530`

```dockerfile
```

-	Layers:
	-	`sha256:b3249f576d23e4e7548245cccb4908affbe646644ffea586a921b59d37c03698`  
		Last Modified: Tue, 18 Mar 2025 01:08:27 GMT  
		Size: 4.0 MB (3977670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aa3217f06728455621bdfb1c3853c2875ea4bc15de0a43fcc1dd527061e82a2`  
		Last Modified: Tue, 18 Mar 2025 01:08:26 GMT  
		Size: 13.4 KB (13424 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:98c3b8e2721a704bc2eb62b98ffde90aa679060beab5c0261fc9fb3e53dcb96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307651943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb51296acba9d650ac317d3461d2ac9bb540d6fb81dbd61b1a1428aa6ad2c696`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Tue, 18 Mar 2025 20:40:17 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Mar 2025 20:40:17 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.1
# Tue, 18 Mar 2025 20:40:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8311170da78e0f4f02362ae6a659d167810f709742e70452a97bc1ed6c226f0f`  
		Last Modified: Tue, 18 Mar 2025 21:25:41 GMT  
		Size: 278.5 MB (278462415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:282e52a9ac85e408eedb4440739808f361af48510d8156e1c2bd4814957bdbc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8b83724ef55ef6269f1ef263febeb2abbb942a857b78e1df41d6dbf88190f3`

```dockerfile
```

-	Layers:
	-	`sha256:87781db510b3a315ee0cc106bbeaeac2133f6fd20338792d8fb660f68a5c5659`  
		Last Modified: Tue, 18 Mar 2025 21:25:34 GMT  
		Size: 3.9 MB (3935242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb30fbe43624741478c4b17522efbe40f63fae35fa6227c10eb334d3616d646f`  
		Last Modified: Tue, 18 Mar 2025 21:25:34 GMT  
		Size: 13.2 KB (13220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:fc579f0495e04131cb8e993755d7e4f040176336759fcb4367b45f0b2611e3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355163739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df30ac614af5e02ec8ee2e7ea1bc84552ca4603cc20d28a0899cf33ac2e76ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Tue, 18 Mar 2025 20:40:17 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Mar 2025 20:40:17 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.1
# Tue, 18 Mar 2025 20:40:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a154c2bdc6a11563f78df213685631567f9761ca9decfb07902d68d5063fbb`  
		Last Modified: Tue, 18 Mar 2025 21:33:45 GMT  
		Size: 323.1 MB (323115925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:59b9cc59f93e10f8aff809c7a58f4c519acdff37696ac47ab4055a36cd49e209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6e50b05a466baa1e6b4de22234899deeb3a3a8dd277f3931c77a8f3f20a44c`

```dockerfile
```

-	Layers:
	-	`sha256:acc33250743a699f68eb5104c68a097737d1e1774041cfd458d9c55a579ced03`  
		Last Modified: Tue, 18 Mar 2025 21:33:36 GMT  
		Size: 3.9 MB (3927888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ff11a085b00a2e25d981a607dd04b609d0848fb44418b0e74dfc665925044a5`  
		Last Modified: Tue, 18 Mar 2025 21:33:35 GMT  
		Size: 13.3 KB (13340 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:205325fca6274a10d37653331b3f19ef277ae66494347092234ac5561d2cbb3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358820914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0fb4fe53407c69f034c4948f4088c76a988d9c9713ffceecfb92dd9d4a8425d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Tue, 18 Mar 2025 20:40:17 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 18 Mar 2025 20:40:17 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.85.1
# Tue, 18 Mar 2025 20:40:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3339fb004c3d0bb9862ba0bce001861fe5cbde9c10d16591eb3f39ee6cd3e7f' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='62cfed758140f94a75074fb350e287dd26d1b6c9a4d6a18616757fb344720bcb' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='c64b33db2c6b9385817ec0e49a84bcfe018ed6e328fe755c3c809580cc70ce7a' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='fec8226fede82b4b886855e4f1b69cdd17a6f60afdddb17f9a814b743c2d5c47' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b1ef09a734ece551456635b25c91a97770392b74c7f793fbc58575ddf0442645' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='8e4e8d5ffd3e6996303faf45670009388f73a4796264230f04f5c29809620c20' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6911e14712af2d8acf94250262f769551e3be5055dbb7dcb50db2e0e43a8da2`  
		Last Modified: Tue, 18 Mar 2025 22:20:09 GMT  
		Size: 332.0 MB (331959855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4fded135842d3f60ffca5c122ad756d13f2e312e5ac4b0adf36ce9b22d025b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3810499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096bf090e3642118b049ce839e933a3e93cb32476981d83ee53944fc7ff96bff`

```dockerfile
```

-	Layers:
	-	`sha256:6b2aaccf85296dbd932b29b64b5e3516f3ca21732bd6cf3033642f688907b47e`  
		Last Modified: Tue, 18 Mar 2025 22:20:04 GMT  
		Size: 3.8 MB (3797227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdecca535d59b793a62c3c9fa83c4735c93893628177317b07be045b6856788d`  
		Last Modified: Tue, 18 Mar 2025 22:20:04 GMT  
		Size: 13.3 KB (13272 bytes)  
		MIME: application/vnd.in-toto+json
