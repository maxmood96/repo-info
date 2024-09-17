## `swift:jammy-slim`

```console
$ docker pull swift@sha256:24ef6df1df6df40df7cf4d9d2d4697df242ed8a34b4038011c937afa44b63546
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:jammy-slim` - linux; amd64

```console
$ docker pull swift@sha256:9ba71ca0b871a7abfeeaa51695210100b96463dd0767aaa92839a4f7686390a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89299960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6813466e42d65ac036a3f9094f7bfd5b79b35ca8e1bf785f70c25f9c87cc75e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Jun 2024 15:11:32 GMT
ARG RELEASE
# Thu, 06 Jun 2024 15:11:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 06 Jun 2024 15:11:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 06 Jun 2024 15:11:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451ca66bb9911d839feaa57be91d226005d250126bebd9124dd9830c9f1837bd`  
		Last Modified: Tue, 17 Sep 2024 01:00:46 GMT  
		Size: 19.2 MB (19194689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04f48b7a332018a90e0e667ce19e9c8f9a5b98a3bc00313c3d1594747d7755c`  
		Last Modified: Tue, 17 Sep 2024 01:00:45 GMT  
		Size: 40.6 MB (40569583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy-slim` - unknown; unknown

```console
$ docker pull swift@sha256:aa8d1af57cfa56f5a04ed920d4f501b4d8a29bed7967348c74ec0e1e547ca2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af58b80ce23098c17a691c3e7da235cba461ed7ebdccd8611408072e2bbaa08`

```dockerfile
```

-	Layers:
	-	`sha256:bb8d90d55788e52684204d9bd69cbef7f7edd8c16383e4b2107c70803fe0ea5f`  
		Last Modified: Tue, 17 Sep 2024 01:00:44 GMT  
		Size: 2.9 MB (2908598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80fb2c1b6062e56457154a24bdd46def624bad5a733d7d18dcb68a045ccc3324`  
		Last Modified: Tue, 17 Sep 2024 01:00:44 GMT  
		Size: 14.7 KB (14669 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:jammy-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:c3d24f2bcd3676970c12170c8040506c0bfd64291ebca0282823d8a789e5accc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86327777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a119059a5a27293a80860b9b7ce2d0dba4fe9d48d149c8a9ccc341fee4a166`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Jun 2024 15:11:32 GMT
ARG RELEASE
# Thu, 06 Jun 2024 15:11:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 06 Jun 2024 15:11:32 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 06 Jun 2024 15:11:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 06 Jun 2024 15:11:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830fdfe7963b0b410c15aededa7b76f2a4496d5a91d628de4377cd1c5e0a0d7b`  
		Last Modified: Sat, 17 Aug 2024 04:57:12 GMT  
		Size: 19.1 MB (19088551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318c596e056dd9f59be07f25a48943aa09380b5cb65948f84046645ada3725e6`  
		Last Modified: Sat, 17 Aug 2024 04:57:13 GMT  
		Size: 39.9 MB (39880543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy-slim` - unknown; unknown

```console
$ docker pull swift@sha256:a6f47e78d6173f38a881d6633ec205e92605dc5d93a55c8ab95141fcd7e56d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2923914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6712c53ad4f93ca3344a3315b7c5cf9382ae5911d9ff6ac048bac91c72887172`

```dockerfile
```

-	Layers:
	-	`sha256:6695764efa1bdeeb45da62336a3a7eca4165800f8fdb188b650419d112bfb4b8`  
		Last Modified: Sat, 17 Aug 2024 04:57:12 GMT  
		Size: 2.9 MB (2908920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a29aaf4bac514a56170a122cebb0164581feaccdb7741bc708d09084f982ec81`  
		Last Modified: Sat, 17 Aug 2024 04:57:12 GMT  
		Size: 15.0 KB (14994 bytes)  
		MIME: application/vnd.in-toto+json
