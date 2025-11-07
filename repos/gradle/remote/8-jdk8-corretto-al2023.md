## `gradle:8-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:6ba7d6e6f3336d54797bfbb7f59873857ca573f62e02a2d5bbb5e2a03e46df86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:afed8a908e6f519c85919aadc9ef0d642048bb45966210fb4a5040860ee6c85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587299228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75df70709c890a70968afcaef88c44a52fbfcc6f356a1efc88abe8488c96fdf2`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 06 Nov 2025 22:15:48 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:15:48 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 23:12:14 GMT
ARG version=1.8.0_472.b08-1
# Thu, 06 Nov 2025 23:12:14 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 23:12:14 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 23:12:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 07 Nov 2025 00:13:16 GMT
CMD ["gradle"]
# Fri, 07 Nov 2025 00:13:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 07 Nov 2025 00:13:16 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 07 Nov 2025 00:13:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 07 Nov 2025 00:13:16 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 07 Nov 2025 00:13:17 GMT
WORKDIR /home/gradle
# Fri, 07 Nov 2025 00:13:17 GMT
ENV GRADLE_VERSION=8.14.3
# Fri, 07 Nov 2025 00:13:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Fri, 07 Nov 2025 00:13:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 07 Nov 2025 00:13:19 GMT
USER gradle
# Fri, 07 Nov 2025 00:13:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 07 Nov 2025 00:13:19 GMT
USER root
```

-	Layers:
	-	`sha256:7857af70cc37714ae4781f1d58242c7667f933ef8be05b0636d2c50e756263b2`  
		Last Modified: Wed, 05 Nov 2025 21:09:20 GMT  
		Size: 54.0 MB (54000503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a466983e04f75b0240d48e3a95c546707491d065df8baa3200522fb42bb1f95`  
		Last Modified: Fri, 07 Nov 2025 00:12:03 GMT  
		Size: 330.9 MB (330868155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2016f01867f18e79357c0042c366ab8a3238904e4a9008af7186fe9bae6a91b`  
		Last Modified: Fri, 07 Nov 2025 00:14:13 GMT  
		Size: 65.0 MB (64978499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4388386657b6a98dcbe3856492529678be6eb4fcca856027fc909ceaf00c5bfc`  
		Last Modified: Fri, 07 Nov 2025 00:14:03 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2b4d41fcbe1ce6b34bb87229fcdf3d2cc1cbc25947b68a9b6fc941965ee953`  
		Last Modified: Fri, 07 Nov 2025 04:58:51 GMT  
		Size: 137.4 MB (137395193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0dba2e25910ef95ff92269fe82ab6406743882c1bb2d3d6f8ac8c431fb6801`  
		Last Modified: Fri, 07 Nov 2025 00:14:03 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:44e55ba4c3fe458b1d6ba8374a5b3cd502b109cd820072bfa7d831daea87ee5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18154003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfeb9a51d4501cebda9568929b375d3348707bae0d6c3364113f3da414f7f44b`

```dockerfile
```

-	Layers:
	-	`sha256:e0c6d44da630f6ee90d4d7c4501c86dd930a602d6c61b6b59f79ad0f4fe4bd1d`  
		Last Modified: Fri, 07 Nov 2025 03:21:04 GMT  
		Size: 18.1 MB (18132487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e037abb93084f2a627f561731002475c847170ef229f6e77190529a1a9d5d99`  
		Last Modified: Fri, 07 Nov 2025 03:21:05 GMT  
		Size: 21.5 KB (21516 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:0c7c51ff1929eae534f1ed0837ee2561a865f74634a272682ad5cdf7ed939891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.5 MB (393470746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ccc8f6be0f5dd0530ec9698782b6930076eda4f19f8149b2aa8330df0b17108`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:11:25 GMT
ARG version=1.8.0_472.b08-1
# Thu, 06 Nov 2025 22:11:25 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:11:25 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:11:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 06 Nov 2025 23:12:44 GMT
CMD ["gradle"]
# Thu, 06 Nov 2025 23:12:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 06 Nov 2025 23:12:44 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 06 Nov 2025 23:12:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 06 Nov 2025 23:12:44 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 06 Nov 2025 23:12:44 GMT
WORKDIR /home/gradle
# Thu, 06 Nov 2025 23:12:44 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 06 Nov 2025 23:12:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 06 Nov 2025 23:12:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 06 Nov 2025 23:12:47 GMT
USER gradle
# Thu, 06 Nov 2025 23:12:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 06 Nov 2025 23:12:47 GMT
USER root
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d1f499ea2be350aeea557e5a54efc605e09542e2e0eb46c78b5696360c7ce2`  
		Last Modified: Thu, 06 Nov 2025 22:12:07 GMT  
		Size: 118.0 MB (117956781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986aa1522394dccd70bc0b30f0f7067a71f616eabba65e2e1c12fb67c55adff8`  
		Last Modified: Thu, 06 Nov 2025 23:13:33 GMT  
		Size: 85.2 MB (85155880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1f1ca17032cfbc03ad9d914279a8a8abedb1f05884805666f42aa278057cf9`  
		Last Modified: Thu, 06 Nov 2025 23:13:27 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b3d8cc92fbf60c45050c17724ddefdeee5a39eb84c9f4b7fba294b5db1e772`  
		Last Modified: Thu, 06 Nov 2025 23:13:20 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2bd56cad367252670931e0ff087976bf553418baa55bc7b9163a345e81833d`  
		Last Modified: Thu, 06 Nov 2025 23:13:27 GMT  
		Size: 59.5 KB (59523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:dedf989892b9c1e37ce9025fd78aca8d16b2594a3cb463737a4d1c32a71039aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11718390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25618ee632fa9f5f307c416ad576bc2760dc5ece620781f06a91905e6e9d1982`

```dockerfile
```

-	Layers:
	-	`sha256:1880c92364491db2068ea984228629ad8046cc63706181fee11e50ef30e80e6e`  
		Last Modified: Fri, 07 Nov 2025 00:21:13 GMT  
		Size: 11.7 MB (11696677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a343ec9af660a77d325cf34e8caaa792084b850ee100b6e6f105639f82511f1b`  
		Last Modified: Fri, 07 Nov 2025 00:21:14 GMT  
		Size: 21.7 KB (21713 bytes)  
		MIME: application/vnd.in-toto+json
