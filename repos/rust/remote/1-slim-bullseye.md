## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:6a86f360ad1b46b21ab3452b5cd8e1541739341e880fc3efb9b9818e684d4985
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

### `rust:1-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:642848c4c3aa8d0afbfb4ca79a62f4990f0f9a488c9fcb6bab4f69b9ec3c9086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275916019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb297170af6cffe9cdab19dccbb60c7cfd1c3f0e2d00f6ba2275c526a2504f91`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
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
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d388dad14656ef1387ef7d81b3a009406d5d9d77a5136fb6c3a9b5a8e76e20cf`  
		Last Modified: Thu, 05 Sep 2024 23:05:05 GMT  
		Size: 244.5 MB (244487342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:752e633d9a7a1899c66e16e9b2b4616012116caf811a9699681579e5ca183ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4176179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21acb0736a28fa7c66a74960b7a19abe6f6090ac8c701e1a350feccfd2808d1`

```dockerfile
```

-	Layers:
	-	`sha256:1e1df90e4e70b0e069b19e23953f3aee4645de2800ad7013e8651cdf384986ca`  
		Last Modified: Thu, 05 Sep 2024 23:04:59 GMT  
		Size: 4.2 MB (4164313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96b5b11d5b0c5f5b63749cab85ff9d8f5c71159729abb29eacb424158dfccccb`  
		Last Modified: Thu, 05 Sep 2024 23:04:58 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:0f937dc535c4023f9c67bb1b87fcbfba9e18ad0b011953f3752108a453221022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290373595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc14e1607d44ec367938ba4b7368e8b452d71d967a9779222ee70f1703e805f1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:c451ece1244c14bce110ffbe6906867ce12f8e88234988b0edba91009a9dbbf8 in / 
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
	-	`sha256:f572303598915f7fb61cc4b47f7207c9ee64d52b9db5fc03ee133ec2dd679347`  
		Last Modified: Wed, 04 Sep 2024 22:02:25 GMT  
		Size: 26.6 MB (26589615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ae599f44e3fdade4d6e6401bf5bd4253fe4160ef604c43147845b8722eef9c`  
		Last Modified: Fri, 06 Sep 2024 05:36:09 GMT  
		Size: 263.8 MB (263783980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:50b2bb90c25335c23388a2c79c43dba5364d92f1004c6b6d47656f04076bfced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3985598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dda8f3568d8a529772149b06db644274bee2ca0bbdaa960580f443399e8bf7`

```dockerfile
```

-	Layers:
	-	`sha256:bb6aa43f747c7e6c3e221a82a11ae547f3e05800376c61e59600b7fd6d5ba5dd`  
		Last Modified: Fri, 06 Sep 2024 05:36:03 GMT  
		Size: 4.0 MB (3973664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57194920ed42b9ae9db6362cbcc50ea1b3dfa2637b705e067ef51181a9a6aab9`  
		Last Modified: Fri, 06 Sep 2024 05:36:02 GMT  
		Size: 11.9 KB (11934 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:316ebb761aaddd9cc29b6071ad58535af3a00f1ef5b2e82df91de037c6f54e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334322977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e8455d8d4e52d1f75628e9dbc2a00e33cfd2a6f46a5b97c8fe0a00460a8d54`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
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
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08443790925c1472128842a72055c35c35ef5be34b66c7c2de8451c09c2800e1`  
		Last Modified: Thu, 05 Sep 2024 23:24:06 GMT  
		Size: 304.2 MB (304248612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b964e4b702213d37495a07c9d5832bf9bb0c4ff3269403ba80d94f6b743625b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0191164e32f761c00db0cb640f36a15b0062db37792b0d0f7bafe8d701dcc67d`

```dockerfile
```

-	Layers:
	-	`sha256:9f9f556c8d4632f6cff8cf8e365e2e0e799393eb531c654bb4ae3bda31847881`  
		Last Modified: Thu, 05 Sep 2024 23:23:59 GMT  
		Size: 4.2 MB (4161095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f3105fb09f27a3a2508d68db3df6e4ac4327fbc13740a227e1794cee61f217b`  
		Last Modified: Thu, 05 Sep 2024 23:23:58 GMT  
		Size: 12.2 KB (12175 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:7bdc070c9adc0187834ee1186bb70b7063d0641eb114f66316cf162e5985785b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290533892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad77317226fb99561724a6b15fa20ce48717457d6211575151bb8d6362b9359`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:9177ff00c3abd0afc64f577295a060d88f4daed1042f024f7cfcfcd8cb1da9b8 in / 
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
	-	`sha256:2e34c6adf259f6e5265d64b5a01b92c3cc93548f22be8c1ccc578b7e9babb30c`  
		Last Modified: Wed, 04 Sep 2024 22:48:51 GMT  
		Size: 32.4 MB (32413314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28b70925923f91bab783596d5dca2fa84132b0448d9e699f64ec588f8d4fdcf`  
		Last Modified: Thu, 05 Sep 2024 23:05:03 GMT  
		Size: 258.1 MB (258120578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:60e6e6e97daf4299f7ef4d1c2096611a9ca673fcd55f0805b743dd6dbe096c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c571fe973b604af5e2301bbf39cc26ecde58f2a945d8dcc1fa7f8b2650c4d8c8`

```dockerfile
```

-	Layers:
	-	`sha256:4a4d123b483d7018c2de8ab380d9459d653d97e0ede4692df2a477407085f33e`  
		Last Modified: Thu, 05 Sep 2024 23:04:55 GMT  
		Size: 4.2 MB (4156081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11bbe4a62cfac441c96dacff08b67adfc5a93c2139b6c735b7d4338c5d7742dc`  
		Last Modified: Thu, 05 Sep 2024 23:04:55 GMT  
		Size: 11.8 KB (11837 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:8decec112addbd13695a85c3e36cfb3cb2234d665990d6f69a9bebfb0bbc1cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.0 MB (333036407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0333435dde12c12f5b045e83da42c26356268ad32349b2de967ad73018c3f85a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
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
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef013636d6b4779de60a6daee7eb6d85444109ea750ff43367edc3b44048045`  
		Last Modified: Thu, 05 Sep 2024 23:39:59 GMT  
		Size: 297.7 MB (297737133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:656e87dfd5b323b3534529ebb6d0988156203604648266168165a837d1ef6dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4137155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5059fbdba445f288b2849f55639287d8333cc7655e843b9fbe7c85020c224d`

```dockerfile
```

-	Layers:
	-	`sha256:d25bcba9a065f355cde74f818a97e486db851e80f67a0a407d235d79d3ade18f`  
		Last Modified: Thu, 05 Sep 2024 23:39:43 GMT  
		Size: 4.1 MB (4125251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d6c5709ca112dc1e234b9723a7a09ca1019d006a2afcc4412640d98e4fea32`  
		Last Modified: Thu, 05 Sep 2024 23:39:42 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:f1a0949c9448b312796a4aec2d6154e999eb2f96afe929b603a213508841435c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340544165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de8960b7a01ddb04ba5bfd4bfb32db85f2897b897dd86ec4323b2621f22f4f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 20:53:31 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
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
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306069be260e0429366a2595212c3875058050805ba1b96aeea8dab379bb2415`  
		Last Modified: Fri, 06 Sep 2024 03:50:36 GMT  
		Size: 310.9 MB (310880718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f155f0ff66d7853629c893ae2d504e8682516a9b70a7cd93d5a8908014def30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c44c2520b53671c6568b4dd36d9c48258d46aa1996934dc922e3db2e6f40e4`

```dockerfile
```

-	Layers:
	-	`sha256:5f3a48f9f2e94610235d8c5b94113c04789bc2d5645daf17048ffe8910ba4b8f`  
		Last Modified: Fri, 06 Sep 2024 03:50:33 GMT  
		Size: 4.0 MB (3996088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69bbabadfe35e88452c9b6e7c9598c0207c7f8a45727e3d37f9cadf57d18f76c`  
		Last Modified: Fri, 06 Sep 2024 03:50:32 GMT  
		Size: 11.9 KB (11866 bytes)  
		MIME: application/vnd.in-toto+json
