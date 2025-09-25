## `gradle:jdk11-corretto`

```console
$ docker pull gradle@sha256:e7c9e7ff219e55e5abd178260fa7cb5e635a02ea28cdbcf73a8265c8572385f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:eec3977b315051936835125c8da90e8240f3a0c48e29d9ca5d6aaa7db7046bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.1 MB (431097501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ad970bd008ced4fa4b813abc91eca12138db40aff872c19fb920b11d97454e`
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
	-	`sha256:b6baa302384dc877580d7e1080dcca1ed66d9d3b38afc9fcc29c360239e3e362`  
		Last Modified: Tue, 16 Sep 2025 20:50:40 GMT  
		Size: 54.0 MB (54005280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a85c53f5c61cce6dc0162eb66e7a7e14c47b0962aa13f24a73b943f9d74e012`  
		Last Modified: Thu, 25 Sep 2025 03:14:46 GMT  
		Size: 154.1 MB (154074648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cff048a9beed31e66b5cac09402374720761125e1e7e6a1279100cebda86dd5`  
		Last Modified: Thu, 25 Sep 2025 03:16:07 GMT  
		Size: 85.6 MB (85565868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720d18a9e693ec0a3b5fa7a10fc8a9a796c90e90ada9127397b688e6f10e801d`  
		Last Modified: Thu, 25 Sep 2025 03:15:56 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f432d7a498d886fc5d611592945612da5446f3e0ce14e84212bc52b040b42630`  
		Last Modified: Thu, 25 Sep 2025 07:16:46 GMT  
		Size: 137.4 MB (137395119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2951f9cae783596859744f7a497a421ce3d0cc2b9e9eccd9bfb994a60c8dc2c4`  
		Last Modified: Thu, 25 Sep 2025 03:15:56 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:d4ca6641b6a00bf27da5660ff24b9f0c0983564f7155e3318614f151076627a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11359215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4dac1e1819e8e9846f27eb1cd79595b37ce906cb6f1fb40938344f97f5f4da1`

```dockerfile
```

-	Layers:
	-	`sha256:74dcfb1cecadd172e3ac9f969af58ad6d3dd7365b4f2de848de89bc358398649`  
		Last Modified: Thu, 25 Sep 2025 05:20:32 GMT  
		Size: 11.3 MB (11337649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebd74bff972910d1f6025c3805a30bbd662da6df064f840336889f0b37db42f7`  
		Last Modified: Thu, 25 Sep 2025 05:20:33 GMT  
		Size: 21.6 KB (21566 bytes)  
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
		Last Modified: Thu, 25 Sep 2025 07:51:16 GMT  
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
