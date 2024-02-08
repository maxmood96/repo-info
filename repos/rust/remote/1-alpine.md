## `rust:1-alpine`

```console
$ docker pull rust@sha256:def35884ff7e1e4b0eae050cbb03ca0900d70d1acbcba1d0e428147ab6786de2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:ec93a9ad3065df593645171a3aa6c47b55578914d2c232860260dbd27bb0cbc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278095626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e2cbd44af8ead94c9de664c90a8cc1abc37142bda38316576558aa0705fbc5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 14:18:11 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Feb 2024 14:18:11 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Thu, 08 Feb 2024 14:18:11 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217efed5d87065eb443c4022186904bd723ac2d26a0f3142b6520b8b9ebba009`  
		Last Modified: Thu, 08 Feb 2024 18:51:06 GMT  
		Size: 55.3 MB (55338075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba7290e92cbede1611e264b6b16eaf3f28794d0864757e5f38ac258fbe7eafc`  
		Last Modified: Thu, 08 Feb 2024 18:51:10 GMT  
		Size: 219.3 MB (219348822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:9ebca91d29a8c7be8c131456246b8d32ec9cc79f761da306e1e9ea527bb79c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.7 KB (608686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981f763cf55544b4b408f1249694b4cf783bb01960674f36a1358f1798206346`

```dockerfile
```

-	Layers:
	-	`sha256:bcb6a54ac3d25a101904e414c13ef2bcfb524907195346a1bcec37c0e2cc5f0d`  
		Last Modified: Thu, 08 Feb 2024 18:51:05 GMT  
		Size: 597.0 KB (596998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47fbda4c54b770842a83bfbac04fe33f1a614b988922fa90e56e469c6d3f64ea`  
		Last Modified: Thu, 08 Feb 2024 18:51:04 GMT  
		Size: 11.7 KB (11688 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1aecf820154a8492d80130b0903065ddff8a429bcb3a983d153486140b156f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286168115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306cbf4029cddcfb1662dcf91cc8f2000611fbd34206a486b3cc332eecc46738`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 14:18:11 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 08 Feb 2024 14:18:11 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.76.0
# Thu, 08 Feb 2024 14:18:11 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd488a9d559b139f8065681a19588c98216ec62e3492eec70f25a04fc6680d70`  
		Last Modified: Thu, 08 Feb 2024 19:37:43 GMT  
		Size: 53.0 MB (52970338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a10c0f0ac4a8946f06f46f2197cfcc2fcfc3fcf13d5a02006c9e3f708c38f2`  
		Last Modified: Thu, 08 Feb 2024 19:37:46 GMT  
		Size: 229.9 MB (229850062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:9f5e5f5157650561ad79f32061eaf18e49bce05f8af9bc1219ae16166946df84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.7 KB (638658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8149d02aafedefb3318bdfbf7635fb9d978b0250a34a2236acc78aa86dbc9e88`

```dockerfile
```

-	Layers:
	-	`sha256:d24e0d3fe64ae06ebd87aee62e7baec04a705ed9d84a97e737433212043dc49c`  
		Last Modified: Thu, 08 Feb 2024 19:37:42 GMT  
		Size: 627.1 KB (627118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff7bb8b629502dee016612b93bb6d20bc28ff96dfe68c65e1d68b9236d43414c`  
		Last Modified: Thu, 08 Feb 2024 19:37:41 GMT  
		Size: 11.5 KB (11540 bytes)  
		MIME: application/vnd.in-toto+json
