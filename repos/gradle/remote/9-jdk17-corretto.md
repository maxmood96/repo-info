## `gradle:9-jdk17-corretto`

```console
$ docker pull gradle@sha256:5ffc78ae4acb20fa1671fed20d50cb52c183e0da1411f0adf5186b6fc08d647e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:427ef21e3c3d7057fdfca6d4e3e223c15264c02b9cf0cf9ce0cfcafccb7757c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.2 MB (438186467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2b7ae5217e94e347b1c64494ee959dab6fd13931c4e8261336ae6fb0b921fa`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 May 2026 20:12:06 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:06 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:37 GMT
ARG version=17.0.19.10-1
# Fri, 22 May 2026 21:11:37 GMT
ARG package_version=1
# Fri, 22 May 2026 21:11:37 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:11:37 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 22 May 2026 22:06:13 GMT
CMD ["gradle"]
# Fri, 22 May 2026 22:06:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 May 2026 22:06:13 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 22 May 2026 22:06:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 22 May 2026 22:06:13 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 May 2026 22:06:13 GMT
WORKDIR /home/gradle
# Fri, 22 May 2026 22:06:13 GMT
ENV GRADLE_VERSION=9.5.1
# Fri, 22 May 2026 22:06:13 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Fri, 22 May 2026 22:06:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 22 May 2026 22:06:15 GMT
USER gradle
# Fri, 22 May 2026 22:06:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 22 May 2026 22:06:16 GMT
USER root
```

-	Layers:
	-	`sha256:c00ef2b893da480d77c559b6862d1ad542cc91c6bb2d3106a00cb8d9c141b797`  
		Last Modified: Fri, 15 May 2026 20:34:40 GMT  
		Size: 54.6 MB (54572440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6459ce5e246b3d8bb1803ab05d270e314eb5e96858a505646b82833ddd5121`  
		Last Modified: Fri, 22 May 2026 21:11:57 GMT  
		Size: 157.2 MB (157158594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b0470d1f2fa2508455e4e44d75be595d18d6c868c3ffac7485252042f80f60`  
		Last Modified: Fri, 22 May 2026 22:06:46 GMT  
		Size: 86.2 MB (86191196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2f5e07b49132a760056287de838a58603d31ef96a97371c6cafe057ac16084`  
		Last Modified: Fri, 22 May 2026 22:06:43 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8890008f7d8f3848b1cc89eac119ba7fbc6c4052365915ca1db3107877582ab4`  
		Last Modified: Fri, 22 May 2026 22:06:47 GMT  
		Size: 140.2 MB (140236945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610c6201f1572606b60f002eabfb79e9cb549f2c1f0bba7f21f52911d17b33ec`  
		Last Modified: Fri, 22 May 2026 22:06:43 GMT  
		Size: 25.6 KB (25611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:c8e3e4445bb3f214785e247159a3ac1588be85709469c8cb9587319eb52fd488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904302b4fbbcf47c39811d7fbcbfcb62db61ba3a678abc0ba635956eb785ebb6`

```dockerfile
```

-	Layers:
	-	`sha256:8f0126340c218f38245e15ad6af24d67600b52c8058e3a43aa8055d606233284`  
		Last Modified: Fri, 22 May 2026 22:06:43 GMT  
		Size: 11.4 MB (11365660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddeeb37a7816786e1218ea9d203f62696d9cae8d75e02b0e42a19520e6dd463d`  
		Last Modified: Fri, 22 May 2026 22:06:43 GMT  
		Size: 21.5 KB (21497 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:21b91b9296b2e294f4079b6da1ddd7243975cbcbe9770dd35e373032f9f782f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.4 MB (435407035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc2026eba4dc2e6d231c6cbbfeafcdbb737cce94a8272f3eefeea1b63146a0d`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 May 2026 20:12:25 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:25 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:33 GMT
ARG version=17.0.19.10-1
# Fri, 22 May 2026 21:11:33 GMT
ARG package_version=1
# Fri, 22 May 2026 21:11:33 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:11:33 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 22 May 2026 22:06:52 GMT
CMD ["gradle"]
# Fri, 22 May 2026 22:06:52 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 May 2026 22:06:52 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 22 May 2026 22:06:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 22 May 2026 22:06:53 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 May 2026 22:06:53 GMT
WORKDIR /home/gradle
# Fri, 22 May 2026 22:06:53 GMT
ENV GRADLE_VERSION=9.5.1
# Fri, 22 May 2026 22:06:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Fri, 22 May 2026 22:06:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 22 May 2026 22:06:56 GMT
USER gradle
# Fri, 22 May 2026 22:06:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 22 May 2026 22:06:57 GMT
USER root
```

-	Layers:
	-	`sha256:a92e5e4b9e90f970dfdf3c3258e673bb767c6401beba9985a3b635162466eedd`  
		Last Modified: Fri, 15 May 2026 20:34:37 GMT  
		Size: 53.5 MB (53454415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76dff99f7dfb9e95ce331867dbe7cc08952add0452592bfbccd1c64d2711416`  
		Last Modified: Fri, 22 May 2026 21:11:55 GMT  
		Size: 156.0 MB (155987820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e631711260fcd3bdf686d1e8b6120482570f6547a642db4be16293184d7f833a`  
		Last Modified: Fri, 22 May 2026 22:07:28 GMT  
		Size: 85.7 MB (85696799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b230e636b83dda31e9f82a7281b8be56ce633672d985093c2aa90c152b2c24`  
		Last Modified: Fri, 22 May 2026 22:07:24 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503068ea5e699b65a834c57bf1d605d2d5fd573799e14319c5f04f82085ca8e9`  
		Last Modified: Fri, 22 May 2026 22:07:29 GMT  
		Size: 140.2 MB (140236982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0dc2b11a49b8b4c10f27ad1bb1b29f8bf3e125365348896252137de06f5e54`  
		Last Modified: Fri, 22 May 2026 22:07:25 GMT  
		Size: 29.3 KB (29344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:a90467efd25680aa18370b77e60919d3c86d467a2bf300e7bbe9bfd9ee148e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11386354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f7454c3fb762f93bf4627ef46cc39296a4c77db8eb5f6dc1f71fa1124fc7a3`

```dockerfile
```

-	Layers:
	-	`sha256:c4c474e9a825910b4fcb69bf7fd73b5252a4ac95cf3618a74cfb19008531c106`  
		Last Modified: Fri, 22 May 2026 22:07:25 GMT  
		Size: 11.4 MB (11364660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:051518963855f35a77c0f3eca91022ab1230c930834163702a3376da2ec5f0c5`  
		Last Modified: Fri, 22 May 2026 22:07:24 GMT  
		Size: 21.7 KB (21694 bytes)  
		MIME: application/vnd.in-toto+json
