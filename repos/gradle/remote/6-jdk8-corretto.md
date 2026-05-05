## `gradle:6-jdk8-corretto`

```console
$ docker pull gradle@sha256:5fd4216ae1982e398fae4861d626545250f5b24cc8f66936f81c2c507b1d5d04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:972179194bd82e2d7fe107bfe6be783dffd241eb2d6f90bdbd8dd435d0785be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.0 MB (559025774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3caad80b291e80cd522298219964b297b87a551002be49a770a9ac229cda771`
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
# Mon, 04 May 2026 20:43:04 GMT
CMD ["gradle"]
# Mon, 04 May 2026 20:43:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 04 May 2026 20:43:04 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 04 May 2026 20:43:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 04 May 2026 20:43:04 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 04 May 2026 20:43:04 GMT
WORKDIR /home/gradle
# Mon, 04 May 2026 20:43:04 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 04 May 2026 20:43:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 04 May 2026 20:43:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 04 May 2026 20:43:06 GMT
USER gradle
# Mon, 04 May 2026 20:43:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 04 May 2026 20:43:07 GMT
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
	-	`sha256:1aedfa21abd58b35311b94693a444e6896f9d9a6bce8c5c3f3d6cb73890febb2`  
		Last Modified: Mon, 04 May 2026 20:43:45 GMT  
		Size: 65.5 MB (65506732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd02367793ec7ecb9a764ccb871360110a904b8db05d838c80d6b2323c4a97f`  
		Last Modified: Mon, 04 May 2026 20:43:42 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032a17a4fb0dd7321d08e6601f8d58231276e0dbc13397af7304c0c4ecac1761`  
		Last Modified: Mon, 04 May 2026 20:43:46 GMT  
		Size: 107.7 MB (107696662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c1d39216c724b7dd1858def1cc29de6e24f0782a00e93dccb012a0e71e08b4`  
		Last Modified: Mon, 04 May 2026 20:43:43 GMT  
		Size: 431.3 KB (431272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:13e1a822a31ad46358eed5f1cf68d5283556268002739cdfde4bbe3f5e09e93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18076514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922834ac2cd35a5bec5a980dc33f3aa15d32ef9773b963e067d5e61895201441`

```dockerfile
```

-	Layers:
	-	`sha256:d5b37b1a167d119799b4b428fed48e6918c9bf78522cac4d728c5c1fd09d3cdd`  
		Last Modified: Mon, 04 May 2026 20:43:43 GMT  
		Size: 18.1 MB (18055649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:701be449d85a949ddba927f8ce5a3b41f44c98c77b0000d7edb4c7295809b8d1`  
		Last Modified: Mon, 04 May 2026 20:43:42 GMT  
		Size: 20.9 KB (20865 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:bc2b56ac42a128bf6a91d4fad8550fc65ffd1b1fee5fa9ff4e5fe1ebea96850b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.2 MB (365182724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30942d977a467653acc91304fc4876043b79f5215cea07a8ad6c4d8eaf71745`
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
# Mon, 04 May 2026 20:42:56 GMT
CMD ["gradle"]
# Mon, 04 May 2026 20:42:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 04 May 2026 20:42:56 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 04 May 2026 20:42:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 04 May 2026 20:42:57 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 04 May 2026 20:42:57 GMT
WORKDIR /home/gradle
# Mon, 04 May 2026 20:42:57 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 04 May 2026 20:42:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 04 May 2026 20:42:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 04 May 2026 20:42:59 GMT
USER gradle
# Mon, 04 May 2026 20:42:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 04 May 2026 20:42:59 GMT
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
	-	`sha256:140c9aa74c9e931067e18b1eb35f8e2b5585a007387a75a6c03a5ab90f753e0a`  
		Last Modified: Mon, 04 May 2026 20:43:30 GMT  
		Size: 85.6 MB (85639920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72127b0ecfb2b24aa216c6dccdd7a2e9b04bd807585c31a90e5ce4ac0890ce2`  
		Last Modified: Mon, 04 May 2026 20:43:26 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8223d3520acc2ffef521fa0f9a51deb7b408551e90bd34c65f6bd3b8635412`  
		Last Modified: Mon, 04 May 2026 20:43:31 GMT  
		Size: 107.7 MB (107696661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35431a90896b100cab3c105fc790d659964cf398786156c14975897085748fdd`  
		Last Modified: Mon, 04 May 2026 20:43:26 GMT  
		Size: 425.0 KB (425024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:eda062706542e6de11a2bc56a28bc904892ab961eb1c3e1381e310651a228319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11640851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed78e85cf76cccb335a3c66f8c73fef0c83daaed2acda7e1a07015e26adf647`

```dockerfile
```

-	Layers:
	-	`sha256:e2e8c36a72f6c76e3838d4475e04b9c2a0685a7a4bead6d8d62a1e9eeb1faf53`  
		Last Modified: Mon, 04 May 2026 20:43:27 GMT  
		Size: 11.6 MB (11619813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b93b40c8ce7bf7dca0619079e763404850a00d9a718d6c33979ca7273a31ad7`  
		Last Modified: Mon, 04 May 2026 20:43:26 GMT  
		Size: 21.0 KB (21038 bytes)  
		MIME: application/vnd.in-toto+json
