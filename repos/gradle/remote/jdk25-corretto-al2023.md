## `gradle:jdk25-corretto-al2023`

```console
$ docker pull gradle@sha256:1e49f6cc4bf749c4c8d9df0584a2e4607232955fb7bc904f7ba376db71d4d84a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk25-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:534e5c3e7120887c6a9816de2cb7dd5f54c3b75b5082a86dac6bd3c347ae9979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.4 MB (464360519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d35a3dedc1dfe02e0328bf0d4b93068034c42d9496a7cba3f486faadb812e28`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Wed, 05 Nov 2025 01:07:15 GMT
ARG version=25.0.1.9-1
# Wed, 05 Nov 2025 01:07:15 GMT
ARG package_version=1
# Wed, 05 Nov 2025 01:07:15 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 05 Nov 2025 01:07:15 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:07:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 05 Nov 2025 04:49:15 GMT
CMD ["gradle"]
# Wed, 05 Nov 2025 04:49:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 05 Nov 2025 04:49:15 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 05 Nov 2025 04:49:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 05 Nov 2025 04:49:16 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 05 Nov 2025 04:49:16 GMT
WORKDIR /home/gradle
# Wed, 05 Nov 2025 04:49:16 GMT
ENV GRADLE_VERSION=9.2.0
# Wed, 05 Nov 2025 04:49:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Wed, 05 Nov 2025 04:49:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 05 Nov 2025 04:49:18 GMT
USER gradle
# Wed, 05 Nov 2025 04:49:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 05 Nov 2025 04:49:19 GMT
USER root
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c1f44d1f333eca771d4302a52c66b724492a443b32096a502dd680573ad6f9`  
		Last Modified: Wed, 05 Nov 2025 04:48:51 GMT  
		Size: 189.2 MB (189168084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97f7c4c472f7c6edd973fcfb0279fd9a12f8828ee4064cbc12f0cd04fb34901`  
		Last Modified: Wed, 05 Nov 2025 04:50:18 GMT  
		Size: 85.6 MB (85612952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2a05b763c8f735711acfba67a32d91877ee0bf5a10273ad896b4cbf9a4c657`  
		Last Modified: Wed, 05 Nov 2025 04:50:14 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a890cd64c30695692a74add781ad6acd86e8224b296763f3905601d9b502c7`  
		Last Modified: Wed, 05 Nov 2025 06:37:43 GMT  
		Size: 135.5 MB (135521660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e2c617ff2100384cf12fc7d45e91f63750dfb25bc6b25ae255516e2db71166`  
		Last Modified: Wed, 05 Nov 2025 04:50:14 GMT  
		Size: 54.9 KB (54903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:0362daff4a5762f8b64f4df65582f1cbeff0a31cb72f542bf9368e35bc73b05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11350173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc034adea7314c86c24ef78ffc274f9ae535aabb6540df8ae130d1e67ae687d`

```dockerfile
```

-	Layers:
	-	`sha256:3395c0117e7098292956e4b1858d133af97c1774a06f4204ae747fbfea29e5bb`  
		Last Modified: Wed, 05 Nov 2025 06:21:29 GMT  
		Size: 11.3 MB (11327953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d5450d10c2bd941d0f772f994ea90738c6557a45056006879b8dd2eb3877970`  
		Last Modified: Wed, 05 Nov 2025 06:21:30 GMT  
		Size: 22.2 KB (22220 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2bf9847cc0e5ea1e72e96f7737ab740d4336a72849db73269c0dfcff68c949aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.7 MB (460742209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73a6607ee2f40cbcb0f45c9fd963a7dfd30c9e8d36bcaa4d0d76e3b7f2b4884`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:14:39 GMT
ARG version=25.0.1.9-1
# Thu, 06 Nov 2025 22:14:39 GMT
ARG package_version=1
# Thu, 06 Nov 2025 22:14:39 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:14:39 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:14:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 06 Nov 2025 23:11:07 GMT
CMD ["gradle"]
# Thu, 06 Nov 2025 23:11:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 06 Nov 2025 23:11:07 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 06 Nov 2025 23:11:07 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 06 Nov 2025 23:11:07 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 06 Nov 2025 23:11:07 GMT
WORKDIR /home/gradle
# Thu, 06 Nov 2025 23:11:07 GMT
ENV GRADLE_VERSION=9.2.0
# Thu, 06 Nov 2025 23:11:07 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Thu, 06 Nov 2025 23:11:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 06 Nov 2025 23:11:09 GMT
USER gradle
# Thu, 06 Nov 2025 23:11:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 06 Nov 2025 23:11:10 GMT
USER root
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123460810639ecd99796c2d04c9c602287fe1bbb2613c2622aabd5176f1a2c40`  
		Last Modified: Thu, 06 Nov 2025 23:10:36 GMT  
		Size: 187.1 MB (187092407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9941f3f78ba4f1f51a56718f83d03da319524ce1031c0c4039c43b0b04f8ba54`  
		Last Modified: Thu, 06 Nov 2025 23:11:57 GMT  
		Size: 85.2 MB (85165250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce43ef991caae384c92e1c59c48088e0dad4f78e16cf9f93206c3d5fc1db334b`  
		Last Modified: Thu, 06 Nov 2025 23:11:49 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256c880637c42e9971c9ca216eb9011365a9c697c9db83077df6b540e99247c5`  
		Last Modified: Thu, 06 Nov 2025 23:11:44 GMT  
		Size: 135.5 MB (135521656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473615ffc003c33b7250b0009a11e878569c776d908617697d5dd7ee24b9b8a1`  
		Last Modified: Thu, 06 Nov 2025 23:11:50 GMT  
		Size: 59.5 KB (59529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:97d552c482656dcd78ef0383403b750760ca7700873f901e47358188d70e8182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11349431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176184d49a1c163c6e2caba89c96b9fcf2cdc57852a6a63612737e418461fe9a`

```dockerfile
```

-	Layers:
	-	`sha256:c08c67d226ce73447726e8207d8f636edb291caa68cbb85d101c22746ac4dcb3`  
		Last Modified: Fri, 07 Nov 2025 00:23:37 GMT  
		Size: 11.3 MB (11326990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2f54739edf56a3ed9d1e698dd2b4a56c0e9afcf70f272c3760983927de06140`  
		Last Modified: Fri, 07 Nov 2025 00:23:38 GMT  
		Size: 22.4 KB (22441 bytes)  
		MIME: application/vnd.in-toto+json
