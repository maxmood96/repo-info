## `gradle:7-jdk11-jammy`

```console
$ docker pull gradle@sha256:0e72ff4dd7a7074841d356e13fa56b449e330c5c8645053a7eb65a4cad7003bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:7-jdk11-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:03b61762bca4ab787f576b29480e2db3823ccbd376de4c0eef9d4f01063308b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.5 MB (362544135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e42a1f020968c7b1c66343a183e5255285dcebcfdf444de10a03341d338924`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:14:56 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:33:35 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:33:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ca1dc604352e9b3906b8955a700745a0a650ed59947f7f354af597871876a716';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='25cf602cac350ef36067560a4e8042919f3be973d419eac4d839e2e0000b2cc8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='7d0e71d8aea6bba27dfbb9ad7434066896c3085327e58776ca89d5e262040bc5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='95a1c215e434c302e43c8039f322b954ee539ca22412cd09b4dd77523aaa861a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='137becfcfa6d288ba8c07ba23bf966c87bedfe7ee5cb3342da833407e13e3cfa';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:33:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:33:46 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:33:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 20:33:46 GMT
CMD ["jshell"]
# Wed, 24 Jan 2024 23:14:46 GMT
CMD ["gradle"]
# Wed, 24 Jan 2024 23:14:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 24 Jan 2024 23:14:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 24 Jan 2024 23:14:47 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 24 Jan 2024 23:14:47 GMT
WORKDIR /home/gradle
# Wed, 24 Jan 2024 23:15:04 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 24 Jan 2024 23:18:28 GMT
ENV GRADLE_VERSION=7.6.3
# Wed, 24 Jan 2024 23:18:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
# Wed, 24 Jan 2024 23:18:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 24 Jan 2024 23:18:33 GMT
USER gradle
# Wed, 24 Jan 2024 23:18:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 24 Jan 2024 23:18:34 GMT
USER root
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e4f12b52933eaf22480862af2278c73cca667e35d95f7c2fa7d5b1e66cdc58`  
		Last Modified: Wed, 17 Jan 2024 07:19:01 GMT  
		Size: 12.9 MB (12906285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e82afaa7e6a306a70bff92bdbddf9d79d8adf11dd0551e001f0151d969e2ca`  
		Last Modified: Wed, 24 Jan 2024 20:43:28 GMT  
		Size: 145.3 MB (145288607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252edfc25a4080f50af55f5977da4775343c7d0362809a14d29bcd15268ddc07`  
		Last Modified: Wed, 24 Jan 2024 20:43:16 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53af593f03bcf81f951d9f8ebedb7007e236a505c38012398c9fa0a87230fd81`  
		Last Modified: Wed, 24 Jan 2024 20:43:16 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d09ac49e96d3dd1338750403be02bb772ba9678f13934ad33300a961f2c8e2`  
		Last Modified: Wed, 24 Jan 2024 23:23:09 GMT  
		Size: 4.4 KB (4370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2119b7d2b0538a6f8b9ccb3276406a2f3d69cc02bc0664d8b3f04d23f69e1e`  
		Last Modified: Wed, 24 Jan 2024 23:23:17 GMT  
		Size: 51.5 MB (51549821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7daa7ddc5d1daddacaa1d42420119ecfecedf46a5d6134a7da08b19c6f4ff5`  
		Last Modified: Wed, 24 Jan 2024 23:28:44 GMT  
		Size: 122.3 MB (122346880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d8d0541592bf9b82a812194898501f7cb25569a3e9e72016bd804332f2acb7`  
		Last Modified: Wed, 24 Jan 2024 23:28:38 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk11-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:87e16c7bd9dfc112aefa8e857225542178bca12fee2f115054d055e3e2c1bd19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.1 MB (354078421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999f88dc9e0c582251db647531f4d3f7a0276f197fecc368074cf05f231d098c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 11 Jan 2024 17:30:37 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:30:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:30:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:30:37 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:30:39 GMT
ADD file:7c2f93ce47dedf9ba449bf11d41e9930af9fa209725f5772dc09f8c8100b5626 in / 
# Thu, 11 Jan 2024 17:30:40 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 09:39:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:39:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:39:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 09:40:02 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 21:11:56 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 21:12:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ca1dc604352e9b3906b8955a700745a0a650ed59947f7f354af597871876a716';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='25cf602cac350ef36067560a4e8042919f3be973d419eac4d839e2e0000b2cc8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='7d0e71d8aea6bba27dfbb9ad7434066896c3085327e58776ca89d5e262040bc5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='95a1c215e434c302e43c8039f322b954ee539ca22412cd09b4dd77523aaa861a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='137becfcfa6d288ba8c07ba23bf966c87bedfe7ee5cb3342da833407e13e3cfa';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 21:12:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 21:12:08 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 21:12:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 21:12:09 GMT
CMD ["jshell"]
# Wed, 24 Jan 2024 21:35:37 GMT
CMD ["gradle"]
# Wed, 24 Jan 2024 21:35:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 24 Jan 2024 21:35:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 24 Jan 2024 21:35:38 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 24 Jan 2024 21:35:38 GMT
WORKDIR /home/gradle
# Wed, 24 Jan 2024 21:35:54 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 24 Jan 2024 21:38:00 GMT
ENV GRADLE_VERSION=7.6.3
# Wed, 24 Jan 2024 21:38:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
# Wed, 24 Jan 2024 21:38:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 24 Jan 2024 21:38:06 GMT
USER gradle
# Wed, 24 Jan 2024 21:38:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 24 Jan 2024 21:38:07 GMT
USER root
```

-	Layers:
	-	`sha256:cea537175db3d13760d71d7a8baa0a5e82491345696d2da089429926cceccffe`  
		Last Modified: Fri, 12 Jan 2024 04:33:34 GMT  
		Size: 27.5 MB (27525460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c76525c6d0fb13a7cef6ae1ed97048d26d601bc0e9c8122dd8f09146633951b`  
		Last Modified: Wed, 17 Jan 2024 09:43:20 GMT  
		Size: 12.5 MB (12495255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6ad80b71281875897870a00549882d9eba04a1b436acfee5981d6d4b45088e`  
		Last Modified: Wed, 24 Jan 2024 21:15:44 GMT  
		Size: 137.8 MB (137815339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492004dcc028f3ceb9714426b533b458b60a41daa55de493eb2c264e4e5890cc`  
		Last Modified: Wed, 24 Jan 2024 21:15:31 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4732eeee2719b8744f82027adc1e49d7fd1060ccc1567ae264d991f20fca01b7`  
		Last Modified: Wed, 24 Jan 2024 21:15:31 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b930f82e5e650e85c226e54876dee912f879a2aacc62d104d435dd48f33403`  
		Last Modified: Wed, 24 Jan 2024 21:41:31 GMT  
		Size: 4.4 KB (4355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904698858169e4e0a02f2f1210eef6fa6ffa4b2cb3af625b4b944d2caad6bcaf`  
		Last Modified: Wed, 24 Jan 2024 21:41:42 GMT  
		Size: 53.9 MB (53890046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1a7e1bc8685296484d7b70f964af72cc60a52ab4edd4c7752c69d539521f8e`  
		Last Modified: Wed, 24 Jan 2024 21:45:00 GMT  
		Size: 122.3 MB (122346906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827502295df181ebd14b964d0195c186fc12f3a9e38bdf98447a9e11dc69fec3`  
		Last Modified: Wed, 24 Jan 2024 21:44:54 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk11-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c321e60d7780cbb73314ccbfa9be1eecc62d3c01cc02110567e601c2c39bfbe4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.7 MB (356737151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11470da5ca82f1b62945dd75c636f5b97b98f23ed0210038962c93f38990085b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 06:57:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 06:57:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 06:57:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 06:57:53 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:41:10 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:41:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ca1dc604352e9b3906b8955a700745a0a650ed59947f7f354af597871876a716';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='25cf602cac350ef36067560a4e8042919f3be973d419eac4d839e2e0000b2cc8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='7d0e71d8aea6bba27dfbb9ad7434066896c3085327e58776ca89d5e262040bc5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='95a1c215e434c302e43c8039f322b954ee539ca22412cd09b4dd77523aaa861a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='137becfcfa6d288ba8c07ba23bf966c87bedfe7ee5cb3342da833407e13e3cfa';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:41:19 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:41:19 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:41:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 20:41:19 GMT
CMD ["jshell"]
# Wed, 24 Jan 2024 23:06:56 GMT
CMD ["gradle"]
# Wed, 24 Jan 2024 23:06:57 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 24 Jan 2024 23:06:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Wed, 24 Jan 2024 23:06:57 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 24 Jan 2024 23:06:57 GMT
WORKDIR /home/gradle
# Wed, 24 Jan 2024 23:07:10 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Wed, 24 Jan 2024 23:11:12 GMT
ENV GRADLE_VERSION=7.6.3
# Wed, 24 Jan 2024 23:11:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
# Wed, 24 Jan 2024 23:11:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 24 Jan 2024 23:11:16 GMT
USER gradle
# Wed, 24 Jan 2024 23:11:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 24 Jan 2024 23:11:17 GMT
USER root
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7847c91c5f9018c3a6f03ce61a2b202d22d91f08283f1981203f8dbbb742edf7`  
		Last Modified: Wed, 17 Jan 2024 07:01:02 GMT  
		Size: 12.8 MB (12849375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63af98611d3b0df3ba07ffee913d6d56c4ce360b299896e6791b2995bbede43c`  
		Last Modified: Wed, 24 Jan 2024 20:48:50 GMT  
		Size: 142.0 MB (142014954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e7577c12606344a8643695f6f22286fd31091e40e64b3c5e6231f3b24f577e`  
		Last Modified: Wed, 24 Jan 2024 20:48:40 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c272bb1c451f75fbe73e897827e2cbc0ee987d4bdccd3b9b74ef18f6ead161`  
		Last Modified: Wed, 24 Jan 2024 20:48:40 GMT  
		Size: 716.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432bc294ec8fc194ba5462f75c4878751d773c70674e1e21b38d17a5b4d79f86`  
		Last Modified: Wed, 24 Jan 2024 23:14:19 GMT  
		Size: 4.4 KB (4369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec07fe04504025eb922f8cb84d63c1e7b3cc7056de0e0c8af9b2f95ebc4cc4c7`  
		Last Modified: Wed, 24 Jan 2024 23:14:26 GMT  
		Size: 51.1 MB (51120867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c7cce03dc30d6002225ce80bf7507bbffc74d4b761bcc71fad3cdcb56c1b3d`  
		Last Modified: Wed, 24 Jan 2024 23:17:55 GMT  
		Size: 122.3 MB (122346911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a459a07abf3b7ae537714f97488f86f3d74ab2d35e5326b3e599a068f7aa946`  
		Last Modified: Wed, 24 Jan 2024 23:17:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk11-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:0b81edc2274f15077ca16b81eff6d6c4a49ea0ee1b5a09dc7c8150fd8b970b75
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359864479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abce0eafbe6cd714eea8a26146a0343441d44b06bb2150263c4f80c4b6f9eacc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 11 Jan 2024 17:10:02 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:10:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:10:06 GMT
ADD file:4da6fb9ba29da03fa46ed73abfae01fa7c87f2c26044ee297c88359085392aef in / 
# Thu, 11 Jan 2024 17:10:06 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:29:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:29:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:29:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:30:29 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:37:22 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 24 Jan 2024 20:37:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ca1dc604352e9b3906b8955a700745a0a650ed59947f7f354af597871876a716';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='25cf602cac350ef36067560a4e8042919f3be973d419eac4d839e2e0000b2cc8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='7d0e71d8aea6bba27dfbb9ad7434066896c3085327e58776ca89d5e262040bc5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='95a1c215e434c302e43c8039f322b954ee539ca22412cd09b4dd77523aaa861a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='137becfcfa6d288ba8c07ba23bf966c87bedfe7ee5cb3342da833407e13e3cfa';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:37:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Thu, 25 Jan 2024 19:25:46 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 25 Jan 2024 19:25:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 19:25:47 GMT
CMD ["jshell"]
# Thu, 25 Jan 2024 19:49:36 GMT
CMD ["gradle"]
# Thu, 25 Jan 2024 19:49:37 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 25 Jan 2024 19:49:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 25 Jan 2024 19:49:40 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 25 Jan 2024 19:49:41 GMT
WORKDIR /home/gradle
# Thu, 25 Jan 2024 19:50:26 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 25 Jan 2024 19:56:09 GMT
ENV GRADLE_VERSION=7.6.3
# Thu, 25 Jan 2024 19:56:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
# Thu, 25 Jan 2024 19:56:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Thu, 25 Jan 2024 19:56:20 GMT
USER gradle
# Thu, 25 Jan 2024 19:56:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Thu, 25 Jan 2024 19:56:23 GMT
USER root
```

-	Layers:
	-	`sha256:898e4a5fe680690395e7fd9d920dfa248b7508ec0573741c491bf250179ddbda`  
		Last Modified: Wed, 17 Jan 2024 05:26:53 GMT  
		Size: 35.7 MB (35657152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f85bd9b095b5879a3465b7ad0b393d5c09a45f44fa356c1d64ce36e5c6517e`  
		Last Modified: Wed, 17 Jan 2024 07:36:37 GMT  
		Size: 13.8 MB (13769329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e4b7fbfa645ffda8cf4f4d6a8cf258d1ba04389610ebc6620b13e891d1a864`  
		Last Modified: Wed, 24 Jan 2024 20:50:35 GMT  
		Size: 132.4 MB (132411376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e3e0bf5e8cf2cb200d02c2c7204912933e549fdd0f43a63f875c45e189ca56`  
		Last Modified: Wed, 24 Jan 2024 20:50:23 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04edfa470bb711565a03cca04d885d15c4db2ca4aba0e037d62bb466ecc25ef`  
		Last Modified: Thu, 25 Jan 2024 19:28:58 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3584aa3512d38fa74dd7b5bf764b03b038882c83a8dfa8e9786e36dd5618b982`  
		Last Modified: Thu, 25 Jan 2024 20:01:34 GMT  
		Size: 4.4 KB (4364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27485cb7cbf34b7dd0ec6faf8210933b965b13970b3ed8b435fc231611e48c3`  
		Last Modified: Thu, 25 Jan 2024 20:01:45 GMT  
		Size: 55.7 MB (55674265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715394a0357282be47dd24bf3b76f2da6d08f45fdae2e113100d2375d902d7d9`  
		Last Modified: Thu, 25 Jan 2024 20:05:33 GMT  
		Size: 122.3 MB (122346914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb8ad28f53057a90b3aa0063561dfaff591a0985300789a6d9aeed45ad25113`  
		Last Modified: Thu, 25 Jan 2024 20:05:26 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk11-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:23106bca4ed5ef4d8262728ea618efe37293a54981eceb0a2906a760161a7004
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340686437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa041d0ba2662f0f0a2e00b8141f3a58a31712e8991d1037224d1a785f0f637f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 11 Jan 2024 17:12:07 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:12:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:12:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:12:07 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:12:10 GMT
ADD file:5ae109128826d2e7660949ed9ff9af4b92bbade5ce06a7011ab7b15bb21d8b75 in / 
# Thu, 11 Jan 2024 17:12:10 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 10:46:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 10:46:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 10:46:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 10:46:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 17:20:55 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Thu, 25 Jan 2024 17:21:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ca1dc604352e9b3906b8955a700745a0a650ed59947f7f354af597871876a716';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='25cf602cac350ef36067560a4e8042919f3be973d419eac4d839e2e0000b2cc8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='7d0e71d8aea6bba27dfbb9ad7434066896c3085327e58776ca89d5e262040bc5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='95a1c215e434c302e43c8039f322b954ee539ca22412cd09b4dd77523aaa861a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='137becfcfa6d288ba8c07ba23bf966c87bedfe7ee5cb3342da833407e13e3cfa';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 25 Jan 2024 17:21:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Thu, 25 Jan 2024 17:21:08 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Thu, 25 Jan 2024 17:21:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 17:21:08 GMT
CMD ["jshell"]
# Thu, 25 Jan 2024 20:23:02 GMT
CMD ["gradle"]
# Thu, 25 Jan 2024 20:23:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 25 Jan 2024 20:23:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 25 Jan 2024 20:23:03 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 25 Jan 2024 20:23:03 GMT
WORKDIR /home/gradle
# Thu, 25 Jan 2024 20:23:30 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 25 Jan 2024 20:30:33 GMT
ENV GRADLE_VERSION=7.6.3
# Thu, 25 Jan 2024 20:30:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
# Thu, 25 Jan 2024 20:30:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Thu, 25 Jan 2024 20:30:41 GMT
USER gradle
# Thu, 25 Jan 2024 20:30:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=740c2e472ee4326c33bf75a5c9f5cd1e69ecf3f9b580f6e236c86d1f3d98cfac
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Thu, 25 Jan 2024 20:30:42 GMT
USER root
```

-	Layers:
	-	`sha256:9767f83c892c3413514216ee1180f4118e77f689d61466a79134bd214cf66520`  
		Last Modified: Wed, 17 Jan 2024 10:37:33 GMT  
		Size: 28.7 MB (28654354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df287fce2d9ba06f3f2c88f705e070ca02b4f9e3965318a9aa010e0b8702171`  
		Last Modified: Wed, 17 Jan 2024 11:05:17 GMT  
		Size: 13.0 MB (12987141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66dd0be4ebb2d9b0feacb30688af8379875a1e76c0f8ee1cf8d23125f3ac012`  
		Last Modified: Thu, 25 Jan 2024 17:43:27 GMT  
		Size: 125.4 MB (125414823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a06976ba3d4bb0395fdad220291b833299783e359d9c7091c74b260f782012`  
		Last Modified: Thu, 25 Jan 2024 17:43:17 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d83d422a0ffe60ba589125b75f8dc2da43085c2528f05dcaf0bc1ffa16e59c`  
		Last Modified: Thu, 25 Jan 2024 17:43:17 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a12320c857db0fe3cfab783788f16c071d0ad782b0d73d92bf5d82820d6b64`  
		Last Modified: Thu, 25 Jan 2024 20:42:01 GMT  
		Size: 4.4 KB (4372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b93b40d0bf9b0c9a7796ac09d5b3d6b1a017ae1026df0695bb70278e7f7365`  
		Last Modified: Thu, 25 Jan 2024 20:42:09 GMT  
		Size: 51.3 MB (51277777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbaba91e54bad57c673a71f0516a588a571620d9e666007d68142ace261847be`  
		Last Modified: Thu, 25 Jan 2024 20:43:54 GMT  
		Size: 122.3 MB (122346910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cded02e4844cb3e2eea6c8863968593b07f041551df109f4f360e2f396484d4b`  
		Last Modified: Thu, 25 Jan 2024 20:43:49 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
