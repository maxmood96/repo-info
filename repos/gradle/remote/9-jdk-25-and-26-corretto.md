## `gradle:9-jdk-25-and-26-corretto`

```console
$ docker pull gradle@sha256:56daee4377105cd7ac3d76bee1e976906d28ed5b119622aa60df27bcd0d380fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-25-and-26-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:dcb3df3744a889238530a77e665a04359fc8805cce681aed23a490d27f40569d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.7 MB (649668823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8fd61ab18f8c729f5d57ef990f792c7b656d1f1dc1c404b5aa2147eef2ec48`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:13:06 GMT
ARG version=25.0.3.9-1
# Mon, 04 May 2026 20:13:06 GMT
ARG package_version=1
# Mon, 04 May 2026 20:13:06 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:13:06 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:13:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 04 May 2026 20:41:39 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Mon, 04 May 2026 20:41:58 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 04 May 2026 20:41:58 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Mon, 04 May 2026 20:41:58 GMT
CMD ["gradle"]
# Mon, 04 May 2026 20:41:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 04 May 2026 20:41:58 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 04 May 2026 20:41:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 04 May 2026 20:41:59 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 04 May 2026 20:41:59 GMT
WORKDIR /home/gradle
# Mon, 04 May 2026 20:41:59 GMT
ENV GRADLE_VERSION=9.5.0
# Mon, 04 May 2026 20:41:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Mon, 04 May 2026 20:42:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 04 May 2026 20:42:01 GMT
USER gradle
# Mon, 04 May 2026 20:42:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 04 May 2026 20:42:02 GMT
USER root
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16eb8b7b35c1b74a9914e9b34dbeae7f97d7de3034c781a050bbb7c92e7a13ae`  
		Last Modified: Mon, 04 May 2026 20:13:28 GMT  
		Size: 189.4 MB (189410977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fdc5099c878cb00871fd98d4a93b174196d17bcd4e84a105b0e3d7f9434248`  
		Last Modified: Mon, 04 May 2026 20:42:42 GMT  
		Size: 179.2 MB (179247471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b84d19a6fbe90e71b5306ea5a6c177a63db05255063b6aa4070cafe777a994`  
		Last Modified: Mon, 04 May 2026 20:42:39 GMT  
		Size: 86.2 MB (86170285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091755f391b5d521653cfbaf745b65b1aaa8e6a93a541b46db235c3b05dd076b`  
		Last Modified: Mon, 04 May 2026 20:42:33 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24716b81eefd33ad66e2e33e7de761ffe3ca92605ff272523b294b5bc1e3a558`  
		Last Modified: Mon, 04 May 2026 20:42:41 GMT  
		Size: 140.2 MB (140235938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981dce73911fb94eed36d5394ff6d1a1cfbad1072c17ce2b4d4959e5bcf6f416`  
		Last Modified: Mon, 04 May 2026 20:42:35 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-26-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:21964ec243db97a158f03342d37e6bd9623eda88c5b54e3a420d723c2a9a4194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11574153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66eb8fbfc73998deab21a2424944ca27f795d1edd6bd4da71e256f698d24e80c`

```dockerfile
```

-	Layers:
	-	`sha256:fd774acd76e9ba5d5ccc99880e15647d5ded390373da745592a064ebae53d895`  
		Last Modified: Mon, 04 May 2026 20:42:35 GMT  
		Size: 11.5 MB (11544643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7ec989dc7119f14fb92daed87dac7fc8efe1f95ec503f1aaccccc90f5640fda`  
		Last Modified: Mon, 04 May 2026 20:42:34 GMT  
		Size: 29.5 KB (29510 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-25-and-26-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8fd6a7acee4962edd75075f35c51b96bf7cbcae4f287d6e6030b29dfaeb3e362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.8 MB (643838357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf56005c10897fb69504df7f72044724b56a1540675bdc1454063e4404c818f`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:40 GMT
ARG version=25.0.3.9-1
# Mon, 04 May 2026 20:12:40 GMT
ARG package_version=1
# Mon, 04 May 2026 20:12:40 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:12:40 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 04 May 2026 20:41:36 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Mon, 04 May 2026 20:41:59 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 04 May 2026 20:41:59 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Mon, 04 May 2026 20:41:59 GMT
CMD ["gradle"]
# Mon, 04 May 2026 20:41:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 04 May 2026 20:41:59 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 04 May 2026 20:42:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 04 May 2026 20:42:00 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 04 May 2026 20:42:00 GMT
WORKDIR /home/gradle
# Mon, 04 May 2026 20:42:00 GMT
ENV GRADLE_VERSION=9.5.0
# Mon, 04 May 2026 20:42:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Mon, 04 May 2026 20:42:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 04 May 2026 20:42:02 GMT
USER gradle
# Mon, 04 May 2026 20:42:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 04 May 2026 20:42:03 GMT
USER root
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fb91f40f3222452d1657188531de5c0a6d13a45344c5ceb4ea6aab586cf782`  
		Last Modified: Mon, 04 May 2026 20:13:06 GMT  
		Size: 187.3 MB (187331106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f07b021cc1442763e460c244364a4783b436e3ae2c703421fc53879acfc0e6`  
		Last Modified: Mon, 04 May 2026 20:42:44 GMT  
		Size: 177.1 MB (177119377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db47057eaae97b73bf94ccf7f34b5cc182c8a6706665ff7934cc316a352e3794`  
		Last Modified: Mon, 04 May 2026 20:42:41 GMT  
		Size: 85.7 MB (85664040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96450f47e1464826714a04b0904a53e49ec46425ed4170d0f9ebff7eb6c39617`  
		Last Modified: Mon, 04 May 2026 20:42:35 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723eedd7471b9dae34587e3ef0fd29d60d142285b1f2d27d7286744884a32145`  
		Last Modified: Mon, 04 May 2026 20:42:43 GMT  
		Size: 140.2 MB (140235937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f56d9edfa89f68d99d39b597fcf31318808abaca284dcf4f08f1c278f0d496f`  
		Last Modified: Mon, 04 May 2026 20:42:37 GMT  
		Size: 29.3 KB (29335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-26-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:3fd92a27951361430f9852d679da989c87d6c963b76cace37278d44b6187af8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11572942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878a072aeff348b13473e4fbab5eaec368285f98834721a0a68c6275b881c897`

```dockerfile
```

-	Layers:
	-	`sha256:271997aa4334b529c5bb4e24f1f2aeea40586fddff7529aea0d6afc7fc1749d2`  
		Last Modified: Mon, 04 May 2026 20:42:36 GMT  
		Size: 11.5 MB (11543113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b63a22057c4c5fa0c25e29308758f9f517b2f35fa52e127a466814da29e5b08`  
		Last Modified: Mon, 04 May 2026 20:42:35 GMT  
		Size: 29.8 KB (29829 bytes)  
		MIME: application/vnd.in-toto+json
