## `gradle:jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:34fac33306f9bcb4af5370db7343d868157f568ac8606238c98bbc9f50d93e07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:bff3ebeeb25d8506fbd6756f7cd83394d1e702d45529f328b0e1fcb2c6e046ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.3 MB (438257153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:566a000a1c795bc65e2d270cd23113775d6b3f57adbfb7fed114fd737b3623fe`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:15 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:15 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:15:28 GMT
ARG version=17.0.19.10-1
# Tue, 16 Jun 2026 01:15:28 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:15:28 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:15:28 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:15:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 16 Jun 2026 02:19:29 GMT
CMD ["gradle"]
# Tue, 16 Jun 2026 02:19:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 16 Jun 2026 02:19:29 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 16 Jun 2026 02:19:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 16 Jun 2026 02:19:29 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 16 Jun 2026 02:19:29 GMT
WORKDIR /home/gradle
# Tue, 16 Jun 2026 02:19:29 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 16 Jun 2026 02:19:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 16 Jun 2026 02:19:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 16 Jun 2026 02:19:32 GMT
USER gradle
# Tue, 16 Jun 2026 02:19:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 16 Jun 2026 02:19:32 GMT
USER root
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cbe16b91281bbab0f677616f852468a1efb463957ba2554f568b2f9ac583b3`  
		Last Modified: Tue, 16 Jun 2026 01:15:51 GMT  
		Size: 157.2 MB (157156724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ff457917a5e5a8695600c6a66dc982e3fe27b5b98a89a46e4bd746a996b7c9`  
		Last Modified: Tue, 16 Jun 2026 02:20:01 GMT  
		Size: 86.3 MB (86265000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475145b646c176d97385fd86e9f810c488208b8bbdb2ec2cadcb84cd54f90c74`  
		Last Modified: Tue, 16 Jun 2026 02:19:57 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab487ba60ff3754887e4aec333b9f0fd5e8d4ba0a0ae9ff04e383edf8cd21b2`  
		Last Modified: Tue, 16 Jun 2026 02:20:02 GMT  
		Size: 140.2 MB (140236985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e9c5b8cbf168babd540f8145bf83e9e499b8be4e6b669a47df99bcaea983dc`  
		Last Modified: Tue, 16 Jun 2026 02:19:57 GMT  
		Size: 25.6 KB (25607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:33a0d7bd2ea89733924a3cd2cb7f6377cd53c7370324bf3412e0bb11590b6fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d307f5e38cecac563ec49c61d7a4985cb2b01fefa5ec019f55a3e47d8a2e23c9`

```dockerfile
```

-	Layers:
	-	`sha256:d73c8d9d66a8b857f5c012feb48d53a75fc9ab97f5e2b667fa604f02a05f392c`  
		Last Modified: Tue, 16 Jun 2026 02:19:58 GMT  
		Size: 11.4 MB (11365662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2220f816dc4b99f2fc1251e0a18caea5d4d52b9a75d837f99af112a2fae4a2f`  
		Last Modified: Tue, 16 Jun 2026 02:19:57 GMT  
		Size: 21.5 KB (21495 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a6275727e5e5a71c291996f8b7cfedd65b56c8da2c8f238ec8caa8d1cf174987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.4 MB (435435340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eac9e03fe8a8434d730d573b8f6a5493b3e62959d5784559be3a3d4f3a462f`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:26 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:16:35 GMT
ARG version=17.0.19.10-1
# Tue, 16 Jun 2026 01:16:35 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:16:35 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:16:35 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:16:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 16 Jun 2026 02:20:14 GMT
CMD ["gradle"]
# Tue, 16 Jun 2026 02:20:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 16 Jun 2026 02:20:14 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 16 Jun 2026 02:20:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 16 Jun 2026 02:20:14 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 16 Jun 2026 02:20:15 GMT
WORKDIR /home/gradle
# Tue, 16 Jun 2026 02:20:15 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 16 Jun 2026 02:20:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 16 Jun 2026 02:20:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 16 Jun 2026 02:20:17 GMT
USER gradle
# Tue, 16 Jun 2026 02:20:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 16 Jun 2026 02:20:18 GMT
USER root
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25f04afa63e84df40811c8b1eb43c711fcfea0a157148dfba69328e8dc1769f`  
		Last Modified: Tue, 16 Jun 2026 01:16:57 GMT  
		Size: 156.0 MB (155987128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cff3dc768ce7ba4169220da641a83b41c44f19f18cafe43dfe43d3a8240ecd`  
		Last Modified: Tue, 16 Jun 2026 02:20:50 GMT  
		Size: 85.7 MB (85722383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987526e52fc39deb9a467998bfcea201dba127d445827942631fc22a893b32f1`  
		Last Modified: Tue, 16 Jun 2026 02:20:46 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1720fb36dc3d09e4c8825e218e8405fddc2d7899160b6049577df6e7eeddc84e`  
		Last Modified: Tue, 16 Jun 2026 02:20:52 GMT  
		Size: 140.2 MB (140236984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a5562c043bdc4113f5c192e488179f26e84103bc728815d9d4226171ff7a74`  
		Last Modified: Tue, 16 Jun 2026 02:20:46 GMT  
		Size: 29.3 KB (29337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:4cccf3cce46eaf867ac0f096411961d2ed59a88d0d6c8fb70c6e471cda7223ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11386356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f22ddc9ba028b31397c383f35ef20a56bc273718713fa6e36a605693cf0ac4`

```dockerfile
```

-	Layers:
	-	`sha256:e5ad4a95863a82a942a63a22bf55bb873e6427aa38098045828585d9d4a59e4f`  
		Last Modified: Tue, 16 Jun 2026 02:20:47 GMT  
		Size: 11.4 MB (11364662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1144b53981aeb5da6c45f9d28cc14d4b68322ec9bff5e3a4a05f6d626c06450`  
		Last Modified: Tue, 16 Jun 2026 02:20:46 GMT  
		Size: 21.7 KB (21694 bytes)  
		MIME: application/vnd.in-toto+json
