## `rust:1-alpine3.19`

```console
$ docker pull rust@sha256:65aa0b28d02612a3811a7fd0c65b56e4ba766c35cef71965f1cacae7555771a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.19` - linux; amd64

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

### `rust:1-alpine3.19` - unknown; unknown

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

### `rust:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:199ba64543606a62d891c6bc10741d1187b15bd7114112f86d6e03686ff0ee68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (284970624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd96fa376eeb0925be9f58576e1fc85c471ba8d3f5a2eaf7007089f312ff884`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Dec 2023 16:57:32 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
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
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aabc96c6f430bef666524451a6a7b3be61f8660baa0acd535a3d18d56cc9417`  
		Last Modified: Sat, 27 Jan 2024 23:25:53 GMT  
		Size: 53.0 MB (52970331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e79dd15600152a45dbb42332e271b46e4be78bfc5f7836bd6d64c57b4c8576`  
		Last Modified: Sat, 27 Jan 2024 23:25:56 GMT  
		Size: 228.7 MB (228652578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:e62d7f22e5575adb731c01654fd671992f7c194991455cc1a31bd303cb0fb2b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.7 KB (638658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc8c3f38f04fd11cb098dcf0db2c0eb026b79a0832b7fc367eb931ed5290ecc`

```dockerfile
```

-	Layers:
	-	`sha256:4e40d93a37d70065a5290187090a855e3a29835cad39ab583cebf2d8a20c1e6c`  
		Last Modified: Sat, 27 Jan 2024 23:25:51 GMT  
		Size: 627.1 KB (627118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde4a6d0ba804823b8a190494cde6f62234b377c25a3617c4092e4d410a281f5`  
		Last Modified: Sat, 27 Jan 2024 23:25:51 GMT  
		Size: 11.5 KB (11540 bytes)  
		MIME: application/vnd.in-toto+json
