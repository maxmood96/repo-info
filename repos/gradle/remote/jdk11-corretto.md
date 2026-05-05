## `gradle:jdk11-corretto`

```console
$ docker pull gradle@sha256:0236e875ddcd46eb2d76dd78cd2869ac6339ac08e5ab469542646109a7fe06d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:a4710da5d16a5486dcc1390d4fd07d8ceb35161c3031f6da81ac8fbd8ce598da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.7 MB (431662899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44163ac22b41bd5305214ca8af2cc0c59cf637d87e4a277db31f435939c6799`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:45 GMT
ARG version=11.0.31.11-1
# Mon, 04 May 2026 20:11:45 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:45 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 04 May 2026 20:42:11 GMT
CMD ["gradle"]
# Mon, 04 May 2026 20:42:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 04 May 2026 20:42:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 04 May 2026 20:42:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 04 May 2026 20:42:11 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 04 May 2026 20:42:11 GMT
WORKDIR /home/gradle
# Mon, 04 May 2026 20:42:11 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 04 May 2026 20:42:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 04 May 2026 20:42:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 04 May 2026 20:42:14 GMT
USER gradle
# Mon, 04 May 2026 20:42:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 04 May 2026 20:42:15 GMT
USER root
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177f5f6694b7a14aaccd527d192e8e76c94dfecbb9fdd2f8693b660e84198ec2`  
		Last Modified: Mon, 04 May 2026 20:12:07 GMT  
		Size: 153.5 MB (153472514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c399b9b09f570f6974ac0e699c2f380116395711d5499086825172b1ba6eee36`  
		Last Modified: Mon, 04 May 2026 20:42:46 GMT  
		Size: 86.2 MB (86168779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779b2e1ad2add44c3f9e2653487eb5d76e0e04184111a373cc129713bcfeb6e2`  
		Last Modified: Mon, 04 May 2026 20:42:42 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf21892d99739aa78228617539fcaf2e318bff2d5663c6877add7134ce1f40ee`  
		Last Modified: Mon, 04 May 2026 20:42:47 GMT  
		Size: 137.4 MB (137388268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8612f8b78ac57f8faec0a36d07c4bb581b2e65012d201dead4c3d1e787234af`  
		Last Modified: Mon, 04 May 2026 20:42:42 GMT  
		Size: 54.9 KB (54903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:bab17f572d65faeae2302ce1d45fc4390f66238f8bf25257f2f4dcbfa6919d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11397204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4d78e2d1f170b0f0c79f1080aac2dd65adffbbeccc851a52d08437edf581db`

```dockerfile
```

-	Layers:
	-	`sha256:9e09a1d123c0fd8cfecd7baa51c91ad222b7394760d780e0d0ce8c7e1b4534fe`  
		Last Modified: Mon, 04 May 2026 20:42:42 GMT  
		Size: 11.4 MB (11375681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f64f7784a8704c7679e82488a3f19bf31253f8d15fa1ba281d27467639dfa3f`  
		Last Modified: Mon, 04 May 2026 20:42:42 GMT  
		Size: 21.5 KB (21523 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c9d7315c9ec1e50d495c76ba8e56a06a97e2c11ae1d1a09b0ad9d1941310d54a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428615645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2b4858571a8adb6b22a78c6ee469457e17e5cc6c681984f432ce512635c95c`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:32 GMT
ARG version=11.0.31.11-1
# Mon, 04 May 2026 20:11:32 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:32 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 04 May 2026 20:42:19 GMT
CMD ["gradle"]
# Mon, 04 May 2026 20:42:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 04 May 2026 20:42:19 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 04 May 2026 20:42:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 04 May 2026 20:42:19 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 04 May 2026 20:42:20 GMT
WORKDIR /home/gradle
# Mon, 04 May 2026 20:42:20 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 04 May 2026 20:42:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 04 May 2026 20:42:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 04 May 2026 20:42:22 GMT
USER gradle
# Mon, 04 May 2026 20:42:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 04 May 2026 20:42:23 GMT
USER root
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838136ec5b6ab2b88d9936cfc6ef1491350d124ec8e540cec804c91561010d10`  
		Last Modified: Mon, 04 May 2026 20:11:53 GMT  
		Size: 152.1 MB (152051592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd30d4bc5b3914383f0952b9d189f125b374696bcdbef76e079c1f06ecd481b`  
		Last Modified: Mon, 04 May 2026 20:42:54 GMT  
		Size: 85.7 MB (85657800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7688e8a6ddd3d571a86480e5d81d8a2312115e438b90669d126156b4ef19be`  
		Last Modified: Mon, 04 May 2026 20:42:50 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b69a3e3f19f1c3e9eef315d63755cb54e3dce1daa604ed30a35ae964bbc8ccf`  
		Last Modified: Mon, 04 May 2026 20:42:55 GMT  
		Size: 137.4 MB (137388267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670b20ba568f4541520a5b09166ce327fd88cb4c543ebb0b1b2099b03df5668d`  
		Last Modified: Mon, 04 May 2026 20:42:50 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:1bc0ed6e0d3eb2454b867da91bc785e7adaab91c3efd80b5f0f5a0131bf67431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11397244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9259ef62e84301e27c8c5dfc6358ec886a2fc555789dbc4899df8b2e25db11f8`

```dockerfile
```

-	Layers:
	-	`sha256:1b38fd28d3612a2924abbad1724fd1a032ebb0e5c51ceac2dc28bcb793f16dab`  
		Last Modified: Mon, 04 May 2026 20:42:51 GMT  
		Size: 11.4 MB (11375524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecbdedaaba14920f61fff6f4c766cd19976a37f06b1264d021a8fc4e815a4b1f`  
		Last Modified: Mon, 04 May 2026 20:42:50 GMT  
		Size: 21.7 KB (21720 bytes)  
		MIME: application/vnd.in-toto+json
