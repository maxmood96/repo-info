## `gradle:7-jdk8-corretto`

```console
$ docker pull gradle@sha256:c6e2f68cb6b58b555cf0bc1ecf49920223aa55fc2f86e32115e23ea569682bb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:3f22ccd6e22bd2768bb9f5cc400ff9f455236a8250699fd4ff1f9d989fe6a293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.5 MB (579474044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a239f9b12e2e6092dcbe468954ffbf0f30e35e38b55035b52de1aa43155b973`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:32 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:32 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:48:05 GMT
ARG version=1.8.0_482.b08-1
# Mon, 13 Apr 2026 22:48:05 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 22:48:05 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:48:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 13 Apr 2026 23:41:04 GMT
CMD ["gradle"]
# Mon, 13 Apr 2026 23:41:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 13 Apr 2026 23:41:04 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 13 Apr 2026 23:41:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 13 Apr 2026 23:41:04 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 13 Apr 2026 23:41:04 GMT
WORKDIR /home/gradle
# Mon, 13 Apr 2026 23:41:04 GMT
ENV GRADLE_VERSION=7.6.6
# Mon, 13 Apr 2026 23:41:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Mon, 13 Apr 2026 23:41:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 13 Apr 2026 23:41:07 GMT
USER gradle
# Mon, 13 Apr 2026 23:41:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 13 Apr 2026 23:41:07 GMT
USER root
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1983f26d4f73d2638487eb5a60254859b1629d25024622b419593661d40b82`  
		Last Modified: Mon, 13 Apr 2026 22:48:58 GMT  
		Size: 330.9 MB (330921442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ad8f9adb9177c2675ee4e82518f25d157c76ade27be7646a1b6c7d4aba44cc`  
		Last Modified: Mon, 13 Apr 2026 23:41:49 GMT  
		Size: 65.5 MB (65455054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bb7989e028b84acb868a9e409c571db5b80baff53bf23eb463db2581385748`  
		Last Modified: Mon, 13 Apr 2026 23:41:45 GMT  
		Size: 1.9 KB (1940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a22d482177ac2982c7e9957cf62775a79064b3a5bf9ebc4a0692abb9f157c3`  
		Last Modified: Mon, 13 Apr 2026 23:41:51 GMT  
		Size: 128.5 MB (128469418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2fcf3571686bab025f8b70a69c521b1a826a5780bf35476588c090d3e54f66`  
		Last Modified: Mon, 13 Apr 2026 23:41:46 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:7764337383e5937066a8fb9c3113c21cea884ad4c97bd86fd2b1c8f15a4e5ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18092908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11597e048d7ef218adbe969acc139eeeca4cd7d7229acdfcb87a9c22dc8684e9`

```dockerfile
```

-	Layers:
	-	`sha256:ae9f1d20cee297d27e9507157c0b8ab6b88466ebaf278f647d3e60c667cc1e4a`  
		Last Modified: Mon, 13 Apr 2026 23:41:46 GMT  
		Size: 18.1 MB (18072044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2ef0ce20c367194724d9c10422e869617f85df59acdd72784d1e2946a834a21`  
		Last Modified: Mon, 13 Apr 2026 23:41:45 GMT  
		Size: 20.9 KB (20864 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9b2d475685730f43a1aaf7f12fd4d7af84d8d53ace76e3036311a96914b5cf6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.5 MB (385519603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b102eba8bcf40800a444a1e4a7cee16596d0035e4ec527a593a179b27d67287`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 22:21:43 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:21:43 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:10:29 GMT
ARG version=1.8.0_482.b08-1
# Mon, 13 Apr 2026 23:10:29 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 23:10:29 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:10:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 13 Apr 2026 23:54:34 GMT
CMD ["gradle"]
# Mon, 13 Apr 2026 23:54:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 13 Apr 2026 23:54:34 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 13 Apr 2026 23:54:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 13 Apr 2026 23:54:34 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 13 Apr 2026 23:54:34 GMT
WORKDIR /home/gradle
# Mon, 13 Apr 2026 23:54:34 GMT
ENV GRADLE_VERSION=7.6.6
# Mon, 13 Apr 2026 23:54:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Mon, 13 Apr 2026 23:54:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 13 Apr 2026 23:54:37 GMT
USER gradle
# Mon, 13 Apr 2026 23:54:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 13 Apr 2026 23:54:38 GMT
USER root
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd51fd7ccca75a0b426896e7519c1bd14d9d834f603f074a9f60c9b5d277a41`  
		Last Modified: Mon, 13 Apr 2026 23:10:49 GMT  
		Size: 118.0 MB (117962706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0304016101a28eb560f0ad8fab079f0a9915e86c9c46c7139be1951fcdae8e`  
		Last Modified: Mon, 13 Apr 2026 23:55:09 GMT  
		Size: 85.6 MB (85583531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bc96b94ab5f6a69cd68d406362bd6d8319ec3b2d45151f811963dc4eed21e3`  
		Last Modified: Mon, 13 Apr 2026 23:55:05 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea3c0c4cfe57cf64ca0cfbe03b8e3d9ca585d0822c87b693831faea078bc86f`  
		Last Modified: Mon, 13 Apr 2026 23:55:09 GMT  
		Size: 128.5 MB (128469418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1162bf4ad961b6211413a87dc8a52b575fce63ebd455264eb2ee975cc76817a`  
		Last Modified: Mon, 13 Apr 2026 23:55:05 GMT  
		Size: 59.5 KB (59529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:2f02946b6b7ee49695e1e77ff669d041e8d20e481c951586b26592b597826acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11657249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c1276276afed9b0026a76a6c842543a6969768672c5cf9e2191faef933ef95`

```dockerfile
```

-	Layers:
	-	`sha256:51316e469d50cec90043c7db27ecbf52000df2650d721543025e9c6d34316267`  
		Last Modified: Mon, 13 Apr 2026 23:55:05 GMT  
		Size: 11.6 MB (11636212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61724b01deb52a94a6871e8322b8c1d9fedeb2e4a4f9ae1c12ca12dcdb78d381`  
		Last Modified: Mon, 13 Apr 2026 23:55:05 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json
