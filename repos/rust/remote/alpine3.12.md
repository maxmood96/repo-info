## `rust:alpine3.12`

```console
$ docker pull rust@sha256:8044072bfff5d1f38577ba699a6bce2e19853ccdb89d637ea1b7fa696b0ab0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `rust:alpine3.12` - linux; amd64

```console
$ docker pull rust@sha256:6a45b33a77748a1219fd7d688581c912052ab0fe34cd0ba5c9f56327f2a8fa0c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241549456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ec1a8e454c627d95f67f90c6d7089a81e6225835baf16ad583ef76a18d3b70`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 02:48:17 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Tue, 11 May 2021 00:41:45 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.52.1
# Tue, 11 May 2021 00:42:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='92e38262ebb9440fbdd229618eb85489d2c3d4a74c68b9ef0fdaf200e19521f8' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='4da6988d6bc80de3fa2d239f7de44152c87c257d208562ad9da17065cc08289b' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331f8f29b357e0d718696e6ad746b514af26675acc6b5184af3044d23565ba11`  
		Last Modified: Thu, 15 Apr 2021 02:51:03 GMT  
		Size: 47.6 MB (47613409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8bfbe6da0ccd460bc49d90a15c481b536b5a03750853ddb87331e45827408c`  
		Last Modified: Tue, 11 May 2021 00:47:46 GMT  
		Size: 191.1 MB (191135480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:alpine3.12` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:95972ed263e1c729f978022cbc22dd3cff9e529e3c6cf084dd88a636ee27c895
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232667090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013225ef11aa8181e85e4b63218a74a4d98e643d539cc2007fcfa35df186e860`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 07:21:31 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Tue, 11 May 2021 02:15:19 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.52.1
# Tue, 11 May 2021 02:15:52 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='92e38262ebb9440fbdd229618eb85489d2c3d4a74c68b9ef0fdaf200e19521f8' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='4da6988d6bc80de3fa2d239f7de44152c87c257d208562ad9da17065cc08289b' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e045015ae0dcaaf2f9e957112b46f53ae85311e5ee7be9320bef5938fa2be7`  
		Last Modified: Thu, 15 Apr 2021 07:24:05 GMT  
		Size: 38.6 MB (38561511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf71a8f3f7256674290c5c485ff38bb513ce1f50f255a8a66f6019c6e308981`  
		Last Modified: Tue, 11 May 2021 02:22:40 GMT  
		Size: 191.4 MB (191394885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
