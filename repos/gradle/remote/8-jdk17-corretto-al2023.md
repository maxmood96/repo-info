## `gradle:8-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:1903edb2b7b5d7120b86d0af5a72456ba61b01862a41f7cf74567d32659ba5a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:11ba5b0496bfce2dc4c83f326eb26c6a10589c5ec318884c4ba393b61200b3c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.6 MB (433637018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fcf2710025f87221628cd07a9d0ac6d900568ef694f4691c97b9b3c9604258d`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
ARG version=17.0.16.8-1
# Thu, 17 Jul 2025 03:50:10 GMT
ARG package_version=1
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=C.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
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
	-	`sha256:7053c3dfee684fe542e0df754b07934a8c7d985befc94dfa121e0569a8c2f94f`  
		Last Modified: Wed, 13 Aug 2025 23:11:14 GMT  
		Size: 156.8 MB (156794651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888743d78a1ad79667bcea376f7bc9df972e1b17600b24a4df4add3eb015e73c`  
		Last Modified: Thu, 14 Aug 2025 06:53:29 GMT  
		Size: 85.6 MB (85552649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbec9d89d161c772d0bb305a43b98a889c3535158e1a9032ae728f117b8f197`  
		Last Modified: Wed, 13 Aug 2025 23:12:34 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f261f18697e4299c837cf3d8912d0776a6eea6c60d57898d65092cf915d3c205`  
		Last Modified: Thu, 14 Aug 2025 02:55:46 GMT  
		Size: 137.4 MB (137395195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9f8a969ba1add8a0c0675cac1e1362da370c8fb0ba4577c6802fe2eada5582`  
		Last Modified: Wed, 13 Aug 2025 23:12:34 GMT  
		Size: 54.9 KB (54887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:a6a196cebccc2bfd0de645156903b3e4938a428eb8b5b4fec0e93de5ff297630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11332283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9b43c92037ef51a3e0bbb4aa498fe82a6efe101e482a5e5017e6f7f9f92907`

```dockerfile
```

-	Layers:
	-	`sha256:7c3425d6dcd66b02e8530f31c56815b8fa8fa97b6c7a90c0105176691cde8069`  
		Last Modified: Thu, 14 Aug 2025 02:21:11 GMT  
		Size: 11.3 MB (11311497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e675ef9d014fbc6a165efa077b5e7d04d341c4fb5ea7c58055d47aae200dacfe`  
		Last Modified: Thu, 14 Aug 2025 02:21:12 GMT  
		Size: 20.8 KB (20786 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:5054dd118621f8027cc90ca5a21f4f0adb7ddbc9a0f27718253b45145f1a3bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.8 MB (430842796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5f1ab94a8adb90bd8b806ec315d6c5248233c2ec3a436e202dd1fe1376a71c`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
ARG version=17.0.16.8-1
# Thu, 17 Jul 2025 03:50:10 GMT
ARG package_version=1
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=C.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
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
	-	`sha256:35ac9d907769c48e7b17f0e81b67567f13bdab1cc081d367ece33201a9dfaf94`  
		Last Modified: Thu, 14 Aug 2025 09:48:41 GMT  
		Size: 155.6 MB (155582881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c12dd44c28b5d21fbc6703e01f515dea0095956d6ae6fc19b03052f7daa22c`  
		Last Modified: Thu, 14 Aug 2025 18:33:55 GMT  
		Size: 85.1 MB (85077116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a752d92b62186f3f6e7c2e37b37eb90b8a9e77f1ec215d496893b32d393d80`  
		Last Modified: Thu, 14 Aug 2025 12:08:17 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffdc2680e9e94f54fbea244efcc674f7f9db05b7d693205fd102bd9a9345182`  
		Last Modified: Thu, 14 Aug 2025 18:34:01 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40232eeea3c0deffe0981a7f18b6fe3f72198416ba6f0174cbd679a91c07c979`  
		Last Modified: Thu, 14 Aug 2025 11:25:16 GMT  
		Size: 59.5 KB (59531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:8163d1a4c1a898d91f41a39b806113c64c89eeeecadd9fdb952488a0d6df7a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11331431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436477319f4e108de536b2e7a7bea562d995818f18ddacebbe3bc7d60baf4582`

```dockerfile
```

-	Layers:
	-	`sha256:3e2295cb2872c5268b4bcfac6b474660f538ed3d5ed43944160a064daaaf5f2c`  
		Last Modified: Thu, 14 Aug 2025 14:20:53 GMT  
		Size: 11.3 MB (11310472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:353e6e91d5965b703692da9e2f079aa511f9a58986ee5e24bea28054c0888715`  
		Last Modified: Thu, 14 Aug 2025 14:20:55 GMT  
		Size: 21.0 KB (20959 bytes)  
		MIME: application/vnd.in-toto+json
