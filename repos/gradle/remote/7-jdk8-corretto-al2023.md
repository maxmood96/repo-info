## `gradle:7-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:3e058c30f6e79e9432f7b4e95c5f894f934bcd8983373f78018cb227463ab986
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:a9e2587b40dca7c491804cbc587c9048d2cb28e21c7100fb5be0efb38a72bee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578814951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c33320b6431e9d1fa02654bc0eb40323ef5fd33270ab4ee1532dce7f25ef25c`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:34 GMT
ARG version=1.8.0_472.b08-1
# Thu, 15 Jan 2026 22:08:34 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:08:34 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:08:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 15 Jan 2026 23:09:13 GMT
CMD ["gradle"]
# Thu, 15 Jan 2026 23:09:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Jan 2026 23:09:13 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Jan 2026 23:09:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Jan 2026 23:09:13 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Jan 2026 23:09:13 GMT
WORKDIR /home/gradle
# Thu, 15 Jan 2026 23:09:13 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 15 Jan 2026 23:09:13 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 15 Jan 2026 23:09:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Jan 2026 23:09:15 GMT
USER gradle
# Thu, 15 Jan 2026 23:09:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Jan 2026 23:09:16 GMT
USER root
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:09:37 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9755244d844db1ed30b93a9af49eae47daeaa66b3de11403953bdb2262b76f3`  
		Last Modified: Thu, 15 Jan 2026 22:09:46 GMT  
		Size: 330.9 MB (330896662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f20ac4e6daac2855c30b01361ad7d2a0d43b0a7d1f97c5ce3f73c200c3588c`  
		Last Modified: Thu, 15 Jan 2026 23:10:17 GMT  
		Size: 65.4 MB (65370785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9443463f80c971c5069a99c772f2fe88d00e895679ff43c81018f82b470cc6cf`  
		Last Modified: Thu, 15 Jan 2026 23:10:05 GMT  
		Size: 1.9 KB (1942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4862ef783b5a6404c3c87c8961e4988afbc4eae0e9f34903296abf5f8c0a127e`  
		Last Modified: Thu, 15 Jan 2026 23:10:15 GMT  
		Size: 128.5 MB (128469413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23c1fff2fd9516d3b38c83bcf9de546a6f853b9a88a14ef2e268c44741d7df6`  
		Last Modified: Thu, 15 Jan 2026 23:10:05 GMT  
		Size: 54.9 KB (54913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:e28e06dafcefbbcad434e0449e18467d9e4e6059737e1ad196b1ee3d1a67e12c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18084723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4151884cde1dbd9b413f5848478fa21892a6432fe3cf655401d67fe3bd2c56ea`

```dockerfile
```

-	Layers:
	-	`sha256:687020ffd41efaf3e514b33062bb67f87f748f0e65471f663109c584c9b00ed5`  
		Last Modified: Fri, 16 Jan 2026 00:22:22 GMT  
		Size: 18.1 MB (18063860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e2c3055779b3c56c4d31ec296e64e23d391a6d2b9d7c478c201d15cdc8227aa`  
		Last Modified: Fri, 16 Jan 2026 00:22:23 GMT  
		Size: 20.9 KB (20863 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:733d5d4d2c775c75fccd34e20a8379c6af7570047ad6384385005edc52e26b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.8 MB (384847259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cdff1b20d5957f44314be295fc29574001b3724f9967724565878c405e62d6f`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:05 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:05 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:25:23 GMT
ARG version=1.8.0_472.b08-1
# Thu, 18 Dec 2025 01:25:23 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:25:23 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:25:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 18 Dec 2025 02:20:30 GMT
CMD ["gradle"]
# Thu, 18 Dec 2025 02:20:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Dec 2025 02:20:30 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Dec 2025 02:20:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Dec 2025 02:20:30 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Dec 2025 02:20:30 GMT
WORKDIR /home/gradle
# Thu, 18 Dec 2025 02:20:30 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 18 Dec 2025 02:20:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 18 Dec 2025 02:20:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Dec 2025 02:20:32 GMT
USER gradle
# Thu, 18 Dec 2025 02:20:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Dec 2025 02:20:33 GMT
USER root
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de3320244c0c5e8689ab3369d4e7efe9e9c7b32724b174d2d0f966d353d04e2`  
		Last Modified: Thu, 18 Dec 2025 01:25:58 GMT  
		Size: 117.9 MB (117927137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b097fbb6c1256468745966a70f021f3202dc39880ebffa5a44fcd1f5436d982`  
		Last Modified: Thu, 18 Dec 2025 02:21:19 GMT  
		Size: 85.5 MB (85516043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ae297617f75978a1e49ff146f6863c375dcea31dfce51f4440e7d6aa71f79c`  
		Last Modified: Thu, 18 Dec 2025 02:21:10 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5417b89536749267cc15adafab062a65ba271930062c67c3613ed88c8382a`  
		Last Modified: Thu, 18 Dec 2025 02:22:24 GMT  
		Size: 128.5 MB (128469418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b12e3ac7ed774bad03a66de713b45e45c72611af50e9543c63ffa286eba6075`  
		Last Modified: Thu, 18 Dec 2025 02:21:10 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:2869237a83e4a41431134e5e5e23736671635814bc4f60acd8ebf914312dc32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11649057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3453c0b83e4ca372261680cb19a9539c274cd1a9cfaaa9781230de2d88672aa2`

```dockerfile
```

-	Layers:
	-	`sha256:aa33a7493a7b334623e0fc75fbccd5c5303c23d12a5726fd3f61f4577271b93f`  
		Last Modified: Thu, 18 Dec 2025 06:19:14 GMT  
		Size: 11.6 MB (11628020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d4be7ad558f466a16763b8f48df549a36cf3b187c705b7c2e83b2f820229834`  
		Last Modified: Thu, 18 Dec 2025 06:19:15 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json
