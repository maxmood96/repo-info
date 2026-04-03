## `gradle:jdk8-corretto`

```console
$ docker pull gradle@sha256:b4984ef163660abc105e7d7bf37634610f95b1e4d4b3bfadcd56d3d5a4c1f52f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:1a823fc29d35551a852ea3e3926f1055c904183f094d54272796948402b98849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.8 MB (587804627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8845d3d8fa0fb92060de30ed60175e3c20815700057d639f0996c4c4685f5330`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:05:57 GMT
ARG version=1.8.0_482.b08-1
# Fri, 03 Apr 2026 17:05:57 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:05:57 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:05:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 03 Apr 2026 17:14:02 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 17:14:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 17:14:02 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 17:14:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 17:14:03 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 17:14:03 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 17:14:03 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 03 Apr 2026 17:14:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 03 Apr 2026 17:14:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 17:14:05 GMT
USER gradle
# Fri, 03 Apr 2026 17:14:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 03 Apr 2026 17:14:06 GMT
USER root
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81535bfa6f7dd029d87921d4ee5a42b77b0743bb69fcf1a6effada460edf0aaa`  
		Last Modified: Fri, 03 Apr 2026 17:06:51 GMT  
		Size: 330.9 MB (330930128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8339c7aac6c44fc96939c4d6e4718b9b5b152c9cfa37cf60134e64a07e4ac46`  
		Last Modified: Fri, 03 Apr 2026 17:14:47 GMT  
		Size: 65.4 MB (65396262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29feedf767d2631d68feeeea7e5971efb77279c09d62e1340eb0b6370a0850e`  
		Last Modified: Fri, 03 Apr 2026 17:14:44 GMT  
		Size: 1.9 KB (1943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862a28d2b265111ae9e0c3b15241da42ac8d969eee290a0acaf2a636a0a94211`  
		Last Modified: Fri, 03 Apr 2026 17:14:48 GMT  
		Size: 137.4 MB (137388268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958c1901fa94ea3568d63b5ff92d7a589877d2844ccc275905c3df260ab69ebc`  
		Last Modified: Fri, 03 Apr 2026 17:14:44 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:d53e842733073d7f209595edee9334c4928960ad2d03bc3cef9eb3ee649815d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18175473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c02bf71c4912b8c53a993082ee2f25f5c1ac6b6cac9c937233fa29e8c98121`

```dockerfile
```

-	Layers:
	-	`sha256:b53634c74cc774d6e4bce09c9e876a799d59e1f3e9a5e3e5f450531849b487d4`  
		Last Modified: Fri, 03 Apr 2026 17:14:45 GMT  
		Size: 18.2 MB (18153958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38a9b87e016c741a535f1bda3ad51be7a421d491665a985d4c4ccea558351d90`  
		Last Modified: Fri, 03 Apr 2026 17:14:44 GMT  
		Size: 21.5 KB (21515 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2afcd6add90e8e29ab8483d3df86b92c0e2e4348181337f15ae41269dcd0f502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.9 MB (393890918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abafea20bec5b35f55b07f30d895bbe87c9afd00026d50dc8ed24f7a7b6391b1`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:13:34 GMT
ARG version=1.8.0_482.b08-1
# Fri, 03 Apr 2026 17:13:34 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:13:34 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:13:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 03 Apr 2026 17:30:48 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 17:30:48 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 17:30:48 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 17:30:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 17:30:48 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 17:30:48 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 17:30:48 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 03 Apr 2026 17:30:48 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 03 Apr 2026 17:30:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 17:30:51 GMT
USER gradle
# Fri, 03 Apr 2026 17:30:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 03 Apr 2026 17:30:52 GMT
USER root
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1aa8e5e0737da73799f0150412039fe08c46d3ce741b2162d8b0315532411c`  
		Last Modified: Fri, 03 Apr 2026 17:13:54 GMT  
		Size: 118.0 MB (117964689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb8970ec5d4249bbd2862f49a9035ae2c835c4ee12c6c267583f67b4186e311`  
		Last Modified: Fri, 03 Apr 2026 17:31:23 GMT  
		Size: 85.5 MB (85535369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220f63bae8e1b9abab21afcb9cbef6d75721acde3c46eec46b79e47fa4ad4038`  
		Last Modified: Fri, 03 Apr 2026 17:31:19 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401b51e1d47060644be27827350676d46cfc1d2750b4e92817ffdc9daca90cb3`  
		Last Modified: Fri, 03 Apr 2026 17:31:24 GMT  
		Size: 137.4 MB (137388269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b4b14ec59803843b2f125d6eb3f914abd97a9ebf187103f0e47422c4a06320`  
		Last Modified: Fri, 03 Apr 2026 17:31:19 GMT  
		Size: 59.5 KB (59535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:a8046532a36ab2f0ebbec960e43685d523b3593a35cc2f12b945ac8028230d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11739859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94868b420158885c152b8c4952f39994bbaeac07a6a9ddb162dc895864c52b21`

```dockerfile
```

-	Layers:
	-	`sha256:fe07d40f2c05cd4f3f4e5e0a34b11566a21fc39968c87f5dff61352b150e8684`  
		Last Modified: Fri, 03 Apr 2026 17:31:20 GMT  
		Size: 11.7 MB (11718146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4de9163ac707045972b50f43a65c21c34e5b3e645f3b3c7a3bb39fdc8970513`  
		Last Modified: Fri, 03 Apr 2026 17:31:18 GMT  
		Size: 21.7 KB (21713 bytes)  
		MIME: application/vnd.in-toto+json
