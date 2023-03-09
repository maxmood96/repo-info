## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:47fb4814dc66fd8699bf0d388afd490d427479d478e605a9c7613e5885064a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:045ddf25180ff01bed2f3d1b4100bab7de7c2af6f278e1b3977507f8eeac277d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275241211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b54af0a35fb63267bd0b06f6789abd46a53893717e1e9dbe854c4860d137b59`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:34 GMT
ADD file:0bc0247df62e3a744ac08bfbb0d34f15d08780974abd1b9b4edc50f5419303c2 in / 
# Wed, 01 Mar 2023 04:09:34 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 18:36:58 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.67.1
# Wed, 01 Mar 2023 18:37:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:6ee0625799a8be4868d0da53c697d402a93a94c3641bf4c617c4683a79556b48`  
		Last Modified: Wed, 01 Mar 2023 04:13:43 GMT  
		Size: 29.1 MB (29065281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba6a5c2ec2325d6dc72bb177a585e363802da98b1963e14511001d4a60ccbb6`  
		Last Modified: Wed, 01 Mar 2023 18:42:26 GMT  
		Size: 246.2 MB (246175930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:a836d69087767db5e4e5030245919e5c7c3e51eac7f356cf109b37644ec76f40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284303336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c95900a1f2c32cd10ff1a0b7ac9f3f6f3773aae14563f66d7d242fc28f1fa04`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:37 GMT
ADD file:da7237367d70e2e0e4696d6e836c51b8202738658f0be04093a63639959719aa in / 
# Wed, 01 Mar 2023 01:57:37 GMT
CMD ["bash"]
# Thu, 09 Mar 2023 22:00:58 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.68.0
# Thu, 09 Mar 2023 22:01:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:07ad0b8b2e8b0a3b44e15b147fb1d22e212258fe6cbff7e0fe1b2ef1925403f9`  
		Last Modified: Wed, 01 Mar 2023 02:02:16 GMT  
		Size: 25.7 MB (25674918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d2f70c40ad41e6ecfb4b06738e2f9535b49a9d07a8281e0c49bb800cc3de2b`  
		Last Modified: Thu, 09 Mar 2023 22:08:20 GMT  
		Size: 258.6 MB (258628418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5ebc8c7d56f68f23f2bc488d3b26a1bb9d9c2ca5e2992d9342a04758f66fba22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.1 MB (338108279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc126ea2c850e951a6f8d8b9ea837074639627fd2817c3b75532998544fd670`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:22 GMT
ADD file:db04e40f784b300b80d5d61ca1debab2a46a5fa38cb5e8f9541e0d87089d5076 in / 
# Wed, 01 Mar 2023 02:20:23 GMT
CMD ["bash"]
# Thu, 09 Mar 2023 21:49:43 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.68.0
# Thu, 09 Mar 2023 21:50:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:b7a2b16a5498b8be22f77c96994969fb75175b766b0be17366f6e1f473240363`  
		Last Modified: Wed, 01 Mar 2023 02:23:39 GMT  
		Size: 29.1 MB (29108415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47f0f5725a4febd2b54e5450fd0e7a50f7fa2222988592afa06fc4dbbbcba1b`  
		Last Modified: Thu, 09 Mar 2023 21:56:24 GMT  
		Size: 309.0 MB (308999864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:ede88db2f7f50b34b2c92a4139c805074bdf1e18e41a9503d2f42fd495945c1b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290067508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab59dec433df51828ae658d7f7bd544a3c3948b73021a8d78f4af80b72efed25`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:38:51 GMT
ADD file:bc9459adea8246d6458b3f6cc20eea8ab9186efb388892e3b42ef19084b34fca in / 
# Wed, 01 Mar 2023 01:38:51 GMT
CMD ["bash"]
# Thu, 09 Mar 2023 21:45:20 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.68.0
# Thu, 09 Mar 2023 21:46:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:61c28ddbda7da8cff9cf0155c9ac5a0ba491864200a5a894207fcff0b665fdea`  
		Last Modified: Wed, 01 Mar 2023 01:43:53 GMT  
		Size: 30.1 MB (30099473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8add919236dc945ca30433affa2b19fad1f1d293dde180b045a8a14e0cb76fea`  
		Last Modified: Thu, 09 Mar 2023 21:53:23 GMT  
		Size: 260.0 MB (259968035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
