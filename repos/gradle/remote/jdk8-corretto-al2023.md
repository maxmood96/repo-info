## `gradle:jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:a849f238787e130ea14f7170aebbcf0dc8d93a365354185f91e8a980ce2409ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:d74217be50ebb30bc13062a5530e86d3833f27b87b352ad2aa2c933d4136b97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.8 MB (587766696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cc88c5cad33e45b7bde346144ff529abd837cd4407fbfd6670009032f85ee1`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:09 GMT
ARG version=1.8.0_482.b08-1
# Wed, 21 Jan 2026 18:59:09 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 18:59:09 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 26 Jan 2026 19:19:47 GMT
CMD ["gradle"]
# Mon, 26 Jan 2026 19:19:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 26 Jan 2026 19:19:47 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 26 Jan 2026 19:19:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 26 Jan 2026 19:19:47 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 26 Jan 2026 19:19:47 GMT
WORKDIR /home/gradle
# Mon, 26 Jan 2026 19:19:47 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 26 Jan 2026 19:19:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 26 Jan 2026 19:19:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 26 Jan 2026 19:19:49 GMT
USER gradle
# Mon, 26 Jan 2026 19:19:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 26 Jan 2026 19:19:50 GMT
USER root
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:08:12 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4054be9abe76295ab4b3be753153a92dc7373aff9dabca474c7604a429b63c`  
		Last Modified: Wed, 21 Jan 2026 19:00:00 GMT  
		Size: 330.9 MB (330929043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56696cee013977b25d2b7ff2c7450f5930b34fa6d93624eeca724678122c1c38`  
		Last Modified: Mon, 26 Jan 2026 19:20:32 GMT  
		Size: 65.4 MB (65371291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1a6af85300c6a89dcf28911fa8181d65c934cd094a669152a4de9b4cc5f71c`  
		Last Modified: Mon, 26 Jan 2026 19:20:28 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee10ff591b6112602f320b644b19c07121de7edf1a808cab836194cb192d389`  
		Last Modified: Mon, 26 Jan 2026 19:20:34 GMT  
		Size: 137.4 MB (137388269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e514d3c60bb03f834c161d272b255187571a2cf38d07e0ee64acc7024a0537f2`  
		Last Modified: Mon, 26 Jan 2026 19:20:28 GMT  
		Size: 54.9 KB (54910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:2935f07f537c76dd9189676a3f851e0e8a556c4577663af55450b5563651ed11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18175375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641c981e73de90c93caed2cddb4113adaff1bf08b653066405c74c4f46cab2a8`

```dockerfile
```

-	Layers:
	-	`sha256:a9257a25e61587d43ca0a67b53499580064aa22f4c570ad0d6e27237ad54957a`  
		Last Modified: Mon, 26 Jan 2026 19:20:30 GMT  
		Size: 18.2 MB (18153859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1f5044daaa77af913bc40eb9ac7154c1a0aa5011ab4f477e3183395bebf7010`  
		Last Modified: Mon, 26 Jan 2026 19:20:28 GMT  
		Size: 21.5 KB (21516 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:53fa9ec0ba8234aea29d02267d216b48bfa24f2ec167e98eb1a1abc4c0c27c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393830696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d363ad822d06e47118ced5a082d62f8ac4cded7151ae7b8737062565f3c0bede`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:28 GMT
ARG version=1.8.0_482.b08-1
# Wed, 21 Jan 2026 18:59:28 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 18:59:28 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 26 Jan 2026 19:19:34 GMT
CMD ["gradle"]
# Mon, 26 Jan 2026 19:19:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 26 Jan 2026 19:19:34 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 26 Jan 2026 19:19:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 26 Jan 2026 19:19:34 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 26 Jan 2026 19:19:34 GMT
WORKDIR /home/gradle
# Mon, 26 Jan 2026 19:19:34 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 26 Jan 2026 19:19:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 26 Jan 2026 19:19:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 26 Jan 2026 19:19:36 GMT
USER gradle
# Mon, 26 Jan 2026 19:19:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 26 Jan 2026 19:19:37 GMT
USER root
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:25 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e639ecdb26d59a37e73ea4a155c69ad55efad10cc4eec6c6e84f5e19ac8fff`  
		Last Modified: Wed, 21 Jan 2026 18:59:49 GMT  
		Size: 118.0 MB (117961188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d319592e06fa4ab76b0c1d9cfd9e295622c68eb0c16660a148a8a71ad96fc639`  
		Last Modified: Mon, 26 Jan 2026 19:20:13 GMT  
		Size: 85.5 MB (85505667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aee69c939fa98901a4c6ceb396e8e1120a8bccc19bd1297086cf7af5b22ecde`  
		Last Modified: Mon, 26 Jan 2026 19:20:10 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbaefd53832e4519e03a39a18d12bfeef289c819269627b32e1347539eb6f6ec`  
		Last Modified: Mon, 26 Jan 2026 19:20:15 GMT  
		Size: 137.4 MB (137388271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef107e86ed6868409b6d2ca9cdb0b3cd6189fa98212dedd6f6e100fbe0d2347`  
		Last Modified: Mon, 26 Jan 2026 19:20:10 GMT  
		Size: 59.5 KB (59536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:e30fbb299651ea3e339e446313fe54a72fd4782721a53aa2d9bbbd490e00a0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11739760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef236125c2806d2e1809853d4a0e33676d5f85131fa23a9a45ad71f6454593d`

```dockerfile
```

-	Layers:
	-	`sha256:da51b5a7ecf90171df432278370b4a1a1090b1037c1acf33127e437e445b1dfc`  
		Last Modified: Mon, 26 Jan 2026 19:20:11 GMT  
		Size: 11.7 MB (11718047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc0f672fcb949680212209cce47d6922d4a8c31b395ffd4674389acce860315`  
		Last Modified: Mon, 26 Jan 2026 19:20:10 GMT  
		Size: 21.7 KB (21713 bytes)  
		MIME: application/vnd.in-toto+json
