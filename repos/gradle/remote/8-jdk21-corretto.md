## `gradle:8-jdk21-corretto`

```console
$ docker pull gradle@sha256:f4006fc879bda95513503c252fbbabef6015cb17f67c6107d0b2856ad055eeb8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:972211a3faffeabf7469b1491787b2fc20ede1d21101090d2ed026a762171cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.3 MB (449313287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc0ca0732620d056de59658a4f1c77d6c3a61a243006fbcdc2ae2df451711e2`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:18:52 GMT
ARG version=21.0.11.10-1
# Sat, 09 May 2026 00:18:52 GMT
ARG package_version=1
# Sat, 09 May 2026 00:18:52 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:18:52 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:18:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 09 May 2026 01:20:51 GMT
CMD ["gradle"]
# Sat, 09 May 2026 01:20:51 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 09 May 2026 01:20:51 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 09 May 2026 01:20:51 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 09 May 2026 01:20:51 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 09 May 2026 01:20:52 GMT
WORKDIR /home/gradle
# Sat, 09 May 2026 01:20:52 GMT
ENV GRADLE_VERSION=8.14.5
# Sat, 09 May 2026 01:20:52 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Sat, 09 May 2026 01:20:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 09 May 2026 01:20:54 GMT
USER gradle
# Sat, 09 May 2026 01:20:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 09 May 2026 01:20:55 GMT
USER root
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d605a7f04b26773a6a7aba7b0d6aa1461c92ae1a610eaf0612445f5621b9a7`  
		Last Modified: Sat, 09 May 2026 00:19:14 GMT  
		Size: 170.4 MB (170444573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e4d34f659f7e11846dab52dba2856100a7ca4ae4ccf6a2f8003765ca705665`  
		Last Modified: Sat, 09 May 2026 01:21:27 GMT  
		Size: 86.2 MB (86166784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b23ac5a1f7a9857701f7f919e690c1c384a70e2f606efcc6e9f8c8bfbf5451`  
		Last Modified: Sat, 09 May 2026 01:21:22 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf25b0b0daddded33ef8b1f0c823b8334d6e540f296dddf4f3390b1deb3c4593`  
		Last Modified: Sat, 09 May 2026 01:21:28 GMT  
		Size: 138.1 MB (138068533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e1f3c7a3581993a07608251af034194ab54618e7d1b0ba0b8562ac280d00af`  
		Last Modified: Sat, 09 May 2026 01:21:23 GMT  
		Size: 54.9 KB (54911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:deaf7feaaa4e1888cc636f72d1f60101e8baeb945c3c5e0e5281c95c8010e61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11373779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025bcb91e121dc51c518bdf53f0983a35292fec90ee8f2cc06e58baea178b869`

```dockerfile
```

-	Layers:
	-	`sha256:7a9ad13894830c5f734a3e5a8eecf4b568a407deb4ac7cbd1d6226bcd33d71f8`  
		Last Modified: Sat, 09 May 2026 01:21:23 GMT  
		Size: 11.4 MB (11352756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f37832af6e6a9466d980046ddd32fe4c39f9e7895cc90d2ac691d4f3ade5a50b`  
		Last Modified: Sat, 09 May 2026 01:21:22 GMT  
		Size: 21.0 KB (21023 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:534b4f738631961338dcecc5dec89878a40c9395539bad12e9ad0cd233047ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.0 MB (445966034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a2a764497dc9b5f0b1c8246948e4919ed01984bedb3d13ab07d46aab196d33`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:16:30 GMT
ARG version=21.0.11.10-1
# Sat, 09 May 2026 00:16:30 GMT
ARG package_version=1
# Sat, 09 May 2026 00:16:30 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:16:30 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:16:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 09 May 2026 01:46:22 GMT
CMD ["gradle"]
# Sat, 09 May 2026 01:46:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 09 May 2026 01:46:22 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 09 May 2026 01:46:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 09 May 2026 01:46:22 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 09 May 2026 01:46:22 GMT
WORKDIR /home/gradle
# Sat, 09 May 2026 01:46:22 GMT
ENV GRADLE_VERSION=8.14.5
# Sat, 09 May 2026 01:46:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Sat, 09 May 2026 01:46:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 09 May 2026 01:46:25 GMT
USER gradle
# Sat, 09 May 2026 01:46:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 09 May 2026 01:46:25 GMT
USER root
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2600f4d09077112d700e69b97b0ce85fa53a45cf0380a0447ccdcb015a271808`  
		Last Modified: Sat, 09 May 2026 00:16:53 GMT  
		Size: 168.7 MB (168722339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa524f0ad4ead7b9123818a3ddfa8fcf9042c7575f237c2fecbe0f6da424c3b`  
		Last Modified: Sat, 09 May 2026 01:46:57 GMT  
		Size: 85.7 MB (85656966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b0805dd4e399e5f4d59aa37d0cecba60145926faf617462e496d0f27816bc0`  
		Last Modified: Sat, 09 May 2026 01:46:53 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a636d648eeb2c78808a8a040db0b294805d93b2648392a54c7f3a7cbc92065bb`  
		Last Modified: Sat, 09 May 2026 01:46:58 GMT  
		Size: 138.1 MB (138068550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39ce150b18c4514648b21b02dae1c758fdaaa50834f776391556f2b7dc2af97`  
		Last Modified: Sat, 09 May 2026 01:46:53 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:d436d145db7d6b5f41ae7302271623aeeb8f352fa07d3ddb2d5b734f286ac063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11372931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc69ecaf04d9d4ebbf5f4b4b09db75ebad2b6de62f97101912e26c86027481a`

```dockerfile
```

-	Layers:
	-	`sha256:cf7ee95185603a8b531e14ba9804e1b361aeb08071b6ac379f6d2f8b2cd9906d`  
		Last Modified: Sat, 09 May 2026 01:46:54 GMT  
		Size: 11.4 MB (11351735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bf2376a9bb581586b65a9562055cfd3855423887f88502aaa846ea5a5582778`  
		Last Modified: Sat, 09 May 2026 01:46:53 GMT  
		Size: 21.2 KB (21196 bytes)  
		MIME: application/vnd.in-toto+json
