## `gradle:7-jdk11-jammy`

```console
$ docker pull gradle@sha256:d8fa3ba88ea68ce68c1c5cc906eef9df3850e34cdc585c7b8439240c5ef1aebd
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
$ docker pull gradle@sha256:ba4452c2eb2ec434ee7f07856f73341ceb760a18d51805b26e5ef38d041b6819
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363140711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5954e1d9fa46e5f75736b8a92befeab3de8552ccb75db966f30300ff9692e28`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Thu, 02 May 2024 01:23:21 GMT
CMD ["gradle"]
# Thu, 02 May 2024 01:23:21 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 02 May 2024 01:23:21 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 02 May 2024 01:23:22 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 02 May 2024 01:23:22 GMT
WORKDIR /home/gradle
# Thu, 02 May 2024 01:23:37 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 02 May 2024 01:28:46 GMT
ENV GRADLE_VERSION=7.6.4
# Thu, 02 May 2024 01:28:46 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Thu, 02 May 2024 01:28:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Thu, 02 May 2024 01:28:51 GMT
USER gradle
# Thu, 02 May 2024 01:28:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Thu, 02 May 2024 01:28:52 GMT
USER root
```

-	Layers:
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce394e5c05f6275f1a3d93ef078caadf4c6e88066e708ffa5cea964ded0c3c2`  
		Last Modified: Thu, 02 May 2024 01:15:30 GMT  
		Size: 12.9 MB (12905606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d13a1bac478ecdcd0a824e7609646cd9aba5a9828352c161e7fde32747890a`  
		Last Modified: Thu, 02 May 2024 01:16:57 GMT  
		Size: 145.5 MB (145509253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fadf6d894d85943f49b4e59e8272d27654b4e9c8ae02ca6a6e17deab85b98b`  
		Last Modified: Thu, 02 May 2024 01:16:46 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d024cc4e78781d92d449d73694e89c2b09f4d2ae2845b781f369c42905ae66ee`  
		Last Modified: Thu, 02 May 2024 01:16:46 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07651f51ba08103e55d206bc647c62c6e01e0c688eea6fea7328850d1a0dd6d7`  
		Last Modified: Thu, 02 May 2024 01:32:57 GMT  
		Size: 4.4 KB (4354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9edd6a3c25b5be22830d2dc9e0ff23788dea73937cf4e67fa8ba002a4cf9c24`  
		Last Modified: Thu, 02 May 2024 01:33:06 GMT  
		Size: 51.6 MB (51550511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4bc5ba545783364e327843bfaab96a8333b044a8e4e3c07e39efa9c93b521b7`  
		Last Modified: Thu, 02 May 2024 01:39:02 GMT  
		Size: 122.7 MB (122730258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ceb26ff7d43ce170930f467b531f865280c1e099bf416e1359e17499ffeb36c`  
		Last Modified: Thu, 02 May 2024 01:38:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk11-jammy` - linux; arm variant v7

```console
$ docker pull gradle@sha256:944a50c9001a34418bbb104687ed64ba711a71799eacf161abe5942834fe3361
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354661478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a530567f44acf4557d11c11f6fdc2bdc3ee051507cb2065b97f8213f7de13b2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Apr 2024 14:35:06 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:35:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:35:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:35:06 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:35:17 GMT
ADD file:ab2e95a123b006ac900aaaf0d1858b88941c8d319f47e41733db6f0f5fe98b87 in / 
# Sat, 27 Apr 2024 14:35:18 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Thu, 02 May 2024 02:29:14 GMT
CMD ["gradle"]
# Thu, 02 May 2024 02:29:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 02 May 2024 02:29:15 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 02 May 2024 02:29:15 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 02 May 2024 02:29:15 GMT
WORKDIR /home/gradle
# Thu, 02 May 2024 02:29:31 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 02 May 2024 02:31:37 GMT
ENV GRADLE_VERSION=7.6.4
# Thu, 02 May 2024 02:31:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Thu, 02 May 2024 02:31:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Thu, 02 May 2024 02:31:43 GMT
USER gradle
# Thu, 02 May 2024 02:31:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Thu, 02 May 2024 02:31:44 GMT
USER root
```

-	Layers:
	-	`sha256:b7e19bb2918236ac8ccf2faf405ff5a9521a86762ef07ef60917aa41d6dc8155`  
		Last Modified: Mon, 29 Apr 2024 07:54:39 GMT  
		Size: 27.5 MB (27536224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e5c703cbff6ae09d1210453797a0781455500f04990cb48a4001c468ac0921`  
		Last Modified: Thu, 02 May 2024 01:27:59 GMT  
		Size: 12.5 MB (12494270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aca631c59555eed552d64fcd4e04b98dbe8a2501f19fdb5ebe2d0b94417e49a`  
		Last Modified: Thu, 02 May 2024 01:29:20 GMT  
		Size: 138.0 MB (138004610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ba1dbbbe8110cd3779eb5198926d4c5093289410714a0a249d2f6e1420cbcd`  
		Last Modified: Thu, 02 May 2024 01:29:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a35cedab49694ec9337deb3a17a69fdadc25456aee53f007e8d767488a8ade`  
		Last Modified: Thu, 02 May 2024 01:29:08 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b277dbb168e690a416bf1ed18ad7738e98f1bf325ce1c7d0decc0e4c2c1f20`  
		Last Modified: Thu, 02 May 2024 02:35:09 GMT  
		Size: 4.3 KB (4341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce32246237ca076707ac6dab00a9afa6ed35e6e623d850dbb4b56c899c10060d`  
		Last Modified: Thu, 02 May 2024 02:35:18 GMT  
		Size: 53.9 MB (53890732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47b68663ae22c6faef573874b713a3e8007dd3bca4efd8a1e56fb5ccf6453d6`  
		Last Modified: Thu, 02 May 2024 02:38:05 GMT  
		Size: 122.7 MB (122730222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92720d566fdf2f8f17b22803e3cd0f6f68d330d7a87766ba1ca35cddb91e86f`  
		Last Modified: Thu, 02 May 2024 02:37:58 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk11-jammy` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:60671893ad398c2ad68746c04c61e6ce3ce08f361a727c0cb08e506d50546333
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.4 MB (357416801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b83d5356d6fd553f614de2d8b42687a10a1244782e0e7bbe6e630fef37a77c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Fri, 26 Apr 2024 04:02:43 GMT
CMD ["gradle"]
# Fri, 26 Apr 2024 04:02:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 26 Apr 2024 04:02:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 26 Apr 2024 04:02:44 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 26 Apr 2024 04:02:44 GMT
WORKDIR /home/gradle
# Fri, 26 Apr 2024 04:02:57 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 26 Apr 2024 04:05:12 GMT
ENV GRADLE_VERSION=7.6.4
# Fri, 26 Apr 2024 04:05:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Fri, 26 Apr 2024 04:05:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Fri, 26 Apr 2024 04:05:17 GMT
USER gradle
# Fri, 26 Apr 2024 04:05:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Fri, 26 Apr 2024 04:05:18 GMT
USER root
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f037ef0398100188bd636ef3da1525cc5cc7f04347a802ecc28ba3240408631`  
		Last Modified: Thu, 25 Apr 2024 21:59:12 GMT  
		Size: 12.8 MB (12846901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d7019dd12a4dbeada6f552e74528388a044b0aff455c1a08400b793feedcea`  
		Last Modified: Thu, 25 Apr 2024 22:00:29 GMT  
		Size: 142.3 MB (142312883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8d1faacb848a9e7ba67fe6821019d2e88da438ce48d82854608e87486d80a9`  
		Last Modified: Thu, 25 Apr 2024 22:00:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910357abf97ff617aa26ddf310a00781560493c85424eb0b17f2176995f46402`  
		Last Modified: Thu, 25 Apr 2024 22:00:21 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b1e395bd1e058d5d02689070f3c2d35542deba7ff4bc65c4cc24a34e12f79b`  
		Last Modified: Fri, 26 Apr 2024 04:08:34 GMT  
		Size: 4.4 KB (4368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee7cfd7724ead9179286ac41746e39ab3cd026544517db38e1b20575f64c15e`  
		Last Modified: Fri, 26 Apr 2024 04:08:41 GMT  
		Size: 51.1 MB (51120307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1129863b079d302d40334d0b9a42d47a8c7154d2026934af7787f91b048e35`  
		Last Modified: Fri, 26 Apr 2024 04:12:19 GMT  
		Size: 122.7 MB (122730262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6088713bdc7d171befcf53d0988105236e0bb6c70f47c9768c3feedba315d4cc`  
		Last Modified: Fri, 26 Apr 2024 04:12:14 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk11-jammy` - linux; ppc64le

```console
$ docker pull gradle@sha256:8ab3051de1a905b93b1d9b8a039e809023c453b72cdad868fdeacb46cde26c76
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.5 MB (360486526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29472a6b5e33b65c5ce7affbf5217ad75a4782f4a415113e6333c0c9ff87276c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 17 Apr 2024 17:51:23 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:51:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:51:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:51:23 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:51:27 GMT
ADD file:a6dad5ca890a7e93d717612d191eff2d9bbab6f9cef18c588630297bd6a61cc4 in / 
# Wed, 17 Apr 2024 17:51:27 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Thu, 25 Apr 2024 23:46:30 GMT
CMD ["gradle"]
# Thu, 25 Apr 2024 23:46:31 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 25 Apr 2024 23:46:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 25 Apr 2024 23:46:34 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 25 Apr 2024 23:46:34 GMT
WORKDIR /home/gradle
# Thu, 25 Apr 2024 23:47:12 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 25 Apr 2024 23:52:06 GMT
ENV GRADLE_VERSION=7.6.4
# Thu, 25 Apr 2024 23:52:07 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Thu, 25 Apr 2024 23:52:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Thu, 25 Apr 2024 23:52:16 GMT
USER gradle
# Thu, 25 Apr 2024 23:52:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Thu, 25 Apr 2024 23:52:19 GMT
USER root
```

-	Layers:
	-	`sha256:a9466735f8829921e05503ca4d4d92bb6f06facd77aa4b2feb86645d7c27b1ba`  
		Last Modified: Thu, 25 Apr 2024 20:35:05 GMT  
		Size: 35.6 MB (35588305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0de467fd0448940d36a45afa474251ce2e8bd6e8f60ef7eb65adb86c07161a`  
		Last Modified: Thu, 25 Apr 2024 20:52:58 GMT  
		Size: 13.8 MB (13767010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2be579025da222547dab87cc571b5b1d60ba6bf3e918459fc23d5877ba59a81`  
		Last Modified: Thu, 25 Apr 2024 20:54:21 GMT  
		Size: 132.7 MB (132720920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048d728296142184b318b85601a9fc1fdfd62c19fa204ed14048012540f453f6`  
		Last Modified: Thu, 25 Apr 2024 20:54:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7cf1930c9a33e537c2223fed1b0eee07923379d6830ed3f8855d2acee243c6`  
		Last Modified: Thu, 25 Apr 2024 20:54:08 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4742eb45056441f54e1d4ee75d1c0baeebcf7e85b84df1fdef6fa31d203dff30`  
		Last Modified: Thu, 25 Apr 2024 23:57:23 GMT  
		Size: 4.4 KB (4362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a830a185019383710df946788fa4e32fa6aefe677131b715284cf7ac2ed2df6f`  
		Last Modified: Thu, 25 Apr 2024 23:57:33 GMT  
		Size: 55.7 MB (55674588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98c16b602c3a651d9ba2fa3fe9dc0c7077328ef7ab11333dcc0c562ea89b3eb`  
		Last Modified: Fri, 26 Apr 2024 00:00:47 GMT  
		Size: 122.7 MB (122730261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a68937b54f5403f6320f788223dee50778595b3152bd500d96b3f59663fd8d3`  
		Last Modified: Fri, 26 Apr 2024 00:00:41 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk11-jammy` - linux; s390x

```console
$ docker pull gradle@sha256:464297c934c01a3b12aee849a065c470316731aec4b53ed7fffcb7dfadbe9df6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341138998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10e8eabd3cb9b91f565c6d8fef77fb1f74040b69dba27434a50e4029f4d822f7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Apr 2024 13:52:56 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:52:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:52:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:52:56 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:52:58 GMT
ADD file:7d693ab3b1f45d4992a119ec94444efc96c176ad954375f3bc1299ab813a46a0 in / 
# Sat, 27 Apr 2024 13:52:58 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Thu, 02 May 2024 03:36:48 GMT
CMD ["gradle"]
# Thu, 02 May 2024 03:36:48 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 02 May 2024 03:36:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Thu, 02 May 2024 03:36:48 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 02 May 2024 03:36:49 GMT
WORKDIR /home/gradle
# Thu, 02 May 2024 03:37:34 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 02 May 2024 03:41:17 GMT
ENV GRADLE_VERSION=7.6.4
# Thu, 02 May 2024 03:41:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Thu, 02 May 2024 03:41:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Thu, 02 May 2024 03:41:25 GMT
USER gradle
# Thu, 02 May 2024 03:41:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Thu, 02 May 2024 03:41:26 GMT
USER root
```

-	Layers:
	-	`sha256:ffda8878ec88daab976ebae63a8dc770c7ff669cb06828bf12b1a5acca67f1f8`  
		Last Modified: Thu, 02 May 2024 01:13:50 GMT  
		Size: 28.6 MB (28637522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fff9a54cf15de3ca0cf1b06659af1fb616f065d79a2849a7d499f81c55128f6`  
		Last Modified: Thu, 02 May 2024 01:44:56 GMT  
		Size: 13.0 MB (12986878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830996f7cbb397be8b6a9e8087afa64739e4abf5d63e915042b07c1436a742a9`  
		Last Modified: Thu, 02 May 2024 01:45:04 GMT  
		Size: 125.5 MB (125500644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f1e9ea80faa17c6774ff1bc4ddf5d1f96e4a6b62a7d1a1e48f29d0d0d76027`  
		Last Modified: Thu, 02 May 2024 01:44:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc98a216e5ca26b61fa5967a499f09b5aa42c12100915195e827d75c2640331`  
		Last Modified: Thu, 02 May 2024 01:44:53 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49683ac8d52b2cb64018e7a2f152acf880a5ae2d9b36ddeb80e98dc4ebecd3e`  
		Last Modified: Thu, 02 May 2024 03:45:46 GMT  
		Size: 4.4 KB (4367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752b7a0b0c25000688114d506b7b733e9aa5d18e448c654bae65f49e50536ee4`  
		Last Modified: Thu, 02 May 2024 03:45:55 GMT  
		Size: 51.3 MB (51278302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95cbf5b0a571c8c0e7a290e6e6b6d743521d29456c5c755352f01e912c78eb75`  
		Last Modified: Thu, 02 May 2024 03:47:40 GMT  
		Size: 122.7 MB (122730209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3af920f0719c95cfff4e846d251942a5f780792f767c3f1eef7c602882fbde3`  
		Last Modified: Thu, 02 May 2024 03:47:35 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
