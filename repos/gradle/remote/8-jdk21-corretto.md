## `gradle:8-jdk21-corretto`

```console
$ docker pull gradle@sha256:971dabf45bb13de410bca963321742c9b1d33068bcf4d8f216027566ce08253b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:1b7a02c4d91602774f3a155306531c1e9d81716196a857bd604061fd07ae8381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.4 MB (433375169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced86ccb34c3ef1d61139fe26556b3491007ada6987203182262b3c5cd99fb0f`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 01 Apr 2025 20:49:23 GMT
COPY /rootfs/ / # buildkit
# Tue, 01 Apr 2025 20:49:23 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:24:24 GMT
ARG version=21.0.7.6-1
# Tue, 15 Apr 2025 14:24:24 GMT
ARG package_version=1
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["gradle"]
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 15 Apr 2025 14:24:24 GMT
WORKDIR /home/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_VERSION=8.13
# Tue, 15 Apr 2025 14:24:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
USER gradle
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
USER root
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec1e3a2d6aab5829276e8f0cf7cd601be82c37d69ed45fb5d0b2277f45320b8`  
		Last Modified: Tue, 15 Apr 2025 23:56:03 GMT  
		Size: 169.9 MB (169917730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040a74ca18032beaeddc3ed6104af423ffd257aa6ace27bb1dcad0de8220a81c`  
		Last Modified: Wed, 16 Apr 2025 00:08:32 GMT  
		Size: 70.5 MB (70505619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c36be730937636fe39ee84774ad79d46a76ce4fd9a40747ad92dea4cb4a547`  
		Last Modified: Wed, 16 Apr 2025 00:08:30 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac9218a394960633ce0ce6296b0af737a04a3e4f8733fcc1823385943b27dea`  
		Last Modified: Wed, 16 Apr 2025 00:08:33 GMT  
		Size: 137.0 MB (136988178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16566aaee1d1c72bd1b1671b4020f0af221bf2b7d2c68343b94eda43bf2482a3`  
		Last Modified: Wed, 16 Apr 2025 00:08:30 GMT  
		Size: 54.9 KB (54910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:d1cb581f88d14fe8eb71e6800e877d4283a7f2fd749e7b24878644e41dfae2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10770352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10cbdb380cac58504e1daed5ef5a1f9cb61b7330f064e02c351cd7d1a9db6c13`

```dockerfile
```

-	Layers:
	-	`sha256:faf991cd8102405cdfec530c4aa383089deb8d77b24f926a741b112c6afe4e0b`  
		Last Modified: Wed, 16 Apr 2025 00:08:31 GMT  
		Size: 10.7 MB (10749833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e1866f71b4077b71970787c596dd2ce135d323ef4d02612a5d5283de2c2eb98`  
		Last Modified: Wed, 16 Apr 2025 00:08:30 GMT  
		Size: 20.5 KB (20519 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:bfd3030c5d2ead3b2a32dd0ad9432811d5b958432ae055a63cc44af7cd253118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.2 MB (430150410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22faf9ad20703d96fa084249d2ce01bbff2f52c46ea58284b63331467341ba6`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=21.0.6.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 27 Mar 2025 21:20:39 GMT
CMD ["gradle"]
# Thu, 27 Mar 2025 21:20:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 27 Mar 2025 21:20:39 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 27 Mar 2025 21:20:39 GMT
WORKDIR /home/gradle
# Thu, 27 Mar 2025 21:20:39 GMT
ENV GRADLE_VERSION=8.13
# Thu, 27 Mar 2025 21:20:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Thu, 27 Mar 2025 21:20:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
USER gradle
# Thu, 27 Mar 2025 21:20:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
USER root
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffca6b39b82b7986bb48be82129ceb9f9a0067ab8aa14e908ea6a8bee317c1d`  
		Last Modified: Wed, 02 Apr 2025 00:33:14 GMT  
		Size: 168.2 MB (168169083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f5f68189a3c544d7b6ad9221cc9d041830e9b30458842333bfe5295c33b56`  
		Last Modified: Wed, 02 Apr 2025 01:08:10 GMT  
		Size: 70.0 MB (69970932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ff0790c312af0157cd29bb176f9938cb1b31e76800a5da8c62779169475218`  
		Last Modified: Wed, 02 Apr 2025 01:08:07 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62ba379b639f1ceed3cf5437b528a5c639c9d2a06d2f23d119111fc63972b89`  
		Last Modified: Wed, 02 Apr 2025 01:08:11 GMT  
		Size: 137.0 MB (136988177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2eea9eada07d7ddbddc775febf23774a5ec1dc37d258d8b7f5da14be6221295`  
		Last Modified: Wed, 02 Apr 2025 01:08:08 GMT  
		Size: 59.5 KB (59531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:f43944ef1aeeb04a62ab8d95f934147fdbe0e83af156c27a4f7757a0745cec90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10769599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71379e966f41facd1dc78f597f686d290bee282c056bc721557ef181341c772c`

```dockerfile
```

-	Layers:
	-	`sha256:c6614a3d5041932ee8191c3d10b2ccb441d052d3fb370d2dfefb66c616a3e416`  
		Last Modified: Wed, 02 Apr 2025 01:08:08 GMT  
		Size: 10.7 MB (10748859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b69620e89f59ee673d540a0622ae8715f256f543d21c5652c700cd969ca2ec`  
		Last Modified: Wed, 02 Apr 2025 01:08:07 GMT  
		Size: 20.7 KB (20740 bytes)  
		MIME: application/vnd.in-toto+json
