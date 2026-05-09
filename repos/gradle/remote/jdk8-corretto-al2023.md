## `gradle:jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:a60164c4a00df322c48e49908e6cfe9391b7bb97a934771f2430599b215d51ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:a1f9fa8b78cf862d64bd9cde61deca2cedb154ea56c352c27bf2e2bb19a7b166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.0 MB (589028903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f457e3a2bb0068a003d63800fca046f7fbb0d86e7bf4a50ece57a184b65d6120`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:14:56 GMT
ARG version=1.8.0_492.b09-2
# Sat, 09 May 2026 00:14:56 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:14:56 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:14:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sat, 09 May 2026 01:21:25 GMT
CMD ["gradle"]
# Sat, 09 May 2026 01:21:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 09 May 2026 01:21:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 09 May 2026 01:21:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 09 May 2026 01:21:25 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 09 May 2026 01:21:25 GMT
WORKDIR /home/gradle
# Sat, 09 May 2026 01:21:25 GMT
ENV GRADLE_VERSION=8.14.5
# Sat, 09 May 2026 01:21:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Sat, 09 May 2026 01:21:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 09 May 2026 01:21:28 GMT
USER gradle
# Sat, 09 May 2026 01:21:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 09 May 2026 01:21:28 GMT
USER root
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd2295c4476393f62916a766a1b4539c0fd524867201f0dcdd4ba2a80ded9a4`  
		Last Modified: Sat, 09 May 2026 00:15:51 GMT  
		Size: 330.8 MB (330819579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476ed5d1c670367fdb9eef45fadffe5843b1191a498fbc6011fc9b44de3e978`  
		Last Modified: Sat, 09 May 2026 01:22:13 GMT  
		Size: 65.5 MB (65507093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7d6c353036f61890e9215273aaef36e2b196d8e25a27e3608d87be425e43ec`  
		Last Modified: Sat, 09 May 2026 01:22:10 GMT  
		Size: 1.9 KB (1942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55880d5a50fd5bdb7566f02f71070ff65b7d0106e9ce6920a08f5f20d720315a`  
		Last Modified: Sat, 09 May 2026 01:22:14 GMT  
		Size: 138.1 MB (138068546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578861bcc7267ca7b9cc29ba5f0de973446be3a0a46b23cbb1107ade56be1bab`  
		Last Modified: Sat, 09 May 2026 01:22:10 GMT  
		Size: 54.9 KB (54907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:a8e41079343a5cd214e519e0b97a2cd3ce496ce3f789fb42d83b230b4155ea2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18185184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d1b50057b828a91799a8e96d6a42ce78142ba5d124737866356058e966a71d`

```dockerfile
```

-	Layers:
	-	`sha256:2d1e7c9aad4bb514655e2d609d793fb711ba65ae10037e74bdaa82afd2afa016`  
		Last Modified: Sat, 09 May 2026 01:22:11 GMT  
		Size: 18.2 MB (18163530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:699f35b4bcfd41fbf3776f977dc589b12e28a01d715f9ce203217e6654b209ce`  
		Last Modified: Sat, 09 May 2026 01:22:10 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:0b11c933c66ba428b968e910f45c4a0146d32233d3043948b71411fa6ff997be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.2 MB (395179841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1133bb25281fb651dc0ecb284d21a1838c21d9106fff2620a1e4b9e57e25271f`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:14:49 GMT
ARG version=1.8.0_492.b09-2
# Sat, 09 May 2026 00:14:49 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:14:49 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:14:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sat, 09 May 2026 01:46:37 GMT
CMD ["gradle"]
# Sat, 09 May 2026 01:46:37 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 09 May 2026 01:46:37 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 09 May 2026 01:46:37 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 09 May 2026 01:46:37 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 09 May 2026 01:46:37 GMT
WORKDIR /home/gradle
# Sat, 09 May 2026 01:46:37 GMT
ENV GRADLE_VERSION=8.14.5
# Sat, 09 May 2026 01:46:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Sat, 09 May 2026 01:46:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 09 May 2026 01:46:40 GMT
USER gradle
# Sat, 09 May 2026 01:46:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 09 May 2026 01:46:40 GMT
USER root
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f381327a354601594ad8bb3da3fa9f604c4e3d4d563f43a2f619ab5ef4c74655`  
		Last Modified: Sat, 09 May 2026 00:15:09 GMT  
		Size: 118.0 MB (117953507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2506b902c3826a984033a6c0245443ca7331cc05f87a942f7b24001ca05630f8`  
		Last Modified: Sat, 09 May 2026 01:47:15 GMT  
		Size: 85.6 MB (85639592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c554423c7060eb9d012f94a5c0c546d70e588191882be17e88edee13b1dfbd`  
		Last Modified: Sat, 09 May 2026 01:47:11 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85daf460bb0689e63ffc20a0d777ddc64ba55a8fb1e0b8d618dffe8b94028a3a`  
		Last Modified: Sat, 09 May 2026 01:47:16 GMT  
		Size: 138.1 MB (138068563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94176e7a5ca23cbfcbd201919eec2dc29dd7ba18b00199ccb27c0acb8595c3bc`  
		Last Modified: Sat, 09 May 2026 01:47:12 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:1c4b382191a8931751183b7e370f19ce1da6a02dfecf7c47baa7209f6c5822cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11749569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555b98149e3ba2ee498730a4a8685ac05be5831aa66a91574f0028875c279bdd`

```dockerfile
```

-	Layers:
	-	`sha256:532c2c1881551a1355ab1c6566ab05c210f189e5074b815928c1bfc7c6397cd1`  
		Last Modified: Sat, 09 May 2026 01:47:12 GMT  
		Size: 11.7 MB (11727718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:071464ba144866de8439ee0d8c6d39a5467b4f775775271b3b4a6a438bc63622`  
		Last Modified: Sat, 09 May 2026 01:47:11 GMT  
		Size: 21.9 KB (21851 bytes)  
		MIME: application/vnd.in-toto+json
