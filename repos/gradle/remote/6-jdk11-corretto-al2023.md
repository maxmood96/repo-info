## `gradle:6-jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:f08da59b8f7795d99d1a9194e298d8f1dad8a6461386614d7387fada2ab6012c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:481941ecdf6d46bc94d20322c5aeb64f1f17bf4660e9df349f379c72a10fe9e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.8 MB (401768303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd4d75278218b9f09150848308572438f7adf590dd8648d9c716e2457c1978`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 23 Sep 2025 15:36:53 GMT
CMD ["gradle"]
# Tue, 23 Sep 2025 15:36:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 23 Sep 2025 15:36:53 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 23 Sep 2025 15:36:53 GMT
WORKDIR /home/gradle
# Tue, 23 Sep 2025 15:36:53 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 23 Sep 2025 15:36:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 23 Sep 2025 15:36:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
USER gradle
# Tue, 23 Sep 2025 15:36:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
USER root
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bea491ccf4f1cb4479c0d0dd695e9eaea15d1c73558a4e304bd3314fb876293`  
		Last Modified: Mon, 06 Oct 2025 22:11:15 GMT  
		Size: 154.1 MB (154072396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11acdbf2bf489a71acc78ab6b9550ffe05cf1917188408a6e9c02ed106748517`  
		Last Modified: Mon, 06 Oct 2025 22:13:07 GMT  
		Size: 85.6 MB (85561164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb22a721b076d7d349c9925cbbd6887392112bba2cd69b75ecc947bf7b9dace`  
		Last Modified: Mon, 06 Oct 2025 22:13:03 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccb1adf727edfb44302aa26f92f3cb99bf29b05c71983d1566e0c6642217d09`  
		Last Modified: Mon, 06 Oct 2025 22:13:13 GMT  
		Size: 107.7 MB (107696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84e065ddf0cf4e800881ddc00cf523f02b422f7592a09987f3569941053d181`  
		Last Modified: Mon, 06 Oct 2025 22:13:01 GMT  
		Size: 431.3 KB (431269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:f0fb35c7f9f10e601a6c0e111cfe4d0d17f12f0f0f13ea90d8bcff382db40c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11250642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235bf3c274a8ae7cef85c134744a90c3af009eb909f9ca115f876cc7227ce612`

```dockerfile
```

-	Layers:
	-	`sha256:8bc92a60b5067fda189cf4b67a6e0e43e35c3c286883cdde8537b5506456bada`  
		Last Modified: Mon, 06 Oct 2025 23:17:32 GMT  
		Size: 11.2 MB (11229728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75cf1224be5e94fbae1fc6858ddbb1d5552fa4bf25d5cac0d2f920e901be99a0`  
		Last Modified: Mon, 06 Oct 2025 23:17:33 GMT  
		Size: 20.9 KB (20914 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2eb98c8e787a24512d03d2aebf6997acdfd27e150394e54b353b33291c8e2fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.0 MB (397999506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc526722c8fb8d3380fe70add581c911164d48bd344c952111eb809baf59266`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 23 Sep 2025 15:36:53 GMT
COPY /rootfs/ / # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 15:36:53 GMT
ARG version=11.0.29.7-1
# Tue, 23 Sep 2025 15:36:53 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
ENV LANG=C.UTF-8
# Tue, 23 Sep 2025 15:36:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 23 Sep 2025 15:36:53 GMT
CMD ["gradle"]
# Tue, 23 Sep 2025 15:36:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 23 Sep 2025 15:36:53 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 23 Sep 2025 15:36:53 GMT
WORKDIR /home/gradle
# Tue, 23 Sep 2025 15:36:53 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 23 Sep 2025 15:36:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 23 Sep 2025 15:36:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
USER gradle
# Tue, 23 Sep 2025 15:36:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
USER root
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb019a3f1f00a60c8fbf7e540ee825161e5b88894ff362d064122d819fd83d5`  
		Last Modified: Tue, 21 Oct 2025 22:12:10 GMT  
		Size: 151.9 MB (151897060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d923db12405d2dbf2dbc76376169a38f1c77328e3bc64eeaf095a08cfa0d7faa`  
		Last Modified: Tue, 21 Oct 2025 22:13:55 GMT  
		Size: 85.1 MB (85087863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8a7c6074e42b33e36e77b87a53cf57d3f64992f2dc23307007cff9618543bd`  
		Last Modified: Tue, 21 Oct 2025 22:13:45 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07c730d4ea92032e468331173be41a30601c88637c9d678ce9c75d1b5afb3df`  
		Last Modified: Wed, 22 Oct 2025 02:46:25 GMT  
		Size: 107.7 MB (107696668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1977bed6669aec8009385412707dfb8df2239ad8cff313f2f70e01c87a1a3334`  
		Last Modified: Tue, 21 Oct 2025 22:13:46 GMT  
		Size: 425.0 KB (425032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:db93e07ba254a8e5d51d7e8a85b24158a49ea564ce690ba36bd1ca5c0f229a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11250634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e275aeedcd3dd4fe9ca5d6d0059408bb2a7c4f2e8e9e5d9fbf2ca5530a5d3d55`

```dockerfile
```

-	Layers:
	-	`sha256:3755678821072e971b5766e42019928d1a63b91faa051e67548f953aa1d50992`  
		Last Modified: Tue, 21 Oct 2025 23:17:31 GMT  
		Size: 11.2 MB (11229547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:435aee9323fd145ea893cf692c6780c5a861f57138106a344cfbbb9f074ec13f`  
		Last Modified: Tue, 21 Oct 2025 23:17:32 GMT  
		Size: 21.1 KB (21087 bytes)  
		MIME: application/vnd.in-toto+json
