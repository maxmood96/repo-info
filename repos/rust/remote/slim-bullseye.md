## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:9f97e865e78727d9821a931ae0b61089983f2f1b88ab59bbe396e366478b22b7
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

### `rust:slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:466bd7fb2bc6b8aa9c36654421b6d560b1a5f04e47f51834eebc369bb24e3eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268626429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ddd21c4dc11ee6f5423c49851a9e67505df86e0cdb38c381dbf0736585cdaf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jan 2024 18:59:53 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 10 Jan 2024 18:59:53 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 18:59:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.75.0
# Wed, 10 Jan 2024 18:59:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e7e2915107b3b509c0216565cad51b8992d66e254768c0633f31d1ce3223d6`  
		Last Modified: Thu, 01 Feb 2024 00:08:52 GMT  
		Size: 237.2 MB (237208602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a454a204709c497bc4152fd21b9a63c6b460205084e347113ec0f6d48d814725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3510661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992fccb4707ca41738ea5b5dcc1862c47990e6af4acd4c36536b5676b622f6ef`

```dockerfile
```

-	Layers:
	-	`sha256:c930929b268517785f828c381bff0f0c2b52ad2f4eb7b51bc08edb575bf7b3e5`  
		Last Modified: Thu, 01 Feb 2024 00:08:46 GMT  
		Size: 3.5 MB (3499147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eb82c13afdff594b59af16c279b2e7411e6e8f3e61b32fb5bd6d7818e5e5e8f`  
		Last Modified: Thu, 01 Feb 2024 00:08:46 GMT  
		Size: 11.5 KB (11514 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:933b8e3fe55199ae4165a5fde7618c6055730ffef5f150d5abca0d31fe7e56cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283556980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b372bfbc7fcdf37e5db4db7653ee04f5f177149f7f40d0467102adb5c8f3a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jan 2024 18:59:53 GMT
ADD file:1a36d919bfcbaa6b981b71ce99d777d303e69c2d6cb1924992e5a9cd811c11c5 in / 
# Wed, 10 Jan 2024 18:59:53 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 18:59:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.75.0
# Wed, 10 Jan 2024 18:59:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:d976170654fe1bc717306b8bf14dc57d20e331b13e4797bc137e6911aa745a8a`  
		Last Modified: Thu, 11 Jan 2024 02:49:26 GMT  
		Size: 26.6 MB (26578974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49141bb3a142c5b3a51f0e3781d06d3c13972f2369d7663d7f84db4113d93c3a`  
		Last Modified: Tue, 16 Jan 2024 19:50:00 GMT  
		Size: 257.0 MB (256978006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:01de3f353e9adcf59fddbb71b25862d80ac05e556a121b4d8bf90dbe84ec5764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3345081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949de0d46156366d466ed4199baf4d22f2a51fdcf2ce2b18e5bbfd6171c64143`

```dockerfile
```

-	Layers:
	-	`sha256:9486d8a4ee98dc193c6a98ad226ce11aff1e609c8eacf3cf841ca657ea0b13b7`  
		Last Modified: Tue, 16 Jan 2024 19:49:52 GMT  
		Size: 3.3 MB (3333664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f82571df634e60ca5e37f387bd9fdc6e88f6c4afdfadc2f94ade91fbafc7d0fd`  
		Last Modified: Tue, 16 Jan 2024 19:49:52 GMT  
		Size: 11.4 KB (11417 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:439100ff9aa7d128f2169162212bb1bce996412578d530be130d985106241aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.5 MB (333515905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64584d57d2775829fcba928e70d5888481c051b8468881469d5fa7116957864e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jan 2024 18:59:53 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 10 Jan 2024 18:59:53 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 18:59:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.75.0
# Wed, 10 Jan 2024 18:59:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe34a26a30f355e8377a739875123f9a136235698af6b6417b9312924f45895c`  
		Last Modified: Thu, 01 Feb 2024 21:35:43 GMT  
		Size: 303.5 MB (303451571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6492b07a5fdbd93ea1649a1b46ddce7a5e76450a1cac80214ec1d39f92d39093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3507809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d428f06f583fb820346c21be971efab85d8f492a493b1372af0050245229b8`

```dockerfile
```

-	Layers:
	-	`sha256:9d8b0c3b26684eb76a067ab15f9a27886763722c02ad5ba55a82ff294eda986b`  
		Last Modified: Thu, 01 Feb 2024 21:35:37 GMT  
		Size: 3.5 MB (3496453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d2c60d3df9827b80d8deb49d7a9f77cce08546bdf4eb62115507445e036a4ed`  
		Last Modified: Thu, 01 Feb 2024 21:35:36 GMT  
		Size: 11.4 KB (11356 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:ea9cf4aa4f77ccae21cd53bd566c482dc00c3810ae4e2a2bf1311b7621b4d8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283827402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d86ff40cdb551e6ee81ca9dad3867f6cb79429045900990b51c046d8a3febaa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jan 2024 18:59:53 GMT
ADD file:0e0961062de8ea0706118b883ee7638aae4465761dec06896f1bd28b9fb4b516 in / 
# Wed, 10 Jan 2024 18:59:53 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 18:59:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.75.0
# Wed, 10 Jan 2024 18:59:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:854acbf4b2df9e625a11c0e67025dce58b41d948bb7e5d4d5e708e25489f6e8f`  
		Last Modified: Wed, 31 Jan 2024 22:44:37 GMT  
		Size: 32.4 MB (32402507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8370385cc2805da79227b1da5196d803d585bce5b2374b1c147502449c3e084`  
		Last Modified: Thu, 01 Feb 2024 00:08:51 GMT  
		Size: 251.4 MB (251424895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:0f8438baadc8f1b42167591d890807bf8eefff5a62c4ad8081ce68c08ea51b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e3ad16686819e61018ef9d5eb024b86078572282d56216fdc579103df41e83`

```dockerfile
```

-	Layers:
	-	`sha256:263fcff2f5c691450af9fd2a0c430bfb2fc9e9c7ad08e735fd5e3a0bb681264a`  
		Last Modified: Thu, 01 Feb 2024 00:08:46 GMT  
		Size: 3.5 MB (3491203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c0a534a2096f1c6233fd05df3d02b0335cc5111cb218f23dfac80fd19015760`  
		Last Modified: Thu, 01 Feb 2024 00:08:46 GMT  
		Size: 11.5 KB (11485 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:0cb4fb68e818232560ea323fc0049a53f35290a642d4b085f36951286a3ec36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281085570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c019a5bb7f6aa4abf5f92d36be970e56b7f756434981ed513a12fb7b95a46429`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jan 2024 18:59:53 GMT
ADD file:35bb0428da48f0fbc9230db1ecddacb636bc61d82e6701574b518b720ae76d7f in / 
# Wed, 10 Jan 2024 18:59:53 GMT
CMD ["bash"]
# Wed, 10 Jan 2024 18:59:53 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.75.0
# Wed, 10 Jan 2024 18:59:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='f21c44b01678c645d8fbba1e55e4180a01ac5af2d38bcbd14aa665e0d96ed69a' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='e7b0f47557c1afcd86939b118cbcf7fb95a5d1d917bdd355157b63ca00fc4333' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='1032934fb154ad2d365e02dcf770c6ecfaec6ab2987204c618c21ba841c97b44' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:4df9a94c24ca5c52fd8a7f1aebc76690845edac56c36acaf79a984722b5e4e48`  
		Last Modified: Wed, 31 Jan 2024 22:35:16 GMT  
		Size: 35.3 MB (35293643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c14458f3c13bdec70c32ef01b89c759c60fa2946a58bc6087a4f16e9dfc97f`  
		Last Modified: Thu, 01 Feb 2024 17:22:39 GMT  
		Size: 245.8 MB (245791927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:702a9def7f6768a5d809f047fa3db1adcf24c5f44bf8207984909c573a3f0b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3477656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7464fd71482d3c484893d0bfbac4aee4a140e2a5c3b575fa5d73cddb25a943c2`

```dockerfile
```

-	Layers:
	-	`sha256:de5b9fe1099e373074f2cf6e7e63a9ff878241e7877c4c17a50c09d679ad0b7c`  
		Last Modified: Thu, 01 Feb 2024 17:22:32 GMT  
		Size: 3.5 MB (3466272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:470eff1bc496fc19b41e18f535b1192cdd48a0043fce183e6cde659eece7fe4e`  
		Last Modified: Thu, 01 Feb 2024 17:22:32 GMT  
		Size: 11.4 KB (11384 bytes)  
		MIME: application/vnd.in-toto+json
