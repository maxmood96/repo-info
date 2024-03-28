## `clojure:temurin-11-boot`

```console
$ docker pull clojure@sha256:79f260b9210ed3ba9dde0fa3a55d5928c4b239135e3d0dc87f9d5eea4b31a755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot` - linux; amd64

```console
$ docker pull clojure@sha256:cf68cd286e4909179a55064863c7aeb8adedc0504dc79f9706ba2be266a0b1d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247804620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c3c92bc7359a4bb7facae4cd17f72444c92050523446b3380303928d9a0e64`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["boot","repl"]`

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
# Wed, 06 Mar 2024 06:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 06:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 06:02:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 06:02:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 06:03:26 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 06 Mar 2024 06:03:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ca1dc604352e9b3906b8955a700745a0a650ed59947f7f354af597871876a716';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.22_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='25cf602cac350ef36067560a4e8042919f3be973d419eac4d839e2e0000b2cc8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.22_7.tar.gz';          ;;        armhf|arm)          ESUM='7d0e71d8aea6bba27dfbb9ad7434066896c3085327e58776ca89d5e262040bc5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_arm_linux_hotspot_11.0.22_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='95a1c215e434c302e43c8039f322b954ee539ca22412cd09b4dd77523aaa861a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.22_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='137becfcfa6d288ba8c07ba23bf966c87bedfe7ee5cb3342da833407e13e3cfa';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.22_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 06:03:36 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 06:03:36 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 06:03:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 06:03:36 GMT
CMD ["jshell"]
# Wed, 06 Mar 2024 14:04:22 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 14:04:22 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 14:04:22 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 14:04:28 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 14:04:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 14:04:28 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 14:04:48 GMT
RUN boot
# Wed, 06 Mar 2024 14:04:48 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8069355d5739c7da6dbe5ac9692d576813db815ada8e298f80c69c9624b46e9b`  
		Last Modified: Wed, 06 Mar 2024 06:07:30 GMT  
		Size: 12.9 MB (12904599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f7a72ac2f841ebf3f4f9be405c1cce2173ce0ca79c0e0176d93b4a66d33b0e`  
		Last Modified: Wed, 06 Mar 2024 06:08:50 GMT  
		Size: 145.3 MB (145288641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5824857684b596ada67060f30f1f216dffbe7639156df1d163f2cc54e06754`  
		Last Modified: Wed, 06 Mar 2024 06:08:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc26d2df5bff2703f0e2f5f9f6458bd9a9e97b8e380aa55ff957ccae9762a9b`  
		Last Modified: Wed, 06 Mar 2024 06:08:39 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4b560d4e569941b83d605c429da5e5661f1918766fd3187832c25690dcb65d`  
		Last Modified: Wed, 06 Mar 2024 14:24:19 GMT  
		Size: 338.6 KB (338559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa101540a8a14ba4605779aec54408f18219521d28f4f29b28861a2aefe5d05`  
		Last Modified: Wed, 06 Mar 2024 14:24:22 GMT  
		Size: 58.8 MB (58820611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:41dfbeddd04b8c58016e549f6730132ca430b4c18ace9a2124bf93d96d7dabc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242421746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1318f2c8c09ca59db05443dd5bd3246796779ee8ca53a323c1f8d040dff0e457`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
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
# Thu, 28 Mar 2024 02:34:43 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 02:34:43 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:34:43 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:34:47 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 02:34:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:34:47 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 02:35:04 GMT
RUN boot
# Thu, 28 Mar 2024 02:35:04 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2168560270786452bc1288278f5b8a7831c90a490efa55dc798deec8e871311a`  
		Last Modified: Thu, 28 Mar 2024 00:48:42 GMT  
		Size: 12.8 MB (12846303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd5f2dc7848119160dd1d53b9506acf5959ee9bbb1237b18a5e135cc705f76e`  
		Last Modified: Thu, 28 Mar 2024 00:50:43 GMT  
		Size: 142.0 MB (142014623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63447d12fb938c3a501e889e70575adf85575a0d36e8b6ba8828f62f7d1262b`  
		Last Modified: Thu, 28 Mar 2024 00:50:33 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d1416e6f1eec4000cbfd3a08d7d33e8200760d235abd6c6581fb30a0e569a6`  
		Last Modified: Thu, 28 Mar 2024 00:50:34 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd8bc2201134d96e83eb5448a54440afc937b99625d2d4f49608c54ac4baeae`  
		Last Modified: Thu, 28 Mar 2024 02:50:40 GMT  
		Size: 338.8 KB (338840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219e437170840f4aeefc0a093e7bd9b597fac2c24d5b21802aeffbd6d913bf88`  
		Last Modified: Thu, 28 Mar 2024 02:50:42 GMT  
		Size: 58.8 MB (58820434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
