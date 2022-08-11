## `clojure:temurin-17-boot-2.8.3-jammy`

```console
$ docker pull clojure@sha256:1c9c7101e4cb1187bc35928d3eedc922486677e3666afe91e21ad22656911eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:049e1c9d2d9754c2bfd21146324bd2b0a8b1b4fb17394ed6319ebd38f2419532
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297611349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2d6f4a2a9620b37e4239e7f2c5f9a391858dc86b97698d3bfaa47e9fef8c39`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:55 GMT
ADD file:396eeb65c8d737180cc1219713cf59efb214027b79d8ea0b7e58a08e7c8d7a21 in / 
# Tue, 02 Aug 2022 01:30:56 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 19:20:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 19:20:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 19:20:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Aug 2022 19:25:04 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Aug 2022 19:25:04 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 11 Aug 2022 19:25:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c23b0b9c65cfe223a07edb8752026afd1e8ec1682630c2d92db4dd5aa039204';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='f499656e581517e62aa954965a7a19bbb0ea8c2e6bd84050527b88efbaa1d96d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e80a0f6626bd28ea20c43524b3ab10af48b3789317aea5b7019c146fe6268d94';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='40b09e8fa473f194030a85c059ba768abf5635a9a6d4dbeb79a87113ee8f4ece';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c0851d610b03cb51e9b360fef3e9ec2026c62837a143e7786649ba94f38cc0d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 11 Aug 2022 19:25:16 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 11 Aug 2022 19:25:16 GMT
CMD ["jshell"]
# Thu, 11 Aug 2022 20:00:05 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Aug 2022 20:00:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Aug 2022 20:00:05 GMT
WORKDIR /tmp
# Thu, 11 Aug 2022 20:00:09 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Aug 2022 20:00:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Aug 2022 20:00:09 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Aug 2022 20:00:41 GMT
RUN boot
# Thu, 11 Aug 2022 20:10:08 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 11 Aug 2022 20:10:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Aug 2022 20:10:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d19f32bd9e4106d487f1a703fc2f09c8edadd92db4405d477978e8e466ab290d`  
		Last Modified: Tue, 02 Aug 2022 01:32:15 GMT  
		Size: 30.4 MB (30426136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b6eaba4d2174e3bed591e0faa47bb5cce268d4172344b196f3fe9feb0bf05e`  
		Last Modified: Thu, 11 Aug 2022 19:36:05 GMT  
		Size: 15.9 MB (15884335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049d7a1f39770acce299de581cdf6214a50dbad4dc3429ba60bebc983d5ac75c`  
		Last Modified: Thu, 11 Aug 2022 19:36:17 GMT  
		Size: 192.1 MB (192143079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0e77f32143041dc7f975af110c42dd4d248cf2c41ab1deebfd4be962f067ca`  
		Last Modified: Thu, 11 Aug 2022 19:36:02 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08eafd434c28a9f659069283a36a246662b0c32aa47b219e500e8c435f30ff0c`  
		Last Modified: Thu, 11 Aug 2022 20:21:24 GMT  
		Size: 336.6 KB (336572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a65879461177a4ba40300196e11708cd1623eaaa3fa9679436339f173e46db`  
		Last Modified: Thu, 11 Aug 2022 20:21:27 GMT  
		Size: 58.8 MB (58820653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49fdd5b811d4104fe11028dafbec11629a5f9f5497dfeb7edfba3f5a645d371`  
		Last Modified: Thu, 11 Aug 2022 20:21:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2cdac1f7006f34c48f60d90f1922f3a37d8e84d0ef26ca51670f1d223bea3e6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295530826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9c8c6feb44bd0e47c86bb63d07f0395f554e705511ea8edda2f773f0d005b7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Thu, 11 Aug 2022 18:40:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 18:40:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 18:40:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Aug 2022 18:45:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 11 Aug 2022 18:45:38 GMT
ENV JAVA_VERSION=jdk-17.0.4+8
# Thu, 11 Aug 2022 18:45:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8c23b0b9c65cfe223a07edb8752026afd1e8ec1682630c2d92db4dd5aa039204';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.4_8.tar.gz';          ;;        armhf|arm)          ESUM='f499656e581517e62aa954965a7a19bbb0ea8c2e6bd84050527b88efbaa1d96d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_arm_linux_hotspot_17.0.4_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e80a0f6626bd28ea20c43524b3ab10af48b3789317aea5b7019c146fe6268d94';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.4_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='40b09e8fa473f194030a85c059ba768abf5635a9a6d4dbeb79a87113ee8f4ece';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.4_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c0851d610b03cb51e9b360fef3e9ec2026c62837a143e7786649ba94f38cc0d1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.4%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.4_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 11 Aug 2022 18:45:48 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 11 Aug 2022 18:45:49 GMT
CMD ["jshell"]
# Thu, 11 Aug 2022 19:46:09 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Aug 2022 19:46:10 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Aug 2022 19:46:11 GMT
WORKDIR /tmp
# Thu, 11 Aug 2022 19:46:18 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Aug 2022 19:46:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Aug 2022 19:46:20 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Aug 2022 19:46:46 GMT
RUN boot
# Thu, 11 Aug 2022 19:56:38 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 11 Aug 2022 19:56:38 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Aug 2022 19:56:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04632ef1df025fa34842e72b255aed8926a8a48dffec56bfbc4b1ccdf186156e`  
		Last Modified: Thu, 11 Aug 2022 18:57:25 GMT  
		Size: 17.3 MB (17322776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e33020429121cee0f40877a0facad934348f3ed81e3feffd7881149433cd588`  
		Last Modified: Thu, 11 Aug 2022 18:57:40 GMT  
		Size: 190.9 MB (190911181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11dbe788e181d05fe7c7beb44bde93c404a54b3ac47bace36e672454e83a13b0`  
		Last Modified: Thu, 11 Aug 2022 18:57:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbb0074a1e3e434b222d2f10f1c3415568e4c82b95651678813f1f344d26423`  
		Last Modified: Thu, 11 Aug 2022 20:08:44 GMT  
		Size: 98.8 KB (98831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0018611bce778c422f1443ef7fc7b0ff115f16bc0f01753c1afb714396d1f78a`  
		Last Modified: Thu, 11 Aug 2022 20:08:49 GMT  
		Size: 58.8 MB (58816327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a679089ddc22661c9c1bdb4568d5c9f5776f1d1b42a6e5457671825557f858`  
		Last Modified: Thu, 11 Aug 2022 20:08:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
