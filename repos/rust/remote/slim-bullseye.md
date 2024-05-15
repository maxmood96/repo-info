## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:807fa54fbd1e1cb72c8df00c9c13f15b67497db9d281a931c7175e59be360106
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

### `rust:slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:00d4e440736f20fd1d0987c2429de68ddf12471bdc5c58afb756e90133aa0147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268953496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90cc8478040e4790280e3ef0b8606ee07045d737000fd10a2fae37d54a2a5ec`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 May 2024 12:45:44 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Thu, 02 May 2024 12:45:44 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991d9a7dc8dff5240efb257e4590f4a1263fe56a15fa15ef9ca85a1d173182bd`  
		Last Modified: Tue, 14 May 2024 02:58:08 GMT  
		Size: 237.5 MB (237519565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:98d1e898b16137735bf708944e34544e5e12a68a7d03531c079814bf9d38a7bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26de6e459d59e55388d02457dd7bfbeb2b1dbf3dcb25c79ec97908d82dd131b`

```dockerfile
```

-	Layers:
	-	`sha256:7a6e00e71fbb994730e342b72ac541f19b42ae9a01fc5fdb79eff46d5fd2b40b`  
		Last Modified: Tue, 14 May 2024 02:58:05 GMT  
		Size: 4.1 MB (4139843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee7d60aebcda63e797ba4e368bcb85fb07818b1190b814087e8d1e79ee3bc2d5`  
		Last Modified: Tue, 14 May 2024 02:58:05 GMT  
		Size: 12.0 KB (11984 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:ba3addc17b025f9053e5362a542e0ee15e392838f4baedafc80d51a2972c71c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281482962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b95c0ae5048ab10cb4db38ce38d69897f16c1c4b93178942915978f935a545e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 May 2024 12:45:44 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Thu, 02 May 2024 12:45:44 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c992d8e7ac430d9dc22cb428287de1b1ad252822c823d4f86975b0ac631fcd`  
		Last Modified: Tue, 14 May 2024 20:25:23 GMT  
		Size: 254.9 MB (254888469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:78763c04f00412fe8c675154a6670113f16c56e28e7a6e8f3ce8c27010fab84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4294eede177445fd63741659c5dfc5bbc3ff5f047ab1d145173683ac76df99`

```dockerfile
```

-	Layers:
	-	`sha256:2dd05fb16e9fa0b2787a6081f837c4f8dbf5cdca6ecd6d1f9cc0ca43976f1c1c`  
		Last Modified: Tue, 14 May 2024 20:25:16 GMT  
		Size: 3.9 MB (3949766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c256b810942a39a26ee3ee249aea7451fc74b3df2eff4678b015d315b96ba70`  
		Last Modified: Tue, 14 May 2024 20:25:15 GMT  
		Size: 11.9 KB (11887 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:e50e5b84dc2dca4f9d876e934bc6fdb265afaa8377b0e21345e361e4f21775b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331830519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde4d49e3645394daa1231a8d08fb3a525aeed96304baa0a7ee2315d2d28cf57`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 May 2024 12:45:44 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Thu, 02 May 2024 12:45:44 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586671c3e1434959c7c01262e28e328c99083d9977f4a0c193b05cbb1ea32ca5`  
		Last Modified: Tue, 14 May 2024 23:42:47 GMT  
		Size: 301.7 MB (301743611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:cc18a2afb6ea7d7df78c77bba1c67acf7c0584ef3d0bd7d90035742f35ad97ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0c7eb0f51b7b4b192c209e8836dbec7194e5654ad15618e1b12a35fc75d2ba`

```dockerfile
```

-	Layers:
	-	`sha256:4d4f0be13aeae74239e4e28da688c9e761df4cf57500b2c65c12e0a5ba9cf97f`  
		Last Modified: Tue, 14 May 2024 23:42:34 GMT  
		Size: 4.1 MB (4136723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d39995db708f64967cae1e603b98f4a01b415da65df7e9947f7fd97c61781679`  
		Last Modified: Tue, 14 May 2024 23:42:34 GMT  
		Size: 11.8 KB (11827 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:829633d7c81f669692cd636273cbe9e1fe74e53dd0406e05041cc2fe4df67b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283596999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049450e6965f7225e4b3142ae1506ed507a6e0129f20961a5ef3c8a3387a5929`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 May 2024 12:45:44 GMT
ADD file:8cc17bd8431911317f7d91df00ff305ed2f31f83f3224da64f6d7b9c38819dae in / 
# Thu, 02 May 2024 12:45:44 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:de7432ff839295b583814dfc21a6afb18eb4e45d8144c26b1402229e5bc8105f`  
		Last Modified: Tue, 14 May 2024 00:52:45 GMT  
		Size: 32.4 MB (32424043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc5eb01e431196b225001c528a99f7bdcedd9ff7604c7d162ef74f3971398d9`  
		Last Modified: Tue, 14 May 2024 01:55:45 GMT  
		Size: 251.2 MB (251172956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b57c6f3f5ea84f5b96a26bc7a075136a1ab51d56ef318eae0c7d742ec16f4637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930b13d7e0a884b8cd1845a7a9ce528396d3c7b2bc8aae6b70d9ff51b69e8d09`

```dockerfile
```

-	Layers:
	-	`sha256:4a13291cc142dd84c549efe8f19a39c3664a60741e92fbd38387a23f1c93453f`  
		Last Modified: Tue, 14 May 2024 01:55:40 GMT  
		Size: 4.1 MB (4131897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39f9a3440b6196cbeed3b4adf9f685b3d4e7c103691e32dbdae3b68a543d74b3`  
		Last Modified: Tue, 14 May 2024 01:55:39 GMT  
		Size: 12.0 KB (11955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:8871027befcd8e0b54582d948b1c4f374c9ec8d850e62e9ddb03571d6d8c6dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277264865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435f2d6678dc6350ea075fe74888dd35530981548a6a9ed0c06c3c0f9692a2e8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 May 2024 12:45:44 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Thu, 02 May 2024 12:45:44 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fce3a86baa2a080573641d659c7f57a2eca4f1992f4c4dad211078c3bec1fb2`  
		Last Modified: Tue, 14 May 2024 16:40:12 GMT  
		Size: 242.0 MB (241953706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:dc3bd83f2352ce767f97aec5261d0237988bab4982ff41971e4793e8482f862a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6c85438d9380bbb482bacf19054e764a34a47796bc0e9e510c0ab1c9cd32e1`

```dockerfile
```

-	Layers:
	-	`sha256:08ad401e301bfe736b322c82ae817bb192100dd712c88e6cf01dfd9b7343da90`  
		Last Modified: Tue, 14 May 2024 16:40:04 GMT  
		Size: 4.1 MB (4100924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d95f7882eb1c64e62c556c006ced21b17de2a0c2da0471c4a0c670fda1ba110`  
		Last Modified: Tue, 14 May 2024 16:40:03 GMT  
		Size: 11.9 KB (11855 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:c15abfc28c3e02a49523ff9c4934ebbe27240edd49a373df4f81613d3170ba67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332289288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543322e79b531e1e9f255ab3d6ee0fe69ef1d8a3806f4ca1aa6d28662d100407`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 May 2024 12:45:44 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
# Thu, 02 May 2024 12:45:44 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee492144331b04cf160aaf3647e3da560e6ba3bed65cc863ad51258e6145c27`  
		Last Modified: Wed, 15 May 2024 00:47:49 GMT  
		Size: 302.6 MB (302615632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:978e77ec1b0cf1bf65c7210b652e8e82945074fc01093474c2545473452c3f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3983864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69219483b4360318e7a13878d4f32dc46d3a82ffcff28caaebfde5c87adcec4d`

```dockerfile
```

-	Layers:
	-	`sha256:654f1637cb4babfc706ebe6d832af7c20599efa994ead8ad0ef08f188956d1ec`  
		Last Modified: Wed, 15 May 2024 00:47:44 GMT  
		Size: 4.0 MB (3972047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc034aff548dd9db93c9cb1155d52f72e92c0ffc361a7780b81c3f46ae2f7ee`  
		Last Modified: Wed, 15 May 2024 00:47:44 GMT  
		Size: 11.8 KB (11817 bytes)  
		MIME: application/vnd.in-toto+json
