## `gradle:7-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:f43abcefb23eae2f9e143ca20bc51a393c10df9d3c457dfeda10ae76f3e58514
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:3959e4cc0150986ceb2a652a6ed31d3c64f715d374a9eee427ea42e530d279b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.9 MB (578886251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b317d36158d7d91c6d8633fe9cd4996ad349754ab89ae0d7f42994995f7ba4fa`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:01 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:09:26 GMT
ARG version=1.8.0_482.b08-1
# Mon, 02 Mar 2026 23:09:26 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:09:26 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:09:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 03 Mar 2026 00:12:23 GMT
CMD ["gradle"]
# Tue, 03 Mar 2026 00:12:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Mar 2026 00:12:23 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 03 Mar 2026 00:12:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 03 Mar 2026 00:12:23 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Mar 2026 00:12:23 GMT
WORKDIR /home/gradle
# Tue, 03 Mar 2026 00:12:23 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 03 Mar 2026 00:12:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 03 Mar 2026 00:12:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 03 Mar 2026 00:12:26 GMT
USER gradle
# Tue, 03 Mar 2026 00:12:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 03 Mar 2026 00:12:26 GMT
USER root
```

-	Layers:
	-	`sha256:2584a8e504dfaf493eadaafafbabd8b97f7cb5bbe3cb6a319fb37cf3c4335d86`  
		Last Modified: Thu, 19 Feb 2026 02:57:43 GMT  
		Size: 54.0 MB (54032840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b18538accb88a58aed84b71209400853929ec0f545d15034e35d003d55ec3`  
		Last Modified: Mon, 02 Mar 2026 23:10:21 GMT  
		Size: 330.9 MB (330924119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670aa7c07b403943f8c3e2c6f1083e3f4c7e2c20511e8651d68746e823188214`  
		Last Modified: Tue, 03 Mar 2026 00:13:08 GMT  
		Size: 65.4 MB (65402998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1083a7768210246c73f5027084cedef9318baf8e1136e365c6396f41801291b8`  
		Last Modified: Tue, 03 Mar 2026 00:13:05 GMT  
		Size: 1.9 KB (1943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec50ca23e9b8615ee09ed8d547cd4de60ff94e412b62ba148fdc99129ec966b`  
		Last Modified: Tue, 03 Mar 2026 00:13:10 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075e234d61e351b2b8bc204dca1c22dd3473861e55a55c4ec961a4517a8949cb`  
		Last Modified: Tue, 03 Mar 2026 00:13:05 GMT  
		Size: 54.9 KB (54903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:b0ae0cbc70fb80157e151dfcad9c6f42607f2413d68e1b85ce9a9998b1d11df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18084819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc4c85295d81a25b727fdf0d68f6073d16eed326eee76e8be0df715a641a6a7`

```dockerfile
```

-	Layers:
	-	`sha256:ee3dbf9ec4d6b0afcf5c77c6ac87bae2fcbf7860542621fb4973355d4eb9fae0`  
		Last Modified: Tue, 03 Mar 2026 00:13:06 GMT  
		Size: 18.1 MB (18063955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03518e4fae1b8e84879e549bb64815516e2ac0ebfed24d6eb0a85b84d689d68a`  
		Last Modified: Tue, 03 Mar 2026 00:13:06 GMT  
		Size: 20.9 KB (20864 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:63e440fdc87eeb85dfbf1bafce87ececf307e36e0620bbbfdb525d0acd93f108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.0 MB (384975224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c74a7089ae4d604f234803cfc1b0e064c772af8b645c980711d003f6628d9b`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:04 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:09:57 GMT
ARG version=1.8.0_482.b08-1
# Mon, 02 Mar 2026 23:09:57 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:09:57 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:09:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 03 Mar 2026 00:13:06 GMT
CMD ["gradle"]
# Tue, 03 Mar 2026 00:13:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Mar 2026 00:13:06 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 03 Mar 2026 00:13:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 03 Mar 2026 00:13:06 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Mar 2026 00:13:06 GMT
WORKDIR /home/gradle
# Tue, 03 Mar 2026 00:13:06 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 03 Mar 2026 00:13:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 03 Mar 2026 00:13:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 03 Mar 2026 00:13:09 GMT
USER gradle
# Tue, 03 Mar 2026 00:13:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 03 Mar 2026 00:13:10 GMT
USER root
```

-	Layers:
	-	`sha256:9330fae67a20d9aa2569828674140d8b67d50cfd127cb99ba0f9be275d35f976`  
		Last Modified: Thu, 19 Feb 2026 02:57:42 GMT  
		Size: 52.9 MB (52941319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de3d3a8cae532adff8f9f52c5b597c5da455126a70f8cfc9bb3ff95473ed1ac`  
		Last Modified: Mon, 02 Mar 2026 23:10:17 GMT  
		Size: 118.0 MB (117965736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d980caa94640e2a23364928f1582da59b56031d3dbc6544526cb46fff005ee`  
		Last Modified: Tue, 03 Mar 2026 00:13:40 GMT  
		Size: 85.5 MB (85537552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba50e263d8729a64dab791f5f0bc8357fa79380d2c335e0af22e64367ac7bf1`  
		Last Modified: Tue, 03 Mar 2026 00:13:37 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ee3344b857084372453a7dc8c96c38baaaa1c17c0e946ce1e2595c1f3eec7d`  
		Last Modified: Tue, 03 Mar 2026 00:13:41 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05902b68655579ce26a0b0e4eeb205ceb3b763b6b1bca514ba8ce2b8d7da90ef`  
		Last Modified: Tue, 03 Mar 2026 00:13:37 GMT  
		Size: 59.5 KB (59522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:db52e334753be585aee5eef665944dd8dec7ddd3907c2f906f95fb03154d14dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11649160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487ca2941b3822387183f04d52df30133415dce44f94df79a84874879e47339a`

```dockerfile
```

-	Layers:
	-	`sha256:e10236ed63e2ef58aa0581448e4578e7f1d071c85e799e0739917f888d2a3789`  
		Last Modified: Tue, 03 Mar 2026 00:13:38 GMT  
		Size: 11.6 MB (11628123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb512e081f55193a50fdf01ce889aecdb8c64e4a7584e9b0e5b67b034493e6a6`  
		Last Modified: Tue, 03 Mar 2026 00:13:37 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json
