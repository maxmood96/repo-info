## `gradle:corretto`

```console
$ docker pull gradle@sha256:bdb92765d3406365e3bdf8a51e8e4291b84d23283ba09932dbee4c850e64526a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:corretto` - linux; amd64

```console
$ docker pull gradle@sha256:6c2eacdb12e27ee9176dbf0ed906131b55e41c7be22d5d4beb5728cf68bb435f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.7 MB (464733444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e5b38afb31ded8507eb07b4b229014f4336175d0b2f6614896ce49ddfaafa4`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:30 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:30 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:17:22 GMT
ARG version=25.0.1.9-1
# Fri, 14 Nov 2025 02:17:22 GMT
ARG package_version=1
# Fri, 14 Nov 2025 02:17:22 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:17:22 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:17:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 14 Nov 2025 03:13:04 GMT
CMD ["gradle"]
# Fri, 14 Nov 2025 03:13:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 14 Nov 2025 03:13:04 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 14 Nov 2025 03:13:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 14 Nov 2025 03:13:05 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 14 Nov 2025 03:13:05 GMT
WORKDIR /home/gradle
# Fri, 14 Nov 2025 03:13:05 GMT
ENV GRADLE_VERSION=9.2.0
# Fri, 14 Nov 2025 03:13:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Fri, 14 Nov 2025 03:13:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 14 Nov 2025 03:13:07 GMT
USER gradle
# Fri, 14 Nov 2025 03:13:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 14 Nov 2025 03:13:08 GMT
USER root
```

-	Layers:
	-	`sha256:b64ab808fd6d460065684b4dcddcfaed550a0161a81a4f24db38100a7cef4ade`  
		Last Modified: Tue, 11 Nov 2025 02:45:03 GMT  
		Size: 54.0 MB (53976715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2515106f02bdcc6255531770f2551b0c5bcf3d036a76d0cca1e8333db900dde7`  
		Last Modified: Fri, 14 Nov 2025 03:12:41 GMT  
		Size: 189.1 MB (189144431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb91451c5c8499b17e842383122cd6d08f093da1cda8d3eb353c951984680717`  
		Last Modified: Fri, 14 Nov 2025 03:13:59 GMT  
		Size: 86.0 MB (86034054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d8f223b005172efab18dbebe485b9eaf2ae045481a320e8799dd2bd7f38f53`  
		Last Modified: Fri, 14 Nov 2025 03:13:52 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d81240ccec164c6e778d94ef5d5fa85148b689a36b88bafde424f8d63b3b5a7`  
		Last Modified: Fri, 14 Nov 2025 07:33:08 GMT  
		Size: 135.5 MB (135521655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a69d03a27afcf0115814a5eabdaaf2fd4d702124cfba7457ebef523d3b75063`  
		Last Modified: Fri, 14 Nov 2025 03:13:52 GMT  
		Size: 54.9 KB (54907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:126ea155df039606d2a6e82b949a500be70608a474f5404beead564e3bb4ac66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11371545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c0bdfcf0be40ec2e169ea9ceb8cfbd00e13738ddbd7597312269afd46b0708`

```dockerfile
```

-	Layers:
	-	`sha256:8b3027ca54412be181bb8c2d28c42c481feeb32f680df2c51375215fc7bd1231`  
		Last Modified: Fri, 14 Nov 2025 06:23:47 GMT  
		Size: 11.3 MB (11349325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:422db597d11fcd0448b863a6b26381f3fd27eb28d1135077e07983f2b3733017`  
		Last Modified: Fri, 14 Nov 2025 06:23:48 GMT  
		Size: 22.2 KB (22220 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:5ed93e7ebfaf62c1eba5d0d54c916cedd3913ca3bc67f825d9e80dca1d6be23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.1 MB (461059562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128ead509ede76ab3890f1b03ad42bd6e35056542a2351532a7a39859ac83235`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:24 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:21:28 GMT
ARG version=25.0.1.9-1
# Fri, 14 Nov 2025 02:21:28 GMT
ARG package_version=1
# Fri, 14 Nov 2025 02:21:28 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:21:28 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:21:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 14 Nov 2025 03:14:07 GMT
CMD ["gradle"]
# Fri, 14 Nov 2025 03:14:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 14 Nov 2025 03:14:07 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 14 Nov 2025 03:14:07 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 14 Nov 2025 03:14:07 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 14 Nov 2025 03:14:07 GMT
WORKDIR /home/gradle
# Fri, 14 Nov 2025 03:14:07 GMT
ENV GRADLE_VERSION=9.2.0
# Fri, 14 Nov 2025 03:14:07 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Fri, 14 Nov 2025 03:14:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 14 Nov 2025 03:14:10 GMT
USER gradle
# Fri, 14 Nov 2025 03:14:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 14 Nov 2025 03:14:10 GMT
USER root
```

-	Layers:
	-	`sha256:7bff4bcb213fec2224ece2638c720fadc39b0d185d5cfe08391265c58685a0ae`  
		Last Modified: Tue, 11 Nov 2025 02:45:05 GMT  
		Size: 52.9 MB (52876656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15de6176bffb9951ebe28648e7fc3c0cb3c2cc00d819513790f17ef97b6d240`  
		Last Modified: Fri, 14 Nov 2025 03:13:40 GMT  
		Size: 187.1 MB (187067280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a132ca1c7c373b4148b440900917a06b3e2f668e5353da8003666ea29e0249a9`  
		Last Modified: Fri, 14 Nov 2025 03:15:00 GMT  
		Size: 85.5 MB (85532765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37f8958f2001a64311f6248e2fd885ee5ba93605a1b9d8abbb9a21c0f3502d3`  
		Last Modified: Fri, 14 Nov 2025 03:14:51 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0ab1c371b564051e84b221c48b4b2281bedf2253c579f1478cf2b0ffaf07c9`  
		Last Modified: Fri, 14 Nov 2025 03:14:44 GMT  
		Size: 135.5 MB (135521655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a0ebfe338e98be48066290075414e4b020cc4760432e60df7aebbf22d81f61`  
		Last Modified: Fri, 14 Nov 2025 03:14:51 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:8d45bf129d4c914c8d50b2919b26fb48fadbf165d5da9fe8ef61929cd758ae0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11370803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1599535691da62761e4bd93a3a60425eeeb8474e5d891e6c8f0f1f04ae9c1ab4`

```dockerfile
```

-	Layers:
	-	`sha256:af1ca20d2a84bfcaeb93c5383ba011ff45f0803f67c784627c5adeed90deea0e`  
		Last Modified: Fri, 14 Nov 2025 06:23:56 GMT  
		Size: 11.3 MB (11348362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bbf35d7b57a0742bea4dda76d5eca654643d9515c79170d6c36f95ba41a3263`  
		Last Modified: Fri, 14 Nov 2025 06:23:57 GMT  
		Size: 22.4 KB (22441 bytes)  
		MIME: application/vnd.in-toto+json
