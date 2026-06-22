## `gradle:jdk-lts-and-current-corretto`

```console
$ docker pull gradle@sha256:682985e08340a85f73f8dab7fa76503785d4a62a1cbc0713e49d195cf9540541
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-lts-and-current-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:6a1e8e8a7150d677fac4edb793c623268d75728ebfd4543e7c3f5c93cb7f3f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.5 MB (650503863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b5a0c2148bcf3f2b323bea3e540b5a30469c8babbac3d44e05b22c90c1a79c`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:15 GMT
ARG version=25.0.3.9-1
# Mon, 22 Jun 2026 18:05:15 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:05:15 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:15 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 22 Jun 2026 18:15:04 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Mon, 22 Jun 2026 18:15:23 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 22 Jun 2026 18:15:23 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Mon, 22 Jun 2026 18:15:23 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:15:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:15:23 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:15:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 22 Jun 2026 18:15:23 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:15:23 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:15:23 GMT
ENV GRADLE_VERSION=9.6.0
# Mon, 22 Jun 2026 18:15:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
# Mon, 22 Jun 2026 18:15:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:15:26 GMT
USER gradle
# Mon, 22 Jun 2026 18:15:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 22 Jun 2026 18:15:27 GMT
USER root
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9187d1c0652a3fc2e5587c51e615fc4dcfb4ee369050a626cc0c5f8763605ac`  
		Last Modified: Mon, 22 Jun 2026 18:05:41 GMT  
		Size: 189.4 MB (189413466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff80b524f027350ee5a3a123a64b9612c455e00c4e986125fa3e8325815ae69`  
		Last Modified: Mon, 22 Jun 2026 18:16:07 GMT  
		Size: 179.2 MB (179247445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebaaa7160836f5e7e7fda455cbabd628cbf298688735c1febc5fe4aef742ed9`  
		Last Modified: Mon, 22 Jun 2026 18:16:04 GMT  
		Size: 86.6 MB (86646263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832f7d1a8e705cb8d42102e2d2113e131091d9c26116efeef93fa31b3926644a`  
		Last Modified: Mon, 22 Jun 2026 18:15:57 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4e93cb6d855bdb3cfb34da26ec8db0b8263ac47f97e3129667dec460e6a550`  
		Last Modified: Mon, 22 Jun 2026 18:16:06 GMT  
		Size: 140.6 MB (140595104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2654e3b6cd6ad313d1d4b715d5f54524ec115bd3130b916d80d91ca9ac9b3e`  
		Last Modified: Mon, 22 Jun 2026 18:15:59 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:4bc3c1c13c663ac839e426786db520fadfbb1f6b0130117ea00b7a874b470cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11591126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21ff1f87072dd1f379f9b3eff1619b1d39e89cdfa28146e78802f2ec8d5ce01`

```dockerfile
```

-	Layers:
	-	`sha256:7c3eb199a66a7f2701df0b84e0c2ca9a965e1d80933254bd33c9a040ca26eaa9`  
		Last Modified: Mon, 22 Jun 2026 18:15:58 GMT  
		Size: 11.6 MB (11561616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e16780929119eebdf383a8a9651b54903a1438ecf1514bbc623ed9f6c2b04927`  
		Last Modified: Mon, 22 Jun 2026 18:15:58 GMT  
		Size: 29.5 KB (29510 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:79bc675195c1319406c257be837797924071fd2446e59101408bfbe52020020d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.6 MB (644561702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d714815cbfbd6caee15a91d91f3e201c1e23c772a78244e1d50559b55adc47a`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:15:33 GMT
ARG version=25.0.3.9-1
# Mon, 22 Jun 2026 18:15:33 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:15:33 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:15:33 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:15:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 22 Jun 2026 18:26:51 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Mon, 22 Jun 2026 18:27:15 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 22 Jun 2026 18:27:15 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Mon, 22 Jun 2026 18:27:15 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:27:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:27:15 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:27:15 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 22 Jun 2026 18:27:15 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:27:15 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:27:15 GMT
ENV GRADLE_VERSION=9.6.0
# Mon, 22 Jun 2026 18:27:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
# Mon, 22 Jun 2026 18:27:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:27:18 GMT
USER gradle
# Mon, 22 Jun 2026 18:27:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 22 Jun 2026 18:27:18 GMT
USER root
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4f1006a54abcd81b4b8010a4470cc0f1ddc33b2dd4191d1661555e3275be62`  
		Last Modified: Mon, 22 Jun 2026 18:15:59 GMT  
		Size: 187.3 MB (187328296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828f48f73abdd63b4ef9f94e8d8921125a63ca85b8a67986cdaedea19bcb5941`  
		Last Modified: Mon, 22 Jun 2026 18:28:00 GMT  
		Size: 177.1 MB (177119325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a233d0604a312c2ec5f7bd84bc5f9718aa1ee5387259d54d32ccf54e63039a`  
		Last Modified: Mon, 22 Jun 2026 18:27:57 GMT  
		Size: 86.0 MB (86037174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a545217e7a0ffe7908669f94612852b87e9c6640f75a7b30d133c133322e546`  
		Last Modified: Mon, 22 Jun 2026 18:27:51 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d1f3875ac06fc98341cce0226b47baab5f080e126e71fc946b241f9a19d605`  
		Last Modified: Mon, 22 Jun 2026 18:27:58 GMT  
		Size: 140.6 MB (140595105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbd04cac53de8fe088d581bfdff89b6d47ca42b8678e87a4826405d03cfe001`  
		Last Modified: Mon, 22 Jun 2026 18:27:53 GMT  
		Size: 29.3 KB (29327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:84c01c3bf8a678ae1970b652f08b1183a638a0510329522a3debd7006bba45dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11589914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544448a46e098b71e31f08cadb5bb252338ffb6bd1bf562d810d3c4def47f527`

```dockerfile
```

-	Layers:
	-	`sha256:5cb5800c407b136059728e95256bb947e6655169e06af8b2234054c486892294`  
		Last Modified: Mon, 22 Jun 2026 18:27:52 GMT  
		Size: 11.6 MB (11560086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02002cd91dc48e882958734e48fc11a943b8ae6bcef3e8b90513baca7ee89ec8`  
		Last Modified: Mon, 22 Jun 2026 18:27:51 GMT  
		Size: 29.8 KB (29828 bytes)  
		MIME: application/vnd.in-toto+json
