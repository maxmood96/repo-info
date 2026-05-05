## `gradle:8-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:a32ad29cf89e307886dcd41e95bd3a0a8db964334ff25ecfb34705ceb56c3e5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:2a8eed1005183d20dec50bf07379071bb265b4b9a1feef60173220dd539e5e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.3 MB (435342582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b492b6af32d8ec8e30aa58ed9e09911a4d44563128480da62b8a5a2aa4d002d`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:21 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:12:21 GMT
ARG package_version=1
# Mon, 04 May 2026 20:12:21 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:12:21 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 04 May 2026 20:42:06 GMT
CMD ["gradle"]
# Mon, 04 May 2026 20:42:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 04 May 2026 20:42:06 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 04 May 2026 20:42:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 04 May 2026 20:42:06 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 04 May 2026 20:42:06 GMT
WORKDIR /home/gradle
# Mon, 04 May 2026 20:42:06 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 04 May 2026 20:42:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 04 May 2026 20:42:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 04 May 2026 20:42:09 GMT
USER gradle
# Mon, 04 May 2026 20:42:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 04 May 2026 20:42:10 GMT
USER root
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be73c3ad3366393074a6eed7a125da1ff3733ec46325d456499b501d1e3f64ea`  
		Last Modified: Mon, 04 May 2026 20:12:44 GMT  
		Size: 157.2 MB (157155466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61dd592490887264d8d325fe50060b016cefdf52e807dde7d787f14317934b7`  
		Last Modified: Mon, 04 May 2026 20:42:41 GMT  
		Size: 86.2 MB (86165520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ce302568cc2848462303f1106a1d1272863fbcb4292257718d2c8b4ceeb995`  
		Last Modified: Mon, 04 May 2026 20:42:38 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19a621c758348dabafd36bd22dfefe333109bf01cdaa7b7b01b92e32ddb5839`  
		Last Modified: Mon, 04 May 2026 20:42:42 GMT  
		Size: 137.4 MB (137388268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4575f7dd34f188f70794c7d3e3cca5e03b19cdc90e016c7b181b4ac5144e20ea`  
		Last Modified: Mon, 04 May 2026 20:42:38 GMT  
		Size: 54.9 KB (54896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:9ad254c0ac891dc7fe474fce2ed9d5e6845e9659272c85ae43daedd4c83bc395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11371075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd50bd3ff995a16e2b242aef915cd4b77c2b6367c6c16099ac78c236f1c4535a`

```dockerfile
```

-	Layers:
	-	`sha256:e3f63ee2136b3199f245c9fac811c3a7a845f965c99e84790fb38eeb5df063dd`  
		Last Modified: Mon, 04 May 2026 20:42:38 GMT  
		Size: 11.4 MB (11350348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8609cb405cde21d2a0b48b857e5faa29e65b9a83f565955316c05cc5ed12783b`  
		Last Modified: Mon, 04 May 2026 20:42:37 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d51c068cbcb8a8608fb47df4be6744d2f2de80ca4ecdc29a53387dda8aefee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.5 MB (432549624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607d980639a2748c7fe05c19b1acc5bee17f8220fcdecd7436248e3fda4778ba`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:40 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:11:40 GMT
ARG package_version=1
# Mon, 04 May 2026 20:11:40 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:40 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 04 May 2026 20:42:14 GMT
CMD ["gradle"]
# Mon, 04 May 2026 20:42:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 04 May 2026 20:42:14 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 04 May 2026 20:42:15 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 04 May 2026 20:42:15 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 04 May 2026 20:42:15 GMT
WORKDIR /home/gradle
# Mon, 04 May 2026 20:42:15 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 04 May 2026 20:42:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 04 May 2026 20:42:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 04 May 2026 20:42:18 GMT
USER gradle
# Mon, 04 May 2026 20:42:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 04 May 2026 20:42:18 GMT
USER root
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322640e3642311a443627a18ff0c4fa0690feddc7c348c64a06d1c5fdac713ba`  
		Last Modified: Mon, 04 May 2026 20:12:03 GMT  
		Size: 156.0 MB (155989760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e09b247cc113dda885ee4e5aabb15b07532effeb13c4cef9ce6238cca4273c`  
		Last Modified: Mon, 04 May 2026 20:42:51 GMT  
		Size: 85.7 MB (85653622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b5ee42205da53c2195be4a210285a5dad6e04781c6b8ffc686d3d31918aa8e`  
		Last Modified: Mon, 04 May 2026 20:42:46 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85829f4a769fb3c38eaca6b16d9eab0afdc317c7541b924f3bf12ee661ba3dd3`  
		Last Modified: Mon, 04 May 2026 20:42:53 GMT  
		Size: 137.4 MB (137388268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea434791469baf8a12bb3f42eefe8fd0df88dd913a22bcedd6a3645942991dee`  
		Last Modified: Mon, 04 May 2026 20:42:47 GMT  
		Size: 59.5 KB (59525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:028f69aa70d41d5101b0bc87605c9bee53b11be52a44b578c9d18d74a99ece17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11370224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e086c6d634e2b376fc19673ea228e74fa6dd7f6780f6e7fd726828e63d96c25`

```dockerfile
```

-	Layers:
	-	`sha256:50384a66c99b9b9e0b47cdde94bad4d63438db58ce913f87f5a0bdba54637acf`  
		Last Modified: Mon, 04 May 2026 20:42:47 GMT  
		Size: 11.3 MB (11349324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82828ede2bce807d0ffd04c34f08e38120c4cb0e74a2eec87af3483e8a26ce63`  
		Last Modified: Mon, 04 May 2026 20:42:46 GMT  
		Size: 20.9 KB (20900 bytes)  
		MIME: application/vnd.in-toto+json
