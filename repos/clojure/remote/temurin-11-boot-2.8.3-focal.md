## `clojure:temurin-11-boot-2.8.3-focal`

```console
$ docker pull clojure@sha256:56f231abd56325a11666fa1dfb39366be3bcb426f4d10203769416775788b71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-focal` - linux; amd64

```console
$ docker pull clojure@sha256:d3f34af8b8e6fdf1cf95ce36fd185e7808581c9b263454e1afc021de492a46c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (249953251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c4cbdadf51a8ce0a7d5c2f3d02c3ea409569f455d964397e62f501aeb8967a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["boot","repl"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
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
ENV JAVA_VERSION=jdk-11.0.22+7
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ca1dc604352e9b3906b8955a700745a0a650ed59947f7f354af597871876a716';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='25cf602cac350ef36067560a4e8042919f3be973d419eac4d839e2e0000b2cc8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='7d0e71d8aea6bba27dfbb9ad7434066896c3085327e58776ca89d5e262040bc5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='95a1c215e434c302e43c8039f322b954ee539ca22412cd09b4dd77523aaa861a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='137becfcfa6d288ba8c07ba23bf966c87bedfe7ee5cb3342da833407e13e3cfa';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 11:07:04 GMT
CMD ["jshell"]
# Thu, 28 Mar 2024 03:00:17 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 03:00:17 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 03:00:17 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:00:26 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 03:00:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 03:00:26 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 03:00:45 GMT
RUN boot
# Thu, 28 Mar 2024 03:00:45 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4482b1922021fb7a7193283132c9143a46f8c6e3f22582ccaaeb3023ef8f0ae3`  
		Last Modified: Thu, 28 Mar 2024 02:03:10 GMT  
		Size: 16.9 MB (16920563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915198a92f5f4d648ccef2889a453c97f173595c052c09f18a8d3e318b25ae9b`  
		Last Modified: Thu, 28 Mar 2024 02:05:58 GMT  
		Size: 145.3 MB (145288200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19819bd56470aad65cff77e72b0e6b8255bb6d956e40c2aac291fdd411ce1e5`  
		Last Modified: Thu, 28 Mar 2024 02:05:47 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a448d8c5209aec49f800c91e2722cfe4f1dacba2df59548d4fc9be1c06ea12`  
		Last Modified: Thu, 28 Mar 2024 02:05:47 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48040e39d6cb4cfea6b27eb3242ef686e62a1d6522bed0a63aa3b518ecd55e9`  
		Last Modified: Thu, 28 Mar 2024 03:20:22 GMT  
		Size: 338.9 KB (338939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096c5c69bea17621aa8f5f317c913d509f190739b54e143557a7fed073a2935e`  
		Last Modified: Thu, 28 Mar 2024 03:20:25 GMT  
		Size: 58.8 MB (58820325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-focal` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:62af346aa9694a8bce5b05d6eb44077894392cddb282f5c8699f28e460efa64a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 MB (245158598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5833da6acf078d2667d00c6ad502280445bb909db1b138c10bb86aef1f357c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 19:07:29 GMT
ARG RELEASE
# Wed, 10 Apr 2024 19:07:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 19:07:30 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 19:07:39 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Wed, 10 Apr 2024 19:07:40 GMT
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
ENV JAVA_VERSION=jdk-11.0.22+7
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ca1dc604352e9b3906b8955a700745a0a650ed59947f7f354af597871876a716';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='25cf602cac350ef36067560a4e8042919f3be973d419eac4d839e2e0000b2cc8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='7d0e71d8aea6bba27dfbb9ad7434066896c3085327e58776ca89d5e262040bc5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='95a1c215e434c302e43c8039f322b954ee539ca22412cd09b4dd77523aaa861a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='137becfcfa6d288ba8c07ba23bf966c87bedfe7ee5cb3342da833407e13e3cfa';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jan 2024 11:07:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 11:07:04 GMT
CMD ["jshell"]
# Tue, 16 Apr 2024 06:34:52 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 16 Apr 2024 06:34:52 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 16 Apr 2024 06:34:52 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:34:55 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 16 Apr 2024 06:34:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Apr 2024 06:34:55 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 16 Apr 2024 06:35:14 GMT
RUN boot
# Tue, 16 Apr 2024 06:35:14 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:7688b82426696e44f961201d38c484dd5279eb88689c7eadb2100dd075e697f8`  
		Last Modified: Fri, 12 Apr 2024 07:29:54 GMT  
		Size: 27.2 MB (27204984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2f0d048c4dc921b108e92215dcba18b91b316fdaad6521463665d94fdab64c`  
		Last Modified: Tue, 16 Apr 2024 02:55:17 GMT  
		Size: 16.8 MB (16777181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de49f131a4c840907a9473cb7aca6a6bc080185a5fb30fc7f60ce72e9c1635ba`  
		Last Modified: Tue, 16 Apr 2024 02:56:25 GMT  
		Size: 142.0 MB (142015833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc1acc04f8bd12be5556a8bb55e7f180762d6324c4ba743590db29dd433650c`  
		Last Modified: Tue, 16 Apr 2024 02:56:15 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2064278750ddac376cecac409fd1b9579364878f3facb858e5e3e6655de399d`  
		Last Modified: Tue, 16 Apr 2024 02:56:15 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b968561b100e19aea7732b80e15db90272ed3244de95a9c2c773853116e70e`  
		Last Modified: Tue, 16 Apr 2024 06:53:14 GMT  
		Size: 339.3 KB (339303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f41f575284d0ad4a8dfc5ef7ef099b7d71b36780152fe91fcd5b4418021ee13`  
		Last Modified: Tue, 16 Apr 2024 06:53:16 GMT  
		Size: 58.8 MB (58820389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
