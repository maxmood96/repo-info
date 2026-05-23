## `gradle:6-jdk8-corretto`

```console
$ docker pull gradle@sha256:ff6d86752ea2fc21c28d3950ecbae859f80364eae53585e5d197d8bf965c6ed6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:8c4c0baecc32040e2012a0f4356f2998dc325f3eab872aca3a693db1d4f7ad20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.1 MB (559063966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e5887574c6fbf0d5831da21ff0b3530e2ab5d99f8726a74f46ba01902e68f7`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 May 2026 20:12:06 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:06 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:23 GMT
ARG version=1.8.0_492.b09-2
# Fri, 22 May 2026 21:11:23 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:11:23 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 22 May 2026 22:07:39 GMT
CMD ["gradle"]
# Fri, 22 May 2026 22:07:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 May 2026 22:07:39 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 22 May 2026 22:07:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 22 May 2026 22:07:40 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 May 2026 22:07:40 GMT
WORKDIR /home/gradle
# Fri, 22 May 2026 22:07:40 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 22 May 2026 22:07:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 22 May 2026 22:07:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 22 May 2026 22:07:42 GMT
USER gradle
# Fri, 22 May 2026 22:07:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 22 May 2026 22:07:42 GMT
USER root
```

-	Layers:
	-	`sha256:c00ef2b893da480d77c559b6862d1ad542cc91c6bb2d3106a00cb8d9c141b797`  
		Last Modified: Fri, 15 May 2026 20:34:40 GMT  
		Size: 54.6 MB (54572440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e164628c07dac6b95a1129a4b9c10a619e5f4780ebd7b5aa462019fee2bd9a`  
		Last Modified: Fri, 22 May 2026 21:12:19 GMT  
		Size: 330.8 MB (330821282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e36f393496d71863f8fbbf4a824fa229dfd3ff2d182a066c2f3d5b93628e79`  
		Last Modified: Fri, 22 May 2026 22:08:21 GMT  
		Size: 65.5 MB (65540338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189d2e46a10e12aca59fdc4a647ce6ed50dfced17d847b304a4dce21404d4c8e`  
		Last Modified: Fri, 22 May 2026 22:08:18 GMT  
		Size: 1.9 KB (1942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4d1c388d0191f8730cbe719b0d68d84e2645dfa61417bd2bafe8a3cc421f69`  
		Last Modified: Fri, 22 May 2026 22:08:22 GMT  
		Size: 107.7 MB (107696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a652b193f1e1f6a10a85794af9ad28e09392baf3a653c529400e3a35c8b1c4`  
		Last Modified: Fri, 22 May 2026 22:08:18 GMT  
		Size: 431.3 KB (431269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:77e3960b3e2f35713391baea1ca11f3196bfbc6c0c606f2eb8ee4f39bab3f7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18076522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c63eca3ab9adf025bd216ec036da4cd8c11fda7b3213bbf2d48cd2571d67755`

```dockerfile
```

-	Layers:
	-	`sha256:36bc1a3ed7a552c640080b0a927760b147b19bc4efc3b1206d2649f64d9ee19b`  
		Last Modified: Fri, 22 May 2026 22:08:19 GMT  
		Size: 18.1 MB (18055657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bb7e53a38a394cfd027a2ac82adb85aac73340393f411d12744462ec85c4532`  
		Last Modified: Fri, 22 May 2026 22:08:18 GMT  
		Size: 20.9 KB (20865 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1beca1cd7e1ebb10f38a3abf8b6249f3d9801d23ad5a7f5c457e40bb2c8b6bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.2 MB (365227778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fddc7e05553fea90e11c8277f88e7a60b35b55adc46deb527b9ac9f9b9ca98a`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 May 2026 20:12:25 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:25 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:10:41 GMT
ARG version=1.8.0_492.b09-2
# Fri, 22 May 2026 21:10:41 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:10:41 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:10:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 22 May 2026 22:08:08 GMT
CMD ["gradle"]
# Fri, 22 May 2026 22:08:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 May 2026 22:08:08 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 22 May 2026 22:08:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 22 May 2026 22:08:08 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 May 2026 22:08:08 GMT
WORKDIR /home/gradle
# Fri, 22 May 2026 22:08:08 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 22 May 2026 22:08:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 22 May 2026 22:08:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 22 May 2026 22:08:11 GMT
USER gradle
# Fri, 22 May 2026 22:08:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 22 May 2026 22:08:11 GMT
USER root
```

-	Layers:
	-	`sha256:a92e5e4b9e90f970dfdf3c3258e673bb767c6401beba9985a3b635162466eedd`  
		Last Modified: Fri, 15 May 2026 20:34:37 GMT  
		Size: 53.5 MB (53454415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba004d93628b9d5794265bf99f9a1a771d2977c59482363489cc72908526a674`  
		Last Modified: Fri, 22 May 2026 21:11:02 GMT  
		Size: 118.0 MB (117957852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44cd83530c2aa6e5650a67647890c5815313d9f987c56bb95c65fd51c7efb8c`  
		Last Modified: Fri, 22 May 2026 22:08:41 GMT  
		Size: 85.7 MB (85692136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef26b5799bc822c99bd940feda89bf18d8e4f5cf1e4dc0147fc4c1200c704c8a`  
		Last Modified: Fri, 22 May 2026 22:08:38 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4809ff38529b374c3b426b7c0a7555c6ab0d22d04b0846b2f0119f389e6a7e3`  
		Last Modified: Fri, 22 May 2026 22:08:42 GMT  
		Size: 107.7 MB (107696668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0368ec9912c05ab86f5c9179a5500d4860778a074ea7e99cef9f6e4c5bae78ac`  
		Last Modified: Fri, 22 May 2026 22:08:38 GMT  
		Size: 425.0 KB (425025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:6cd059a9966b1e8ad245bcbbf1f8da3c1a0da80fb64490ab76fb74c176b12870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11640850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90bab0919f59b9a916c679b97bbb1c3fb3d5c607556c59135b52e906fa9337d`

```dockerfile
```

-	Layers:
	-	`sha256:7797fbf966f98ed1184510fc652b7cba70f79452e4570c735a2eb3c1ca622a9e`  
		Last Modified: Fri, 22 May 2026 22:08:38 GMT  
		Size: 11.6 MB (11619813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:224e4327859d5933c67324d24c223d3bc4df9f9b7e0447d2edcdd25691172b75`  
		Last Modified: Fri, 22 May 2026 22:08:37 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json
