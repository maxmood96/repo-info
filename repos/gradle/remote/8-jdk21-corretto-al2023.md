## `gradle:8-jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:d70fa8b38c96928c755567042ef8f5115a7bb8d8c4869fd8b9269f6bdd70521a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:a9db1b1ba1221691afe468f756d0c34ed629c0471450852bd3246e7341dbf2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.8 MB (449786679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9dc38c3d1a330f24b67fdfe623cb3f779b7c6358d59f0d6694a6f79dc5e18cf`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:12 GMT
ARG version=21.0.11.10-1
# Mon, 22 Jun 2026 18:05:12 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:05:12 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:12 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 22 Jun 2026 18:15:17 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:15:17 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:15:17 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:15:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 18:15:17 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:15:17 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:15:17 GMT
ENV GRADLE_VERSION=8.14.5
# Mon, 22 Jun 2026 18:15:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Mon, 22 Jun 2026 18:15:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:15:20 GMT
USER gradle
# Mon, 22 Jun 2026 18:15:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 22 Jun 2026 18:15:20 GMT
USER root
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbda8bbed2402313490b832b371f9a31cefa72cc0c1f79f7de0207d319faaf9`  
		Last Modified: Mon, 22 Jun 2026 18:05:38 GMT  
		Size: 170.4 MB (170446421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a6e305388b3a59023cc4de1a293e7d72e6d980e5c62fcbd8b06d2c4a2aeb45`  
		Last Modified: Mon, 22 Jun 2026 18:15:50 GMT  
		Size: 86.6 MB (86640960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3887f3080809c3107b5952715a12815a23495621dd06c7a65aac5065ba9d6ae5`  
		Last Modified: Mon, 22 Jun 2026 18:15:46 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a392fc04680433b2b5c6cf8b793ba93d33a3cb84e84b062512cd612195f2f573`  
		Last Modified: Mon, 22 Jun 2026 18:15:51 GMT  
		Size: 138.1 MB (138068530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5093b68ed1b0c023e4a037ba5ca7a5a46720a36851b1a244611b2c4a6e63ec14`  
		Last Modified: Mon, 22 Jun 2026 18:15:46 GMT  
		Size: 54.9 KB (54907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:59638be637f1119b690de792970a1f513c8aae715b7a7bf985a6aaf30ff8ec82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11378924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd57de7ea859b6f950c279d3a697cb20a16ca0a47e0b64c4fe56b54e2e176861`

```dockerfile
```

-	Layers:
	-	`sha256:1dc2881fadd4eb40a5db090dbe0afb090f697b34e018fd874430c0c4abb58951`  
		Last Modified: Mon, 22 Jun 2026 18:15:47 GMT  
		Size: 11.4 MB (11357901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f50c0ba8c8a358a27daceaa79141e9a674c6b9ad7bcd59910f99e95f1847136d`  
		Last Modified: Mon, 22 Jun 2026 18:15:46 GMT  
		Size: 21.0 KB (21023 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:0bdf9b71c08a654c1439bd72c2e708b81db8e4da0fb35eba3fbddbe3d7c73034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.3 MB (446340917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71756080bb62c503325637b3cab4c5a4b336232565f581dc7291d75902ccd8f2`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:15:10 GMT
ARG version=21.0.11.10-1
# Mon, 22 Jun 2026 18:15:10 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:15:10 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:15:10 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:15:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 22 Jun 2026 18:27:10 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:27:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:27:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:27:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 18:27:10 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:27:10 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:27:10 GMT
ENV GRADLE_VERSION=8.14.5
# Mon, 22 Jun 2026 18:27:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Mon, 22 Jun 2026 18:27:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:27:13 GMT
USER gradle
# Mon, 22 Jun 2026 18:27:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 22 Jun 2026 18:27:13 GMT
USER root
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10beb5c68f4d3c7d1c45314bbff9c0bb6baf58079563b749b2f64ac9f3c511d3`  
		Last Modified: Mon, 22 Jun 2026 18:15:34 GMT  
		Size: 168.7 MB (168721711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b92983fb034b42f5f8467dec7e0a12f225e0176edca2404975806e9b1e2df2e`  
		Last Modified: Mon, 22 Jun 2026 18:27:45 GMT  
		Size: 86.0 MB (86038737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e725cae3a6396cda98c79cbd6d71cbb4c360bc520b086a19c64edd2ad545ab`  
		Last Modified: Mon, 22 Jun 2026 18:27:41 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649cb1283806b8bc39fbaf14f9916101a25b48f1d7e64b98480cab3fd37c1968`  
		Last Modified: Mon, 22 Jun 2026 18:27:46 GMT  
		Size: 138.1 MB (138068573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90aa3ff4833bdb903cd215cecb71e8176b07b69f8b97b5039847a08c4448a0e`  
		Last Modified: Mon, 22 Jun 2026 18:27:41 GMT  
		Size: 59.5 KB (59532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:43b30dbc298530f3bd4a0d2ea3b0e651d47b225691ab50f925c1f0adcd62d9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11378076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034f25d6cf136e2f0c335714e1447d8a8f98feeb1843419ecdc79ca8d14959dc`

```dockerfile
```

-	Layers:
	-	`sha256:79b0be038db2cbcdb84e4d9b5a69ebcce2373c6ac8ee9245388aa0e4090c96ac`  
		Last Modified: Mon, 22 Jun 2026 18:27:42 GMT  
		Size: 11.4 MB (11356880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:045de552d0f0f15e55c12bcc217fd9690e61ebbd99a8cba538dec64e97854198`  
		Last Modified: Mon, 22 Jun 2026 18:27:41 GMT  
		Size: 21.2 KB (21196 bytes)  
		MIME: application/vnd.in-toto+json
