## `gradle:7-jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:c007ecd7daa427b29398a85e27c027af302ff2588910165d4651ebb0633e15c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:1f9566c7a5346bb877edd0b9405f118318c4e4097085419be02cbab3deadbb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.9 MB (421902728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de73f1ddb74d28ab40ee9bdb316a0c72415d0ac8fce90025951a062f1690f3b`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:41 GMT
ARG version=11.0.29.7-1
# Thu, 15 Jan 2026 22:09:41 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:09:41 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:09:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 15 Jan 2026 23:08:44 GMT
CMD ["gradle"]
# Thu, 15 Jan 2026 23:08:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Jan 2026 23:08:44 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Jan 2026 23:08:45 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Jan 2026 23:08:45 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Jan 2026 23:08:45 GMT
WORKDIR /home/gradle
# Thu, 15 Jan 2026 23:08:45 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 15 Jan 2026 23:08:45 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 15 Jan 2026 23:08:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Jan 2026 23:08:47 GMT
USER gradle
# Thu, 15 Jan 2026 23:08:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Jan 2026 23:08:47 GMT
USER root
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:09:37 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d80e849e0986824104f94780e496e5f0b7ca3decbfc934b6f1ee3b8406bd6c8`  
		Last Modified: Thu, 15 Jan 2026 22:10:03 GMT  
		Size: 153.3 MB (153314830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ace9d5fcb3e30f1f8dbdc78612ce0877e9ab592edc06169a456528963c535be`  
		Last Modified: Thu, 15 Jan 2026 23:09:34 GMT  
		Size: 86.0 MB (86040710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252afa28cfe166fd19a63112ef8414816f9430252f26087242dfa7c4485b3fc7`  
		Last Modified: Thu, 15 Jan 2026 23:09:13 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77140682db0b7214b8015dbc56feb2263c25e2a4f6e9310783bf5c7576d3038`  
		Last Modified: Thu, 15 Jan 2026 23:09:17 GMT  
		Size: 128.5 MB (128469407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3b7283c981ccf7a9f846bb59d366dcf9263cc25ae73d2a7721d8137ee7fa6e`  
		Last Modified: Thu, 15 Jan 2026 23:09:13 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:5e74b473f4f4604f6c96cdb7f9ef0d1ae37e4c2afe75bb3dfdac2f2edcbbd156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11296850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220aafecf9de7bafde81b93bb4e16e68c23a1bd24fe1bfc3c263d4a744ed26e6`

```dockerfile
```

-	Layers:
	-	`sha256:477fa79f4bdb1922a21d84e5d354a5fae183691c7b7b35b1fe7b1757698feab1`  
		Last Modified: Fri, 16 Jan 2026 00:21:38 GMT  
		Size: 11.3 MB (11275979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7310ca1c085da106a13512d384c5a19bffa5b68b6c49a40377866963c0d88d53`  
		Last Modified: Fri, 16 Jan 2026 00:21:39 GMT  
		Size: 20.9 KB (20871 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c8604f2db47859e9429d2c055a416de656f95d20ef720b05b7f4627c6532572e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.8 MB (418825014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc9de80fa138ce9e0ebff0a5e516f02f6e692a92cd37772379ddbc0993069dc`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:34 GMT
ARG version=11.0.29.7-1
# Thu, 15 Jan 2026 22:08:34 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:08:34 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:08:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 15 Jan 2026 23:16:18 GMT
CMD ["gradle"]
# Thu, 15 Jan 2026 23:16:18 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Jan 2026 23:16:18 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Jan 2026 23:16:18 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Jan 2026 23:16:18 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Jan 2026 23:16:18 GMT
WORKDIR /home/gradle
# Thu, 15 Jan 2026 23:16:18 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 15 Jan 2026 23:16:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 15 Jan 2026 23:16:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Jan 2026 23:16:20 GMT
USER gradle
# Thu, 15 Jan 2026 23:16:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Jan 2026 23:16:21 GMT
USER root
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:25 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb516caff5975026fd4cb1685b25ef916ac594c49bf6ec816847c2506e060df`  
		Last Modified: Thu, 15 Jan 2026 22:08:56 GMT  
		Size: 151.9 MB (151859277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8d316ea17c5ce9127206e73ff62c75394fe1933526588447f7efe1a420a81e`  
		Last Modified: Thu, 15 Jan 2026 23:16:52 GMT  
		Size: 85.5 MB (85520756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe71796a1c92c598924df2dbfc8f84ed80e2047c3cc7ea75a5854b9b0fde290e`  
		Last Modified: Thu, 15 Jan 2026 23:16:58 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791244627990edd940b1be9cf3b70ec624f95913e056bb5aa6de2d9958c07ad1`  
		Last Modified: Thu, 15 Jan 2026 23:17:28 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da1b9d02cd182dbd37aa7674d5c9c5da111078938978aaae03e73a80464ece3`  
		Last Modified: Thu, 15 Jan 2026 23:16:48 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:ddd4cfe48140607847b11e9792ebb5f70c67b4bd9f429c1b150868f62c6babab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11296838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4e309995a4221d71afd2b5e5dd9ce1a26220e32734d7c705943cc0d56a2e94`

```dockerfile
```

-	Layers:
	-	`sha256:015038db273a163b5deddb15a448e5491562dc8a8e9339a2dff4c8d92fc76285`  
		Last Modified: Thu, 15 Jan 2026 23:16:49 GMT  
		Size: 11.3 MB (11275794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:124bb10478d623dbb13b31e419b841e3f12508601efc72ee4e81ee88ba583d5b`  
		Last Modified: Fri, 16 Jan 2026 00:23:12 GMT  
		Size: 21.0 KB (21044 bytes)  
		MIME: application/vnd.in-toto+json
