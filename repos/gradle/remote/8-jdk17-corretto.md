## `gradle:8-jdk17-corretto`

```console
$ docker pull gradle@sha256:df62819bf514bb8b1b41ffdaf8b80600f2575098fc3b7d3f83938b65b4935bc9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:fb72b6cd210e58d9af3349272a86996c63e259849608b0319dd65cc9d754b32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.0 MB (435025803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73c8237bb05c9df5b24ccc33b2e4ef71c2261b3bc6ab5dd20859c28736dfbc0`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:16 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:36 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 22:14:36 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:14:36 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:14:36 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 03 Apr 2026 23:12:03 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 23:12:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 23:12:03 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 23:12:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 23:12:03 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 23:12:03 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 23:12:03 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 03 Apr 2026 23:12:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 03 Apr 2026 23:12:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 23:12:06 GMT
USER gradle
# Fri, 03 Apr 2026 23:12:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 03 Apr 2026 23:12:06 GMT
USER root
```

-	Layers:
	-	`sha256:a2488c40110fb2b90385f44d9af6173894e14350935e38653aee164551cb70d6`  
		Last Modified: Thu, 02 Apr 2026 00:19:16 GMT  
		Size: 54.6 MB (54571303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa6c65371a2d0452e68a7849e65aa6fec9a2eacabd234c5f9ae4305aa623f8e`  
		Last Modified: Fri, 03 Apr 2026 22:14:58 GMT  
		Size: 156.9 MB (156911184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a15a1ea1d05cfe22b215328f21be58f8d99ec05242c86e97e7df0df7c29fbe`  
		Last Modified: Fri, 03 Apr 2026 23:12:38 GMT  
		Size: 86.1 MB (86098469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d89686788503e0b2705bae1d5e654bd62b8b88f608334d4106f9cbf7c46ee0`  
		Last Modified: Fri, 03 Apr 2026 23:12:34 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e260cd50e8193909f11c385ebce6d753875a16d68c612c39cd5239e826ba14f8`  
		Last Modified: Fri, 03 Apr 2026 23:12:40 GMT  
		Size: 137.4 MB (137388273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a94073042432a88ad64da34c642541dbdc3c71b91f91fc51f174812aa2fdd0`  
		Last Modified: Fri, 03 Apr 2026 23:12:34 GMT  
		Size: 54.9 KB (54893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:411de51ec2ff7975f64aa3eac480154b5c696b33812de198fe24d8cf5c257f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11368745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9f4032c78407c97920ccddfb9dabe2ead06b778267c8aa23f0131c8f9610df`

```dockerfile
```

-	Layers:
	-	`sha256:835f349107b909c8ff5056ea9e40667f7e1c6133f6535c33137251ea94b02c46`  
		Last Modified: Fri, 03 Apr 2026 23:12:35 GMT  
		Size: 11.3 MB (11348018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a748f0febeab8af0a5c26e93ab07d00f896a35a6da52128c9f1f34dad353222`  
		Last Modified: Fri, 03 Apr 2026 23:12:34 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2ea0919ca1186c81b02abc991ecdc406c46bde9f13c8ff1fb6cfd350a083d980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.2 MB (432225389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca875cedece576d0e8ba27514eca30ce27d6db0c7612f5e75d3add124cf90ef`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:52:42 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 22:52:42 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:52:42 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:52:42 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:52:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 03 Apr 2026 23:12:34 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 23:12:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 23:12:34 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 23:12:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 23:12:35 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 23:12:35 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 23:12:35 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 03 Apr 2026 23:12:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 03 Apr 2026 23:12:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 23:12:38 GMT
USER gradle
# Fri, 03 Apr 2026 23:12:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 03 Apr 2026 23:12:38 GMT
USER root
```

-	Layers:
	-	`sha256:cf8ff26f8ca2e7db6c1eb2c69aec532f89cf3016cc84f77de00b260ba62b2ffc`  
		Last Modified: Thu, 02 Apr 2026 00:19:15 GMT  
		Size: 53.4 MB (53442825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a171146ed2608cfed7379a8e096372cbf936c9d64c321d3b501ba505f2694fb8`  
		Last Modified: Fri, 03 Apr 2026 22:53:07 GMT  
		Size: 155.7 MB (155728253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59d1f3db86a671d2aabcc993372f389cc77c700df0d861b36efb5f74c27e0b6`  
		Last Modified: Fri, 03 Apr 2026 23:13:10 GMT  
		Size: 85.6 MB (85604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f961e6ed976607f3272ff2494f0be15baf966aa89f662f360f2bf548a70faf`  
		Last Modified: Fri, 03 Apr 2026 23:13:06 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335c117ec42a4f973ef37293a9ece042e9ae69859088b2e910d30b21f2862ff8`  
		Last Modified: Fri, 03 Apr 2026 23:13:11 GMT  
		Size: 137.4 MB (137388270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fafdf697ba626696afb0b4e6b581a222ef0e85867445f72e9e5fd9a617e8e1`  
		Last Modified: Fri, 03 Apr 2026 23:13:07 GMT  
		Size: 59.5 KB (59522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:7ac6c1b2f6b30e240dc119e44af73aa387629438748662969c835ed972ab5f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11367893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06144bbfa242ffa6b738f831a6f5a3d266da2f4d4ffccfaf6cfd64f02eab6709`

```dockerfile
```

-	Layers:
	-	`sha256:5db03174517a99fc72a1a798ebe92073d578997742bc6499f3ae419fe3f0203e`  
		Last Modified: Fri, 03 Apr 2026 23:13:07 GMT  
		Size: 11.3 MB (11346993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea9a2e2be2832b58e44d5cb062c3ccc1d9864c03c21d2a29ccfed25ccbb097aa`  
		Last Modified: Fri, 03 Apr 2026 23:13:06 GMT  
		Size: 20.9 KB (20900 bytes)  
		MIME: application/vnd.in-toto+json
