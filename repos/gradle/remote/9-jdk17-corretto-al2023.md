## `gradle:9-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:d1970384baf6aa1da7f4c0cb648607c72407e3ebd90b97f1902815db2e432c1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:cde28c3f28eb1f14ca8bf9f852fcc58e55eef6f9e184246659f832346c8a1db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.1 MB (434056530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d30d0109021ebf3b49937c7817aa3cf04eaa94ad5e1ad54363a6cbad54d1df1`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:01 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:13:35 GMT
ARG version=17.0.18.9-1
# Mon, 02 Mar 2026 23:13:35 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:13:35 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:13:35 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:13:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 03 Mar 2026 00:11:54 GMT
CMD ["gradle"]
# Tue, 03 Mar 2026 00:11:54 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Mar 2026 00:11:54 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 03 Mar 2026 00:11:54 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 03 Mar 2026 00:11:54 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Mar 2026 00:11:54 GMT
WORKDIR /home/gradle
# Tue, 03 Mar 2026 00:11:54 GMT
ENV GRADLE_VERSION=9.3.1
# Tue, 03 Mar 2026 00:11:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Tue, 03 Mar 2026 00:11:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 03 Mar 2026 00:11:57 GMT
USER gradle
# Tue, 03 Mar 2026 00:11:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 03 Mar 2026 00:11:57 GMT
USER root
```

-	Layers:
	-	`sha256:2584a8e504dfaf493eadaafafbabd8b97f7cb5bbe3cb6a319fb37cf3c4335d86`  
		Last Modified: Thu, 19 Feb 2026 02:57:43 GMT  
		Size: 54.0 MB (54032840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291656abe10718a5b7ecb3affcd502d6d49aac432bab42c4affe10d8907b4b47`  
		Last Modified: Mon, 02 Mar 2026 23:13:54 GMT  
		Size: 156.9 MB (156911090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4e2ce5e6d2f98dfdfeddedbd7446ef57cc7fbc679dd5324e3944b91f2f6905`  
		Last Modified: Tue, 03 Mar 2026 00:12:28 GMT  
		Size: 86.1 MB (86065622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66df4af62f0a388c0549170050d014459eff42f19b3c058c79f3b1d740f5342`  
		Last Modified: Tue, 03 Mar 2026 00:12:24 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339211370af1905547c420ddcd2ffdd1528cbea88045d9a983ad5854f83fc4b8`  
		Last Modified: Tue, 03 Mar 2026 00:12:29 GMT  
		Size: 137.0 MB (137019693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9cb9ae946289c489ea4a4cb2b9c1954c1faa3a21aea65da4710e96637ce0ab`  
		Last Modified: Tue, 03 Mar 2026 00:12:25 GMT  
		Size: 25.6 KB (25605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:fa255e9cc28625bb5754d0c01b2a4f7bc6224b7950cefc7fe9cf3157cf94813d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11345292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ab644b25a1ae4cdb3d3384138a273eec3bc220358262e4df7eeebec43f9bb7`

```dockerfile
```

-	Layers:
	-	`sha256:ca19866392a76a9d787ee68b48d0c996d915b5fac13411c085d5b5a017b8c88b`  
		Last Modified: Tue, 03 Mar 2026 00:12:25 GMT  
		Size: 11.3 MB (11323795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d9b4ab5e982c33122e8c5a03850150e9f258ca52a960595d0185675243a10d`  
		Last Modified: Tue, 03 Mar 2026 00:12:24 GMT  
		Size: 21.5 KB (21497 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:bdc7558e69bd5e90431570f763072e60821c6b3899746e18f9b9aa6f284eaffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.3 MB (431263869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7119099b66ecef36ce691b92fed37f31d8ebadad0119367d9d8a875fb0da6bbf`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:04 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:14:40 GMT
ARG version=17.0.18.9-1
# Mon, 02 Mar 2026 23:14:40 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:14:40 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:14:40 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:14:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 03 Mar 2026 00:12:10 GMT
CMD ["gradle"]
# Tue, 03 Mar 2026 00:12:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Mar 2026 00:12:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 03 Mar 2026 00:12:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 03 Mar 2026 00:12:10 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Mar 2026 00:12:10 GMT
WORKDIR /home/gradle
# Tue, 03 Mar 2026 00:12:10 GMT
ENV GRADLE_VERSION=9.3.1
# Tue, 03 Mar 2026 00:12:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Tue, 03 Mar 2026 00:12:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 03 Mar 2026 00:12:13 GMT
USER gradle
# Tue, 03 Mar 2026 00:12:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 03 Mar 2026 00:12:13 GMT
USER root
```

-	Layers:
	-	`sha256:9330fae67a20d9aa2569828674140d8b67d50cfd127cb99ba0f9be275d35f976`  
		Last Modified: Thu, 19 Feb 2026 02:57:42 GMT  
		Size: 52.9 MB (52941319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458a2c883ef0e813dd59cc98f7ab9fa2c67d320d0117be74523be410b68ca3ed`  
		Last Modified: Mon, 02 Mar 2026 23:15:03 GMT  
		Size: 155.7 MB (155727670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf48c883cedb0a67086e7f1b5e153cf1c26767dc100949311336271c167b1406`  
		Last Modified: Tue, 03 Mar 2026 00:12:45 GMT  
		Size: 85.5 MB (85544180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e6d3555d9d4f05eb6f581fa8c89df8e9bab4698a3dbb5ac5c5459dbe4bf4fe`  
		Last Modified: Tue, 03 Mar 2026 00:12:42 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54068eadee2e58b7e9b93dd07c937b1fbc280eef4335dcfdd2be638e69e7c1f`  
		Last Modified: Tue, 03 Mar 2026 00:12:47 GMT  
		Size: 137.0 MB (137019693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a10f0ddabd26811a060e763be86ef23ed87767a160807368355d90def3ce14`  
		Last Modified: Tue, 03 Mar 2026 00:12:42 GMT  
		Size: 29.3 KB (29330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:393d1b4e11c9ee2eed4b8d877ddd00538ac55b880c68f5908e75912d089dbc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11344488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39e15782358c793ad9eed7826f34dc2f508003938e58b0667f1aa94a177f746`

```dockerfile
```

-	Layers:
	-	`sha256:fd0ae60105a364f37a4cc75fd8c0e6ff7f4b3367f09df2b50f4e72a23edb0ddd`  
		Last Modified: Tue, 03 Mar 2026 00:12:42 GMT  
		Size: 11.3 MB (11322794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81d850e59437b7b2c62cbc81a50d5912b2260e0af8af41b810c3bc8a127b9093`  
		Last Modified: Tue, 03 Mar 2026 00:12:42 GMT  
		Size: 21.7 KB (21694 bytes)  
		MIME: application/vnd.in-toto+json
