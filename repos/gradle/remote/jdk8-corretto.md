## `gradle:jdk8-corretto`

```console
$ docker pull gradle@sha256:8978f2136cd1c23c6ee4ca51ffb745b61ff18b81475587145719452c6e9cb158
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:7249fdfe8a82cc0820588e4f4683b8ee86eb54bd072538585da21c8f1a3fa208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.8 MB (587768668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:679061f1a54738e23cdd924c580ba7358d6376a6d31ab50769d3c9fbdf2fa4a5`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:39 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:39 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:11:48 GMT
ARG version=1.8.0_482.b08-1
# Tue, 27 Jan 2026 22:11:48 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:11:48 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:11:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 27 Jan 2026 23:13:08 GMT
CMD ["gradle"]
# Tue, 27 Jan 2026 23:13:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 Jan 2026 23:13:08 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 Jan 2026 23:13:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 27 Jan 2026 23:13:08 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 Jan 2026 23:13:08 GMT
WORKDIR /home/gradle
# Tue, 27 Jan 2026 23:13:08 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 27 Jan 2026 23:13:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 27 Jan 2026 23:13:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 Jan 2026 23:13:11 GMT
USER gradle
# Tue, 27 Jan 2026 23:13:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 27 Jan 2026 23:13:11 GMT
USER root
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0063fa961a83ea80f8505890b5b30904bbad941f436b6fd6a97260438d9779ba`  
		Last Modified: Tue, 27 Jan 2026 22:12:42 GMT  
		Size: 330.9 MB (330929315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c4d2ddb1440fffb085e464f9701ce706944d3abe96970981f0e9cb1daaaa7f`  
		Last Modified: Tue, 27 Jan 2026 23:13:51 GMT  
		Size: 65.4 MB (65370342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e002d28238043d79829253be57c9e3813f2981928719dfb1a2d5a2ce788a5624`  
		Last Modified: Tue, 27 Jan 2026 23:13:48 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e074e7f29d8a5e117d28d439812c1a34dbd7ba694c518e50196e0371012434`  
		Last Modified: Tue, 27 Jan 2026 23:13:53 GMT  
		Size: 137.4 MB (137388293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58a63b180986cdb7c442a90c57ce02b12c9d4a719cf8b7ead5c3c446716b0de`  
		Last Modified: Tue, 27 Jan 2026 23:13:49 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:41621d284518878f7a184df780b3be242df851cb599e55c63d598f58bd65ac73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18175374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362b246a4ed201cccff95ef96660fd46f061b3a0e626b8ae35b364a6b3ebbecf`

```dockerfile
```

-	Layers:
	-	`sha256:f5c883aa67055fac323eba72259f46065b9a28c04c435b1582e0842292851e8c`  
		Last Modified: Tue, 27 Jan 2026 23:13:49 GMT  
		Size: 18.2 MB (18153859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a81ca42204604a54c3d3e47828dd33db85f77186d09051c8f9acaf3805cae07`  
		Last Modified: Tue, 27 Jan 2026 23:13:48 GMT  
		Size: 21.5 KB (21515 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2c9fb1b51e939466a9f3b1023a2dc118aff530d462d3cf109d0426b6e38b01c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393834991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd510d43839d59acc4ec9dbdb72d5043d8cdc776cbdd002c05f47c1478554ae`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Jan 2026 21:24:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:24:49 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:05 GMT
ARG version=1.8.0_482.b08-1
# Tue, 27 Jan 2026 22:12:05 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:12:05 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 27 Jan 2026 23:12:39 GMT
CMD ["gradle"]
# Tue, 27 Jan 2026 23:12:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 Jan 2026 23:12:39 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 Jan 2026 23:12:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 27 Jan 2026 23:12:39 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 Jan 2026 23:12:39 GMT
WORKDIR /home/gradle
# Tue, 27 Jan 2026 23:12:39 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 27 Jan 2026 23:12:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 27 Jan 2026 23:12:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 Jan 2026 23:12:42 GMT
USER gradle
# Tue, 27 Jan 2026 23:12:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 27 Jan 2026 23:12:42 GMT
USER root
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded9aa2f6e708c1d1f17fd2a1840ac61815ced878bdcc03dada3d4e84e3a55f4`  
		Last Modified: Tue, 27 Jan 2026 22:12:24 GMT  
		Size: 118.0 MB (117962683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a1c74c66318a8e051a37ee981cd2b1d5c9c189f7d428d21377853483a8325b`  
		Last Modified: Tue, 27 Jan 2026 23:13:17 GMT  
		Size: 85.5 MB (85506173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be565ecdbf6ee2afdfc7929001e36db32c5baa1b092ae1b8d9646b12225fef6a`  
		Last Modified: Tue, 27 Jan 2026 23:13:10 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee590df37b7df947d697d9bdc3a16ce7dc7495517c078d2d51708c0bc8263805`  
		Last Modified: Tue, 27 Jan 2026 23:13:16 GMT  
		Size: 137.4 MB (137388293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8e88156e9f347202996c986a869397e1503d3d03b86266530b67e310f277dc`  
		Last Modified: Tue, 27 Jan 2026 23:13:10 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:adf7b10d580478a606ae48d64342e676e9b2a96ae526f7ee8f416906e2063cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11739760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b0db614a2d38ee77fdd48a9a3031d8033a96f18c37a4fdb8dc2cde720ce76f`

```dockerfile
```

-	Layers:
	-	`sha256:6e6914ef9d9661664f6f059682fc9c23b2dd6268fcbff1f2f97d577aab688961`  
		Last Modified: Tue, 27 Jan 2026 23:13:11 GMT  
		Size: 11.7 MB (11718047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43473cb47270bd647d959c5726b70fc4f6340a85396eb70bfcf2f31a617c17d`  
		Last Modified: Tue, 27 Jan 2026 23:13:10 GMT  
		Size: 21.7 KB (21713 bytes)  
		MIME: application/vnd.in-toto+json
