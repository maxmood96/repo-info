## `gradle:7-jdk11-corretto`

```console
$ docker pull gradle@sha256:bee5d34dab9adcd1fd8da155c78e2db31b5f5e3ee7bc91f3bea8615b14fe64a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:b1ddeb1962364015b3b4052b5697c9fa62524fa0965b5cfc0a88800ae05afb84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.8 MB (422766336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8527f87a2b493734814dc74513f8315cefb3ab3761a5752b977568cf9cd54b30`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 May 2026 20:12:06 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:06 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:11 GMT
ARG version=11.0.31.11-1
# Fri, 22 May 2026 21:11:11 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:11:11 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 22 May 2026 22:07:11 GMT
CMD ["gradle"]
# Fri, 22 May 2026 22:07:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 May 2026 22:07:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 22 May 2026 22:07:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 22 May 2026 22:07:11 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 May 2026 22:07:11 GMT
WORKDIR /home/gradle
# Fri, 22 May 2026 22:07:11 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 22 May 2026 22:07:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 22 May 2026 22:07:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 22 May 2026 22:07:14 GMT
USER gradle
# Fri, 22 May 2026 22:07:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 22 May 2026 22:07:14 GMT
USER root
```

-	Layers:
	-	`sha256:c00ef2b893da480d77c559b6862d1ad542cc91c6bb2d3106a00cb8d9c141b797`  
		Last Modified: Fri, 15 May 2026 20:34:40 GMT  
		Size: 54.6 MB (54572440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576a116e357ee250e46eda5c05ba229716ef3641e5c2ce1d8cdc025752b9955f`  
		Last Modified: Fri, 22 May 2026 21:11:33 GMT  
		Size: 153.5 MB (153474290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb3b5cf9e551c5cd019c08c5ea75b632d43bba71a46a920fe48f44f1ca9ff7b`  
		Last Modified: Fri, 22 May 2026 22:07:44 GMT  
		Size: 86.2 MB (86193607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8a296b5d879f466728a59d2fdce0ef6dd80fd8f0cf37724cc91bb7f702e162`  
		Last Modified: Fri, 22 May 2026 22:07:40 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120a780c7ab54f12d740d3839d2bfcf817add02ba8c448685543656c837b55a9`  
		Last Modified: Fri, 22 May 2026 22:07:45 GMT  
		Size: 128.5 MB (128469420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe9d8e8d5c5584167910b5057c2eff81e13e0957cb760a045fb32d6f635ae5c`  
		Last Modified: Fri, 22 May 2026 22:07:41 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:99dafd3ddf7faae0e829c4f1ada101d558f52160f2e7913fcf3b519e3d488c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11306545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c243e3d19254b7da6146af1ce57655f26d1ad463075fef3e9e0451d9531c931f`

```dockerfile
```

-	Layers:
	-	`sha256:e672563f604b75ce8c1671997ea92ab59aa194204ea395c6a708c2aa50e4d140`  
		Last Modified: Fri, 22 May 2026 22:07:41 GMT  
		Size: 11.3 MB (11285674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:923fc4bfc94d9b28f42d3deab27c6500b7e5147ff4fdcf45c0388037c277fe00`  
		Last Modified: Fri, 22 May 2026 22:07:40 GMT  
		Size: 20.9 KB (20871 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:dc943fd407b5d365f733ff78e3d9c872d1fddb21fe80165e91966d61ae716032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.7 MB (419730591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a74ab063ccb090e5b98718126a10abcdc6a4c281c78b6428c9f580224497d5e`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 May 2026 20:12:25 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:25 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:10:48 GMT
ARG version=11.0.31.11-1
# Fri, 22 May 2026 21:10:48 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:10:48 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:10:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 22 May 2026 22:07:54 GMT
CMD ["gradle"]
# Fri, 22 May 2026 22:07:54 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 May 2026 22:07:54 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 22 May 2026 22:07:54 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 22 May 2026 22:07:54 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 May 2026 22:07:54 GMT
WORKDIR /home/gradle
# Fri, 22 May 2026 22:07:54 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 22 May 2026 22:07:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 22 May 2026 22:07:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 22 May 2026 22:07:56 GMT
USER gradle
# Fri, 22 May 2026 22:07:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 22 May 2026 22:07:57 GMT
USER root
```

-	Layers:
	-	`sha256:a92e5e4b9e90f970dfdf3c3258e673bb767c6401beba9985a3b635162466eedd`  
		Last Modified: Fri, 15 May 2026 20:34:37 GMT  
		Size: 53.5 MB (53454415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e0330030cf9dbc79176f06edbd88d18ca7a4124ad9736bc15fad2c2d57305c`  
		Last Modified: Fri, 22 May 2026 21:11:10 GMT  
		Size: 152.0 MB (152049570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432d53f222d92f8e884ef0be5ae15968d64ac4357e06680a765ca5e276a43e3e`  
		Last Modified: Fri, 22 May 2026 22:08:27 GMT  
		Size: 85.7 MB (85695980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c97d3f0ae1b31d35ee65c09fbbf9f9b2f9b035e8aaa34ffa6dd820a34083bf0`  
		Last Modified: Fri, 22 May 2026 22:08:23 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574790e36a4dace11ee9f01b45f09fd4e26365a605178fcf044a0a64f974345e`  
		Last Modified: Fri, 22 May 2026 22:08:28 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db22bc210ed812832c8555d87007e1e92f9084cafe90bab4489425c886ec8152`  
		Last Modified: Fri, 22 May 2026 22:08:24 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:243a98266186bf9f0bffd226ebdfecea399ab51148328b14ec055f102a85c850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11306537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322459a2fc1ccdb5c7fa5cbc16542c700cef91dcd7b56d062c5ed9ba55ec7f7d`

```dockerfile
```

-	Layers:
	-	`sha256:32a5175418f3ed72f49ec4510f1c09d246b5986fcc3b6d61cc1e0f633d0fdce1`  
		Last Modified: Fri, 22 May 2026 22:08:25 GMT  
		Size: 11.3 MB (11285493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0cfcad72c9c519359d8a1eda17acd16a1d3bfca5056ceaca7bd2cd2266e896`  
		Last Modified: Fri, 22 May 2026 22:08:24 GMT  
		Size: 21.0 KB (21044 bytes)  
		MIME: application/vnd.in-toto+json
