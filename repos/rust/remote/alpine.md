## `rust:alpine`

```console
$ docker pull rust@sha256:4a7925c3974fab3fb68b3f4d93d1a4a36cb201f9f87b01014def219b125f1960
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:28686f6f8723dbb3fe75cf802c33f8887901af81bd5b842ad90900edc3974b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272508266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27038750bd432607fed7fe11c41f99325117b88f67de55d6993d0eea6d0a626`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 21 Mar 2024 14:04:03 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 21 Mar 2024 14:04:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.0
# Thu, 21 Mar 2024 14:04:03 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480cf671aba1a13d2302a988d402ddd928172621b44632436fe02fed563679eb`  
		Last Modified: Thu, 21 Mar 2024 18:49:50 GMT  
		Size: 55.3 MB (55346796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ad899dac3f7d454483f7998905320e1834d75ecba0379a2fa35a11b9226dfc`  
		Last Modified: Thu, 21 Mar 2024 18:49:52 GMT  
		Size: 213.8 MB (213752741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:4ae083ca97045d0100e84dcac9bcf285c7f2c171d6019ab3a4a8ceb145208456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.3 KB (722304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a99761605bc307508fb7720de2db00156410dfb7148960906ede70d6a032299`

```dockerfile
```

-	Layers:
	-	`sha256:6655254ffbef32b88b12b36c952595c1a1fc0d427dfcd6f7367a2f42ce523fb7`  
		Last Modified: Thu, 21 Mar 2024 18:49:48 GMT  
		Size: 710.6 KB (710617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c248aea4dfdd5ddbe54c6c445796db4bee6713f6d701f03801b44ab4046bf049`  
		Last Modified: Thu, 21 Mar 2024 18:49:48 GMT  
		Size: 11.7 KB (11687 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:63f1b5ec86360a64d3b73d16ed9cc065bde9494d55f5715b46cd5c332bffa201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278834332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e8d1b334dddf3f047b8f60dd31096a5af6ec15ed9aa1d3a378961a4c9b3773`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 21 Mar 2024 14:04:03 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 21 Mar 2024 14:04:03 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.0
# Thu, 21 Mar 2024 14:04:03 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d651ca114e522c42e6bb17953edf4a18bba82fe2287f93e32f6b3957ff901c2`  
		Last Modified: Sat, 16 Mar 2024 17:12:47 GMT  
		Size: 53.0 MB (52970287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6135fd10d4f7034dd56d4452fc8b35fc0b634aea048deaebaff25511d75c9de`  
		Last Modified: Thu, 21 Mar 2024 19:02:30 GMT  
		Size: 222.5 MB (222516330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:977b242868bc2e735c456ef172bd35dcac79dd7ce11980da8963b1bc23399808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **753.1 KB (753138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95cdc51f230e3926c466de4559ce65bcaf5881164d8e59f515da6d1a09c24dd4`

```dockerfile
```

-	Layers:
	-	`sha256:0a70a07d5009d3a98fb42154cd33cf91b74a6a1b7c21aab89fd680a4552445b0`  
		Last Modified: Thu, 21 Mar 2024 19:02:25 GMT  
		Size: 741.6 KB (741598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f0b5b8ce3af2c884fc7c35bcc91f7a6c59e82bc8729471c888b2276eb92b14`  
		Last Modified: Thu, 21 Mar 2024 19:02:24 GMT  
		Size: 11.5 KB (11540 bytes)  
		MIME: application/vnd.in-toto+json
