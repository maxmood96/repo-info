## `gradle:6-jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:ba7aea1a80bb9f84a92bb819c459ed9efe1f025fdd027d96f6632c8ba81d4e7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:9e4676261b6d70a8458a4b5935f47128f581667336d0304d2919d8ac259f8497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.3 MB (402323129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9d4bd9e89e865363947ffac42b451f68f5de1b8f296ee695d7440eea990852`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:40 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:09:57 GMT
ARG version=11.0.31.11-1
# Fri, 24 Apr 2026 00:09:57 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:09:57 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:09:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 24 Apr 2026 01:12:30 GMT
CMD ["gradle"]
# Fri, 24 Apr 2026 01:12:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 24 Apr 2026 01:12:30 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 24 Apr 2026 01:12:31 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 24 Apr 2026 01:12:31 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 24 Apr 2026 01:12:31 GMT
WORKDIR /home/gradle
# Fri, 24 Apr 2026 01:12:31 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 24 Apr 2026 01:12:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 24 Apr 2026 01:12:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 24 Apr 2026 01:12:34 GMT
USER gradle
# Fri, 24 Apr 2026 01:12:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 24 Apr 2026 01:12:34 GMT
USER root
```

-	Layers:
	-	`sha256:60406c832328f9a4f3aa21eb9cb5b2182d79ad008cd21f0bbac4517c1836be2e`  
		Last Modified: Tue, 14 Apr 2026 01:03:42 GMT  
		Size: 54.6 MB (54569705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80d44373b6b20ce8327f1b15c6a0145f06a261ca87e4a1909cc7eae76089226`  
		Last Modified: Fri, 24 Apr 2026 00:10:24 GMT  
		Size: 153.5 MB (153474084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0864f2b9b52e1f46d9544754ce4cc71e2e9f58bb2b5388a566d2d5340a07560`  
		Last Modified: Fri, 24 Apr 2026 01:13:04 GMT  
		Size: 86.1 MB (86149754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db5d3f1ef63099cc276b271a5f3011a525109b377e2e30ebeb48400c929950c`  
		Last Modified: Fri, 24 Apr 2026 01:13:00 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95b0f82c66799a9bfdd7b410d7fd08fda8805faa1ea82079cf2e8ce7629b9c7`  
		Last Modified: Fri, 24 Apr 2026 01:13:05 GMT  
		Size: 107.7 MB (107696631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007a6d639d3a85d331e3f57273f7b19714510bca978eb275a4da6f9d8371622`  
		Last Modified: Fri, 24 Apr 2026 01:13:01 GMT  
		Size: 431.3 KB (431277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:1192f5504488a06417a0a861d9ba631bf794ab1dc86eceb62208409f2af8e147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11288472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c011f2cc1a1a5926c2a0c1015903834656d80d99d1ac2780ffb4637a03cc328`

```dockerfile
```

-	Layers:
	-	`sha256:0a64a31593a9274df6441434ebe6d04754a42e60beb9ebe18c4654226547b397`  
		Last Modified: Fri, 24 Apr 2026 01:13:01 GMT  
		Size: 11.3 MB (11267600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9cfe494cea0e16354a48a5f8f2f7bd8d6888605541c12f82cb0ca51b1724c4e`  
		Last Modified: Fri, 24 Apr 2026 01:13:00 GMT  
		Size: 20.9 KB (20872 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e4fb9a426ef39665f81ba2762a14996ee0bdefbe68dff4bedd5ca4c76133e6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.3 MB (399282254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd584c45a94a3dd19be08b82da7f89ac831852f68c63fc7e61ef4274f1a2bfa`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:02 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:09:13 GMT
ARG version=11.0.31.11-1
# Fri, 24 Apr 2026 00:09:13 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:09:13 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:09:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 24 Apr 2026 01:12:47 GMT
CMD ["gradle"]
# Fri, 24 Apr 2026 01:12:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 24 Apr 2026 01:12:47 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 24 Apr 2026 01:12:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 24 Apr 2026 01:12:47 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 24 Apr 2026 01:12:47 GMT
WORKDIR /home/gradle
# Fri, 24 Apr 2026 01:12:47 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 24 Apr 2026 01:12:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 24 Apr 2026 01:12:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 24 Apr 2026 01:12:49 GMT
USER gradle
# Fri, 24 Apr 2026 01:12:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 24 Apr 2026 01:12:50 GMT
USER root
```

-	Layers:
	-	`sha256:a89c935522476873ac76a02a8b4103cba17c6900bdcb1d98998ed64657edf59f`  
		Last Modified: Tue, 14 Apr 2026 02:24:36 GMT  
		Size: 53.5 MB (53452253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a43495d7ee4b274fe35850640e64823f0ffec4fc64191728ae88a758c10954`  
		Last Modified: Fri, 24 Apr 2026 00:09:36 GMT  
		Size: 152.1 MB (152050389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38ae3590ffff1a4229c8be6a35933e8ed470a6e63dc16f519080c1baac95428`  
		Last Modified: Fri, 24 Apr 2026 01:13:21 GMT  
		Size: 85.7 MB (85656237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef18366bec24962815ecfd807ede585ffe62496207e73cd7f85aff9d06f4dd7`  
		Last Modified: Fri, 24 Apr 2026 01:13:17 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7215a2a827c43a64e68fc3eb99f9f23ddf0b541497d9e662802704f46dfff73b`  
		Last Modified: Fri, 24 Apr 2026 01:13:21 GMT  
		Size: 107.7 MB (107696665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606585aea1222c90957d01353a63b096cc4748a5b7d72f85828fb7fd8abe0ea9`  
		Last Modified: Fri, 24 Apr 2026 01:13:17 GMT  
		Size: 425.0 KB (425031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:86da3db4d96057a5ba7158bb39204cbae376d7957026d4e54b6b6b73eddc3ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11288464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:933913d19f6f6544d3c19a1205682070ce844b780fe34698e5cee02b3b241a3b`

```dockerfile
```

-	Layers:
	-	`sha256:046662125b2edcc737f7fe3729ad880d74e02728679eec3d6f7e96cd508cee1a`  
		Last Modified: Fri, 24 Apr 2026 01:13:18 GMT  
		Size: 11.3 MB (11267419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b2d74abcee6e6bb856dda781a652e97edd84e5f7e90c96c41d4ae3703ae5b2a`  
		Last Modified: Fri, 24 Apr 2026 01:13:17 GMT  
		Size: 21.0 KB (21045 bytes)  
		MIME: application/vnd.in-toto+json
