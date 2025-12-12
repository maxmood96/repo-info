## `gradle:jdk-25-and-25-corretto`

```console
$ docker pull gradle@sha256:cf21ea4e0e2f4493896570dbabc2d1809ef97b5b51fe032e93065691f5da1506
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-25-and-25-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:9d4b448f47e7025ce3232405f27523f2c0b8c5ec3ff5825c1b3024276f6c4dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.7 MB (464723215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f435ed5a10fb1cfdd9c4e656f8df3492231f9b3ca2d11beefa6fab5023aac25`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:09 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:09 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:13:21 GMT
ARG version=25.0.1.9-1
# Thu, 11 Dec 2025 22:13:21 GMT
ARG package_version=1
# Thu, 11 Dec 2025 22:13:21 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:13:21 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:13:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 11 Dec 2025 22:17:23 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 11 Dec 2025 22:17:23 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 11 Dec 2025 22:17:23 GMT
CMD ["gradle"]
# Thu, 11 Dec 2025 22:17:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 11 Dec 2025 22:17:23 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 11 Dec 2025 22:17:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 11 Dec 2025 22:17:23 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 11 Dec 2025 22:17:23 GMT
WORKDIR /home/gradle
# Thu, 11 Dec 2025 22:17:23 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 11 Dec 2025 22:17:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 11 Dec 2025 22:17:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 11 Dec 2025 22:17:25 GMT
USER gradle
# Thu, 11 Dec 2025 22:17:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 11 Dec 2025 22:17:26 GMT
USER root
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91413819017580b0cad6a6036474dd8d9101d5528fc612f3e8b639ab91f6de1b`  
		Last Modified: Thu, 11 Dec 2025 22:17:29 GMT  
		Size: 189.1 MB (189138728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cd44cd27843952ac670c142ecb803787cb858b358d73c41260bac27dfa1be5`  
		Last Modified: Thu, 11 Dec 2025 22:18:09 GMT  
		Size: 86.0 MB (86017381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4176be9806fe115fa968e88891572f248783c55097d32840ce20713db80f3863`  
		Last Modified: Thu, 11 Dec 2025 22:18:00 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808da3f3bb3d0676040df3a7c6f1de44c0d8e42533f87a1af251dea988f11f91`  
		Last Modified: Thu, 11 Dec 2025 22:38:20 GMT  
		Size: 135.5 MB (135521964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f81c330ac104741b435055e1b8d7dba01f475c318df2e9a91ba1a389de74c98`  
		Last Modified: Thu, 11 Dec 2025 22:18:00 GMT  
		Size: 54.9 KB (54896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-25-and-25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:23d2b73126b8ace8d2c7415cbaab8e1225502409a8b3a69e5c1d0efa037e6100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11378164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be2a96c4cc398926365d17b363aacd3c465b0c200210239cd31b1b4323c75ea`

```dockerfile
```

-	Layers:
	-	`sha256:4bc57aecab50196f4e250d5a45e0dc7a8b390a8f0f7e67c9bfaca2d40024ab99`  
		Last Modified: Fri, 12 Dec 2025 00:23:02 GMT  
		Size: 11.4 MB (11351687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94ee5f81b4878b25ff5f8b45886a509458ed400f535619c04fd917f6cf896991`  
		Last Modified: Fri, 12 Dec 2025 00:23:03 GMT  
		Size: 26.5 KB (26477 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-25-and-25-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:06b1ed8bf51df4789ca54cebbd44aeac82847c9fc42ab5c516e84a5a9a47ed67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.0 MB (461038785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2d213ed300dc5aa239b1bd338281b89049909b4a8bd14195db269d03abd9f0`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 11 Dec 2025 21:45:58 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:45:58 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:13:00 GMT
ARG version=25.0.1.9-1
# Thu, 11 Dec 2025 22:13:00 GMT
ARG package_version=1
# Thu, 11 Dec 2025 22:13:00 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:13:00 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:13:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 11 Dec 2025 22:18:11 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 11 Dec 2025 22:18:11 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 11 Dec 2025 22:18:11 GMT
CMD ["gradle"]
# Thu, 11 Dec 2025 22:18:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 11 Dec 2025 22:18:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 11 Dec 2025 22:18:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 11 Dec 2025 22:18:12 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 11 Dec 2025 22:18:12 GMT
WORKDIR /home/gradle
# Thu, 11 Dec 2025 22:18:12 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 11 Dec 2025 22:18:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 11 Dec 2025 22:18:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 11 Dec 2025 22:18:14 GMT
USER gradle
# Thu, 11 Dec 2025 22:18:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 11 Dec 2025 22:18:15 GMT
USER root
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddfd06178dcdca2a5cd3684d7be72c33b03527be5f3cd9c8aa6e0db1f16ac0b`  
		Last Modified: Thu, 11 Dec 2025 22:35:49 GMT  
		Size: 187.1 MB (187059439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e464cca9957e10d388447a539bbe37fdaa85bdce88d2ff67c8330327a2232c6f`  
		Last Modified: Thu, 11 Dec 2025 22:19:13 GMT  
		Size: 85.5 MB (85522616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d779e1c1c7feeae482420e85c203e443761e22e2053b664b5bbf3d51d926ff`  
		Last Modified: Thu, 11 Dec 2025 22:18:52 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125a6c9f03e6c1f13d9b552d0deb1ede0a35e1a7af8a7d2a80d3532291741c06`  
		Last Modified: Thu, 11 Dec 2025 22:37:16 GMT  
		Size: 135.5 MB (135521960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64dd9f85e71012870def7df5b0c9a20162ed14c1549004ad7dcf6248f940d8f`  
		Last Modified: Thu, 11 Dec 2025 22:37:11 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-25-and-25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:228d92f88066c3cc15466d1962f40693984e3e0f8e64a085ad56badd88e047f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11377566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ead4612c8c8542121d5b908bb634dce89c8529ac3e96ee336d3fe07075515d`

```dockerfile
```

-	Layers:
	-	`sha256:f90df20f7c643c6db475d08a660100f2b4b754c7bc55d3c2c0c22c2a518081b4`  
		Last Modified: Fri, 12 Dec 2025 00:23:13 GMT  
		Size: 11.4 MB (11350796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:801fa30397b10c84f4e0fda56234a80212d45a218daa683be916fc26be5c45bf`  
		Last Modified: Fri, 12 Dec 2025 00:23:14 GMT  
		Size: 26.8 KB (26770 bytes)  
		MIME: application/vnd.in-toto+json
