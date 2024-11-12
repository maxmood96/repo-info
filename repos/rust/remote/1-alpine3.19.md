## `rust:1-alpine3.19`

```console
$ docker pull rust@sha256:fcd6117426b140d94e833c54c6e05612c1fa15d9f065b7ca21f7a266a8327870
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:cd6e942d21a09065bb77508e0652cad35ef32938cee4727f8e00c4ef3ae4f9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291926676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52bab6d057387ec516cb502d1d9be60aaa9ae67f887fa4204ad3778c824deef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7f9aa2a63c77c6dfea9a616ba8de311167963accbb062595e525a14855dd77`  
		Last Modified: Tue, 12 Nov 2024 02:49:15 GMT  
		Size: 55.3 MB (55346808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3e15e1bb1f3d07546e99251b81032a4a9038fadbf9b9ebd27e2afbf930429d`  
		Last Modified: Tue, 12 Nov 2024 02:49:19 GMT  
		Size: 233.2 MB (233160140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:7dbbbafbd89f297fdf36b0e0086b8d676e024539d52d541582c9f41e063ed24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **724.5 KB (724455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8758812fd52c11e30054af7f1f6afd3dc1d32b6bffee934556cc4642587c469e`

```dockerfile
```

-	Layers:
	-	`sha256:30f938cb5f53250c3b423cd92520cd8df1cd4fbbc6f7610f85795ac313fbb787`  
		Last Modified: Tue, 12 Nov 2024 02:49:13 GMT  
		Size: 713.7 KB (713741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ec1f9818cc762ca92550827ee60d791ab5ba54775746c16d27c288d6446876`  
		Last Modified: Tue, 12 Nov 2024 02:49:13 GMT  
		Size: 10.7 KB (10714 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:499c93a743c096822c3ce050e96df3f22ceb5abf517422c3cfc3e34be779b334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298153503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb195d39c948c729c2a621ced30c3cb838d44b72fc12084fe9c364ba5daaf1c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 17:01:39 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 17 Oct 2024 17:01:39 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 17 Oct 2024 17:01:39 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.82.0
# Thu, 17 Oct 2024 17:01:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.1/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832c2f560bcd7cc2071a2ff7b80d28d566d9bc6644db81915a561a051e27d00e`  
		Last Modified: Fri, 18 Oct 2024 00:29:56 GMT  
		Size: 53.0 MB (52995407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e9dcbde1ac8d276d321ba07f80f05e9ffee4fae318dae571a76d7cf5264f3c`  
		Last Modified: Fri, 18 Oct 2024 00:30:00 GMT  
		Size: 241.8 MB (241798993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:985e97b0beed650244a2e606b90ea14955f2e370312715ead82e5c874bb39aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.0 KB (760049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e44d5402fbaee4e101aecb1bf614fdbb58f6c24413a149931fd7cfc97b7621`

```dockerfile
```

-	Layers:
	-	`sha256:7f55f4dc6a64459bf97682966e85d4d3faaa31836315dd9bd160eea17bc2a50f`  
		Last Modified: Fri, 18 Oct 2024 00:29:55 GMT  
		Size: 749.4 KB (749423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8624b8420bd192f3fcc11e096d27439030ddff55ca81b0b89530581ea062c2a9`  
		Last Modified: Fri, 18 Oct 2024 00:29:55 GMT  
		Size: 10.6 KB (10626 bytes)  
		MIME: application/vnd.in-toto+json
