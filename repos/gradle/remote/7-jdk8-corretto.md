## `gradle:7-jdk8-corretto`

```console
$ docker pull gradle@sha256:baeb066eb0b60a994e716ed6bcaebe2d90e28558850ed67995bfb614523202fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:2a0c926b3a5c6352e05f94f6d11c997ed18d6200ab038b993d395e31e6fe9fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.3 MB (559316706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebdefbbf4af2247950f7941905fd8707469251b82fb08d367c6a5aaf65fdad75`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:23:11 GMT
COPY /rootfs/ / # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:23:11 GMT
ARG version=1.8.0_452.b09-1
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: version=1.8.0_452.b09-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENV LANG=C.UTF-8
# Sun, 30 Mar 2025 18:23:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:23:11 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_VERSION=7.6.4
# Sun, 30 Mar 2025 18:23:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER gradle
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER root
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32848075c7081f2fe7eb81d0ef0f244572848c72b0b29722f2dbd36e85414491`  
		Last Modified: Tue, 15 Apr 2025 23:56:39 GMT  
		Size: 328.8 MB (328785081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0aee8f2906cf71415b4d41eab07dbd2554e2ea1d3cc9549f79d7bbf95cba21`  
		Last Modified: Wed, 16 Apr 2025 00:08:56 GMT  
		Size: 51.8 MB (51837190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70ccef9998f2e796928452e439480a8ac5bbd9c5147fbb45284a6d570a13602`  
		Last Modified: Wed, 16 Apr 2025 00:08:55 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dadff7770a67b0e250d53e1ad5566b2f45a1ebd5e871230a39829b23e8e2fbd`  
		Last Modified: Wed, 16 Apr 2025 00:08:57 GMT  
		Size: 122.7 MB (122730507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f8fd1ec122d2abf959b773b9951fc3ac4267e6aa207ff945732df7e48da16f`  
		Last Modified: Wed, 16 Apr 2025 00:08:55 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:d006f1fad96bf938e0062ea801bbfbc95f9f84bf1f18e164cc17708698d626f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17477077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b616f5bba0a83ed2dc6e95715b6a507b21f348b43dae53f3b930309da37e8764`

```dockerfile
```

-	Layers:
	-	`sha256:bbf547e03564f74f3dcaf36342c82c5436f1f067de260ccce94c96496a228d93`  
		Last Modified: Wed, 16 Apr 2025 00:08:55 GMT  
		Size: 17.5 MB (17457827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7e697b9795a1f91fcb9d6c29996d87d671712531a1bf60cc7b37791f42adcb7`  
		Last Modified: Wed, 16 Apr 2025 00:08:55 GMT  
		Size: 19.2 KB (19250 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:820b2edcff6792ff15a673a49741feae39c44f2651401635be09a928c99431ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.6 MB (365646105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e02168ac5a34cdba533bed313ef5bc020f9ec0f96b97ba3ab2a4af283855f1c`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:23:11 GMT
COPY /rootfs/ / # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:23:11 GMT
ARG version=1.8.0_452.b09-1
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: version=1.8.0_452.b09-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENV LANG=C.UTF-8
# Sun, 30 Mar 2025 18:23:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:23:11 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_VERSION=7.6.4
# Sun, 30 Mar 2025 18:23:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER gradle
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER root
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eeb1785ecbd42f2418ca7fde3d9206f686229d30624028cc939c484353fae0f`  
		Last Modified: Tue, 15 Apr 2025 23:56:08 GMT  
		Size: 117.9 MB (117930711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec34ba379527cfd87e7a4d2a110a432765150e3ac7e28fdd01a90f7e28a65ec`  
		Last Modified: Wed, 16 Apr 2025 00:27:51 GMT  
		Size: 70.0 MB (69962669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c05847fc4f3cfe8f457ca10adaca490f168476f962cae333e26691016726f2`  
		Last Modified: Wed, 16 Apr 2025 00:27:48 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7666b1cb0a823f70617368a84df9f414dc5aa44942bd2a0c2b143f66719b7999`  
		Last Modified: Wed, 16 Apr 2025 00:29:11 GMT  
		Size: 122.7 MB (122730509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a8c0e4a0a79094c3bdf523235b2fd27a4065e276d1e439ece856df73f92b64`  
		Last Modified: Wed, 16 Apr 2025 00:29:07 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:77daf74f28fef88da5bd886a12736b6f00d6811848ab3617ce51d5f2afe40368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11053042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b6f3651f9e068ac58539537e1c424f929b762bd7f87ad57f94647ae661818c`

```dockerfile
```

-	Layers:
	-	`sha256:45265b0477d364be2afdc9c802c4bb48e3542c670a7f84df9d8d9466401d428b`  
		Last Modified: Wed, 16 Apr 2025 00:29:08 GMT  
		Size: 11.0 MB (11033619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35467f6272ff48533c6e7caf72999e273a77ea6d951ac85fa38e0686f5dad8b6`  
		Last Modified: Wed, 16 Apr 2025 00:29:07 GMT  
		Size: 19.4 KB (19423 bytes)  
		MIME: application/vnd.in-toto+json
