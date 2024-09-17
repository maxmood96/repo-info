## `gradle:jdk11-jammy`

```console
$ docker pull gradle@sha256:c657a7cfad2238d9f1f8141d39fc55dd8a91f5f3ca0e36c60de593cde68be719
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

### `gradle:jdk11-jammy` - linux; amd64

```console
$ docker pull gradle@sha256:cff16d71e74919f9ea78e535e96126c6cd74eb3c7da6cc6979a7fe3dd8faef51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.2 MB (377219670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7be040eb36f47eaf46c0b3312f4adc826fb91eb98349bd7174467ae280cf6d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 09 Sep 2024 18:59:34 GMT
ARG RELEASE
# Mon, 09 Sep 2024 18:59:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 18:59:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 18:59:34 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 18:59:34 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["gradle"]
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 09 Sep 2024 18:59:34 GMT
WORKDIR /home/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_VERSION=8.10.1
# Mon, 09 Sep 2024 18:59:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER gradle
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER root
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a925ab929ad30c9575f0f5adfd3cb8cae7ae5e9d76aa62360634e5a5a1217c`  
		Last Modified: Tue, 17 Sep 2024 01:07:21 GMT  
		Size: 12.9 MB (12870929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037f7ad340249c03b08fcb3689e1d698e72f966714599191cd3d4d644b5b0262`  
		Last Modified: Tue, 17 Sep 2024 01:08:33 GMT  
		Size: 145.6 MB (145559108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d799aa97b0a9369dc2186b90c55ddde300ee8d9263825aa54926f5e8deab9896`  
		Last Modified: Tue, 17 Sep 2024 01:08:21 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b216715d6ce690de6bbaca940720273dd1d6b660cfda5fd66e71558af045c432`  
		Last Modified: Tue, 17 Sep 2024 01:08:21 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f7b91de7e8df9af5c9213fa01db2ca8115ccbd938f89b88ff58167c234d6d`  
		Last Modified: Tue, 17 Sep 2024 02:00:14 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88594850e152398e66b993fd486f803dd1f4cca4545c37061c00d9550a4cba8e`  
		Last Modified: Tue, 17 Sep 2024 02:00:15 GMT  
		Size: 51.6 MB (51560323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e955737c57cf9eae794cd519d6544caccd67f6606dc8c76236076fd8f1939e34`  
		Last Modified: Tue, 17 Sep 2024 02:00:16 GMT  
		Size: 136.7 MB (136727843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037d28a7d46724014258bffb91cd89e6cf9c6d887f103bc80c3feb4ecdeb3a04`  
		Last Modified: Tue, 17 Sep 2024 02:00:14 GMT  
		Size: 54.9 KB (54908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:42abfedd95dcd339e7c48607ac5d991e54a1ce3ddbcc1d9b64c038658c1372da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7117774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155c27b4686dc44eaa00d50f9d70d966ff144993ffe8e4f43349bfa4b4549d5c`

```dockerfile
```

-	Layers:
	-	`sha256:b3ce7dd1938141671e9805f321db90e3c87483b0e7437a652f46f401cd7a303a`  
		Last Modified: Tue, 17 Sep 2024 02:00:14 GMT  
		Size: 7.1 MB (7094873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27af15e0f5e2f1541b121690e5551b123d10391f178e81cf25e37dc2e17734a`  
		Last Modified: Tue, 17 Sep 2024 02:00:14 GMT  
		Size: 22.9 KB (22901 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:383d204e2fc24b905460978b7197399414686514d11e4881b6ee484fbb603fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.7 MB (368658003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100458942e888031d75c764dfa2d494159d202e77db508bfa78b6a1a185f5791`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 09 Sep 2024 18:59:34 GMT
ARG RELEASE
# Mon, 09 Sep 2024 18:59:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 18:59:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 18:59:34 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 18:59:34 GMT
ADD file:291158c1d919b2d4290b5112a77dc0f7bdf0d45caa53b3556390707d29d2796a in / 
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["gradle"]
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 09 Sep 2024 18:59:34 GMT
WORKDIR /home/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_VERSION=8.10.1
# Mon, 09 Sep 2024 18:59:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER gradle
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER root
```

-	Layers:
	-	`sha256:35baf9f88f9b2cb840329dab5e6720d4fc535f9c150ca402cd7cd955065cd481`  
		Last Modified: Fri, 13 Sep 2024 12:45:25 GMT  
		Size: 27.5 MB (27534027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31edfebc2dc37b7fcd5adfb6ee3872ba74788ba24e8c2c3a40107b9fd85153c`  
		Last Modified: Tue, 17 Sep 2024 01:23:55 GMT  
		Size: 12.5 MB (12463235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454e2dbad66138305aac2fddafa46583967344da8430e203cb19aee1d40a034e`  
		Last Modified: Tue, 17 Sep 2024 01:25:08 GMT  
		Size: 138.0 MB (138036733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b561cd0b9b295942e0ea150243cb9461ab2c419157c307d958efb56a174838e`  
		Last Modified: Tue, 17 Sep 2024 01:24:55 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8302dc9e095dc856ba92e2e643c815e76d8188cb307ed265deaec92e1f234af3`  
		Last Modified: Tue, 17 Sep 2024 01:24:55 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cc17523d308b6a9bf0a8b07b25c41b16af54fd79db0f771a6ed1013457a1ce`  
		Last Modified: Tue, 17 Sep 2024 02:04:06 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5df6c47fec2b8afc6dc3dd32321c88a97a8d21bdf8e1baef705a7504fd9732`  
		Last Modified: Tue, 17 Sep 2024 02:04:09 GMT  
		Size: 53.9 MB (53889311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c8d4ccc11515ac8b79c3e3186eedc705afdbfcc0ba22e949eec1985155c101`  
		Last Modified: Tue, 17 Sep 2024 02:04:11 GMT  
		Size: 136.7 MB (136727799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de853b9f5dc987eb5df0e0c5e3dba18bf9e2feadac06852d79f4d27c3c141684`  
		Last Modified: Tue, 17 Sep 2024 02:04:07 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:17d5c3b9893e3ed149bc9b161a1a02b679dcd04f73fd7976d06372b213a10343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7118206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4248d9397f17e832f9c2b9ef169d01e79ef5b77ad3f47a7cfa886983adb5c72d`

```dockerfile
```

-	Layers:
	-	`sha256:a896efdb8577ab7ddc84facd6e14f147e69445de552b79072bec9215f39aa522`  
		Last Modified: Tue, 17 Sep 2024 02:04:07 GMT  
		Size: 7.1 MB (7095166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec8be9f986ed4d9c93f479f5948f3d7c259d0466b0f6eec5d288843d4a1869d9`  
		Last Modified: Tue, 17 Sep 2024 02:04:06 GMT  
		Size: 23.0 KB (23040 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c8e8442a138d30db1c7f8f997e0b4c753f79af9109820d603606f60f60f634b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.5 MB (371510373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4444c7fef19511f1291d5b8e72fbfe0b34a0a67fcf99e6d9617661cee1316ef`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 13 Aug 2024 09:28:17 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:28:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:28:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Aug 2024 09:28:20 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Tue, 13 Aug 2024 09:28:20 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["gradle"]
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 09 Sep 2024 18:59:34 GMT
WORKDIR /home/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_VERSION=8.10.1
# Mon, 09 Sep 2024 18:59:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER gradle
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER root
```

-	Layers:
	-	`sha256:f99601f39010ba98f3cb03ebfcc356cf14d93d5f585f680a3651901dce700f45`  
		Last Modified: Fri, 09 Aug 2024 02:12:50 GMT  
		Size: 28.4 MB (28397110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a13fc23d23d50177fc33d5df0e5c516fdbaae7d5cb53c11d634dff7e6e365e`  
		Last Modified: Sat, 17 Aug 2024 01:33:12 GMT  
		Size: 12.8 MB (12813299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f656d93317051f3cdb283b66fc2717d7d7d268b47856976ab7c6907d8e019676`  
		Last Modified: Sat, 17 Aug 2024 01:34:23 GMT  
		Size: 142.4 MB (142360696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918ef52692472e8ef39e46e84fc5d024069158d6d63705c7fc431b575592a2bd`  
		Last Modified: Sat, 17 Aug 2024 01:34:14 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb23af7d44149e17e19ad297bbdebad5bd0149f50058d45ef27526fb8da47f7f`  
		Last Modified: Fri, 23 Aug 2024 19:43:39 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3d36348418ae7c9e862b8409a6dfc43a7a072f3ed5f47b3b9a9f8ad1bafffb`  
		Last Modified: Mon, 09 Sep 2024 22:55:14 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11ecaaf077ee3cc810792f53746ea51814567d0e1af75ac50748d61ad319fe2`  
		Last Modified: Mon, 09 Sep 2024 22:55:15 GMT  
		Size: 51.1 MB (51145272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a374eb3c14e6aa3106aa9d04212da455229a302d5bdc68354e61a406a457f4e2`  
		Last Modified: Mon, 09 Sep 2024 22:55:18 GMT  
		Size: 136.7 MB (136727831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd823056d7bf574953682a4b908ff84ebe8c2896e848fb00ac0b392705ab1fc`  
		Last Modified: Mon, 09 Sep 2024 22:55:14 GMT  
		Size: 59.5 KB (59531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:dae4216afcbd39a51069b1b3ed3be5785ebb0b7cb4dc88109872e178bdec5a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7124633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03209ed7b8512a5e425746a89f9461ad29939d2c4d7abb34397aa3b2112037cd`

```dockerfile
```

-	Layers:
	-	`sha256:c58b26a7e9918e869476c626ffdef04f07261a49614ce22c520b360871b47b6a`  
		Last Modified: Mon, 09 Sep 2024 22:55:14 GMT  
		Size: 7.1 MB (7101367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:360981643d155ccbda91a86d05ca04c5928874aa4711529b7d49e8412e89b6d6`  
		Last Modified: Mon, 09 Sep 2024 22:55:14 GMT  
		Size: 23.3 KB (23266 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:803885c4866572536b8d60cb58fa2b69d1ecc87116c22cad552862577e785567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.5 MB (374463112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4caac40416fc14df7a5745866b88aadae340a8a9f78a8a81ba95be7d0544f5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 09 Sep 2024 18:59:34 GMT
ARG RELEASE
# Mon, 09 Sep 2024 18:59:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 18:59:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 18:59:34 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 18:59:34 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["gradle"]
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 09 Sep 2024 18:59:34 GMT
WORKDIR /home/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_VERSION=8.10.1
# Mon, 09 Sep 2024 18:59:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER gradle
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER root
```

-	Layers:
	-	`sha256:236617759af12844c70d91474e8f2748f6a9f3ac0963254dd335e676f7936871`  
		Last Modified: Tue, 17 Sep 2024 00:52:05 GMT  
		Size: 35.6 MB (35585488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d696101a4a3a03793ce680e8598666401008f4e60322822739c52ddc68887de`  
		Last Modified: Tue, 17 Sep 2024 01:05:41 GMT  
		Size: 13.7 MB (13714935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2aaa156444ab33e68b96cb44d9ae47fa6b6e48be1d02dee2c46178acdbfe6e`  
		Last Modified: Tue, 17 Sep 2024 01:07:02 GMT  
		Size: 132.8 MB (132755357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3225da20f12d9fb56f98e6541f4a1073d86406c0bb850ec3dee6441ad513d06`  
		Last Modified: Tue, 17 Sep 2024 01:06:49 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aecd142376b91b6d4e1f821255e0d6c2f41e5db86c92f411a4ca563205c35e7`  
		Last Modified: Tue, 17 Sep 2024 01:06:49 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39d54a3219279fd859a73d4b31e06efb5eb476bef2b9d73cf22bbc403b59758`  
		Last Modified: Tue, 17 Sep 2024 03:22:45 GMT  
		Size: 4.3 KB (4310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac863fc0f654ed8f9b40b11a2ae7a5fb0d32138631cc0693e2e93cf03277cc1e`  
		Last Modified: Tue, 17 Sep 2024 03:22:48 GMT  
		Size: 55.7 MB (55672586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b144cf91ca0be9100f70e63d5d847a778d63d61a2f955398bca0571eaefab11`  
		Last Modified: Tue, 17 Sep 2024 03:22:51 GMT  
		Size: 136.7 MB (136727829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7cc5c22d0e39a444743a3760f5e7e14ad7ed8f0475f6e61c9f93ee8ea60382`  
		Last Modified: Tue, 17 Sep 2024 03:22:46 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:08409b4b89536ce3d41fb974c93acf2970a3567602a028c65c1090c6e4262d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7125656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e61db8bc85819a9ccc81b516ef0cc4e73e954902c80e2ec984460c7e02c8c65`

```dockerfile
```

-	Layers:
	-	`sha256:d594c020593aae2e764d8e1b634821fe3541c9d987342c1c5bd358ceae94f8d2`  
		Last Modified: Tue, 17 Sep 2024 03:22:45 GMT  
		Size: 7.1 MB (7102689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce35fbed64bdcc430c2c7d22ad0e3137ff920b339e75f58722942b6688b6f6a8`  
		Last Modified: Tue, 17 Sep 2024 03:22:44 GMT  
		Size: 23.0 KB (22967 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:9ed96deff8eb1a2ac01a8a005d2f27a187807d56470debc2ae7909b58812dc1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.1 MB (355116700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8612098c02e3670857a3f94e010804fd9f8dfa9e57ef6fcc9d66283faaea0c68`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 09 Sep 2024 18:59:34 GMT
ARG RELEASE
# Mon, 09 Sep 2024 18:59:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Sep 2024 18:59:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Sep 2024 18:59:34 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Sep 2024 18:59:34 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        arm64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        armhf)          ESUM='9d14a076d1440161ab4c9736644e8e9f4719eb8e9f44c03470640960c3cd5e00';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64el)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
# Mon, 09 Sep 2024 18:59:34 GMT
CMD ["gradle"]
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 09 Sep 2024 18:59:34 GMT
WORKDIR /home/gradle
# Mon, 09 Sep 2024 18:59:34 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
ENV GRADLE_VERSION=8.10.1
# Mon, 09 Sep 2024 18:59:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER gradle
# Mon, 09 Sep 2024 18:59:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=1541fa36599e12857140465f3c91a97409b4512501c26f9631fb113e392c5bd1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 09 Sep 2024 18:59:34 GMT
USER root
```

-	Layers:
	-	`sha256:f9df71dee8900bd2b66db03a746f148929f7c0843181466bdcceef094456bf75`  
		Last Modified: Tue, 17 Sep 2024 01:28:20 GMT  
		Size: 28.6 MB (28639268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f167cb8c929ef00f2a29c0d4cae6d826f9e1395db78b9eb3ff0c70ff8f5b92`  
		Last Modified: Tue, 17 Sep 2024 01:38:50 GMT  
		Size: 13.0 MB (12955169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e54bf39b24ad37e63a68908fba59a15c4cb602df9cb6b316b640b01d7b1ce15`  
		Last Modified: Tue, 17 Sep 2024 01:38:57 GMT  
		Size: 125.5 MB (125524777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6853fe9c7bc5d8d672962d3506aebed9c155c9c4791116dd1b9828236e9b9a`  
		Last Modified: Tue, 17 Sep 2024 01:38:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b86c50d5a3703f45d99f59a86bf3be9336aab3c76f3af2686b3cae791538c2`  
		Last Modified: Tue, 17 Sep 2024 01:38:48 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d18378493eabd06253dcfcc6ad9a4c43f6069a8530e4379d4cc66b97d5342a9`  
		Last Modified: Tue, 17 Sep 2024 03:05:11 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a0f3cc46e13cfaa772d1f9807b27ef4bdc27394dd3a4c7bd7c40770a6b0b9e`  
		Last Modified: Tue, 17 Sep 2024 03:05:14 GMT  
		Size: 51.3 MB (51262735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6d2525f3fc5a3a3e62b40e043227e02a4eb4fc1554fc03c61a40918ab638e2`  
		Last Modified: Tue, 17 Sep 2024 03:05:15 GMT  
		Size: 136.7 MB (136727830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bf5008e503a361fc0b472af4ad465f5fc4af9c596c8ba9572528baf59d240b`  
		Last Modified: Tue, 17 Sep 2024 03:05:12 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-jammy` - unknown; unknown

```console
$ docker pull gradle@sha256:7999ab6ce79e00e5338f79247d702e1eae8dbf99ddabcebc0fe27ac763f3c5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7117575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5550590f3fe34a4a65e0c234419fe4364bef0d36229d534391645f4e1dd98c`

```dockerfile
```

-	Layers:
	-	`sha256:066ad6c5633c4309989d667cb568a35415efdda22865c4c662eb6d5fdc306f56`  
		Last Modified: Tue, 17 Sep 2024 03:05:11 GMT  
		Size: 7.1 MB (7094676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a6e03ad61c3262d2a561a59f02c413b4e4b4ae6c6b94b3aa2fcce735bbd9948`  
		Last Modified: Tue, 17 Sep 2024 03:05:11 GMT  
		Size: 22.9 KB (22899 bytes)  
		MIME: application/vnd.in-toto+json
