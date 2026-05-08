## `gradle:jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:8979790113b4f9e859d93fd3e7bb3321b24434a79f67ce8b30604c1724ea0333
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:cfd399bc28ca549331fc766380270763b9cd56228bc6ffa7461d7f3149c14d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.0 MB (589021708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6ceedcc07fbce1bf9bd51571b798ee4875f248c698aefd875748bcd49bc8f2`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:42 GMT
ARG version=1.8.0_492.b09-1
# Mon, 04 May 2026 20:11:42 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:42 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 08 May 2026 17:48:49 GMT
CMD ["gradle"]
# Fri, 08 May 2026 17:48:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 17:48:49 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 08 May 2026 17:48:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 17:48:50 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 17:48:50 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 17:48:50 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 08 May 2026 17:48:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 08 May 2026 17:49:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 17:49:12 GMT
USER gradle
# Fri, 08 May 2026 17:49:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 17:49:12 GMT
USER root
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd2ff23a0524b1c7113ef94f2af3cff82ef1d7e86189b3e37a0a49a3e8a4e2c`  
		Last Modified: Mon, 04 May 2026 20:12:39 GMT  
		Size: 330.8 MB (330812379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c77b5a2dc42e0ae3b5999d498d0903c90dc47048ca22cc7b06930ea626a3909`  
		Last Modified: Fri, 08 May 2026 17:49:53 GMT  
		Size: 65.5 MB (65507160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87af335a1fd6218e2a32766a35baa84f95f82a07a96b97fd31cff9cd763083b4`  
		Last Modified: Fri, 08 May 2026 17:49:50 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f6e123524ebea73ddcee4b87e72be960afd30d6f95d5e74a44a6eef102659`  
		Last Modified: Fri, 08 May 2026 17:49:55 GMT  
		Size: 138.1 MB (138068531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f49fcd1dfadf6c5f79bac6e40a35777056842c6d20bd86074a24c7c3947ac0`  
		Last Modified: Fri, 08 May 2026 17:49:50 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:20d7313badaf32a09c8202f2c739b922c9deba93b175abba38f94c3bfbbb6aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18185183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7cac41e2005b416774730d222c6b5939afb7b29dbef4f73805ba8ab5ef6079`

```dockerfile
```

-	Layers:
	-	`sha256:81da98373ba80aa935d1d1457bc08daa76e87eba8e17699facfd28611e2da736`  
		Last Modified: Fri, 08 May 2026 17:49:51 GMT  
		Size: 18.2 MB (18163530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df4ad72dcc65c23ef3071a2eb63aa2397d772f15d05d48597aac47c4ced3fcb8`  
		Last Modified: Fri, 08 May 2026 17:49:50 GMT  
		Size: 21.7 KB (21653 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:94c9c7491daf009827bd9e0836a4b6743a8b741090adcd8bc1f08f96fdce7e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.2 MB (395189183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b93dc14cfe8776bc743df4b9d8a856fcb977744fb090e9d9e459266dd0abdc`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:02 GMT
ARG version=1.8.0_492.b09-1
# Mon, 04 May 2026 20:11:02 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:02 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 08 May 2026 17:49:15 GMT
CMD ["gradle"]
# Fri, 08 May 2026 17:49:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 17:49:15 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 08 May 2026 17:49:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 17:49:16 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 17:49:16 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 17:49:16 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 08 May 2026 17:49:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 08 May 2026 17:49:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 17:49:18 GMT
USER gradle
# Fri, 08 May 2026 17:49:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 17:49:19 GMT
USER root
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f663ff8f95b0ac33e5eeb3a57969767ad4ebbcf9ffbf6f56257306287e40928`  
		Last Modified: Mon, 04 May 2026 20:11:22 GMT  
		Size: 118.0 MB (117962667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325615d1e9abc87d3dda9801c3817868ebaf64205d5c04922af9f96882e86497`  
		Last Modified: Fri, 08 May 2026 17:49:51 GMT  
		Size: 85.6 MB (85640000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02d3117b3de63555bb37bcf51fceb7d39f077a2fb4ae876bd58101b7078ffde`  
		Last Modified: Fri, 08 May 2026 17:49:46 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6edb5a3d72e74caa7613fe40823a486d67e776bb03307518e3a066c37bbb05`  
		Last Modified: Fri, 08 May 2026 17:49:52 GMT  
		Size: 138.1 MB (138068532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6157db0f6648885b3dff6e79599dcb6b1eafbef00a80cbce47b61b36a6f3ebdc`  
		Last Modified: Fri, 08 May 2026 17:49:47 GMT  
		Size: 59.5 KB (59536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:1851ceef8998eb50490a05b68c98618f22832986dc42cb59dd82165a65422c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11749569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff92974e7010677cc65d01fc6245f38bf2a56246129deb569f5dcb43a925d70`

```dockerfile
```

-	Layers:
	-	`sha256:ca97f5436b6544bbd61206e3947ecbd45921dab9c3bd01431f296d515cc02ed2`  
		Last Modified: Fri, 08 May 2026 17:49:47 GMT  
		Size: 11.7 MB (11727718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c9d446f2d0b0f4e7d0e789a51984dbd50df58f304342a490fd342bba6dedcb`  
		Last Modified: Fri, 08 May 2026 17:49:46 GMT  
		Size: 21.9 KB (21851 bytes)  
		MIME: application/vnd.in-toto+json
