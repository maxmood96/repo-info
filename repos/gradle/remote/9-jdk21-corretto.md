## `gradle:9-jdk21-corretto`

```console
$ docker pull gradle@sha256:9cc9d0c0090a49986a9dce0e361eb74ebd78a595706cc628d780530e95ed154b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk21-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:64fede2954954571b552d33165ac0a60dbe305cdaf19156128750cdde504aedd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.3 MB (447339257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ef87d0407e2860f13689a86cca92b6b4897b72d9f08c7fc36bf5f75096ff8d`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:01 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:15:44 GMT
ARG version=21.0.10.7-1
# Mon, 02 Mar 2026 23:15:44 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:15:44 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:15:44 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:15:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 03 Mar 2026 00:11:46 GMT
CMD ["gradle"]
# Tue, 03 Mar 2026 00:11:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Mar 2026 00:11:46 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 03 Mar 2026 00:11:46 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 03 Mar 2026 00:11:46 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Mar 2026 00:11:46 GMT
WORKDIR /home/gradle
# Tue, 03 Mar 2026 00:11:46 GMT
ENV GRADLE_VERSION=9.3.1
# Tue, 03 Mar 2026 00:11:46 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Tue, 03 Mar 2026 00:11:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 03 Mar 2026 00:11:49 GMT
USER gradle
# Tue, 03 Mar 2026 00:11:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 03 Mar 2026 00:11:49 GMT
USER root
```

-	Layers:
	-	`sha256:2584a8e504dfaf493eadaafafbabd8b97f7cb5bbe3cb6a319fb37cf3c4335d86`  
		Last Modified: Thu, 19 Feb 2026 02:57:43 GMT  
		Size: 54.0 MB (54032840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3206d69860349aa25c9a225b33200274130746ada51655fcd2c5184f817fc0bb`  
		Last Modified: Mon, 02 Mar 2026 23:16:07 GMT  
		Size: 170.2 MB (170191580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590e0f1eb49e6c4424c4e14a2d1321db9cc2de4ba4c3cbc4ee18fbbf4cf6338e`  
		Last Modified: Tue, 03 Mar 2026 00:12:21 GMT  
		Size: 86.1 MB (86067850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32441df5bbfae0e042a1b1499615ebba54f58fcb823c58f38fb1b85376e59aa0`  
		Last Modified: Tue, 03 Mar 2026 00:12:18 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dacf14b9b5b2b9d63c430b8609a57118bf6d971b5d2cdc8695664f00b2eca69`  
		Last Modified: Tue, 03 Mar 2026 00:12:23 GMT  
		Size: 137.0 MB (137019697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2846c39a4aa351ce2acd18a18dddca1b56bd460a78f942334e5f8290ed5493`  
		Last Modified: Tue, 03 Mar 2026 00:12:17 GMT  
		Size: 25.6 KB (25611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:17dc161b1bec42f74131a65f09eafadb65f15f03343a7155112aba19bab9041a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11347872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe06ff6a6067490b8f985e5eb6bba4a6cf07717c4030cf9aa524593ef1a3266`

```dockerfile
```

-	Layers:
	-	`sha256:d9e5397672ad468a16325b3eb7961121ec20a41b26aee7b1c9bffe1a7f4d59f7`  
		Last Modified: Tue, 03 Mar 2026 00:12:18 GMT  
		Size: 11.3 MB (11326221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27984fa6c0c0de2805fd97340ded651419db17abc96d135be8c4c88c5696a925`  
		Last Modified: Tue, 03 Mar 2026 00:12:17 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6091e28db7223956bced3a497f6d60f0e15beeafe2d62b02128b5bed43c48fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.0 MB (444002978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77467abaf112ce7094c0ebaefe94049c67abaf55fde054e40ed533113b1e372`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:04 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:15:20 GMT
ARG version=21.0.10.7-1
# Mon, 02 Mar 2026 23:15:20 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:15:20 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:15:20 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:15:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 03 Mar 2026 00:19:54 GMT
CMD ["gradle"]
# Tue, 03 Mar 2026 00:19:54 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Mar 2026 00:19:54 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 03 Mar 2026 00:19:54 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 03 Mar 2026 00:19:54 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Mar 2026 00:19:54 GMT
WORKDIR /home/gradle
# Tue, 03 Mar 2026 00:19:54 GMT
ENV GRADLE_VERSION=9.3.1
# Tue, 03 Mar 2026 00:19:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Tue, 03 Mar 2026 00:19:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 03 Mar 2026 00:19:57 GMT
USER gradle
# Tue, 03 Mar 2026 00:19:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 03 Mar 2026 00:19:58 GMT
USER root
```

-	Layers:
	-	`sha256:9330fae67a20d9aa2569828674140d8b67d50cfd127cb99ba0f9be275d35f976`  
		Last Modified: Thu, 19 Feb 2026 02:57:42 GMT  
		Size: 52.9 MB (52941319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d70bc2bd9019cfe8ff01c08bf2c88be35366884c0a91749017cdbe727033a85`  
		Last Modified: Mon, 02 Mar 2026 23:15:44 GMT  
		Size: 168.5 MB (168466634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bcfbde420843721d5409e9a33fb4141dbbea88d3229767ef221c94de93e3b3`  
		Last Modified: Tue, 03 Mar 2026 00:20:28 GMT  
		Size: 85.5 MB (85544314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a28ad446696e32cb65cf84025c29df81ccf3672004b0a4357e587bff8f1c39f`  
		Last Modified: Tue, 03 Mar 2026 00:20:25 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1bd7780d3195560f7dd8b27d5d5a837576fbf25fa32394ecebcf1665dcc647`  
		Last Modified: Tue, 03 Mar 2026 00:20:29 GMT  
		Size: 137.0 MB (137019691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064307d8482d678a74a86049368925c568481f364e62c9695788d8776db7550e`  
		Last Modified: Tue, 03 Mar 2026 00:20:25 GMT  
		Size: 29.3 KB (29340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:1a17d05cb4669c4c38c8e7890ca6f29522d95ecb28453da8404392f71a7c35e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11347071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026d3c4bd5e01108bc5299ef41d9cca73ea26c425bb9aacb8c9053ccc91fd5f8`

```dockerfile
```

-	Layers:
	-	`sha256:09656470d2a3bc8fdefd7d8fdf7399ea1d719260b7c763aff96464d45b6515fd`  
		Last Modified: Tue, 03 Mar 2026 00:20:26 GMT  
		Size: 11.3 MB (11325223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adb29a4fd87a97ed98622584347a148ce46f53ff5c059d0af1e05b12110c12dc`  
		Last Modified: Tue, 03 Mar 2026 00:20:25 GMT  
		Size: 21.8 KB (21848 bytes)  
		MIME: application/vnd.in-toto+json
