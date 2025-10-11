## `gradle:jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:f381ef8e0a2bb63f6ee314a0bec885e2fef8786932e92aba86661dc250f6e07f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:e11cd3ad037626e34e94edd68d244642ff816908f7c9a036a07c9348312e9e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.1 MB (431090561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863438a76951cb0a43633d9cec8ff37af2969cdd20205be2e6bef4c5a5aaeb54`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 29 Sep 2025 16:01:58 GMT
CMD ["gradle"]
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Sep 2025 16:01:58 GMT
WORKDIR /home/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_VERSION=8.14.3
# Mon, 29 Sep 2025 16:01:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER gradle
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER root
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bea491ccf4f1cb4479c0d0dd695e9eaea15d1c73558a4e304bd3314fb876293`  
		Last Modified: Mon, 06 Oct 2025 22:11:15 GMT  
		Size: 154.1 MB (154072396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b30de40c51fd8678b22ba939f23d285445e4cdd78b6820a14e7371a3ae02b1`  
		Last Modified: Mon, 06 Oct 2025 22:12:23 GMT  
		Size: 85.6 MB (85561312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269e4f6f8db81c6e354f8eadd972d5af308a48fd3d530d085761119813ecc827`  
		Last Modified: Mon, 06 Oct 2025 22:12:18 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b903ec27f32bb9c2c7a6e3dfa7adbaa4a3bf314e4899198496264fe09f5638e`  
		Last Modified: Tue, 07 Oct 2025 05:07:46 GMT  
		Size: 137.4 MB (137395130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff90997ba34ffa2d1a72185c4766fc31e8212cd99658522d9e5759deea57085`  
		Last Modified: Mon, 06 Oct 2025 22:12:18 GMT  
		Size: 54.9 KB (54913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:3214eb72ed688420d2719c10a7cfbf86ad1c066947091d9a6a4ef9717c99a91b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11359215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a89f880479792efc85939e41b2cc06d6491d53df43d1fbbc875f9b848c90d62`

```dockerfile
```

-	Layers:
	-	`sha256:ea3361e195e7aa120b82e87a9a13f80ffb38c0e6a0b1759c40f1003ea89d862f`  
		Last Modified: Mon, 06 Oct 2025 23:20:39 GMT  
		Size: 11.3 MB (11337649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0946ba12b85c607ae24fb1584f2f0f16986e58c80203f3571a876bffaeafcf03`  
		Last Modified: Mon, 06 Oct 2025 23:20:40 GMT  
		Size: 21.6 KB (21566 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1627e2a8b26197aa79e5c24122613ce2a5a89479b922f08de1b1ed279336854c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.0 MB (428014887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c48cbf51823c36008d76b4b7a252dc90af07ca2a2301d3eaec76a30f1ab701`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 29 Sep 2025 16:01:58 GMT
CMD ["gradle"]
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Sep 2025 16:01:58 GMT
WORKDIR /home/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_VERSION=8.14.3
# Mon, 29 Sep 2025 16:01:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER gradle
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER root
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60693563db8a15ef6cbbb254b5f7cdd25c3f0b7dea83ba28e605d00261462016`  
		Last Modified: Mon, 06 Oct 2025 22:11:35 GMT  
		Size: 152.6 MB (152580439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee613fb6927a314bcaf1fa064d829ea0cdd6a0c13e2d3138ccc7adf9d17bc8ca`  
		Last Modified: Mon, 06 Oct 2025 22:13:07 GMT  
		Size: 85.1 MB (85086905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9386d2f779f3bd29b236926431399293c411d9191b5c6a6394fe150c6948b2`  
		Last Modified: Mon, 06 Oct 2025 22:13:01 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b9159c28ab1e67ab81e9838d6061d359c987fa4c4b5f9b800190a203dd8abf`  
		Last Modified: Wed, 08 Oct 2025 06:08:29 GMT  
		Size: 137.4 MB (137395130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2944faa15b094a60971f6190d2590008af23126acdd805c8ad72524e99fd89b6`  
		Last Modified: Mon, 06 Oct 2025 22:13:01 GMT  
		Size: 59.5 KB (59531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:29cc389a14f248b760d50ccb9ab69466459312f5ca0435fe6e07d3f283b25cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11359255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4144f3fc55008446e5771aa35aea7fd45c8588a92f1acd5cdb79654d67b4c046`

```dockerfile
```

-	Layers:
	-	`sha256:a47a6fa36ce206bae28790f35999287c318966624f4aad6667fa9ae5c1b2785d`  
		Last Modified: Mon, 06 Oct 2025 23:20:48 GMT  
		Size: 11.3 MB (11337492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78580cefc714b5429f947bf094c22c56c98e7a6e51f5a18ad1b2c1c37e708022`  
		Last Modified: Mon, 06 Oct 2025 23:20:50 GMT  
		Size: 21.8 KB (21763 bytes)  
		MIME: application/vnd.in-toto+json
