## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:94b8825ddcac835957f623577a5ec0aeefb9012655f4920edc323640e5555620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:b324bc103b15141293bdc79a4284f5cb1f1b2844825abf5aead34b5bd61fdff9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246713443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e90fa06329d29506d096835c7b5255395456fb706528abe45ef25989f03421`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Jul 2024 21:19:52 GMT
COPY dir:15f372c0d55f5152b222fa508a1a8c382d0621d72fdef0d2b746557a14bc0dd9 in / 
# Thu, 18 Jul 2024 21:19:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 21:36:25 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 18 Jul 2024 21:36:26 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 18 Jul 2024 21:38:05 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 18 Jul 2024 21:38:05 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 18 Jul 2024 21:38:05 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 18 Jul 2024 21:38:05 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 18 Jul 2024 21:38:05 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 18 Jul 2024 21:38:05 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 18 Jul 2024 21:38:41 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:1e5e0347739e5468c65eed56d50fba90128674d8aae6fa196a8c01eeea145da9`  
		Last Modified: Thu, 18 Jul 2024 21:20:18 GMT  
		Size: 62.6 MB (62647926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0104d1eba4aa981334afa15495e3e68aea2250321195169d2615f04b4b4b8b0`  
		Last Modified: Thu, 18 Jul 2024 21:52:08 GMT  
		Size: 184.1 MB (184065517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:96527ff1b1dec9286c766e04411ec1e17367bd59062c03d4b80b759b1a76ef85
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.0 MB (223959123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca3dda0e3e04ea11f65707c0d857bef3d6c65cb6dd405080db102c9985f4b7e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Jul 2024 21:39:44 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Thu, 18 Jul 2024 21:39:45 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 21:55:41 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 18 Jul 2024 21:55:41 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 18 Jul 2024 21:57:19 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 18 Jul 2024 21:57:19 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 18 Jul 2024 21:57:19 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 18 Jul 2024 21:57:19 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 18 Jul 2024 21:57:20 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 18 Jul 2024 21:57:20 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 18 Jul 2024 21:57:57 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d7c7acbfc600c247c4661c437f1db50a0a22553f25fa5c150a260a2fadde03`  
		Last Modified: Thu, 18 Jul 2024 22:07:37 GMT  
		Size: 159.4 MB (159383812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
