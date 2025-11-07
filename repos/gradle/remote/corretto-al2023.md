## `gradle:corretto-al2023`

```console
$ docker pull gradle@sha256:70bcf04498f587a7193f0f2a6c0ad5accd9105f18b7e92995a57907611b1c0cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:5af7655f16dc115e14e691e4151f741eb9c58badfb1e43bf4482d02c38419f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.4 MB (464359830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bbcfd522e2274f52141fd819110ccd6ed7fe0be61e603f2080004632245c547`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 06 Nov 2025 22:15:48 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:15:48 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 23:12:37 GMT
ARG version=25.0.1.9-1
# Thu, 06 Nov 2025 23:12:37 GMT
ARG package_version=1
# Thu, 06 Nov 2025 23:12:37 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 23:12:37 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 23:12:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 07 Nov 2025 00:11:59 GMT
CMD ["gradle"]
# Fri, 07 Nov 2025 00:11:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 07 Nov 2025 00:11:59 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 07 Nov 2025 00:12:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 07 Nov 2025 00:12:00 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 07 Nov 2025 00:12:00 GMT
WORKDIR /home/gradle
# Fri, 07 Nov 2025 00:12:00 GMT
ENV GRADLE_VERSION=9.2.0
# Fri, 07 Nov 2025 00:12:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Fri, 07 Nov 2025 00:12:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 07 Nov 2025 00:12:02 GMT
USER gradle
# Fri, 07 Nov 2025 00:12:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 07 Nov 2025 00:12:03 GMT
USER root
```

-	Layers:
	-	`sha256:7857af70cc37714ae4781f1d58242c7667f933ef8be05b0636d2c50e756263b2`  
		Last Modified: Wed, 05 Nov 2025 21:09:20 GMT  
		Size: 54.0 MB (54000503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ff4d7205da8b8271c826b4d33c535dc537a1d647dc5aaac7acbed9389cdd36`  
		Last Modified: Fri, 07 Nov 2025 00:11:33 GMT  
		Size: 189.2 MB (189168050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f943349345670e12757fdb8eaad8b81cb7528def8d1e1793e978600607697ba9`  
		Last Modified: Fri, 07 Nov 2025 00:13:00 GMT  
		Size: 85.6 MB (85613032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab6549fdde8c4016ea07266a0ef1661f6d1f99b8a58318c8d6f47de9fd87690`  
		Last Modified: Fri, 07 Nov 2025 00:12:49 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fe5b4f02e80dc6f55cb07d281b645012f7f590cc708c45c49ce5e16272c243`  
		Last Modified: Fri, 07 Nov 2025 05:00:31 GMT  
		Size: 135.5 MB (135521657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7483beaae61be4f5b3abbced5e5927789909140eb3b3bde342f4f8d84747a9a7`  
		Last Modified: Fri, 07 Nov 2025 00:12:48 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:df77ba01525a0f5ff9282ea9c96e132e270e8f5a115ee4f5045bd70a38b1af57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11350173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bc386443252a07cc83a28f2e23adf09c129de91677be4d8833eae7c6795957`

```dockerfile
```

-	Layers:
	-	`sha256:b91eb9643039c95d46b7f7867009492520f0b8705f9b577652538d4d94554803`  
		Last Modified: Fri, 07 Nov 2025 03:23:38 GMT  
		Size: 11.3 MB (11327953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33564df88a7e3bfb760c39d90953bd426e84713873e9c57eccf6eb72ad31a995`  
		Last Modified: Fri, 07 Nov 2025 03:23:39 GMT  
		Size: 22.2 KB (22220 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:corretto-al2023` - linux; arm64 variant v8

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
		Last Modified: Fri, 07 Nov 2025 14:12:53 GMT  
		Size: 135.5 MB (135521656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473615ffc003c33b7250b0009a11e878569c776d908617697d5dd7ee24b9b8a1`  
		Last Modified: Thu, 06 Nov 2025 23:11:50 GMT  
		Size: 59.5 KB (59529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto-al2023` - unknown; unknown

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
