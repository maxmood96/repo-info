## `swift:rhel-ubi9-slim`

```console
$ docker pull swift@sha256:2f1d6c940dc9f1ca5cb9c56d2ac9a37b2f2ee2a7061ba3cae484fabe13de6baa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:rhel-ubi9-slim` - linux; amd64

```console
$ docker pull swift@sha256:693b777577bf96d0427938b5463ef82fcfe31151842f659dbc17900805296d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134552820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a54afc305f74caca5c6b351462ab241f34208a20683b28a54177ca529fc40d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL url="https://www.redhat.com"
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.5"       distribution-scope="public"
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL io.openshift.expose-services=""
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 01 Apr 2025 00:12:10 GMT
ENV container oci
# Tue, 01 Apr 2025 00:12:10 GMT
COPY dir:58f1fd7370bf1be7d595081ce89267556404935630c8266504f6865623b28c9f in / 
# Tue, 01 Apr 2025 00:12:10 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 01 Apr 2025 00:12:10 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 00:12:10 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL "build-date"="2025-05-13T04:57:10" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0d3315aaa0c7b5560abd0b7de30e7d003d748698" "release"="1747112166"
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_BRANCH=swift-6.1-release
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_VERSION=swift-6.1-RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:9ecd6eb4d9863a9e6f886b8bf6ac4ca5da3289365ffaccdcf95d3a78de75aad8`  
		Last Modified: Tue, 13 May 2025 05:40:56 GMT  
		Size: 79.6 MB (79613859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daadbda7b75cf6234a3ac20416cbdfdc328350200a9bd92091b7a7c59a6b03a5`  
		Last Modified: Tue, 13 May 2025 19:55:15 GMT  
		Size: 54.9 MB (54938961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:da20770c07364e6b5de25b6037796d6d2284e024864e1d25751acf64b2c9a50b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6389886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb72908f42a49bd01ef55d958dabd6dc6bbf6b0996b288e8e7390c7a40343bc`

```dockerfile
```

-	Layers:
	-	`sha256:d61e7ce6ee5eaf814b302393852cdbe95189f8c0712434e03c3a7d10d9371b21`  
		Last Modified: Tue, 13 May 2025 19:55:14 GMT  
		Size: 6.4 MB (6378395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32ab8202806d40432c02ec6d26c7c6a0f6f4d62c84890a0416a3dd2526ce2c28`  
		Last Modified: Tue, 13 May 2025 19:55:13 GMT  
		Size: 11.5 KB (11491 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:rhel-ubi9-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:794a09148bc83284dca72914f97c13d2031e9c461833a101754fd20db4801182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131071310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc12b8834fb744d6ba7da825a57755b48b62cdecbe4570fd52daf9f3f302072`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer="Red Hat, Inc."       vendor="Red Hat, Inc."
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL url="https://www.redhat.com"
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL com.redhat.component="ubi9-container"       name="ubi9"       version="9.5"       distribution-scope="public"
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL summary="Provides the latest release of Red Hat Universal Base Image 9."
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL io.k8s.description="The Universal Base Image is designed and engineered to be the base layer for all of your containerized applications, middleware and utilities. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9"
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL io.openshift.expose-services=""
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL io.openshift.tags="base rhel9"
# Tue, 01 Apr 2025 00:12:10 GMT
ENV container oci
# Tue, 01 Apr 2025 00:12:10 GMT
COPY dir:bd057af80b77177e32488d4a9c1e03eec3fc66f6e6013bdff07c26eb0b7e514d in / 
# Tue, 01 Apr 2025 00:12:10 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 01 Apr 2025 00:12:10 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 00:12:10 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL "build-date"="2025-05-13T05:02:19" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0d3315aaa0c7b5560abd0b7de30e7d003d748698" "release"="1747112166"
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_PLATFORM=ubi9
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_BRANCH=swift-6.1-release
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_VERSION=swift-6.1-RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubi9 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:a8496f8c23f8ff4fb8427e3c056159cbcdbfe54f7e65970b7ae4037235801074`  
		Last Modified: Tue, 13 May 2025 06:08:14 GMT  
		Size: 77.4 MB (77395445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7ea946effcaf92c0119dc1fe78231462b2919827265fcd35e2c2526032e57e`  
		Last Modified: Tue, 13 May 2025 20:23:44 GMT  
		Size: 53.7 MB (53675865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:rhel-ubi9-slim` - unknown; unknown

```console
$ docker pull swift@sha256:a285b1a98847c4d0c8e2bf924d4172a86f31aa56f100d6d1b0754274168cdf42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6385775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0441a0be400dca2e90ed6229e6dee6fdc5612b80231854f2e735b4be857daf3`

```dockerfile
```

-	Layers:
	-	`sha256:6613f7478a8d6306c029eab098ef0ff66af2fc003220a47f5ddcc32b68a0670e`  
		Last Modified: Tue, 13 May 2025 20:23:43 GMT  
		Size: 6.4 MB (6374198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:390dc5ea2b523c14e73a36272f1b8916362bf15fa177c84bcd0b343f84a73b3a`  
		Last Modified: Tue, 13 May 2025 20:23:42 GMT  
		Size: 11.6 KB (11577 bytes)  
		MIME: application/vnd.in-toto+json
