## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:389d4f077d81efbceac76c40c5567516056f47f42ff2220a8c4f8bbf0fd85f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `rust:1-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:588341651c59060178a81c5de999fe47f2d0db1e55dac0b9ad7cf61ba5e4aae1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.0 MB (277043435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a7ca30ca4abd8b360b737446297c8994d45e3a2c0e6322a2994b1020598dc4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:34 GMT
ADD file:0bc0247df62e3a744ac08bfbb0d34f15d08780974abd1b9b4edc50f5419303c2 in / 
# Wed, 01 Mar 2023 04:09:34 GMT
CMD ["bash"]
# Thu, 09 Mar 2023 22:22:22 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.68.0
# Thu, 09 Mar 2023 22:23:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:6ee0625799a8be4868d0da53c697d402a93a94c3641bf4c617c4683a79556b48`  
		Last Modified: Wed, 01 Mar 2023 04:13:43 GMT  
		Size: 29.1 MB (29065281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dae69b5a25a74818940a09a3e02a5688764625b5d04e029dc11eb3839e18319`  
		Last Modified: Thu, 09 Mar 2023 22:28:50 GMT  
		Size: 248.0 MB (247978154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:367dbf6274c5ee9dc1fc195310d40bc8b65f05cf16cee3833e4dc66f4f98ca51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284301925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f982cbcd4f88b400daf87604aec994bfd666058bfde73017a9524dd073856517`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:13:11 GMT
ADD file:8292555b52d2bb56959d4eb73174e182ce8ae231ddce0385e0177b9f325f774e in / 
# Thu, 23 Mar 2023 01:13:12 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:22:50 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.68.0
# Thu, 23 Mar 2023 12:23:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:df7162aa8cb926599b6249fd43b78b8dbf70d2400e56898782927be1a883817f`  
		Last Modified: Thu, 23 Mar 2023 01:32:46 GMT  
		Size: 25.7 MB (25681928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c19db5a14ce21d196dfbd5d971e339230dd71f9d8953969624651200c3c6f76`  
		Last Modified: Thu, 23 Mar 2023 12:26:23 GMT  
		Size: 258.6 MB (258619997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:10038370479b2acae42576ca5e320e7d1fda37352d20ed6985a8f6226b5ae6e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.1 MB (338131997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba0b289855d9d9c0eeaee33fc8523d388a2c6d2cedc4506fcb752496e8bf449`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:44:55 GMT
ADD file:b3c7cfb1fd031012c20cd6ee37e3c98495a4c4af45480d83b8b16d9a7ba83c70 in / 
# Thu, 23 Mar 2023 00:44:56 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:32:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.68.0
# Thu, 23 Mar 2023 06:32:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='bb31eaf643926b2ee9f4d8d6fc0e2835e03c0a60f34d324048aa194f0b29a71c' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='6626b90205d7fe7058754c8e993b7efd91dedc6833a11a225b296b7c2941194f' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='4ccaa7de6b8be1569f6b764acc28e84f5eca342f5162cd5c810891bff7ed7f74' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='34392b53a25c56435b411d3e575b63aab962034dd1409ba405e708610c829607' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.25.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*;
```

-	Layers:
	-	`sha256:015f7b32198b1c57333fa9e151a0b54ccfe05dfef57e98b87c27d426f134db80`  
		Last Modified: Thu, 23 Mar 2023 00:47:30 GMT  
		Size: 29.1 MB (29117766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd93101bbf65cac74402908362fc8c9ad9cf77c87c59a60506242d9664d64db`  
		Last Modified: Thu, 23 Mar 2023 06:35:36 GMT  
		Size: 309.0 MB (309014231 bytes)  
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
