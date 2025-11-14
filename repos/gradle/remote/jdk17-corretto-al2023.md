## `gradle:jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:6b28f27178b026af4aa554ffc9a8cf34b29bce62da5f7d41d5d3f04866cfe591
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:4467a07c980d3c9383e0a05601f9e7555cbdab78eae130f262c3b3661d1f75f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.5 MB (432484905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10aede75cfb14c8eadc710fba96437d27f6fa108b60fe8394847284d7c6a2442`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:30 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:30 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:16:12 GMT
ARG version=17.0.17.10-1
# Fri, 14 Nov 2025 02:16:12 GMT
ARG package_version=1
# Fri, 14 Nov 2025 02:16:12 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:16:12 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:16:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 14 Nov 2025 03:13:21 GMT
CMD ["gradle"]
# Fri, 14 Nov 2025 03:13:21 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 14 Nov 2025 03:13:21 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 14 Nov 2025 03:13:21 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 14 Nov 2025 03:13:21 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 14 Nov 2025 03:13:21 GMT
WORKDIR /home/gradle
# Fri, 14 Nov 2025 03:13:21 GMT
ENV GRADLE_VERSION=9.2.0
# Fri, 14 Nov 2025 03:13:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Fri, 14 Nov 2025 03:13:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 14 Nov 2025 03:13:24 GMT
USER gradle
# Fri, 14 Nov 2025 03:13:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 14 Nov 2025 03:13:25 GMT
USER root
```

-	Layers:
	-	`sha256:b64ab808fd6d460065684b4dcddcfaed550a0161a81a4f24db38100a7cef4ade`  
		Last Modified: Tue, 11 Nov 2025 02:45:03 GMT  
		Size: 54.0 MB (53976715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a75351a7b85edc90f47359058b146538723c16f6b9c27c24811f2017369409`  
		Last Modified: Fri, 14 Nov 2025 03:12:58 GMT  
		Size: 156.9 MB (156906057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41101678753fbf553a11e07910e3d716dfdae485aac2aeec8a4de3e2fda446b`  
		Last Modified: Fri, 14 Nov 2025 03:14:14 GMT  
		Size: 86.0 MB (86023898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1dda553351bc7c28bbb852ede2b7e402096f23ee7fd6e683f052758ecae7fb`  
		Last Modified: Fri, 14 Nov 2025 03:14:04 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20866c5870d3e55283fd9188484a4d7e4bf9ec3b606758b0b326f8a96d4d957b`  
		Last Modified: Fri, 14 Nov 2025 06:53:41 GMT  
		Size: 135.5 MB (135521657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448e127fe80824c7d25ab13e3c9379f36f41b88b4c7fa3632c0ff4b3802f8da0`  
		Last Modified: Fri, 14 Nov 2025 03:14:04 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:dd4e87090cd8aa3c506282d0b40ae22bef517569bb6905511eaf4f17e1f770e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11356178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00e93165f5fa590e026e85c425d295a0077931835ea90bff423c9a2c44142db`

```dockerfile
```

-	Layers:
	-	`sha256:085c40c23616f0745e7868cadc4a9008eef22e1992ee9c213383e3d77fbf1c08`  
		Last Modified: Fri, 14 Nov 2025 06:23:12 GMT  
		Size: 11.3 MB (11334730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2455673bfe93ecbb2b1a2b7d51a167fef1c6fd4952597ed433f589dcec89e693`  
		Last Modified: Fri, 14 Nov 2025 06:23:13 GMT  
		Size: 21.4 KB (21448 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ec810cf2160a9b6b43427786ce0dd621097aecfce44dff3a882ddc67719eef38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.7 MB (429709852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81106115d4f4df465b044d01196b79044c4d2dfd79b2df1edd846717fbdf63b`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:24 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:17:48 GMT
ARG version=17.0.17.10-1
# Fri, 14 Nov 2025 02:17:48 GMT
ARG package_version=1
# Fri, 14 Nov 2025 02:17:48 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:17:48 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:17:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 14 Nov 2025 03:14:05 GMT
CMD ["gradle"]
# Fri, 14 Nov 2025 03:14:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 14 Nov 2025 03:14:05 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 14 Nov 2025 03:14:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 14 Nov 2025 03:14:05 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 14 Nov 2025 03:14:05 GMT
WORKDIR /home/gradle
# Fri, 14 Nov 2025 03:14:05 GMT
ENV GRADLE_VERSION=9.2.0
# Fri, 14 Nov 2025 03:14:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Fri, 14 Nov 2025 03:14:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 14 Nov 2025 03:14:08 GMT
USER gradle
# Fri, 14 Nov 2025 03:14:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 14 Nov 2025 03:14:08 GMT
USER root
```

-	Layers:
	-	`sha256:7bff4bcb213fec2224ece2638c720fadc39b0d185d5cfe08391265c58685a0ae`  
		Last Modified: Tue, 11 Nov 2025 02:45:05 GMT  
		Size: 52.9 MB (52876656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c714347cee11166831f6d46e7650af7bf3a94113523fcd0a24080f090b89a4`  
		Last Modified: Fri, 14 Nov 2025 03:13:38 GMT  
		Size: 155.7 MB (155716125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e615c615812b6a7c6af80f03d3dbdf959d865450ff1082ad2b691abf7210b92`  
		Last Modified: Fri, 14 Nov 2025 03:14:58 GMT  
		Size: 85.5 MB (85534214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eec72c988d696a82dbf302fa295329ba8ab2c27e7564bf84fc12e2e7e28bf45`  
		Last Modified: Fri, 14 Nov 2025 03:14:51 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ce5ab23830dbbd6d9909ab14c555578128c395d6cd85ffa000f1c7c6893968`  
		Last Modified: Fri, 14 Nov 2025 03:14:42 GMT  
		Size: 135.5 MB (135521658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076c38406bb676c5ceab3de219d2b0221cdc2df4ce9d7f648b6a068f22caf8de`  
		Last Modified: Fri, 14 Nov 2025 03:14:51 GMT  
		Size: 59.5 KB (59522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:44ccb9289d7421fb50da613432a22ae590b42d1dde14604a2015d88f9037d2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11355374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7f9a36089300af46a34af10ce5abc01811b5c46fa09b4675c99790d383c368`

```dockerfile
```

-	Layers:
	-	`sha256:348ae549002a5369be345261d73195b4aac0d373350b1a36f4cbc2d7fb8082c7`  
		Last Modified: Fri, 14 Nov 2025 06:23:22 GMT  
		Size: 11.3 MB (11333729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9084426ecc1deb6a507e184e9fcda0ea8a86838d00e9ce94ed208bfccb28627e`  
		Last Modified: Fri, 14 Nov 2025 06:23:23 GMT  
		Size: 21.6 KB (21645 bytes)  
		MIME: application/vnd.in-toto+json
