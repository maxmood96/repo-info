## `gradle:7-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:8fa1d6db0200401f91d37584b80ee5a92d53d8d9b0eac783d463754f0344f65e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto-al2023` - linux; amd64

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

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

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

### `gradle:7-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3fc2136872a5c8a172be9f392636dc3d044ce57c2a9480606cfa86c0214974eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 MB (382158897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c223856ad22dd914215216570d2ed59ddfdf20510f6de6f44324c5dafb63963`
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
	-	`sha256:ba09f42fc275188932072e6c429c18ecea19f0ee9531c6f5aa93b39fc8318457`  
		Last Modified: Wed, 04 Jun 2025 21:27:11 GMT  
		Size: 128.5 MB (128469906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589f0103f4837d625cb9f624ccc520c89039205e90c716e20336da2f40eb54d4`  
		Last Modified: Wed, 04 Jun 2025 21:27:35 GMT  
		Size: 59.5 KB (59535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:5c4ef6ad2d068895684a1ad3669771ead72fda39d09df894696789d08903832f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11577256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e0629c7c835654d79a673ed020ce075c602a40b72568f28a77e6074dfd8f3e`

```dockerfile
```

-	Layers:
	-	`sha256:068bb90d4eed3f4e921b1fbe096a5a9e6987c45d1f2d9e102c2de64f49ff3f86`  
		Last Modified: Wed, 04 Jun 2025 23:19:59 GMT  
		Size: 11.6 MB (11556160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beeb080d5b04d939774372d1ae0e5318d5427cc78c29f2dadc9651488feb282d`  
		Last Modified: Wed, 04 Jun 2025 23:20:00 GMT  
		Size: 21.1 KB (21096 bytes)  
		MIME: application/vnd.in-toto+json
