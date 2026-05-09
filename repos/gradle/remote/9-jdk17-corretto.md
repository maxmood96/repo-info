## `gradle:9-jdk17-corretto`

```console
$ docker pull gradle@sha256:5b65df19596adcad6697fdbd5e036882087a222a09f38e9a711edbfeeff11cfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:437ddd4d1d1c624054357bd1c039ddf425e9e3d0c26d506c8f42d127815259a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.2 MB (438161184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0618e0c2ced9a2a03ac44887b9cd49d1154d8feebdc6920c33cc7a9da15d9ed`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:18:09 GMT
ARG version=17.0.19.10-1
# Sat, 09 May 2026 00:18:09 GMT
ARG package_version=1
# Sat, 09 May 2026 00:18:09 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:18:09 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:18:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 09 May 2026 01:20:22 GMT
CMD ["gradle"]
# Sat, 09 May 2026 01:20:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 09 May 2026 01:20:22 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 09 May 2026 01:20:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 09 May 2026 01:20:22 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 09 May 2026 01:20:22 GMT
WORKDIR /home/gradle
# Sat, 09 May 2026 01:20:22 GMT
ENV GRADLE_VERSION=9.5.0
# Sat, 09 May 2026 01:20:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Sat, 09 May 2026 01:20:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 09 May 2026 01:20:25 GMT
USER gradle
# Sat, 09 May 2026 01:20:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 09 May 2026 01:20:25 GMT
USER root
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6309fe2525fbad905fb54629ab668afd9f6065eb3bc1686f59c768bd61e63066`  
		Last Modified: Sat, 09 May 2026 00:18:31 GMT  
		Size: 157.2 MB (157155542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f1b62b10c4bbd0c430a53dbbd3c8c9a207bfc1a37bd017210c930f9b64bc0b`  
		Last Modified: Sat, 09 May 2026 01:20:57 GMT  
		Size: 86.2 MB (86165612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70de344eeeb55453b5150bd8a1d82217e9378a5a1147d264c5ef4e51feddc78`  
		Last Modified: Sat, 09 May 2026 01:20:54 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc2af802fd1378cd8cf84f6cef47ad6f44323450b0ad000795d453c327ff1ea`  
		Last Modified: Sat, 09 May 2026 01:20:59 GMT  
		Size: 140.2 MB (140235942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf035bb617f0b9bd0d9b73d3b97ce05122dc2660d7b0eddb1e69f54fddd06b7`  
		Last Modified: Sat, 09 May 2026 01:20:54 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:e645b3513356f1982d3f93caa21ebccb8a5537bad8bdfb4f15f0d76aa4c4a799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00848a540f0fe9d3112d94950eba721631940f1690ad75f5af6ebdb95e9e3505`

```dockerfile
```

-	Layers:
	-	`sha256:76a9fef0b1da06994efa48d99ef4d612701f36b326a93f6b3c4f25a3eb3f272e`  
		Last Modified: Sat, 09 May 2026 01:20:55 GMT  
		Size: 11.4 MB (11365660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a8171711050af9e6a756618e17d673810601028f686a567e01e430cd97fa22a`  
		Last Modified: Sat, 09 May 2026 01:20:54 GMT  
		Size: 21.5 KB (21497 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e8eb9d81fef205a0f2706d81147a797f8f5e6f0db87145e17e7aebc0878dd0c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.4 MB (435367632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee66e1abc06e9c4d19b4f84654530bd09b9adf966427054e33c941ea2e1aa24c`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:15:52 GMT
ARG version=17.0.19.10-1
# Sat, 09 May 2026 00:15:52 GMT
ARG package_version=1
# Sat, 09 May 2026 00:15:52 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:15:52 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:15:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 09 May 2026 01:45:38 GMT
CMD ["gradle"]
# Sat, 09 May 2026 01:45:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 09 May 2026 01:45:38 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 09 May 2026 01:45:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 09 May 2026 01:45:38 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 09 May 2026 01:45:38 GMT
WORKDIR /home/gradle
# Sat, 09 May 2026 01:45:38 GMT
ENV GRADLE_VERSION=9.5.0
# Sat, 09 May 2026 01:45:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Sat, 09 May 2026 01:45:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 09 May 2026 01:45:41 GMT
USER gradle
# Sat, 09 May 2026 01:45:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 09 May 2026 01:45:42 GMT
USER root
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772fbf79450c266cc92f9965e1f1e49f242635187b875a839de4e43a7de43446`  
		Last Modified: Sat, 09 May 2026 00:16:15 GMT  
		Size: 156.0 MB (155989906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0061cdee324b3d13e8af02db9970ce9847d5c3a66e4bdf5e03037fb136664c8`  
		Last Modified: Sat, 09 May 2026 01:46:15 GMT  
		Size: 85.7 MB (85653794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcae005b65badfa53a1e6a2f772f31d749a1967f2d561cd5087fb6bfb1b6bea`  
		Last Modified: Sat, 09 May 2026 01:46:09 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adb64495a7dc7f1508437b92b8922ebdbdeb604ee8b59727dcceab86fc4376d`  
		Last Modified: Sat, 09 May 2026 01:46:17 GMT  
		Size: 140.2 MB (140235943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b572b69f4768a760771119c79b0de29be5daa3fd5b8ecba102f0bf3853c43ecf`  
		Last Modified: Sat, 09 May 2026 01:46:09 GMT  
		Size: 29.3 KB (29336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:1809d1e0018460eebe706df2918c0f1c8796407169288ddf8bf78f5658b56b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11386354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f2745fba569d7a5db9ae39c1720b05a0ec34269be21c9ecdd6a9e65de26407`

```dockerfile
```

-	Layers:
	-	`sha256:9136ac4bc8dcb3e90c02ac71034bf706c489a2f70d921ab0f769e2ebe2270a92`  
		Last Modified: Sat, 09 May 2026 01:46:10 GMT  
		Size: 11.4 MB (11364660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f47108a541464a30be1fc4aaf4088ad42c0a5c3ba9772c4f6b6a53d1232eb4bd`  
		Last Modified: Sat, 09 May 2026 01:46:09 GMT  
		Size: 21.7 KB (21694 bytes)  
		MIME: application/vnd.in-toto+json
