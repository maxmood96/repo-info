## `rust:alpine`

```console
$ docker pull rust@sha256:b27b56f077b159cf23ae75e96d10269c1bc8f8b7cadcd11ed47661ccf882b6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:17c40510db4c8eb5b80f8543f10bac3676e4e2e5e3dcf091ce04952c53e987f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258407826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1178cc15e653de052bdd29e5114d0e009ed8e0902eb2f3cb58309f069c5f6a22`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 02:49:01 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 17 Jun 2021 23:25:23 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.53.0
# Thu, 17 Jun 2021 23:25:43 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='bdf022eb7cba403d0285bb62cbc47211f610caec24589a72af70e1e900663be9' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='89ce657fe41e83186f5a6cdca4e0fd40edab4fd41b0f9161ac6241d49fbdbbbe' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.3/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0be8eca5527a01ceab7f038cf1613c804e74597a07cde2e89d3c7bb2bc3d952`  
		Last Modified: Thu, 15 Apr 2021 02:52:05 GMT  
		Size: 42.2 MB (42173846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c22c6ce94671cbed201daa9a5b2041d8af4105ae5fab8f026f39b827c404749`  
		Last Modified: Thu, 17 Jun 2021 23:30:50 GMT  
		Size: 213.4 MB (213422011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a3244c5ba0262412c8d169085393dbbe7497dbe2574d4fa2d25bb0c8f2d4d176
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268628935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27af3127cd79adf52241e9124e30b6b3058232120623eed55a0119096851d522`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jun 2021 21:44:56 GMT
ADD file:6797caacbfe41bfe44000b39ed017016c6fcc492b3d6557cdaba88536df6c876 in / 
# Tue, 15 Jun 2021 21:44:56 GMT
CMD ["/bin/sh"]
# Thu, 29 Jul 2021 22:32:45 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Thu, 29 Jul 2021 22:32:45 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.54.0
# Thu, 29 Jul 2021 22:33:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='bdf022eb7cba403d0285bb62cbc47211f610caec24589a72af70e1e900663be9' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='89ce657fe41e83186f5a6cdca4e0fd40edab4fd41b0f9161ac6241d49fbdbbbe' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.3/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:58ab47519297212468320b23b8100fc1b2b96e8d342040806ae509a778a0a07a`  
		Last Modified: Tue, 15 Jun 2021 21:46:03 GMT  
		Size: 2.7 MB (2709626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad37cd6caf86daf731832e8beca9a5c2d46313bbf9e1e74bcd3358c95b678585`  
		Last Modified: Thu, 29 Jul 2021 22:39:47 GMT  
		Size: 35.9 MB (35936460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a68d0ab645511794c3d7c96744470202d0fba02d58d82c6ee702feb83fe115`  
		Last Modified: Thu, 29 Jul 2021 22:40:15 GMT  
		Size: 230.0 MB (229982849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
