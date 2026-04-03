## `gradle:8-jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:0e3a2d316281f6070a9cefaa5e6d738ae651e8714a10f73be2dd8e6f09232053
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:88219ffa6118852c0f0db8e709c8750c7d176954ee6263794fe3aa0121939709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.7 MB (447740401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f628353bc0fb778481cbf155209ab55cd4cdfb7811e59ea4c96a00c8f1778854`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:09:28 GMT
ARG version=21.0.10.7-1
# Fri, 03 Apr 2026 17:09:28 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:09:28 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:09:28 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:09:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 03 Apr 2026 17:29:24 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 17:29:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 17:29:24 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 17:29:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 17:29:25 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 17:29:25 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 17:29:25 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 03 Apr 2026 17:29:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 03 Apr 2026 17:29:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 17:29:27 GMT
USER gradle
# Fri, 03 Apr 2026 17:29:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 03 Apr 2026 17:29:28 GMT
USER root
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91612493fd72368b685c337f3f583067a94ee0ef306766e8d11839845e7daf8`  
		Last Modified: Fri, 03 Apr 2026 17:09:55 GMT  
		Size: 170.2 MB (170192316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cabf8d9ab1cfffcc3d46d2a0189d55aa6aed007c3262477cd88ddad1d5b5256`  
		Last Modified: Fri, 03 Apr 2026 17:29:59 GMT  
		Size: 86.1 MB (86070137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a349f43f871901f701baf2cf122995c390be083460f4ce9774d601f378b75a`  
		Last Modified: Fri, 03 Apr 2026 17:29:55 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6f8dc0e2e22f5d3e2c504c3964390b4492cb01abf99f76a5769b5191547036`  
		Last Modified: Fri, 03 Apr 2026 17:30:00 GMT  
		Size: 137.4 MB (137388268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f937f8e9186bc0a39d85979c5757a2ef502820ce51e37c7bbcca43583f7ee4a`  
		Last Modified: Fri, 03 Apr 2026 17:29:55 GMT  
		Size: 54.9 KB (54912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:38c2f05484f3826364fcfda8548f90456ed24e155ca6e972df4084743c68d865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11363236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef5754c51d94092460e34cc2e26f4b4db2a6be7842ce0a06b69fea425933762`

```dockerfile
```

-	Layers:
	-	`sha256:a44c1c4a008993292c4f92f091c532fc875ada54d0b767faac1a7f40eb6a6258`  
		Last Modified: Fri, 03 Apr 2026 17:29:56 GMT  
		Size: 11.3 MB (11342355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ff85dc7a4f7024f38fada12b8866fb958578842bd8c9163e2240689d060d2da`  
		Last Modified: Fri, 03 Apr 2026 17:29:55 GMT  
		Size: 20.9 KB (20881 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a31b84a0d42d3ec5b925364e78e96f85244f701bc051efb120714a0259b13eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.4 MB (444399542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c64f04294f14822640d39b18bde6d36efc4f1b408c1954196d4b192e237976`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:16:52 GMT
ARG version=21.0.10.7-1
# Fri, 03 Apr 2026 17:16:52 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:16:52 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:16:52 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:16:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 03 Apr 2026 17:29:28 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 17:29:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 17:29:28 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 17:29:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 17:29:28 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 17:29:28 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 17:29:28 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 03 Apr 2026 17:29:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 03 Apr 2026 17:29:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 17:29:31 GMT
USER gradle
# Fri, 03 Apr 2026 17:29:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 03 Apr 2026 17:29:31 GMT
USER root
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1644240415892ae6adc3944665a6a99351819a4043adb69ab2e97d280a16aae6`  
		Last Modified: Fri, 03 Apr 2026 17:17:15 GMT  
		Size: 168.5 MB (168466722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c537cd5171be3895d4e733df894682a72cac5e78bd21ac1f17035b0aa64fea9`  
		Last Modified: Fri, 03 Apr 2026 17:30:03 GMT  
		Size: 85.5 MB (85541972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8020575d95d3a68fef497310b0fe0c1551539d7687e32d4d520c9b3084823bc6`  
		Last Modified: Fri, 03 Apr 2026 17:29:59 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fb55bb5b2aa220329b54c90c5aa9184af5b5b7f847899c3c3b53a653281e08`  
		Last Modified: Fri, 03 Apr 2026 17:30:05 GMT  
		Size: 137.4 MB (137388269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d8238e0a073f099096383a20847577027599594346853748df655bc07b0ec2`  
		Last Modified: Fri, 03 Apr 2026 17:29:59 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:f519c491f5c99a791d3a9d508698a671d4320d769bad3644e5a606813d0c3ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11362387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04175d1687e2b7acb6f71c351afcefa020e45f43607b32c55b133d1e4fe53184`

```dockerfile
```

-	Layers:
	-	`sha256:b9faf01efb44e1a6607b2c5eea25c8b42dcb9434ccdb63ab87623b3275757331`  
		Last Modified: Fri, 03 Apr 2026 17:30:00 GMT  
		Size: 11.3 MB (11341333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4f47565a4abae7b3f8754610a85f5e6f2b1b53046c4aaf199dd65e974d8b23d`  
		Last Modified: Fri, 03 Apr 2026 17:29:59 GMT  
		Size: 21.1 KB (21054 bytes)  
		MIME: application/vnd.in-toto+json
