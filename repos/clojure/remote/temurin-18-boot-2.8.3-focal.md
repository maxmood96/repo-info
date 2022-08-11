## `clojure:temurin-18-boot-2.8.3-focal`

```console
$ docker pull clojure@sha256:e8aadf97826b8cce2ad7e728605d6ad371bfbb52e520d016edb0e74353af1521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-18-boot-2.8.3-focal` - linux; amd64

```console
$ docker pull clojure@sha256:b23ca099a8e4d8f76281c3977da2722151153285a7eefb420e202d536e333e64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297604516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2495b7040d2faf40bd2fc534acc9d2302461df77df105a62086e48c3c468fff6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 19:19:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 19:19:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 19:19:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Aug 2022 19:24:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Aug 2022 19:26:54 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Thu, 11 Aug 2022 19:27:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f4aca720bfcea4df7f02b59de1f68648632070c492f210b9e41e69170ee5e48f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.2_9.tar.gz';          ;;        armhf|arm)          ESUM='52ec0ddee9ff16397de2c9f614ff6b5464220bd5c3d705e8b89d28fd478feb60';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_arm_linux_hotspot_18.0.2_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4262677f8b6054d26f1c0042ac47dfbaab6a18d7dc73fa807b15ee03cdcbdece';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.2_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d916cfa15552ae2ad2f2c96ebc72aaaea4c844af9842f5ca9724fcbbdc08d25c';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.2_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5e5dbf6f1308829528778e00631ec83e252d90fc444503091e71a66465e88941';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_linux_hotspot_18.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 11 Aug 2022 19:27:12 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 11 Aug 2022 19:27:12 GMT
CMD ["jshell"]
# Thu, 11 Aug 2022 20:12:55 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Aug 2022 20:12:55 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Aug 2022 20:12:55 GMT
WORKDIR /tmp
# Thu, 11 Aug 2022 20:13:00 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Aug 2022 20:13:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Aug 2022 20:13:00 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Aug 2022 20:13:18 GMT
RUN boot
# Thu, 11 Aug 2022 20:13:19 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 11 Aug 2022 20:13:19 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Aug 2022 20:13:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dd6b41e17bd3ada96d1c3dafaeca8e6ef810daf9822be394cbebf694c15561`  
		Last Modified: Thu, 11 Aug 2022 19:35:38 GMT  
		Size: 16.3 MB (16299780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1392d2793c8c587e314bc1e4cbecee611fbc3fa66154814efdaed3d86d80e94`  
		Last Modified: Thu, 11 Aug 2022 19:38:45 GMT  
		Size: 193.6 MB (193578827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece9e452506d41e98d84ea560c71f2ab6027362b327878ad56977c943dab1d78`  
		Last Modified: Thu, 11 Aug 2022 19:38:30 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84da84e7a1fa3f50bba83131bbdcc21b31a0ae2536cd994eadd968bb1b3df3dd`  
		Last Modified: Thu, 11 Aug 2022 20:23:16 GMT  
		Size: 332.2 KB (332222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f053c83889c7d0ccbf7487b8b4a8b9a95310be7a92bb0761b6a4fe662ed517`  
		Last Modified: Thu, 11 Aug 2022 20:23:20 GMT  
		Size: 58.8 MB (58820518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126397fbbed984bf368a1b0bd81c6199541cffee419dd4cec300d91eb1ff1da4`  
		Last Modified: Thu, 11 Aug 2022 20:23:16 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-18-boot-2.8.3-focal` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fc9cdb401e7deb914ba7ba8859e01ebf91b9f960e8aee8b9d1e4d89fd4ea7f20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295541511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e0b1ca6e19a743fd3ce7e22970586524d9ac5b2e71cda674f3edff303dd6f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:39:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:39:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:39:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Aug 2022 18:44:54 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Aug 2022 18:47:12 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Thu, 11 Aug 2022 18:47:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f4aca720bfcea4df7f02b59de1f68648632070c492f210b9e41e69170ee5e48f';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_aarch64_linux_hotspot_18.0.2_9.tar.gz';          ;;        armhf|arm)          ESUM='52ec0ddee9ff16397de2c9f614ff6b5464220bd5c3d705e8b89d28fd478feb60';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_arm_linux_hotspot_18.0.2_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4262677f8b6054d26f1c0042ac47dfbaab6a18d7dc73fa807b15ee03cdcbdece';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_ppc64le_linux_hotspot_18.0.2_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='d916cfa15552ae2ad2f2c96ebc72aaaea4c844af9842f5ca9724fcbbdc08d25c';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_s390x_linux_hotspot_18.0.2_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='5e5dbf6f1308829528778e00631ec83e252d90fc444503091e71a66465e88941';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_linux_hotspot_18.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 11 Aug 2022 18:47:28 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 11 Aug 2022 18:47:29 GMT
CMD ["jshell"]
# Thu, 11 Aug 2022 19:59:50 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Aug 2022 19:59:51 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Aug 2022 19:59:52 GMT
WORKDIR /tmp
# Thu, 11 Aug 2022 19:59:59 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Aug 2022 19:59:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Aug 2022 20:00:00 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Aug 2022 20:00:15 GMT
RUN boot
# Thu, 11 Aug 2022 20:00:16 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 11 Aug 2022 20:00:16 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Aug 2022 20:00:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb7631a1ffbba0a5b60549c314d974241510989eeceaa9db55cdc489b0e2ae0`  
		Last Modified: Thu, 11 Aug 2022 18:56:54 GMT  
		Size: 17.0 MB (17006184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93463167319e95aad850cde591cc61d4a2407e07b63887eb338372072115d10`  
		Last Modified: Thu, 11 Aug 2022 18:59:45 GMT  
		Size: 192.4 MB (192431721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a63be3658a2d858a10b5e46bb0dc9a623da2f592994ecde47c0f0f1e369b1af`  
		Last Modified: Thu, 11 Aug 2022 18:59:24 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041b5bc03f18b5c8df476525d2147216f1f7100ee5b2b84f7d4f56057b69fcd8`  
		Last Modified: Thu, 11 Aug 2022 20:09:58 GMT  
		Size: 95.7 KB (95650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339378613a348305d514fa8d9ee2fdfbaad2de416e8bba702ddee1299d424bd`  
		Last Modified: Thu, 11 Aug 2022 20:10:03 GMT  
		Size: 58.8 MB (58815592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956b2d5d2856f630b9a30d97f7ccf47173e28673f74ea8cfb299c1a3c8373a8e`  
		Last Modified: Thu, 11 Aug 2022 20:09:58 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
