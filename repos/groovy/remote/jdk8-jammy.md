## `groovy:jdk8-jammy`

```console
$ docker pull groovy@sha256:b5989fa8dd6374b21eb5c88ac6dda7d6868362ac8d532e1b758f6992d15dec6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `groovy:jdk8-jammy` - linux; amd64

```console
$ docker pull groovy@sha256:72aad4f8ee358cf1ee6a99ca7b82846836d0c815cf50c4bc3716cdb754cf46f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180512724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a812d9a00d720cee5540ca2d8fa3b595d7a10a6b6185907859f2e6fe6de5ae`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 28 Mar 2024 02:48:23 GMT
CMD ["groovysh"]
# Thu, 28 Mar 2024 02:48:23 GMT
ENV GROOVY_HOME=/opt/groovy
# Thu, 28 Mar 2024 02:48:24 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy
# Thu, 28 Mar 2024 02:48:24 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Thu, 28 Mar 2024 02:48:24 GMT
WORKDIR /home/groovy
# Thu, 28 Mar 2024 02:48:30 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/*
# Thu, 28 Mar 2024 02:48:30 GMT
ENV GROOVY_VERSION=4.0.20
# Thu, 28 Mar 2024 02:48:39 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy
# Thu, 28 Mar 2024 02:48:40 GMT
USER 1000:1000
# Thu, 28 Mar 2024 02:48:41 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcf356fa6e6902e661a53c29cf3b351f284090cb2c0de2ad6c5c238a6fdb9a8`  
		Last Modified: Thu, 28 Mar 2024 02:03:28 GMT  
		Size: 12.9 MB (12904693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf62b0dd6e4e68ab72316aeb589f5593b8c17e9c1c7713578bf3fcda29bd50fd`  
		Last Modified: Thu, 28 Mar 2024 02:03:33 GMT  
		Size: 103.6 MB (103601321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdbcbf92947e43bf222292a1e0d251f46ddfeb5e0924a6638653e972e1660d35`  
		Last Modified: Thu, 28 Mar 2024 02:03:25 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401c25db2ebafaaede733d2b3e5cd7dc70e004edd4e8b8fbe8768a80106825ec`  
		Last Modified: Thu, 28 Mar 2024 02:03:25 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a682a3b517e3b9ab339f343f2890c4fd845aa53a70ef80238324746cf71b54`  
		Last Modified: Thu, 28 Mar 2024 02:51:01 GMT  
		Size: 4.4 KB (4388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acef9815606ae06013e563b829052937f5cf5718297810b099f91067513d83d4`  
		Last Modified: Thu, 28 Mar 2024 02:51:02 GMT  
		Size: 3.7 MB (3739312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbec98924cf50fe21ac38af4dec3dd1aa8ba9fa15461bd665c0be5855b8b884`  
		Last Modified: Thu, 28 Mar 2024 02:51:03 GMT  
		Size: 29.8 MB (29810645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3907fa79f6a5c7cef89592911b3994ee072f2d0845081809730fa65947e256d`  
		Last Modified: Thu, 28 Mar 2024 02:51:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `groovy:jdk8-jammy` - linux; arm variant v7

```console
$ docker pull groovy@sha256:a7320b40836675ae907c1d9a98a8223c0d880287496ea8f3d9de499ad17f4cf7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172949046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bf68821f9d2757a2cece2c84040bc8f6355afed6cc9298322068b603ecac92`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 10 Apr 2024 19:09:04 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:09:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:09:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 19:09:15 GMT
ADD file:f06c8189c311b0927a0efa31910e5bea10b17d8efb376240376fef41170e3a6a in / 
# Wed, 10 Apr 2024 19:09:16 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 16 Apr 2024 02:55:16 GMT
CMD ["groovysh"]
# Tue, 16 Apr 2024 02:55:16 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 16 Apr 2024 02:55:17 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy
# Tue, 16 Apr 2024 02:55:17 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 16 Apr 2024 02:55:17 GMT
WORKDIR /home/groovy
# Tue, 16 Apr 2024 02:55:27 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/*
# Tue, 16 Apr 2024 02:55:27 GMT
ENV GROOVY_VERSION=4.0.20
# Tue, 16 Apr 2024 02:55:38 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy
# Tue, 16 Apr 2024 02:55:38 GMT
USER 1000:1000
# Tue, 16 Apr 2024 02:55:40 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:8e34fc49fc731bf85ce0a83deec49456ee2c584bf1a5c472db447d8a9b9a06cb`  
		Last Modified: Fri, 12 Apr 2024 01:35:18 GMT  
		Size: 27.5 MB (27533083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fcdb6b302d1f197eacdca37c53a51b762670c261ce3f687c83be6f26ee6ab6`  
		Last Modified: Tue, 16 Apr 2024 01:53:36 GMT  
		Size: 12.5 MB (12492494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9549270c0400020ac4d39910dbdba7b68460d48b89cb3df9802bc28eca7fc90`  
		Last Modified: Tue, 16 Apr 2024 01:53:42 GMT  
		Size: 99.2 MB (99229838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6947c43b4b7c229a60942600268e0a4a73ff660354cab49692bb0a2bf090cf`  
		Last Modified: Tue, 16 Apr 2024 01:53:33 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86878729b01a16bc2d8ee3c9f922b443373e5ef206dc26dad25b27e18fd37b1`  
		Last Modified: Tue, 16 Apr 2024 01:53:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d7b589a493a0eaf4c0cb201c70ffa5fc83dea7520fbbf7fb6d8255a68e3435`  
		Last Modified: Tue, 16 Apr 2024 02:56:48 GMT  
		Size: 4.4 KB (4375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756ebd34f33695d0bacc9b0fefd1816203ab96233cb7fa354f2cf3ae6a56393d`  
		Last Modified: Tue, 16 Apr 2024 02:56:49 GMT  
		Size: 3.9 MB (3877562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484905c6b58d5df452bc875a70d14d40dded6feac7286e8460c6c03cab3524d4`  
		Last Modified: Tue, 16 Apr 2024 02:56:51 GMT  
		Size: 29.8 MB (29810627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a855bfa694020b49bec88d6710407d8ec8b42d826672b17ca93e4adefb6c627`  
		Last Modified: Tue, 16 Apr 2024 02:56:48 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `groovy:jdk8-jammy` - linux; arm64 variant v8

```console
$ docker pull groovy@sha256:8aa511203b2cbe5f3dbdc2583d66b866e3954efce13d0c09671996ed23d22a9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177477985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4755d40863c14c10fe8f41dfb854cf365c6fcd2de6abd31de541845c4660a45`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 16 Apr 2024 07:17:18 GMT
CMD ["groovysh"]
# Tue, 16 Apr 2024 07:17:18 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 16 Apr 2024 07:17:18 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy
# Tue, 16 Apr 2024 07:17:18 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 16 Apr 2024 07:17:18 GMT
WORKDIR /home/groovy
# Tue, 16 Apr 2024 07:17:25 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/*
# Tue, 16 Apr 2024 07:17:25 GMT
ENV GROOVY_VERSION=4.0.20
# Tue, 16 Apr 2024 07:17:50 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy
# Tue, 16 Apr 2024 07:17:50 GMT
USER 1000:1000
# Tue, 16 Apr 2024 07:17:51 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62af4570e03cd18721264dca7618ad8bfe7fc52046caf98dd92dbd19a11ae3bf`  
		Last Modified: Tue, 16 Apr 2024 02:55:33 GMT  
		Size: 12.8 MB (12847096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf5b9b92f83f681a3f91c9cb85f608bc30c6d4ec302783cfd703738ea3fae8e`  
		Last Modified: Tue, 16 Apr 2024 02:55:38 GMT  
		Size: 102.7 MB (102705855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4065d353278a49c3128c777d20e01d3df8ef30765213e3ced91f979533b131`  
		Last Modified: Tue, 16 Apr 2024 02:55:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7e61e73d177d812a79aa62fd956d1ec4986f0d3229b0b27f43f7496e463dcf`  
		Last Modified: Tue, 16 Apr 2024 02:55:32 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dda856a244b2710dd0d48a7340e73cc1f24b19f92d2abed76305fba3728e50`  
		Last Modified: Tue, 16 Apr 2024 07:20:34 GMT  
		Size: 4.4 KB (4395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f391a33c1c812cc6cee10995631cc0660e3ea154b518e85d4941c68cf03bea4b`  
		Last Modified: Tue, 16 Apr 2024 07:20:34 GMT  
		Size: 3.7 MB (3708640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b547f9467474e1ab89447bc94ca889560e28b8eecf5a5851d80dafffbfc88b01`  
		Last Modified: Tue, 16 Apr 2024 07:20:36 GMT  
		Size: 29.8 MB (29810638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe3b864231f6e0878d5190dc24788bf6a1ccbd066e6ac5f90f54ca9b1e13149`  
		Last Modified: Tue, 16 Apr 2024 07:20:34 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `groovy:jdk8-jammy` - linux; ppc64le

```console
$ docker pull groovy@sha256:d3c945250f00077352ae04419b09fe5ec7cf3308609a0f17932b83f5ae908a99
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184679377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3986829efe81fa32a65c7ab7ddde7c3a668812787cbc6f573c4e0d65232d9cb6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["groovysh"]`

```dockerfile
# Wed, 10 Apr 2024 18:53:14 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:53:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:53:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:53:18 GMT
ADD file:417bf7a0c7958ce23aaf2e92c63328e2bc36835d1c9b8c8302702ba8bdf3cc7b in / 
# Wed, 10 Apr 2024 18:53:18 GMT
CMD ["/bin/bash"]
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jan 2024 11:07:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 11:07:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='241a72d6f0051de30c71e7ade95b34cd85a249c8e5925bcc7a95872bee81fd84';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u402b06.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fcfd08abe39f18e719e391f2fc37b8ac1053075426d10efac4cbf8969e7aa55e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u402b06.tar.gz';          ;;        armhf|arm)          ESUM='271f28c7b3592b201b7434292c21d923f520af8ff1c090b6849cb946e34a6bdb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u402b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='64bc05cdffe827c84000177dca2eb4ff0a8ff0021889bb75abff3639d4f51838';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u402-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u402b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 16 Apr 2024 06:12:54 GMT
CMD ["groovysh"]
# Tue, 16 Apr 2024 06:12:55 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 16 Apr 2024 06:12:56 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && groupadd --system --gid 1000 groovy     && useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown --recursive groovy:groovy /home/groovy     && chmod --recursive 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln --symbolic /home/groovy/.groovy /root/.groovy
# Tue, 16 Apr 2024 06:12:56 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 16 Apr 2024 06:12:57 GMT
WORKDIR /home/groovy
# Tue, 16 Apr 2024 06:13:14 GMT
RUN set -o errexit -o nounset     && apt-get update     && echo "Installing build dependencies"     && apt-get install --yes --no-install-recommends         dirmngr         gnupg         unzip         wget     && rm --recursive --force /var/lib/apt/lists/*
# Tue, 16 Apr 2024 06:13:14 GMT
ENV GROOVY_VERSION=4.0.20
# Tue, 16 Apr 2024 06:13:28 GMT
RUN set -o errexit -o nounset     && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm --recursive --force "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && rm --force "${GROOVY_HOME}/lib/groovy-raw-${GROOVY_VERSION}-raw.jar"     && ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy
# Tue, 16 Apr 2024 06:13:29 GMT
USER 1000:1000
# Tue, 16 Apr 2024 06:13:32 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:fdd7d0bd8ffc52196a33ea69f83c6ade1ff36b223484bae6626aa6f7db714a40`  
		Last Modified: Tue, 16 Apr 2024 02:34:05 GMT  
		Size: 35.6 MB (35587250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27059a37dad5b2569dc7e52921098941cfcaf0d5cde7c56e3a893ad1e2f636f`  
		Last Modified: Tue, 16 Apr 2024 02:49:35 GMT  
		Size: 13.8 MB (13767192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0f9da2feb6df5ec14f058f954b3427daa6530a401f882ef48b292259023c32`  
		Last Modified: Tue, 16 Apr 2024 02:49:44 GMT  
		Size: 101.1 MB (101070326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9471df0774c293ca9a01b1c7052835f432157ebf2110a661ad5382fcbce098`  
		Last Modified: Tue, 16 Apr 2024 02:49:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def833364bc06a3bef19a6bcc6e5bb9862ff426cc04648b17090ce02d42e3de1`  
		Last Modified: Tue, 16 Apr 2024 02:49:31 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0576dae04604fec6cecdec90b6df4902f91c2ab3f5636d9c267573e11e24768c`  
		Last Modified: Tue, 16 Apr 2024 06:15:22 GMT  
		Size: 4.4 KB (4385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6248abe58c9fee09da8e77040a79c25735cd6f43bab79c9da1ca901ed7048083`  
		Last Modified: Tue, 16 Apr 2024 06:15:24 GMT  
		Size: 4.4 MB (4438514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2927d1ce0e62a65082a70c1184215502e8def2a8f432903090efc6f7b820bbc`  
		Last Modified: Tue, 16 Apr 2024 06:15:25 GMT  
		Size: 29.8 MB (29810646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c984208ac4b5492fd65e65ee9aa72af80616e8470157b4b6629a2e301739b0f0`  
		Last Modified: Tue, 16 Apr 2024 06:15:24 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
