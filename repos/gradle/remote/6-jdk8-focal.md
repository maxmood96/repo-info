## `gradle:6-jdk8-focal`

```console
$ docker pull gradle@sha256:fd70a374c764b336536b99cec3357aec19ebb7eec89d3fea7d69c8c6210ad9c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:6-jdk8-focal` - linux; amd64

```console
$ docker pull gradle@sha256:f47e1b4086ec865a179a9e60659a53ce26d21b1a76bd42a1c86ab4051fb4e008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275947109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224a7d7aeda873fad6db4312a4c588db8e6890f7071e893579e66aa5f9ca5db5`
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
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
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
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20980e7d78f727e72412bce891dc672054ede0e7266aa671206c81efba9e2c2`  
		Last Modified: Thu, 08 May 2025 17:14:38 GMT  
		Size: 20.3 MB (20260437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7778ef8878677f723d33d7e7a3a6921f72123b78dd518f1202d8f5bfd7dd6e8c`  
		Last Modified: Thu, 08 May 2025 17:14:41 GMT  
		Size: 54.7 MB (54721859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbc5a2fd6ab8c3df0b9b9e316280ada9c3cfbfade63bf4bf37fc926033a0362`  
		Last Modified: Thu, 08 May 2025 17:14:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0090a29e4e6c6a31cbd8b2c92d593b8e7689f9ba14aaea5de73fb5f79e5497b8`  
		Last Modified: Thu, 08 May 2025 17:14:37 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14270dd8a3449d33be21607f36597f626320aa078100cb4de7e6f0721b045b6c`  
		Last Modified: Mon, 28 Apr 2025 20:51:11 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf04a53219ee5c405a43d6f245e723afcb5b1b6a68e809a7cc4fca107907a477`  
		Last Modified: Mon, 28 Apr 2025 20:51:13 GMT  
		Size: 65.3 MB (65319711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e78c7b90f9414417277f79347eb91c04362598b3bd7d4f1069a350012f23fe8`  
		Last Modified: Mon, 28 Apr 2025 20:51:14 GMT  
		Size: 107.7 MB (107696660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ecf7a13fb3930ea954b07785f0951d8f385f290ca7f4df270c4ec7db53bbbf`  
		Last Modified: Mon, 28 Apr 2025 20:51:11 GMT  
		Size: 431.3 KB (431269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:546f1b802eba2fa110a06a543fe28db11b71788ee2947c0f49e09675aec5f668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7856063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d47dd815e9352167d4de47ab87bb51ea42c59167e7376b10fa8c73733e650ed`

```dockerfile
```

-	Layers:
	-	`sha256:c09e8e89eaf9922d0cd55192db0c5ed71b2a664181a93908af7474056bf07dc2`  
		Last Modified: Mon, 28 Apr 2025 20:51:11 GMT  
		Size: 7.8 MB (7834672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20d06fb80be769d8be372b4235968af0329566aa96e4a84116da53ccbcc682aa`  
		Last Modified: Mon, 28 Apr 2025 20:51:11 GMT  
		Size: 21.4 KB (21391 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-focal` - linux; arm variant v7

```console
$ docker pull gradle@sha256:731e9597835c857017c9fe6f85cfba5ba3c90c1ec2fa3924e96243a0bf912fe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (259950327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afb98cb8a956a2fea301db6699aef3cb5ee670c283500e6a039549f4defc7b4`
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
ADD file:bd50d86208ba682c6f55f52b7ec95adbfb2e247d9dfff47b9c3871d27a7b0d19 in / 
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
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:12c22ff1560db33ab4235fc5b1744509b7c274b95beb2a7ba7b6671705fcef6e`  
		Last Modified: Thu, 08 May 2025 17:24:17 GMT  
		Size: 23.6 MB (23624063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584dcd1f0ae60202572ceaaf1d1ff21ed62161827b256dfd50433bbcba261dfd`  
		Last Modified: Wed, 09 Apr 2025 11:38:16 GMT  
		Size: 18.5 MB (18478140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9f96d95f94d5af90d6cd265bb97d46182bc537498034bc122edc669727daf2`  
		Last Modified: Mon, 28 Apr 2025 20:07:36 GMT  
		Size: 50.1 MB (50125439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772c02b1ea58c6a75828813c7686282de45592f615262262a5beb5d8d1e021be`  
		Last Modified: Mon, 28 Apr 2025 20:07:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b453f5bc04aa4d7d836b6017c3843aedd22648e51bff93cc04e84ec0d13ea3a6`  
		Last Modified: Mon, 28 Apr 2025 20:07:34 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb7270637900b49b0c2175df4ab19a0e035f17af1fd75a9a5aec8b9489e0fb0`  
		Last Modified: Mon, 28 Apr 2025 21:01:22 GMT  
		Size: 4.3 KB (4300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72a6aff7c79f9c02fe28c759badd18b30afe8a5e329d63608af6c44d8469201`  
		Last Modified: Mon, 28 Apr 2025 21:01:25 GMT  
		Size: 60.0 MB (59987997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1d27230100559250125da2a3c8609209679ed3f0dfc43ee62e4b143be9d3b2`  
		Last Modified: Mon, 28 Apr 2025 21:05:24 GMT  
		Size: 107.7 MB (107696650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa9c10ceac8ffffc3a2537490eb29456b02021bb0ceba48a45e7ae44a8d16c3`  
		Last Modified: Mon, 28 Apr 2025 21:05:20 GMT  
		Size: 31.3 KB (31272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:10467438ad31d7836659f41de64341ab33eaed56790df0d046d38319061c10b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7861367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aecf3b9f05d63efc9c5500d0653474222f94ae9707925dda8d14662e570f8226`

```dockerfile
```

-	Layers:
	-	`sha256:2555a17dfd7db24d98399e02f000a450a1bdb90ed560106a9707c907544e5093`  
		Last Modified: Mon, 28 Apr 2025 21:05:21 GMT  
		Size: 7.8 MB (7839870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8cec5b663cb9b442c89563bf0bfae92d3e68922d4f384bd0a3ecb2d04b14348`  
		Last Modified: Mon, 28 Apr 2025 21:05:20 GMT  
		Size: 21.5 KB (21497 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:cd0ed23a890bbe7947f3f718164bd59b77cd44fa5e89987cf76df5af6926476d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.1 MB (273106755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230f555f7cbf7cd0e8c8194bba4c7e2fa6e654bba07274a92a341a8cac0d6de4`
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
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af9d62a97be401b93c2f6eb1dc4bb4c70329ac3b300956d3867dfc020b29c3e`  
		Last Modified: Thu, 08 May 2025 17:09:10 GMT  
		Size: 20.1 MB (20092976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c00c0b5c103330a238db0e07c88322ec3b801e044907a6ee5bf54251f50252`  
		Last Modified: Thu, 08 May 2025 17:16:38 GMT  
		Size: 53.8 MB (53834692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6602bf4e0b42d138670f1641a397f020adb9041bace6008882cc98ad0595ea8`  
		Last Modified: Thu, 08 May 2025 17:16:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4675a7cf7687748bf9b99626829b1724a4c405d81d66ddb19b67b51cc2d34c`  
		Last Modified: Thu, 08 May 2025 17:16:44 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed15ff56b54d8fafcb877ab1d5505f10cc072e64600f784933181e24c7011ec`  
		Last Modified: Mon, 28 Apr 2025 21:01:28 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f0267b463b51a9e95aa0562eedc068b2d5f3b71d57bf072748fef3c8ae3190`  
		Last Modified: Mon, 28 Apr 2025 21:01:31 GMT  
		Size: 65.1 MB (65072958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e7b36e4aae95cf24db344b39bebe7cf9834d09a32af43350bce7fef25f7b60`  
		Last Modified: Mon, 28 Apr 2025 21:04:27 GMT  
		Size: 107.7 MB (107696666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a5a6550f0c784a697d0cb65e78c9efc8b226e37c5cd39817a7ddc6380d78e`  
		Last Modified: Mon, 28 Apr 2025 21:04:24 GMT  
		Size: 425.0 KB (425023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:e34bd63c8c1350ddc47498917a57585f6da4f463932163511799c1752763046c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7862718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641d83b63a9ff9d2ae42f8329520008727765c8dcea45c272258c0b11c8de92b`

```dockerfile
```

-	Layers:
	-	`sha256:bb40664f3640b81cedd4de151000adb4ff6fda945a8e56bcc9288ec39e835a1c`  
		Last Modified: Mon, 28 Apr 2025 21:04:24 GMT  
		Size: 7.8 MB (7841190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f27780adecc574e8bcd05a37562c8db6a471a9fb2d8859b719ea283358c6426`  
		Last Modified: Mon, 28 Apr 2025 21:04:23 GMT  
		Size: 21.5 KB (21528 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-focal` - linux; ppc64le

```console
$ docker pull gradle@sha256:76ec93fc13f2bbffc74df02b337e7b8488dc5b2219f4abffac7bc902f73bf11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288055449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5885b6d899a09a15ad019ff4b448f287154cf47d0b9f0df88e421e5f5d4ade19`
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
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        arm64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        armhf)          ESUM='a467f86d0dc4c9077edeac5eeae0622a556399180628eee6969c745afb1deaf0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_arm_linux_hotspot_8u452b09.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 30 Mar 2025 18:19:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
		Last Modified: Thu, 08 May 2025 21:39:31 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5eddb83d3002695f58ef132a43fe0c41ba6a1338438d3698725700dfbf1177`  
		Last Modified: Wed, 09 Apr 2025 04:33:49 GMT  
		Size: 22.4 MB (22424673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9eef0be3f478cf7b447ba64a0da2b3e80a3bf3611e591cf5e919c4e7099e380`  
		Last Modified: Mon, 28 Apr 2025 20:07:56 GMT  
		Size: 52.2 MB (52168619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8741079b5f79fd6329e63d54b05157175d23c60526801255e4d311b3d4a0442c`  
		Last Modified: Mon, 28 Apr 2025 20:07:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ac0617f4761bfff5a6bd3badeb391144d791076226cdbe054bdd5925a220fe`  
		Last Modified: Mon, 28 Apr 2025 20:07:54 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617d135a71c25b735d1bb8311f1c60a594c815989f4ecec529a7e6966b4e649b`  
		Last Modified: Mon, 28 Apr 2025 21:04:40 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87754f3043d9aa4f782d7580c5d442dd64680797053c0fb3ea0a0c3c72febfff`  
		Last Modified: Mon, 28 Apr 2025 21:04:43 GMT  
		Size: 73.6 MB (73646793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d52c1233e530aa0ecce4fbfc09e59faf9c43ec727830dbf763f38ced049c23`  
		Last Modified: Mon, 28 Apr 2025 21:11:04 GMT  
		Size: 107.7 MB (107696651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbc11735fb1c6e91a5cfe9446d77ba1f27d6f6400e728eae6f267269f25599a`  
		Last Modified: Mon, 28 Apr 2025 21:11:00 GMT  
		Size: 35.0 KB (34986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-focal` - unknown; unknown

```console
$ docker pull gradle@sha256:55f1ea88d179163818e8b335461df389807458469205dc50336d2ea157f88644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7862050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83bcfd20beb03d7be155db0b5bbe75e1fc1aa9ee3147638bfb1cae8f52e41602`

```dockerfile
```

-	Layers:
	-	`sha256:780ce1acd5ebc2dd87dfffabf45289545ba0a1fc0c3385e0dfbaa1b08bcb06c0`  
		Last Modified: Mon, 28 Apr 2025 21:11:01 GMT  
		Size: 7.8 MB (7840616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a35672ebeb8cb8110ff05b1630293877c5de6f6a12e9db98ad742f1b47c82502`  
		Last Modified: Mon, 28 Apr 2025 21:11:00 GMT  
		Size: 21.4 KB (21434 bytes)  
		MIME: application/vnd.in-toto+json
