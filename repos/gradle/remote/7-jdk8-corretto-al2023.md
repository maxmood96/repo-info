## `gradle:7-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:052d097c9838c4934634b797b4066883f457ebda8f794db5ac44f7fd5a26f542
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:ac7af02895ca6a34e5a47a512af7dc115d6ffec99444a42c59dad9eba9a12b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.4 MB (578374327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740baf5d4b74c89dbb0c26abeb46be05ad662234f5cba9d64f6271388824937a`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:25 GMT
ARG version=1.8.0_472.b08-1
# Fri, 31 Oct 2025 00:11:25 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:11:25 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 31 Oct 2025 01:12:33 GMT
CMD ["gradle"]
# Fri, 31 Oct 2025 01:12:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 31 Oct 2025 01:12:33 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 31 Oct 2025 01:12:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 31 Oct 2025 01:12:33 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 31 Oct 2025 01:12:33 GMT
WORKDIR /home/gradle
# Fri, 31 Oct 2025 01:12:33 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 31 Oct 2025 01:12:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 31 Oct 2025 01:12:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 31 Oct 2025 01:12:36 GMT
USER gradle
# Fri, 31 Oct 2025 01:12:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 31 Oct 2025 01:12:36 GMT
USER root
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d90a02718a2ec471735b22a7012a63f3b6fd6aa7b11464ff1edf280a2e204b8`  
		Last Modified: Fri, 31 Oct 2025 01:12:00 GMT  
		Size: 330.9 MB (330868176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33aab67b89b5d8fa23252372d76a3f28bf11e568fc63029d00cdb045766c7dd8`  
		Last Modified: Fri, 31 Oct 2025 01:13:27 GMT  
		Size: 65.0 MB (64978603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bea58504799fcf17f46652d83dcd1bdc1c36a68ef0682674211c843cf8f09d`  
		Last Modified: Fri, 31 Oct 2025 01:13:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1d4cbc1952c491bcd9bbfdbbae6983cf72ac2a8d17b7865bbddf7192f990de`  
		Last Modified: Fri, 31 Oct 2025 05:51:13 GMT  
		Size: 128.5 MB (128469441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0052b5b547df6f4ccceba362dacb966e4d455f968fe137bc87815e4c92977836`  
		Last Modified: Fri, 31 Oct 2025 01:13:21 GMT  
		Size: 54.9 KB (54895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:4770bb85794aba8230c7dbbf6a3d358c8ec80610b1cebcd4225319fcbcc91c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18063334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16eed7a171440c491e5d52fd03705291734ecbdcb605140af7224a9eadacef5c`

```dockerfile
```

-	Layers:
	-	`sha256:f9cc419c25c8e71c8216cb6ab280ef3d0f31546e3da63a0c6924c8649441f8d2`  
		Last Modified: Fri, 31 Oct 2025 02:19:05 GMT  
		Size: 18.0 MB (18042470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1313ede95d5a98f87bef66b24a75c1f6e6ad23afdc6260ebb27892020f62d4a`  
		Last Modified: Fri, 31 Oct 2025 02:19:06 GMT  
		Size: 20.9 KB (20864 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c05c50a2e6050b7d156e475583a4f6be6a790acaa61d0306daf9a8781639f0ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384544810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921d7de3b91d118aa319516b87de7371ace1f308a2b3a0c375b91954890d7ea5`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:43 GMT
ARG version=1.8.0_472.b08-1
# Fri, 31 Oct 2025 00:11:43 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:11:43 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 31 Oct 2025 01:12:50 GMT
CMD ["gradle"]
# Fri, 31 Oct 2025 01:12:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 31 Oct 2025 01:12:50 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 31 Oct 2025 01:12:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 31 Oct 2025 01:12:50 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 31 Oct 2025 01:12:50 GMT
WORKDIR /home/gradle
# Fri, 31 Oct 2025 01:12:50 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 31 Oct 2025 01:12:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 31 Oct 2025 01:12:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 31 Oct 2025 01:12:53 GMT
USER gradle
# Fri, 31 Oct 2025 01:12:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 31 Oct 2025 01:12:53 GMT
USER root
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d388cefb5877034eb46c74035ba24455c55fff50dbbe8d7c47526c4022768c`  
		Last Modified: Fri, 31 Oct 2025 01:12:01 GMT  
		Size: 118.0 MB (117956928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c20230ac0f11c5043e45be8ad4f306c63a929e41078a4c556099559309d387`  
		Last Modified: Fri, 31 Oct 2025 01:13:38 GMT  
		Size: 85.2 MB (85155391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291ceca803a73b8a56eab8a7895feb929b2dd09b8a24769de108e76eed211bed`  
		Last Modified: Fri, 31 Oct 2025 01:13:31 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e575ed2d6ba4bc378c39043cf5c575b81d9733f245d10b15c4dc93e39bd1d8`  
		Last Modified: Fri, 31 Oct 2025 13:44:23 GMT  
		Size: 128.5 MB (128469441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f096f7d2c09676999778d7d3ad60672d43f0377ef7808b506b724fa5409ece`  
		Last Modified: Fri, 31 Oct 2025 01:13:31 GMT  
		Size: 59.5 KB (59520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:2cdac513f92dfc959a73fe84ec586f7c11fc1161b98508b99409ac3fe9643cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11627669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ae4924642b03b2ebf71d2bd114080d5a4722985f32d42d2e59a07acfc05b43`

```dockerfile
```

-	Layers:
	-	`sha256:8668179ea9736b8476bb9ded0577f44dc783450a5c4e524655d4d0cc83318132`  
		Last Modified: Fri, 31 Oct 2025 02:19:22 GMT  
		Size: 11.6 MB (11606632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b2001e3f2f44bf825c2f1c400b7e710a1d8f158e062eb6727dc5715b4255577`  
		Last Modified: Fri, 31 Oct 2025 02:19:22 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json
