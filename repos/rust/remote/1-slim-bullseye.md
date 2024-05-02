## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:b2d2c235a6c5e0f60d5723a48df6ca4f2c2441ad3bd28ea8afd03ec190657920
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
$ docker pull rust@sha256:ebd24f6078bcc9f6b23f99a23e450f07d593f570d4bf072b5077added128bf8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268954860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0502ee249ca6bfa22cfade789d5296feac6f0928a18703146f522c7cbf7ced10`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e70c0d176523de333ba6a5be57344d80ccfba2589ed97a0714e502d2a34ca43`  
		Last Modified: Thu, 02 May 2024 17:53:20 GMT  
		Size: 237.5 MB (237520597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a4dcfa88f53f7b2928efe6b3b835f897d81e20fddd853c43354998e2e042cabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ef9d771e215a52ef1e40b292ede0d829c632e49e4c2367b41dac17ea648ac2`

```dockerfile
```

-	Layers:
	-	`sha256:cef011c9722bb44d4620b4e6bf096623230158399e11cb7d6d6f6c1a1af4bd58`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 4.1 MB (4139833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:599c91eec4cbd0f1ff1398eba0b589af02754a51f58dcd99213c8a7b227dac30`  
		Last Modified: Thu, 02 May 2024 17:53:14 GMT  
		Size: 12.0 KB (11983 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:7fcc03d8853b0c868fca3da391bdbc4d5316b474f77f2ad4c4d510bc16f400ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277276826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d64a77e0c4a24b62540d60a1ea1a05e5026c6bae3809782862e96dd5519862`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 15 Apr 2024 05:37:46 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Mon, 15 Apr 2024 05:37:46 GMT
CMD ["bash"]
# Mon, 15 Apr 2024 05:37:46 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 15 Apr 2024 05:37:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Mon, 15 Apr 2024 05:37:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023aa397f1e25725442a58a72e5a336eab0a55ec4078c071a6173a31c4a45a5a`  
		Last Modified: Mon, 29 Apr 2024 19:45:17 GMT  
		Size: 250.7 MB (250682084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:bdc8975a2ac8784330d818fb376433e27b2fdf0209e46bda7f9b22035469e4c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5382df8bca202c106bda60ab0e2811d653d92371d4027a107635969c4f54f7db`

```dockerfile
```

-	Layers:
	-	`sha256:c73bff56a965620f6a9785f3667551db99c6abd22006a44c2cc2c09265305240`  
		Last Modified: Mon, 29 Apr 2024 19:45:12 GMT  
		Size: 3.9 MB (3949756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ffe79a4c3446bcc96100bc370e75bb9120698436b99396f62400165ce89dc1b`  
		Last Modified: Mon, 29 Apr 2024 19:45:11 GMT  
		Size: 11.9 KB (11887 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:95886fe58a28e6f4b7d40c690765d54493906d63f11ece7000176b9b5573d93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327241671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e84f0f1aa6a11b526bf31375c0a890dfbc3c3f082c793fe5f8068e86005a6c5a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 15 Apr 2024 05:37:46 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Mon, 15 Apr 2024 05:37:46 GMT
CMD ["bash"]
# Mon, 15 Apr 2024 05:37:46 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 15 Apr 2024 05:37:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Mon, 15 Apr 2024 05:37:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf22490665d5848902eb58fdb5288abe1860ee139dfe8db3104f9c4e2a5828d2`  
		Last Modified: Tue, 30 Apr 2024 06:27:32 GMT  
		Size: 297.2 MB (297154335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:012c3a0f379154c813d3c7856640ac6f5cddad87b26a1ef83c8508ef987f6cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1d2dacba5830c1d4eb537c21d0205211cc7a2b8b4ba18c8042c916ac3ca645`

```dockerfile
```

-	Layers:
	-	`sha256:864237cf54c45ecfb3ce86612055be9e3fbe2a4bd3442dd9ea94f379d7237e59`  
		Last Modified: Tue, 30 Apr 2024 06:27:26 GMT  
		Size: 4.1 MB (4136713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85c82b47c9ef95079363d217ea92442e5bd5fe56743f84e023a1e130d89567fc`  
		Last Modified: Tue, 30 Apr 2024 06:27:26 GMT  
		Size: 11.8 KB (11827 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:b189e96e3c85ca97178eb44feb77efb715773ecfe115c08226820247f7cd4371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283597724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d042e33fb45d8dbb5ab9375e1f445cca9f0842403742ac8e16e14a492d1379b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:20 GMT
ADD file:51089e94fd65259117206f5ee6b1fd709e8c1754176d4f625ae49abbee751047 in / 
# Wed, 24 Apr 2024 03:39:20 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:112c04b2ac24eb2c6dfef961130b9b3d298e6d4b8e125bbebaa1137d773f7d7d`  
		Last Modified: Wed, 24 Apr 2024 03:44:22 GMT  
		Size: 32.4 MB (32424773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d994d194bfa3acf9a46df705316048a9e421612eb43dc8e67d2fc7c4b47dc8cd`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 251.2 MB (251172951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:23c07842a4cfddec1e1f1e230639073243847f2eb36626a93f578ed729e42f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9ef9f2ac9c96e93217e0d144744e8d8278050716ca0834c70afa220c7c8939`

```dockerfile
```

-	Layers:
	-	`sha256:80add452afc9acafbae3ebdaf81b51e772270d4168261abc531caa3d40d6f8f2`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 4.1 MB (4131887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9032987821a421011b12f5c932db84722ec77469e7d51d50c7f52fc9d678ac72`  
		Last Modified: Thu, 02 May 2024 17:53:17 GMT  
		Size: 12.0 KB (11955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:f231b14bfd93102c404e608edce59336c32bbf5bc5b16dde3b83c3b3058aa530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277263350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6022c77c11237120364d8daebc5e4a7f79b239f345aadfe10e08162f3991d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:44 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Wed, 24 Apr 2024 03:21:47 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a8be3c69cc41100693d385b45a719b06420c1a8633ddefd2cd065116e4a80f`  
		Last Modified: Thu, 02 May 2024 18:10:20 GMT  
		Size: 242.0 MB (241951625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1bb874168defcf306f4d12a18fa1d1a431164a64175ab74ccc234d19145dafe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf50d0079f8c3085c91f49970a4c034af187ead7b500a47212bad01b95a54c4`

```dockerfile
```

-	Layers:
	-	`sha256:c87e1c0879f136a39e78ff54f5cea16d36b7126d98ada10edad69ab8afe45793`  
		Last Modified: Thu, 02 May 2024 18:10:13 GMT  
		Size: 4.1 MB (4100914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ee003b3c784435c5aab66ccdc806e9767a27f9edd3cef32418dbc7142a51ac6`  
		Last Modified: Thu, 02 May 2024 18:10:13 GMT  
		Size: 11.9 KB (11855 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:8bc2b8d188d9352aaf574be5780a32a417b891822e4ff69db4365afafcc76942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326740580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86482a0fc00f33dece3ab2320607f4f4131dd70981c060b484acddcd5044a853`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 15 Apr 2024 05:37:46 GMT
ADD file:acaea4e054f1ab7ae5cbc8f02c73b546c367aebfcc48c7fb4f0dd9f3628bc25e in / 
# Mon, 15 Apr 2024 05:37:46 GMT
CMD ["bash"]
# Mon, 15 Apr 2024 05:37:46 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Mon, 15 Apr 2024 05:37:46 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Mon, 15 Apr 2024 05:37:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6f588995519e0e04ef4c150b91ad96c3c85667869db0ad72e5a78d4fab796e70`  
		Last Modified: Wed, 24 Apr 2024 03:49:47 GMT  
		Size: 29.7 MB (29673934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff354a4edd9ef3609a91b1ea4a1b4e838e2b9c3fc806f5d133f817bc565fc5b3`  
		Last Modified: Mon, 29 Apr 2024 19:36:10 GMT  
		Size: 297.1 MB (297066646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:84742eb7467128c120fad9b72891de1baebac6f5158318829c77e55abef13be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3983854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b54f647356baff1ae0921958734872e56a7d37d3c577408f3fab9b66e088789`

```dockerfile
```

-	Layers:
	-	`sha256:21287a5375f23b37fe5c503d1f800d7cc1cf34c7a3afc7a79ac5a5c252383da8`  
		Last Modified: Mon, 29 Apr 2024 19:36:06 GMT  
		Size: 4.0 MB (3972037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5592dc2fd9362a30486770663ccf99eabc2acb63088ca5b33704e4d99de54c7`  
		Last Modified: Mon, 29 Apr 2024 19:36:06 GMT  
		Size: 11.8 KB (11817 bytes)  
		MIME: application/vnd.in-toto+json
