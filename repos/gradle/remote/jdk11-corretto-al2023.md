## `gradle:jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:d89e2e28ad716320536720596275866739bc32174d62afe3aa4ee7d8f9b28175
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:3bfd2b045076d09645d043e0901d3e578f7bd3b628a36d648ae5c1d5eba9f476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.3 MB (432343259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45ac7cc6e9c95ee6cd6434bdfb26acb3fafe2ef5bdb448b4812d43e04fe3dae`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:45 GMT
ARG version=11.0.31.11-1
# Mon, 04 May 2026 20:11:45 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:45 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 08 May 2026 17:48:25 GMT
CMD ["gradle"]
# Fri, 08 May 2026 17:48:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 17:48:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 08 May 2026 17:48:26 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 17:48:26 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 17:48:26 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 17:48:26 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 08 May 2026 17:48:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 08 May 2026 17:48:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 17:48:28 GMT
USER gradle
# Fri, 08 May 2026 17:48:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 17:48:28 GMT
USER root
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177f5f6694b7a14aaccd527d192e8e76c94dfecbb9fdd2f8693b660e84198ec2`  
		Last Modified: Mon, 04 May 2026 20:12:07 GMT  
		Size: 153.5 MB (153472514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e213dc39ccceded1d2899aad08ff85079f636fab2a99fe4a7996b011cc59500b`  
		Last Modified: Fri, 08 May 2026 17:48:57 GMT  
		Size: 86.2 MB (86168879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee063b08ddbe42b0c6685ba29fcffb7dca8d2e8caae66811a2a948fffa5294a`  
		Last Modified: Fri, 08 May 2026 17:48:53 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3031b0a6307392f1ce162d49cb75de2c4ceb1406ff0e24788a0f0d9b3419811c`  
		Last Modified: Fri, 08 May 2026 17:48:58 GMT  
		Size: 138.1 MB (138068532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed53d84b075d6922a84841cfab2ded852cceaa6b72a9b80913abaa31b5792b52`  
		Last Modified: Fri, 08 May 2026 17:48:53 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:afd91888a0d5822922a8792e00ffbcfba28ad0918bd5fa072617f94df29a520d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11397327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e906bff5501c4a8bd5525073c389097c0bbc9a4d2b282e43bcc78ba9c4d3f3b2`

```dockerfile
```

-	Layers:
	-	`sha256:a86e5fb3d5595088e564733f20e1c3b1b0452d310b7e9d79d197bac1a1fd97ce`  
		Last Modified: Fri, 08 May 2026 17:48:54 GMT  
		Size: 11.4 MB (11375663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:170c79b518501a286eb8112680466c3336d854cfea8e97dc4ef46fb3869343f7`  
		Last Modified: Fri, 08 May 2026 17:48:53 GMT  
		Size: 21.7 KB (21664 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:788f320b871fb669d9d3d2489ca38143cd277c701386d13f855ce6d111bad9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.3 MB (429296485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6556d2e249459e3dd1e9d943e6fe1b777ef09bcb9934ab0767a1a4041748cc01`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:32 GMT
ARG version=11.0.31.11-1
# Mon, 04 May 2026 20:11:32 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:32 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 08 May 2026 17:48:56 GMT
CMD ["gradle"]
# Fri, 08 May 2026 17:48:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 17:48:56 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 08 May 2026 17:48:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 17:48:56 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 17:48:56 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 17:48:56 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 08 May 2026 17:48:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 08 May 2026 17:49:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 17:49:18 GMT
USER gradle
# Fri, 08 May 2026 17:49:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 17:49:19 GMT
USER root
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838136ec5b6ab2b88d9936cfc6ef1491350d124ec8e540cec804c91561010d10`  
		Last Modified: Mon, 04 May 2026 20:11:53 GMT  
		Size: 152.1 MB (152051592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40022efb224aef9c37abef255be7d279a9e255888f2da06151b5ccab020fd0a5`  
		Last Modified: Fri, 08 May 2026 17:49:51 GMT  
		Size: 85.7 MB (85658373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c961dd93308dd315fb1eedf0c2d9ec6d3b422e9d097baee5dd12de260fdeec`  
		Last Modified: Fri, 08 May 2026 17:49:47 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b449f0b0fefb36beeea8ee95202bdd865520256a55434a73e4ec4f62cf8e179`  
		Last Modified: Fri, 08 May 2026 17:49:52 GMT  
		Size: 138.1 MB (138068532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7af55971420eeb24431695b17ad0c1156736d7f403b6cc503a807f1f63e6557`  
		Last Modified: Fri, 08 May 2026 17:49:47 GMT  
		Size: 59.5 KB (59537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:3b202a55f873a8182be2994e3cebd03bc8adb7471a0d14f6bf7cae64a1306325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11397368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5433936c5ca0bc5ced258318516fa22739258342cff881d2487a0c27d1e9c3d1`

```dockerfile
```

-	Layers:
	-	`sha256:2db9348abd4c089626290a69b4c581b86f7c3ef407c61e9df0a24522efa4114b`  
		Last Modified: Fri, 08 May 2026 17:49:48 GMT  
		Size: 11.4 MB (11375506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b318e30f3c5495d6dda95393c5f5474164f80ae2cb0b9e5c7e5683259e185901`  
		Last Modified: Fri, 08 May 2026 17:49:47 GMT  
		Size: 21.9 KB (21862 bytes)  
		MIME: application/vnd.in-toto+json
