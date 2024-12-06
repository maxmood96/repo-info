## `rust:alpine3.21`

```console
$ docker pull rust@sha256:a95131484fc2aae71c04a76b15c31f723447d4ca2b9db9f6871819607d6f3d1a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `rust:alpine3.21` - linux; amd64

```console
$ docker pull rust@sha256:3e8b0e9d4aad767ceaa31e328c5c3a0f6c5995c6a99a39f8d88c991cec8fc121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296401172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a2321d34732ab3b433221f562777a0d6c23fede534f689b9d5b26c2e1d477a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 22:20:09 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 05 Dec 2024 22:20:09 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 05 Dec 2024 22:20:09 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.83.0
# Thu, 05 Dec 2024 22:20:09 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc2fea9d7119845ce1daa03c7e4a48cc033e3cbb3c96820e4795db455788dbf`  
		Last Modified: Fri, 06 Dec 2024 01:28:40 GMT  
		Size: 61.6 MB (61561193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266d44bee3385049ce6053d09f0ebfd171096b92dfed8c0b8a746c294680b4eb`  
		Last Modified: Fri, 06 Dec 2024 01:28:42 GMT  
		Size: 231.2 MB (231195536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.21` - unknown; unknown

```console
$ docker pull rust@sha256:069c6111a36e5e5e3dd3f76286fb551a3089cca99059e98b6f425ab95bca1bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.7 KB (795718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d6d7694a95b36a92a0168223ac6bbdd67c49bd7723b3215c1898922f6f3e10`

```dockerfile
```

-	Layers:
	-	`sha256:b519e2f0285f4fa6d5a519a027494f9bdbace9fb0f0f429667cea4fa336c7c33`  
		Last Modified: Fri, 06 Dec 2024 01:28:39 GMT  
		Size: 783.8 KB (783800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3803d179910ce97b74b86e18cfd422e28248f12af5005003ff37185e6f7ffa4f`  
		Last Modified: Fri, 06 Dec 2024 01:28:39 GMT  
		Size: 11.9 KB (11918 bytes)  
		MIME: application/vnd.in-toto+json
