## `gradle:7-jdk11-corretto`

```console
$ docker pull gradle@sha256:6583b3367364aa169f45ff2e2d281c981602d36e1698b7337eee1c75e41afc6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:e73a007843be30543e7539f09ad78c48fb9af4a2acd963b04eba6ea9bdcd159e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.7 MB (422667340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fea0b5468d887b1fda58745af610de165a52941e3006c4a428547a9520a629`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:33:19 GMT
ARG version=11.0.31.11-1
# Wed, 22 Apr 2026 21:33:19 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:33:19 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 22 Apr 2026 22:12:19 GMT
CMD ["gradle"]
# Wed, 22 Apr 2026 22:12:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 22 Apr 2026 22:12:19 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 22 Apr 2026 22:12:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 22 Apr 2026 22:12:19 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 22 Apr 2026 22:12:19 GMT
WORKDIR /home/gradle
# Wed, 22 Apr 2026 22:12:19 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 22 Apr 2026 22:12:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 22 Apr 2026 22:12:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 22 Apr 2026 22:12:22 GMT
USER gradle
# Wed, 22 Apr 2026 22:12:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 22 Apr 2026 22:12:22 GMT
USER root
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a88a81ff0950e289635eefbfbb2c99d4e5fa9802747adfbe0deab3edf23eb`  
		Last Modified: Wed, 22 Apr 2026 21:33:40 GMT  
		Size: 153.5 MB (153477599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddd59a8366e5216b058929af205d1b21c5b168ee9c68bbbf22d6c55e483cfa4`  
		Last Modified: Wed, 22 Apr 2026 22:12:52 GMT  
		Size: 86.1 MB (86092486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e49d13170c379081984435d1a4834844b3041113f7db7207f0796e23038423`  
		Last Modified: Wed, 22 Apr 2026 22:12:48 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf4a68654b304fca634d52894e84be32ac63e89162a4bc4491118d7e4e0354d`  
		Last Modified: Wed, 22 Apr 2026 22:12:52 GMT  
		Size: 128.5 MB (128469414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2e34205bce8e9602defa5f7022d14fd1713c42370d847a4cf158af5c1610c5`  
		Last Modified: Wed, 22 Apr 2026 22:12:48 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:d6a2d21d127ffc880863f7d03318a65b70aa705e9540c21d8dc389ce3ad1255e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11305044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd07f6bfdf5b6b32755e93981486f2bb688af937b2782151ef8d7f430c9f82e`

```dockerfile
```

-	Layers:
	-	`sha256:00a9aec0350a24de8dadbeeffec7c0f6ba220a51886f696f4b7bbb663effdc4e`  
		Last Modified: Wed, 22 Apr 2026 22:12:49 GMT  
		Size: 11.3 MB (11284173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b951c9f08d9eb1ff9efe14bfc725a54aec1cd460c818571c26585e7bf32384d9`  
		Last Modified: Wed, 22 Apr 2026 22:12:48 GMT  
		Size: 20.9 KB (20871 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:37c6624198b0f2f815adb344d0b52e8cc4eb413b11a1bfc179d954ab109994f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.6 MB (419628387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924f80508d577fc6df7cb1b13e2bd6db3fc5e7db30a48fe3c368a274bb9f2301`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:33:31 GMT
ARG version=11.0.31.11-1
# Wed, 22 Apr 2026 21:33:31 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:33:31 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 22 Apr 2026 22:12:01 GMT
CMD ["gradle"]
# Wed, 22 Apr 2026 22:12:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 22 Apr 2026 22:12:01 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 22 Apr 2026 22:12:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 22 Apr 2026 22:12:01 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 22 Apr 2026 22:12:01 GMT
WORKDIR /home/gradle
# Wed, 22 Apr 2026 22:12:01 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 22 Apr 2026 22:12:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 22 Apr 2026 22:12:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 22 Apr 2026 22:12:04 GMT
USER gradle
# Wed, 22 Apr 2026 22:12:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 22 Apr 2026 22:12:04 GMT
USER root
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a1e2a231db3544e8a7929f99d6ce37f195163dc73ffccb051764be2f886290`  
		Last Modified: Wed, 22 Apr 2026 21:33:54 GMT  
		Size: 152.1 MB (152053159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7ace6b7e1cfcf3fa832acd1dfabbbca57569ec5b25b1be2ce3b9f6b1069b89`  
		Last Modified: Wed, 22 Apr 2026 22:12:36 GMT  
		Size: 85.6 MB (85601867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bc77e3bbc654c845b22f6bbaefc71c0b33fe22eb8e587d02da245d32e0a5f0`  
		Last Modified: Wed, 22 Apr 2026 22:12:31 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8495e9e690dfe3b03f1d86268abfb8f8e61653a28a0aa5d4a921f08653cded36`  
		Last Modified: Wed, 22 Apr 2026 22:12:36 GMT  
		Size: 128.5 MB (128469415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02f64e4d344e81eb269061f80129efcb4d510870570fc96679e6409a49d746b`  
		Last Modified: Wed, 22 Apr 2026 22:12:31 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:b1383bb9a8d47660c5d2dc06b79d2c390a68867f2a34f7ab44e076376f32c6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11305036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0572d5fbf9ab3fd43df66d89d56f7aac8cb336e8e99a2c6f758d2a2ed22ebe9f`

```dockerfile
```

-	Layers:
	-	`sha256:4c7dd0db2e0043655dc06ec142ed7ed5cb7e85be894ad5a15c26deb2ab714dfd`  
		Last Modified: Wed, 22 Apr 2026 22:12:32 GMT  
		Size: 11.3 MB (11283992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbe971951bfa2c4ea127026214e4c295dc750e77fb9504a57aa44b1c3e6f02fa`  
		Last Modified: Wed, 22 Apr 2026 22:12:31 GMT  
		Size: 21.0 KB (21044 bytes)  
		MIME: application/vnd.in-toto+json
