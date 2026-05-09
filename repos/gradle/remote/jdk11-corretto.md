## `gradle:jdk11-corretto`

```console
$ docker pull gradle@sha256:9c5e4d77ce4b569481ac472516d1149ac6e936b55c2292ac08511a58200c706b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:747936a2af530f5afe25fc66e5fb7a1befd442cd73e40ce1d37acfd27ad5eb8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.3 MB (432343382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d23b70e5aacd00cef49787d0a5149e7989fbbc4bcfe1882a46097fe55682d4`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:18:06 GMT
ARG version=11.0.31.11-1
# Sat, 09 May 2026 00:18:06 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:18:06 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:18:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 09 May 2026 01:21:10 GMT
CMD ["gradle"]
# Sat, 09 May 2026 01:21:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 09 May 2026 01:21:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 09 May 2026 01:21:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 09 May 2026 01:21:10 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 09 May 2026 01:21:10 GMT
WORKDIR /home/gradle
# Sat, 09 May 2026 01:21:10 GMT
ENV GRADLE_VERSION=8.14.5
# Sat, 09 May 2026 01:21:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Sat, 09 May 2026 01:21:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 09 May 2026 01:21:13 GMT
USER gradle
# Sat, 09 May 2026 01:21:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 09 May 2026 01:21:13 GMT
USER root
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137e8ef4b5fb927c0c86de92b3247666810672cabd7e058c5262c750d5d34c79`  
		Last Modified: Sat, 09 May 2026 00:18:27 GMT  
		Size: 153.5 MB (153472393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c52ead6352cd6bda28c6b5b2eea567b6785bed353b64a74acebcf5801584b4`  
		Last Modified: Sat, 09 May 2026 01:21:44 GMT  
		Size: 86.2 MB (86169068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777ee6882eabd265f4baea120cc491a15c4727d871591b4b672de78cf7e06f41`  
		Last Modified: Sat, 09 May 2026 01:21:40 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c7c70c5ae69ca91f7afc1b2f753f0c91d6b56f2d30a5779d7d43e46b7f812f`  
		Last Modified: Sat, 09 May 2026 01:21:45 GMT  
		Size: 138.1 MB (138068534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea50c3525f401ec5c567a8d879f8565f5fc42a6c9d765232854a1c29e8deaaeb`  
		Last Modified: Sat, 09 May 2026 01:21:40 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:9fe8caf59877b7d4cfff91c09cb219a520415030d22d6686bdb552f239594855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11397328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d532011a516976facb1199ad60eda19728340baa694dafeaa646ee9c8fb24a7b`

```dockerfile
```

-	Layers:
	-	`sha256:3535c508dd9b0f1b18deaab4bd7d8b48634ac424006e2fff8bb45048ecf361cb`  
		Last Modified: Sat, 09 May 2026 01:21:41 GMT  
		Size: 11.4 MB (11375663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bce65091aba776c69a5d32c4b4a04cf60ebd46c9e2bebcb97605b29ba53ed6f1`  
		Last Modified: Sat, 09 May 2026 01:21:40 GMT  
		Size: 21.7 KB (21665 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3c845a401dfdeef3363153b3e8ac370cb7bb266b0d7c3b4cbeed4e1ba78c5bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.3 MB (429296009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09fcfca4df977524ccd75579c1e7ecf878479ea3d8137548f6a44b6292dfa82`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:15:25 GMT
ARG version=11.0.31.11-1
# Sat, 09 May 2026 00:15:25 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:15:25 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:15:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 09 May 2026 01:46:25 GMT
CMD ["gradle"]
# Sat, 09 May 2026 01:46:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 09 May 2026 01:46:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 09 May 2026 01:46:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 09 May 2026 01:46:25 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 09 May 2026 01:46:25 GMT
WORKDIR /home/gradle
# Sat, 09 May 2026 01:46:25 GMT
ENV GRADLE_VERSION=8.14.5
# Sat, 09 May 2026 01:46:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Sat, 09 May 2026 01:46:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 09 May 2026 01:46:28 GMT
USER gradle
# Sat, 09 May 2026 01:46:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 09 May 2026 01:46:29 GMT
USER root
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8763299e6b6a5390624676a6a883b80df08afbd0fe328882a6aa37029abd1826`  
		Last Modified: Sat, 09 May 2026 00:15:47 GMT  
		Size: 152.1 MB (152051820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f64d9b757224bc912d9a57471f9f8d8ec9f29d828b6bec4ea5e0e6e501805c`  
		Last Modified: Sat, 09 May 2026 01:47:01 GMT  
		Size: 85.7 MB (85657469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabe58a36ccbfd3a014d0b3fc08452d3f10d21ba89760c3f7dcb8c58664dfce5`  
		Last Modified: Sat, 09 May 2026 01:46:57 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a293ef562f13ba5506beb0d23f912a886c1c75cf23ce62b6112e18e9b606ff`  
		Last Modified: Sat, 09 May 2026 01:47:02 GMT  
		Size: 138.1 MB (138068531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503968527bd09cafb542ae9b4f761f83b9bd0a84288b6c14f3a3a95896741fe3`  
		Last Modified: Sat, 09 May 2026 01:46:58 GMT  
		Size: 59.5 KB (59533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:a74ac925038adb8eb62e5207c99454aad9052a4461386e160d25d1ad3fa3841a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11397368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838dd8a395e0d9435d129e60c443c31c85f2e7d77d45348982724b47ac7857a4`

```dockerfile
```

-	Layers:
	-	`sha256:dccece9af2f5a4154c1bba3690472aa97ea05583f5322ac9ae020f51bba7c377`  
		Last Modified: Sat, 09 May 2026 01:46:58 GMT  
		Size: 11.4 MB (11375506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f32c1470ee7c50e8105386dc2c120ee6002eb1c7e469a8a8faf54462e56c1395`  
		Last Modified: Sat, 09 May 2026 01:46:57 GMT  
		Size: 21.9 KB (21862 bytes)  
		MIME: application/vnd.in-toto+json
