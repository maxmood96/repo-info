## `gradle:9-jdk26-corretto-al2023`

```console
$ docker pull gradle@sha256:0b5e9b945b505df89ca9e7964fb1a01272daa8b7ed7eb071c24fc012ac22b508
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk26-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:2b8758723bbfef161c48e6a34e3d66ef827faf3b459b7b7708fad54a2e31838b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.4 MB (474433283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d43643b08a9530c5611e3f67ed5b6411bb7b8044f1781107c00a2cbfa8866d8`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:40 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:14:02 GMT
ARG version=26.0.1.8-1
# Fri, 24 Apr 2026 00:14:02 GMT
ARG package_version=1
# Fri, 24 Apr 2026 00:14:02 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:14:02 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:14:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Tue, 28 Apr 2026 23:31:45 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:31:45 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:31:45 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:31:45 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:31:45 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:31:45 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:31:45 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:31:45 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:31:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:31:48 GMT
USER gradle
# Tue, 28 Apr 2026 23:31:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:31:48 GMT
USER root
```

-	Layers:
	-	`sha256:60406c832328f9a4f3aa21eb9cb5b2182d79ad008cd21f0bbac4517c1836be2e`  
		Last Modified: Tue, 14 Apr 2026 01:03:42 GMT  
		Size: 54.6 MB (54569705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f87b01bb5180aa982f4efb9e7cb22d986f93d4249ff9fd60ca7218567db2884`  
		Last Modified: Fri, 24 Apr 2026 00:14:27 GMT  
		Size: 193.4 MB (193449987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a3f145bbc1e33a5ebb86b5ad7f4696b57b32aadad99d830b27012535913987`  
		Last Modified: Tue, 28 Apr 2026 23:32:20 GMT  
		Size: 86.2 MB (86150406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c44f848525059362989e0548276792e6b05c26fa9a2d816ecc5d42aaa9b6e41`  
		Last Modified: Tue, 28 Apr 2026 23:32:16 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb1a11c5f2daca40e4a947702e2bf688fb4cafc6b6ea1881875b94c264abd5e`  
		Last Modified: Tue, 28 Apr 2026 23:32:21 GMT  
		Size: 140.2 MB (140235902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed6edbd2b16a721fc59bb7f3ea5a664b6402ec468d663f687d793735395b82c`  
		Last Modified: Tue, 28 Apr 2026 23:32:16 GMT  
		Size: 25.6 KB (25604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:b1a8f2675c8e17ddc304a49daf68fc954f7fac842f1e81623ba1575823ff2950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11397019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab4c5ece4b353a558220ca29bc8b680c7b1f9e1fb877a115483a47248b00486`

```dockerfile
```

-	Layers:
	-	`sha256:e647dab2061d299292d06bbd6ee40d0a8c22495ef608a3ea66e4e263b7ab5e1c`  
		Last Modified: Tue, 28 Apr 2026 23:32:17 GMT  
		Size: 11.4 MB (11375368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe862665a75610633226c2d0eafd6552eeec6b73dd7dd0cf29a2d03fb88cea8`  
		Last Modified: Tue, 28 Apr 2026 23:32:16 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ed927b1627ba74eeb1b6cf3c15dbdd0ac00ad84322900cab7c052dcbaf7ebbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.6 MB (470648897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ec6366cfef1ba523a57b4a1fa81d8da4aa8727b0b4a936c362e95141c926b9`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:02 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:14:53 GMT
ARG version=26.0.1.8-1
# Fri, 24 Apr 2026 00:14:53 GMT
ARG package_version=1
# Fri, 24 Apr 2026 00:14:53 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:14:53 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:14:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Tue, 28 Apr 2026 23:33:07 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:33:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:33:07 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:33:07 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:33:07 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:33:07 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:33:07 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:33:07 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:33:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:33:10 GMT
USER gradle
# Tue, 28 Apr 2026 23:33:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:33:11 GMT
USER root
```

-	Layers:
	-	`sha256:a89c935522476873ac76a02a8b4103cba17c6900bdcb1d98998ed64657edf59f`  
		Last Modified: Tue, 14 Apr 2026 02:24:36 GMT  
		Size: 53.5 MB (53452253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d8e233aa6f445f4d6449e2fca0acaa53a4ea5ef7c115b1ac7964fd61baa648`  
		Last Modified: Fri, 24 Apr 2026 00:15:24 GMT  
		Size: 191.3 MB (191271425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39616774cd714033628514b0d1810a4b86e3d093c54fe2689cf6880151f0de37`  
		Last Modified: Tue, 28 Apr 2026 23:33:43 GMT  
		Size: 85.7 MB (85658251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673996e96bc2b53985044941ecfeaa66241af89ccfe3938d93d8abc8f20f9cf4`  
		Last Modified: Tue, 28 Apr 2026 23:33:39 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7000e0a48959b6df4d7d4adf4acd3f767a29c8f03dde30a1b63468d3c40ff79f`  
		Last Modified: Tue, 28 Apr 2026 23:33:45 GMT  
		Size: 140.2 MB (140235939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37d03d76af19db8a7d8b170d43d8598cfe1b8a77d3a2a888480ae8f39ab5618`  
		Last Modified: Tue, 28 Apr 2026 23:33:39 GMT  
		Size: 29.4 KB (29350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:60042b82682db9eb262564973d417cf371ee3249b208c6d43825cc78111581cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11396225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4725c9574f3158f9c710cfa4c231601f279b32274d666e01d6ff19e1d888ff`

```dockerfile
```

-	Layers:
	-	`sha256:5349d85f17dd4498e6b3346284899ec172d0f4cd86d4c574154b3390e199d73a`  
		Last Modified: Tue, 28 Apr 2026 23:33:40 GMT  
		Size: 11.4 MB (11374377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2973af84d7e70a1ec3d059c68311d25e45ed869bf672685fbdc2ff7f9e55a642`  
		Last Modified: Tue, 28 Apr 2026 23:33:39 GMT  
		Size: 21.8 KB (21848 bytes)  
		MIME: application/vnd.in-toto+json
