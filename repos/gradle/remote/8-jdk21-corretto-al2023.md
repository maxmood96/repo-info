## `gradle:8-jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:646471e3dc14b105c0c794f22a53ee4f00f38d69cf4379e675ea138389512e7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:0e1b1270c498ce39f364380ba44370824d8ec2554fd1c4597901b0a1105a0c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.4 MB (449405978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4553bfa190605f772596904797594ab50c6f4e912f1acf119547c85426c5848`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:24 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:24 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:31 GMT
ARG version=21.0.11.10-1
# Tue, 09 Jun 2026 21:12:31 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:12:31 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:12:31 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 09 Jun 2026 22:05:24 GMT
CMD ["gradle"]
# Tue, 09 Jun 2026 22:05:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 09 Jun 2026 22:05:24 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 09 Jun 2026 22:05:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 09 Jun 2026 22:05:24 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 09 Jun 2026 22:05:24 GMT
WORKDIR /home/gradle
# Tue, 09 Jun 2026 22:05:24 GMT
ENV GRADLE_VERSION=8.14.5
# Tue, 09 Jun 2026 22:05:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Tue, 09 Jun 2026 22:05:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 09 Jun 2026 22:05:26 GMT
USER gradle
# Tue, 09 Jun 2026 22:05:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 09 Jun 2026 22:05:27 GMT
USER root
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655da4f67bbe8b448c113c5608d6d6a794180419e8ce9d70d44ad817230d8f55`  
		Last Modified: Tue, 09 Jun 2026 21:12:55 GMT  
		Size: 170.4 MB (170445528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba86d5e02bf4a0df978449a3ee5309158940b290df08b01022d099a27a68474`  
		Last Modified: Tue, 09 Jun 2026 22:05:55 GMT  
		Size: 86.3 MB (86264173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e40b34af0bc5b0064fa8a273241e6db3003c6eed2e840a332238b279528bfc0`  
		Last Modified: Tue, 09 Jun 2026 22:05:51 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e32f6aa09f7be43c89dd58ea2c25694fe8f5787b93f55340f18722568bc0ff`  
		Last Modified: Tue, 09 Jun 2026 22:05:56 GMT  
		Size: 138.1 MB (138068534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa074f192ea6af42058ec8d6e9f06775a76c0a09a98251780818c10fb8bb5978`  
		Last Modified: Tue, 09 Jun 2026 22:05:51 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:687dc277d3046f2d76049b5eb7c55d054cfa18da4a99db447cbd6baa4fa16e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11373781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7585bd270a7b36c36feac33a7fd111d2ae8e4c9880235c3d61a449e459555a00`

```dockerfile
```

-	Layers:
	-	`sha256:c8d283548c29c7fc2b1807596d75b6873b19f9a72e88dcf33c96ab6140cfa8fe`  
		Last Modified: Tue, 09 Jun 2026 22:05:52 GMT  
		Size: 11.4 MB (11352758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7b734c3bcd0303a081ed39ce07e4077c66899bf731313ccd2c11fcd3314a51b`  
		Last Modified: Tue, 09 Jun 2026 22:05:51 GMT  
		Size: 21.0 KB (21023 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e8c2e25b53ef81ee2645177fc246bbc22c5045d1fe371dd6376c07bb8585b7bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.0 MB (446031573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f241bc1054f5fef95e6cacd4c91d14a683264870d1f04045668fd4e87c4576e2`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:28 GMT
ARG version=21.0.11.10-1
# Sat, 30 May 2026 01:12:28 GMT
ARG package_version=1
# Sat, 30 May 2026 01:12:28 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:12:28 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 30 May 2026 02:12:17 GMT
CMD ["gradle"]
# Sat, 30 May 2026 02:12:17 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 30 May 2026 02:12:17 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 30 May 2026 02:12:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 30 May 2026 02:12:17 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 30 May 2026 02:12:17 GMT
WORKDIR /home/gradle
# Sat, 30 May 2026 02:12:17 GMT
ENV GRADLE_VERSION=8.14.5
# Sat, 30 May 2026 02:12:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Sat, 30 May 2026 02:12:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 30 May 2026 02:12:20 GMT
USER gradle
# Sat, 30 May 2026 02:12:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 30 May 2026 02:12:21 GMT
USER root
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6dcf128c8239e095d4cadda037b6a5b5c267ad60f46b5b8fa317ff773db55`  
		Last Modified: Sat, 30 May 2026 01:12:53 GMT  
		Size: 168.7 MB (168720905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8bec2a82af6d40239e4c7b46d2f486849c38f96771da5ba76b93d7fff0447e`  
		Last Modified: Sat, 30 May 2026 02:12:52 GMT  
		Size: 85.7 MB (85723104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61594060f6a0f2c4c7619839ae4eef1f40dece2f66bc9926cb0e89516a4fe75a`  
		Last Modified: Sat, 30 May 2026 02:12:49 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe5bb7117b54959183ff6d1bbfac85c37794083ff141768ada143c754327044`  
		Last Modified: Sat, 30 May 2026 02:12:54 GMT  
		Size: 138.1 MB (138068537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1ad04fa18fd8f4f8eeb770fc94f48d33748d81f23b07980558aecab196abe8`  
		Last Modified: Sat, 30 May 2026 02:12:49 GMT  
		Size: 59.5 KB (59521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:264c0e2c801b470681151adfc53b7d72c0ecb8e562482bd39b3cd9f2d4b5a975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11372932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a88dd41600471a716c519a407be2847569320c3c7c47721bbd3942b85160860`

```dockerfile
```

-	Layers:
	-	`sha256:ce7cfca4df522b043ec8a7ee75163e770c5b4e6ac23d7eff5f81657dd08c0474`  
		Last Modified: Sat, 30 May 2026 02:12:50 GMT  
		Size: 11.4 MB (11351737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96388487f72eb28c0913bbdea486a0aa7aff521dee1404f66315f03781a8f68b`  
		Last Modified: Sat, 30 May 2026 02:12:49 GMT  
		Size: 21.2 KB (21195 bytes)  
		MIME: application/vnd.in-toto+json
