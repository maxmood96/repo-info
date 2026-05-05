## `gradle:7-jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:f67ec82f28135ccf8eaebaecf9778dbfb7ba4c04a89509dd85e4ee96efca2218
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:075aa31a771a9d6e27d2c3a54a30a97d1325ac148dedb68eb091480834cf0010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.7 MB (422744192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb8afd6104ffc7693ae7501e38b4916cab578870f8004602b8a0cf7efacfc26`
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
# Mon, 04 May 2026 20:42:47 GMT
CMD ["gradle"]
# Mon, 04 May 2026 20:42:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 04 May 2026 20:42:47 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 04 May 2026 20:42:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 04 May 2026 20:42:47 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 04 May 2026 20:42:47 GMT
WORKDIR /home/gradle
# Mon, 04 May 2026 20:42:47 GMT
ENV GRADLE_VERSION=7.6.6
# Mon, 04 May 2026 20:42:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Mon, 04 May 2026 20:42:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 04 May 2026 20:42:50 GMT
USER gradle
# Mon, 04 May 2026 20:42:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 04 May 2026 20:42:50 GMT
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
	-	`sha256:f397845d703466b7ddb6943e6c623ecaf1536324f2621e363a636288451dcdbb`  
		Last Modified: Mon, 04 May 2026 20:43:20 GMT  
		Size: 86.2 MB (86168926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dda4850f50d699621c9b6ed4623c66807c44abf9497dec83c8c24c328293c12`  
		Last Modified: Mon, 04 May 2026 20:43:16 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7629c8c78ea05b947f95b817331a30a374cdd745cc0ce66adb62a6da7370f52f`  
		Last Modified: Mon, 04 May 2026 20:43:21 GMT  
		Size: 128.5 MB (128469414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041a3bdaca42e62156e81e0dcbc4a927d5ab87f4245381e9d9e0b44fc1fa9836`  
		Last Modified: Mon, 04 May 2026 20:43:16 GMT  
		Size: 54.9 KB (54907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:b7532614245cdabcb040e315246235bd38e58bf6e3d6e241d3d7ed393b3f0c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11306545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a59457b5668cdacafc80702788d6d8b6bd00ccf13c1d4c2107b4ec4d1194bad`

```dockerfile
```

-	Layers:
	-	`sha256:61428bec008bef08f72cf1dddee233cde478472ca63f08a872ec45d0710074a3`  
		Last Modified: Mon, 04 May 2026 20:43:17 GMT  
		Size: 11.3 MB (11285674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:488c48d3cd8a5e5edc5e080e4a95b589c49e96429f5c831c94208bb07f61f931`  
		Last Modified: Mon, 04 May 2026 20:43:16 GMT  
		Size: 20.9 KB (20871 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1759777121bd20107d99e77dc42fb6b3a5eb6f160daad84434e383744b7af485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.7 MB (419695905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb9dfbc23bbb1c15e53fa938053056a616a8c44f107f65349671590d0ba72cf`
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
# Mon, 04 May 2026 20:42:33 GMT
CMD ["gradle"]
# Mon, 04 May 2026 20:42:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 04 May 2026 20:42:33 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 04 May 2026 20:42:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 04 May 2026 20:42:34 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 04 May 2026 20:42:34 GMT
WORKDIR /home/gradle
# Mon, 04 May 2026 20:42:34 GMT
ENV GRADLE_VERSION=7.6.6
# Mon, 04 May 2026 20:42:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Mon, 04 May 2026 20:42:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 04 May 2026 20:42:36 GMT
USER gradle
# Mon, 04 May 2026 20:42:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 04 May 2026 20:42:37 GMT
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
	-	`sha256:da3dfe62d81f0025f4c693ec873af1df48826d4f7ae59c650365652cc945730a`  
		Last Modified: Mon, 04 May 2026 20:43:07 GMT  
		Size: 85.7 MB (85656893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1d0d49165d7a48cb3515d860dc699946538aad792e1237ade0bff59859e7ee`  
		Last Modified: Mon, 04 May 2026 20:43:03 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da6179d7a8b2cd6ee77ab2a7b36b1fa9aa1b80e66412e7906edabdb1f97d663`  
		Last Modified: Mon, 04 May 2026 20:43:08 GMT  
		Size: 128.5 MB (128469441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbafdf23561d4797347b4bd8c7e1dcfc54817951fdd50ea3761902e3fcd489a`  
		Last Modified: Mon, 04 May 2026 20:43:03 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:5e5767ab276fbc3126af07e01a52d90176fb10387377585e0481d0d769e59150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11306541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a917b6c1a20739e7f5404dfd405bd9aed1a5f24ff5b0b2bc1fe532eab3b2efaa`

```dockerfile
```

-	Layers:
	-	`sha256:cc99d65eb6e3c5e6e74738b33673d8c11b780bc0c7edcdabbb555b916b12bdfa`  
		Last Modified: Mon, 04 May 2026 20:43:04 GMT  
		Size: 11.3 MB (11285497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dd15c4a4c5e3aa28b4f271d0186209bed7a3beac97ff9dad4ea63af21c724bb`  
		Last Modified: Mon, 04 May 2026 20:43:03 GMT  
		Size: 21.0 KB (21044 bytes)  
		MIME: application/vnd.in-toto+json
