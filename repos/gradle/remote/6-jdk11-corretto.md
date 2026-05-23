## `gradle:6-jdk11-corretto`

```console
$ docker pull gradle@sha256:ff6e6cf3752aff3f15b1c8ac05570dfe2bd422453c29429302d3812a16e4517d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:4d59d828b7214fdf3b99520e7353d30cf56418aec50383e9e514cf443644843e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.4 MB (402369906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869845fc2762c6f6abbb0d5cb816758b8befb0e2f7465a096cb10b62db02abd9`
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
# Fri, 22 May 2026 22:07:19 GMT
CMD ["gradle"]
# Fri, 22 May 2026 22:07:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 May 2026 22:07:19 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 22 May 2026 22:07:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 22 May 2026 22:07:19 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 May 2026 22:07:19 GMT
WORKDIR /home/gradle
# Fri, 22 May 2026 22:07:19 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 22 May 2026 22:07:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 22 May 2026 22:07:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 22 May 2026 22:07:21 GMT
USER gradle
# Fri, 22 May 2026 22:07:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 22 May 2026 22:07:22 GMT
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
	-	`sha256:0bdeb2d37bba2911ad8e48c708142ce244ee05415af5ede84bceca2c9596a98c`  
		Last Modified: Fri, 22 May 2026 22:07:48 GMT  
		Size: 86.2 MB (86193551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bce02db10fd660b4ceae1855ad2ff490aa6d52c60a34c7ce29aaca7ece547e`  
		Last Modified: Fri, 22 May 2026 22:07:45 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f95a991f986d0a9c01b9f71473153357e39306df24dfecd552f86242339ae2a`  
		Last Modified: Fri, 22 May 2026 22:07:49 GMT  
		Size: 107.7 MB (107696664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fecfe97eca682140f9938ca3d1ee37c728e9497db129ccff076e8682dff437`  
		Last Modified: Fri, 22 May 2026 22:07:45 GMT  
		Size: 431.3 KB (431283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:c479575c9795e195290cf17a9c2428476efa8de79fdde9387a35b06f020b1fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11288650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e92fa1dd7c3bef4562ffe6f53c92253f65407c031436257e22f291de10edbb`

```dockerfile
```

-	Layers:
	-	`sha256:e65b6b40856873791c18dd017f9d869247f0e88afbc661b918294a1a83ce1f17`  
		Last Modified: Fri, 22 May 2026 22:07:46 GMT  
		Size: 11.3 MB (11267778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f29aa1badcba361ae6cac99addc2c27415f4e1078616683015dc422f8f81e15b`  
		Last Modified: Fri, 22 May 2026 22:07:45 GMT  
		Size: 20.9 KB (20872 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ab1f429c36cdf513e0abdc90b6e317ff84a9f067a1ace7298e91d13a51f4ac7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.3 MB (399323286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae65fa6931fa39bf3996a53b34813fff8a3abb60a43b07441f3a99caa5db65b9`
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
# Fri, 22 May 2026 22:08:05 GMT
CMD ["gradle"]
# Fri, 22 May 2026 22:08:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 May 2026 22:08:05 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 22 May 2026 22:08:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 22 May 2026 22:08:05 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 May 2026 22:08:05 GMT
WORKDIR /home/gradle
# Fri, 22 May 2026 22:08:05 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 22 May 2026 22:08:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 22 May 2026 22:08:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 22 May 2026 22:08:08 GMT
USER gradle
# Fri, 22 May 2026 22:08:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 22 May 2026 22:08:08 GMT
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
	-	`sha256:b565ff39d82cee9df3af2f9cf54d8ee56ab95bc896085f06e87a600160624778`  
		Last Modified: Fri, 22 May 2026 22:08:39 GMT  
		Size: 85.7 MB (85695958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94391bfdf24da002f4c58c4202ac7ec10bb8ae7fb53bc70512c005fff254c2fb`  
		Last Modified: Fri, 22 May 2026 22:08:35 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ec5dcaf4372bb5df0980c68d594cd7990476b5d4d4794a6781bb210b74fd9d`  
		Last Modified: Fri, 22 May 2026 22:08:39 GMT  
		Size: 107.7 MB (107696634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61521679a633172d11d8c6ef99e05997439f51fcebd9be0de4df38f7452a385`  
		Last Modified: Fri, 22 May 2026 22:08:35 GMT  
		Size: 425.0 KB (425027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:ea71db74bcfb6cbf45a7e69e8d0c8fd5a8d0512cc8553ce218d21d05b17d54cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11288642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86c55a8a48d511fd353ebcdc1cdae9913542b30702997755e24cef8883dde83`

```dockerfile
```

-	Layers:
	-	`sha256:9caa426d76280cff19a514ebed7c13630a17edd50f676ac13454be7e1ca0799b`  
		Last Modified: Fri, 22 May 2026 22:08:36 GMT  
		Size: 11.3 MB (11267597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82261b7afed8ba3e8920c5d4f2490586d9b7e844985aeeb4857568853a602b78`  
		Last Modified: Fri, 22 May 2026 22:08:35 GMT  
		Size: 21.0 KB (21045 bytes)  
		MIME: application/vnd.in-toto+json
