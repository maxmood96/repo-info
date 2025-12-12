## `gradle:9-jdk21-corretto`

```console
$ docker pull gradle@sha256:703b16d2b5ca9e48d3356f0373a6d7cc15923b8f293b1f1e1e38049c01fba080
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk21-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:92af76c506cab9e373c4be39ebc2d7a13815d37d0861d110373119335939ad10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.8 MB (445773678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda5c04a47a27bf3c101470c7c7d21b3b8b76d1628e8f294024d5b8a2f79bf0a`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:09 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:09 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:12:59 GMT
ARG version=21.0.9.11-1
# Thu, 11 Dec 2025 22:12:59 GMT
ARG package_version=1
# Thu, 11 Dec 2025 22:12:59 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:12:59 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 11 Dec 2025 22:17:15 GMT
CMD ["gradle"]
# Thu, 11 Dec 2025 22:17:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 11 Dec 2025 22:17:15 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 11 Dec 2025 22:17:15 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 11 Dec 2025 22:17:15 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 11 Dec 2025 22:17:16 GMT
WORKDIR /home/gradle
# Thu, 11 Dec 2025 22:17:16 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 11 Dec 2025 22:17:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 11 Dec 2025 22:17:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 11 Dec 2025 22:17:18 GMT
USER gradle
# Thu, 11 Dec 2025 22:17:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 11 Dec 2025 22:17:18 GMT
USER root
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1983de2659861ae4a7da7c71a688d5396c76239007401de1c63944edec3edc`  
		Last Modified: Thu, 11 Dec 2025 22:17:35 GMT  
		Size: 170.2 MB (170185873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2871f902537c807d2a010f70d805d2a4aaba70ac7b5b10e4a8fcd86ad4947cb0`  
		Last Modified: Thu, 11 Dec 2025 22:18:04 GMT  
		Size: 86.0 MB (86020711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8752a59b827b7220781542aa512bfe896275f07f4daf8d0c207b0c81bf1c2e0`  
		Last Modified: Thu, 11 Dec 2025 22:17:53 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8086c96d0b00c5d2065f1128322244f6a5522f27ee9b16f34c5aa444971c20d`  
		Last Modified: Fri, 12 Dec 2025 00:26:06 GMT  
		Size: 135.5 MB (135522053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed265a2efbe3de872327ef5fb5c5a98583f2bc2c0a39bc2a92fbe78fc3522c9a`  
		Last Modified: Thu, 11 Dec 2025 22:17:53 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:389b501955f5e2bc727baceb0313cdc0c9b163d802360050e21415738203eaa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11358807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe34bacb24c124c7472098f7430b36e87a2cbc895c0d3694855e55cfc23627e`

```dockerfile
```

-	Layers:
	-	`sha256:caa97c70e14dbb0e3033f3f21bb4f6349378c3512f07079338f0668371f5a8f3`  
		Last Modified: Fri, 12 Dec 2025 00:23:46 GMT  
		Size: 11.3 MB (11337156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d005fa1e6bb23df65ee16147b9d4f54394c6ecc1085941dfb9f446fef97a91`  
		Last Modified: Fri, 12 Dec 2025 00:23:47 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:4e16abb66e66e0bcda063c0abba1cc4c7e45f778c0bba87c69f185016eab39f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.4 MB (442420112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f373875b8e87d2809a7223e143f0477883c0575f4c4fb687015692e62d71ee6`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 11 Dec 2025 21:45:58 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:45:58 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:03 GMT
ARG version=21.0.9.11-1
# Thu, 11 Dec 2025 22:11:03 GMT
ARG package_version=1
# Thu, 11 Dec 2025 22:11:03 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:11:03 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 11 Dec 2025 22:17:40 GMT
CMD ["gradle"]
# Thu, 11 Dec 2025 22:17:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 11 Dec 2025 22:17:40 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 11 Dec 2025 22:17:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 11 Dec 2025 22:17:40 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 11 Dec 2025 22:17:40 GMT
WORKDIR /home/gradle
# Thu, 11 Dec 2025 22:17:40 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 11 Dec 2025 22:17:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 11 Dec 2025 22:17:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 11 Dec 2025 22:17:43 GMT
USER gradle
# Thu, 11 Dec 2025 22:17:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 11 Dec 2025 22:17:43 GMT
USER root
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30afd867ba668143b0a83a28a417a56cea6bcf0208274f896e340f22161a864`  
		Last Modified: Thu, 11 Dec 2025 22:17:44 GMT  
		Size: 168.4 MB (168441547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542189056aef9ea37a0c8a323ef4456b716882022f2b6f98f6f9f9034d5ec867`  
		Last Modified: Thu, 11 Dec 2025 22:18:34 GMT  
		Size: 85.5 MB (85521940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd20990bbae44d065255b2e265f95d30e272c4ebd2e9bdac0f5089e415f5044d`  
		Last Modified: Thu, 11 Dec 2025 22:18:26 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01a642b88121c0bc98d62f9b88106e91703ee9cd14c2a144fc0515feeb5244a`  
		Last Modified: Fri, 12 Dec 2025 01:05:07 GMT  
		Size: 135.5 MB (135521967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e835de9faa0ba2c526defe973a82df2d903fa8fdedd07282329a5c28149fe90`  
		Last Modified: Thu, 11 Dec 2025 22:18:26 GMT  
		Size: 59.5 KB (59525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:796078a41b55c17b0cca475121a1d4ca04cbccc925d3535031f0714c26051c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11358006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8130fb627d39f5bad37de7675ba455052562d4cceb2c30ba6816ced96b85f636`

```dockerfile
```

-	Layers:
	-	`sha256:fa016ceb8710db7287ab1c1809f1fd2c44a4c4d1f1686db5be079b2b1a15d7c2`  
		Last Modified: Fri, 12 Dec 2025 00:23:57 GMT  
		Size: 11.3 MB (11336158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08af8e9ff06680f104495d2bdf30a78628703ee5fb3e4acfbc448baf9a65ad4f`  
		Last Modified: Fri, 12 Dec 2025 00:23:59 GMT  
		Size: 21.8 KB (21848 bytes)  
		MIME: application/vnd.in-toto+json
