## `gradle:jdk11-corretto`

```console
$ docker pull gradle@sha256:6198796905b3bc7a04dc5db8f9fb92771185c426aefaf8dbab7cc85ba1bfade2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:eed719aab47ed2a1f0223e65510f0b464890744937d8b4d01d291f08fba15d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.6 MB (428639484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242aa4e004b6aacc78fc088ba8fb8a15f9c53891c484a8dce4abdbb74d4d0055`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:d680ca3f92ab1808f4ae68645f57801d7a408a68d8d17cd7b28da6cfad1ad3d7`  
		Last Modified: Thu, 15 May 2025 19:36:56 GMT  
		Size: 53.6 MB (53614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889e9ac9fc3d45e4907ce0fcf1fdda95e985943f212ff7c433b40b7471c65762`  
		Last Modified: Mon, 19 May 2025 23:45:53 GMT  
		Size: 153.9 MB (153910910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763176388aa8d98d14e19c1801b05254921f1b8b5044b2dd98fe7ed4a65c5289`  
		Last Modified: Thu, 05 Jun 2025 23:30:57 GMT  
		Size: 83.7 MB (83661812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6990335040995958e0a798df6e86542cc080bcfebe10b1d617d19e419e7c98e`  
		Last Modified: Thu, 05 Jun 2025 23:30:53 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a84cda9858f0e5cd78f2cad44e4da1a90559457529ebd000d5c7565b226ba4`  
		Last Modified: Thu, 05 Jun 2025 23:31:01 GMT  
		Size: 137.4 MB (137395474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db0885b26fa3ed1eba4501960c637de3c972b9a027331412832d5a530fa4ca1`  
		Last Modified: Thu, 05 Jun 2025 23:30:54 GMT  
		Size: 54.9 KB (54907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:8c9dfb45b4b6bd3f987420d7b3fdb2f768c7a51bc933315ae0d206b5c59962aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11315722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c161eb74f5bdbb59be724b518933fa656133b33cd22c3fd77820b412d252eba`

```dockerfile
```

-	Layers:
	-	`sha256:d37418ad53d26a99a2b7864ba8f6bf050e78b320ca02edf7526bab6362019b90`  
		Last Modified: Thu, 05 Jun 2025 20:20:31 GMT  
		Size: 11.3 MB (11294140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e8b8ddbdccc5721cf5365b0299d69fa162960a1cd256784a327102c90df8f1c`  
		Last Modified: Thu, 05 Jun 2025 20:20:32 GMT  
		Size: 21.6 KB (21582 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3633384541c40a3a7142ce3bb48b1eb62badd9c55dcf80d6cce61ce363235318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.7 MB (425692699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03b379793754589dcb2d0a2b006f5c8d5a5773cb39df4629ada97cb86252934`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Thu, 15 May 2025 19:36:48 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b7c511921905c90e2da7ccd5e55a13dc20d0647295cec48db9cd48880a4519`  
		Last Modified: Tue, 20 May 2025 01:02:47 GMT  
		Size: 152.4 MB (152434450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90443e2e7591cc04cb8fd0e4ac9893f80e76d61494c0abf16332ed4ca2735bbf`  
		Last Modified: Thu, 05 Jun 2025 02:20:58 GMT  
		Size: 83.2 MB (83235788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a012bbdd5a202a0f453b869bf58e5b7424e3c293f10503ca804d1d6abba5d0a3`  
		Last Modified: Tue, 03 Jun 2025 16:34:40 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661818f73ecf9b1faf3baf43f481407b87d485a0eb7826cfb3400d33c5bdd017`  
		Last Modified: Fri, 06 Jun 2025 02:09:03 GMT  
		Size: 137.4 MB (137395505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5683a07940bff58730649380250b4440b3aa5c926189fb22dbb8a8036e81f5f8`  
		Last Modified: Thu, 05 Jun 2025 20:21:02 GMT  
		Size: 59.5 KB (59542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:246ea3cc211a1d2c2c979edc5933f787a2854410b2575445656a6a289a11c93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11315762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7aaae56b357d19d6a0bd5e82b38c2c0b226667f172b84575194a909034147c8`

```dockerfile
```

-	Layers:
	-	`sha256:802e286d6dbab3cbf680c857c46d1ab4748e41e0a21c1c1e069c64c090f1d368`  
		Last Modified: Thu, 05 Jun 2025 23:21:01 GMT  
		Size: 11.3 MB (11293983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea4b6391057d22201f6a31a1f8b0da2aea4eb863d1fcc9ea16e797a6baa87da`  
		Last Modified: Thu, 05 Jun 2025 23:21:02 GMT  
		Size: 21.8 KB (21779 bytes)  
		MIME: application/vnd.in-toto+json
