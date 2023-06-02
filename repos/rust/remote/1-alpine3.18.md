## `rust:1-alpine3.18`

```console
$ docker pull rust@sha256:5070644f339278f21146d3d1f752a4a5f72d1f56d33d802780d67241e8601cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `rust:1-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:9958c163bc23d9c1c0e99442f529a77e763777229d6978e2b7d34d8cfe0ffff4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274969167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bd2706261780736ce968dd1dc2464afda03ac11247b32216e3d1d68c2b41b3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 19:51:29 GMT
RUN apk add --no-cache         ca-certificates         gcc
# Fri, 02 Jun 2023 19:51:29 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.70.0
# Fri, 02 Jun 2023 19:51:43 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.26.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eec1f40b6fbda823f59ba71ff3f9d2aed6c58b84bab52916d364ed48eff32f5`  
		Last Modified: Fri, 02 Jun 2023 19:57:10 GMT  
		Size: 46.1 MB (46066584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e6908afe9bb4710c6015608da2d9d0447fbb22a30affc79c787e49b9cbda6`  
		Last Modified: Fri, 02 Jun 2023 19:57:28 GMT  
		Size: 225.6 MB (225559735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
