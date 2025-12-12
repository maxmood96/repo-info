## `gradle:8-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:fd3b2dc56c6898c88aed8af77b704ba22c74da956c3b27e0dba63607d6bfed5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:ec5bb3f767da70a40ec0053fd810ea09b17d122149dcf2a38c51ce944cba5489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.7 MB (587697935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066f77075eb94f3ce307f632a84dac6b4b6ebeef210f82139eec878441d0a16b`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:09 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:09 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:42 GMT
ARG version=1.8.0_472.b08-1
# Thu, 11 Dec 2025 22:11:42 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:11:42 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 11 Dec 2025 22:17:55 GMT
CMD ["gradle"]
# Thu, 11 Dec 2025 22:17:55 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 11 Dec 2025 22:17:55 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 11 Dec 2025 22:17:55 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 11 Dec 2025 22:17:55 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 11 Dec 2025 22:17:55 GMT
WORKDIR /home/gradle
# Thu, 11 Dec 2025 22:17:55 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 11 Dec 2025 22:17:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 11 Dec 2025 22:17:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 11 Dec 2025 22:17:57 GMT
USER gradle
# Thu, 11 Dec 2025 22:17:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 11 Dec 2025 22:17:58 GMT
USER root
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56aa5671e4c6388bab5eaf668041a81c0906c37489a66a044c651a8ef17681b4`  
		Last Modified: Thu, 11 Dec 2025 22:12:45 GMT  
		Size: 330.9 MB (330888100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d672d6435a060853ab0117bd62bd63bfc493d2be322b7caafc24760ab4422f`  
		Last Modified: Thu, 11 Dec 2025 22:18:53 GMT  
		Size: 65.4 MB (65369297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ee03bc8563e3f5592fa2c03ef9a10f4289408c41827015693bfe556a96d1ba`  
		Last Modified: Thu, 11 Dec 2025 22:18:45 GMT  
		Size: 1.9 KB (1943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ffd4509fa03eca176d4dacc67194449c1181baabe85b12617cf0e02c922662`  
		Last Modified: Thu, 11 Dec 2025 22:18:41 GMT  
		Size: 137.4 MB (137395194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abd9602ec203cd8e8891c35dd1ff99b6997046656c724c70d9900dbf0b09c5e`  
		Last Modified: Thu, 11 Dec 2025 22:18:45 GMT  
		Size: 54.9 KB (54909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:d3a6bbc17b870303aba92cb5eb1bc1a95512666a17d86912aea5529e3a228ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18175389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb80e1b88468af72b46ee96748e831ba2acdd0555c00286bb6c6180b8aeb6e5`

```dockerfile
```

-	Layers:
	-	`sha256:4336ffd444311ad809fe9d1724f804294d531b541658ba4fcc39141927fd898c`  
		Last Modified: Fri, 12 Dec 2025 00:21:22 GMT  
		Size: 18.2 MB (18153873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2374fdbade3737b4245f7ff675e85aea751f9242a80c8a391b1ac7f234161578`  
		Last Modified: Fri, 12 Dec 2025 00:21:23 GMT  
		Size: 21.5 KB (21516 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ed8ef906b355db02c6c51664a2ab41e7ab044d65aef3518c2e3904d173a2a662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393772755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8baa06b83be44760a3bf05c964356d15a95e0801e2e17e59031a24f13e3215f0`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 11 Dec 2025 21:45:58 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:45:58 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:30 GMT
ARG version=1.8.0_472.b08-1
# Thu, 11 Dec 2025 22:11:30 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:11:30 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 11 Dec 2025 22:17:18 GMT
CMD ["gradle"]
# Thu, 11 Dec 2025 22:17:18 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 11 Dec 2025 22:17:18 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 11 Dec 2025 22:17:18 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 11 Dec 2025 22:17:18 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 11 Dec 2025 22:17:18 GMT
WORKDIR /home/gradle
# Thu, 11 Dec 2025 22:17:18 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 11 Dec 2025 22:17:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 11 Dec 2025 22:17:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 11 Dec 2025 22:17:20 GMT
USER gradle
# Thu, 11 Dec 2025 22:17:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 11 Dec 2025 22:17:21 GMT
USER root
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c48e9835d76eae2b2c4e9d6c02f6408efc2e56451c92c8fa9e4c21b8dd8690`  
		Last Modified: Thu, 11 Dec 2025 22:12:13 GMT  
		Size: 117.9 MB (117927059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ace4a80798ece7091cc7870fdbceb3fb3da36159aa414dfc301064155b14f3`  
		Last Modified: Thu, 11 Dec 2025 22:18:05 GMT  
		Size: 85.5 MB (85515841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013a93e46bbe9edbdbda1a2f3e39e2d783392ac60d4fc2906db79ca3212d34bd`  
		Last Modified: Thu, 11 Dec 2025 22:17:59 GMT  
		Size: 1.6 KB (1641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f27839a54f91f0bac3c05078ae15b16eb7258d1398c8e21e4c2a34c71296d68`  
		Last Modified: Thu, 11 Dec 2025 22:17:52 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe7f94a99d99b87b0e386a550793d3800f21f1b0884f9e52a695196fa14e0ee`  
		Last Modified: Thu, 11 Dec 2025 22:17:59 GMT  
		Size: 59.5 KB (59536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:854a3fc4206742bf651c2dd1e82fd4ebdc4bb69b924ac64a7982e2708c3e3495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11739774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64603b2f83172ef8f61a00b0a9146a938a0d6289d1772bc44b1bc600923f889c`

```dockerfile
```

-	Layers:
	-	`sha256:fa6aea55ed6abd28c22b89d136a9f939fe55db3a6c7803c103025c85a9e91d9b`  
		Last Modified: Fri, 12 Dec 2025 00:21:41 GMT  
		Size: 11.7 MB (11718061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b4d3bbde2c3410287e223a9d1b17ea94f41125e94c229fa49e340421ce780b`  
		Last Modified: Fri, 12 Dec 2025 00:21:41 GMT  
		Size: 21.7 KB (21713 bytes)  
		MIME: application/vnd.in-toto+json
