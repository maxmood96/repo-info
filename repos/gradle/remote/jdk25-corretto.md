## `gradle:jdk25-corretto`

```console
$ docker pull gradle@sha256:a320546200e99f590049665ead3693f675eef67de8796c2b28b4776d722aa502
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk25-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:23160bbb860ac3dad76005bbc4e867b87e5b0f34072de968db5a38face55a87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.3 MB (463274441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b222182a7f97baf4e0437f9b6f08d5342aaab0690c6b75bce56a859cdb1933`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:20 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36-2
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:b6baa302384dc877580d7e1080dcca1ed66d9d3b38afc9fcc29c360239e3e362`  
		Last Modified: Tue, 16 Sep 2025 20:50:40 GMT  
		Size: 54.0 MB (54005280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a075fb8961d282a9f92fb75aaa159d8011cb3dba1aa6fea626361cc411336906`  
		Last Modified: Thu, 25 Sep 2025 03:19:01 GMT  
		Size: 189.1 MB (189134365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c190e47e5ce0186568fbc193d681091a6f96dd74bc161289b2a0d4cd37aa22`  
		Last Modified: Tue, 30 Sep 2025 16:55:26 GMT  
		Size: 85.6 MB (85563542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42df161f5b94aa219213b3c6f1c87fa3d5e5fb8b2b70dcb4d1029dd6e8b10ab`  
		Last Modified: Tue, 30 Sep 2025 16:55:20 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d156f977ca2e05a1a37a783acacf73cdbf63a2858b55cdb7f8e84c08572313af`  
		Last Modified: Tue, 30 Sep 2025 21:14:51 GMT  
		Size: 134.5 MB (134514677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabc7b0ad378a4f074ee3479f98aabb697fa51962853bd7e4e913d3d02bfbc0d`  
		Last Modified: Tue, 30 Sep 2025 16:55:20 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:9001421c0a4a24e596bf0037618807c2200ae6ba126dbd0aad27b8e3b02af1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11336454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0521060d95b42b3281fac6a165aa5a47934449c90f2a61ba53e8ca08b238dd2`

```dockerfile
```

-	Layers:
	-	`sha256:f72bab1229920a57842467915200613894fb8d42a5f93a7cccdd9738bd4cde58`  
		Last Modified: Tue, 30 Sep 2025 20:22:18 GMT  
		Size: 11.3 MB (11314191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:140ca66dea69784575bcd9c7d2b876847db5e505537ffe7040b074b2073573c5`  
		Last Modified: Tue, 30 Sep 2025 20:22:19 GMT  
		Size: 22.3 KB (22263 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:baadf88b63e22e218080c7b332cb698539da43dfbc41c25e9328cb4e3a1be7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.6 MB (459575081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e3c8fb0d9dbebd91c1ad6acf6c354d497d5f1d34204fe1c08330709c8cd5a2`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:25 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36-2
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:202438f011bd656c28426fbd92ff7e7030b77e67ebafd3bec95dbce9626db73c`  
		Last Modified: Tue, 16 Sep 2025 22:16:03 GMT  
		Size: 52.9 MB (52899438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898bb6a5c4e092b471dfbda1890bda78055f9989087ac015177c092ddf1ad3cf`  
		Last Modified: Wed, 24 Sep 2025 22:15:39 GMT  
		Size: 187.0 MB (187019791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef1b39bb271e365a63d5b06b333c6f685ed701dce9e4a6ea52fe3b27b25c529`  
		Last Modified: Tue, 30 Sep 2025 16:43:18 GMT  
		Size: 85.1 MB (85079959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4340f498ec87e2ea89a5f713a2575eb26c7cd68f7e7b277b9123acae90d8adf3`  
		Last Modified: Tue, 30 Sep 2025 16:43:09 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171a88507b556f8e2facf30c5aa306ff57f13dfcb7e7bc1b37ac307a531a4523`  
		Last Modified: Thu, 02 Oct 2025 08:18:42 GMT  
		Size: 134.5 MB (134514676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e557a083955ebed4ca13706f9bdbcefaf1c8e9496461b81af7f09aa9155dc015`  
		Last Modified: Tue, 30 Sep 2025 16:43:09 GMT  
		Size: 59.5 KB (59538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:a9b8cd22c06dcc0834a6faece593a21be7d8d39ab439b32a49b4ac7c5e42dd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11335712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d457aabd2dc37a1953ef393b00d65e4136e7a67b423cb1c1f2c243bf21427f`

```dockerfile
```

-	Layers:
	-	`sha256:5c994572e2b5044a9d79e13f2cec2025a202c5634f9f8a72b91ca28f4ed6465d`  
		Last Modified: Wed, 01 Oct 2025 20:24:48 GMT  
		Size: 11.3 MB (11313228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d6c05f7d40518e2f1a7086c29e9bea71a1b594633860afd28aa0e26e0ef982c`  
		Last Modified: Wed, 01 Oct 2025 20:24:49 GMT  
		Size: 22.5 KB (22484 bytes)  
		MIME: application/vnd.in-toto+json
