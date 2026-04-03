## `gradle:9-jdk17-corretto`

```console
$ docker pull gradle@sha256:8337ca045b17927c260bc60f3c528ff3467e3a803faeefb1b2812247df21161a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:62d3f51bfd63d6c4961a158ff6a7398c71c35f61aba6aea20c1cd42783803275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.8 MB (434849587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92220184d2deafd9e73dbb5c8e5e97d20bcd997cfb6611166942133f24c0ea32`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:07:56 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 17:07:56 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:07:56 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:07:56 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:07:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 03 Apr 2026 17:29:23 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 17:29:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 17:29:23 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 17:29:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 17:29:24 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 17:29:24 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 17:29:24 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 03 Apr 2026 17:29:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 03 Apr 2026 17:29:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 17:29:26 GMT
USER gradle
# Fri, 03 Apr 2026 17:29:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 03 Apr 2026 17:29:27 GMT
USER root
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d132f643ccc51adef2f8116c0839f1a3410d13832ab23aab291b4c6648c895`  
		Last Modified: Fri, 03 Apr 2026 17:08:16 GMT  
		Size: 156.9 MB (156911186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5682ab9cc3bf948e36e70253355c9f485dcd33176d24d7d3233f256df8b91db`  
		Last Modified: Fri, 03 Apr 2026 17:29:57 GMT  
		Size: 86.1 MB (86069686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e68a3a2112fd914094e43d65014e3f8c75606e9de20e9837c7c48b16cd5921a`  
		Last Modified: Fri, 03 Apr 2026 17:29:53 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36699a4ee5f3afa03c888b15324b688f7d63e9390a07acba1ce099d6ed23f45`  
		Last Modified: Fri, 03 Apr 2026 17:29:58 GMT  
		Size: 137.8 MB (137808335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efb9714b9d62c82758660d7adf18289a443d31d07f3afe6e8d58b375cb91cc1`  
		Last Modified: Fri, 03 Apr 2026 17:29:54 GMT  
		Size: 25.6 KB (25611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:28a47ba2193cd62e96f6d276c7ce4cad3f99a31547c35730740afbed57104812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11347829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd78d710f332881a9849fdff5ca278f30d55af5688cab4c7b986f5e6b8fed8d`

```dockerfile
```

-	Layers:
	-	`sha256:b2f0205551991562ad9bf80ff69a926adc65ecb7bcad5aee92d32a8ca7cbd560`  
		Last Modified: Fri, 03 Apr 2026 17:29:54 GMT  
		Size: 11.3 MB (11326332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ec0f9f1d5afb6a662a79ef266ae70e97c092197aa80d216b147b320bd0af6a`  
		Last Modified: Fri, 03 Apr 2026 17:29:53 GMT  
		Size: 21.5 KB (21497 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:fe678b87e7e4d73e2881160c602ce319b26f0f05d9038221ffbae25938f96bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.1 MB (432054059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa6aec8fb38a744a99b7bcb3e4fae8cc5ff729e205c7bda14e9e0267947af63`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:15:23 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 17:15:23 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:15:23 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:15:23 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:15:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 03 Apr 2026 17:28:18 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 17:28:18 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 17:28:18 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 17:28:18 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 17:28:18 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 17:28:18 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 17:28:18 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 03 Apr 2026 17:28:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 03 Apr 2026 17:28:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 17:28:21 GMT
USER gradle
# Fri, 03 Apr 2026 17:28:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 03 Apr 2026 17:28:21 GMT
USER root
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429711ba4253426e63ee61f0328e01ea895f7d5cae97ca247ad3ab091625ab5c`  
		Last Modified: Fri, 03 Apr 2026 17:15:45 GMT  
		Size: 155.7 MB (155727752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f6a0a746491411082e6ace714f01d2d30f980491fb30790e55a6214c9331d7`  
		Last Modified: Fri, 03 Apr 2026 17:28:52 GMT  
		Size: 85.5 MB (85545594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b2052dffd8e932e012aa62c00ac613a64b7305fd3a542d1729b5293381793a`  
		Last Modified: Fri, 03 Apr 2026 17:28:49 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc8476b1c2843f31f33bbdc5b93d540f455be659b8cc2eb9d0223aee73e9bdc`  
		Last Modified: Fri, 03 Apr 2026 17:28:53 GMT  
		Size: 137.8 MB (137808332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335ce08cc1c03a4c49381201898980de393cf869c5176238a5d409e4ed44be32`  
		Last Modified: Fri, 03 Apr 2026 17:28:49 GMT  
		Size: 29.3 KB (29329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:c7f16baddd1da0198375e17527d33b69456d83369c0970e2a379e044764c4563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11347025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6fada4ac4c05bb1a475857b4d206a5f0c61f9e9aa7af4431318a240c2771a3`

```dockerfile
```

-	Layers:
	-	`sha256:e3397bf553149fc4ee061c5980f5e80aefa997854f52e4a8abec0f4511ccd8da`  
		Last Modified: Fri, 03 Apr 2026 17:28:49 GMT  
		Size: 11.3 MB (11325331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ffab74f5c6a5bd82ef29a73d81aaaa019544dcc98d134f0b3e9e9ce7bf09367`  
		Last Modified: Fri, 03 Apr 2026 17:28:49 GMT  
		Size: 21.7 KB (21694 bytes)  
		MIME: application/vnd.in-toto+json
