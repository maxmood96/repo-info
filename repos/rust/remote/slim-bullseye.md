## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:1a0ae98affa8f875bd0107143f97b7333d731d1c7eb3f81601ae0751243aaba7
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
$ docker pull rust@sha256:e3703a692d6689cee0490363bfc8108a9c9e590df6988f2920eb71ab77937c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264463700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fc023abba24900ad681ae8421b1f2d1c477a0cdc7f8779c5147a5df2e64d1f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ab2f2a3ce344d856412bb76c0cbce30a35aeb53176eb5cec120e3c216f01a`  
		Last Modified: Wed, 10 Apr 2024 02:56:20 GMT  
		Size: 233.0 MB (233035962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:93f63b6fad174237aa1145d25dad1cc04f8aea997947828b38063021fe446db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78abe840ffae11375c7e3b134fad5ba0df3447f6e29e7245a2f7719df6a63b15`

```dockerfile
```

-	Layers:
	-	`sha256:6f58cc69594b21ac6cab79cbd7ffe7bb3572c3a95b2e9e4d2ab1e80b47bde438`  
		Last Modified: Wed, 10 Apr 2024 02:56:14 GMT  
		Size: 4.1 MB (4139675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a713004d07c70ce533a189ac1c7759bf8978f36fa4e86386307445c2f7a4b4df`  
		Last Modified: Wed, 10 Apr 2024 02:56:14 GMT  
		Size: 11.6 KB (11626 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:8aca37551f443b83fc41d8e420dd85c4fb39876025a9dc0c8c4a875599d8eb9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277474858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d53503de09ea3608bc18b50a1c520242c3303cf5cdf553e8903b2e3e64ff0df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:f7685078edb9bb9e45a932713c0364f985baac4241d098518b48718ca3f587aa in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:e373dd4d84cbc3bf4d587e26357a41105c418866d41051d5ad5d54c706941e10`  
		Last Modified: Wed, 10 Apr 2024 01:05:12 GMT  
		Size: 26.6 MB (26588474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf2c6214c00d254b01b9963272ac40745b82b566ea309692ba97530cee2f8b1`  
		Last Modified: Thu, 11 Apr 2024 11:19:23 GMT  
		Size: 250.9 MB (250886384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:f95f9472df530b36e47942cca0534998f1f624e670401dbbb2adab6546efb333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04943ad4c452dec70e3a1ce9a89f7c5455bcac4fb271e8d672556009c1bdcd4a`

```dockerfile
```

-	Layers:
	-	`sha256:4757646cebc8f798ad16826910f8db480c9014980cff1bd3c86985af82fa4200`  
		Last Modified: Thu, 11 Apr 2024 11:19:18 GMT  
		Size: 3.9 MB (3949600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd705c9420916009abb8672f4e3ea4211867bf570e070ac66a543a94c3238603`  
		Last Modified: Thu, 11 Apr 2024 11:19:18 GMT  
		Size: 11.5 KB (11529 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4c5434f97e2e831215a9c5ed5abdf21894ad3c1e7f85f3661cc20c4f1d5fdcf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327435048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3e88fc0ee536589d8ff9f84db749baeb19f637ca9d3ca26f872061af6ab348`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00ffe28413ff737e9319fc6b161f92951752ebcccd38ff443b7b7a1bf7c46ec`  
		Last Modified: Wed, 10 Apr 2024 21:19:30 GMT  
		Size: 297.4 MB (297358742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:07546376e3d6ff97ef9245f0ddf9c23c2343abfcfc0d612ecd603355351e4fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b9a0d3926f551a4aa8aa4b4aa20168cbead544a81f98131d46e0b3d74339b3`

```dockerfile
```

-	Layers:
	-	`sha256:80783504581f38a49f386edba09b9cd5153392c5ad0174015ef551f090f4452b`  
		Last Modified: Wed, 10 Apr 2024 21:19:23 GMT  
		Size: 4.1 MB (4136557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:333d3575ff26376a87ab3ee97463a3424ff3ef7b03e78b7c28d8433a6e4586b9`  
		Last Modified: Wed, 10 Apr 2024 21:19:23 GMT  
		Size: 11.5 KB (11469 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:e47eddf08aa277fd773b469789469b80214dc1c6eb89cc52dbaed2a45572b346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280210792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c34fb5b92c2203fcb8db1509344b4fad479143f90c59036e639d20e6cf231`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:107da403005e1b6808da193b1f269be14ac31b0bd6d87b7609e9080e75f08eab in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ec8b01fa71b8466600831f50045cfc2951257ac6eee36ce2a0fbe3dbe0098d42`  
		Last Modified: Wed, 10 Apr 2024 01:02:53 GMT  
		Size: 32.4 MB (32413416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f761c683b352d393ff3a70a31f1cdb3309470baef708acaaec1d5f65178a780`  
		Last Modified: Wed, 10 Apr 2024 01:54:11 GMT  
		Size: 247.8 MB (247797376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d1306fc47b4244d7f9e7943f5aae84fd486ba130d8d39c608767cb956ddf3271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3908b559c177afd6719140b5a2a3541d95e0921cb245764b7a06f080971b6ac3`

```dockerfile
```

-	Layers:
	-	`sha256:a032ac7469111c4a51d7d1e1b0c75b35aa34e3c8b0d8d8e5bd42030f843b8926`  
		Last Modified: Wed, 10 Apr 2024 01:54:05 GMT  
		Size: 4.1 MB (4131731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0b157250963b35b33549efb108518a419ccc9f570c228ba225ea203828b0aa6`  
		Last Modified: Wed, 10 Apr 2024 01:54:05 GMT  
		Size: 11.6 KB (11597 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:a63f38c0ec7a495b5327c4fd3529513a1c7bc1a7f95c7708696604217089abfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278816651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03e47df5af118f1fd6697fe8a10bd00c84d003669e9807115a0a30bb899384a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:33f8251ee78dc536740a4ab4a9c9a75ab2c3f5d7be0a41f41dea318cc8e93dbd in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2608681ad30ed92fce8f1b566ae32649b5bfa30cc4df8792977ed14a0bc7cbe6`  
		Last Modified: Wed, 10 Apr 2024 01:32:01 GMT  
		Size: 35.3 MB (35304089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468a82d98bd93efa1f7aefdd71f5d2536b850b6df7127d6a700257a58695aaa6`  
		Last Modified: Wed, 10 Apr 2024 22:32:41 GMT  
		Size: 243.5 MB (243512562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3fecdad593ab09fc07ea7b1eb0d3016a9eb8f71e5ab29d31b4da3ad9b234caef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e01b2f947f5180e0f4a13968ef784360371458d30748f677f68307242d705f`

```dockerfile
```

-	Layers:
	-	`sha256:46df647f9f81d00e6fc59e6c6987cea791d70c43ba99a55ab0db0d947b780bbf`  
		Last Modified: Wed, 10 Apr 2024 22:32:35 GMT  
		Size: 4.1 MB (4100758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:120c1672876f6881be32ef97ce50a16bc4d3192a8263c0a8d42b465368e15136`  
		Last Modified: Wed, 10 Apr 2024 22:32:34 GMT  
		Size: 11.5 KB (11497 bytes)  
		MIME: application/vnd.in-toto+json
