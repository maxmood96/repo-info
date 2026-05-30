## `gradle:8-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:b5475afe9e329ef9388224f175ae314b821851cf63f8daeabc37f78e70c4b937
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:98e307cc0d483588a2b1cac23a5fb807da1277cd282afaf4c468adced67e53d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.1 MB (436116858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83557f1a21be11d59d9b9c79f94cefd0b1d5da00bf8024742114256ac4b8abc`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 30 May 2026 00:26:56 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:26:56 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:59 GMT
ARG version=17.0.19.10-1
# Sat, 30 May 2026 01:11:59 GMT
ARG package_version=1
# Sat, 30 May 2026 01:11:59 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:11:59 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 30 May 2026 02:12:05 GMT
CMD ["gradle"]
# Sat, 30 May 2026 02:12:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 30 May 2026 02:12:05 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 30 May 2026 02:12:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 30 May 2026 02:12:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 30 May 2026 02:12:05 GMT
WORKDIR /home/gradle
# Sat, 30 May 2026 02:12:05 GMT
ENV GRADLE_VERSION=8.14.5
# Sat, 30 May 2026 02:12:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Sat, 30 May 2026 02:12:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 30 May 2026 02:12:08 GMT
USER gradle
# Sat, 30 May 2026 02:12:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 30 May 2026 02:12:08 GMT
USER root
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f5461596ec82cf1472eb49d2c4ccb688b3d1a9f53b7f3ed65132c7161de215`  
		Last Modified: Sat, 30 May 2026 01:12:20 GMT  
		Size: 157.2 MB (157156699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d492768463b52021e9dd1d78c29b29decddf12a2729b371ac38ed1075a49ec78`  
		Last Modified: Sat, 30 May 2026 02:12:40 GMT  
		Size: 86.3 MB (86263897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de48b37ef444ab8315833214e4b7f96b4ddd683b96d206a6abf0e04924c432a`  
		Last Modified: Sat, 30 May 2026 02:12:36 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb99fc55846e192578e4682ecfd47d8d3518fe4ab534f1d0758f0f608d9e4fe`  
		Last Modified: Sat, 30 May 2026 02:12:42 GMT  
		Size: 138.1 MB (138068535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2296b36696dfb889f5027b153787750c2d70e7d8b3cb4acff45c3fa67dbd2e3`  
		Last Modified: Sat, 30 May 2026 02:12:36 GMT  
		Size: 54.9 KB (54891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:e3094d921c1062fcc4b2d7c0535b1ce0bfa843296767d54bb4b0332d21e1e77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11371197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab89e1592c5e81a713497dffd306cbd703c27ffb54f823b89f85073e0ac29cc`

```dockerfile
```

-	Layers:
	-	`sha256:e8523b1baa09f51bbc3d8a17e21ae2ae30c30f09fa52d7279cc4de56b669b31c`  
		Last Modified: Sat, 30 May 2026 02:12:37 GMT  
		Size: 11.4 MB (11350332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df5048d545acdc95b879b62a4ce1d1373bd5a9b9d873af5c6f601d0a2b486209`  
		Last Modified: Sat, 30 May 2026 02:12:36 GMT  
		Size: 20.9 KB (20865 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d7cdd9ec69950c53f1d8c155a21b8909959b7524ec7e4be0646e545d6f68aef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.3 MB (433296272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7852af58f188cddc8f98cc6d1a8946b10b8140382fe80da9c1dea68c1c9d77f`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:35 GMT
ARG version=17.0.19.10-1
# Sat, 30 May 2026 01:11:35 GMT
ARG package_version=1
# Sat, 30 May 2026 01:11:35 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:11:35 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 30 May 2026 02:11:55 GMT
CMD ["gradle"]
# Sat, 30 May 2026 02:11:55 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 30 May 2026 02:11:55 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 30 May 2026 02:11:55 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 30 May 2026 02:11:55 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 30 May 2026 02:11:55 GMT
WORKDIR /home/gradle
# Sat, 30 May 2026 02:11:55 GMT
ENV GRADLE_VERSION=8.14.5
# Sat, 30 May 2026 02:11:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Sat, 30 May 2026 02:11:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 30 May 2026 02:11:58 GMT
USER gradle
# Sat, 30 May 2026 02:11:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 30 May 2026 02:11:58 GMT
USER root
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9482a7eeb42d8af7aec6211eea7980986e31da05224bb8f4570edda7f0275cdf`  
		Last Modified: Sat, 30 May 2026 01:11:58 GMT  
		Size: 156.0 MB (155987199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a929281b011cdbc57f1534406c5ba4be38175b9f3db8f9f133cc0e1c99dbc1`  
		Last Modified: Sat, 30 May 2026 02:12:30 GMT  
		Size: 85.7 MB (85721511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fea715ab81b63f04e78d284fe77b4525a88d208b4a01bd650d0b8dfa6bea8f`  
		Last Modified: Sat, 30 May 2026 02:12:26 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3403c558a965b9ca94e027fd4bf3edc03fa59d96bd3461df0aa67a825664a4cd`  
		Last Modified: Sat, 30 May 2026 02:12:31 GMT  
		Size: 138.1 MB (138068543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c764a151261c083892a01249f05c25d3682f999661e163158250cd43238a6257`  
		Last Modified: Sat, 30 May 2026 02:12:26 GMT  
		Size: 59.5 KB (59515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:fa7b4977c64b781cf917d89645fb194e90df243a965c306af10515f4aa2ffbd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11370346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e20ef398c537660d3910df45c2b7505363ba5c34efbde462603e07ad2c40f9`

```dockerfile
```

-	Layers:
	-	`sha256:ec1c703b05faea3d9aeb3803eca6b48345d211106c90421bd1e587173c157379`  
		Last Modified: Sat, 30 May 2026 02:12:27 GMT  
		Size: 11.3 MB (11349308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15988ddb6e64dc7c958c17f46f99f7472b88748509b564872ebbcfafc6746764`  
		Last Modified: Sat, 30 May 2026 02:12:26 GMT  
		Size: 21.0 KB (21038 bytes)  
		MIME: application/vnd.in-toto+json
