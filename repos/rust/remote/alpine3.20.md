## `rust:alpine3.20`

```console
$ docker pull rust@sha256:ef86f37c2819ebd1ecb1dbd7efda70c693cb013232688aa136a5a2f1e3b65e55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `rust:alpine3.20` - linux; amd64

```console
$ docker pull rust@sha256:a97b713ba0b992d4855de682705a1671a9f1bdbf56c63106e3b450732ffd31ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322314091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f5a88bc4032951a2b68c4d0695f33ba0c4d4313454952d17e7a3a403713a51`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a081b9ffe7512b030d0920eb506f7c1bdbd5353c51f1960af8fc4d16a313033`  
		Last Modified: Wed, 08 Oct 2025 23:48:38 GMT  
		Size: 55.3 MB (55309661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483b1a71ca7cafce114e0d2124a2448acddbf1e3eda67dfb387c28d92d6b498c`  
		Last Modified: Wed, 08 Oct 2025 23:49:06 GMT  
		Size: 263.4 MB (263377374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:24e8dd54d6ad7a7e7dbecca0c8c9e83421a68648c336216f8217e666a50ca241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.0 KB (720952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d368e2e22b7effe99b5a2bc6ccace24606c18a48fa7fb0382074f287232c805e`

```dockerfile
```

-	Layers:
	-	`sha256:f7637da0d7c6704319b9717d659cab4afc248751241fd31c1faae5ecfebbb85f`  
		Last Modified: Wed, 08 Oct 2025 23:44:30 GMT  
		Size: 709.9 KB (709860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:686c296cfedd0c7ba040e33922df421ff0eb8f7e42fc4d42dbd32143f0338fd0`  
		Last Modified: Wed, 08 Oct 2025 23:44:30 GMT  
		Size: 11.1 KB (11092 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:44cacafd135db6161d33d79b5e65fbb9375c7bb80c242d07e7c09d112981113f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325626931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d07c7cdf49502e377e4226d37bb1689174bf58c2216080a90efea482747e88f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ff9590a5b60b1e15970e7ac0f37a1e6a85eb616f7d31e8a6045ef19a423947`  
		Last Modified: Wed, 08 Oct 2025 22:08:32 GMT  
		Size: 52.9 MB (52945612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7cff9f5a1f683000cf98855496c2efcfbed8bd539ca0dc203b19637697acfb`  
		Last Modified: Thu, 09 Oct 2025 00:33:09 GMT  
		Size: 268.6 MB (268591942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:31f1257ccf79fbeb2d88ee06899530d562565e104b1fef746fb24eed8bcf9363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.0 KB (757003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:864fe8aca16a5ffc92e0f9568d7086de910e8e228fc016a4aefa3b19d12ef662`

```dockerfile
```

-	Layers:
	-	`sha256:a23ba2d9c570f34d097a32fdeb9f470b023f783f21412f62b312d87d38a399cd`  
		Last Modified: Wed, 08 Oct 2025 23:44:34 GMT  
		Size: 745.8 KB (745792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d149eb4b21c73b2e4630fabe7854f8362c6237e94d34d5ff8c35bbb30c907b7`  
		Last Modified: Wed, 08 Oct 2025 23:44:34 GMT  
		Size: 11.2 KB (11211 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.20` - linux; ppc64le

```console
$ docker pull rust@sha256:323e9bb9f5bdb3e1b11a122014bc05492bc31fc24ad050be8e38a6774662b1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345167925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01759e6bacb31eac791d7252f80007f9302f67878ee1a72bbde55ad9e4a211ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Sep 2025 14:07:21 GMT
ADD alpine-minirootfs-3.20.8-ppc64le.tar.gz / # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
CMD ["/bin/sh"]
# Thu, 18 Sep 2025 14:07:21 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 18 Sep 2025 14:07:21 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 18 Sep 2025 14:07:21 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.90.0
# Thu, 18 Sep 2025 14:07:21 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;;         ppc64le) rustArch='powerpc64le-unknown-linux-musl'; rustupSha256='08423383d36362d93f8d85f208aa5004a7cef77b69b29fb779ba03ed0544e4f1' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.28.2/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:a78577222d4c08b54b062e8bf30834a3c610281d9b4780d34cac9394431f7f25`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 3.6 MB (3575563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3d4fef061972b5a536d5dc27c6e2ec1a6af1868c7a8ed73649e96ef403cc78`  
		Last Modified: Thu, 09 Oct 2025 11:00:09 GMT  
		Size: 54.1 MB (54069626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959cfe92ddb8a18926e7717589b1acaf295e33b15ca60e9c9e7e65a7567b6de`  
		Last Modified: Thu, 09 Oct 2025 11:01:15 GMT  
		Size: 287.5 MB (287522736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.20` - unknown; unknown

```console
$ docker pull rust@sha256:abdc08db7e1da362ae2750b3c87e0e0bf162b47b03ba70929616e05f4660490d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **714.9 KB (714867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9d3a994f7137a606e5fc3bb60732e62b3e11339944cb30264794ee2aff7d0e`

```dockerfile
```

-	Layers:
	-	`sha256:299f111c291c6146617598d78e4abf1162dd1e235a847eeaad20bfeef341b474`  
		Last Modified: Thu, 09 Oct 2025 08:44:30 GMT  
		Size: 703.7 KB (703728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaf82392610784b6dc5a5fc46d0db40e68de482571e5808a27a534fc99f1b32d`  
		Last Modified: Thu, 09 Oct 2025 08:44:31 GMT  
		Size: 11.1 KB (11139 bytes)  
		MIME: application/vnd.in-toto+json
