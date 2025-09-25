## `gradle:8-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:d2b8542ccfcc0e9e94179bcf23c2c568ba52951051e0696d000edf6d745c8c1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:8419f615d3d2aa3ddf77a3e2df668e6577cc2224f1afe3c8269a3814739bb91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.8 MB (433819647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a674a59353fa4bf5aa65dde85dec179502b7cb11592ff30f9a70062ad87129`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 12 Sep 2025 13:29:01 GMT
COPY /rootfs/ / # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
CMD ["/bin/bash"]
# Fri, 12 Sep 2025 13:29:01 GMT
ARG version=17.0.16.8-1
# Fri, 12 Sep 2025 13:29:01 GMT
ARG package_version=1
# Fri, 12 Sep 2025 13:29:01 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
ENV LANG=C.UTF-8
# Fri, 12 Sep 2025 13:29:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 12 Sep 2025 13:29:01 GMT
CMD ["gradle"]
# Fri, 12 Sep 2025 13:29:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Sep 2025 13:29:01 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
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
	-	`sha256:e12dd6684c9f24dc470a6beea3b0f60e59af88cc80973c45685158e242e9b972`  
		Last Modified: Thu, 25 Sep 2025 03:13:23 GMT  
		Size: 156.8 MB (156804152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3c8127cb68625a5dca7060bcaf02716e1c4c091e5e6bf837eafb8c7a6e6ebf`  
		Last Modified: Thu, 25 Sep 2025 03:16:05 GMT  
		Size: 85.6 MB (85558515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02445eecd6d44b79ef4b042f5c4b7bd6e7e0f7029528e5372d03cf29e0ddddb9`  
		Last Modified: Thu, 25 Sep 2025 03:15:54 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2114dd5b234b6811afcc1bb5440c6d9c060f1e231909bee55b83ce7ed4f234b0`  
		Last Modified: Thu, 25 Sep 2025 06:00:37 GMT  
		Size: 137.4 MB (137395132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c669c20dc9abc9f8a1a41b65b1c6e8d2fce2be225e2241e4ea0a88ef6649698e`  
		Last Modified: Thu, 25 Sep 2025 03:15:54 GMT  
		Size: 54.9 KB (54892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:808ae0a2e583830a7577791f58a60a9390db4d92c5f09db9f98a9e96d74adcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11332267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c092280f58395e1effe277406b34e69db6bccf45b3590d647cfc82756634851`

```dockerfile
```

-	Layers:
	-	`sha256:75e65fd7241bc6158973065505e34c568d872460a0fe66d48e457157c24055ec`  
		Last Modified: Thu, 25 Sep 2025 05:20:43 GMT  
		Size: 11.3 MB (11311497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c397580dcf608a58859d99c50aad0237ef937b35ae43a0fbb80b636b0539c42`  
		Last Modified: Thu, 25 Sep 2025 05:20:44 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e9275d6a78b98cbbac58dc9323763b91ce77acc124d85f0480b07499e4bec56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 MB (431032720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d454d06204e1a71bcced850b0397f41de9b4d4aea6e1015c7b3efdc27280e027`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 12 Sep 2025 13:29:01 GMT
COPY /rootfs/ / # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
CMD ["/bin/bash"]
# Fri, 12 Sep 2025 13:29:01 GMT
ARG version=17.0.16.8-1
# Fri, 12 Sep 2025 13:29:01 GMT
ARG package_version=1
# Fri, 12 Sep 2025 13:29:01 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
ENV LANG=C.UTF-8
# Fri, 12 Sep 2025 13:29:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 12 Sep 2025 13:29:01 GMT
CMD ["gradle"]
# Fri, 12 Sep 2025 13:29:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Sep 2025 13:29:01 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
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
	-	`sha256:a2fd24def9f1346651b22961e5b32ca8c4eb0ab12446d66c8a07c7a139ad48b7`  
		Last Modified: Wed, 24 Sep 2025 22:10:55 GMT  
		Size: 155.6 MB (155593727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9083a1fbdb25ab91a678cc952170892993e36442a0e53399ad0db5e51bef1e4b`  
		Last Modified: Wed, 24 Sep 2025 22:12:22 GMT  
		Size: 85.1 MB (85083135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745226536defcc7ecf05f3daaab327f6908e2c47cb694e02dd7e226141fd05ca`  
		Last Modified: Wed, 24 Sep 2025 22:12:17 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bca8e496222bdaa78c7258cfc94cca93b3c5ee282a1fdd8bf8ab4d141d5cc3`  
		Last Modified: Thu, 25 Sep 2025 05:35:32 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e590a44f4258889c7c2a03801025af00b3bc7002fb077f6ad05112dd0dacc57`  
		Last Modified: Wed, 24 Sep 2025 22:12:17 GMT  
		Size: 59.5 KB (59546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:0c60804be9c6ec3346d6cb122fde843e66e1f6d1747b9e73fbde821e173f0cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11331415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242808922b83970967040c394d20f9aace3212e19e19cc3a87ddd87174700ac6`

```dockerfile
```

-	Layers:
	-	`sha256:0376f31b04cba01f43b811edd9898ed6ec58a745eeedc3a31e49f3a51931c5b6`  
		Last Modified: Thu, 25 Sep 2025 02:20:48 GMT  
		Size: 11.3 MB (11310472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:324f9b7ee28a702c4b0632976feb82717f15533d6729634f6f219f0ce2ad5899`  
		Last Modified: Thu, 25 Sep 2025 02:20:48 GMT  
		Size: 20.9 KB (20943 bytes)  
		MIME: application/vnd.in-toto+json
