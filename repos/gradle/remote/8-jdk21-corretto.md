## `gradle:8-jdk21-corretto`

```console
$ docker pull gradle@sha256:5d2e6415df3c5f77759935421f10a35331579349eda74209404cb619b9462cb2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:ff34358a4975affe94a1ac0df5a51bd00398a80924373388b058b89b84cf2ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.3 MB (449334632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c834e5bddb22209268235f4be8d85ec89bfff76feda146507d424b080efcf919`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 May 2026 20:12:06 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:06 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:12:23 GMT
ARG version=21.0.11.10-1
# Fri, 22 May 2026 21:12:23 GMT
ARG package_version=1
# Fri, 22 May 2026 21:12:23 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:12:23 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:12:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 22 May 2026 22:06:46 GMT
CMD ["gradle"]
# Fri, 22 May 2026 22:06:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 May 2026 22:06:46 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 22 May 2026 22:06:46 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 22 May 2026 22:06:46 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 May 2026 22:06:46 GMT
WORKDIR /home/gradle
# Fri, 22 May 2026 22:06:46 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 22 May 2026 22:06:46 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 22 May 2026 22:06:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 22 May 2026 22:06:49 GMT
USER gradle
# Fri, 22 May 2026 22:06:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 22 May 2026 22:06:49 GMT
USER root
```

-	Layers:
	-	`sha256:c00ef2b893da480d77c559b6862d1ad542cc91c6bb2d3106a00cb8d9c141b797`  
		Last Modified: Fri, 15 May 2026 20:34:40 GMT  
		Size: 54.6 MB (54572440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff121652fd8f348860139cbe6d75ae68e9269ce4de11a62feb50538f65ba9d01`  
		Last Modified: Fri, 22 May 2026 21:12:44 GMT  
		Size: 170.4 MB (170447593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728c8fdbee4fb66367cbdcaa47f9dd781def43d02bc55c9841da6dc97ec87f94`  
		Last Modified: Fri, 22 May 2026 22:07:21 GMT  
		Size: 86.2 MB (86189478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54cf1250f8fe0ad61fd3aa52d71b522270252b7e1b2d3c51fd47c671063a45`  
		Last Modified: Fri, 22 May 2026 22:07:18 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b06f81749c24b5fa1f869a499cf6840e0d828ef3224797476ff09bfa0663b5`  
		Last Modified: Fri, 22 May 2026 22:07:22 GMT  
		Size: 138.1 MB (138068537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38cdece08661835e54a74265d25bcc986078ffab0aa8dec26c0318638bd1224`  
		Last Modified: Fri, 22 May 2026 22:07:18 GMT  
		Size: 54.9 KB (54903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:a147b53dd283d7b6ca5ada5b6365d3590218c8029153ace7dc13af126b737443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11373779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26630e8404f749f3f5f8e3b6b17c0b56af02035533a16798ca502f7db1fe4917`

```dockerfile
```

-	Layers:
	-	`sha256:f51ca0e95763e015f8d379e13fb782d8a446e251c2fcc7c4cb771f68e5d6a24d`  
		Last Modified: Fri, 22 May 2026 22:07:18 GMT  
		Size: 11.4 MB (11352756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c7067e257333f1803a714c0116f7613d0b6f384108957b8fb4adace9004e30`  
		Last Modified: Fri, 22 May 2026 22:07:18 GMT  
		Size: 21.0 KB (21023 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:77e3fa2838bb7e0e701dfd0dd6dc67a2d640416c9f8bfab2bf25b021e9280215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.0 MB (445996320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a613d2683bc2f43d1d56383ae9b4d1710ea429ed36e5f8ba5ae5d86eb083dc90`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 May 2026 20:12:25 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:25 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:12:07 GMT
ARG version=21.0.11.10-1
# Fri, 22 May 2026 21:12:07 GMT
ARG package_version=1
# Fri, 22 May 2026 21:12:07 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:12:07 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:12:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 22 May 2026 22:06:55 GMT
CMD ["gradle"]
# Fri, 22 May 2026 22:06:55 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 May 2026 22:06:55 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 22 May 2026 22:06:55 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 22 May 2026 22:06:55 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 May 2026 22:06:55 GMT
WORKDIR /home/gradle
# Fri, 22 May 2026 22:06:55 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 22 May 2026 22:06:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 22 May 2026 22:06:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 22 May 2026 22:06:59 GMT
USER gradle
# Fri, 22 May 2026 22:06:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 22 May 2026 22:06:59 GMT
USER root
```

-	Layers:
	-	`sha256:a92e5e4b9e90f970dfdf3c3258e673bb767c6401beba9985a3b635162466eedd`  
		Last Modified: Fri, 15 May 2026 20:34:37 GMT  
		Size: 53.5 MB (53454415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c09cffee1deca5889479ce29d580c920fd0813f91a6e360f166fd36a236292a`  
		Last Modified: Fri, 22 May 2026 21:12:32 GMT  
		Size: 168.7 MB (168720490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4b4c9d41e9c32e91849a64809a9039836f491681a815072d0f52311ae34e6d`  
		Last Modified: Fri, 22 May 2026 22:07:32 GMT  
		Size: 85.7 MB (85691671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2606bfd8967c31aa756b01e89120e424560b477ced15a99fd99214670f5925`  
		Last Modified: Fri, 22 May 2026 22:07:28 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7403385b7e0a998e27ece9bcc60e2f2b271c8a840fd1c5423cc77800889b08b2`  
		Last Modified: Fri, 22 May 2026 22:07:33 GMT  
		Size: 138.1 MB (138068533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed00e249dc511107dcf742c979dbe9a6f5ebd789589e37e3698ff648447e1a79`  
		Last Modified: Fri, 22 May 2026 22:07:29 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:b1429599be4fd602bf40fa52ce46a40faef4086bbb578cc0e153f0dbc77b1c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11372929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b920a4e3601e91d65b415fa14e09cf3021d2790b82f75c699e9d77bcdd7320`

```dockerfile
```

-	Layers:
	-	`sha256:132c3a0183c0a2e3cd0d0820bede0ad0061d8fa6e3ae4eece0223208e6a9eda1`  
		Last Modified: Fri, 22 May 2026 22:07:29 GMT  
		Size: 11.4 MB (11351735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e39dcce85885cf7e4a56eb85bed58c4ed6b5a993a2d60ef67fa12c35b992cf6`  
		Last Modified: Fri, 22 May 2026 22:07:28 GMT  
		Size: 21.2 KB (21194 bytes)  
		MIME: application/vnd.in-toto+json
