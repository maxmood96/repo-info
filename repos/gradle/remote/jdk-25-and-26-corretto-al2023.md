## `gradle:jdk-25-and-26-corretto-al2023`

```console
$ docker pull gradle@sha256:27959fe892c9a72f10f3985a469a178087026806903ccd6eaec8721383c977a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-25-and-26-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:c2acd2ac93717fb8eb4672bf67b156ca20bb066c1edf473e4de52564d887ddd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.9 MB (646947204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3bd316f3671a62b54b248f3d10e69a458cc31fef9b24c4ca51c6abe0fbc7793`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:26:44 GMT
ARG version=25.0.2.10-1
# Wed, 15 Apr 2026 21:26:44 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:26:44 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:26:44 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:26:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 15 Apr 2026 22:17:24 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Wed, 15 Apr 2026 22:17:44 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 15 Apr 2026 22:17:44 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Wed, 15 Apr 2026 22:17:44 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 22:17:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 22:17:44 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 22:17:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Wed, 15 Apr 2026 22:17:44 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 22:17:44 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 22:17:44 GMT
ENV GRADLE_VERSION=9.4.1
# Wed, 15 Apr 2026 22:17:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Wed, 15 Apr 2026 22:17:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 22:17:47 GMT
USER gradle
# Wed, 15 Apr 2026 22:17:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 15 Apr 2026 22:17:47 GMT
USER root
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1ea217645c100a6a722630601c1c84cdadb45351d90b7a9d6e48270865321b`  
		Last Modified: Wed, 15 Apr 2026 21:27:09 GMT  
		Size: 189.2 MB (189188253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3910f641f04d974bad04e5e8934e9b86a4f787459f78996191ade39651526a99`  
		Last Modified: Wed, 15 Apr 2026 22:18:35 GMT  
		Size: 179.2 MB (179246165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30b1d5b9a86c812c063ae6d252ffe8fa454021e39e6cedbbde5bcf989a375f7`  
		Last Modified: Wed, 15 Apr 2026 22:18:31 GMT  
		Size: 86.1 MB (86105805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dab6fcdd5190a46f6b99c908871249a03d248d83c88163c63d0ee870f3b7f52`  
		Last Modified: Wed, 15 Apr 2026 22:18:25 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f33ad2b81777903e887dab71d1927e42639f19cb1c00c47bf24d472ead3c254`  
		Last Modified: Wed, 15 Apr 2026 22:18:34 GMT  
		Size: 137.8 MB (137808336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032293160c72e8856f2dcb8a1ac2e2e94c85debe2401a61cd53e25ff9980bed4`  
		Last Modified: Wed, 15 Apr 2026 22:18:27 GMT  
		Size: 25.6 KB (25602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-25-and-26-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:9ce0c7024eeb661180394034edf9a8a0f5723b35a63fb225fb1b6d8ddf186ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11542919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30ae1f928bbcdcbb512d772b492fc6811d8e8b897fc43e5fc9bfae90f758cf6`

```dockerfile
```

-	Layers:
	-	`sha256:927fabe31ee1e9bef1870ddbdb7eaaab9aa5fa75a2533809b626c5d7cfa724a5`  
		Last Modified: Wed, 15 Apr 2026 22:18:27 GMT  
		Size: 11.5 MB (11513410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d25b18fcd957fbc8cc520bcedb3ac7573f25ff05559dec22f029ddc8a2ba8e74`  
		Last Modified: Wed, 15 Apr 2026 22:18:25 GMT  
		Size: 29.5 KB (29509 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-25-and-26-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:699c694ab67ec4217fb708fc87929f828edf2cd63dc4317386bca0d94d6739f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.1 MB (641090393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45227ac331ccc793df3d4404fcb93b0ab6a5912cf1236e244cbb77d6117cae0`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:39:50 GMT
ARG version=25.0.2.10-1
# Wed, 15 Apr 2026 21:39:50 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:39:50 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:39:50 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:39:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 15 Apr 2026 22:29:45 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Wed, 15 Apr 2026 22:30:10 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 15 Apr 2026 22:30:10 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Wed, 15 Apr 2026 22:30:10 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 22:30:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 22:30:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 22:30:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Wed, 15 Apr 2026 22:30:10 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 22:30:10 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 22:30:10 GMT
ENV GRADLE_VERSION=9.4.1
# Wed, 15 Apr 2026 22:30:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Wed, 15 Apr 2026 22:30:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 22:30:13 GMT
USER gradle
# Wed, 15 Apr 2026 22:30:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 15 Apr 2026 22:30:13 GMT
USER root
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97e5eaff5c173c2d572c7ece0a4ad5d4ba6d11aa38fa3b123836e74ff874e0f`  
		Last Modified: Wed, 15 Apr 2026 21:40:18 GMT  
		Size: 187.1 MB (187089832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e909887d2547ebf21f1842e61f14b59c5cd31c7553ed39b0ac1db00fe4f3a2`  
		Last Modified: Wed, 15 Apr 2026 22:30:57 GMT  
		Size: 177.1 MB (177115713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a996a260be26d3e2ab18163183bd9530068e1770776b9b8f63c5bf78e5a6dcaa`  
		Last Modified: Wed, 15 Apr 2026 22:30:54 GMT  
		Size: 85.6 MB (85602662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1357a4df54d76afc78c708547de2908ff3fc11deb65bbe0fcda872aa6957e6`  
		Last Modified: Wed, 15 Apr 2026 22:30:50 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98403334571fcdb888acda0647f47fef4c60cabe838f16db97487cc31530cf45`  
		Last Modified: Wed, 15 Apr 2026 22:30:56 GMT  
		Size: 137.8 MB (137808331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283eea40cfceb6e7a17254c8e8a2ce3a0c4bcdeca482c53ce8b6c2e7540772ba`  
		Last Modified: Wed, 15 Apr 2026 22:30:51 GMT  
		Size: 29.3 KB (29326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-25-and-26-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:23e0f7e378eb207a92ca6c0c5684f9dd600a8239a1e3f7175519319db2610c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11541708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1397b25d95fb942f7c627bed2301f8888279a87022eabfdea9cf47379a42fa6e`

```dockerfile
```

-	Layers:
	-	`sha256:13d575af00ff4129e44af679de70597d35f4a8c9e46e9900ee5f36d5dd10ab5f`  
		Last Modified: Wed, 15 Apr 2026 22:30:51 GMT  
		Size: 11.5 MB (11511879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:781ae5514f70be4631e33888b73812f6738c5a77acf6af494158a1fb6e1b2fe4`  
		Last Modified: Wed, 15 Apr 2026 22:30:50 GMT  
		Size: 29.8 KB (29829 bytes)  
		MIME: application/vnd.in-toto+json
