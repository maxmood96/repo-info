## `swift:bookworm-slim`

```console
$ docker pull swift@sha256:eddd42860b29830a5c7c63726022951d47e207dd520bd89706732fbc47e261a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm-slim` - linux; amd64

```console
$ docker pull swift@sha256:9e1d8c43334f253dcaeb9d84014a472b84379c5c1b7eebd606e513b13ad4a567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123410024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea070f8fa3c7e6c2d3bb1cba5b36c86364babb9bee78e7c2102874267e1e14bf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:13:47 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 11 Jun 2026 01:13:47 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 11 Jun 2026 01:13:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:13:47 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 11 Jun 2026 01:13:47 GMT
ARG SWIFT_PLATFORM=debian12
# Thu, 11 Jun 2026 01:13:47 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Thu, 11 Jun 2026 01:13:47 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Thu, 11 Jun 2026 01:13:47 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 11 Jun 2026 01:13:47 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 11 Jun 2026 01:14:20 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27d24060918b9cb40fcf071814b7d5daa3e9dd6c94cd7c20c633ab4ca6af0a7`  
		Last Modified: Thu, 11 Jun 2026 01:14:34 GMT  
		Size: 23.6 MB (23647415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ba700a70537e6f6a1bcfa86ccf1c6389bd60a4457773d972ba6fe82cb5cfbd`  
		Last Modified: Thu, 11 Jun 2026 01:14:35 GMT  
		Size: 51.3 MB (51260567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:1f362823b0c82d31dc38dcd0ad15817f9f06a8dfe87207a61ae440ec92267864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4429880ced3da538a6fa0a20c4b0a34d0899cd56e66c7b3eef5fbe125f3d2c2`

```dockerfile
```

-	Layers:
	-	`sha256:6674f41d767c5f8ee810448fe93243768611856cad5a5adf102a9f6c2635519c`  
		Last Modified: Thu, 11 Jun 2026 01:14:33 GMT  
		Size: 4.2 MB (4157008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46f8db40c73406d81028c697fe0f2e8f79547b41d1e0ad0421c218e53adaf91b`  
		Last Modified: Thu, 11 Jun 2026 01:14:33 GMT  
		Size: 13.9 KB (13926 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:2c595c3ca60b97f0cfe50865d32c9234ad479e4b3a2a409ac4df547fb79689fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122399868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5b8dabe18f1afb4ad1e48a29ed48210c4f7759297c14282194b9618aa54166`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:17:56 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 11 Jun 2026 01:17:56 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 11 Jun 2026 01:17:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:17:56 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 11 Jun 2026 01:17:56 GMT
ARG SWIFT_PLATFORM=debian12
# Thu, 11 Jun 2026 01:17:56 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Thu, 11 Jun 2026 01:17:56 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Thu, 11 Jun 2026 01:17:56 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 11 Jun 2026 01:17:56 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 11 Jun 2026 01:18:43 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80fc456157216a381e41e330a3d25ea8ce782821d286b9510d9b48397d6b33a`  
		Last Modified: Thu, 11 Jun 2026 01:19:00 GMT  
		Size: 23.5 MB (23464422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f896a50ca984099c38fc9a420078590cb5e58baf1dc915309698eb0f4e3baf6c`  
		Last Modified: Thu, 11 Jun 2026 01:19:02 GMT  
		Size: 50.5 MB (50546430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:c1ad337acd200f0b4302978290356e3f01864e3067d03a3d700d7ba1b473c627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e589f345c9966c7dff51fa281f7d2ea235dec546252047b82a89f6274604a9`

```dockerfile
```

-	Layers:
	-	`sha256:ba03f5ad2005c7df9ab88f92cff50e7b5bc331955061261b645476e4509f19db`  
		Last Modified: Thu, 11 Jun 2026 01:18:59 GMT  
		Size: 4.2 MB (4157285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:770dfb02661869120f76ede6e709b1c65b2ee480439064b8a122c38f1b22cc5e`  
		Last Modified: Thu, 11 Jun 2026 01:18:59 GMT  
		Size: 14.0 KB (14033 bytes)  
		MIME: application/vnd.in-toto+json
