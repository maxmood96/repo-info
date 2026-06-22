## `gradle:7-jdk11-corretto`

```console
$ docker pull gradle@sha256:f634ee4b78f14844e4a3d0aaf90c16714b4f3e5e4a4f3aa6ee9bd68913aa81eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:de54b3df459698b41cdf966dc670d34df730103d6a1f268a60708528b2e4abf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.2 MB (423219155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43561a5e3f23454b473081d191325eae80b0fdd2ce775b58e399357528e2ddf7`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:03:18 GMT
ARG version=11.0.31.11-1
# Mon, 22 Jun 2026 18:03:18 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:03:18 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:03:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 22 Jun 2026 18:16:16 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:16:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:16:16 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:16:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 18:16:16 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:16:16 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:16:16 GMT
ENV GRADLE_VERSION=7.6.6
# Mon, 22 Jun 2026 18:16:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Mon, 22 Jun 2026 18:16:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:16:19 GMT
USER gradle
# Mon, 22 Jun 2026 18:16:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 22 Jun 2026 18:16:19 GMT
USER root
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b86e893760418631bb758ba7596a4f62c94cb9b2a50a89142f128dcddcf769`  
		Last Modified: Mon, 22 Jun 2026 18:03:40 GMT  
		Size: 153.5 MB (153472915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a7b2584ebb2d06f5682032dce876542e7a738b029ab81929774030d3b54666`  
		Last Modified: Mon, 22 Jun 2026 18:16:49 GMT  
		Size: 86.6 MB (86646031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61a47d48a969b217b96c62566febd7b369b03d5fa1a53fc71fd4edc8737b771`  
		Last Modified: Mon, 22 Jun 2026 18:16:46 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e4b7c68122fe78ce47e91f0b9a5e1bc702de803e9150369c2dcd30f144cd4`  
		Last Modified: Mon, 22 Jun 2026 18:16:50 GMT  
		Size: 128.5 MB (128469440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063cfc053d22818207b6e3e772260cdb1a21dc7712d31e55f6f4ba03795e6249`  
		Last Modified: Mon, 22 Jun 2026 18:16:46 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:baa3d1547925cc10d4b6f50f7f33c601b95a83c6fcad013d15a3c463d3827821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11311694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8e9112e1b79758ad81ddd41c98773264f295d68500a0156b47bb9b7aafdb6c`

```dockerfile
```

-	Layers:
	-	`sha256:eca0ad76ba20abe6dd1d2dadaffdcea5119653f6b3e23c55a9be94c836e4df9f`  
		Last Modified: Mon, 22 Jun 2026 18:16:46 GMT  
		Size: 11.3 MB (11290823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e36f447c5cf509228bb22c03656aa54fa8bfa3e44370778fbf01d8d808a6aff`  
		Last Modified: Mon, 22 Jun 2026 18:16:45 GMT  
		Size: 20.9 KB (20871 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:bc35e6f0a06ff823aef2219c800d3039beb225f1f6ecff1045d3564c0466e170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.1 MB (420067936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9374f584b8882de73a47cb005ec355af5b80f8edcfeaee0b12d9315f07c59d`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:10 GMT
ARG version=11.0.31.11-1
# Mon, 22 Jun 2026 18:14:10 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:14:10 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 22 Jun 2026 18:29:38 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:29:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:29:38 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:29:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 18:29:38 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:29:38 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:29:38 GMT
ENV GRADLE_VERSION=7.6.6
# Mon, 22 Jun 2026 18:29:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Mon, 22 Jun 2026 18:29:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:29:41 GMT
USER gradle
# Mon, 22 Jun 2026 18:29:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 22 Jun 2026 18:29:41 GMT
USER root
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edde251e78ae931471e2eec1d6090d2888ad7ce776de98251a52827dff5f3dba`  
		Last Modified: Mon, 22 Jun 2026 18:14:31 GMT  
		Size: 152.1 MB (152050355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cacd14b1f171bc8440e0e989e6149e53cf1956cf3d7c99aa9a6ad03f40052f`  
		Last Modified: Mon, 22 Jun 2026 18:30:13 GMT  
		Size: 86.0 MB (86036295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d543551b1e251e093284ea397773cc9026046e855bd0a10cae9f261f77f727`  
		Last Modified: Mon, 22 Jun 2026 18:30:09 GMT  
		Size: 1.6 KB (1642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f072022a43e496fd04e6d4a4b92d98e6788ecd81a4dfbd696f84ed53c1d72ee`  
		Last Modified: Mon, 22 Jun 2026 18:30:14 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0ae97ec03725a49988e62a44a1754eaba10db7202106d3b6fe3695505dbce2`  
		Last Modified: Mon, 22 Jun 2026 18:30:09 GMT  
		Size: 59.5 KB (59509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:703d65124c32759649f66db81044c625df7382cc8b60e4dd2ad245f239a4d976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11311685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d831ac7a42eceeb633a0db41d87ea75baa364c92ce8d59816df27090760c029`

```dockerfile
```

-	Layers:
	-	`sha256:dd4eac08ce70d3f59cfd0478045b1d46801e53e716ab071855d4453449746d7a`  
		Last Modified: Mon, 22 Jun 2026 18:30:09 GMT  
		Size: 11.3 MB (11290642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cd4270b2b1ba18373bc8ca540a6f1e99ef0570973a2263f0bd1f97f38112308`  
		Last Modified: Mon, 22 Jun 2026 18:30:09 GMT  
		Size: 21.0 KB (21043 bytes)  
		MIME: application/vnd.in-toto+json
