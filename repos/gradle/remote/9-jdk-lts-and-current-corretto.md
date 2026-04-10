## `gradle:9-jdk-lts-and-current-corretto`

```console
$ docker pull gradle@sha256:c699611555c2a51ab108160daa64c7330a0a57de19a5dc0668d10192a6b855aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-lts-and-current-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:ee191f9978411f28088578c420176e3c359135f3fa17b02c65a54f9a092647e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.9 MB (646945101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97849632f005bbd01ac701c6675e463bb61e9a4eaaca2eae226a6631b175ebe4`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:16 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:15:18 GMT
ARG version=25.0.2.10-1
# Fri, 03 Apr 2026 22:15:18 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:15:18 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:15:18 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:15:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 10 Apr 2026 16:56:10 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Fri, 10 Apr 2026 16:56:28 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 10 Apr 2026 16:56:28 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Fri, 10 Apr 2026 16:56:28 GMT
CMD ["gradle"]
# Fri, 10 Apr 2026 16:56:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 10 Apr 2026 16:56:28 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 10 Apr 2026 16:56:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 10 Apr 2026 16:56:28 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 10 Apr 2026 16:56:28 GMT
WORKDIR /home/gradle
# Fri, 10 Apr 2026 16:56:28 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 10 Apr 2026 16:56:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 10 Apr 2026 16:56:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 10 Apr 2026 16:56:31 GMT
USER gradle
# Fri, 10 Apr 2026 16:56:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 10 Apr 2026 16:56:31 GMT
USER root
```

-	Layers:
	-	`sha256:a2488c40110fb2b90385f44d9af6173894e14350935e38653aee164551cb70d6`  
		Last Modified: Thu, 02 Apr 2026 00:19:16 GMT  
		Size: 54.6 MB (54571303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4030c8d5ea3bcece5fef2fe49c6a99e8136494b402a9bd8cc173876dc309ddf`  
		Last Modified: Fri, 03 Apr 2026 22:15:43 GMT  
		Size: 189.2 MB (189188269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60b16ccd3b505189b7c0e15df6caa8bb99ba9ce798a713e0a3710dcd0c4e14d`  
		Last Modified: Fri, 10 Apr 2026 16:57:09 GMT  
		Size: 179.2 MB (179246157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0b92184f24643dfbbc0c1b49c14b8de298b5228fe66393633bf731eba83033`  
		Last Modified: Fri, 10 Apr 2026 16:57:06 GMT  
		Size: 86.1 MB (86103646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d5f6397e38fca1979deb785e90befad90b89c68b66aa98f1f85720fbce4f3f`  
		Last Modified: Fri, 10 Apr 2026 16:57:01 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2087f704f6f6c01e0c0e66a1630bb198c323b0cd3ab820f9e84ccdcf541ad4d`  
		Last Modified: Fri, 10 Apr 2026 16:57:08 GMT  
		Size: 137.8 MB (137808332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d48465091bf670ebb16e46fb6bc68f8c45368297fa7001619f1fddf597735fa`  
		Last Modified: Fri, 10 Apr 2026 16:57:02 GMT  
		Size: 25.6 KB (25604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:d8db42d0f503e1cbcf2e2ef6c20b079402500454bc59ec6541376528aaf6b113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11542920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18fd7ffd7e29fbf8ccbb1a85cf7a825abbb351404d8a8ca53c504cd5b55eae3`

```dockerfile
```

-	Layers:
	-	`sha256:14ba35c3373d1b8bacc83f7d6df5421e791d6c5123de54d876cf9afac8762397`  
		Last Modified: Fri, 10 Apr 2026 16:57:01 GMT  
		Size: 11.5 MB (11513410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60edcaccb3e390c425ad266340f9157df146be28dfc5cd84575bfa6ad110f89f`  
		Last Modified: Fri, 10 Apr 2026 16:57:01 GMT  
		Size: 29.5 KB (29510 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-lts-and-current-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:cc6b9a3785118ce778f5717a312adcd28af857ea1e013262cef2098c3ad8a1fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.1 MB (641091465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb8de929b33f4661e719baad90a3e3035623e7c81ee84294980842455bb62fa`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:40 GMT
ARG version=25.0.2.10-1
# Fri, 03 Apr 2026 22:14:40 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:14:40 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:14:40 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 10 Apr 2026 16:58:52 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Fri, 10 Apr 2026 16:59:14 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 10 Apr 2026 16:59:14 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Fri, 10 Apr 2026 16:59:14 GMT
CMD ["gradle"]
# Fri, 10 Apr 2026 16:59:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 10 Apr 2026 16:59:14 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 10 Apr 2026 16:59:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 10 Apr 2026 16:59:14 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 10 Apr 2026 16:59:14 GMT
WORKDIR /home/gradle
# Fri, 10 Apr 2026 16:59:14 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 10 Apr 2026 16:59:14 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 10 Apr 2026 16:59:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 10 Apr 2026 16:59:17 GMT
USER gradle
# Fri, 10 Apr 2026 16:59:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 10 Apr 2026 16:59:18 GMT
USER root
```

-	Layers:
	-	`sha256:cf8ff26f8ca2e7db6c1eb2c69aec532f89cf3016cc84f77de00b260ba62b2ffc`  
		Last Modified: Thu, 02 Apr 2026 00:19:15 GMT  
		Size: 53.4 MB (53442825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228d5c433fb7209c25bd1da18d7c83a79e304608f678efb8cf0f824894a3b8af`  
		Last Modified: Fri, 03 Apr 2026 22:15:06 GMT  
		Size: 187.1 MB (187089716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d8fac9f9fd7ad11cd3217a23e959e06adbd82771f434400051db38e15f2213`  
		Last Modified: Fri, 10 Apr 2026 16:59:57 GMT  
		Size: 177.1 MB (177115750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a4a967e3b69587e460a2c85e3ead586c5c66421df7ec7235de934cc6ef4077`  
		Last Modified: Fri, 10 Apr 2026 16:59:55 GMT  
		Size: 85.6 MB (85603718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10719506ca7ddeaa8754a33cb7803b1d9adb624b6b08444a728ab8a6d1533ec`  
		Last Modified: Fri, 10 Apr 2026 16:59:50 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09625fa30d6bc49ceb81378b7b2b9b266e09bca3e3ad3084c3d492323a590f18`  
		Last Modified: Fri, 10 Apr 2026 16:59:57 GMT  
		Size: 137.8 MB (137808334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc93da8374c3dbe2c5fa57e932b016e1ed1acc49103bf1c1808b949138dc921`  
		Last Modified: Fri, 10 Apr 2026 16:59:52 GMT  
		Size: 29.3 KB (29336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:3ae22e207957495bc5175436a65bcba699e6ff32b7692d52c62d1f33f5bf06a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11541708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38afa782d7fe90e3e08d51d7a8f4b03738d8b11034c7f4b11ca8d25d725ac5f8`

```dockerfile
```

-	Layers:
	-	`sha256:b04b224117afa32e095d023f62a08dfb720284e8ad45e3cadd3acbcd0c3a5775`  
		Last Modified: Fri, 10 Apr 2026 16:59:51 GMT  
		Size: 11.5 MB (11511879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ead40c68652fc13dfff23a3e302d5c53e3b3b7c2ef27d253ac8a7d6a1d6bba1`  
		Last Modified: Fri, 10 Apr 2026 16:59:50 GMT  
		Size: 29.8 KB (29829 bytes)  
		MIME: application/vnd.in-toto+json
