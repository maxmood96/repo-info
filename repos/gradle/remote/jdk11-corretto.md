## `gradle:jdk11-corretto`

```console
$ docker pull gradle@sha256:a5d335cb4e0b8e0d12b7d4ec35d6ee667601811d724992ad230c4b4a4e1bed39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:e5590b047f2d2a5b383307b9b6e6e2f4a3feceb757e2e3d42cf59b157ed3e214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430909721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255583b19b837cc76e5f5d29d0c0f39fe4b67ce11628e1f6cbe1801470779dbe`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
ARG version=11.0.28.6-1
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=C.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER gradle
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER root
```

-	Layers:
	-	`sha256:b9bd06b1e98f2884554d02055b944634294fa4d6f341ec4d0d7349c492676b31`  
		Last Modified: Sat, 09 Aug 2025 04:12:21 GMT  
		Size: 53.8 MB (53837959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec828ce5d2d44eda954aac728695e0e891c8a7cd07cc61c3e2be05880101eaf`  
		Last Modified: Wed, 13 Aug 2025 23:11:17 GMT  
		Size: 154.1 MB (154063982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4842e5460a5ee0509527a2fe9c6c724f957a0fb2c1837564fbb8b8398f8fa2`  
		Last Modified: Thu, 14 Aug 2025 03:20:53 GMT  
		Size: 85.6 MB (85556003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3705f01f3ed7450cd8a0bd438897543cac80c2b1522ed15efdc91a1f4a3fcc`  
		Last Modified: Wed, 13 Aug 2025 23:19:51 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066ccb23e5b43a65aa3081a7d7597bb6727d98a17055f1e70e59f15c43d04e6e`  
		Last Modified: Thu, 14 Aug 2025 06:51:23 GMT  
		Size: 137.4 MB (137395199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b789667a59aadccae6f5f0fc0d3aa310f0ca2e1c9e1d33a01fc68713204015b`  
		Last Modified: Wed, 13 Aug 2025 23:19:56 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:707657bc4b76b296aa82b3d82f1e8879a443dba2fb1bad71255308d2a04489e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11359230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdd814fefceb34ebffe5a7c002620942eb8114a08bacbfddcc97b6ccf939737`

```dockerfile
```

-	Layers:
	-	`sha256:1f45525030a4a3401a9723312d2c4051e01f4e8ab8f176f4155493f888ac77ac`  
		Last Modified: Thu, 14 Aug 2025 02:20:55 GMT  
		Size: 11.3 MB (11337649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d9645c177112924a1ed2e670e0bccf6ddf8ed64aca3d7f60954136da1595d69`  
		Last Modified: Thu, 14 Aug 2025 02:20:56 GMT  
		Size: 21.6 KB (21581 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e50562fd3379f167cb2b5c51cc5af3d42373ec85c4bcf023b9944b24aecd6a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.8 MB (427828430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6616d56fc19637c237acc54f7fcfcd999498b5baddfc11b709036c5ff29ea63a`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
ARG version=11.0.28.6-1
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=C.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER gradle
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER root
```

-	Layers:
	-	`sha256:93b5cbbc86ee614f8432762e1f7f34b6cc9d6d4b95867cf25bca6ae179f49439`  
		Last Modified: Sat, 09 Aug 2025 04:12:37 GMT  
		Size: 52.7 MB (52726394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20183faf628bb3bf8416e2bff502cb48f4f73fb58cc8166653501de1e32f063`  
		Last Modified: Thu, 14 Aug 2025 11:54:11 GMT  
		Size: 152.6 MB (152569365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811b3d7ea8a7405ca7784141ff239fe8e1f2b4168bfcfeff0ce785e2679f4ef9`  
		Last Modified: Thu, 14 Aug 2025 11:25:57 GMT  
		Size: 85.1 MB (85076328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c03269481c820847a85cd3728cbaa14b6d2568eb0bd170f3bf5ac3731a186d2`  
		Last Modified: Thu, 14 Aug 2025 11:59:40 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a593cca480b335d0efd0653db6897100ed82f8be6217cfb6127ebd5405329a`  
		Last Modified: Thu, 14 Aug 2025 11:25:59 GMT  
		Size: 137.4 MB (137395130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42822d3c830d5c5425d94876617ae8ef5e0ebf23e7b2b7ff20ff86c65c81fe83`  
		Last Modified: Thu, 14 Aug 2025 11:59:39 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:bb5864217e902f8c305ba5b422ed1bcad694bd00dc1d2159d0d21dc9253da60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11359271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6152abd2cfc9ad072687596a0129a6b9eef7310fab76b87a9e711a95f8c14f4a`

```dockerfile
```

-	Layers:
	-	`sha256:86e924d39a35caa3e5bd9736e7b1b8b33c8dae38f8425cfdc467b04489d222ff`  
		Last Modified: Thu, 14 Aug 2025 14:20:36 GMT  
		Size: 11.3 MB (11337492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c7ae2d3fb3aada50e3da2b4b0ce713d741c4ccf0cd17e74fca01525dce8ddbd`  
		Last Modified: Thu, 14 Aug 2025 14:20:37 GMT  
		Size: 21.8 KB (21779 bytes)  
		MIME: application/vnd.in-toto+json
