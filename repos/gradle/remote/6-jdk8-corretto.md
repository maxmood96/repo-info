## `gradle:6-jdk8-corretto`

```console
$ docker pull gradle@sha256:29da0c090d900d1a6473e2e480e39de534e9f4c39eb47ecb65d9f4e3397854bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:8fd4eb4bd5ae3086a41316f79a26fd90233d90650639daa276a0cc3f8846b746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.1 MB (559134875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb8ac3adb7c1e0a01d04ccaa0353b18ca3853f36345c4cb66b5d60bd7db47ec`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:40 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:07:42 GMT
ARG version=1.8.0_492.b09-1
# Fri, 24 Apr 2026 00:07:42 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:07:42 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:07:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 24 Apr 2026 01:12:44 GMT
CMD ["gradle"]
# Fri, 24 Apr 2026 01:12:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 24 Apr 2026 01:12:44 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 24 Apr 2026 01:12:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 24 Apr 2026 01:12:44 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 24 Apr 2026 01:12:44 GMT
WORKDIR /home/gradle
# Fri, 24 Apr 2026 01:12:44 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 24 Apr 2026 01:12:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 24 Apr 2026 01:12:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 24 Apr 2026 01:12:47 GMT
USER gradle
# Fri, 24 Apr 2026 01:12:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 24 Apr 2026 01:12:48 GMT
USER root
```

-	Layers:
	-	`sha256:60406c832328f9a4f3aa21eb9cb5b2182d79ad008cd21f0bbac4517c1836be2e`  
		Last Modified: Tue, 14 Apr 2026 01:03:42 GMT  
		Size: 54.6 MB (54569705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fcbe00f05919278904b5563c0e887d2bd2e587821525f8d12a15136824da25`  
		Last Modified: Fri, 24 Apr 2026 00:08:37 GMT  
		Size: 330.9 MB (330925523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c483dc864100a82142fceb207256ebbbf9d2fb591e6e331ae5b7885f7b1a040f`  
		Last Modified: Fri, 24 Apr 2026 01:13:30 GMT  
		Size: 65.5 MB (65509722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bdaf323ab8e0e0f169381a8a0321b0e2b08608780ccb42605170bc60279d46`  
		Last Modified: Fri, 24 Apr 2026 01:13:27 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04db13401e66014e6a79c002ddb2e949f692b78c4e1cbe26e4d51fea14660230`  
		Last Modified: Fri, 24 Apr 2026 01:13:31 GMT  
		Size: 107.7 MB (107696669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3370778aab82c882ef161b67e1d5fbbe43e724cc81d0221873a5c6008c63c744`  
		Last Modified: Fri, 24 Apr 2026 01:13:27 GMT  
		Size: 431.3 KB (431283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:e4fcb2e91fb069f186af4e23a0455475a78033b1575f66d31531309ef26dc22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18076336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c36203cd09e2a1792c8f8a2fea78e407d898f03ce914f00a7df45c197e3cf62`

```dockerfile
```

-	Layers:
	-	`sha256:220b0d3cdbfd5e83c4132360a254961a499bd01410f63280a5412f6161e7df97`  
		Last Modified: Fri, 24 Apr 2026 01:13:28 GMT  
		Size: 18.1 MB (18055471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce47de35060f41a5cf9ebc433cb7be73f4cb150bd712626e1d6548fc31834305`  
		Last Modified: Fri, 24 Apr 2026 01:13:26 GMT  
		Size: 20.9 KB (20865 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:18a5fb4524aed1ef2b94283bf90fa89ea26c7da9372d9d494f07bc4364cd1691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.2 MB (365178995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02595f64c4846c3990794faf0f3a76d8c6850f7f01f2a11a159249dc596a94e4`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:02 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:08:01 GMT
ARG version=1.8.0_492.b09-1
# Fri, 24 Apr 2026 00:08:01 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:08:01 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:08:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 24 Apr 2026 01:12:48 GMT
CMD ["gradle"]
# Fri, 24 Apr 2026 01:12:48 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 24 Apr 2026 01:12:48 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 24 Apr 2026 01:12:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 24 Apr 2026 01:12:49 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 24 Apr 2026 01:12:49 GMT
WORKDIR /home/gradle
# Fri, 24 Apr 2026 01:12:49 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 24 Apr 2026 01:12:49 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 24 Apr 2026 01:12:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 24 Apr 2026 01:12:51 GMT
USER gradle
# Fri, 24 Apr 2026 01:12:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 24 Apr 2026 01:12:52 GMT
USER root
```

-	Layers:
	-	`sha256:a89c935522476873ac76a02a8b4103cba17c6900bdcb1d98998ed64657edf59f`  
		Last Modified: Tue, 14 Apr 2026 02:24:36 GMT  
		Size: 53.5 MB (53452253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592711723e0842403f83b69e22d505864fc2b3d35777efa566c46b8e549191a1`  
		Last Modified: Fri, 24 Apr 2026 00:08:22 GMT  
		Size: 118.0 MB (117963358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d832cffcc5694dca9b368a16a518c562ed3a159f2656ba72f6537303b77b2ce6`  
		Last Modified: Fri, 24 Apr 2026 01:13:22 GMT  
		Size: 85.6 MB (85640007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb8a4b69c48789af4c6948042ac5c856dba9eb0a7595ff59c4f6c57c2a57bb6`  
		Last Modified: Fri, 24 Apr 2026 01:13:18 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b62d1ae0783d55bbbb5f421569736091da2333d5747e0ab17b42f272145faf2`  
		Last Modified: Fri, 24 Apr 2026 01:13:23 GMT  
		Size: 107.7 MB (107696665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a03ae331c2c222aba097f7ef7f49fde1240362b0e880521ef639843775c87e`  
		Last Modified: Fri, 24 Apr 2026 01:13:18 GMT  
		Size: 425.0 KB (425031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:6d8d270c9c557ca71c505fb7730e43d98644c10c4c87b30aa86e1e48aa892274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11640673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1e62bcf64cfd373a67ec4cec9baa47d6280c3a9d72a2af34c54ee1f12f1259`

```dockerfile
```

-	Layers:
	-	`sha256:ed575efb01afa5330ff6885047f2bf7ed7030b1463b18374950907937fe9cea7`  
		Last Modified: Fri, 24 Apr 2026 01:13:19 GMT  
		Size: 11.6 MB (11619635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f66a161421922aff97754de3ea2fb70e7d56df2d23ea1498eeedd3194bcb5e81`  
		Last Modified: Fri, 24 Apr 2026 01:13:18 GMT  
		Size: 21.0 KB (21038 bytes)  
		MIME: application/vnd.in-toto+json
