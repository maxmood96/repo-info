## `gradle:7-jdk17-corretto`

```console
$ docker pull gradle@sha256:2aac5cefc147c151df4db01d9644a8199e67f030f839319ac3d6c6aae5fe3b15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:4579f6eb111e84139c286837852c610616b9c7b81437010020b0e4f5a30fa36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.4 MB (426404748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:203e8fb3b8a00f3a12b1eeb6e840cc09ec1f7eb60a3cb933ccad304988c43b3b`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:40 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:12:23 GMT
ARG version=17.0.19.10-1
# Fri, 24 Apr 2026 00:12:23 GMT
ARG package_version=1
# Fri, 24 Apr 2026 00:12:23 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:12:23 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:12:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 24 Apr 2026 01:11:59 GMT
CMD ["gradle"]
# Fri, 24 Apr 2026 01:11:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 24 Apr 2026 01:11:59 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 24 Apr 2026 01:11:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 24 Apr 2026 01:11:59 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 24 Apr 2026 01:11:59 GMT
WORKDIR /home/gradle
# Fri, 24 Apr 2026 01:11:59 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 24 Apr 2026 01:11:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 24 Apr 2026 01:12:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 24 Apr 2026 01:12:02 GMT
USER gradle
# Fri, 24 Apr 2026 01:12:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 24 Apr 2026 01:12:02 GMT
USER root
```

-	Layers:
	-	`sha256:60406c832328f9a4f3aa21eb9cb5b2182d79ad008cd21f0bbac4517c1836be2e`  
		Last Modified: Tue, 14 Apr 2026 01:03:42 GMT  
		Size: 54.6 MB (54569705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477e9f05faae959d6f84685f2d7a1a34f252a50c991cef521592fa0ba7eb6e19`  
		Last Modified: Fri, 24 Apr 2026 00:12:45 GMT  
		Size: 157.2 MB (157155286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c07e272c267c2d9472b3be8271067923b80affc06c5747fc03fd313f28c1c7e`  
		Last Modified: Fri, 24 Apr 2026 01:12:33 GMT  
		Size: 86.2 MB (86153766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c2dd96d81ae08c1a58ed58bc2599cdccd3744172672fb1f08895c9f14c7b33`  
		Last Modified: Fri, 24 Apr 2026 01:12:27 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d950909e502bec502f61f61a909af7b537c701d3753fc28bc1b84610718df290`  
		Last Modified: Fri, 24 Apr 2026 01:12:34 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c87bca93b7ec77a519e19d7aecca8c1241015a983fbf6f1cb62795a2562721`  
		Last Modified: Fri, 24 Apr 2026 01:12:27 GMT  
		Size: 54.9 KB (54895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:8a41566ff67cb3ea1b42f408f50f5cb02b3b0627678caa4dd25a9f417f0a4e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11281518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f174c418bc2c4db06441910391bab60f304e14f1127b7fabb8d5d8ad63f231a5`

```dockerfile
```

-	Layers:
	-	`sha256:d0b6fc154c8a7583863c830ed161450815e057b7276989006430fd29bdd3e7d2`  
		Last Modified: Fri, 24 Apr 2026 01:12:28 GMT  
		Size: 11.3 MB (11260805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5123766ba92fa9bb74526319c3a067fbe26a6cbc34c997a0b8aa93dc530024b0`  
		Last Modified: Fri, 24 Apr 2026 01:12:28 GMT  
		Size: 20.7 KB (20713 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8d3427e50224800e19e0b677f7963e1bf2cc6829df6a3d9fb8f113f9f2ed3c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.6 MB (423627773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6856a2d767b11a1a81068796d69c8e9373ce7372bfeb852014b4d1a1eb6f4d1`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:02 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:11:41 GMT
ARG version=17.0.19.10-1
# Fri, 24 Apr 2026 00:11:41 GMT
ARG package_version=1
# Fri, 24 Apr 2026 00:11:41 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:11:41 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:11:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 24 Apr 2026 01:12:10 GMT
CMD ["gradle"]
# Fri, 24 Apr 2026 01:12:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 24 Apr 2026 01:12:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 24 Apr 2026 01:12:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 24 Apr 2026 01:12:11 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 24 Apr 2026 01:12:11 GMT
WORKDIR /home/gradle
# Fri, 24 Apr 2026 01:12:11 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 24 Apr 2026 01:12:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 24 Apr 2026 01:12:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 24 Apr 2026 01:12:13 GMT
USER gradle
# Fri, 24 Apr 2026 01:12:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 24 Apr 2026 01:12:14 GMT
USER root
```

-	Layers:
	-	`sha256:a89c935522476873ac76a02a8b4103cba17c6900bdcb1d98998ed64657edf59f`  
		Last Modified: Tue, 14 Apr 2026 02:24:36 GMT  
		Size: 53.5 MB (53452253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19190c1206066bd46b5a1a6031fd9b5849728dcd0c5a9c3b3c243071f3d9160`  
		Last Modified: Fri, 24 Apr 2026 00:12:03 GMT  
		Size: 156.0 MB (155987864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71a08fb76103a613908d50ef5fe0f4193fed853efe372030c1651d46238bce9`  
		Last Modified: Fri, 24 Apr 2026 01:12:46 GMT  
		Size: 85.7 MB (85656992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2031d855296ccc3afc187bac83ebf9163314eeb155aab13e4ce484546d93dc`  
		Last Modified: Fri, 24 Apr 2026 01:12:42 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b773165dbc6c41c17bbb8a6aed37bb9ad7669d93cdbc76f0fca501742f370a2b`  
		Last Modified: Fri, 24 Apr 2026 01:12:47 GMT  
		Size: 128.5 MB (128469463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce5748beec5de5251555e59e7939ca3acac27219a9d8f42aa6492aa4d2d5c15`  
		Last Modified: Fri, 24 Apr 2026 01:12:43 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:581a8422745117070579ef26bd2375bb5dd906457d5bddd49632cf9e2d68dd0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11280671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d2ca1dccc659ee9b1cc7bcc70a359f295848a34867b0f6e4d0c50e1dfe268d`

```dockerfile
```

-	Layers:
	-	`sha256:91890c8e50e5c88f414acf4268b63430cb1c5e47db10eab5e6327ef640eeb281`  
		Last Modified: Fri, 24 Apr 2026 01:12:43 GMT  
		Size: 11.3 MB (11259785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59cd387dc47083d852d2eeb0fe29cfd7b9a47eccb98996f761c16a4a77727bd0`  
		Last Modified: Fri, 24 Apr 2026 01:12:42 GMT  
		Size: 20.9 KB (20886 bytes)  
		MIME: application/vnd.in-toto+json
