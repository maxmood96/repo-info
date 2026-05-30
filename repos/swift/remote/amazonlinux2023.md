## `swift:amazonlinux2023`

```console
$ docker pull swift@sha256:eaebcbb1333d5353ccaec48a23fdc22caaabac6addffcef475c5cd911e806664
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2023` - linux; amd64

```console
$ docker pull swift@sha256:8f1dc4fdd5c999eaf0984ac9c36ebf3af594c701d55bb69d6a90979094279288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1475580816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1fc0ebbcb73b2da03a96b039e76aa6d00dee0bad5bfefa82cc462cc328d70a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:26:56 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:26:56 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:13:38 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 30 May 2026 01:13:38 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 30 May 2026 01:13:38 GMT
RUN dnf -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata # buildkit
# Sat, 30 May 2026 01:13:41 GMT
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Sat, 30 May 2026 01:13:41 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Sat, 30 May 2026 01:13:41 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Sat, 30 May 2026 01:13:41 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Sat, 30 May 2026 01:13:41 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Sat, 30 May 2026 01:13:41 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 30 May 2026 01:13:41 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 30 May 2026 01:14:18 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Sat, 30 May 2026 01:14:18 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3a6cc6c6f9d4fe76a201b0477b62904d76f8d9db646a062b408a4006f7b3c2`  
		Last Modified: Sat, 30 May 2026 01:16:49 GMT  
		Size: 277.8 MB (277816458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e494abbd50ec38d3188a3687d9a0bc0e55015044b5b53bbaa5c077dd9ca8ff8f`  
		Last Modified: Sat, 30 May 2026 01:16:43 GMT  
		Size: 23.8 MB (23796928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7648537195355608e978da07f79a6a83d841d7d41b38e165ca805e4a9e05120b`  
		Last Modified: Wed, 13 May 2026 18:21:41 GMT  
		Size: 1.1 GB (1119396103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12258ca69f8da7b857b9699c97fac234716927b653ec40283799311f463aa18e`  
		Last Modified: Sat, 30 May 2026 01:16:42 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023` - unknown; unknown

```console
$ docker pull swift@sha256:db46f0818ffa2be0d33285684f3d64bcad75076d84353a241ba195bf6cee8643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13808168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef609ad281b9d5f876d91d68de3425ec3c6a416a9b0b9ce46a992855939308cb`

```dockerfile
```

-	Layers:
	-	`sha256:c25ddb8979074c412770b1d52442ab7e492cace0197d970418fd10855c9821e4`  
		Last Modified: Sat, 30 May 2026 01:16:42 GMT  
		Size: 13.8 MB (13791941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df80cf3040770f836ba607ffc356f54361383cb08873e72d49b1239f93192a8a`  
		Last Modified: Sat, 30 May 2026 01:16:41 GMT  
		Size: 16.2 KB (16227 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2023` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:ff3d37c34ebc0f8a17505bb864347f8fbd42ea6f2a8bd05973020e32c6431b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1457610484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9387d885a5f418332f0c7a9014329bceef75bc4dd56cf01d47f54236ff0bf382`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:13:28 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 30 May 2026 01:13:28 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 30 May 2026 01:13:28 GMT
RUN dnf -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata # buildkit
# Sat, 30 May 2026 01:13:31 GMT
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Sat, 30 May 2026 01:13:31 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Sat, 30 May 2026 01:13:31 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Sat, 30 May 2026 01:13:31 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Sat, 30 May 2026 01:13:31 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Sat, 30 May 2026 01:13:31 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 30 May 2026 01:13:31 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 30 May 2026 01:14:08 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Sat, 30 May 2026 01:14:08 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd112dbec6ce2f7ce8134d46c47b2b0e8e3e7c202c27775358149a49a399b97`  
		Last Modified: Sat, 30 May 2026 01:16:38 GMT  
		Size: 269.3 MB (269289950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff3492bd076279a3c15a504db95d031361a3597d7a5786f772b33f53b2dc1fe`  
		Last Modified: Sat, 30 May 2026 01:16:33 GMT  
		Size: 23.4 MB (23441107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732e2f8c819c0db9ad335e0ab6fd5c6681e1b0183481e5d714d48b72e8537ba4`  
		Last Modified: Wed, 13 May 2026 18:08:33 GMT  
		Size: 1.1 GB (1111421425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61409965ae3b0bc01c5aef027b7ff89c5db92827e1ae27a9a218c98b943e5d3`  
		Last Modified: Sat, 30 May 2026 01:16:31 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023` - unknown; unknown

```console
$ docker pull swift@sha256:1f383f57105f28a0fafed81cb518a86b9242860248773f9de85686856eea354d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13678358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63871171c03a0a7dece6a45bab3e4f44552c3d8806a0dfdff399e76f498f3c17`

```dockerfile
```

-	Layers:
	-	`sha256:079846f8989357a9ff3625de50d972d1706dbb2afd7d61f8708979aa40a7f6ea`  
		Last Modified: Sat, 30 May 2026 01:16:32 GMT  
		Size: 13.7 MB (13661994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0858415457ab9f2b7e85e632c00aedabd5abae28bb4c718ba02473f2d511e26`  
		Last Modified: Sat, 30 May 2026 01:16:31 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json
