## `gradle:7-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:4fae1e2c05da00164cd5458cb2cd763abc1f9fe96945a8323846d4766757d58a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:cf825d2c42bde47d35535151bea31e7df2754e0dcb615dd6021e03937f3e9775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.3 MB (578260156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77a15bf05dfa72b38e41d374b6a27336e2bb670f837e04da170974609a6b61c`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 10 Sep 2025 15:58:43 GMT
COPY /rootfs/ / # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
CMD ["/bin/bash"]
# Wed, 10 Sep 2025 15:58:43 GMT
ARG version=1.8.0_462.b08-1
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
ENV LANG=C.UTF-8
# Wed, 10 Sep 2025 15:58:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 10 Sep 2025 15:58:43 GMT
CMD ["gradle"]
# Wed, 10 Sep 2025 15:58:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 10 Sep 2025 15:58:43 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 10 Sep 2025 15:58:43 GMT
WORKDIR /home/gradle
# Wed, 10 Sep 2025 15:58:43 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 10 Sep 2025 15:58:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
USER gradle
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
USER root
```

-	Layers:
	-	`sha256:b6baa302384dc877580d7e1080dcca1ed66d9d3b38afc9fcc29c360239e3e362`  
		Last Modified: Tue, 16 Sep 2025 20:50:40 GMT  
		Size: 54.0 MB (54005280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b7f6114f43162a846905e6f7eb9e665dbc7d004c5eaed3284e1e08792ab7e5`  
		Last Modified: Thu, 25 Sep 2025 02:15:26 GMT  
		Size: 330.8 MB (330839736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634370fa55c2ff6130b15ba5415b3a4b97a412986c16b53efa1d4aea015b617a`  
		Last Modified: Thu, 25 Sep 2025 03:50:05 GMT  
		Size: 64.9 MB (64888853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5252cc58e115f57f719140d4b8eafc79cdaa7305ac19d82b1ba935dde5765abc`  
		Last Modified: Thu, 25 Sep 2025 03:50:00 GMT  
		Size: 1.9 KB (1942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291963f84392f01975cd6f20a25fb00c016e22176942486d2ffd980aafbd2456`  
		Last Modified: Thu, 25 Sep 2025 22:20:00 GMT  
		Size: 128.5 MB (128469409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec3128c7b0d80d5c9ea48d5bcf310634ccf934dcc5cd0a0427a3abdd6002767`  
		Last Modified: Thu, 25 Sep 2025 03:50:00 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:f6493ee00a17c1bab86b9057e0c8cb4f84b74a16fa8937061efcd59605105b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18056396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d6e2c8704f85b5e1414cb17c15526ae1edb41362d420f996e1454a49f116c8`

```dockerfile
```

-	Layers:
	-	`sha256:494e1373aeb0a1588501dfdfbc904798c358576b5aa2b8946cb4418b4d636901`  
		Last Modified: Thu, 25 Sep 2025 05:18:55 GMT  
		Size: 18.0 MB (18035489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c51b144e9c8c94394e79ebea0ab454982d267ae61d9b9269c354b576c3d6420`  
		Last Modified: Thu, 25 Sep 2025 05:18:56 GMT  
		Size: 20.9 KB (20907 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:4d2d2adfd78b14ffd4026259c092033f26c0ca84030d04c970445049e145e1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 MB (384445415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad222e1da44a44aedc9f5238733d3299fd6323e0ae6c63c6067c542bca0790ff`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 10 Sep 2025 15:58:43 GMT
COPY /rootfs/ / # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
CMD ["/bin/bash"]
# Wed, 10 Sep 2025 15:58:43 GMT
ARG version=1.8.0_462.b08-1
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
ENV LANG=C.UTF-8
# Wed, 10 Sep 2025 15:58:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 10 Sep 2025 15:58:43 GMT
CMD ["gradle"]
# Wed, 10 Sep 2025 15:58:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 10 Sep 2025 15:58:43 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 10 Sep 2025 15:58:43 GMT
WORKDIR /home/gradle
# Wed, 10 Sep 2025 15:58:43 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 10 Sep 2025 15:58:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
USER gradle
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
USER root
```

-	Layers:
	-	`sha256:202438f011bd656c28426fbd92ff7e7030b77e67ebafd3bec95dbce9626db73c`  
		Last Modified: Tue, 16 Sep 2025 22:16:03 GMT  
		Size: 52.9 MB (52899438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76e2ef61c12423fdc72412cc6a21aaf6508a2b71e1a953a0fef12f68ec587c7`  
		Last Modified: Wed, 24 Sep 2025 21:12:18 GMT  
		Size: 117.9 MB (117939624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b79d8291d8efc9b643c955a461bba2bcd4a84765dc995c2132388684429ad2a`  
		Last Modified: Thu, 25 Sep 2025 22:21:32 GMT  
		Size: 85.1 MB (85075723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1319b92a2a144cd8534713673c7087695857cdc1322c0a69a7e81ca075f5167`  
		Last Modified: Thu, 25 Sep 2025 01:17:17 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d55f339ddbe3adf3d1050d02475ba1697582cafdc6cdd67d6bc77b3d0403bc4`  
		Last Modified: Thu, 25 Sep 2025 22:21:42 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ef28e975c1bbbfefc2fda0cb538916307e93fd88472af3ca91da0abb5812a9`  
		Last Modified: Wed, 24 Sep 2025 22:53:08 GMT  
		Size: 59.5 KB (59533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:19ec1fd60859616cbde9a48562696a98ff56dc31d1410eb1676b3c83625030b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11620753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac4000c03641aa827f60bc8a6d13e7c0fcbb64f7150e510e15735571a1f82ae`

```dockerfile
```

-	Layers:
	-	`sha256:9ced7b87093c0f66a124a2063f0e0f938807357defebba38b1735e7ea817bd9e`  
		Last Modified: Thu, 25 Sep 2025 02:19:06 GMT  
		Size: 11.6 MB (11599673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:032a296c3416bbb154f897bdd1b8182a22657e1c2b1abdead0fbbcb44f6ac519`  
		Last Modified: Thu, 25 Sep 2025 02:19:07 GMT  
		Size: 21.1 KB (21080 bytes)  
		MIME: application/vnd.in-toto+json
