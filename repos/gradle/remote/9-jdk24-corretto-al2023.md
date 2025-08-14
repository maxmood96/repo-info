## `gradle:9-jdk24-corretto-al2023`

```console
$ docker pull gradle@sha256:20d275dd773ac63145c924126f6827b3ec35a5a618243974edb82baf6753e49b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk24-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:0cd8deac67460e822f5d8a090496d2c5f2baaa004860d8ae04b79a8b230e69fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.3 MB (461312510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c243e0e22c6282dcd6bff7798a78d13def735d9da3e4548509c56edd8654ad`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=24.0.2.12-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER gradle
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER root
```

-	Layers:
	-	`sha256:b9bd06b1e98f2884554d02055b944634294fa4d6f341ec4d0d7349c492676b31`  
		Last Modified: Sat, 09 Aug 2025 04:12:21 GMT  
		Size: 53.8 MB (53837959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d48750dcbc88918e08cdc4bda3900bf3a452f14a5f37b204bc3502dfaab038`  
		Last Modified: Wed, 13 Aug 2025 23:11:05 GMT  
		Size: 187.4 MB (187386721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8d9ec3c2b9a3b66d1011aa74878c76a8c6f5d487d05b553da315b1adfdb3ca`  
		Last Modified: Thu, 14 Aug 2025 03:02:21 GMT  
		Size: 85.6 MB (85550429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb6ffa89a759c6a99e1e4e9f0fac082a3f667019f2003b0a5d20803f9b2d11f`  
		Last Modified: Thu, 14 Aug 2025 02:11:17 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559c8c7f616521faec96da0337394b5a338e0ee69fb743e13a45e876bb74e4d0`  
		Last Modified: Thu, 14 Aug 2025 06:39:29 GMT  
		Size: 134.5 MB (134480828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4596e244b91680e044fbfa1edf8d57d8079737f8a29fc40af66794c1e421127f`  
		Last Modified: Thu, 14 Aug 2025 02:03:32 GMT  
		Size: 54.9 KB (54894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk24-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:0a108a4679b1936a14a53e11855d9fdc3f49271af373503a3dab02b950cc7196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11333876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a82ee6b2a6d6ab8afdbbab68accdeb1261903babc538da80816b234f6f96e33`

```dockerfile
```

-	Layers:
	-	`sha256:fbcd835eefa7d495f92a803d3e6d6bc4268a32eb6ad428a3fe6b0c39077a3ad9`  
		Last Modified: Thu, 14 Aug 2025 02:25:27 GMT  
		Size: 11.3 MB (11312305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb20cb5d67789dc0a67f9c90b611dce1080cd380259ddd62773c699b8b0cc1b8`  
		Last Modified: Thu, 14 Aug 2025 02:25:28 GMT  
		Size: 21.6 KB (21571 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk24-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:dcb890f2e2d560affb170bcfe94776a9c8a0a810b2591f63ae39184025ca2ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **457.8 MB (457771375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6ce29b2eadf050fe1fc2385400835052083ecc8dfd93dae8ff04993a836a4e`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=24.0.2.12-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER gradle
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER root
```

-	Layers:
	-	`sha256:93b5cbbc86ee614f8432762e1f7f34b6cc9d6d4b95867cf25bca6ae179f49439`  
		Last Modified: Sat, 09 Aug 2025 04:12:37 GMT  
		Size: 52.7 MB (52726394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8fe3dd6a3466db38a1fbed83ebaa82aec0d67c18d03baa73602aa3563e2ac9`  
		Last Modified: Thu, 14 Aug 2025 12:48:43 GMT  
		Size: 185.4 MB (185426437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6ca815e3767afabbd76da833d7e2a77001b4ceee72a823530f4a3e3fd691cc`  
		Last Modified: Thu, 14 Aug 2025 11:22:07 GMT  
		Size: 85.1 MB (85076495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06863f932b196e3d323d95d97d5957cf742c5100ca047a5863bb0f49c205889`  
		Last Modified: Thu, 14 Aug 2025 11:21:37 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b891679c9b63b755aba7c4de0300cec62281406cee8252fc7e2bc8b8127f4ecb`  
		Last Modified: Thu, 14 Aug 2025 14:40:19 GMT  
		Size: 134.5 MB (134480835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39406f8d9d86ab797bb4cf6ea60b3a4ecd242b8bb5a0a72856fbbe716df3b62a`  
		Last Modified: Thu, 14 Aug 2025 11:21:37 GMT  
		Size: 59.5 KB (59535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk24-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:753c1f465367003aa7489e6253087d978ef717202ad3689d2612fb287e55a620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11333085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c1b18ae275d1c682442a035bad4a75d2a819fbc7676cf43f9a6b3a5397228e`

```dockerfile
```

-	Layers:
	-	`sha256:db99a1cc25c4c9b75797d15154fb6cd35e3b3af4d35990cf36da8080c9db6e23`  
		Last Modified: Thu, 14 Aug 2025 14:25:40 GMT  
		Size: 11.3 MB (11311318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d1a58577d22bcc18553f629e250cbe60ca5ec810afbd51ebbf8bfe18b054254`  
		Last Modified: Thu, 14 Aug 2025 14:25:41 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json
