## `gradle:6-jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:ca31c2725da0ef255a63eeacd461b039d58039805e903b4d05cc1c22381eff86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:d238e8783f8e5cf69b22ed98a5d527b90290eea938650055721077d939f156a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.4 MB (402437326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78fde46bcb1f7c942c9fee6c97b81ca66bfd297190467c811cda1a26fd978a59`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 30 May 2026 00:26:56 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:26:56 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:11 GMT
ARG version=11.0.31.11-1
# Sat, 30 May 2026 01:11:11 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:11:11 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 30 May 2026 02:12:39 GMT
CMD ["gradle"]
# Sat, 30 May 2026 02:12:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 30 May 2026 02:12:39 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 30 May 2026 02:12:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 30 May 2026 02:12:39 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 30 May 2026 02:12:39 GMT
WORKDIR /home/gradle
# Sat, 30 May 2026 02:12:39 GMT
ENV GRADLE_VERSION=6.9.4
# Sat, 30 May 2026 02:12:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Sat, 30 May 2026 02:12:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 30 May 2026 02:12:42 GMT
USER gradle
# Sat, 30 May 2026 02:12:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 30 May 2026 02:12:42 GMT
USER root
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c301665885e6ad3943c3d90b6300031bffd77f1526c8e1fb4fcff7a8956e38`  
		Last Modified: Sat, 30 May 2026 01:11:32 GMT  
		Size: 153.5 MB (153471531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eff3cb52d61e9157b42cf5ae9dff5b59bb47d7b0e8400ab2e62f8ff44282e2`  
		Last Modified: Sat, 30 May 2026 02:13:09 GMT  
		Size: 86.3 MB (86265025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850be05eaab4b3e358ff0a603c6a90fe9cc77fbb0acd8bc2ce3216cd58183018`  
		Last Modified: Sat, 30 May 2026 02:13:06 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b122bb4f077e8b10f0149f28ce64964ca045fe21373d0baefbdf04ed8b381d4d`  
		Last Modified: Sat, 30 May 2026 02:13:10 GMT  
		Size: 107.7 MB (107696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2221cae13a114f3dd0eb0a3e7978c6a29a81b0d99d33a2d8bc51b75bff589d`  
		Last Modified: Sat, 30 May 2026 02:13:06 GMT  
		Size: 431.3 KB (431274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:d36e6e7db324262e525ea6a335f2f6ac2b8935e0d9340178053e3a615af3a5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11288651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e6518d56bc7ee2b5559bdf2d7fbf4b238c858a2f33f16c4db93c0c6e870f67`

```dockerfile
```

-	Layers:
	-	`sha256:676fb4aedab32e6ed3d16b24e46f05fc997eb885334eb8163719b48063696667`  
		Last Modified: Sat, 30 May 2026 02:13:06 GMT  
		Size: 11.3 MB (11267780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cca0f648cfa1d796548cf7445e3b19dd03d95ee9e1d378c6a0e7e25a428133e2`  
		Last Modified: Sat, 30 May 2026 02:13:06 GMT  
		Size: 20.9 KB (20871 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1080999e46935020e5a89708e6896c68c30d29f0d0f67145cfdbaff5b0ae9af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.4 MB (399354632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b06d9496a1fd281d36f3945570ab4948dd26501bf0d3aec9433c1a75af096f4`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:29 GMT
ARG version=11.0.31.11-1
# Sat, 30 May 2026 01:11:29 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:11:29 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
ENV GRADLE_VERSION=6.9.4
# Sat, 30 May 2026 02:12:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Sat, 30 May 2026 02:12:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 30 May 2026 02:12:46 GMT
USER gradle
# Sat, 30 May 2026 02:12:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 30 May 2026 02:12:46 GMT
USER root
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f79fb9911ea68ee16566e2d860d6457ab071bbc028d8cd54cc7be3f1495db6`  
		Last Modified: Sat, 30 May 2026 01:11:51 GMT  
		Size: 152.0 MB (152048594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524c3ffe53221f4da87e654261d5b63fa038f6f51407259b673383c3256fa97a`  
		Last Modified: Sat, 30 May 2026 02:13:17 GMT  
		Size: 85.7 MB (85724853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0132126954834055d1fb3ff33311170df434ae1a72f34db4e610aa06276322c`  
		Last Modified: Sat, 30 May 2026 02:13:13 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f89d5a65fc44464310ab1acf2226ba8b6c3a6500ba8178f9e20804d06f503d`  
		Last Modified: Sat, 30 May 2026 02:13:18 GMT  
		Size: 107.7 MB (107696662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603ffe23a3204cbfb40425cf4faecb19d71ba3c59a471175c1e0579e06165701`  
		Last Modified: Sat, 30 May 2026 02:13:13 GMT  
		Size: 425.0 KB (425017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:c79008d6fb4c0f447a8a2b2f0a328b3b7c231ab12d28118dfdc30d38aba32294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11288644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795e0a4c0f00ea0fa067126b425623b4d622d5bc58cbe49120ac82ecd75c4d6f`

```dockerfile
```

-	Layers:
	-	`sha256:1a3e4bc97beafb3f29869d5d3572818fbd4dd59654bcd93dfef2e6a8231e6702`  
		Last Modified: Sat, 30 May 2026 02:13:14 GMT  
		Size: 11.3 MB (11267599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc99068a297652639ec367e5e2317ca35c9f562a3867ed25ff06058ea5d369a8`  
		Last Modified: Sat, 30 May 2026 02:13:13 GMT  
		Size: 21.0 KB (21045 bytes)  
		MIME: application/vnd.in-toto+json
