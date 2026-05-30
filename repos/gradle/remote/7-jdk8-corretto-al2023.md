## `gradle:7-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:81ee24fba97d46c2084c5cc7aee810422d5e71a676cd4681f3ceb7aa39a66bb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:255ef0c9ffd40f9ec283e7b902e7a90b952b0cfa91773a73d8f3ed63c2ce2534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.5 MB (579519388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9dfd895e8a8c044513b810259ef96ccbbfd3783cd044880a9af95ad0d82d267`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 30 May 2026 00:26:56 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:26:56 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:14 GMT
ARG version=1.8.0_492.b09-2
# Sat, 30 May 2026 01:11:14 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:11:14 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sat, 30 May 2026 02:12:36 GMT
CMD ["gradle"]
# Sat, 30 May 2026 02:12:36 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 30 May 2026 02:12:36 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 30 May 2026 02:12:36 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 30 May 2026 02:12:36 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 30 May 2026 02:12:36 GMT
WORKDIR /home/gradle
# Sat, 30 May 2026 02:12:36 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 30 May 2026 02:12:36 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 30 May 2026 02:12:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 30 May 2026 02:12:39 GMT
USER gradle
# Sat, 30 May 2026 02:12:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 30 May 2026 02:12:39 GMT
USER root
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c124850171618c8c06b3e9af5da7cfa5fedee3f73019b295148322981a9978`  
		Last Modified: Sat, 30 May 2026 01:12:04 GMT  
		Size: 330.8 MB (330826743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975681894420f00c1e6c531884da50d854d7b992b096ea2f22c1dc8ff67065aa`  
		Last Modified: Sat, 30 May 2026 02:13:16 GMT  
		Size: 65.6 MB (65595199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402ba3ba6abb79b4b146b7c9f7eef9f3a289c159d442978cec92f7c9077e70df`  
		Last Modified: Sat, 30 May 2026 02:13:13 GMT  
		Size: 1.9 KB (1943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecbe82ceadf360025562ba26420b729ddc0f014152a202a30a310e404c93a5e`  
		Last Modified: Sat, 30 May 2026 02:13:17 GMT  
		Size: 128.5 MB (128469415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bc48563984252b9124bccfc8124679a877841ab34e1e4b085154e9cf9c7802`  
		Last Modified: Sat, 30 May 2026 02:13:13 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:8f133c0163ce63d0d0db8053d92870454d592b35ca74c307b0f764a66ec8dfc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18094423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c645358e507eb18a76f8a2bcfdc9aea6a43ef10c034620e21bf06e8c0158f9`

```dockerfile
```

-	Layers:
	-	`sha256:2eefc8e212f96490b9af34d1f1c81c6b33811f45cf0d33478eec29064c92a964`  
		Last Modified: Sat, 30 May 2026 02:13:14 GMT  
		Size: 18.1 MB (18073559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03dda3f9366be02f3db64cab0e03a1a90705f7d6b4be6844d51bf080572d2605`  
		Last Modified: Sat, 30 May 2026 02:13:13 GMT  
		Size: 20.9 KB (20864 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:255951c4df561a06603aa91e08da01516e3f9dc3e54cd79c795ecc3f4f54baf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.7 MB (385661313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10af17a6d1e4ba3ff28755875b1a4f7108c0c92bca0d3d467be04e8ec8b3ad8`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:10:57 GMT
ARG version=1.8.0_492.b09-2
# Sat, 30 May 2026 01:10:57 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:10:57 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:10:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sat, 30 May 2026 02:12:43 GMT
CMD ["gradle"]
# Sat, 30 May 2026 02:12:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 30 May 2026 02:12:43 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 30 May 2026 02:12:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 30 May 2026 02:12:43 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 30 May 2026 02:12:43 GMT
WORKDIR /home/gradle
# Sat, 30 May 2026 02:12:43 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 30 May 2026 02:12:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 30 May 2026 02:12:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 30 May 2026 02:12:46 GMT
USER gradle
# Sat, 30 May 2026 02:12:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 30 May 2026 02:12:46 GMT
USER root
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e03a6be935c18229b50b865fef1df8933b41369ff27f8ccd898fb5b43bf2c1`  
		Last Modified: Sat, 30 May 2026 01:11:17 GMT  
		Size: 118.0 MB (117955656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a34f4e364b98ef804e83849648916d840c220b291f5f33b0ab4eb271b7f0fe`  
		Last Modified: Sat, 30 May 2026 02:13:16 GMT  
		Size: 85.7 MB (85717214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4fa030aad2d0ddb96e7020df376cf1e12a335ee8a8cfb148cde394221ef935`  
		Last Modified: Sat, 30 May 2026 02:13:13 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58732ae16f3c05972793ff60732490459a2ca9ddb4a6b8dae85638ac9548309d`  
		Last Modified: Sat, 30 May 2026 02:13:17 GMT  
		Size: 128.5 MB (128469419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f3349a6dbc425d5af6f8b4573eb50b6f33a283bc729aa5f4af0cd900613560`  
		Last Modified: Sat, 30 May 2026 02:13:13 GMT  
		Size: 59.5 KB (59515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:8a424e5c97c514381d39bd90d08836bc2e569d19c6df6c9ef96bb213b630281c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11658752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d269d47cebc72ee4df415ffde580a01702d5727947047f533272e81450c348e1`

```dockerfile
```

-	Layers:
	-	`sha256:1ca96c87695e8348b4651449e4b218f94c9cf4e7a1daac222498d733cad2c1d4`  
		Last Modified: Sat, 30 May 2026 02:13:14 GMT  
		Size: 11.6 MB (11637715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a85554a10aeede6bfb231dbce5289ef960816cbabb257f7c1387e2fc5351d25`  
		Last Modified: Sat, 30 May 2026 02:13:13 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json
