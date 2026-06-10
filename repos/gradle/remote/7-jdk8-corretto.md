## `gradle:7-jdk8-corretto`

```console
$ docker pull gradle@sha256:3bd6ba6e1cd96d5053feeae9e628f6bcb1de1e5d916c6ca78cee90f27327b18f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:d7bf0307dacf32a34bac10fe192e1f59e47c634c622b8fe9a871480d8e306703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.5 MB (579518548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e408be5e4975a95602fbed3bd8537b57e1f79e9e4f4c57bedbcb89377e2f71d`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:24 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:24 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:11:11 GMT
ARG version=1.8.0_492.b09-2
# Tue, 09 Jun 2026 21:11:11 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:11:11 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:11:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 09 Jun 2026 22:06:25 GMT
CMD ["gradle"]
# Tue, 09 Jun 2026 22:06:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 09 Jun 2026 22:06:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 09 Jun 2026 22:06:26 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 09 Jun 2026 22:06:26 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 09 Jun 2026 22:06:26 GMT
WORKDIR /home/gradle
# Tue, 09 Jun 2026 22:06:26 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 09 Jun 2026 22:06:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 09 Jun 2026 22:06:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 09 Jun 2026 22:06:28 GMT
USER gradle
# Tue, 09 Jun 2026 22:06:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 09 Jun 2026 22:06:28 GMT
USER root
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c2e3cf8908eccca20edf90d28e3fee070f14d8c192deedf6386f8c0d9b165a`  
		Last Modified: Tue, 09 Jun 2026 21:12:09 GMT  
		Size: 330.8 MB (330825369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1e0fbc41e0cf34c812fac1ae50cdb4abb38a57cdc9ff8ebf87e12b8d00e2e1`  
		Last Modified: Tue, 09 Jun 2026 22:07:08 GMT  
		Size: 65.6 MB (65595744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbf2a1b782440f3cb79d5e4e7d224a441c955c7afe2b547c732f16183c7815b`  
		Last Modified: Tue, 09 Jun 2026 22:07:04 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f16c39e721bea49946ce16270481053a113e55b3b90ef70fe3d3a45e3f8b566`  
		Last Modified: Tue, 09 Jun 2026 22:07:10 GMT  
		Size: 128.5 MB (128469406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c00d62596f94126f7e7ef6b07401b3bdf8821bf42000f0cd2b30a9705854170`  
		Last Modified: Tue, 09 Jun 2026 22:07:05 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:edb72cc0425cafb66056b6ec009730d7463e7a4f139e398ec55a931cc3527c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18094423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4927bba9851c73cfc17e2bb380d6d8c7beba6429ecda74c1acfb0085b800cbcc`

```dockerfile
```

-	Layers:
	-	`sha256:8d1751d927bc31befc153a614ef990348a56c019fc884d937607fee362a997c5`  
		Last Modified: Tue, 09 Jun 2026 22:07:06 GMT  
		Size: 18.1 MB (18073559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c51a6403cbeedc4195467fd02b1102380db1019f61e65fb89784ff7c1705212`  
		Last Modified: Tue, 09 Jun 2026 22:07:04 GMT  
		Size: 20.9 KB (20864 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6716a85c6440d56e9b6794d332c23550d66424e3bcfda1c9686ab29d7b6200b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.7 MB (385661092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd831949ae26da705bd7732cc6a67ec7bc5818e01aa31d68fe45292984a40969`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:21 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:21 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:10:44 GMT
ARG version=1.8.0_492.b09-2
# Tue, 09 Jun 2026 21:10:44 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:10:44 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:10:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 09 Jun 2026 22:07:02 GMT
CMD ["gradle"]
# Tue, 09 Jun 2026 22:07:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 09 Jun 2026 22:07:02 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 09 Jun 2026 22:07:02 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 09 Jun 2026 22:07:02 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 09 Jun 2026 22:07:02 GMT
WORKDIR /home/gradle
# Tue, 09 Jun 2026 22:07:02 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 09 Jun 2026 22:07:02 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 09 Jun 2026 22:07:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 09 Jun 2026 22:07:05 GMT
USER gradle
# Tue, 09 Jun 2026 22:07:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 09 Jun 2026 22:07:05 GMT
USER root
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac744debc1aeda7f8a15a7e95c01905f3886e894cc1989142c7256e5bc4cdaca`  
		Last Modified: Tue, 09 Jun 2026 21:11:04 GMT  
		Size: 118.0 MB (117955626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8bdb434caa4778752ce1edd1e795e84b6d4803a49dc644284b0553b506d92e`  
		Last Modified: Tue, 09 Jun 2026 22:07:36 GMT  
		Size: 85.7 MB (85717014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a8bde2385d9843cc34985ba3321d2d2aa15f43d6f1ad0417a517c8e689aa09`  
		Last Modified: Tue, 09 Jun 2026 22:07:32 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0cb666ee1851589e55fd8d81e9aaf80e3bfac08bcacddecac6b4011708d459`  
		Last Modified: Tue, 09 Jun 2026 22:07:37 GMT  
		Size: 128.5 MB (128469418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34335abd8b2e5fe63016a2f30cdd420e292c12d1dee6208ba081f2c4ca61e56`  
		Last Modified: Tue, 09 Jun 2026 22:07:32 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:7cb012db08111629ffc5665a33ad0777671f3e2cc9b8a9e4e113d762dd887fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11658752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f9fe7d8696b65a088553e4a1ee7bebb9634151302bff2aef412cc2159e3739`

```dockerfile
```

-	Layers:
	-	`sha256:962b44f91ae845b5013240aef6c5343e2c0f65f767fd72ef193f35a887f62f3b`  
		Last Modified: Tue, 09 Jun 2026 22:07:33 GMT  
		Size: 11.6 MB (11637715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:028fb3de7a230d2e69a3b1fae6b75e68858fb323ed40248d35a2418164d31347`  
		Last Modified: Tue, 09 Jun 2026 22:07:32 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json
