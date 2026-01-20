## `gradle:jdk-25-and-25-corretto`

```console
$ docker pull gradle@sha256:5f2dd1b31f7227e35930494602b0e49c0bb94bfc76a3fbbf2a23fcaf68cbfa98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-25-and-25-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:57241b88c2131b6a2acab6f8ed0af25a75e7d836b5a6868a78cf0d0fd078a1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.2 MB (466211647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61950306c4fa098a4beb44c8f582fd606896008db123fda5c1375223444c4036`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:13 GMT
ARG version=25.0.1.9-1
# Thu, 15 Jan 2026 22:10:13 GMT
ARG package_version=1
# Thu, 15 Jan 2026 22:10:13 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:10:13 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:10:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 16 Jan 2026 21:47:33 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 16 Jan 2026 21:47:33 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 16 Jan 2026 21:47:33 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:47:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:47:33 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 16 Jan 2026 21:47:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 16 Jan 2026 21:47:33 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:47:33 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:47:33 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:47:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:47:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:47:35 GMT
USER gradle
# Fri, 16 Jan 2026 21:47:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:47:36 GMT
USER root
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:09:37 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d88fe3c4b256f3e9e43b9cb5ec26a56a3f9a83b14d7daf8a3ab39250d61c86`  
		Last Modified: Thu, 15 Jan 2026 22:10:37 GMT  
		Size: 189.1 MB (189137832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0c350cb483370d69561566b71f23f4121757e057506387f3151c7310a1f5e0`  
		Last Modified: Fri, 16 Jan 2026 21:48:23 GMT  
		Size: 86.0 MB (86036356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae0ef20ebdf480d70156a4550d6be72e68b0a3145364db4cc43b149df7af0ea`  
		Last Modified: Fri, 16 Jan 2026 21:48:12 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2554e7c4869dd4aaeab71d08daa7c1b3696c5ab85191dd2ab92ec85bfe88842e`  
		Last Modified: Sat, 17 Jan 2026 19:20:32 GMT  
		Size: 137.0 MB (136988870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f570bacb2059372cca55b40f45a57e61ede2b0881db7892928b22de5fca39d`  
		Last Modified: Fri, 16 Jan 2026 21:48:12 GMT  
		Size: 25.6 KB (25595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-25-and-25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:365a589d88e93f1cd3b49516fcfa33832ac134ea889b42451d59d553598055b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11367128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c15ff9e19e24455d7ea0491c801470ca6ef50b4b1e6427108636462aa45b95`

```dockerfile
```

-	Layers:
	-	`sha256:f7e8c028471970b57d5190afc3bcb75d3466fff933fea158fd9f804e689a9586`  
		Last Modified: Sat, 17 Jan 2026 00:22:24 GMT  
		Size: 11.3 MB (11340651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bf43f1e55350bf9f7b9b5c9f18f16a4938b180cf78b4c99202ff2c5608dd7b`  
		Last Modified: Sat, 17 Jan 2026 00:22:25 GMT  
		Size: 26.5 KB (26477 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-25-and-25-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:421abae53ca5f49a67d6d97f269a65f0a07f7e50e608b701476162d23c4784d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.5 MB (462511142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9465c04acc86d2fe8fff7bab46714fc851a3d11d2de12fd325aa0177d0de452d`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:20 GMT
ARG version=25.0.1.9-1
# Thu, 15 Jan 2026 22:10:20 GMT
ARG package_version=1
# Thu, 15 Jan 2026 22:10:20 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:10:20 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:10:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 16 Jan 2026 21:47:24 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 16 Jan 2026 21:47:24 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 16 Jan 2026 21:47:24 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:47:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:47:24 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 16 Jan 2026 21:47:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 16 Jan 2026 21:47:24 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:47:24 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:47:24 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:47:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:47:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:47:26 GMT
USER gradle
# Fri, 16 Jan 2026 21:47:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:47:27 GMT
USER root
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:25 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506418744a0e688a95c939f508921fc21e961eb25ec4bf5c8550b47aee8f9d3e`  
		Last Modified: Thu, 15 Jan 2026 22:52:34 GMT  
		Size: 187.1 MB (187059433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91edce49067b8740644cacf2b669bacda50ad41ed690c09521b3bab4ba5ebee`  
		Last Modified: Fri, 16 Jan 2026 21:48:01 GMT  
		Size: 85.5 MB (85517384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec7c550e8574e63567c814059734cd0e0bf31d9dcedf157916447da10532854`  
		Last Modified: Fri, 16 Jan 2026 21:48:12 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c03945396134a0670a2463063ecb244f5ab40f6fd3d194df8450ad17dac638`  
		Last Modified: Sun, 18 Jan 2026 09:26:21 GMT  
		Size: 137.0 MB (136988870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa47346277ec57c3af2cd76b0ba5907678c6aa2b85617fe58e79c1c6def2cf88`  
		Last Modified: Fri, 16 Jan 2026 21:47:55 GMT  
		Size: 29.3 KB (29312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-25-and-25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:cece704c7238ebe689c47d9041fd80583843b29317c881097f4df4de21dc3dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11366529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801e20a648bc89984eea745595e67b2e503b51288ae6ab675fdd039af2072877`

```dockerfile
```

-	Layers:
	-	`sha256:ebd8c0796a23f9d73a41b005dd762fd936e0f61d7ca2afaeb4b3b18afb95c5ac`  
		Last Modified: Sat, 17 Jan 2026 00:22:37 GMT  
		Size: 11.3 MB (11339760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dbc3751c267527327f902d4047aa2f329ef78d4440fad3e8de3343b63e2856c`  
		Last Modified: Sat, 17 Jan 2026 00:22:38 GMT  
		Size: 26.8 KB (26769 bytes)  
		MIME: application/vnd.in-toto+json
