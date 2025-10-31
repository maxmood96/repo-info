## `gradle:6-jdk8-corretto`

```console
$ docker pull gradle@sha256:e0b1b01acd8e7ffc862e7b6b0dd201f548788c469430d1553a7a4992fda8c814
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:f05823bbce141186e0844b995ee39ba4329696fb6b883024bdf707540d1277d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.0 MB (557976839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2794721371f233cc7fa8d8e6dc542f4e787f47bccb848dc85de18d05835bf36`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:25 GMT
ARG version=1.8.0_472.b08-1
# Fri, 31 Oct 2025 00:11:25 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:11:25 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 31 Oct 2025 01:12:42 GMT
CMD ["gradle"]
# Fri, 31 Oct 2025 01:12:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 31 Oct 2025 01:12:42 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 31 Oct 2025 01:12:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 31 Oct 2025 01:12:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 31 Oct 2025 01:12:42 GMT
WORKDIR /home/gradle
# Fri, 31 Oct 2025 01:12:42 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 31 Oct 2025 01:12:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 31 Oct 2025 01:12:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 31 Oct 2025 01:12:45 GMT
USER gradle
# Fri, 31 Oct 2025 01:12:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 31 Oct 2025 01:12:45 GMT
USER root
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d90a02718a2ec471735b22a7012a63f3b6fd6aa7b11464ff1edf280a2e204b8`  
		Last Modified: Fri, 31 Oct 2025 01:12:00 GMT  
		Size: 330.9 MB (330868176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4478c0ecd7f093a28d4c71746438f18a3e3c36ae428745e45a9cca00a459f75b`  
		Last Modified: Fri, 31 Oct 2025 01:13:45 GMT  
		Size: 65.0 MB (64977556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629450ba27c2a67cf7123e4cdc240d581d8eba066a0f1087d371863fa153e434`  
		Last Modified: Fri, 31 Oct 2025 01:13:33 GMT  
		Size: 1.9 KB (1942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb6d516e5749397d3a74e202f9f654f38ae580364e20f82efb2f6b8030c604e`  
		Last Modified: Fri, 31 Oct 2025 01:13:42 GMT  
		Size: 107.7 MB (107696635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bc2e93ab33a88b66be2243b202d4dd9a6ae0883225e2ee268e4debfce675aa`  
		Last Modified: Fri, 31 Oct 2025 01:13:34 GMT  
		Size: 431.3 KB (431263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:48067a6306c3356febefc50951025dbbb5554fdaea4c37d45a847b2c080d41b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18045435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477eda28c290d49c7bd9c8f02032ef398583b4991a18d8ec297c62613785a982`

```dockerfile
```

-	Layers:
	-	`sha256:42c9b6f9e3d7c6f0497ddc20f75c0cd06889e1a48eb088ddc74a54fa204ad89e`  
		Last Modified: Fri, 31 Oct 2025 02:17:41 GMT  
		Size: 18.0 MB (18024570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f379ad59523df2eb3cd0aa7d1bf9b0987439cc148083778acb1d552274d2b919`  
		Last Modified: Fri, 31 Oct 2025 02:17:42 GMT  
		Size: 20.9 KB (20865 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:510895fc6372e2c8c2581c4ebde5f291be3381fb622d06266fdb2b14760e616f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.1 MB (364137371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98057572989c54570b5cbf9eb9a969ad4f1f494a02695de75c1631457e475472`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:43 GMT
ARG version=1.8.0_472.b08-1
# Fri, 31 Oct 2025 00:11:43 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:11:43 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 31 Oct 2025 01:13:05 GMT
CMD ["gradle"]
# Fri, 31 Oct 2025 01:13:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 31 Oct 2025 01:13:05 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 31 Oct 2025 01:13:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 31 Oct 2025 01:13:06 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 31 Oct 2025 01:13:06 GMT
WORKDIR /home/gradle
# Fri, 31 Oct 2025 01:13:06 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 31 Oct 2025 01:13:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 31 Oct 2025 01:13:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 31 Oct 2025 01:13:08 GMT
USER gradle
# Fri, 31 Oct 2025 01:13:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 31 Oct 2025 01:13:08 GMT
USER root
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d388cefb5877034eb46c74035ba24455c55fff50dbbe8d7c47526c4022768c`  
		Last Modified: Fri, 31 Oct 2025 01:12:01 GMT  
		Size: 118.0 MB (117956928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fafe45721d1125c596676619a7951455cbab25b5d8da24db6d711f9c0c7ce4c`  
		Last Modified: Fri, 31 Oct 2025 01:13:52 GMT  
		Size: 85.2 MB (85155295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adde1b8c5b946b73764968b6aa07737911cf12997f798eda9adc51d95f1f574b`  
		Last Modified: Fri, 31 Oct 2025 01:13:45 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73988b133c350a1d975924554dad0688957f3841b0fe6b7bc4f5625ba850085c`  
		Last Modified: Fri, 31 Oct 2025 01:13:56 GMT  
		Size: 107.7 MB (107696605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8f1da9c64ef17c45623f7d401ef33084d56ad6ff1451fd866ee1428270b101`  
		Last Modified: Fri, 31 Oct 2025 01:13:45 GMT  
		Size: 425.0 KB (425011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:f3d1ce61ab71153aeedda08b32771d76dfabb02e0022507bb7d3ced6e5c1bce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11609773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910a275dc6c700370f4b49aa37aa3ddb53457a7376dc1e86734b2a49a9499405`

```dockerfile
```

-	Layers:
	-	`sha256:5474d505aa7bd4586c9f86572c7665b6b129fc325e2a2afcaba4d4eeb0efa302`  
		Last Modified: Fri, 31 Oct 2025 02:17:58 GMT  
		Size: 11.6 MB (11588736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cd1bf28f86ec6fac87aec23356eef108797080a16c0e5128f4c39011ab7ecd4`  
		Last Modified: Fri, 31 Oct 2025 02:17:58 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json
