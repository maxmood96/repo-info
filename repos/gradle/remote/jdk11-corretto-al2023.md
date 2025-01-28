## `gradle:jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:64b65b569aac6f14ccd7a8bceb95e1a9f4c8597f2989bc0ac53f295425317929
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:33d25f648c87d97f313c07b602c76394054d0a0e1ac776d5525808de932525a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.3 MB (414317784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c828667895840497bfeb7e635da66fa33f447088566b306448e96f0a39d1467`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:40 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=11.0.26.4-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 27 Jan 2025 19:22:41 GMT
CMD ["gradle"]
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 27 Jan 2025 19:22:41 GMT
WORKDIR /home/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_VERSION=8.12.1
# Mon, 27 Jan 2025 19:22:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Mon, 27 Jan 2025 19:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
USER gradle
# Mon, 27 Jan 2025 19:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
USER root
```

-	Layers:
	-	`sha256:fa97b7596fdd91f8ccf1ccf8ee7189f9449877cc795e39ad814638444b666c80`  
		Last Modified: Fri, 17 Jan 2025 02:00:45 GMT  
		Size: 53.2 MB (53152535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8adfade431f4ceecf5e37a3552e317d176c76d5e7b8e57017211557db5ba362`  
		Last Modified: Thu, 23 Jan 2025 23:08:09 GMT  
		Size: 153.9 MB (153883276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae24d41a9635de4034fa851933b4e4446cfe66c2e81419a1ff0664f4e228b2c`  
		Last Modified: Tue, 28 Jan 2025 01:28:50 GMT  
		Size: 70.7 MB (70663450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f9f2f870e32a15581b80c6a1eb19e5720b8f01616e4102bdea38ad04ddf46c`  
		Last Modified: Tue, 28 Jan 2025 01:28:49 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df31cc9c681d99e2daebbea1863c36cef4fc65fd4d762ed89661dabae7cc592`  
		Last Modified: Tue, 28 Jan 2025 01:28:51 GMT  
		Size: 136.6 MB (136561941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edc53fb2a46baa419cccb48856a14f9f70689ca543835859862a15feb3755eb`  
		Last Modified: Tue, 28 Jan 2025 01:28:49 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:179ea00c576252463f3cbb574fa9a491792554c123d1e876d1eef5390de9abf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10763883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af96b12ed55fda9185f6fb8911b855df8c3570f49ea048a276f1f3de5a664c96`

```dockerfile
```

-	Layers:
	-	`sha256:92543a2470f330c2fafce283ba7b0b4e069c46dc5264ceed16b30b20645fa613`  
		Last Modified: Tue, 28 Jan 2025 01:28:49 GMT  
		Size: 10.7 MB (10743974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:399fd87f0b6c1b99db7566393072cf16ef32136bba7173cffe78faf27aeac0cc`  
		Last Modified: Tue, 28 Jan 2025 01:28:49 GMT  
		Size: 19.9 KB (19909 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:41fb012e0bffd5d1eb96968884846fe971d4e2f8ae097a34e056b1a6ca5999b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.6 MB (411626155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e800a09baea3994e75fb6b424446966c6873a2646d5d446e8e36c8a51df7c37`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:44 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:44 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=11.0.26.4-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 27 Jan 2025 19:22:41 GMT
CMD ["gradle"]
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 27 Jan 2025 19:22:41 GMT
WORKDIR /home/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_VERSION=8.12.1
# Mon, 27 Jan 2025 19:22:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Mon, 27 Jan 2025 19:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
USER gradle
# Mon, 27 Jan 2025 19:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
USER root
```

-	Layers:
	-	`sha256:23c58bc83b4b2c70780808282eab12c25cdbe212cc6fa4cd0d9a4d82b1cbf7ce`  
		Last Modified: Fri, 17 Jan 2025 02:10:39 GMT  
		Size: 52.3 MB (52270199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41040c42d483e286e764c6fc046959b40e374d0a17723f788d6f9a48b7c957a7`  
		Last Modified: Thu, 23 Jan 2025 23:12:00 GMT  
		Size: 152.4 MB (152375466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0010fc71c9de033dc0a0417c2bd2c505b8f5c40ccc352214ab528e3f077495`  
		Last Modified: Fri, 24 Jan 2025 00:09:41 GMT  
		Size: 70.4 MB (70357339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158df7895bdc254e5632488e6ba977e3bab367b6595f945f9c56077d936a543c`  
		Last Modified: Fri, 24 Jan 2025 00:09:39 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3632fa093a79128855c08ba5e5ba111c445e06aed03d69b2552474e46893444b`  
		Last Modified: Tue, 28 Jan 2025 01:57:27 GMT  
		Size: 136.6 MB (136561940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598fd64e55d43e5e7c042e2ab02a0be9a41319734e764fdab7f0d8b1db4a20ea`  
		Last Modified: Tue, 28 Jan 2025 01:57:22 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:0f8b530faddea4164da623cc1cc298eb0c476a952d4c02b939525299e02a4e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10763923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9501314af6f90b6b57e5061ac483653c898be759be64a70f59e2ffb0f6ff5f44`

```dockerfile
```

-	Layers:
	-	`sha256:ed8dc1371dd9e5b06dbb5be7a684e783d6eb27ad2c28191f4a09b992e1009506`  
		Last Modified: Tue, 28 Jan 2025 01:57:22 GMT  
		Size: 10.7 MB (10743817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35953e121e79be6eb26666b9ba81634501eba18ad57f05a5ad49fff153a94ce8`  
		Last Modified: Tue, 28 Jan 2025 01:57:22 GMT  
		Size: 20.1 KB (20106 bytes)  
		MIME: application/vnd.in-toto+json
