## `swift:slim`

```console
$ docker pull swift@sha256:1d2b7c9e9956b5ebea8bf1c3c21cbdeff3a5ad34856c51daad0758e73ae8ad0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:slim` - linux; amd64

```console
$ docker pull swift@sha256:cbd7ff8dd8c1436d97d7617c89caee5b535bd408d8d5d72c0b5f7a99cc9bf7c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113325881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa83638093052d81505fef76462c4245e7ff5bfae308895f83ac6b6ad1285cc5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Oct 2024 18:01:55 GMT
ARG RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Oct 2024 18:01:55 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Mon, 28 Oct 2024 18:01:55 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Oct 2024 18:01:55 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_BRANCH=swift-6.0.2-release
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_VERSION=swift-6.0.2-RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab657320931b9c48b888dbfdd5bca900aa067ac4cf050dc6ffebcff980fc25dd`  
		Last Modified: Tue, 03 Dec 2024 02:37:46 GMT  
		Size: 20.0 MB (20014680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f06660758714cb3f79d5a111a49a60b3ebab46f0ab1e6eaafe9585989824051`  
		Last Modified: Tue, 03 Dec 2024 02:37:46 GMT  
		Size: 63.6 MB (63559233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:slim` - unknown; unknown

```console
$ docker pull swift@sha256:0b873dd199c84b6b2b3cb00d65209fe854dfe7d1a65b959313797a0705f45536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2389602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfcc4dd05a23fd5c19d38c960b0fb2fb2407d320301deeda5f8f4021cb4fa2e`

```dockerfile
```

-	Layers:
	-	`sha256:d7db558ac431a6144df5ac7c578454c64a1b5d6964ca7a7ce07d179ed0997d0d`  
		Last Modified: Tue, 03 Dec 2024 02:37:46 GMT  
		Size: 2.4 MB (2374722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6179e2b7c5f1bfbfb3a4a823c687d382b5c4076e737f099f5b50c98728b8cdd7`  
		Last Modified: Tue, 03 Dec 2024 02:37:45 GMT  
		Size: 14.9 KB (14880 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:795c15e66f66139ddd5bd75fd3a591767a7f8886867f23af582f41ea463526d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112174360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a71de4189cc6e8ecb11f77cdcc21bac959061d771394563eb0a0b814e59908`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Oct 2024 18:01:55 GMT
ARG RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Oct 2024 18:01:55 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Mon, 28 Oct 2024 18:01:55 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Oct 2024 18:01:55 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_BRANCH=swift-6.0.2-release
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_VERSION=swift-6.0.2-RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1553a3e1eccf67903996048d391ab6bdd9c733c69ea10c47f7febe8cec6e8680`  
		Last Modified: Tue, 03 Dec 2024 11:02:45 GMT  
		Size: 20.0 MB (20028792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46512453a48ca9218f85f8915cd97f5d4ece7502ef95a40cf1ff09167db0618`  
		Last Modified: Tue, 03 Dec 2024 11:02:46 GMT  
		Size: 63.3 MB (63252897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:slim` - unknown; unknown

```console
$ docker pull swift@sha256:38ab4834429f87d838f51089c850978b31119e823bac2014e17447abdb883d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2390862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc55d4a9bf61dd6ce39599cfa7244c016caab69a7e33f74c48d74dd7e2ab37e`

```dockerfile
```

-	Layers:
	-	`sha256:cb8dc2c2ac02fce50ba0f257bed33633994d1ac8e7ae0bd3cded34f086d61b16`  
		Last Modified: Tue, 03 Dec 2024 11:02:44 GMT  
		Size: 2.4 MB (2375838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56e118170ede1ea2a8e4200847cb65e010d10f3e4f35aca020f58d9c8702225c`  
		Last Modified: Tue, 03 Dec 2024 11:02:44 GMT  
		Size: 15.0 KB (15024 bytes)  
		MIME: application/vnd.in-toto+json
