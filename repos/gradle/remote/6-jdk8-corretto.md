## `gradle:6-jdk8-corretto`

```console
$ docker pull gradle@sha256:509b58d9a0f557aa8da2dc799733f8340ab80cdc4d8d451645337b3138656a1d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:f64967f831c113247c427d8b0347a9a9840bf9650bb385dc88c31029b91ca25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.1 MB (559121840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25bbd6212f876f00b08f853156c0e6b2c5cfabff2d6db96b05ef563ea62ec143`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:15 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:15 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:14:47 GMT
ARG version=1.8.0_492.b09-2
# Tue, 16 Jun 2026 01:14:47 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:14:47 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:14:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 16 Jun 2026 02:20:51 GMT
CMD ["gradle"]
# Tue, 16 Jun 2026 02:20:51 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 16 Jun 2026 02:20:51 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 16 Jun 2026 02:20:51 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 16 Jun 2026 02:20:51 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 16 Jun 2026 02:20:51 GMT
WORKDIR /home/gradle
# Tue, 16 Jun 2026 02:20:51 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 16 Jun 2026 02:20:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 16 Jun 2026 02:20:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 16 Jun 2026 02:20:53 GMT
USER gradle
# Tue, 16 Jun 2026 02:20:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 16 Jun 2026 02:20:54 GMT
USER root
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a9338e5bb90c4ef8359da9c0e3f2d72978a857c7e3798beaca7a77fdf7adba`  
		Last Modified: Tue, 16 Jun 2026 01:15:43 GMT  
		Size: 330.8 MB (330824841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58ad3fb2bf4bbf1bcae11df5d2e940ecf38aa0408652a3fd065f36af7a8ddfe`  
		Last Modified: Tue, 16 Jun 2026 02:21:36 GMT  
		Size: 65.6 MB (65595917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb4febc44494934600ab8e7aab538efe2c0a1ee78ec56e99b97f1c3af1ceb22`  
		Last Modified: Tue, 16 Jun 2026 02:21:32 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4071306061ba9ce50badfe57da6af010c11218c850fce2aec59239b0b7254c00`  
		Last Modified: Tue, 16 Jun 2026 02:21:37 GMT  
		Size: 107.7 MB (107696664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4abcefd5af198cccbdd69c856f50521c4437d7a31de0f36afb6d9a954b624e5`  
		Last Modified: Tue, 16 Jun 2026 02:21:32 GMT  
		Size: 431.3 KB (431286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:fabd2b1248a5021929fedf1f58aa349970772ba6031a1783ab7b93fe11bf5463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18076528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f859e53689f0a55576cddb3025081d019dda032765decdcded7598979afe68`

```dockerfile
```

-	Layers:
	-	`sha256:212431be2c737cc99fdabadd6f9162f9f74860183cc7e36df365ee8c41d23506`  
		Last Modified: Tue, 16 Jun 2026 02:21:33 GMT  
		Size: 18.1 MB (18055663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44097b13258d014f16ec96031b69eb1eed750f19ca72e301c2f2fbf7f0c04365`  
		Last Modified: Tue, 16 Jun 2026 02:21:32 GMT  
		Size: 20.9 KB (20865 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:225ab2a9c1f264cf7269c8d285029153888b6751dd58786b28c09f1d1fc38763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365253790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f588855eb3b201ac9d2a884e7596fddcc862b3885fb4920931fa529aac1320f`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:26 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:15:51 GMT
ARG version=1.8.0_492.b09-2
# Tue, 16 Jun 2026 01:15:51 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:15:51 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:15:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 16 Jun 2026 02:21:27 GMT
CMD ["gradle"]
# Tue, 16 Jun 2026 02:21:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 16 Jun 2026 02:21:27 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 16 Jun 2026 02:21:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 16 Jun 2026 02:21:28 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 16 Jun 2026 02:21:28 GMT
WORKDIR /home/gradle
# Tue, 16 Jun 2026 02:21:28 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 16 Jun 2026 02:21:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 16 Jun 2026 02:21:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 16 Jun 2026 02:21:30 GMT
USER gradle
# Tue, 16 Jun 2026 02:21:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 16 Jun 2026 02:21:30 GMT
USER root
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643c45da3b90b926ec08b5c1cfaceec12449a27d0b19cdaa1064c36dcf3e921b`  
		Last Modified: Tue, 16 Jun 2026 01:16:11 GMT  
		Size: 118.0 MB (117955739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aec361cca0a85ef8e9ec4e74218050c3f65f5ab6385a7f6fcb964f8285319c7`  
		Last Modified: Tue, 16 Jun 2026 02:22:00 GMT  
		Size: 85.7 MB (85716858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08762cdc19bf25bc34e749a018cda2e1c9c6fbff8354b57584c572e6e66fdecc`  
		Last Modified: Tue, 16 Jun 2026 02:21:57 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc203df76f016c177b5fce391d0c34d1bf3dbd4d409dccefcdbffb44e0e680`  
		Last Modified: Tue, 16 Jun 2026 02:22:00 GMT  
		Size: 107.7 MB (107696664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207a836301ad144a673f59815f3de8755a3d41a94e1dc5ad3f1b40a9c6edf9fa`  
		Last Modified: Tue, 16 Jun 2026 02:21:57 GMT  
		Size: 425.0 KB (425021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:0068035fe6e2999df5ceccec2dbc6bb0d0bd7fa09087302e6a175cb75fc41c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11640853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a8167d7417732617fd4acb60914205ae77fc54e3f6a3197280c77b048b0249`

```dockerfile
```

-	Layers:
	-	`sha256:322864815773f8b549e0b341f435c762c5950227345e420b6997ad270fecb159`  
		Last Modified: Tue, 16 Jun 2026 02:21:58 GMT  
		Size: 11.6 MB (11619815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b2981bac521d55208973a8916e54aa521c9618b70d40b23c774407890da6ee0`  
		Last Modified: Tue, 16 Jun 2026 02:21:57 GMT  
		Size: 21.0 KB (21038 bytes)  
		MIME: application/vnd.in-toto+json
