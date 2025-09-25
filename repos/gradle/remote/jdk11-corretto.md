## `gradle:jdk11-corretto`

```console
$ docker pull gradle@sha256:68825c4bd6ffd3c70fd65d83e13e83dbad04a48e824252906c89fed13bfde94a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:c6e54c8f000c09ea6773a599a87c19ea049eecbe0799f49c2dc2cf62cd775ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (430955481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e3b1717f88755d4923a18c3e1c943c586abff911913e854ae2c6afb39e7a59`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
ARG version=11.0.28.6-1
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=C.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER gradle
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER root
```

-	Layers:
	-	`sha256:0727f841555e830a24054117b5d53ecc18438e2e82fc78dd3cc766ca6bb76cab`  
		Last Modified: Wed, 10 Sep 2025 02:33:49 GMT  
		Size: 53.9 MB (53875706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f8145f80f6a9693df4d2f42ea579d9b299c3223cd58a6b1c3ba0ca3078d209`  
		Last Modified: Fri, 12 Sep 2025 02:10:10 GMT  
		Size: 154.1 MB (154069919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d8214549e2c1397ffdcb2c4b93b092fc7560aae26db9c6fd0e9f05df6c369e`  
		Last Modified: Fri, 12 Sep 2025 07:24:05 GMT  
		Size: 85.6 MB (85558070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd410c2ede3c9a2570c087027458e50c78156e2d481cad9f87c7a6d897f46056`  
		Last Modified: Fri, 12 Sep 2025 02:11:28 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eaddd13ce0f26b406509a63e0c9ad5452fa587cf9f7355b24c84b43411cb244`  
		Last Modified: Fri, 12 Sep 2025 07:24:11 GMT  
		Size: 137.4 MB (137395201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533a97dbd1b9c40451db23513a73a6d59bd2a3c5dfa1cd22594105b37d168f88`  
		Last Modified: Fri, 12 Sep 2025 02:11:45 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:cd2e18679c907cbc8e0e6080c24931267478ab4882cc5d69611e8b806dd8ed5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11359214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac2c729d0e82961566db227eadf0a1c7d0f6a2f4d7e3995463b1c8927e1cc2ba`

```dockerfile
```

-	Layers:
	-	`sha256:82fee5a2f7ff66c7015654e91e45f4a7efffe1fbdaddc287e86852d76d7f597f`  
		Last Modified: Fri, 12 Sep 2025 05:20:47 GMT  
		Size: 11.3 MB (11337649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af0ae82a90efec2930cd5d6baca75ea109dfa4125d5898389d17d627e72d48db`  
		Last Modified: Fri, 12 Sep 2025 05:20:48 GMT  
		Size: 21.6 KB (21565 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:85330f8bba635e7a320576df6cadf2759efc0788a1f105820a2df988f07e5d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.0 MB (428020940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a0223f69766cda3c237a427cbc8885ce7a17e4a0bd79114cee6890ec8c1871`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 12 Sep 2025 13:29:01 GMT
COPY /rootfs/ / # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
CMD ["/bin/bash"]
# Fri, 12 Sep 2025 13:29:01 GMT
ARG version=11.0.28.6-1
# Fri, 12 Sep 2025 13:29:01 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
ENV LANG=C.UTF-8
# Fri, 12 Sep 2025 13:29:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 12 Sep 2025 13:29:01 GMT
CMD ["gradle"]
# Fri, 12 Sep 2025 13:29:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Sep 2025 13:29:01 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Sep 2025 13:29:01 GMT
WORKDIR /home/gradle
# Fri, 12 Sep 2025 13:29:01 GMT
ENV GRADLE_VERSION=8.14.3
# Fri, 12 Sep 2025 13:29:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Fri, 12 Sep 2025 13:29:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
USER gradle
# Fri, 12 Sep 2025 13:29:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
USER root
```

-	Layers:
	-	`sha256:202438f011bd656c28426fbd92ff7e7030b77e67ebafd3bec95dbce9626db73c`  
		Last Modified: Tue, 16 Sep 2025 22:16:03 GMT  
		Size: 52.9 MB (52899438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba67c498ac860f8cfec44394c18e432ed8fc284cdcd5fac40c1f6a02566a52e`  
		Last Modified: Wed, 24 Sep 2025 22:11:32 GMT  
		Size: 152.6 MB (152579454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6119163cb745a6b24892862c41bd4135ad7dc41e9759439c9a86a1135223ac28`  
		Last Modified: Wed, 24 Sep 2025 22:13:01 GMT  
		Size: 85.1 MB (85085642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdabc671e648a739cb1cefcbf69cad71a12f92149dcac5b5a83b89866ba53f4`  
		Last Modified: Wed, 24 Sep 2025 22:12:54 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e70c611f5f04fef6c2064dd99035d613bc88729d909227578ae458d085ddb2`  
		Last Modified: Wed, 24 Sep 2025 22:12:33 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e0e8abef881aa7dacd93a98e67e9a48b7afd0a1d59be9e9da659826131f3e9`  
		Last Modified: Wed, 24 Sep 2025 22:12:54 GMT  
		Size: 59.5 KB (59531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:c8d64c208b4a5f193073d851be2f064da90bd67e79d154170b7e00dcb4c2346c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11359254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0603104ff31fe8ed6c2af6a40f171befcad32b764b21364c88d186fb0c8155e`

```dockerfile
```

-	Layers:
	-	`sha256:441075d83f34c8fd0ad48b5a5ae933f25b50eea538475f26fdbaee07d2f01b91`  
		Last Modified: Thu, 25 Sep 2025 02:20:37 GMT  
		Size: 11.3 MB (11337492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c69d971f8bcacef10b4214b396c68a064db6d5043e0acea127dcce3b10c390e1`  
		Last Modified: Thu, 25 Sep 2025 02:20:38 GMT  
		Size: 21.8 KB (21762 bytes)  
		MIME: application/vnd.in-toto+json
