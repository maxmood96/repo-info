## `gradle:8-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:8f18b0c18d3e4832c03ad34427fdfd74387d6545cf696a683a0376e413f0a81b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:0875ec47c3e750343bb60d5a3b51a8841d1d2b32d230329ae0b88c9da1fb48af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.5 MB (434454416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93bd597dc5e0bea8b8333b7378866c0e9c729b8c8ae770721b3fa124cbc24d0`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:01 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:13:35 GMT
ARG version=17.0.18.9-1
# Mon, 02 Mar 2026 23:13:35 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:13:35 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:13:35 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:13:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 03 Mar 2026 00:12:08 GMT
CMD ["gradle"]
# Tue, 03 Mar 2026 00:12:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Mar 2026 00:12:08 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 03 Mar 2026 00:12:09 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 03 Mar 2026 00:12:09 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Mar 2026 00:12:09 GMT
WORKDIR /home/gradle
# Tue, 03 Mar 2026 00:12:09 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 03 Mar 2026 00:12:09 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 03 Mar 2026 00:12:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 03 Mar 2026 00:12:11 GMT
USER gradle
# Tue, 03 Mar 2026 00:12:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 03 Mar 2026 00:12:12 GMT
USER root
```

-	Layers:
	-	`sha256:2584a8e504dfaf493eadaafafbabd8b97f7cb5bbe3cb6a319fb37cf3c4335d86`  
		Last Modified: Thu, 19 Feb 2026 02:57:43 GMT  
		Size: 54.0 MB (54032840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291656abe10718a5b7ecb3affcd502d6d49aac432bab42c4affe10d8907b4b47`  
		Last Modified: Mon, 02 Mar 2026 23:13:54 GMT  
		Size: 156.9 MB (156911090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea640e8bcf291ea5b4e54bce8e0ac1882a11e3789803533cb74d44761ec5f00d`  
		Last Modified: Tue, 03 Mar 2026 00:12:41 GMT  
		Size: 86.1 MB (86065610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6cd3ad9c44e1fa3e9da703d6fea6a2b79f8711f8ae193a9c4ba1f1bf695176`  
		Last Modified: Tue, 03 Mar 2026 00:12:37 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9540cc656aac5778d91bb212e2fdec0254e93622e6a7e5b188a8023ec3578da7`  
		Last Modified: Tue, 03 Mar 2026 00:12:42 GMT  
		Size: 137.4 MB (137388295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46f09ea56cef25aec9dbfd30bfddfee0f515a36fa577cf8f8f81e1a4b9b128d`  
		Last Modified: Tue, 03 Mar 2026 00:12:37 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:f0ff2081340cbde87a61db53716fcb7995fed983da39e11b4a86be106853798d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11360656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87f2dcdc44c08022b312ae6364fb293b65ca21470c4eae3a426aa456bfe4113`

```dockerfile
```

-	Layers:
	-	`sha256:89c5ec4e7553b84567790ae570a3fe41f4c76adf312e3da528a1c2b081f578c0`  
		Last Modified: Tue, 03 Mar 2026 00:12:38 GMT  
		Size: 11.3 MB (11339929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:196342bee8558c0b26bfaaed7976d8b51a72ace12aee657b4689e93f8d1c8549`  
		Last Modified: Tue, 03 Mar 2026 00:12:37 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:7d54e85d4b10573d65eeb0cc398f18b83096751994e5beec971bfda14539203d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.7 MB (431662634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30cf7757948c1b6b740b97d13db7e2f0c8d4f2c54af2ecf09f079720486ae6a1`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:04 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:14:40 GMT
ARG version=17.0.18.9-1
# Mon, 02 Mar 2026 23:14:40 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:14:40 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:14:40 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:14:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 03 Mar 2026 00:12:44 GMT
CMD ["gradle"]
# Tue, 03 Mar 2026 00:12:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Mar 2026 00:12:44 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 03 Mar 2026 00:12:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 03 Mar 2026 00:12:44 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Mar 2026 00:12:44 GMT
WORKDIR /home/gradle
# Tue, 03 Mar 2026 00:12:44 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 03 Mar 2026 00:12:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 03 Mar 2026 00:12:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 03 Mar 2026 00:12:47 GMT
USER gradle
# Tue, 03 Mar 2026 00:12:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 03 Mar 2026 00:12:47 GMT
USER root
```

-	Layers:
	-	`sha256:9330fae67a20d9aa2569828674140d8b67d50cfd127cb99ba0f9be275d35f976`  
		Last Modified: Thu, 19 Feb 2026 02:57:42 GMT  
		Size: 52.9 MB (52941319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458a2c883ef0e813dd59cc98f7ab9fa2c67d320d0117be74523be410b68ca3ed`  
		Last Modified: Mon, 02 Mar 2026 23:15:03 GMT  
		Size: 155.7 MB (155727670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0280b29986d4bb71ac4d67dd16602b6c7a67e9393114ede1405e4c1a7c762e75`  
		Last Modified: Tue, 03 Mar 2026 00:13:19 GMT  
		Size: 85.5 MB (85544179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2b94415e6a26f054b46d85d8a884ade314e9b76ce1a484fd22038526983f6`  
		Last Modified: Tue, 03 Mar 2026 00:13:15 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4092646ad484680a26dad3c81aaa9b661ae7a9953975249a25b7b1a5deba00a7`  
		Last Modified: Tue, 03 Mar 2026 00:13:20 GMT  
		Size: 137.4 MB (137388269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45b7c662efd9628f7fb69e282037c0bed9cf9a7d9f2f3beaad5a8e90063c1d7`  
		Last Modified: Tue, 03 Mar 2026 00:13:15 GMT  
		Size: 59.5 KB (59520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:5a5aef759ebd11e7f643281798e514f61a60a531c387dfeea947e27736ab2c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11359804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec4e7596e79f13e59bec0c03b8eaef8ee39d1010b75e64fa650b40f9653fcbf`

```dockerfile
```

-	Layers:
	-	`sha256:287d358ca84140791ce581c27284ed3f94a19ca108d733663dc369b6ef2e6f17`  
		Last Modified: Tue, 03 Mar 2026 00:13:16 GMT  
		Size: 11.3 MB (11338904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a45f9060dc5ffa3cb4f586d7960ffde8a2eb53a796dc22b5295d231d285e7382`  
		Last Modified: Tue, 03 Mar 2026 00:13:15 GMT  
		Size: 20.9 KB (20900 bytes)  
		MIME: application/vnd.in-toto+json
