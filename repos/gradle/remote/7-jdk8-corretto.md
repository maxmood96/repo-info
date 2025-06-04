## `gradle:7-jdk8-corretto`

```console
$ docker pull gradle@sha256:235e21682df7b003622a737436c5d4e755288faee516dbf69638c8ffaf7a8149
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:fb6c49c6abcb92a2b43c0932de00dbbaa38535d40c5e23b3f9e6050a6fcd92fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **575.8 MB (575822681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bfa0faee4726458d5df15ba82944b3884f7b70409bc4a6449c4ffe0263fa2f`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=1.8.0_452.b09-2
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=1.8.0_452.b09-2
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 04 Jun 2025 15:28:43 GMT
CMD ["gradle"]
# Wed, 04 Jun 2025 15:28:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 04 Jun 2025 15:28:43 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 04 Jun 2025 15:28:43 GMT
WORKDIR /home/gradle
# Wed, 04 Jun 2025 15:28:43 GMT
ENV GRADLE_VERSION=7.6.5
# Wed, 04 Jun 2025 15:28:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
# Wed, 04 Jun 2025 15:28:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
USER gradle
# Wed, 04 Jun 2025 15:28:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
USER root
```

-	Layers:
	-	`sha256:d680ca3f92ab1808f4ae68645f57801d7a408a68d8d17cd7b28da6cfad1ad3d7`  
		Last Modified: Thu, 15 May 2025 19:36:56 GMT  
		Size: 53.6 MB (53614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fe6cf55dc3adf66743afc67d7bcfc0ce974e2646080ac95d6c204123e58662`  
		Last Modified: Mon, 19 May 2025 23:46:39 GMT  
		Size: 330.7 MB (330665928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3859ac7d32a8b159350b3fc2d7d5e94e0c8d6c3a7f85747151537fee3e7faf6`  
		Last Modified: Wed, 04 Jun 2025 18:04:49 GMT  
		Size: 63.0 MB (63015252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f7d705c327a77a63b449212a0dd8794338990faefc1747107b378a1349b5e5`  
		Last Modified: Wed, 04 Jun 2025 18:04:42 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea6bf0ca79aa685aa3958d7aea55dbf341f07936ba8d8fe2fc72eba75312bbd`  
		Last Modified: Wed, 04 Jun 2025 18:04:17 GMT  
		Size: 128.5 MB (128469908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd6727b64136e43ad06ead482bd98b84f80f58bf621e78df5ceb317d42730ac`  
		Last Modified: Wed, 04 Jun 2025 18:04:44 GMT  
		Size: 54.9 KB (54910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:c02be65dfacb2d512036441ae8ca127ef5f34ea0d1b21c14b2c06f8a0160ea65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18008823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b37a19549f371f57681abb2bb93b4180dbb53a2dc3bdd9575a963d0b4bde67`

```dockerfile
```

-	Layers:
	-	`sha256:ce8b446c992c551567d5eabfd177b6b715e823f14d03863f00beec06ca65f8fe`  
		Last Modified: Wed, 04 Jun 2025 20:19:23 GMT  
		Size: 18.0 MB (17987900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4e075704fe4622a295d84899db79573acae7055ba97433c5a5063c63676cb79`  
		Last Modified: Wed, 04 Jun 2025 20:19:24 GMT  
		Size: 20.9 KB (20923 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a182cb7bb73c8ef0c4d8adefbe40e531f9586c1e4a1c0d204586e5a00235aeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.4 MB (376419521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef855d2d85d19f77aacb2b6542dcd839a0e89161f852a8e92d6fc249f1515377`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=1.8.0_452.b09-2
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=1.8.0_452.b09-2
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 29 May 2025 19:53:06 GMT
CMD ["gradle"]
# Thu, 29 May 2025 19:53:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 29 May 2025 19:53:06 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 29 May 2025 19:53:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 29 May 2025 19:53:06 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 29 May 2025 19:53:06 GMT
WORKDIR /home/gradle
# Thu, 29 May 2025 19:53:06 GMT
ENV GRADLE_VERSION=7.6.4
# Thu, 29 May 2025 19:53:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Thu, 29 May 2025 19:53:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 29 May 2025 19:53:06 GMT
USER gradle
# Thu, 29 May 2025 19:53:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 29 May 2025 19:53:06 GMT
USER root
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Thu, 15 May 2025 19:36:48 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ba910b575edfd05c7f13065f2a17cff35d62e2af5009fcfda96edd05eb5b25`  
		Last Modified: Tue, 20 May 2025 01:31:01 GMT  
		Size: 117.8 MB (117849549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fc11a710abef911acfcace2edde4d57b344a68bb715a41e607fb2cf7b8c3bd`  
		Last Modified: Wed, 04 Jun 2025 19:47:15 GMT  
		Size: 83.2 MB (83212495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d19c2811dd48e022546f7be82efde619a8b51d4efb0f2919e2d5a537819086`  
		Last Modified: Tue, 03 Jun 2025 16:32:48 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396370a4d3610230796e924253627b831aa5fb291028eea0ad54e4a695fc554a`  
		Last Modified: Mon, 02 Jun 2025 17:38:11 GMT  
		Size: 122.7 MB (122730528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80126f0634cb9c7670ca0c9584ca467266ddee783930ac1598059b8e8437d25a`  
		Last Modified: Tue, 03 Jun 2025 15:13:17 GMT  
		Size: 59.5 KB (59537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:c5a20eb0341ead6fc2242fae9db97d6d0587b7ca5975c1bf629609498d369c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11570772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fc7f788c25f89d109449b16e94650f214acb2825169d80b405e020174f7c06`

```dockerfile
```

-	Layers:
	-	`sha256:36b5894bc5cf32b4a838b56c8183ddd87e15fe934cc3e07c639a2016a9f9326b`  
		Last Modified: Wed, 04 Jun 2025 20:19:39 GMT  
		Size: 11.5 MB (11549676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d4ede6791680e8e35abf3093618aba9e77c99e4e253d34e719a64cd76cce1cd`  
		Last Modified: Wed, 04 Jun 2025 20:19:40 GMT  
		Size: 21.1 KB (21096 bytes)  
		MIME: application/vnd.in-toto+json
