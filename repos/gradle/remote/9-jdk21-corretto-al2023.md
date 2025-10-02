## `gradle:9-jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:b4ff75849d74631bb3672de731f84cf7039633e2277d44fbd4049812ae30460c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:7d7e90dbf7b0ae6edee5ffc8b451b3563d5ffbb2b845b4cb61be7a70a92f2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.2 MB (444249186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37f8af67302285d3e7e3bee433306892c1f6af9ce5c8c3add5227facbe06093`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:20 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=21.0.8.9-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
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
	-	`sha256:b6baa302384dc877580d7e1080dcca1ed66d9d3b38afc9fcc29c360239e3e362`  
		Last Modified: Tue, 16 Sep 2025 20:50:40 GMT  
		Size: 54.0 MB (54005280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c498890e134f4cb5ae6fe96c92110f3c6a1643cbe0d8dbf42d1e54cd30b431`  
		Last Modified: Thu, 25 Sep 2025 03:12:20 GMT  
		Size: 170.1 MB (170113309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d562438b2d50e07e4b9e7a77efacb5a1844c935d052c7de35a3133575e54de`  
		Last Modified: Tue, 30 Sep 2025 16:58:23 GMT  
		Size: 85.6 MB (85559341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf0f4c5efd5bedc9f7b0b40dae3e52e0448446568afef442c2d14e0dcd307eb`  
		Last Modified: Tue, 30 Sep 2025 16:58:14 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ab89b26a95165c4ea8bef3223ddb6a71e1a9747cacbf30c78848af3e19d613`  
		Last Modified: Wed, 01 Oct 2025 14:32:20 GMT  
		Size: 134.5 MB (134514677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9112af54be72dc7c06474ec9203f97f833ad11620ff4f0631b145adaef0f5cfd`  
		Last Modified: Tue, 30 Sep 2025 16:58:14 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:6f017752e0a53fe91998c6755ebfa84a8fe66f08ed554aab3e14fa0235dee894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11323642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ee6027be271706ab8345fbed634c3c90dd094050b60c646cad7daebed5287c`

```dockerfile
```

-	Layers:
	-	`sha256:58f04996c0d9d47ec8704006e68b0ad4ae967f02ad483d3d4b42ec1ce75ab7e6`  
		Last Modified: Wed, 01 Oct 2025 14:22:52 GMT  
		Size: 11.3 MB (11301998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f24e5b0ba080413bc424c9d77a53a8abb8f0358f0d313a88d67fe460ae46c84`  
		Last Modified: Wed, 01 Oct 2025 14:22:53 GMT  
		Size: 21.6 KB (21644 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:35a311fa191d1dc427432c8bda65657939cdfcea9279dff1cf7308f85107a3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.0 MB (440958425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a245e8ab7a901cec2eb7bf791ab3f44a7a87caa00b5470a9bf10abae8a5882b6`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:25 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=21.0.8.9-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
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
	-	`sha256:202438f011bd656c28426fbd92ff7e7030b77e67ebafd3bec95dbce9626db73c`  
		Last Modified: Tue, 16 Sep 2025 22:16:03 GMT  
		Size: 52.9 MB (52899438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda7a391125898fe088b7a329ba667267f6a8e4cd156d822b71c3cc24d07388e`  
		Last Modified: Wed, 24 Sep 2025 22:10:27 GMT  
		Size: 168.4 MB (168400554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5a664f8392bfe3c710995f39d959319f20067e96d9903991ac90b0c3851f4c`  
		Last Modified: Thu, 02 Oct 2025 06:54:45 GMT  
		Size: 85.1 MB (85082481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d91f6cb67ee29422ca3e92875212b6f2e384375ff28cf40cb7d48124b6b54a`  
		Last Modified: Wed, 01 Oct 2025 06:34:00 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb76e1a3bbfec87ac9ff86e36a7e2a7dd12f3cf0733fa68c39617a961f597a2`  
		Last Modified: Thu, 02 Oct 2025 06:54:52 GMT  
		Size: 134.5 MB (134514744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5209f85cfc65ea932f6fca6e69cdc5a48070dc0f2e0b5bfb80bdc057cf9fb134`  
		Last Modified: Wed, 01 Oct 2025 06:40:04 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:b146d1576e65526faccd63df4e0448f93c88fd1042a747df63a26b7efdce130f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11322842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488f27a5ec3dc96361f3e4828ae6b4032144cf1a895bf295eed41316e7ca8ab4`

```dockerfile
```

-	Layers:
	-	`sha256:146572c102b27d0780db1fa05b3b2c7c9a835c93af4bebf027b93a01a36b85eb`  
		Last Modified: Wed, 01 Oct 2025 20:26:48 GMT  
		Size: 11.3 MB (11301000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19efd780ba78fd2b4e87551f10ba1eed311961dc0a36cf87e75c332a6a62fbdc`  
		Last Modified: Wed, 01 Oct 2025 20:26:50 GMT  
		Size: 21.8 KB (21842 bytes)  
		MIME: application/vnd.in-toto+json
