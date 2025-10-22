## `gradle:9-jdk17-corretto`

```console
$ docker pull gradle@sha256:1078ae8204be62b1ef3391eb052bf8015dabc44044e0827641f02d564b9a18bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:1fbe80a7eb7b23e42defc68831987e4e663ef42172cd4b41ad484d37e62831a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.1 MB (431067245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9191b3b686164f3fa1b99ff02e34bea0b0f6a56c7cf61d57c84177b550e80231`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 30 Sep 2025 09:31:25 GMT
COPY /rootfs/ / # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 09:31:25 GMT
ARG version=17.0.17.10-1
# Tue, 30 Sep 2025 09:31:25 GMT
ARG package_version=1
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV LANG=C.UTF-8
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c18700ed5b667d3e3ad2c64896284eb1ca36287f16a71ecfb7d35d0da454038`  
		Last Modified: Wed, 22 Oct 2025 00:50:39 GMT  
		Size: 156.9 MB (156935240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bbdf8a5077433ccd574bce30f835d5298674a2ba85cfa056a9c57360f0b494`  
		Last Modified: Wed, 22 Oct 2025 02:38:32 GMT  
		Size: 85.6 MB (85555629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2018fe9dc835001c723c9e92d8c114062b9155cc6968221f058b538d777b07f1`  
		Last Modified: Wed, 22 Oct 2025 02:38:23 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225f275e7b008820afdf74b8a204de3f79f495541f88ff25a091a25a8cebb2a8`  
		Last Modified: Wed, 22 Oct 2025 06:12:09 GMT  
		Size: 134.5 MB (134514677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096228683cde96e043c7cc54e7de19e74c2809cb2ef7b2ca1efe42e040bdb36c`  
		Last Modified: Wed, 22 Oct 2025 02:38:23 GMT  
		Size: 54.9 KB (54893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:23a11c2360e4b322bb961329f5196e90b7304bedd8a46869b1e42005d0efc9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11321085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aae4da0918bab3cd627176ad9500b89a84143de1344e1174b73f942343c400c`

```dockerfile
```

-	Layers:
	-	`sha256:a34df85856c0b21b7d8804a1749ae627b0a600605c94854c380f9b017bd4496b`  
		Last Modified: Wed, 22 Oct 2025 05:22:56 GMT  
		Size: 11.3 MB (11299594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1586e4840ef858773fad295fda0bba850986d491b4dacacee8104a2d34948214`  
		Last Modified: Wed, 22 Oct 2025 05:22:57 GMT  
		Size: 21.5 KB (21491 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:806b683ff9b2ccd2c4ec3a9204ed480d64fef51e716176130ddaf93cabecddcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.3 MB (428298933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0dd3da4ae49e3c06b64acea8f23caac340f8f94e89cbfbbd26ab43d3fd331f`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 30 Sep 2025 09:31:25 GMT
COPY /rootfs/ / # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 09:31:25 GMT
ARG version=17.0.17.10-1
# Tue, 30 Sep 2025 09:31:25 GMT
ARG package_version=1
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV LANG=C.UTF-8
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6803c97e6c0d717ec8eb0dfce3611037cd37d1539766448f9235c54a09a795`  
		Last Modified: Tue, 21 Oct 2025 22:11:31 GMT  
		Size: 155.7 MB (155747849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5ea8161a27649bb1cff5b66658a5abbb4cc08f6cc916ea9b0e37e346eef681`  
		Last Modified: Tue, 21 Oct 2025 22:12:47 GMT  
		Size: 85.1 MB (85084000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c226f78b42bd0a78428b9750e209cce152848a29abfb2ef6a32e3bc02ea7266e`  
		Last Modified: Tue, 21 Oct 2025 22:12:39 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f0d7157d0dccf1bc12be042d5b004fa7f2eb8f03868611e56967d8f67018d9`  
		Last Modified: Wed, 22 Oct 2025 03:33:03 GMT  
		Size: 134.5 MB (134514677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50ecd26cd3905694e8ce838d1ff917d3c8d8ccdde5500842cdfb7715e2c9303`  
		Last Modified: Tue, 21 Oct 2025 22:12:38 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:0694566937638a564f41a1b6ea13ef3c4df11a94c90515cab6089c9fe3e3cea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11320281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989e428f819591f2799ff6e2f34e1702194d63e9b21ac5cf6c2c07c9b615ed96`

```dockerfile
```

-	Layers:
	-	`sha256:e23901b399cb773baf932eb2b73bfd5459fe4b955aaa3ff5a8604b0db2d65291`  
		Last Modified: Tue, 21 Oct 2025 23:23:09 GMT  
		Size: 11.3 MB (11298593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73013f6312271823ca06c421e8183b94f5c3f10ca884573cce35dee81a24fa45`  
		Last Modified: Tue, 21 Oct 2025 23:23:10 GMT  
		Size: 21.7 KB (21688 bytes)  
		MIME: application/vnd.in-toto+json
