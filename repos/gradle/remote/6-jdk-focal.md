## `gradle:6-jdk-focal`

```console
$ docker pull gradle@sha256:09504127b92bdb12998efbe0f981888c1f80f33b93a5eebfb04471bbb43caec3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gradle:6-jdk-focal` - linux; amd64

```console
$ docker pull gradle@sha256:f976b03d7fab76801acce91f5f63a968a1bb1e85239d0d80653fba6593436efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.0 MB (366992673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824800f587bf1b2d8c1b6dc1187a9f0ba85afda7c70b8f2d5084ad6c1ab028d8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='5eb00b18e37757775e6f46c706eae38d9e91be49de5712987801cba8ffd77767';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Thu, 29 May 2025 19:34:11 GMT
CMD ["gradle"]
# Thu, 29 May 2025 19:34:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 29 May 2025 19:34:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 29 May 2025 19:34:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 29 May 2025 19:34:11 GMT
WORKDIR /home/gradle
# Thu, 29 May 2025 19:34:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 29 May 2025 19:34:11 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 29 May 2025 19:34:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 29 May 2025 19:34:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 29 May 2025 19:34:11 GMT
USER gradle
# Thu, 29 May 2025 19:34:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 29 May 2025 19:34:11 GMT
USER root
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2990f2ec4f6cc8c74bc08632aa6ae84b2e5da5d73a4ceb4aec2bb4fff1a1a6b`  
		Last Modified: Wed, 23 Apr 2025 16:32:02 GMT  
		Size: 20.3 MB (20260573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f523acdfc02687aaadb32d1cfd1cbb7b1ddded9196c778ce861911356514121`  
		Last Modified: Wed, 23 Apr 2025 16:32:05 GMT  
		Size: 145.6 MB (145643714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c842fad8a44bf7264fbb843b1cd9ce799f2dd4b83d3af89a610fc4158ffedaa4`  
		Last Modified: Wed, 23 Apr 2025 16:32:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c2dfaad4ab404d3d81612a2e724ff25aebba209b94a1b95875374a03a94e10`  
		Last Modified: Wed, 23 Apr 2025 16:32:01 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad079e710d4b636cd050ca8a0c9c87424506ae97437151486b1fcc229373e59a`  
		Last Modified: Mon, 02 Jun 2025 16:49:01 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28e1c722e4939a79807cb94b5951406ef3afb952ac92df0dd32d07a64ecd876`  
		Last Modified: Mon, 02 Jun 2025 16:49:03 GMT  
		Size: 65.4 MB (65443274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcabfc5ca0bf93ee24dd45f1d680466e2b8737ad3162f2a9df66ffb0a9d6791`  
		Last Modified: Mon, 02 Jun 2025 16:49:04 GMT  
		Size: 107.7 MB (107696649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f32ae79dce65299cfd95f0ba7950dd455c551c980d660986e66857485b1b4e`  
		Last Modified: Mon, 02 Jun 2025 16:49:02 GMT  
		Size: 431.3 KB (431279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:b4c5ad4922015f4b2387f9bcd6c41cd7fa01a4a05c50810b8dceae95c884839e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7809206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c93e45bebeb61f9fa655c68fc82a1e087941196ef7fcbd74095de40b2227863`

```dockerfile
```

-	Layers:
	-	`sha256:214c463eb7474b0620e50f0def965e895428bc3c7a8daaedd91e53fd8ae3241d`  
		Last Modified: Mon, 02 Jun 2025 16:49:02 GMT  
		Size: 7.8 MB (7784420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9647b0a1568c6d47bfe38c81f84bfe8d1f90ec580cea6bdb0c38cb7067c01a71`  
		Last Modified: Mon, 02 Jun 2025 16:49:01 GMT  
		Size: 24.8 KB (24786 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk-focal` - linux; arm variant v7

```console
$ docker pull gradle@sha256:fc350161c476fdbbdc87f897f5e782258bb3192f2e5decc90a047547cd60a3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.0 MB (348045967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302226c11b93e79d51d6055078f183c1699c9f98cd0ee8491e8ff53d73b9c4d7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 08 Apr 2025 10:45:56 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:45:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:45:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:45:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:45:59 GMT
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
# Tue, 08 Apr 2025 10:45:59 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='5eb00b18e37757775e6f46c706eae38d9e91be49de5712987801cba8ffd77767';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Thu, 29 May 2025 19:34:11 GMT
CMD ["gradle"]
# Thu, 29 May 2025 19:34:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 29 May 2025 19:34:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 29 May 2025 19:34:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 29 May 2025 19:34:11 GMT
WORKDIR /home/gradle
# Thu, 29 May 2025 19:34:11 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 29 May 2025 19:34:11 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 29 May 2025 19:34:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 29 May 2025 19:34:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 29 May 2025 19:34:11 GMT
USER gradle
# Thu, 29 May 2025 19:34:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 29 May 2025 19:34:11 GMT
USER root
```

-	Layers:
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Tue, 08 Apr 2025 11:48:35 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584dcd1f0ae60202572ceaaf1d1ff21ed62161827b256dfd50433bbcba261dfd`  
		Last Modified: Wed, 09 Apr 2025 11:38:16 GMT  
		Size: 18.5 MB (18478140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a9aaf9f795beb05b576a0533456c6b4111eac7b69e323d47a8a7537f4133e9`  
		Last Modified: Wed, 23 Apr 2025 17:02:48 GMT  
		Size: 138.1 MB (138116955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edebee74a587fe1c5dc840dd7f05f2a7ad9ea7b43be2568102be4d13bfae7d6e`  
		Last Modified: Wed, 23 Apr 2025 17:02:44 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275c208356b87a2f3a2db69768b8806c25cde8a4b4d5dd66e43262128771acbf`  
		Last Modified: Wed, 23 Apr 2025 17:02:44 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96237c055b50345022c81a9138cfd0960dcbccf08e39a9944ce744025ac4c48f`  
		Last Modified: Tue, 27 May 2025 21:10:59 GMT  
		Size: 4.3 KB (4298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdafef3a88edb71f884050fc5722a40262aec6ed000646e3aa2bdd349d776f1b`  
		Last Modified: Mon, 02 Jun 2025 16:55:12 GMT  
		Size: 60.1 MB (60092092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585b63efee0fd330c226dd56304254a1ddac9141a908941cd74b855bdc513a29`  
		Last Modified: Mon, 02 Jun 2025 17:05:53 GMT  
		Size: 107.7 MB (107696670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af92d2170c05fba0ba16db3d3db35b24c22d20ad14109402da84295c6df4130`  
		Last Modified: Mon, 02 Jun 2025 17:05:50 GMT  
		Size: 31.3 KB (31278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:58161af64aa2b51135acb48817da5363735d5652b5f4ab2e34bc3ac0cb972ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7811959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5f93db806d8fd7695b1fccd88b37122a4d3e45cbe09c062427a4c29af42c7f`

```dockerfile
```

-	Layers:
	-	`sha256:a369549df7c66cc8e18ce1592a75bad918f5f16c62598d8b3b7a64d39c102411`  
		Last Modified: Mon, 02 Jun 2025 17:05:50 GMT  
		Size: 7.8 MB (7787018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f7eefebfda45b65622011c0c7213e91117ed967dc3844321058e699252a5b63`  
		Last Modified: Mon, 02 Jun 2025 17:05:49 GMT  
		Size: 24.9 KB (24941 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:fdaf04204e0cd866e5edac5910aa94f51b5fe2de5e610e3fc09f01a94a150558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.7 MB (361705690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d488a0a8b77149b10308d5360412f35c102e83120d6f78fc447967d73454a9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:19:35 GMT
ARG RELEASE
# Sun, 30 Mar 2025 18:19:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Mar 2025 18:19:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Mar 2025 18:19:35 GMT
LABEL org.opencontainers.image.version=20.04
# Sun, 30 Mar 2025 18:19:35 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:19:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Mar 2025 18:19:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Mar 2025 18:19:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='5eb00b18e37757775e6f46c706eae38d9e91be49de5712987801cba8ffd77767';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["jshell"]
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:19:35 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_VERSION=6.9.4
# Sun, 30 Mar 2025 18:19:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER gradle
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER root
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af9d62a97be401b93c2f6eb1dc4bb4c70329ac3b300956d3867dfc020b29c3e`  
		Last Modified: Wed, 09 Apr 2025 06:57:19 GMT  
		Size: 20.1 MB (20092976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab4c8be69a99c7f35c5de30635734ecfdbe82a5b388f8516f2086d13689c1d1`  
		Last Modified: Wed, 23 Apr 2025 16:31:16 GMT  
		Size: 142.4 MB (142431854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e521eabc169cc18d48289493cf2c0df51bf18dbe3ba218d6b5a547794ad6041`  
		Last Modified: Wed, 23 Apr 2025 16:31:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02f2567c557894b689bd4347d34d45e657af6886f0023d2ffa31e0294948dd2`  
		Last Modified: Wed, 23 Apr 2025 16:31:12 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2e5812277fc5a555d8abe030fa3f02bcd602c238d5e0aad22c17a1a8caabef`  
		Last Modified: Wed, 23 Apr 2025 17:34:58 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6ea936e35f3db7a7a72e1925d7ce43de35c8d917ddd8d7de7b5fdf1b5fbc54`  
		Last Modified: Wed, 23 Apr 2025 17:35:01 GMT  
		Size: 65.1 MB (65074727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e82da25b1fae4f7c2a90443d25907d5563274c9d861e68c1a89ad321093338`  
		Last Modified: Wed, 23 Apr 2025 17:41:39 GMT  
		Size: 107.7 MB (107696665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9da033a2e8c696a75298b0ce66a4bc41889cb1a1bec35dd12a7d8e61e52e36`  
		Last Modified: Wed, 23 Apr 2025 17:41:36 GMT  
		Size: 425.0 KB (425021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:f1b5bf602520b2a3d6538548dbef02042b25e79b4daebde40d687c7bef30cf1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7765032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c03c47f653938789a71a8c359871530aa636c90707fa195d2fdb0e52c97b0b`

```dockerfile
```

-	Layers:
	-	`sha256:1b62fd9795bb8bfcb24328903e7bf835d0c49b12020ec1520e7256ae6be3d6ef`  
		Last Modified: Wed, 23 Apr 2025 17:41:37 GMT  
		Size: 7.7 MB (7741561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c0f4d593e9fa00a64d4a523662381841f8e8a5795e695ab5d4b5dba6a0be120`  
		Last Modified: Wed, 23 Apr 2025 17:41:36 GMT  
		Size: 23.5 KB (23471 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk-focal` - linux; ppc64le

```console
$ docker pull gradle@sha256:7719b747c69ab9b47f0cc1a1448ccf54fc84d913c3da7357cb55864445d5aac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.7 MB (368718771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad9007b28f91d9dc8ef31e98c4a99ed8639b30a576aecfb7d186e132b327031`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:19:35 GMT
ARG RELEASE
# Sun, 30 Mar 2025 18:19:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Mar 2025 18:19:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Mar 2025 18:19:35 GMT
LABEL org.opencontainers.image.version=20.04
# Sun, 30 Mar 2025 18:19:35 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:19:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Mar 2025 18:19:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Mar 2025 18:19:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='5eb00b18e37757775e6f46c706eae38d9e91be49de5712987801cba8ffd77767';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["jshell"]
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:19:35 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_VERSION=6.9.4
# Sun, 30 Mar 2025 18:19:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER gradle
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER root
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5eddb83d3002695f58ef132a43fe0c41ba6a1338438d3698725700dfbf1177`  
		Last Modified: Wed, 09 Apr 2025 04:33:49 GMT  
		Size: 22.4 MB (22424673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487f6b4cae0672692f77a99ad0a2ea0d04e3b50919170bc9d60b7cb2a3be2c4f`  
		Last Modified: Wed, 23 Apr 2025 16:32:20 GMT  
		Size: 132.8 MB (132827168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f835426b7cac4952788507d7461c504f365b7623f1d94342b9dc681267dfcd7b`  
		Last Modified: Wed, 23 Apr 2025 16:32:16 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f531d3e761dcb504eda7601632df0bbd9b81b59fd82258c8b5e99ab25b1aa9`  
		Last Modified: Wed, 23 Apr 2025 16:32:16 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf65842dd0333b44cbf2b466068e25905cd0aaf8be2204a9d6a1ada7241048`  
		Last Modified: Wed, 23 Apr 2025 17:29:39 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85209ef619e057fd9b7f239fdb4edbe44946bd9a2fd33e38ad7868c8e72ded5f`  
		Last Modified: Wed, 23 Apr 2025 17:29:42 GMT  
		Size: 73.7 MB (73651539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6729b6cce616b59fb171ead87949b243782306dbe476fb7e51052c2e85351828`  
		Last Modified: Wed, 23 Apr 2025 17:40:56 GMT  
		Size: 107.7 MB (107696668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cca70358c0cea63f91932889a3c3396f711ba303019a72131d6d5955c3573b1`  
		Last Modified: Wed, 23 Apr 2025 17:40:52 GMT  
		Size: 35.0 KB (34988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:0ee0d395757fc8c9f80f2222e54db1b545886c9cea08ebb26147100d0d3e239c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7763164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2593d7e1e9eb8406021612e9a8b7f99996c90aeafe4a9611d2dcd89114cf3b9c`

```dockerfile
```

-	Layers:
	-	`sha256:4c2287e1f7a7e3a5bf79cc07c9b5468f9776efc35599dcb75e32e5c49f45c9f5`  
		Last Modified: Wed, 23 Apr 2025 17:40:53 GMT  
		Size: 7.7 MB (7739823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e5ae1c1ab81288143750f6d43d459feea432da7aefb5b0f2ca06cc61faf208e`  
		Last Modified: Wed, 23 Apr 2025 17:40:52 GMT  
		Size: 23.3 KB (23341 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk-focal` - linux; s390x

```console
$ docker pull gradle@sha256:a159cf14ca61c887b3ed404b90d8004dd1445d482e75d15abb661c662bb650fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.2 MB (344235738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c87d4c2a2b72ca639028f8457a44aa3d133b96d3ee2a6c922f6b922bb18c74f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:19:35 GMT
ARG RELEASE
# Sun, 30 Mar 2025 18:19:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Mar 2025 18:19:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Mar 2025 18:19:35 GMT
LABEL org.opencontainers.image.version=20.04
# Sun, 30 Mar 2025 18:19:35 GMT
ADD file:82f0132f510f24adc12d74491187647b94a14baa7a57fd22a67a5c3767541496 in / 
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:19:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 30 Mar 2025 18:19:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 30 Mar 2025 18:19:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        arm64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        armhf)          ESUM='5eb00b18e37757775e6f46c706eae38d9e91be49de5712987801cba8ffd77767';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_arm_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64el)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["jshell"]
# Sun, 30 Mar 2025 18:19:35 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:19:35 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENV GRADLE_VERSION=6.9.4
# Sun, 30 Mar 2025 18:19:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER gradle
# Sun, 30 Mar 2025 18:19:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
USER root
```

-	Layers:
	-	`sha256:b35596e17e863edd4c594d026a60e36f73cc6a076370f55a24732114fd25ff68`  
		Last Modified: Tue, 08 Apr 2025 11:48:56 GMT  
		Size: 26.4 MB (26368190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86df5de06adafff5e91defb0ae071cda11948fd1f3ad0b05fbc6819acc60390`  
		Last Modified: Wed, 09 Apr 2025 04:15:20 GMT  
		Size: 19.9 MB (19901168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3f08f5ac08dc697434f4bdf19a5a4f628e80aa9e42a5f810835e994080b0a6`  
		Last Modified: Wed, 23 Apr 2025 16:31:39 GMT  
		Size: 125.6 MB (125598014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df622b3d9284836480ad32dbf79bb60cfead24ecab64b0234d921bfdc7e067`  
		Last Modified: Wed, 23 Apr 2025 16:31:37 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b273028092c40df0426a03e1841dab86ff1ac619fff36c614d98805074ca664f`  
		Last Modified: Wed, 23 Apr 2025 16:31:37 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ecb6550f80b87ef50bb3057e4da4c3a52a61207ca1869bbd705b1abb1901c3`  
		Last Modified: Wed, 23 Apr 2025 17:20:49 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d57a1da0c7f13d1c68fde08c63e3b3dd3be40ce7fde4b05bddcf8317b5421`  
		Last Modified: Wed, 23 Apr 2025 17:20:51 GMT  
		Size: 64.6 MB (64629925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92db6409a8771ca87943449ba2d5edc6206cea258b32ec1c3ac61fc74b8f85a5`  
		Last Modified: Wed, 23 Apr 2025 17:28:46 GMT  
		Size: 107.7 MB (107696669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e69be215ec049e5a7ca2db2e1c2f8a91f5c21ca0b38397d03334c711ae0719`  
		Last Modified: Wed, 23 Apr 2025 17:28:44 GMT  
		Size: 35.0 KB (34981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:260f54687c9c313e7603180ec67188d91a4e9dc58dcea0fdb8ec74c7ba72a6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7753366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65850fceefb1105991a9c8fc0b49d054039c413f2f89ddaaab02a6cbef3ee60c`

```dockerfile
```

-	Layers:
	-	`sha256:cf8366c84f922bc7c674c72db62b0d2abdab68a33fe6f86b88d5fb9a25a1ac26`  
		Last Modified: Wed, 23 Apr 2025 17:28:44 GMT  
		Size: 7.7 MB (7730105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cb7ee68c7103c082db7ff1bd8e3cc44a3de6b8e1395dfc58a3f9e8ac871b76d`  
		Last Modified: Wed, 23 Apr 2025 17:28:44 GMT  
		Size: 23.3 KB (23261 bytes)  
		MIME: application/vnd.in-toto+json
