## `swift:amazonlinux2023`

```console
$ docker pull swift@sha256:3468c2017209a8e09530ba182e9db3b3f86671b67aa578584662520bdf87b3cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2023` - linux; amd64

```console
$ docker pull swift@sha256:024a040c2ccb49b7b2c3af34d9338772f0840ebff5f19abf275cdba82a6e5aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1468712268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076895d8fb14a6258a4ce3143796026f04933da1f424f2ea1cac6fff4e97ed82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:13:47 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 04 May 2026 20:13:47 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 04 May 2026 20:13:47 GMT
RUN dnf -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata # buildkit
# Mon, 04 May 2026 20:13:50 GMT
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Mon, 04 May 2026 20:13:50 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 04 May 2026 20:13:50 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Mon, 04 May 2026 20:13:50 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Mon, 04 May 2026 20:13:50 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Mon, 04 May 2026 20:13:50 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 04 May 2026 20:13:50 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 04 May 2026 20:14:31 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 04 May 2026 20:14:31 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95317a59b8f1fde9cc21baec9dbbebba1d6e5da377b5479b17722422c5f94b8a`  
		Last Modified: Mon, 04 May 2026 20:16:51 GMT  
		Size: 270.8 MB (270788613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b277bdf7e47b51df22a8c4cfe2d41d5cd8c894a845055093070579324cb7f25a`  
		Last Modified: Mon, 04 May 2026 20:16:47 GMT  
		Size: 23.8 MB (23799080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509f13cc778a767668a55d9c211eea58182be256f51344c23464ebb3329f2d7c`  
		Last Modified: Mon, 20 Apr 2026 21:56:08 GMT  
		Size: 1.1 GB (1119547649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5b63eea31c0b603ac49c68980f1e882e35482be0c431c698be14656716d7fa`  
		Last Modified: Mon, 04 May 2026 20:16:46 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023` - unknown; unknown

```console
$ docker pull swift@sha256:c261e9579aae3735eac554d975c9292917b862fc79eaa94468ad8eb0ca133ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13807386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b513c10fa331486241c4219d6f30f6633621a599bd128beb708ba865910f3f8`

```dockerfile
```

-	Layers:
	-	`sha256:d8b2f6d016411fb45a6fc49fee2e9b41611eb5577bcd2ed0d13df9752d78a789`  
		Last Modified: Mon, 04 May 2026 20:16:47 GMT  
		Size: 13.8 MB (13791159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12259730402e7cb14bfcca19af20052ced997ddad0d866cd35e292eaa4209d12`  
		Last Modified: Mon, 04 May 2026 20:16:46 GMT  
		Size: 16.2 KB (16227 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2023` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:601d78122f2ae4c6367ff072d1aaf329eefb42809151a6a030b19357ac909cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1450802859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2722e578946c07567cf975eaab52a53bda7dd8e16defd2d9dec09630a0efa22`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:13:27 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 04 May 2026 20:13:27 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 04 May 2026 20:13:27 GMT
RUN dnf -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata # buildkit
# Mon, 04 May 2026 20:13:32 GMT
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Mon, 04 May 2026 20:13:32 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 04 May 2026 20:13:32 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Mon, 04 May 2026 20:13:32 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Mon, 04 May 2026 20:13:32 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Mon, 04 May 2026 20:13:32 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 04 May 2026 20:13:32 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 04 May 2026 20:14:09 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 04 May 2026 20:14:09 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5eabb3eaffb84108d696787567d0324df4c4d03bfbb268f87e5374de227752`  
		Last Modified: Mon, 04 May 2026 20:16:35 GMT  
		Size: 262.3 MB (262312918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb095b81e882962cf9cb89a1adc2db64a926fc54c12a22d6ec0ce45a38a2f46`  
		Last Modified: Mon, 04 May 2026 20:16:29 GMT  
		Size: 23.4 MB (23444212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41840fcb6f0f4c207268c52452e608556e0288a5ddad24dae641ee61260665f`  
		Last Modified: Mon, 20 Apr 2026 22:03:50 GMT  
		Size: 1.1 GB (1111588785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa85840cda562d04c16f1b86d77baf81c3e0d736d526e445e0cc88000b69189`  
		Last Modified: Mon, 04 May 2026 20:16:27 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023` - unknown; unknown

```console
$ docker pull swift@sha256:7756458c881cf7f500c95f08fdb5494ddee9fcd72a9dfddc86a5a9ecb3c37faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13677576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c82880f7c94a8f2885da0acf7104350ba65520ea0cd6bf76d55a272b04f957`

```dockerfile
```

-	Layers:
	-	`sha256:ab3f906106fbf67053dd69622d90f08de262eafed111aca113550b563408d203`  
		Last Modified: Mon, 04 May 2026 20:16:28 GMT  
		Size: 13.7 MB (13661212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c366cfa8d4864d5c7c18e581b2c62b20bbd333db73633cad82080fd32c8e61`  
		Last Modified: Mon, 04 May 2026 20:16:28 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json
