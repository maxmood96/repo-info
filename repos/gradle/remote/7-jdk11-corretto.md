## `gradle:7-jdk11-corretto`

```console
$ docker pull gradle@sha256:c76d19acc21a04e0afc09ad1810b5af6787e8585037c9c0ce06860b84f518d56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:9824bd2ec9fe20ca9d2a54276a8dcebc55e704f8a6c09d2c4bbb9cd54a54abdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.0 MB (421994499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d785ff60bfeae00487054eafc5d97ef789db0281817c1c8e088bdf303d49cb2`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:01 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:11:21 GMT
ARG version=11.0.30.7-1
# Mon, 02 Mar 2026 23:11:21 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:11:21 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:11:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 03 Mar 2026 00:12:19 GMT
CMD ["gradle"]
# Tue, 03 Mar 2026 00:12:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Mar 2026 00:12:19 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 03 Mar 2026 00:12:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 03 Mar 2026 00:12:20 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Mar 2026 00:12:20 GMT
WORKDIR /home/gradle
# Tue, 03 Mar 2026 00:12:20 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 03 Mar 2026 00:12:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 03 Mar 2026 00:12:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 03 Mar 2026 00:12:22 GMT
USER gradle
# Tue, 03 Mar 2026 00:12:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 03 Mar 2026 00:12:23 GMT
USER root
```

-	Layers:
	-	`sha256:2584a8e504dfaf493eadaafafbabd8b97f7cb5bbe3cb6a319fb37cf3c4335d86`  
		Last Modified: Thu, 19 Feb 2026 02:57:43 GMT  
		Size: 54.0 MB (54032840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bad2af03af5188a3cc6de4fd433994d98208a28c2aadd7bd215b1c171939319`  
		Last Modified: Mon, 02 Mar 2026 23:11:43 GMT  
		Size: 153.4 MB (153362633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6a5a5efdabce542a88ad78beb913d97d078f5c13420191f06e423d197b6608`  
		Last Modified: Tue, 03 Mar 2026 00:12:54 GMT  
		Size: 86.1 MB (86073020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293dd4a084be3bf710b7eec58379700706cc2926e57bc3558bb3175368c43753`  
		Last Modified: Tue, 03 Mar 2026 00:12:50 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868a07be03319a609ef7334d220018d02dbbb3f4bcc17176edfd27913db7a20b`  
		Last Modified: Tue, 03 Mar 2026 00:12:55 GMT  
		Size: 128.5 MB (128469414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e6ed2f4f8bbb68c1b6c6739387ebc93cdbfc147c1086a4deacee793866ab41`  
		Last Modified: Tue, 03 Mar 2026 00:12:50 GMT  
		Size: 54.9 KB (54911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:326c0094184b0cdfe7bd670a0d1c80d728275fcb7f7e396faeb0f9577a946a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11296949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baefd45d05db33d96fa4bb01624aa00afe5354e0d92cd2a4fa9ff5eda0d5293c`

```dockerfile
```

-	Layers:
	-	`sha256:dc759272650012905a27a1857e29e6eb9ededb3cb1b955556809ac1d2b438741`  
		Last Modified: Tue, 03 Mar 2026 00:12:51 GMT  
		Size: 11.3 MB (11276078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37373cf533b60f24a2d1f3538e096bae909b5a40094c482bf91ed250d5e9338`  
		Last Modified: Tue, 03 Mar 2026 00:12:50 GMT  
		Size: 20.9 KB (20871 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:4af0330895679d8687111e8d1f6531ac6b8de0839e69c6f9c0a46c0afd0e1a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.9 MB (418940622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80522dd74cfaff2ee2ba65d6f2db4e4ece3fe5064862cb7b9ac218e8849a0253`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:04 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:12:32 GMT
ARG version=11.0.30.7-1
# Mon, 02 Mar 2026 23:12:32 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:12:32 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:12:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 03 Mar 2026 00:12:55 GMT
CMD ["gradle"]
# Tue, 03 Mar 2026 00:12:55 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Mar 2026 00:12:55 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 03 Mar 2026 00:12:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 03 Mar 2026 00:12:56 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Mar 2026 00:12:56 GMT
WORKDIR /home/gradle
# Tue, 03 Mar 2026 00:12:56 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 03 Mar 2026 00:12:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 03 Mar 2026 00:12:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 03 Mar 2026 00:12:58 GMT
USER gradle
# Tue, 03 Mar 2026 00:12:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 03 Mar 2026 00:12:59 GMT
USER root
```

-	Layers:
	-	`sha256:9330fae67a20d9aa2569828674140d8b67d50cfd127cb99ba0f9be275d35f976`  
		Last Modified: Thu, 19 Feb 2026 02:57:42 GMT  
		Size: 52.9 MB (52941319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7350756942f6b9b7af025da5fd26f1c03d9276b1ea1bc9aa9432be6e9b01612`  
		Last Modified: Mon, 02 Mar 2026 23:12:53 GMT  
		Size: 151.9 MB (151924448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea7aac593c8317a06e4ada8cc0ccdb27c89dc533f1664c1332c9d56761cd69c`  
		Last Modified: Tue, 03 Mar 2026 00:13:30 GMT  
		Size: 85.5 MB (85544221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d528ce1a442cf45cf08fc2c2da63b2da99d8a509c83df87bc41c46995e1c78d`  
		Last Modified: Tue, 03 Mar 2026 00:13:26 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c814d011b32d90130f39cc8dbcbb88a32d9f6db5b6a86f20345ee9069b0bc07a`  
		Last Modified: Tue, 03 Mar 2026 00:13:31 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b441e1df915dca58674752b3db2f93f5438d792dde71a39413ec839968dbfd56`  
		Last Modified: Tue, 03 Mar 2026 00:13:27 GMT  
		Size: 59.5 KB (59536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:d826a6454f945441b3efa39db763a9e1ca27bfb7820d5328e16648352c865b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11296941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42334be075bf9326e8fe18efd2f8e561a742ceec587596840842e94b174379d0`

```dockerfile
```

-	Layers:
	-	`sha256:21fa65d2ad99645e374d68d56ee48b67deb0b691dbb80401747431d46bb1a399`  
		Last Modified: Tue, 03 Mar 2026 00:13:27 GMT  
		Size: 11.3 MB (11275897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fea16c413eeef1f6c5d8cee5ad2c09fde7dccbe000e77a6eef95231ca62eab3`  
		Last Modified: Tue, 03 Mar 2026 00:13:26 GMT  
		Size: 21.0 KB (21044 bytes)  
		MIME: application/vnd.in-toto+json
