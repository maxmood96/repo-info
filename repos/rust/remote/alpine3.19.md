## `rust:alpine3.19`

```console
$ docker pull rust@sha256:b5773467f5a74c7151c9f49463678327f28834f7500d5b3b22522fe76d3046d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:9af4ed962405e24b37240ce34a2272e40cff99b4f5150cc6a53b03f95d40e6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275635894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0d56f91c538a0ed2c771f2f7cc3572c8b4bc10401d094983da43814b5fde3d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Dec 2023 16:57:32 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Thu, 28 Dec 2023 16:57:32 GMT
CMD ["/bin/sh"]
# Thu, 28 Dec 2023 16:57:32 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Dec 2023 16:57:32 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.75.0
# Thu, 28 Dec 2023 16:57:32 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bee9a3318268c539b5c897260eca6e5a5763f74b9ce4bf5aae4696e6fea0654`  
		Last Modified: Sat, 27 Jan 2024 00:54:43 GMT  
		Size: 55.3 MB (55338149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffe342ed7260b95666c165ad4e54762468867e4df5879e5fdc34e67cf45212d`  
		Last Modified: Sat, 27 Jan 2024 00:54:45 GMT  
		Size: 216.9 MB (216889016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:d9ddd8dea573e27360b427860d44318db71c8669321a64009a8eb8ddf4fa99a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.7 KB (608685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dea64e1ec279fab113b2f68f738aaf32f6548c416e2650e07a0cb3f0cc81213`

```dockerfile
```

-	Layers:
	-	`sha256:04c55fba5eeebb0b5ea25c3de41d320e5d9a160750191d854f8a66dde7930392`  
		Last Modified: Sat, 27 Jan 2024 00:54:42 GMT  
		Size: 597.0 KB (596998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a02d5bc50a8b37ffcaa215d510c94da171c0ce2f089a61bb7c5618c9d91f54a7`  
		Last Modified: Sat, 27 Jan 2024 00:54:42 GMT  
		Size: 11.7 KB (11687 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9ac01910bdfbc8691ecde655658dc80cbf5d230318c811674afcb694dd8351f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (284970634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb66f6dc4b2ae18b0fbc01cc17c047ac4dd06d3fc8a8f112c5aa2c088d5ad4c9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 28 Dec 2023 16:57:32 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 28 Dec 2023 16:57:32 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.75.0
# Thu, 28 Dec 2023 16:57:32 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398a117cba8f243a8212efa566d79dfd680896f0215b7a1aafc5fe11b4936c48`  
		Last Modified: Fri, 12 Jan 2024 20:59:01 GMT  
		Size: 53.0 MB (52970308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4fcefdf27eb3113a62dc19f4cae7871500e84233d63c90ed5bf73108337fdf`  
		Last Modified: Fri, 12 Jan 2024 20:59:04 GMT  
		Size: 228.7 MB (228652532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:a93fdc4dbf76f825b07e1a95ca2ca55a6314b9494be9a8dd8614fee43d1fb225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.7 KB (638652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886d34c73f68578c64d50ce734e3f7f2cbd47565808288e663ed205675e02e7d`

```dockerfile
```

-	Layers:
	-	`sha256:59356123c7f5fa5286fc5ce121b399f016fa98f1fa4d31af4b7245f94dad29a7`  
		Last Modified: Fri, 12 Jan 2024 20:58:59 GMT  
		Size: 627.1 KB (627112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d316f8c2df143549fc807a30bb0307a8b4eafe1baedced8e9f785052e8a1170`  
		Last Modified: Fri, 12 Jan 2024 20:58:59 GMT  
		Size: 11.5 KB (11540 bytes)  
		MIME: application/vnd.in-toto+json
