## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:acf5a96dc3176ec85412a3ab4394a2fcbd4baecb0c142bb0db7381024bd1909a
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

### `rust:1-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:4d97e2a4297727a5fb59ce5cfebb0bfd06c97311737e473466671c08159d3130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279881584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd2eb15e3fadbd7c70467d95ce4e37e54b22770a92df45c59736fd755880107`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Mar 2024 15:56:03 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Mon, 11 Mar 2024 15:56:03 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 15:56:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb15ef77ffb54dd96d76bf6a36d8d6be648b636bc1223b10a2dfe4a2447ec93a`  
		Last Modified: Tue, 12 Mar 2024 01:57:38 GMT  
		Size: 250.8 MB (250757403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:99b0158b673025282375a821440167ce36abc1d111710166b3d700c2d24077a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3933048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4dd4e54c90a3bc2b3b7d67508d2450f9ccbeda2360ab7d61ee10e2d69ec50e`

```dockerfile
```

-	Layers:
	-	`sha256:a25e338fcf84ca626e90db9ad0f689a31826ed0133f0595b9397ae4dd8d763bb`  
		Last Modified: Tue, 12 Mar 2024 01:57:31 GMT  
		Size: 3.9 MB (3920346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d295e3650a2c777d471095859678a872a75283ea5a6ab2a59d0505afe250d4f8`  
		Last Modified: Tue, 12 Mar 2024 01:57:30 GMT  
		Size: 12.7 KB (12702 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:1feab1e60fc1afed053bcb51348eec1db18c7b65126f53ec55208098a4ecfd67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289130756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52240fcd117b1dfdaf7ead6def64fbe5b07b549b609a8a8f06806bf88376589f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:07 GMT
ADD file:9766a0d12bded41ae2e7bcaa8d246afb6f5d5b6d2222e97193d07737d3f5b609 in / 
# Tue, 13 Feb 2024 01:20:07 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 15:56:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:7a5e2a926145215a27b5a8051ed294061243135af64539be80d4449e05f71f52`  
		Last Modified: Tue, 13 Feb 2024 01:26:50 GMT  
		Size: 24.7 MB (24716645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fbcd2eedbc5fd5423f9a42c52a1b36ad360b82f74e551301d0f8b8b1afda1e`  
		Last Modified: Mon, 11 Mar 2024 20:04:06 GMT  
		Size: 264.4 MB (264414111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b6060cd40c864100a1bb2e2c64e2a7b6ebc73730b5288b0d5597b36ce9688c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e99d403a9f02959952368f364eaa74de5ca8eb032ffdbf6fb21b8777713969`

```dockerfile
```

-	Layers:
	-	`sha256:bba8069f716d0f5e800230f14bab244ecad5b2adb9368641db6e6a8dd26e7046`  
		Last Modified: Mon, 11 Mar 2024 20:04:00 GMT  
		Size: 3.7 MB (3737518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d11b8c5a4b3a1a2cf58271c6ced2ef263b8a73b56f5e56383684b5ed0a6ab2c1`  
		Last Modified: Mon, 11 Mar 2024 20:04:00 GMT  
		Size: 12.6 KB (12637 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:da63f7373999460f8610b2fb2b2cd309b36664ff0a60ceef3d22445f45b9be0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.7 MB (344651807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b012da62d236667ca4033767a8f526838cdc26f2a9205c775a93a1ae10c7485`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 15:56:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5e10d484d85b01d69f114ab24609f20510e8a95358797590c23ed916b63901`  
		Last Modified: Mon, 11 Mar 2024 20:00:29 GMT  
		Size: 315.5 MB (315495444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1da6bba66cffcbdcf1c6f1de0be35d61598d331da5df6cb9ae119b43e83c0315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3955182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7a275862a31eb4306e69cc43c73e34b88c3ef978a6d40efa13a7a9d847660e`

```dockerfile
```

-	Layers:
	-	`sha256:e7c2257c707c6b937222e2151bf855cefa3acf27fd001b571c2a46f4881ae47d`  
		Last Modified: Mon, 11 Mar 2024 20:00:16 GMT  
		Size: 3.9 MB (3942630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96e3ec7151527c5ba790dec4c76ecf0d3aec292ec33d8c3cc861bcc9501b9495`  
		Last Modified: Mon, 11 Mar 2024 20:00:16 GMT  
		Size: 12.6 KB (12552 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:c03ffa0509c87598ac4aa8887ae4c440b300f3b9064680045eaa24d6ed0d6e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.2 MB (291204007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065925f04e1b71bb8f63c5a16c11f7cdbb8fabaacfe55717206ff4d90c7e9617`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Mar 2024 15:56:03 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Mon, 11 Mar 2024 15:56:03 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 15:56:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fe77b3df121565227718afe1c6b248423edfea08b27b184f46c8e8fa27e991`  
		Last Modified: Tue, 12 Mar 2024 02:01:23 GMT  
		Size: 261.1 MB (261062134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:77ede3a6960447382fb148e28e44ba5b35faba25d774ed3a111fb6fa8ad6ec7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3914698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3025cf24a2d2819840ad6dab81988127ad52a402962b552002e5ab167244e1ac`

```dockerfile
```

-	Layers:
	-	`sha256:56d00834ba968dcb6a6562b8e5d678fc476b5d013db6bbacb2812aad22f23e42`  
		Last Modified: Tue, 12 Mar 2024 02:01:13 GMT  
		Size: 3.9 MB (3902045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03b0cfa1e238eca9716c2f738bd53a58c6281e8d6afabf55b3821f954fd77fc6`  
		Last Modified: Tue, 12 Mar 2024 02:01:12 GMT  
		Size: 12.7 KB (12653 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:3a08e57222cd5391f8c5a8b0783501c02a0bd203ef6b5d1d9a31609215fa294f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295272427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6a328fcd9613febb9ce7d9cd90f738bfb0d140526d24348b82828e596fc153`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
CMD ["bash"]
# Mon, 11 Mar 2024 15:56:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Mon, 11 Mar 2024 15:56:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdd67ab6451ca83efacd3922162d6ee5fb727ca6ad58a2367d69aa20f6e39f4`  
		Last Modified: Mon, 11 Mar 2024 20:16:14 GMT  
		Size: 262.2 MB (262153519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:0716e1f2aa809a3076a6180cd172d1eece72d9167ff6002f750b59e5dcd703d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3905390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72cde117446677f331a58516913110b4e434273345ba2b027a272bfbd329a28d`

```dockerfile
```

-	Layers:
	-	`sha256:38d1062f6c9567cbea8582c6da8ae4e9210d342231cc0c063c234d6cf2e15a71`  
		Last Modified: Mon, 11 Mar 2024 20:16:08 GMT  
		Size: 3.9 MB (3892794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:becad4964c3ece0633a328d6611eead4e21fc844abd86db81feb0e4b44b98065`  
		Last Modified: Mon, 11 Mar 2024 20:16:09 GMT  
		Size: 12.6 KB (12596 bytes)  
		MIME: application/vnd.in-toto+json
