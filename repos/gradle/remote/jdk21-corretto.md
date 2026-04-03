## `gradle:jdk21-corretto`

```console
$ docker pull gradle@sha256:6d373213f94391df2337d2de4e643567e6c88035ef06d8cb28a31fc49da6afb8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk21-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:2e5da32126a54b022abda35c6a7177e2f2cefa30647a54e066503c4c18685fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.1 MB (448131051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4301fd9aa3f1f260286959d92e490923641bc2a26cf7403fb004b7e0301f0d4f`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:09:28 GMT
ARG version=21.0.10.7-1
# Fri, 03 Apr 2026 17:09:28 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:09:28 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:09:28 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:09:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 03 Apr 2026 17:29:20 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 17:29:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 17:29:20 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 17:29:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 17:29:20 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 17:29:20 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 17:29:20 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 03 Apr 2026 17:29:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 03 Apr 2026 17:29:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 17:29:23 GMT
USER gradle
# Fri, 03 Apr 2026 17:29:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 03 Apr 2026 17:29:23 GMT
USER root
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91612493fd72368b685c337f3f583067a94ee0ef306766e8d11839845e7daf8`  
		Last Modified: Fri, 03 Apr 2026 17:09:55 GMT  
		Size: 170.2 MB (170192316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac70a25fff02956d8c80cfb7bdf6b3a745672ca631ecbfc822e1879e9d19f6c`  
		Last Modified: Fri, 03 Apr 2026 17:29:52 GMT  
		Size: 86.1 MB (86070024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c28c6175bddfcea4bae96819665518baea925d0e61e4d1803783044a2d730e`  
		Last Modified: Fri, 03 Apr 2026 17:29:48 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06aacc45088eec62b4709e9e8b5b0a0269b2e56689cea74ead410d2a234703b9`  
		Last Modified: Fri, 03 Apr 2026 17:29:52 GMT  
		Size: 137.8 MB (137808333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab4f621440711f78de8dda1ae2072eb73abd7161aebb5c6c4286b8788d8d89c`  
		Last Modified: Fri, 03 Apr 2026 17:29:48 GMT  
		Size: 25.6 KB (25608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:bbd0ba84907072af2561a2e9a25c444b340e494bb49720fe7e0eadb2e51bc5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11350408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090ed3a8cfc69a5c48614e7a993cd861085426bf3117269f5e0b2692b910cd11`

```dockerfile
```

-	Layers:
	-	`sha256:17b16f5cccc1c1dbff50563957c8b73a58dbb4a2658950d36864a9653c4de1ba`  
		Last Modified: Fri, 03 Apr 2026 17:29:48 GMT  
		Size: 11.3 MB (11328758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c6443fcb67d419ef547be7a5886e58aa30162e1d1c99e632aeeee0a654db9bb`  
		Last Modified: Fri, 03 Apr 2026 17:29:48 GMT  
		Size: 21.6 KB (21650 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1e825919ec93642fd966ee586eb26bddeebac23e2479f24d3df77134ca0ed1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.8 MB (444789159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908e4ad199b598ae72dbbd52b2ab51228786dfa2bb88a61ce1f7513950253e59`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:16:52 GMT
ARG version=21.0.10.7-1
# Fri, 03 Apr 2026 17:16:52 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:16:52 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:16:52 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:16:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 03 Apr 2026 17:27:11 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 17:27:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 17:27:11 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 17:27:11 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 03 Apr 2026 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 03 Apr 2026 17:27:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 17:27:14 GMT
USER gradle
# Fri, 03 Apr 2026 17:27:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 03 Apr 2026 17:27:14 GMT
USER root
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1644240415892ae6adc3944665a6a99351819a4043adb69ab2e97d280a16aae6`  
		Last Modified: Fri, 03 Apr 2026 17:17:15 GMT  
		Size: 168.5 MB (168466722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535964826a5b77d1d90f61d8caabb7380731b9dca16143717134ac329378b9b9`  
		Last Modified: Fri, 03 Apr 2026 17:27:46 GMT  
		Size: 85.5 MB (85541717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950bd2fc17532552994876e0e1648a31ab091dd41017c07b189983f953f7ce3b`  
		Last Modified: Fri, 03 Apr 2026 17:27:42 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86779aab4c361c6efcacbfac44c8589fecee16900101255ccf67f68f2559e443`  
		Last Modified: Fri, 03 Apr 2026 17:27:48 GMT  
		Size: 137.8 MB (137808332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da37ab8004843037abfe9592c9da89ee22951e61894cba107dc0b68e2600c725`  
		Last Modified: Fri, 03 Apr 2026 17:27:42 GMT  
		Size: 29.3 KB (29333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:bf1c5a3fdd5a4ec740433c3b99bf67cd9a8bb20385660c5a291c80055a4901a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11349608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c2231657bf29980cc307e50216ae257952751a33b1afa2c23bee3556b06613`

```dockerfile
```

-	Layers:
	-	`sha256:abbb3752e115315e51381d717e42b0d84fc25c64125f254cf4dac46f0bd0407c`  
		Last Modified: Fri, 03 Apr 2026 17:27:43 GMT  
		Size: 11.3 MB (11327760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:474583f1f22abf4b5ff60ae6aab06f4fed8b7dd7ea570aea945bc9ba06fe0967`  
		Last Modified: Fri, 03 Apr 2026 17:27:42 GMT  
		Size: 21.8 KB (21848 bytes)  
		MIME: application/vnd.in-toto+json
