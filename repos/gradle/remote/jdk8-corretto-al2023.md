## `gradle:jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:7e09538be821c9da707c47a8d4610670bd2ba13e5248f01c7e3594b4a2e3c816
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:0a50ef1b3394744c53a2b53388b2fa27d0d059bbd24f1f2b33bbb6b31b92fb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.7 MB (587740960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f502e128f91307d8114c8655cc0aebe7400fe9cfc21e1dc6989b084f93ef5bcf`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:34 GMT
ARG version=1.8.0_472.b08-1
# Thu, 15 Jan 2026 22:08:34 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:08:34 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:08:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 15 Jan 2026 23:09:04 GMT
CMD ["gradle"]
# Thu, 15 Jan 2026 23:09:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Jan 2026 23:09:04 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Jan 2026 23:09:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Jan 2026 23:09:04 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Jan 2026 23:09:04 GMT
WORKDIR /home/gradle
# Thu, 15 Jan 2026 23:09:04 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 15 Jan 2026 23:09:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 15 Jan 2026 23:09:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Jan 2026 23:09:07 GMT
USER gradle
# Thu, 15 Jan 2026 23:09:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Jan 2026 23:09:07 GMT
USER root
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:08:12 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9755244d844db1ed30b93a9af49eae47daeaa66b3de11403953bdb2262b76f3`  
		Last Modified: Thu, 15 Jan 2026 22:09:33 GMT  
		Size: 330.9 MB (330896662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949c462b06a07fd1e951d425dcd4324dafa1b786f5f56793c85aa44e31f3e224`  
		Last Modified: Thu, 15 Jan 2026 23:10:02 GMT  
		Size: 65.4 MB (65371016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7c6bb4ca60c2dce96cdce1409eda9731ace5748da69e85919e5f8566987824`  
		Last Modified: Thu, 15 Jan 2026 23:09:56 GMT  
		Size: 1.9 KB (1943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b798283d61081b0ad659e7d8d52fa64f64c5f090304ca9cf9e6869078421b7`  
		Last Modified: Thu, 15 Jan 2026 23:09:50 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83c7c11a664b4260d5a2743343bacf053407e4bf3fcfb08d76b8d8c96867498`  
		Last Modified: Thu, 15 Jan 2026 23:09:56 GMT  
		Size: 54.9 KB (54907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:416f41266eacf924f372f89bbae94b2983c967068a75e89fbc4f4ac8d8fbbe15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18175392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f6b9acd4ae2a532abf2054d6d2f3bb01a1f3d9a7f805ac1ffcb0d7665002fc`

```dockerfile
```

-	Layers:
	-	`sha256:d0c1b0114491eeb19e9ea376e0a6986fa647c8160ef7f43b72147f9fac14267a`  
		Last Modified: Thu, 15 Jan 2026 23:09:47 GMT  
		Size: 18.2 MB (18153877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee21d8f475c9b23bd5d7e5ca69ca66cf102666543735a37e7e223f5a5e1d5fe6`  
		Last Modified: Fri, 16 Jan 2026 00:28:27 GMT  
		Size: 21.5 KB (21515 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d65bced36bae8ac47c73163ec32955534553512eb3e3987b854c7e6e2692975b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393802990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a83df50e07d6a106edaf976eed098b421c2add2dd5041708c84eb102d66e4a`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:37 GMT
ARG version=1.8.0_472.b08-1
# Thu, 15 Jan 2026 22:08:37 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:08:37 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:08:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 15 Jan 2026 23:16:05 GMT
CMD ["gradle"]
# Thu, 15 Jan 2026 23:16:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Jan 2026 23:16:05 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Jan 2026 23:16:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Jan 2026 23:16:05 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Jan 2026 23:16:05 GMT
WORKDIR /home/gradle
# Thu, 15 Jan 2026 23:16:05 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 15 Jan 2026 23:16:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 15 Jan 2026 23:16:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Jan 2026 23:16:08 GMT
USER gradle
# Thu, 15 Jan 2026 23:16:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Jan 2026 23:16:08 GMT
USER root
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:36 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744d133b9cd24f4f90f79a72608e56f1397b2bbb440dbeba7d073b497a0c9ac3`  
		Last Modified: Thu, 15 Jan 2026 22:09:24 GMT  
		Size: 117.9 MB (117927015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950927e1b708bc092fb4893b30aaa78ee7625a3b4224e3018a998d00267c1189`  
		Last Modified: Thu, 15 Jan 2026 23:16:57 GMT  
		Size: 85.5 MB (85505208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a60b460e9329b670fed103c7c4e3ff4719f4d86e935d6d9e1fef15edc8938b2`  
		Last Modified: Thu, 15 Jan 2026 23:16:46 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efac9aa4116d332eb510888681a2208f57e34de2d8a7d2ff19609188457b5c6d`  
		Last Modified: Thu, 15 Jan 2026 23:16:40 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c67206c5baec0a3633035b565b429faa6853f327984366cb7788d6e7dc7256`  
		Last Modified: Thu, 15 Jan 2026 23:16:36 GMT  
		Size: 59.5 KB (59533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:e0334ed747120abfdfdb79d3383077d98527ccdef48cd7185213a3f887c1b10e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11739778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf11050bcd9c94981a8ed8801b1e9a37e9c989f2f0e14c154f6e9a24ccb4000`

```dockerfile
```

-	Layers:
	-	`sha256:821f78631ae89f403e933cf00f1d9ca3e448bc9b8b3af8dd38646fe161a40849`  
		Last Modified: Thu, 15 Jan 2026 23:16:37 GMT  
		Size: 11.7 MB (11718065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ea9a86dede893679ee2ded0c7a580dc7837def92043fd407a9f7a33632892d`  
		Last Modified: Fri, 16 Jan 2026 00:30:45 GMT  
		Size: 21.7 KB (21713 bytes)  
		MIME: application/vnd.in-toto+json
