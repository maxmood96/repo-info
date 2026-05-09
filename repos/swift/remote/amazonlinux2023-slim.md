## `swift:amazonlinux2023-slim`

```console
$ docker pull swift@sha256:73add0ded9fb0f3077058072dac1275a549c1f441b2f62eb3831f16966e56b66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2023-slim` - linux; amd64

```console
$ docker pull swift@sha256:2751713e12cb0c470a4c9e13a7a296e8d7af1f6651241ea15fb7e086cdc2f57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251916181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660a509a826bceafc83e38681638055029ea5c95215c609735f4c670623a7204`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:19:48 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 09 May 2026 00:19:48 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 09 May 2026 00:19:48 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Sat, 09 May 2026 00:19:48 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Sat, 09 May 2026 00:19:48 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Sat, 09 May 2026 00:19:48 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Sat, 09 May 2026 00:19:48 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 09 May 2026 00:19:48 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 09 May 2026 00:19:48 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Sat, 09 May 2026 00:20:26 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && dnf -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffa738d0d5ebe1fec47ff91aa15a2183bc9f4dda655de67eb9e0d588d5191b3`  
		Last Modified: Sat, 09 May 2026 00:20:47 GMT  
		Size: 142.5 MB (142517531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53cc13486069d68ea67a4b5c3b73eb21a87de15504cfbe4585003b8f18888413`  
		Last Modified: Sat, 09 May 2026 00:20:45 GMT  
		Size: 54.8 MB (54821846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023-slim` - unknown; unknown

```console
$ docker pull swift@sha256:048070ac16600ae8d74b423554fcf9a1582765001674a66d9bf6ffa2131494aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6465686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c83677d944f297d46e7bae36c07688b7cd6db3d88192d6c5fa1bf71fad0f3b`

```dockerfile
```

-	Layers:
	-	`sha256:a8731d6a9621fcc12b077678d18d263ae974808a82403d945dd894c89b2db147`  
		Last Modified: Sat, 09 May 2026 00:20:43 GMT  
		Size: 6.5 MB (6452556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea14429a94956dba6cb151635a1c637051954f9bbcee2929bfec3fc0b9f075be`  
		Last Modified: Sat, 09 May 2026 00:20:42 GMT  
		Size: 13.1 KB (13130 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2023-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:c3391e6fdde28f4f4aa759ce6959d7e92914dea57ef2120525ae2f4a685e30b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248885564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7491d053272ff11cb18bbf3f4c47393e52c62201fe15e460389803c850829b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:17:35 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 09 May 2026 00:17:35 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 09 May 2026 00:17:35 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Sat, 09 May 2026 00:17:35 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Sat, 09 May 2026 00:17:35 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Sat, 09 May 2026 00:17:35 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Sat, 09 May 2026 00:17:35 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 09 May 2026 00:17:35 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 09 May 2026 00:17:35 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Sat, 09 May 2026 00:18:11 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && dnf -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471e9152a9ee9c55b5599b43189c28ed1ca266915074ab84867f1873cd09be8b`  
		Last Modified: Sat, 09 May 2026 00:18:33 GMT  
		Size: 141.2 MB (141208382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83179cfbc52bc6c55603434629554fba53bad9d68364abc219e793061aba94e9`  
		Last Modified: Sat, 09 May 2026 00:18:31 GMT  
		Size: 54.2 MB (54220207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023-slim` - unknown; unknown

```console
$ docker pull swift@sha256:7d25260f2282506728f7285f8f26e2044327ef0a265b926a146dad90462a1c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6465300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ee5cb51bd81ed1c9f579a2ad73118b7070ec44d81489fc3c49691dc1a16dc8`

```dockerfile
```

-	Layers:
	-	`sha256:1fc91b0924202b0682d02b8add9af25ecba7454a63a629ca1858a5f7d49e40c2`  
		Last Modified: Sat, 09 May 2026 00:18:29 GMT  
		Size: 6.5 MB (6452063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b8adc8450942aa831675f775a222ad02e8d7f41de7b902a1dd6a17d487c78e7`  
		Last Modified: Sat, 09 May 2026 00:18:29 GMT  
		Size: 13.2 KB (13237 bytes)  
		MIME: application/vnd.in-toto+json
