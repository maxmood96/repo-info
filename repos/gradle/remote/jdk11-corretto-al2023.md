## `gradle:jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:963d01406f452e173a9cec329c304e2e59918a06c8e065175da0b3cd38ac83d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:42d1e469ed46a8207a3b812cd4bb6744915f819b3a067fc1c3847624c8f213be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.5 MB (431477839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31d0da84c31b67948fd58175f6542fff77b517139c31c7ef3efe225d4f568ff1`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:16 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:50 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 22:13:50 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:13:50 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 03 Apr 2026 23:12:05 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 23:12:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 23:12:05 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 23:12:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 23:12:05 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 23:12:05 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 23:12:05 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 03 Apr 2026 23:12:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 03 Apr 2026 23:12:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 23:12:08 GMT
USER gradle
# Fri, 03 Apr 2026 23:12:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 03 Apr 2026 23:12:08 GMT
USER root
```

-	Layers:
	-	`sha256:a2488c40110fb2b90385f44d9af6173894e14350935e38653aee164551cb70d6`  
		Last Modified: Thu, 02 Apr 2026 00:19:16 GMT  
		Size: 54.6 MB (54571303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14afc2702a7f10f51001c183da30616257459b7a21460ae343e010ff2341af55`  
		Last Modified: Fri, 03 Apr 2026 22:14:10 GMT  
		Size: 153.4 MB (153364606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061d7d521ed08d57dc96d13d40a52e1d364afd160199969a7d58f8b0e70bcdb`  
		Last Modified: Fri, 03 Apr 2026 23:12:42 GMT  
		Size: 86.1 MB (86097083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c801552f0567c269c3847513e266624a2a9e5094bc6f561c77870c9aebdae6c3`  
		Last Modified: Fri, 03 Apr 2026 23:12:36 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4960fff94cfc4cee177e4b4b3cbe2f645f396b2f28d953b47f1cce15e96c8814`  
		Last Modified: Fri, 03 Apr 2026 23:12:41 GMT  
		Size: 137.4 MB (137388272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7e2f608c5e421a98f67f0b1ce41c22a235cb59d079156f38a6a52dff87b045`  
		Last Modified: Fri, 03 Apr 2026 23:12:37 GMT  
		Size: 54.9 KB (54895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:bda99b787edf31155e0d1c45321b7c3fac7f9ca0ca770571c0c5ba31fc3a56a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11395692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef19cc9a37744f6241ff52bb105435183f55c1019092278bc3ff787d0d531159`

```dockerfile
```

-	Layers:
	-	`sha256:d91b4dd2b99ed7e4cd406f267d69f79a57a1930996df680e011e05a34048aa1f`  
		Last Modified: Fri, 03 Apr 2026 23:12:37 GMT  
		Size: 11.4 MB (11374170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81de61493c46e2b8c96aa6cd06e169eec69ba35603ccb48b2d125cd655cfac27`  
		Last Modified: Fri, 03 Apr 2026 23:12:37 GMT  
		Size: 21.5 KB (21522 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:907f646e9d1d1e56e08f733aa58600de6d7609a3e43eb6b4acef5ac6c097a653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.4 MB (428419093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f6d601f64556b7a60f74a88c47e564cd3119cbde965ea27e4356ef6258550a`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:47 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 22:13:47 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:13:47 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 03 Apr 2026 23:12:39 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 23:12:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 23:12:39 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 23:12:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 23:12:39 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 23:12:39 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 23:12:39 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 03 Apr 2026 23:12:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 03 Apr 2026 23:12:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 23:12:42 GMT
USER gradle
# Fri, 03 Apr 2026 23:12:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 03 Apr 2026 23:12:43 GMT
USER root
```

-	Layers:
	-	`sha256:cf8ff26f8ca2e7db6c1eb2c69aec532f89cf3016cc84f77de00b260ba62b2ffc`  
		Last Modified: Thu, 02 Apr 2026 00:19:15 GMT  
		Size: 53.4 MB (53442825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a77dccec3e92a918f77b51b05b9a494897149cb94761faec731163d8c68bc2`  
		Last Modified: Fri, 03 Apr 2026 22:14:09 GMT  
		Size: 151.9 MB (151923526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9865cdeb588591f42ccb010988e48f1b483ba3243d3b8c0c6bb1e0564a07367a`  
		Last Modified: Fri, 03 Apr 2026 23:13:14 GMT  
		Size: 85.6 MB (85603263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b89a7dca69b79cd76904ea97570619da8f5e3fb3afeeeb71bed11e8c7fd52a`  
		Last Modified: Fri, 03 Apr 2026 23:13:11 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a914ba465046051e50a6413e0be19242aa7000be7ac6d9189b36177a45d38b1f`  
		Last Modified: Fri, 03 Apr 2026 23:13:15 GMT  
		Size: 137.4 MB (137388267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9c44f49a314a11a2548b17539515bbbfee8bc2ef4389423859b086b3cc4844`  
		Last Modified: Fri, 03 Apr 2026 23:13:11 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:71a028229e42acf49ca997ab10ee247f1806f00f1f45b2bc4cd7a56859f9e250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11395733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632069f9d1ff2a5a31ea099165478cd836643b5261ef09d524265f3bb7582adf`

```dockerfile
```

-	Layers:
	-	`sha256:767ed7212c5647faf92f1d204d86d0f6515b55b76ecac07550a410e6c2f878b3`  
		Last Modified: Fri, 03 Apr 2026 23:13:11 GMT  
		Size: 11.4 MB (11374013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:367565605117251f95a00cd73cd293c8806c444517f1ec78443cf724139f4fa0`  
		Last Modified: Fri, 03 Apr 2026 23:13:11 GMT  
		Size: 21.7 KB (21720 bytes)  
		MIME: application/vnd.in-toto+json
