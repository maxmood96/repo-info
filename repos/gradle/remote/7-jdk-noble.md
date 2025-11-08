## `gradle:7-jdk-noble`

```console
$ docker pull gradle@sha256:1b0bbb4afed712b23de1feaa0185c021092a4f700ff6fb98945d60ca59bb40e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gradle:7-jdk-noble` - linux; amd64

```console
$ docker pull gradle@sha256:a06b6d9d6b64353bae13f66315d9d6461e3b0c4e2997d1c0e5c2a1d4f6bbbb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 MB (389699324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc63ba7cf5c260e8dac1c4e3f5958dfd157d3d7076b3f263a437f2dcaa071ab`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:44 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='fba21763f6553efb65d774f51ab6a347e67a69eb2bb2d26980cdf2ee0f35a6db';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:58:50 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 18:24:02 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 18:24:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 18:24:02 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 08 Nov 2025 18:24:02 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 18:24:02 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 18:24:19 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 08 Nov 2025 18:24:19 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 08 Nov 2025 18:24:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 08 Nov 2025 18:24:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 18:24:21 GMT
USER gradle
# Sat, 08 Nov 2025 18:24:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 18:24:21 GMT
USER root
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25920ebbd6a84721e1e5049be4abb4372aac6b434e2d35ecadb1e0531e9c829`  
		Last Modified: Sat, 08 Nov 2025 17:59:16 GMT  
		Size: 23.0 MB (22959363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c7168445ec5b684bbb75dd952c2f5ccc6f4fa9d7473349ea381615bfe0637b`  
		Last Modified: Sat, 08 Nov 2025 18:21:56 GMT  
		Size: 144.9 MB (144851049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45898453371862116f2fa2a01423984dca5a071ed2eaf303071a673dae89df1b`  
		Last Modified: Sat, 08 Nov 2025 17:59:14 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c42b4fc61f80b85e95d240e8b993ff3872653af5f525bdfb818646431eb40ac`  
		Last Modified: Sat, 08 Nov 2025 17:59:14 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dbfbd1a2590fa140878a8a4b2341bb60a3106a880eb299144691bd5f5e3e26`  
		Last Modified: Sat, 08 Nov 2025 18:24:50 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2135d41c04a2ee1aa87de99cb0d5b5d84d023d9517740e57899e5cf7d1668d63`  
		Last Modified: Sat, 08 Nov 2025 18:25:03 GMT  
		Size: 63.6 MB (63637693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5c28dde2b6e93fbff7ddfb469d728fd3fe18ea1dba822fd4bb1d0cf912859c`  
		Last Modified: Sat, 08 Nov 2025 21:22:33 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c970414df481c325ca2431ca4a70610a49cd33e0294f831c235ae617addef70a`  
		Last Modified: Sat, 08 Nov 2025 18:24:50 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:634802924e680f619d1e9a9d8e27d3a3d214089fc98f2c670ffbbac453d36650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe74c2b7a0732566e053077e5d2a2a03f342c16d35f0378d6d43dda88391d21`

```dockerfile
```

-	Layers:
	-	`sha256:29a983c3d4bd2e69bba3adb51f64231023f7092e627c0ed2cc369b7dc1bca4e5`  
		Last Modified: Sat, 08 Nov 2025 21:20:19 GMT  
		Size: 7.3 MB (7311632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca8d8fdc228bd0157950e2f54943d7732867399b06804efb92e7c0bba314dd74`  
		Last Modified: Sat, 08 Nov 2025 21:20:20 GMT  
		Size: 27.7 KB (27653 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk-noble` - linux; arm variant v7

```console
$ docker pull gradle@sha256:001ae73792b071f74b27456602f14bbc889ff749e058436668f03c4bb9b1b57a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.2 MB (385246331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b2a9d6a227e37530907a6681280e80d7ac056e8ce31e8e3e29921c8d9edad3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:27 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:27 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:31 GMT
ADD file:1ccdd7fca45ec88ba0ddda07e5e5acb6b40ddcb3023e0cbc04ffffdf4e30fb0a in / 
# Wed, 01 Oct 2025 13:02:31 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:55:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:55:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:55:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:55:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:55:15 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:55:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='fba21763f6553efb65d774f51ab6a347e67a69eb2bb2d26980cdf2ee0f35a6db';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:55:26 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:55:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:55:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:55:26 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 18:12:39 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 18:12:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 18:12:39 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 08 Nov 2025 18:12:39 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 18:12:39 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 18:13:44 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 08 Nov 2025 18:13:44 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 08 Nov 2025 18:13:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 08 Nov 2025 18:13:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 18:13:46 GMT
USER gradle
# Sat, 08 Nov 2025 18:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 18:13:47 GMT
USER root
```

-	Layers:
	-	`sha256:4afa85c5883c0db62b02025c149edaaa237af5ba25ea48039e875a802d465ac7`  
		Last Modified: Wed, 01 Oct 2025 18:03:16 GMT  
		Size: 26.9 MB (26851732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5945fc00cca8a9e7c8ced02c595076b8b378c2cfbe5e081383f82900cb4741e`  
		Last Modified: Sat, 08 Nov 2025 17:55:55 GMT  
		Size: 21.4 MB (21384668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce09966a198f2aaa0092a742f646a7e2d79621c2c2049addf2af02a3e52e71de`  
		Last Modified: Sat, 08 Nov 2025 18:12:37 GMT  
		Size: 142.3 MB (142329981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0678f9d654f6dafc844b52bc162473c81ae301142ff12371c204d78f404012a3`  
		Last Modified: Sat, 08 Nov 2025 17:55:53 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c98be88ba69082b70aa39413f98cc884544056b09e359de80a69d1f866c801`  
		Last Modified: Sat, 08 Nov 2025 17:55:53 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57a3fa92e71c29805401abcb4e933f9d4745cd4770b7fef67dbe57c381ad16e`  
		Last Modified: Sat, 08 Nov 2025 18:14:17 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713fec251096fb459b9ef59cc4f35159a78fcc3bed92f99b0b8a444620199a7d`  
		Last Modified: Sat, 08 Nov 2025 21:24:48 GMT  
		Size: 66.2 MB (66175466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f4e13688e26119f565ab770d248ce9c5b8f37f9bf4776d26990190442ff968`  
		Last Modified: Sat, 08 Nov 2025 21:24:42 GMT  
		Size: 128.5 MB (128469419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e931d7982f715f596dd9efe32745d76f18141871c6111d61639b1c1b8ed93cca`  
		Last Modified: Sat, 08 Nov 2025 18:14:17 GMT  
		Size: 31.3 KB (31304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:af4f0e681db3421e8eaedc3b049bd24ac58d97f8fc20fc68cd7696c4d6b14417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7278165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0591f2cb735c674b84550635925b266d927f91c22044295ecdc88b9df2cd65de`

```dockerfile
```

-	Layers:
	-	`sha256:e8c7aaf1fa590f357e4e1203536684f25053b337d80db9a337aab08f6472909a`  
		Last Modified: Sat, 08 Nov 2025 21:20:52 GMT  
		Size: 7.3 MB (7250280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50b67dc3821c8c7e1a58cfdbb7c17de910026a090d49689998665425ab4ceff5`  
		Last Modified: Sat, 08 Nov 2025 21:20:52 GMT  
		Size: 27.9 KB (27885 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk-noble` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ea71a38d1b294c7ae4339a4ce7796f708b208cfa75434a88d7f9fd3a4308c5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.3 MB (388329695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001593707daaf1d135f5a9f9d6b98e7668e033e41e53c776b0ed6d5fdb7add8d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:58:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:58:16 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='fba21763f6553efb65d774f51ab6a347e67a69eb2bb2d26980cdf2ee0f35a6db';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:58:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:58:23 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 18:24:14 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 18:24:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 18:24:14 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 08 Nov 2025 18:24:14 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 18:24:14 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 18:24:34 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 08 Nov 2025 18:24:34 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 08 Nov 2025 18:24:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 08 Nov 2025 18:24:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 18:24:36 GMT
USER gradle
# Sat, 08 Nov 2025 18:24:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 18:24:37 GMT
USER root
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561253e11209acbb43fcd6b388c3ddffbca64af1dcbc277fc57abdad62bf159f`  
		Last Modified: Sat, 08 Nov 2025 17:58:50 GMT  
		Size: 24.2 MB (24167132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469f4e46e93d94ef5404dbc9cd2c1262c5d42a1eab43113b343c428d3e2c92f9`  
		Last Modified: Sat, 08 Nov 2025 18:22:47 GMT  
		Size: 143.7 MB (143681466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e005444c1ba34cfa232667001d45aee7021a6ed83e7e96b65184777c0ce00b64`  
		Last Modified: Sat, 08 Nov 2025 17:58:49 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342c79245f97781260d40c83fa2256cfca9667676168b1eeaee191ac429046aa`  
		Last Modified: Sat, 08 Nov 2025 17:58:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d879b9e8841a5baabe8f3ed40b20725221cb13179a229d02b113519840843e9d`  
		Last Modified: Sat, 08 Nov 2025 18:25:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255e7c520954a83fcb76fa08ff07ec942a02c77f93711691ef4f9fb87d1b0a5`  
		Last Modified: Sat, 08 Nov 2025 18:25:18 GMT  
		Size: 63.1 MB (63086631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2215ca4ec07439fa7b11247f3a1af840937fac8b9ceaf48aada55f34008f46ea`  
		Last Modified: Sat, 08 Nov 2025 21:24:47 GMT  
		Size: 128.5 MB (128469467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642a7a5b309f48542308a27aec0670ffb75a78bf9c0d23f5ce3ed4d91e23284f`  
		Last Modified: Sat, 08 Nov 2025 18:25:08 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:02f26ecc3c8cdaddd4c753eed94063cae1ad4a82c434688e3194d4e3113de32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7477448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467828d99fa3057404a495fdec80611ea94fc7f419861dd21c87d6f01362f3fc`

```dockerfile
```

-	Layers:
	-	`sha256:fb76fea460da4d94bba76678f0c610f073d78332c657a0f5aa713608d9d3f17b`  
		Last Modified: Sat, 08 Nov 2025 21:20:58 GMT  
		Size: 7.4 MB (7449478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff70930a9a765c27a28e8782b4bfbf1dbda6f6c5efb68f1a5b298e6598ab00b3`  
		Last Modified: Sat, 08 Nov 2025 21:20:59 GMT  
		Size: 28.0 KB (27970 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk-noble` - linux; ppc64le

```console
$ docker pull gradle@sha256:dd994535dddcbdfc7c9d9eea44f75301350b9a62ee4f715641349ceb13087b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.3 MB (400330929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7957a38eec94e8d7a1acfe0aea93d9445547ae6d7b380f52f5da7cb4d3c17e72`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 18:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:11:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:11:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:11:52 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:12:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='fba21763f6553efb65d774f51ab6a347e67a69eb2bb2d26980cdf2ee0f35a6db';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:12:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:12:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:12:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:12:07 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 20:20:54 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 20:20:54 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 20:20:54 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 08 Nov 2025 20:20:54 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 20:20:54 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 20:21:29 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 08 Nov 2025 20:21:29 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 08 Nov 2025 20:21:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 08 Nov 2025 20:25:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 20:25:43 GMT
USER gradle
# Sat, 08 Nov 2025 20:25:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 20:25:43 GMT
USER root
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af803f8884d3afe1ea5fb332376bcda6dbb5106e6da31473c33181c55712ebaf`  
		Last Modified: Sat, 08 Nov 2025 18:12:55 GMT  
		Size: 24.1 MB (24103249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a07efb663f7ba00bb6cd6bd5d3a0e5e19d66e04c4ddefc150f219cee72a97b`  
		Last Modified: Sat, 08 Nov 2025 21:25:08 GMT  
		Size: 144.5 MB (144533791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5419e601e1b62471aa9b09c374d1e679a3d44cfea0883f3924301f14351919`  
		Last Modified: Sat, 08 Nov 2025 18:12:53 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb0dd49e55f1dc220fcda5120553d2a894ec2b7da8a2e6f16ad72a109d787b5`  
		Last Modified: Sat, 08 Nov 2025 18:12:53 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7298d45db5043eb4c4290c863516eee528ffab34adedf6102d39b805bacdd6`  
		Last Modified: Sat, 08 Nov 2025 20:22:37 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fa023f100ad5ae10f6fa16d4f4f8251b63a73c65012a9208fa673fbb98ae98`  
		Last Modified: Sat, 08 Nov 2025 20:22:48 GMT  
		Size: 68.9 MB (68882190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1c2bf19a99cb3972923068c73b25e864799b88235365fc1423691554e90a35`  
		Last Modified: Sat, 08 Nov 2025 21:24:52 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6b4c198441996dfa9c4683c7d4737b8850823f551071ab539e4daf9c0c66e7`  
		Last Modified: Sat, 08 Nov 2025 20:26:30 GMT  
		Size: 35.0 KB (35002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:a4637cb0d2e00aba0c2c7fb5786ba3120664f74053d8ad85ad51775efedd9b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7390612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9f9249af5ff86bf48b43f9ada112dc1f317b0602c734d7c4e99392118231c8`

```dockerfile
```

-	Layers:
	-	`sha256:ad8dee543fc3bd2e18211f6f80df0a82eaf3f43dac06c106a4cb7675ef825dfb`  
		Last Modified: Sat, 08 Nov 2025 21:21:04 GMT  
		Size: 7.4 MB (7362824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db679391135d804a2a016f410405f5599f67a8f55452df4c869a946ac961a8af`  
		Last Modified: Sat, 08 Nov 2025 21:21:05 GMT  
		Size: 27.8 KB (27788 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk-noble` - linux; riscv64

```console
$ docker pull gradle@sha256:414bfe0ff50b90bf4b920443f66e11526b8fcfa9e98ec6175abd6df1cac93989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 MB (389820669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7257785bc0dc0f98303355fa7b4aa6eec5321d968aecd56e99a4500a19c38137`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:857dc87fbafae31881cff8c69aed267a033f5df226dd351ee89de918ad5678ce in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        arm64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        armhf)          ESUM='bc8ba665df25378cfca76b2d2ca6821ba32c4d45934aa5beea5b542d6658f5d6';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64el)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        riscv64)          ESUM='42cc01235222a27576de8331a532da200ce36c9d155c93e9e0b4d565dcaf684a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 23 Sep 2025 15:37:00 GMT
CMD ["gradle"]
# Tue, 23 Sep 2025 15:37:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 23 Sep 2025 15:37:00 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 23 Sep 2025 15:37:00 GMT
WORKDIR /home/gradle
# Tue, 23 Sep 2025 15:37:00 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 23 Sep 2025 15:37:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 23 Sep 2025 15:37:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
USER gradle
# Tue, 23 Sep 2025 15:37:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
USER root
```

-	Layers:
	-	`sha256:ff47a256ba51b80e9880bc96be4ac2f094c47e0fcd7eec71bab85787cfa54b8b`  
		Last Modified: Mon, 13 Oct 2025 04:10:18 GMT  
		Size: 31.0 MB (30951381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ab17616cf4e436097dac72b5902ca2cd73114fe92dc0252d55ec741bd29f55`  
		Last Modified: Wed, 15 Oct 2025 06:43:49 GMT  
		Size: 20.1 MB (20143051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551035489d743f17dc9740f3c01b799c7d98b9883451ccb9480760aadc3b4234`  
		Last Modified: Wed, 15 Oct 2025 09:15:47 GMT  
		Size: 138.6 MB (138580506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a88fe41db3f5505f916ebc5c378fca961448a3cfe5efaada32fd02f9b995cd2`  
		Last Modified: Wed, 15 Oct 2025 06:43:47 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b81bb73b26c3bac26deebbdec70892c0e1d5ba5913751f81f98d8564db2059`  
		Last Modified: Wed, 15 Oct 2025 06:43:47 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35baf8f9885781a12d6702617fc1d49ae2c453146d31276dc16db4ab1464591`  
		Last Modified: Thu, 16 Oct 2025 01:07:10 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f079c896a458934ff4fc4e36dd2ceb20f1c2fe2c15a550630b13a56d61c903`  
		Last Modified: Thu, 16 Oct 2025 01:35:43 GMT  
		Size: 71.6 MB (71637532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5a0bc9a562645734ed82610a6af6f04c7cfb0abe24c026a2190f8093d03bb0`  
		Last Modified: Thu, 16 Oct 2025 02:08:58 GMT  
		Size: 128.5 MB (128469418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e5eabda9e9221d9853bf2e432c5d9bea0fae16acc003834a589afcaa152eb2`  
		Last Modified: Thu, 16 Oct 2025 01:41:40 GMT  
		Size: 35.0 KB (35019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:3db8bb4403b3017bc85a3f19688f54820405a036184a13038342b0d0e9572f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74fb2d5fa3b404bea529e798e0ec52e4301ecbe8e33d53bd2338f02fa709bfa2`

```dockerfile
```

-	Layers:
	-	`sha256:47ad7adc0f839aa4c3895bf68c08d55d2da5d0e180b4130f0b51ab4a71953309`  
		Last Modified: Thu, 16 Oct 2025 02:18:21 GMT  
		Size: 7.4 MB (7413564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a1489e0acfea22520c3fa04f40ed171beae90e370f71943a9644899507436d6`  
		Last Modified: Thu, 16 Oct 2025 02:18:22 GMT  
		Size: 27.8 KB (27827 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk-noble` - linux; s390x

```console
$ docker pull gradle@sha256:326a1dc419ca4c908d8e0139556db1004f6e651daa5304178185e5e54317ae26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.8 MB (380752908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0243748404d98144cf5d0d33b787085a5d0abe45795952963c14670055f7c315`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:05 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:06 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:07 GMT
ADD file:1c921a1d937949898d3d4ba499ce8d41425fe6dd2c8fdbcddd0070f2699f05b2 in / 
# Wed, 01 Oct 2025 13:02:07 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 18:01:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:01:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:01:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:01:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:01:40 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:01:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        arm64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        armhf)          ESUM='a0129be48dfbd16b7c6a158bf9e91683be2e292c473085294a6d436bbc5f4ea9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_arm_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64el)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        riscv64)          ESUM='fba21763f6553efb65d774f51ab6a347e67a69eb2bb2d26980cdf2ee0f35a6db';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 18:01:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:01:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:01:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:01:50 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 18:24:29 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 18:24:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 18:24:29 GMT
RUN set -o errexit -o nounset     && echo "Renaming ubuntu user and group to gradle"     && groupmod --new-name gradle ubuntu     && mkdir /home/gradle     && usermod --login gradle --home /home/gradle --groups gradle ubuntu     && chown gradle /home/gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 08 Nov 2025 18:24:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 18:24:29 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 18:29:08 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         make                 unzip                 brz         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which brz     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 08 Nov 2025 18:29:08 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 08 Nov 2025 18:29:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 08 Nov 2025 18:38:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 18:38:50 GMT
USER gradle
# Sat, 08 Nov 2025 18:38:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 18:38:52 GMT
USER root
```

-	Layers:
	-	`sha256:67735b72a65d308a2c2c9505d0d6e8419b7f2654a16cbd56963d88e01202d507`  
		Last Modified: Wed, 01 Oct 2025 15:43:10 GMT  
		Size: 29.9 MB (29906151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cfa5332fec2dcb147043885d5f4d85503b0e5f3e3b8897a9485fc9daa1b15c`  
		Last Modified: Sat, 08 Nov 2025 18:02:23 GMT  
		Size: 22.1 MB (22130373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f931bf9601922561dda01872949af57d5540f4c0ca6e02522e98fe9f852ed4c9`  
		Last Modified: Sat, 08 Nov 2025 19:40:49 GMT  
		Size: 134.9 MB (134863740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271e096f910d75229ad43b3669caa71acdf86820f1f66c3abe1fd002beece148`  
		Last Modified: Sat, 08 Nov 2025 18:02:22 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb3019c952600008c28cc038da9f43884573c40f4abc3ab06c479886373e051`  
		Last Modified: Sat, 08 Nov 2025 18:02:22 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dd9777fc2ebb1623a2a38a4e89cf3b9db7f35379b594d121993cdd3afb6371`  
		Last Modified: Sat, 08 Nov 2025 18:29:59 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9befd4e6c869c896cf8596f84938c5e16d9ea7ed4bbe089fe93f48b4706754d1`  
		Last Modified: Sat, 08 Nov 2025 18:30:10 GMT  
		Size: 65.3 MB (65344448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f08f4d9b0f69602a8ae499fc1abb8fce38322bf9df3b4409aeecc6871cb6427`  
		Last Modified: Sat, 08 Nov 2025 21:25:00 GMT  
		Size: 128.5 MB (128469420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f242006a5da657211170a35fb650749b7c105cf4e9703cb11baed0d8754722d9`  
		Last Modified: Sat, 08 Nov 2025 20:18:30 GMT  
		Size: 35.0 KB (35008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-noble` - unknown; unknown

```console
$ docker pull gradle@sha256:b29649b96d29bfc573af88ed8012fd610012716c5f54b72cda5ff30b675ac596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7284587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ec2d107b44bd3e22d172a8d24718a6d3e7bd5b89d5382554fd9763907d99a0`

```dockerfile
```

-	Layers:
	-	`sha256:e8bccf065410fc8a81fe9cd8d881cc53a90948e9c561e6cde57d5f89ca7c215b`  
		Last Modified: Sat, 08 Nov 2025 21:21:16 GMT  
		Size: 7.3 MB (7256933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50ebbc21891133b5323a057a59e3a8dacda110e0122be6a26306ce878b01bd41`  
		Last Modified: Sat, 08 Nov 2025 21:21:17 GMT  
		Size: 27.7 KB (27654 bytes)  
		MIME: application/vnd.in-toto+json
