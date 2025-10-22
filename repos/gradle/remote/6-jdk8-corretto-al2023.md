## `gradle:6-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:e0c819291798690820e003206b0c5a61bab072b30ec934a13c7e3ec30e19a1e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:0cecf1cc99740d94518ce5feafbd892e510433d7554dac8c2253f48f7872b149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.9 MB (557912954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14ce074d7c00b885b3074a9c949df61c79c97d4e98721cfa67c2d297cc09ef4`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 23 Sep 2025 15:36:53 GMT
COPY /rootfs/ / # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 15:36:53 GMT
ARG version=1.8.0_472.b08-1
# Tue, 23 Sep 2025 15:36:53 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
ENV LANG=C.UTF-8
# Tue, 23 Sep 2025 15:36:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 23 Sep 2025 15:36:53 GMT
CMD ["gradle"]
# Tue, 23 Sep 2025 15:36:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 23 Sep 2025 15:36:53 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 23 Sep 2025 15:36:53 GMT
WORKDIR /home/gradle
# Tue, 23 Sep 2025 15:36:53 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 23 Sep 2025 15:36:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 23 Sep 2025 15:36:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
USER gradle
# Tue, 23 Sep 2025 15:36:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
USER root
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7cb1a2144d133ea8df6530b1b49b0a08bf3c6ecf08514a495182d46a12c94e`  
		Last Modified: Wed, 22 Oct 2025 01:16:49 GMT  
		Size: 330.9 MB (330880308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e48d6ef67f57e762a8c78eb83e0defb9494ea5e318969239ee40cf8bd83e46c`  
		Last Modified: Wed, 22 Oct 2025 02:40:15 GMT  
		Size: 64.9 MB (64897590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56efa2f0ce1ee8418076b2858e0d7ee2d78caab17f023594816caa24deae4ab`  
		Last Modified: Wed, 22 Oct 2025 02:39:59 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be83ca809938d6712f4bee32898a5eba0aa4f6849596dc0984b102f346820fa3`  
		Last Modified: Wed, 22 Oct 2025 02:40:23 GMT  
		Size: 107.7 MB (107696664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5081a48f49313f5a7efa07cbd13c1dd1cef0d37ba3f0b2dfe6191aa2abb40b0`  
		Last Modified: Wed, 22 Oct 2025 02:40:00 GMT  
		Size: 431.3 KB (431278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:0245cf01da40186df2d3189c3a61c7cec58815cd7830733c636c2a6bd18ad038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (18038515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cf0180cb09f0dce03608482f81a9e543836dbf557047629663dbed5aadbdec`

```dockerfile
```

-	Layers:
	-	`sha256:4393eb95306f76bd5d935bafd9de86d31969e6817ec0941a92b2f67b993680a5`  
		Last Modified: Wed, 22 Oct 2025 05:17:48 GMT  
		Size: 18.0 MB (18017607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c090fb6b5a40fb93b1439c1d864acdb185eb43087475b07b4273f6bacad30871`  
		Last Modified: Wed, 22 Oct 2025 05:17:49 GMT  
		Size: 20.9 KB (20908 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:548214ec6f9342efde4ba775532c75472e6b2343bdf1496e1c2b68c03ec8b011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.1 MB (364055002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645299c62be236bf449fe52696cd4e3a888449d585ca633d160d6b77185ee0de`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 23 Sep 2025 15:36:53 GMT
COPY /rootfs/ / # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 15:36:53 GMT
ARG version=1.8.0_472.b08-1
# Tue, 23 Sep 2025 15:36:53 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
ENV LANG=C.UTF-8
# Tue, 23 Sep 2025 15:36:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 23 Sep 2025 15:36:53 GMT
CMD ["gradle"]
# Tue, 23 Sep 2025 15:36:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 23 Sep 2025 15:36:53 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 23 Sep 2025 15:36:53 GMT
WORKDIR /home/gradle
# Tue, 23 Sep 2025 15:36:53 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 23 Sep 2025 15:36:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 23 Sep 2025 15:36:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
USER gradle
# Tue, 23 Sep 2025 15:36:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
USER root
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674e071575b5649265d982d1973f5eae415eda1d4607f8c12d44a14efb490e9c`  
		Last Modified: Tue, 21 Oct 2025 21:49:03 GMT  
		Size: 118.0 MB (117963037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d433ec21a7ef591e389ddd4d9d4e17d753226f3f73504766ba44bbb9c770f6`  
		Last Modified: Tue, 21 Oct 2025 22:13:54 GMT  
		Size: 85.1 MB (85077395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8a7c6074e42b33e36e77b87a53cf57d3f64992f2dc23307007cff9618543bd`  
		Last Modified: Tue, 21 Oct 2025 22:13:45 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98315aca0467a433e066892902a0b732b3709d810fe40351dbc381edcc7a6a9f`  
		Last Modified: Tue, 21 Oct 2025 22:14:03 GMT  
		Size: 107.7 MB (107696665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bad4d57e711474c2a83252ce888fb08916cc2f50b655849e0bfb98377e72ac`  
		Last Modified: Tue, 21 Oct 2025 22:13:46 GMT  
		Size: 425.0 KB (425022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:1035d58a5f3e8626bcb509ea4e708ff1dd177c9c024103aed6fd992381164ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11602854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b62f3e60851321e2fc15716e59daeaebc4f56eb02202a8ffe9dc8dc9f9018e`

```dockerfile
```

-	Layers:
	-	`sha256:711c0894f4f2e9c9bf95626de36cd3eeeda37681daa46224c89fee2cd9b70cfa`  
		Last Modified: Tue, 21 Oct 2025 23:17:50 GMT  
		Size: 11.6 MB (11581773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b212fe6bcdde83022741c7a828e22f89b02b140be90e63b677e2ebf315d276`  
		Last Modified: Tue, 21 Oct 2025 23:17:51 GMT  
		Size: 21.1 KB (21081 bytes)  
		MIME: application/vnd.in-toto+json
