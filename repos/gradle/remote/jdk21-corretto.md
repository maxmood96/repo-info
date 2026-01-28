## `gradle:jdk21-corretto`

```console
$ docker pull gradle@sha256:17e363f9f5dee65eb3b31ef134d4fbdae2a6b349bf79fa831cdba5234f5f71a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk21-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:65a32b39adfbc8e21d7dade2e08c251c7747f0d9fc19e3b67c7c2d61f72c7ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.3 MB (447269722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a681f7fc057ab930efdd3fee44b048b93f7f68ac0e17bc8a544b4a007d7ea7c`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:39 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:39 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:11:36 GMT
ARG version=21.0.10.7-1
# Tue, 27 Jan 2026 22:11:36 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:11:36 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:11:36 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:11:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 27 Jan 2026 23:11:56 GMT
CMD ["gradle"]
# Tue, 27 Jan 2026 23:11:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 Jan 2026 23:11:56 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 Jan 2026 23:11:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 27 Jan 2026 23:11:56 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 Jan 2026 23:11:56 GMT
WORKDIR /home/gradle
# Tue, 27 Jan 2026 23:11:56 GMT
ENV GRADLE_VERSION=9.3.0
# Tue, 27 Jan 2026 23:11:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Tue, 27 Jan 2026 23:11:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 Jan 2026 23:11:59 GMT
USER gradle
# Tue, 27 Jan 2026 23:11:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 27 Jan 2026 23:11:59 GMT
USER root
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6b2affcaf3319a5d68a22e24f47aa31f4eb325a0d9638c8931197c613f6a33`  
		Last Modified: Tue, 27 Jan 2026 22:11:57 GMT  
		Size: 170.2 MB (170196234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3d1911aae59c4e979b31f9189283c471883b02cd697fb01498ae31e19749f3`  
		Last Modified: Tue, 27 Jan 2026 23:12:30 GMT  
		Size: 86.0 MB (86033510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5a64264493ff501e9f61cafbeadac3669d8658b162e881d82523fd08e3ad04`  
		Last Modified: Tue, 27 Jan 2026 23:12:25 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0319d6b9bb0331d65574bd94724aff26d0b06293e14f6d6d2e0a087906ace9`  
		Last Modified: Tue, 27 Jan 2026 23:12:32 GMT  
		Size: 137.0 MB (136988872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bc61266ffe7e56a1c6fe8c2c2a607557808a891780012cd27cb9086c937304`  
		Last Modified: Tue, 27 Jan 2026 23:12:26 GMT  
		Size: 25.6 KB (25591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:3034d2db8616fc34b18e5e11221dd9e5cb58ac29f19d86a64974d7f8853fd15f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11347773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968c376701158e5b4a20aa8dadd1dcc75a3616a01e64d5183bc68f4f794d409f`

```dockerfile
```

-	Layers:
	-	`sha256:7ea41696aefb599686012a10d6fd3f24edd97a35dc7ec85724f1fa4cb1e38f37`  
		Last Modified: Tue, 27 Jan 2026 23:12:26 GMT  
		Size: 11.3 MB (11326122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4494f7acb1d192e7d50a4ec09045fa91bff206e57b26e5af0a42443ed04e83`  
		Last Modified: Tue, 27 Jan 2026 23:12:25 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:77c6f2fa9c1e9d04584333e683f4cf7c2fc9065de0f91ca2568c0377e2008e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.9 MB (443918761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e71f6c320226538d1197becb59b513de3f4e4d0ae871cc305662b3145329765`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Jan 2026 21:24:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:24:49 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:44 GMT
ARG version=21.0.10.7-1
# Tue, 27 Jan 2026 22:12:44 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:12:44 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:12:44 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 27 Jan 2026 23:12:14 GMT
CMD ["gradle"]
# Tue, 27 Jan 2026 23:12:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 Jan 2026 23:12:14 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 Jan 2026 23:12:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 27 Jan 2026 23:12:14 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 Jan 2026 23:12:14 GMT
WORKDIR /home/gradle
# Tue, 27 Jan 2026 23:12:14 GMT
ENV GRADLE_VERSION=9.3.0
# Tue, 27 Jan 2026 23:12:14 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Tue, 27 Jan 2026 23:12:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 Jan 2026 23:12:16 GMT
USER gradle
# Tue, 27 Jan 2026 23:12:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 27 Jan 2026 23:12:17 GMT
USER root
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f46fcbcc478da5af0cdc2bd8402eaa8b18d5383a839c1f65a081622797b132`  
		Last Modified: Tue, 27 Jan 2026 22:13:08 GMT  
		Size: 168.5 MB (168468866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff995b5cc1393dfcf5fdd0aaa9c477766b64708087fafc8bceb67c9dd0b5e0d`  
		Last Modified: Tue, 27 Jan 2026 23:12:49 GMT  
		Size: 85.5 MB (85513389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fc12137a52aa4050ce6aab07fbbbdcdbfa4a0cb8e04e700e684047dfa4edbb`  
		Last Modified: Tue, 27 Jan 2026 23:12:45 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52fd7e9998e907a35993cd432a00e730bddbcf94170172099d03a3694ad2828`  
		Last Modified: Tue, 27 Jan 2026 23:12:50 GMT  
		Size: 137.0 MB (136988869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f657975b0b5ef89da0fe8a0cd3b9cbd8d92b2941881bfc2592dacc04cc03e82`  
		Last Modified: Tue, 27 Jan 2026 23:12:45 GMT  
		Size: 29.3 KB (29320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:b8998c8cd17ca3785fe621c43beef975fe13013922b5fd846672e139eeea9d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11346971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f505f5d14ac34b454c089b9134c6c1014cbeb5f4c8aeb1a668895ff1543800d`

```dockerfile
```

-	Layers:
	-	`sha256:9a4a4078cac9f9ae7dbb6c37f0bdf255fc2164ed66f38b54f9bf3ad228018e01`  
		Last Modified: Tue, 27 Jan 2026 23:12:46 GMT  
		Size: 11.3 MB (11325124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42df4acf0cb1a4c300115b854274b7d70d0136ab1e2f26d1ef102027155294fb`  
		Last Modified: Tue, 27 Jan 2026 23:12:45 GMT  
		Size: 21.8 KB (21847 bytes)  
		MIME: application/vnd.in-toto+json
