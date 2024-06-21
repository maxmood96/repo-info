## `rust:alpine3.19`

```console
$ docker pull rust@sha256:987333dba5b5e5cc845194a8818b9bebb8a2513f0c5447ef077499bc50636caf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:2eefd0cf36303166a1a42a6e9e1c3b76f645cfa59b44e7acadb78034408bb0f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (277961489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c33aaa0820dd0be424e6faa6a817372de5fd4b20135d0ff566ffc665427b603`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 13 Jun 2024 14:36:52 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 13 Jun 2024 14:36:52 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bda3f2636ac42feb41df00f5fab377b3b95ea1d5dfaab08ead20507d2c1417f`  
		Last Modified: Thu, 20 Jun 2024 20:57:20 GMT  
		Size: 55.3 MB (55346825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70de78e86496a1081e36777bc38f488a6bcd05381f71dc063fc01ddcbdcc5ae0`  
		Last Modified: Thu, 20 Jun 2024 20:57:24 GMT  
		Size: 219.2 MB (219197332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:7a59723872a56d1f935646a22eac11883ccd53f38980f8b3221b1878d9749733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.0 KB (718951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5da31c6ec031a070bc2d5057a815be5c38948d4773d4f52731a68ffc83e1ed`

```dockerfile
```

-	Layers:
	-	`sha256:2e021acfb7db3de15879602f17aed65273ef09f3d135999d9d9996a632a579d3`  
		Last Modified: Thu, 20 Jun 2024 20:57:18 GMT  
		Size: 708.5 KB (708476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a00f6d025f8951da81e735105a47d18494fa10486d90f4b84ed3901d243877`  
		Last Modified: Thu, 20 Jun 2024 20:57:18 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:06fa379e5fd40ecaa4441210078938c2cf81cc97f35335c78a79eca07bbd2def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283432030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39be765ea23b3a9be3e8b9c0d8908983e7b251a7fa4e224ee6422dfee8a9367a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 13 Jun 2024 14:36:52 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 13 Jun 2024 14:36:52 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 13 Jun 2024 14:36:52 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.79.0
# Thu, 13 Jun 2024 14:36:52 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627ade2ee15c5e4f2d325fe7691878559de2fe1dd2b30c21353acde7fd039504`  
		Last Modified: Fri, 14 Jun 2024 04:27:07 GMT  
		Size: 53.0 MB (52995425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85c208cca21d34be42f891bad0161a7edf96bc8bc82b9afad76ea19ff7ccc0b`  
		Last Modified: Fri, 14 Jun 2024 04:27:11 GMT  
		Size: 227.1 MB (227088890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:91025fd4883f59fc0e56bb83d31404d017c617332a236b4d5475cdfb0c15e1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **756.2 KB (756178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67f4198bcdd2684ed4754d2446d5e5ce89b2e8a8e8038ebfa1e472d167b0294`

```dockerfile
```

-	Layers:
	-	`sha256:34ae58cd819b1d4211d149f53f33ac6c6a5812a12c2d26dee4010cbf43122121`  
		Last Modified: Fri, 14 Jun 2024 04:27:06 GMT  
		Size: 745.4 KB (745403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16e2fa7af366029b87aadc8def547a086b2817767de27a49c706cb9bfa347bc7`  
		Last Modified: Fri, 14 Jun 2024 04:27:05 GMT  
		Size: 10.8 KB (10775 bytes)  
		MIME: application/vnd.in-toto+json
