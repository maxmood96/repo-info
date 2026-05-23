## `gradle:jdk11-corretto`

```console
$ docker pull gradle@sha256:739960c7c3970d40128e5b058ae8a6469a5d5004cb285a3d747f3287d6c27bb3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:ebcbf62c0c2b9383444268b74246b679861f2c024034fd727966ebb9f50ebddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.4 MB (432365364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3803d06b3563883d6f284fe5664e4bd8dd5ecefe036e7aeedc663db893fa5a1c`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 May 2026 20:12:06 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:06 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:11 GMT
ARG version=11.0.31.11-1
# Fri, 22 May 2026 21:11:11 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:11:11 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 22 May 2026 22:06:33 GMT
CMD ["gradle"]
# Fri, 22 May 2026 22:06:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 May 2026 22:06:33 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 22 May 2026 22:06:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 22 May 2026 22:06:33 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 May 2026 22:06:33 GMT
WORKDIR /home/gradle
# Fri, 22 May 2026 22:06:33 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 22 May 2026 22:06:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 22 May 2026 22:06:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 22 May 2026 22:06:36 GMT
USER gradle
# Fri, 22 May 2026 22:06:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 22 May 2026 22:06:36 GMT
USER root
```

-	Layers:
	-	`sha256:c00ef2b893da480d77c559b6862d1ad542cc91c6bb2d3106a00cb8d9c141b797`  
		Last Modified: Fri, 15 May 2026 20:34:40 GMT  
		Size: 54.6 MB (54572440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576a116e357ee250e46eda5c05ba229716ef3641e5c2ce1d8cdc025752b9955f`  
		Last Modified: Fri, 22 May 2026 21:11:33 GMT  
		Size: 153.5 MB (153474290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dede95c5d0a50ff18e9b6e11cff7cc6115717eda4d9e90ead1177b06e59a331`  
		Last Modified: Fri, 22 May 2026 22:07:06 GMT  
		Size: 86.2 MB (86193511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7552705fd1653299d381f96911f86bfc83d27d3537688ac35106f0767bf9364a`  
		Last Modified: Fri, 22 May 2026 22:07:03 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146b0abf427f70168bdfaf5f2265cbbf4b4810e74a3721c43502de43a3fb6684`  
		Last Modified: Fri, 22 May 2026 22:07:08 GMT  
		Size: 138.1 MB (138068533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ad28c6825ad03291ac713d7822d9cc8ecf454f8d496fe26e93c91a2939af89`  
		Last Modified: Fri, 22 May 2026 22:07:03 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:3aa6c5dc719375c4d13782db818dddad29e385a9fc37e5444f07aeae52fe618c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11397328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdd7625090c2f6fe7a12148774699164c6210e83deb61cf9b352e2263481293`

```dockerfile
```

-	Layers:
	-	`sha256:64e0ada07e5bfbdf8ace222e3500dd5888ee045926cd9496b2b0e9ff56e17325`  
		Last Modified: Fri, 22 May 2026 22:07:04 GMT  
		Size: 11.4 MB (11375663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a198875f2b2f0a3e09e7f0feffbbec08883971e9d120172b83500e7c2a72cca`  
		Last Modified: Fri, 22 May 2026 22:07:03 GMT  
		Size: 21.7 KB (21665 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:dc9fbec8e823bee5141d8c312942ac2de6b8d8d052b463a5ee1b5b20cfd68dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.3 MB (429330069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc031b60bb03cc81ab7e15a9f86eec48cdedd4a779e24bddaf2e44b7aac3118e`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 May 2026 20:12:25 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:25 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:10:48 GMT
ARG version=11.0.31.11-1
# Fri, 22 May 2026 21:10:48 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:10:48 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:10:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 22 May 2026 22:07:03 GMT
CMD ["gradle"]
# Fri, 22 May 2026 22:07:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 May 2026 22:07:03 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 22 May 2026 22:07:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 22 May 2026 22:07:03 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 May 2026 22:07:03 GMT
WORKDIR /home/gradle
# Fri, 22 May 2026 22:07:03 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 22 May 2026 22:07:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 22 May 2026 22:07:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 22 May 2026 22:07:06 GMT
USER gradle
# Fri, 22 May 2026 22:07:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 22 May 2026 22:07:06 GMT
USER root
```

-	Layers:
	-	`sha256:a92e5e4b9e90f970dfdf3c3258e673bb767c6401beba9985a3b635162466eedd`  
		Last Modified: Fri, 15 May 2026 20:34:37 GMT  
		Size: 53.5 MB (53454415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e0330030cf9dbc79176f06edbd88d18ca7a4124ad9736bc15fad2c2d57305c`  
		Last Modified: Fri, 22 May 2026 21:11:10 GMT  
		Size: 152.0 MB (152049570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ccac29e521d313841c858cee2f6526dccb86d273e1d9731a38f84b233413e1`  
		Last Modified: Fri, 22 May 2026 22:07:37 GMT  
		Size: 85.7 MB (85696344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57de5e67dfda715d30c6898195e6f6338049b24ba38ac984d3af1ad49912b122`  
		Last Modified: Fri, 22 May 2026 22:07:34 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d1aa48fa38b2702dee7794158d57a16e5c0f7c16935d972a73aa3eba30b4b7`  
		Last Modified: Fri, 22 May 2026 22:07:38 GMT  
		Size: 138.1 MB (138068534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b55e570f087e1baa6489a22fcc8e11e196afc8c4f7ac1814acbabdcb3dc56de`  
		Last Modified: Fri, 22 May 2026 22:07:34 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:dfe4a38b33e14aa550a2f9feb5ad1a047a8d43cbf819783f9ec20d5225eeedf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11397368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c93dded104e15549e6fc0b3eb103000f359d332df4ccf1199c4ab825b574f5`

```dockerfile
```

-	Layers:
	-	`sha256:8a7008b8589fdf93511e87a8252aeaf6b5fc4d37a23a71cb771b2b15b393eb65`  
		Last Modified: Fri, 22 May 2026 22:07:34 GMT  
		Size: 11.4 MB (11375506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f5e9f17ca291dfef64163905016734c4908a069f993a1ef40a798d606fa75c`  
		Last Modified: Fri, 22 May 2026 22:07:34 GMT  
		Size: 21.9 KB (21862 bytes)  
		MIME: application/vnd.in-toto+json
