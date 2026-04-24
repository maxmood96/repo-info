## `gradle:jdk11-corretto`

```console
$ docker pull gradle@sha256:e46554de2c56e845e8499f5bba4007b4d2def675c1ba45b76ccf9215a8c07acd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:2321177b6c92ae999201e721924d7c185f930dadc23aa11ee2d8f3f340089460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.6 MB (431637854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2828ae27551674f861e241b0b4a0db5e069317628824fc7008b6a90ce752f477`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:40 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:09:57 GMT
ARG version=11.0.31.11-1
# Fri, 24 Apr 2026 00:09:57 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:09:57 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:09:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 24 Apr 2026 01:11:53 GMT
CMD ["gradle"]
# Fri, 24 Apr 2026 01:11:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 24 Apr 2026 01:11:53 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 24 Apr 2026 01:11:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 24 Apr 2026 01:11:53 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 24 Apr 2026 01:11:53 GMT
WORKDIR /home/gradle
# Fri, 24 Apr 2026 01:11:53 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 24 Apr 2026 01:11:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 24 Apr 2026 01:11:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 24 Apr 2026 01:11:57 GMT
USER gradle
# Fri, 24 Apr 2026 01:11:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 24 Apr 2026 01:11:57 GMT
USER root
```

-	Layers:
	-	`sha256:60406c832328f9a4f3aa21eb9cb5b2182d79ad008cd21f0bbac4517c1836be2e`  
		Last Modified: Tue, 14 Apr 2026 01:03:42 GMT  
		Size: 54.6 MB (54569705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80d44373b6b20ce8327f1b15c6a0145f06a261ca87e4a1909cc7eae76089226`  
		Last Modified: Fri, 24 Apr 2026 00:10:24 GMT  
		Size: 153.5 MB (153474084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a5ef7acddb1115030a9dd62934b12dd2dbe9008d9316707ae02044d4dacbb0`  
		Last Modified: Fri, 24 Apr 2026 01:12:28 GMT  
		Size: 86.1 MB (86149216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509d0e6a04d2b808f084b5ba1d07c7df57c8cd99686a5bcfbcb800b7aa29c531`  
		Last Modified: Fri, 24 Apr 2026 01:12:24 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728fec3083b57adf88e8a02ce52f3d3e4a005ac43bacc1f0c3c215eb0e6d3b03`  
		Last Modified: Fri, 24 Apr 2026 01:12:29 GMT  
		Size: 137.4 MB (137388269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afda4ad0199a4a6b18d7d65ccd1a4ae0a80d4f1e2a11577a9a61c6bd2fb57f04`  
		Last Modified: Fri, 24 Apr 2026 01:12:24 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:91a7246ce11a0a3827ed95061773e7ac65ae2b275aa0ef9941f0289eeee7efd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11397026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b453a712243411b12f56e4eef97fa99d65893a9107767902df69e0f8dfd959a`

```dockerfile
```

-	Layers:
	-	`sha256:39daa05e6d02b060f01a65120c69aaf9d1c72c0c3c1a8780baefbb55c2c3e9b5`  
		Last Modified: Fri, 24 Apr 2026 01:12:25 GMT  
		Size: 11.4 MB (11375503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33ec4fca5f5786bb13cf94ac5b0d98672c670c164c575b47ddacd0574aa9141d`  
		Last Modified: Fri, 24 Apr 2026 01:12:24 GMT  
		Size: 21.5 KB (21523 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:7fd91f5020fb05d911f694b9543519c423cb83879705b367601be91d39e87abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428608716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e7e7c06dfe546539b5afec6e70c82d7a9541ec26abed93c24fe3e03a9294de`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:02 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:09:13 GMT
ARG version=11.0.31.11-1
# Fri, 24 Apr 2026 00:09:13 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:09:13 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:09:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 24 Apr 2026 01:11:48 GMT
CMD ["gradle"]
# Fri, 24 Apr 2026 01:11:48 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 24 Apr 2026 01:11:48 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 24 Apr 2026 01:11:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 24 Apr 2026 01:11:48 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 24 Apr 2026 01:11:48 GMT
WORKDIR /home/gradle
# Fri, 24 Apr 2026 01:11:48 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 24 Apr 2026 01:11:48 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 24 Apr 2026 01:11:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 24 Apr 2026 01:11:51 GMT
USER gradle
# Fri, 24 Apr 2026 01:11:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 24 Apr 2026 01:11:51 GMT
USER root
```

-	Layers:
	-	`sha256:a89c935522476873ac76a02a8b4103cba17c6900bdcb1d98998ed64657edf59f`  
		Last Modified: Tue, 14 Apr 2026 02:24:36 GMT  
		Size: 53.5 MB (53452253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a43495d7ee4b274fe35850640e64823f0ffec4fc64191728ae88a758c10954`  
		Last Modified: Fri, 24 Apr 2026 00:09:36 GMT  
		Size: 152.1 MB (152050389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007ff19e86154998822ec4441c69940af835eb4e1536d0b09b5f33b053eee208`  
		Last Modified: Fri, 24 Apr 2026 01:12:24 GMT  
		Size: 85.7 MB (85656596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bb6b9fc19119518d5e0f1c9b83c316d6844c5b3a7dec8a30bc49872c43f79d`  
		Last Modified: Fri, 24 Apr 2026 01:12:19 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfeb3ae8054e79ec92aba1445a2f5f66310019805e0379354f8d4e218178abe8`  
		Last Modified: Fri, 24 Apr 2026 01:12:24 GMT  
		Size: 137.4 MB (137388270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cc59f585d7449576cbd56a6d0d504612650be89477801220bd5dda4dfd010e`  
		Last Modified: Fri, 24 Apr 2026 01:12:19 GMT  
		Size: 59.5 KB (59531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:46f864eb86a315639db298bd25df2af0983b26fd92d8fcd09070d6c539dabff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11397066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4175224856d80c759264d446fcd5bb08a4ec274ef975b7a11cca909321f18b5c`

```dockerfile
```

-	Layers:
	-	`sha256:73285ec58dfdc7293078596c7ea028d7571c45e72c76e99dd1bd87573a5b1dad`  
		Last Modified: Fri, 24 Apr 2026 01:12:20 GMT  
		Size: 11.4 MB (11375346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c4314cb6b48a155f879a0968c0316637d6fb455eccb8b3950bf4ab266cbb42`  
		Last Modified: Fri, 24 Apr 2026 01:12:19 GMT  
		Size: 21.7 KB (21720 bytes)  
		MIME: application/vnd.in-toto+json
