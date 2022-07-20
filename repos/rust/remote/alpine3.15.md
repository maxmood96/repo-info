## `rust:alpine3.15`

```console
$ docker pull rust@sha256:94c8257e384b0a5adaaea87935f2cdbeac321433395858899d21ed56a9065bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `rust:alpine3.15` - linux; amd64

```console
$ docker pull rust@sha256:51fb27d7b3fd0e56d83fd9c6e512781f373787e07ca2bb4cc5f4d9b07a51cabf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 MB (245237239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a2037652ab1df6aa9e70679bf575251323711b8fc2a34ce266149f58e05410`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 02:00:44 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Wed, 20 Jul 2022 02:00:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.62.1
# Wed, 20 Jul 2022 02:01:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='bdf022eb7cba403d0285bb62cbc47211f610caec24589a72af70e1e900663be9' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='89ce657fe41e83186f5a6cdca4e0fd40edab4fd41b0f9161ac6241d49fbdbbbe' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.3/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931c0442ee528559ad9816e61973c24388cb67024a3a594ffe632c29de699ea9`  
		Last Modified: Wed, 20 Jul 2022 02:01:59 GMT  
		Size: 42.5 MB (42476673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0eb914ff77a03dc6ca6a5f047a5e713c56bd7cca4e713c7bf9c447a38cc7c38`  
		Last Modified: Wed, 20 Jul 2022 02:02:22 GMT  
		Size: 199.9 MB (199945921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rust:alpine3.15` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:e3ef9c0e5e8e3d42897e294d94f8f94d8bbb8433018cb86117ca4060fd37bfef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243225288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c48f8136dda39f04567a6f04a5ed96eb0a6eb8d3fae31ca168d7e1d46170c7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:36 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Tue, 19 Jul 2022 17:15:04 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.62.1
# Tue, 19 Jul 2022 17:15:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='bdf022eb7cba403d0285bb62cbc47211f610caec24589a72af70e1e900663be9' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='89ce657fe41e83186f5a6cdca4e0fd40edab4fd41b0f9161ac6241d49fbdbbbe' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.24.3/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c79c9d0c9a2cc2bdae9476b20ddb336848888d44ff7d5dfb719ff227ffb79c4`  
		Last Modified: Tue, 05 Apr 2022 07:21:11 GMT  
		Size: 36.1 MB (36073695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352eb29472eb237963a375fb79b261c79410ed4e54e5867eea380735eb7fc0e3`  
		Last Modified: Tue, 19 Jul 2022 17:21:27 GMT  
		Size: 204.4 MB (204435116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
