## `gradle:7-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:cafa0837e3ad1f8c8c64585604445ef05827f1ac689863993ce3b2a3a70aed6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:b4c1d2002f549102a798bfcb55d0c35fb06dd6666472885aba155b403c768e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.4 MB (425432029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f775cacee977ebca9866aae1da8fcc395011b6c5bc12746cc5ed0fe4ef32d36`
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
# Fri, 14 Nov 2025 03:14:17 GMT
CMD ["gradle"]
# Fri, 14 Nov 2025 03:14:17 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 14 Nov 2025 03:14:17 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 14 Nov 2025 03:14:18 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 14 Nov 2025 03:14:18 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 14 Nov 2025 03:14:18 GMT
WORKDIR /home/gradle
# Fri, 14 Nov 2025 03:14:18 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 14 Nov 2025 03:14:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 14 Nov 2025 03:14:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 14 Nov 2025 03:14:21 GMT
USER gradle
# Fri, 14 Nov 2025 03:14:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 14 Nov 2025 03:14:21 GMT
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
	-	`sha256:6f513e58511b2581746ff8e0fe31db65347575349ef8fd8f4ade4af3cbab539e`  
		Last Modified: Fri, 14 Nov 2025 03:15:08 GMT  
		Size: 86.0 MB (86023240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f2000c0eec61beb5fe3728e784d41af0dc68fea52cc48ca4c860b572606648`  
		Last Modified: Fri, 14 Nov 2025 03:14:55 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db42468fa7252372b656706eb8bb57330a21191734929ac418acb3fb3d61780`  
		Last Modified: Fri, 14 Nov 2025 10:12:56 GMT  
		Size: 128.5 MB (128469440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c516deee09ed73bc012f60d0215d83763b2ca1b83ce5cbda3683457a8ca959`  
		Last Modified: Fri, 14 Nov 2025 03:14:55 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:a589f1d4b06f235c6a8a171e43cf3edad3f6fd8385835118d62504b2bc86e794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11271175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece30eb1f8bee2c50e4290ef94b010880d14696f4bd9a3dce21c0241435ec7b5`

```dockerfile
```

-	Layers:
	-	`sha256:d70dd20c352900ad3afa79441d130f877e01d6b208a2e4174773da2b08bbf91a`  
		Last Modified: Fri, 14 Nov 2025 06:18:51 GMT  
		Size: 11.3 MB (11250463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccf7a23939f87053cba7a3cb78f00187b483d2f3717694657a9c64a24415fa75`  
		Last Modified: Fri, 14 Nov 2025 06:18:52 GMT  
		Size: 20.7 KB (20712 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ff6c01fb6837d2b53ad9ceef738f84525f0f85cd468853dac550324a9b9240c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.7 MB (422657644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f926eac272c30c95048bffe0d40da14f76f72d005e39c2f884b1e19647fe0ba9`
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
# Fri, 14 Nov 2025 03:14:51 GMT
CMD ["gradle"]
# Fri, 14 Nov 2025 03:14:51 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 14 Nov 2025 03:14:51 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 14 Nov 2025 03:14:52 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 14 Nov 2025 03:14:52 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 14 Nov 2025 03:14:52 GMT
WORKDIR /home/gradle
# Fri, 14 Nov 2025 03:14:52 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 14 Nov 2025 03:14:52 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 14 Nov 2025 03:14:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 14 Nov 2025 03:14:54 GMT
USER gradle
# Fri, 14 Nov 2025 03:14:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 14 Nov 2025 03:14:55 GMT
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
	-	`sha256:9c0d3403465001b1977783730c5e4633037564997e93c7063f60e3d88a379133`  
		Last Modified: Fri, 14 Nov 2025 03:15:38 GMT  
		Size: 85.5 MB (85534240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64278192afddc16ea23cb744c8bbbbb87d6c56c45ea66eb0d686f08cd9945eac`  
		Last Modified: Fri, 14 Nov 2025 03:15:31 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fca108a791d552ac81a8753360d4ca04930f3d021fdf641a6628e54439ab480`  
		Last Modified: Fri, 14 Nov 2025 10:14:31 GMT  
		Size: 128.5 MB (128469414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31443e14b17ff74444177b6a9d4f2bf0ed92602d955ce4f3a8bf28492ec9688e`  
		Last Modified: Fri, 14 Nov 2025 03:15:31 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:1a7da8417793e71f821efea4bc4b68452918f625b3869ce965ed7981adf1b68f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11270324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffbe02931cb4476c8fcbecb7b21b1821db31a8e39c6bce3454f566f70804124`

```dockerfile
```

-	Layers:
	-	`sha256:66311b93b4a668af6db00a8a019109a8c583f78a1dfb47cff6d127f21d422d1e`  
		Last Modified: Fri, 14 Nov 2025 06:19:01 GMT  
		Size: 11.2 MB (11249438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1269d447e51807ee603f271533a1778643f8926419972ed456117c1627900a71`  
		Last Modified: Fri, 14 Nov 2025 06:19:02 GMT  
		Size: 20.9 KB (20886 bytes)  
		MIME: application/vnd.in-toto+json
