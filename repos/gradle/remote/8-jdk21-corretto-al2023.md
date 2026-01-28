## `gradle:8-jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:9749aeb6e21df69f663ae2a353b9ffa6b754cf69e8a3d83eed3bd7081ebbf6de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:f3ef54c0628f45d7f61b1578b823c38f038558ed584b07e986aa2b66f41b5ff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.7 MB (447698218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a350e1c17fbf8ff7fce48b43a7b227a0f4c364d8da4bce921641180137b1d7`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:39 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:39 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:11:36 GMT
ARG version=21.0.10.7-1
# Tue, 27 Jan 2026 22:11:36 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:11:36 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:11:36 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:11:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 27 Jan 2026 23:12:24 GMT
CMD ["gradle"]
# Tue, 27 Jan 2026 23:12:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 Jan 2026 23:12:24 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 Jan 2026 23:12:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 27 Jan 2026 23:12:24 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 Jan 2026 23:12:24 GMT
WORKDIR /home/gradle
# Tue, 27 Jan 2026 23:12:24 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 27 Jan 2026 23:12:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 27 Jan 2026 23:12:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 Jan 2026 23:12:27 GMT
USER gradle
# Tue, 27 Jan 2026 23:12:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 27 Jan 2026 23:12:27 GMT
USER root
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6b2affcaf3319a5d68a22e24f47aa31f4eb325a0d9638c8931197c613f6a33`  
		Last Modified: Tue, 27 Jan 2026 22:11:57 GMT  
		Size: 170.2 MB (170196234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bcf1ebfbb75acda39a518e6311a6ec417210b305f798e8bf590e5045269a2a`  
		Last Modified: Tue, 27 Jan 2026 23:12:56 GMT  
		Size: 86.0 MB (86033300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef672f84a272c054d0b1f15f5613510661bc033a424d603c097d70c8f4a2abe`  
		Last Modified: Tue, 27 Jan 2026 23:12:52 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc61004fc490475f6e10fb7850e7c1a02b0420884b245b6ee74e9658e0ef343`  
		Last Modified: Tue, 27 Jan 2026 23:12:56 GMT  
		Size: 137.4 MB (137388269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bb07704c160bd3bd4984eb631b6a6b19941fe23e11bd6d0bf687022eba5799`  
		Last Modified: Tue, 27 Jan 2026 23:12:52 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:fdf3dfefeea2466793d47917edfecfe79ba2a6780ef16f5f7b087a445eece256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11363137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c43bccd86dcb7848f45851c31835372920e893646a8ecd8e52974bf866028e1`

```dockerfile
```

-	Layers:
	-	`sha256:24eb195599010f1dc80e6ab12f6f71dec205331d1cd9ecf19e8321902987c758`  
		Last Modified: Tue, 27 Jan 2026 23:12:53 GMT  
		Size: 11.3 MB (11342256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd56ce6a1b6a69cd1884b35746766e0a89b75e7a5fbea051a584a8dcf3de6ea`  
		Last Modified: Tue, 27 Jan 2026 23:12:52 GMT  
		Size: 20.9 KB (20881 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:5e93edf7aa93572fbe9ae38ba2f4acc15adb9c33438bd2e651f77dd6ca907607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.3 MB (444348531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab36f0745ac413fbcdf860f8defdcafd41a167a058e2977e6ab86816327e586`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Jan 2026 21:24:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:24:49 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:44 GMT
ARG version=21.0.10.7-1
# Tue, 27 Jan 2026 22:12:44 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:12:44 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:12:44 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 27 Jan 2026 23:12:38 GMT
CMD ["gradle"]
# Tue, 27 Jan 2026 23:12:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 Jan 2026 23:12:38 GMT
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
# Tue, 27 Jan 2026 23:12:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 Jan 2026 23:12:41 GMT
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
	-	`sha256:33f46fcbcc478da5af0cdc2bd8402eaa8b18d5383a839c1f65a081622797b132`  
		Last Modified: Tue, 27 Jan 2026 22:13:08 GMT  
		Size: 168.5 MB (168468866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1dab280f58be27e7ba2fb5edf0cfe570c8e0c2c36b343dba4fb312f935fe73`  
		Last Modified: Tue, 27 Jan 2026 23:13:12 GMT  
		Size: 85.5 MB (85513541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0a13a3aed9c2b5cdb86cf6f5339826036e7761c4c5f538992c7cb776557d52`  
		Last Modified: Tue, 27 Jan 2026 23:13:09 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dce29c895112b4e8ccdae78a80169c46a7e0e337ea61ee611159c78c49cb83e`  
		Last Modified: Tue, 27 Jan 2026 23:13:13 GMT  
		Size: 137.4 MB (137388267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90c3195f912696084e13c6a3834ab9e47c2d5d9849b2e76209ddf0d608bc21`  
		Last Modified: Tue, 27 Jan 2026 23:13:09 GMT  
		Size: 59.5 KB (59537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:08750d5ef4a928c2980b5aea8990d5292187a6a432438fbdc88ae4d136d126fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11362288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bc499e9670c13c592e625c61a7100506638b578d450a3bc6e63400a8770c1c`

```dockerfile
```

-	Layers:
	-	`sha256:2f00ebea6edbd9f8d1f607be908799d7096c70facb2728764f82f773da183fef`  
		Last Modified: Tue, 27 Jan 2026 23:13:10 GMT  
		Size: 11.3 MB (11341234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d757295dad3a3c0e1f852b6c73b0128a8e192cbf85782d68f6051e0171513a9`  
		Last Modified: Tue, 27 Jan 2026 23:13:09 GMT  
		Size: 21.1 KB (21054 bytes)  
		MIME: application/vnd.in-toto+json
