## `gradle:jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:f21b69218d68f772f87f6ab6c58c7578692f5c22419444514393f7a1154bc2bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:60d72b344cfd7baeb3b054a07122fa9be883228d1276e89ea8eca5cef1908430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428600687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2880e61993297c28537eba4a96d24cbe3a9b8c0a6c342473dc99345be6b0e069`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 05 Jul 2025 02:23:10 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:23:10 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 05 Jul 2025 02:23:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
USER gradle
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
USER root
```

-	Layers:
	-	`sha256:a00db81cfbfcbbcc0cbe194011d1372b5452428d24845777fa6177ed15ce473c`  
		Last Modified: Thu, 26 Jun 2025 02:06:50 GMT  
		Size: 53.8 MB (53840211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334ff24e3acbef631a7f1329bde3fb6bab6f22f75ffd4641efffd0d4245b34c`  
		Last Modified: Fri, 04 Jul 2025 00:14:07 GMT  
		Size: 153.9 MB (153924822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d62e6492e7935782b03d6e4ddd9b6287deeecfc31981d46d02d1acee8b98682`  
		Last Modified: Mon, 07 Jul 2025 20:32:55 GMT  
		Size: 83.4 MB (83383878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55abd6d77def9e14cb836c74cbb9a1f3ea2174c3f34e76e232286b016c714af9`  
		Last Modified: Mon, 07 Jul 2025 20:32:51 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4874bc04d88e81295649fbaa4bf8a7bcd2498fe9030f5bb047d837e6f00523f8`  
		Last Modified: Tue, 08 Jul 2025 00:56:52 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5599b56babe39569b548a2c870521c593de23b9ae52bc5e96d0df8fccf8369d`  
		Last Modified: Mon, 07 Jul 2025 20:32:52 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:76829b86cacd30e114688305ba419e2e471b29767c193f195349cabd7c01a847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11318738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b95acbe6978c1fd57458ac53ea7f93b0fae7430ccc6e273ede817c8fe104dd4`

```dockerfile
```

-	Layers:
	-	`sha256:b16dd7c817c27f6c8aeb240b3af6bf2221bec04aa2d5dc56c47704fdd6c85553`  
		Last Modified: Mon, 07 Jul 2025 23:24:54 GMT  
		Size: 11.3 MB (11297156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91ad01b11a888777aa5f2217f0e783233dc5995adb41401b96d1039cf3008a74`  
		Last Modified: Mon, 07 Jul 2025 23:24:55 GMT  
		Size: 21.6 KB (21582 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9568fb502a61f1b7f9f652caf74dac2659e4ac4dad933b4fe97c4375d3bb047f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.6 MB (425565687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9f4eab6d86de73e1665bf6ab1c45c92a76050e1014dd4d507595a809056b46`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 05 Jul 2025 02:23:10 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:23:10 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 05 Jul 2025 02:23:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
USER gradle
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
USER root
```

-	Layers:
	-	`sha256:0e455f237a70326021a937388393d9d7ac6f9ae1616673300f248aeb280add13`  
		Last Modified: Thu, 26 Jun 2025 02:06:50 GMT  
		Size: 52.7 MB (52717557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085b81b35eefb761e2f4006c23782253bf6d96365b07f6834c4de33e5989192d`  
		Last Modified: Fri, 04 Jul 2025 04:17:17 GMT  
		Size: 152.4 MB (152440112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126dc54a3a0479c5d4e2e14b3cce8d706f3a4cafbe3b5b8fdb1bb77d15565a89`  
		Last Modified: Fri, 04 Jul 2025 13:56:29 GMT  
		Size: 83.0 MB (82951597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f7df84d489d0b741e784a954aada49fd462ec190c985b4f6b2f202cbff4d1b`  
		Last Modified: Fri, 04 Jul 2025 04:48:43 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4765cbafd8fe458151d5a4b23b881c1e98cd0dbfb6c17804c78ff623470c84`  
		Last Modified: Mon, 07 Jul 2025 20:42:38 GMT  
		Size: 137.4 MB (137395200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d907d6c2392d61261d5bd8d415a89ed132204e77541ed20dcf39698ad69c9d4b`  
		Last Modified: Mon, 07 Jul 2025 20:42:45 GMT  
		Size: 59.5 KB (59542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:52eb0e5c56d9e56098356dc5a8e959dda4cb27c8a16daf45c7863b652adf9a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11318778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8f7e2b2e848187b8e3658468bfcfe4f23186972cd1901514c38daedf6f95e0`

```dockerfile
```

-	Layers:
	-	`sha256:b70a43c50f1a553130f203925430ad6d0273fd5f6b3f4951fe99228994e4f775`  
		Last Modified: Mon, 07 Jul 2025 23:25:03 GMT  
		Size: 11.3 MB (11296999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8b902d57441cd3dfd0d9a597a161e10877c40521e04a5deeb9800d6503b6dee`  
		Last Modified: Mon, 07 Jul 2025 23:25:04 GMT  
		Size: 21.8 KB (21779 bytes)  
		MIME: application/vnd.in-toto+json
