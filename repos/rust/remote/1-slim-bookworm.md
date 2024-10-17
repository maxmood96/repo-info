## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:5f54e4f0f25ffcb8493d73f38cbd7dd5f6b83ca78d6a33224fc326f6d654d16f
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

### `rust:1-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:45966c8f3e8348b7643bd40eb846b87015a6f1694ed2a13ca8475c5be35df8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284254306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b63b5bcc9542ec50795afee904fd719f71dbf5f3cd84e74de4c92f7808a727f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0607d7c68e964f9d197627ffe492db8c9ce40d39951ee73a3182e028b0be4e`  
		Last Modified: Thu, 17 Oct 2024 01:30:10 GMT  
		Size: 255.1 MB (255128017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:f17aeca9415c8c8b3eec6d14b5a90f91bbe302ef815e6513d5763f9b1d2b645c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3958138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010e722839b0079d58e9aa6bcd3b6446f5bd6702bbfe47fc984b869d24c68e15`

```dockerfile
```

-	Layers:
	-	`sha256:e6e2cf59070156e4177eabcbb570b524e550d23ecba4082cc0876549b6a34458`  
		Last Modified: Thu, 17 Oct 2024 01:30:03 GMT  
		Size: 3.9 MB (3945048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78cde42d64af02ec433aba2279aede7b5ce92746174556b598fd74de7abd9517`  
		Last Modified: Thu, 17 Oct 2024 01:30:03 GMT  
		Size: 13.1 KB (13090 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:08dbf3d9d24bae232365620c62410ec5d83596ff380aad5f49e27cdec7317513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294070169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e6abf46c4d525890ed87fc173518b54a4bd6a1b01b96fe447fb1d17e08346a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4408bd841243a9a42a8e256c364029c480e1b0b2865b22e70a46bde0100c866`  
		Last Modified: Fri, 27 Sep 2024 18:42:06 GMT  
		Size: 269.4 MB (269352024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:df722b016f3cca3b94348d0bc6f597be00e94961777ca5cb428cf4cdd0af6f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e61fad66437481804743201bd550faf73c0e8846ddb64f6d8bf18e0dff7a4a3`

```dockerfile
```

-	Layers:
	-	`sha256:e090a867d43bfae1fb514bbb85985f7c87fff9bd5a411d0ec1cdcf062ed1c5f1`  
		Last Modified: Fri, 27 Sep 2024 18:42:01 GMT  
		Size: 3.8 MB (3761505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bffb56d93014b97c2bf56f856a3b3c0c1c6de63989a9e8fca173c3abc901f156`  
		Last Modified: Fri, 27 Sep 2024 18:42:00 GMT  
		Size: 13.2 KB (13156 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3ba3fbf62527788a60c4908b3c389bab7f5ab6fb919ea3c771aeb9a278966253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343526226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233c27109e17c04665f9ed9ede09369aacd1865fc09fd1a6f5ac4863e32fc4a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995fd26d021eddb871651f81a432e2662de3c5b719d2248d4552105c40a67e47`  
		Last Modified: Fri, 27 Sep 2024 23:32:02 GMT  
		Size: 314.4 MB (314369857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:e4a5a923d2e13d83eb71aa2cb933b273577721a70c5ff55a15af8cd5f4d21978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3980828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633019f2483a2e86da7ee1384084a836d087aab2347f626c8490a683b80397fc`

```dockerfile
```

-	Layers:
	-	`sha256:45375e55489ffbdb8bd47dbec3eee1f67a6679081f46e4dc1ac6c76ce18b1904`  
		Last Modified: Fri, 27 Sep 2024 23:31:56 GMT  
		Size: 4.0 MB (3967417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f968eae71eae982a4adc164da8a72a293dd418f197ba71ede38a68bb18be6c05`  
		Last Modified: Fri, 27 Sep 2024 23:31:56 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:ba4ee661bb466ab49f6ceb8c6d9e9f9784bba7c6e45225187cd3c7fb1fbc12ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295093589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e4df283163309e2fdaa8101fa73b670d133162155d4cd23424016dd87db8e4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 05 Oct 2024 18:56:13 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Sat, 05 Oct 2024 18:56:13 GMT
CMD ["bash"]
# Sat, 05 Oct 2024 18:56:13 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Sat, 05 Oct 2024 18:56:13 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Sat, 05 Oct 2024 18:56:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a718584a1346679f83b1655ad2ac313c29bec26411eeb7c34dad2a91b6577448`  
		Last Modified: Thu, 17 Oct 2024 01:30:07 GMT  
		Size: 264.9 MB (264949322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4c72332e16899bfc022e891c90f0d93e00f555271f92b2e38817f8afa453c722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3939504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881ca94475147e0318e9bad8ec073ef9dd87fef510c2eed0171a3f48a81c843a`

```dockerfile
```

-	Layers:
	-	`sha256:12434a1e188136de888271297f6eb4670c269905a0833cb0c26866ab817a1eac`  
		Last Modified: Thu, 17 Oct 2024 01:30:00 GMT  
		Size: 3.9 MB (3926461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11e3392f42511d72755c775a9cd45fb9f2d612485058889a5a61cbb5dda587f`  
		Last Modified: Thu, 17 Oct 2024 01:30:00 GMT  
		Size: 13.0 KB (13043 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:46bcce128e6ab5402c648739e95aa56eb2ed32d840ff42da0975ec8428034ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344618727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4f6cbc6fd8ecc671e77ece602998ab1fa543c11db83d5d64fa6bc051b111c8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097a47a9153a9d3d44374a545c87a489f3842a16e291caf5a817ebaa5a0f1552`  
		Last Modified: Sat, 28 Sep 2024 04:15:09 GMT  
		Size: 311.5 MB (311496564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:fa335487319e81174f0920ee7efa014f25d5cdbbfdf8648c77cfeb1f771129bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f51b298cbeb650a1f7674e47e0ff5da39045f7a1c1b12678284013db4153e2`

```dockerfile
```

-	Layers:
	-	`sha256:17e6bf4b03c232f13acb280f35f3b04cad777afeab1156732f6d6e80ae08ac03`  
		Last Modified: Sat, 28 Sep 2024 04:15:00 GMT  
		Size: 3.9 MB (3917210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9673908047a020854098b5704b6ac719a43c3c5263868a007ef95e1dd656fe03`  
		Last Modified: Sat, 28 Sep 2024 04:15:00 GMT  
		Size: 13.1 KB (13116 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:1986b817125878c181d9add8424b112238bbcd915e03b3444b6e3b9962a71844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346124228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aaf144d0210bf05141bac7875bc21c09171ace17f17693c306e46ee2347cc8d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Wed, 04 Sep 2024 20:53:31 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 20:53:31 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Wed, 04 Sep 2024 20:53:31 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.81.0
# Wed, 04 Sep 2024 20:53:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='3c4114923305f1cd3b96ce3454e9e549ad4aa7c07c03aec73d1a785e98388bed' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='0a6bed6e9f21192a51f83977716466895706059afb880500ff1d0e751ada5237' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='079430f58ad4da1d1f4f5f2f0bd321422373213246a93b3ddb53dad627f5aa38' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='e7f89da453c8ce5771c28279d1a01d5e83541d420695c74ec81a7ec5d287c51c' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d24393939cc6c4eddc3a49c03d07080edb453591af15f5f40c3481b1c43289`  
		Last Modified: Fri, 27 Sep 2024 17:42:41 GMT  
		Size: 318.6 MB (318634204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:981dce7ac4cd7769d68270976ad41a566057debc664228639318ceeee2878c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb7573b7c4578171c99e4b1c475220bae80fd01a2abcc1ff7de0c789cee9993`

```dockerfile
```

-	Layers:
	-	`sha256:165fd9d1067cb2b20bc1127fb26bf62317d9ec727e17d418b73ad480975a460f`  
		Last Modified: Fri, 27 Sep 2024 17:42:37 GMT  
		Size: 3.8 MB (3787373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03aa2d5f9daee31ee7485507b38e1a42c341c49bd4f504117c96708fe84908d5`  
		Last Modified: Fri, 27 Sep 2024 17:42:36 GMT  
		Size: 13.1 KB (13054 bytes)  
		MIME: application/vnd.in-toto+json
