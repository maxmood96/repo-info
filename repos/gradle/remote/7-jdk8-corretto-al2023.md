## `gradle:7-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:d67458d8d5e689b949e216a2413dc7f6435cdf9a442a872bbc37d5ebe5cf1a4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:775cecb8a685accfc6cabe1d249b791e4c2041d341bb0b8d82a78bbfc68df3ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.9 MB (578854523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1305d73cc1682226557868c0526b188f6a7d1d376d23d88abb227664466abe3`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:49 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:04 GMT
ARG version=1.8.0_482.b08-1
# Tue, 10 Feb 2026 18:31:04 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:31:04 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 10 Feb 2026 19:07:11 GMT
CMD ["gradle"]
# Tue, 10 Feb 2026 19:07:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 10 Feb 2026 19:07:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 10 Feb 2026 19:07:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 10 Feb 2026 19:07:11 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 10 Feb 2026 19:07:11 GMT
WORKDIR /home/gradle
# Tue, 10 Feb 2026 19:07:11 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 10 Feb 2026 19:07:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 10 Feb 2026 19:07:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 10 Feb 2026 19:07:14 GMT
USER gradle
# Tue, 10 Feb 2026 19:07:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 10 Feb 2026 19:07:14 GMT
USER root
```

-	Layers:
	-	`sha256:3ffbc2e8833044834ccfc60c99f6275f3632718226c6ef0c9706b41890795123`  
		Last Modified: Mon, 09 Feb 2026 18:58:55 GMT  
		Size: 54.0 MB (54038228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffde5948ea75b47d8b1d783268ee006167908155c0b852232a68d3addb78f4e`  
		Last Modified: Tue, 10 Feb 2026 18:31:57 GMT  
		Size: 330.9 MB (330926190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de06fc41f06fb6b2eb6df0d5c157123af75f53a2c2f7e0c22bb8142f8a2de11`  
		Last Modified: Tue, 10 Feb 2026 19:07:56 GMT  
		Size: 65.4 MB (65363787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58b66f08c05c321fe51b3d85c521154cf0f372e31ce792f3bd6ea1de1f59a75`  
		Last Modified: Tue, 10 Feb 2026 19:07:52 GMT  
		Size: 1.9 KB (1942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a1553e9230ed94b6022672852b1109d34fdb1d7e95487b74a87c0e82c9cbf3`  
		Last Modified: Tue, 10 Feb 2026 19:07:57 GMT  
		Size: 128.5 MB (128469443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3eb4af1e670e54147d2454ce6dfd517684d707f1336ea1ad871cdede10e562d`  
		Last Modified: Tue, 10 Feb 2026 19:07:53 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:98fa7271b4af5844c94ea6baefbf6ce27d91b3ad23ff7b266733d17dd08065a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18084753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0afbf2ee6970a6de098c13d10f6097714dd1abc8c50861734a01454b74adbc3a`

```dockerfile
```

-	Layers:
	-	`sha256:2c492ed5abf3304e39b4a7afa3118422332d65914c43d88085d35e138dff360e`  
		Last Modified: Tue, 10 Feb 2026 19:07:54 GMT  
		Size: 18.1 MB (18063889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91ab2709ef70c8549fb0533dd478e39dd69a78da2b08b8f9824948ace74ccdb1`  
		Last Modified: Tue, 10 Feb 2026 19:07:52 GMT  
		Size: 20.9 KB (20864 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:fbaeaaf6ecd9b068ed49ece02ab6ec517f1ddb9505ac7a089fbefb7126754d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.9 MB (384911445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da21c5495f7cdbbf5e5086bd7e8897224a9c564800655dbdfbf4bdf4996500b`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:36 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:36 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:30:39 GMT
ARG version=1.8.0_482.b08-1
# Tue, 10 Feb 2026 18:30:39 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:30:39 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:30:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 10 Feb 2026 19:09:53 GMT
CMD ["gradle"]
# Tue, 10 Feb 2026 19:09:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 10 Feb 2026 19:09:53 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 10 Feb 2026 19:09:54 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 10 Feb 2026 19:09:54 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 10 Feb 2026 19:09:54 GMT
WORKDIR /home/gradle
# Tue, 10 Feb 2026 19:09:54 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 10 Feb 2026 19:09:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 10 Feb 2026 19:09:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 10 Feb 2026 19:09:56 GMT
USER gradle
# Tue, 10 Feb 2026 19:09:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 10 Feb 2026 19:09:57 GMT
USER root
```

-	Layers:
	-	`sha256:72831a4cffd207c00f002b53208af67cc59cf3af51b98b118c11c230a7926a2d`  
		Last Modified: Mon, 09 Feb 2026 20:01:25 GMT  
		Size: 52.9 MB (52918211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0baf47396438aac29add42cb10c2c15d95e93ce32ecd998e951f3511d5ac22`  
		Last Modified: Tue, 10 Feb 2026 18:30:59 GMT  
		Size: 118.0 MB (117959813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acc239d85f37e8f188f491cc3630445631cedec10877e780b95fce74a39b6e8`  
		Last Modified: Tue, 10 Feb 2026 19:10:27 GMT  
		Size: 85.5 MB (85502790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dd7cf483e45f0e27ec90e3cfb4250641eedd79f02779a1120d0ef45114e126`  
		Last Modified: Tue, 10 Feb 2026 19:10:24 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b778f805057e6a770b81cd3111f1d4c7d18a1c906fc74f045dc943381a7c0c6c`  
		Last Modified: Tue, 10 Feb 2026 19:10:28 GMT  
		Size: 128.5 MB (128469415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33de0f74a8c9eed58d2f6cf95e71bca548dd3d17f70c4bd64f282c97bb7936e1`  
		Last Modified: Tue, 10 Feb 2026 19:10:24 GMT  
		Size: 59.5 KB (59531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:097b8952f9e009e5b8493ecefdc3836b83e3405f9a3a1646546bb866c08362fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11649086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbc7fbb1bd807c19b96c2b18cd24d2dfe7c042e723d43c6e5eb0683ab979395`

```dockerfile
```

-	Layers:
	-	`sha256:ff1a77ede2032ca8b7f4c4eda45f65a9e936ad582d0b50b522ca9f6ab4676b50`  
		Last Modified: Tue, 10 Feb 2026 19:10:25 GMT  
		Size: 11.6 MB (11628049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e22bd48244909d9f91709da5f80a7a9116f239f6668f71e7508830eb776f8c75`  
		Last Modified: Tue, 10 Feb 2026 19:10:24 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json
