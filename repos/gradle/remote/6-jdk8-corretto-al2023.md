## `gradle:6-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:6ff354f74ac86bed101ea7b14142f1d0e080b56676b367791327f220304dc993
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:8947398fdeb060d7080054506da10582153e564793fb87055764a6930e6ee25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.0 MB (557977871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9c2b3aa2f794260ac9f2f3a93a2bcdb2c7449555b83e3239c01b83213b35ed`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 06 Nov 2025 22:15:48 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:15:48 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 23:12:14 GMT
ARG version=1.8.0_472.b08-1
# Thu, 06 Nov 2025 23:12:14 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 23:12:14 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 23:12:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 07 Nov 2025 00:13:19 GMT
CMD ["gradle"]
# Fri, 07 Nov 2025 00:13:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 07 Nov 2025 00:13:19 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 07 Nov 2025 00:13:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 07 Nov 2025 00:13:19 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 07 Nov 2025 00:13:19 GMT
WORKDIR /home/gradle
# Fri, 07 Nov 2025 00:13:19 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 07 Nov 2025 00:13:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 07 Nov 2025 00:13:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 07 Nov 2025 00:13:22 GMT
USER gradle
# Fri, 07 Nov 2025 00:13:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 07 Nov 2025 00:13:22 GMT
USER root
```

-	Layers:
	-	`sha256:7857af70cc37714ae4781f1d58242c7667f933ef8be05b0636d2c50e756263b2`  
		Last Modified: Wed, 05 Nov 2025 21:09:20 GMT  
		Size: 54.0 MB (54000503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a466983e04f75b0240d48e3a95c546707491d065df8baa3200522fb42bb1f95`  
		Last Modified: Fri, 07 Nov 2025 00:12:03 GMT  
		Size: 330.9 MB (330868155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a490b7a178d58fc316e7e3e2aeba5d28342bf3cc4bc22f667ef7bc1d4c3fe292`  
		Last Modified: Fri, 07 Nov 2025 00:14:21 GMT  
		Size: 65.0 MB (64979301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ae5b0a5b6947c6efff8971faf37fc711c11987388856617ab3cdf8f5e2db3d`  
		Last Modified: Fri, 07 Nov 2025 00:14:11 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8714f05331d30c21e81b1c3698014af256af2f241864efb42e6c2f8cdde9e76c`  
		Last Modified: Fri, 07 Nov 2025 00:14:23 GMT  
		Size: 107.7 MB (107696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ec31c1f3e3cc5d07c63b8f24f4d697f12bc269a03aaa6ec3927268c6fe41ed`  
		Last Modified: Fri, 07 Nov 2025 00:14:12 GMT  
		Size: 431.3 KB (431272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:2764e476a1f9c7ea493c8791fcb533e9dc7cbbf3e02892025c11ce30ea977df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18045435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f37a073927fc32084d88e81e111f72837417e18cc0e7b3da5b2c57028cf5134`

```dockerfile
```

-	Layers:
	-	`sha256:0ce0bfa1be1e23b0a1bea5f4366a766f357c7c4b60aad9dfaa4281dc1729cc00`  
		Last Modified: Fri, 07 Nov 2025 03:17:36 GMT  
		Size: 18.0 MB (18024570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29e97f973aeb99388a49d4f1d40ff296335aeb53ccd78b60384f635573c47811`  
		Last Modified: Fri, 07 Nov 2025 03:17:38 GMT  
		Size: 20.9 KB (20865 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9f1a37af5fbf8de0a75be54bb155186dc92abee83947add692574a13d48e4266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.1 MB (364136768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e70bd7dd4d3b8a069a1a2e0d7e585c2051a2555d3e4b98eef60e81d269c938`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:11:25 GMT
ARG version=1.8.0_472.b08-1
# Thu, 06 Nov 2025 22:11:25 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:11:25 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:11:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 06 Nov 2025 23:13:15 GMT
CMD ["gradle"]
# Thu, 06 Nov 2025 23:13:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 06 Nov 2025 23:13:15 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 06 Nov 2025 23:13:15 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 06 Nov 2025 23:13:15 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 06 Nov 2025 23:13:15 GMT
WORKDIR /home/gradle
# Thu, 06 Nov 2025 23:13:15 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 06 Nov 2025 23:13:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 06 Nov 2025 23:13:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 06 Nov 2025 23:13:18 GMT
USER gradle
# Thu, 06 Nov 2025 23:13:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 06 Nov 2025 23:13:18 GMT
USER root
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d1f499ea2be350aeea557e5a54efc605e09542e2e0eb46c78b5696360c7ce2`  
		Last Modified: Thu, 06 Nov 2025 22:12:07 GMT  
		Size: 118.0 MB (117956781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77f637ff8ed0f0b358629c1eab166b88133a254e92e64e89530256d1578ea8b`  
		Last Modified: Thu, 06 Nov 2025 23:14:09 GMT  
		Size: 85.2 MB (85154934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb10f806a8b5a9b2851f6327e41544109c07c6855c5e1001270a237eef3bcb0d`  
		Last Modified: Thu, 06 Nov 2025 23:13:57 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaf4c83d05e8ecbd31c4a4533d41bd9d62c5fadc031e7dbfe2566b120d35fcd`  
		Last Modified: Thu, 06 Nov 2025 23:14:15 GMT  
		Size: 107.7 MB (107696664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e230431d43f1a196007e93454c945f95a802ac2853aa84e3b3bf31012555901`  
		Last Modified: Thu, 06 Nov 2025 23:13:58 GMT  
		Size: 425.0 KB (425024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:9e7019cea89d770371a5a82da6e1fa23da64d9e39c6feeb238d1329a7ba0bef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11609773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3d6b3caccc155b882c4d94cdf65cb794a7ddaa39c2d75579604b52efc312cf`

```dockerfile
```

-	Layers:
	-	`sha256:7541f5fa163fe944d7d6d8bbe139cd1dbf38a8379fe32574fb0c0b5971442c92`  
		Last Modified: Fri, 07 Nov 2025 00:17:52 GMT  
		Size: 11.6 MB (11588736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d37c914f2c854abc59bd0511085aebebd393da048bc672a27ca37bd1edd4283e`  
		Last Modified: Fri, 07 Nov 2025 00:17:56 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json
