## `tomcat:9-jre11-temurin`

```console
$ docker pull tomcat@sha256:14d147d4053a799b8b812e4a4d323ceb09591c628fcff21011bfa2410ea4de3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:9-jre11-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:f0518ebc1cc3167ca1c34c15325a048a92a069cb6689b1ae40f85e6e14dd98dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103425559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e34b7d302d232e279cd5bd8f3b059e12dd390eb21b728970bcab00db732da5`
-	Default Command: `["catalina.sh","run"]`

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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7290ace47a030d89ea023c28e7aa555c9da72b4194f73b39ec9d058011bf06dd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='786a72296189ba8e43999532aa73730d87ec1fce558eb3c4e98b611b423375e3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='025f994549708f7291ce3b0fa7c41f7e78ec3af3eae3f85fffe9c5fa4a54889f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b3fbd324620fd914bd8462e292124493fcf846fd69195c4b9a231131dc68d5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='25abb7f74f55847b0d509402111084bd7a244d904744f3bfffa89528bc3b8a69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 May 2024 06:56:08 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 02 May 2024 06:56:08 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 06:56:09 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 02 May 2024 06:56:09 GMT
WORKDIR /usr/local/tomcat
# Thu, 02 May 2024 06:56:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 06:56:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 06:59:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 02 May 2024 06:59:42 GMT
ENV TOMCAT_MAJOR=9
# Tue, 07 May 2024 21:42:18 GMT
ENV TOMCAT_VERSION=9.0.89
# Tue, 07 May 2024 21:42:18 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Tue, 07 May 2024 21:42:18 GMT
COPY dir:03582b173557204a95fff712863e0cee570a66428ce082b553e7d1e2f60d1263 in /usr/local/tomcat 
# Tue, 07 May 2024 21:42:23 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 21:42:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 07 May 2024 21:42:25 GMT
EXPOSE 8080
# Tue, 07 May 2024 21:42:25 GMT
ENTRYPOINT []
# Tue, 07 May 2024 21:42:25 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:86a4fe39e025c0d70e3c2c3a1510492b0a70e33a0159d57fc035797a31b71963`  
		Last Modified: Thu, 02 May 2024 01:17:33 GMT  
		Size: 47.2 MB (47186118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cead845a4dcc6ed61dc10dc98ab58222d356380c07ab6e2c17d1d4739030d9e`  
		Last Modified: Thu, 02 May 2024 01:17:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06de8810f58de3dcb64fa6fb3dec94ef3834943dacd5331567d11be89704500e`  
		Last Modified: Thu, 02 May 2024 01:17:26 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55614dadd1ab5a5496f658762e14010c4ca88c3d0718ece860633735d79e3966`  
		Last Modified: Thu, 02 May 2024 07:07:40 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772ea1d8e83d363b4ceb3ad3698d5eeecbea33b6dfe6b9bb7ef93c1ede7f4e08`  
		Last Modified: Tue, 07 May 2024 21:51:52 GMT  
		Size: 12.4 MB (12436680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea04b58b5b787a21dcaeba5b67a14f90e4b21878c17c7d99aec2b9430b800054`  
		Last Modified: Tue, 07 May 2024 21:51:51 GMT  
		Size: 456.3 KB (456309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009728510406e63c0d8b5b5542c73b6f31b6773a241151c542e7c0873715dbb0`  
		Last Modified: Tue, 07 May 2024 21:51:51 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:c6e98b699f5623e62981c00026d79590272adf1ae9177a321b59a724d5861781
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98116644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1804bb7fe547998c3f3e71027d0bca5065886ea2b77bef1d0f610bd473086f3`
-	Default Command: `["catalina.sh","run"]`

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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7290ace47a030d89ea023c28e7aa555c9da72b4194f73b39ec9d058011bf06dd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='786a72296189ba8e43999532aa73730d87ec1fce558eb3c4e98b611b423375e3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='025f994549708f7291ce3b0fa7c41f7e78ec3af3eae3f85fffe9c5fa4a54889f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b3fbd324620fd914bd8462e292124493fcf846fd69195c4b9a231131dc68d5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='25abb7f74f55847b0d509402111084bd7a244d904744f3bfffa89528bc3b8a69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 May 2024 02:16:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 02 May 2024 02:16:31 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 02:16:32 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 02 May 2024 02:16:32 GMT
WORKDIR /usr/local/tomcat
# Thu, 02 May 2024 02:16:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 02:16:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 02:18:50 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 02 May 2024 02:18:50 GMT
ENV TOMCAT_MAJOR=9
# Thu, 02 May 2024 02:18:50 GMT
ENV TOMCAT_VERSION=9.0.88
# Thu, 02 May 2024 02:18:50 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Thu, 02 May 2024 02:18:51 GMT
COPY dir:52f0561705644ce94bf9e7a0127a46d3d3f66dc07fae2257447287c763649047 in /usr/local/tomcat 
# Thu, 02 May 2024 02:18:55 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:18:56 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 02 May 2024 02:18:56 GMT
EXPOSE 8080
# Thu, 02 May 2024 02:18:57 GMT
ENTRYPOINT []
# Thu, 02 May 2024 02:18:57 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:7c7efc9401e560f8b38136b91365ad34a8bee881b12dd3903332db10a0f4328c`  
		Last Modified: Thu, 02 May 2024 01:29:53 GMT  
		Size: 45.3 MB (45296189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e1523954567389cd04cb8d71f44733479f87634405d158e42b0e1b882bb3aa`  
		Last Modified: Thu, 02 May 2024 01:29:46 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2db7ba0d673339794602c5308437cec154295c04dd5e288d3e2ed8e6210b406`  
		Last Modified: Thu, 02 May 2024 01:29:46 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f4ea92c3c6d8c7bf5bee99301ec6f49fd970ce6ee856697f000d6fdf270d00`  
		Last Modified: Thu, 02 May 2024 02:23:41 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8401e6702b002512d3951fb8ec454c13041f47c2ce04250e08219d8b349c2d`  
		Last Modified: Thu, 02 May 2024 02:25:49 GMT  
		Size: 12.4 MB (12358111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d902f74cf0cce6a00e7ddd1c62592948905d261e822845aa41f22bcc93f20df`  
		Last Modified: Thu, 02 May 2024 02:25:48 GMT  
		Size: 430.7 KB (430657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c42e647901ac39b21a17d1c16e9ce8f8264cd55393f76e43a1c4bea5ed5f8f`  
		Last Modified: Thu, 02 May 2024 02:25:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:7ba9a393f4efbf41eacae865861c662eb85a5c57eef4afc43f445e11e71c35da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99692429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10978900d0ad13913571973576da97a353ae6d26430417adb5d66ee9e89ff93`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7290ace47a030d89ea023c28e7aa555c9da72b4194f73b39ec9d058011bf06dd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='786a72296189ba8e43999532aa73730d87ec1fce558eb3c4e98b611b423375e3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='025f994549708f7291ce3b0fa7c41f7e78ec3af3eae3f85fffe9c5fa4a54889f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b3fbd324620fd914bd8462e292124493fcf846fd69195c4b9a231131dc68d5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='25abb7f74f55847b0d509402111084bd7a244d904744f3bfffa89528bc3b8a69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 May 2024 07:36:09 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 02 May 2024 07:36:09 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 07:36:09 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 02 May 2024 07:36:09 GMT
WORKDIR /usr/local/tomcat
# Thu, 02 May 2024 07:36:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 07:36:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 07:38:59 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 02 May 2024 07:38:59 GMT
ENV TOMCAT_MAJOR=9
# Thu, 02 May 2024 07:38:59 GMT
ENV TOMCAT_VERSION=9.0.88
# Thu, 02 May 2024 07:38:59 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Thu, 02 May 2024 07:38:59 GMT
COPY dir:a7244f13ab8401e57c132eab9688793d5f02b85b4b0bc9dedcb053a1bbd03c7f in /usr/local/tomcat 
# Thu, 02 May 2024 07:39:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 07:39:04 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 02 May 2024 07:39:04 GMT
EXPOSE 8080
# Thu, 02 May 2024 07:39:04 GMT
ENTRYPOINT []
# Thu, 02 May 2024 07:39:04 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2472ac6840da0115175cae8b0be8d1b8c2b6b74acb5fc6bf185b0c9333b8a3`  
		Last Modified: Thu, 02 May 2024 04:17:28 GMT  
		Size: 12.8 MB (12847034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7d04c7a1163e887fde96d5de8c35431947e2714d44c2d767038c7371c5f04b`  
		Last Modified: Thu, 02 May 2024 04:19:13 GMT  
		Size: 45.6 MB (45556488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5621c450b08f8951efbc916ac9e002c6721dcea044b8348ca5409db1748edb`  
		Last Modified: Thu, 02 May 2024 04:19:07 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf99ddb38b812212a8029a07871cbe9294d1d3137b659cb54aa3f2fbebb5a3dc`  
		Last Modified: Thu, 02 May 2024 04:19:07 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd2d4dbeb2ac44961cefa09509d30755d51ea0577319da31c9732f42f1007c1`  
		Last Modified: Thu, 02 May 2024 07:46:01 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80630dd7e9bbc254f01ec614a3c0f104b631423d3d4a2320effef6e0533f231f`  
		Last Modified: Thu, 02 May 2024 07:48:58 GMT  
		Size: 12.4 MB (12430972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3302252bf0ab6e23820e88205edbf07aaaf16a860ba612535328f36ec81cca`  
		Last Modified: Thu, 02 May 2024 07:48:57 GMT  
		Size: 455.6 KB (455559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d7fae99f5ab08f51e6cca1ed9534f5c276613ba5bd50bdbc0b5146a5a342e0`  
		Last Modified: Thu, 02 May 2024 07:48:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:3a56552fe08b235d1f3770502260210105802618ad26c5418c629c871914ad1c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104935210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a0654b84f126d98e063c5323ec33366d0dc44a31fd9e8ea55a6f83b9a018c7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7290ace47a030d89ea023c28e7aa555c9da72b4194f73b39ec9d058011bf06dd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='786a72296189ba8e43999532aa73730d87ec1fce558eb3c4e98b611b423375e3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='025f994549708f7291ce3b0fa7c41f7e78ec3af3eae3f85fffe9c5fa4a54889f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b3fbd324620fd914bd8462e292124493fcf846fd69195c4b9a231131dc68d5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='25abb7f74f55847b0d509402111084bd7a244d904744f3bfffa89528bc3b8a69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 May 2024 04:50:27 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 02 May 2024 04:50:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 04:50:31 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 02 May 2024 04:50:32 GMT
WORKDIR /usr/local/tomcat
# Thu, 02 May 2024 04:50:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 04:50:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 04:58:56 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 02 May 2024 04:58:56 GMT
ENV TOMCAT_MAJOR=9
# Thu, 02 May 2024 04:58:57 GMT
ENV TOMCAT_VERSION=9.0.88
# Thu, 02 May 2024 04:58:57 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Thu, 02 May 2024 04:58:58 GMT
COPY dir:f262ea60e5e9bc82d72cb863c23f615d97e3d8d95c4cb3bd5a5d1fe6de681dd1 in /usr/local/tomcat 
# Thu, 02 May 2024 04:59:05 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 04:59:08 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 02 May 2024 04:59:09 GMT
EXPOSE 8080
# Thu, 02 May 2024 04:59:09 GMT
ENTRYPOINT []
# Thu, 02 May 2024 04:59:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:ef1313ed517c6def5644ab70e25cc66f1c4cd52b1e81c07fb33bfb8850b39c25`  
		Last Modified: Thu, 02 May 2024 01:40:15 GMT  
		Size: 35.6 MB (35588524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615a40d637191fd38e803d020c6fd9ef07a75d9c895faae5c0a3a02afa988fbc`  
		Last Modified: Thu, 02 May 2024 01:51:41 GMT  
		Size: 13.8 MB (13767451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa16f06513d4ca807d0c9ce8b6e713d40df4a17768d0de842e8ff554c294a83`  
		Last Modified: Thu, 02 May 2024 01:53:40 GMT  
		Size: 42.6 MB (42639864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ca7bc920bc45e1807481eebb57129486a0cda09e98becbaea5756aef9a6ca5`  
		Last Modified: Thu, 02 May 2024 01:53:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc9b8b8cfe6961f44e88bfeed59c05b0cb4b6b884bc684b6daed9ebc3965667`  
		Last Modified: Thu, 02 May 2024 01:53:33 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a290bbd076555a5e58ff317262c3bcd075756122f65b8b7ac920c02e2b68b4`  
		Last Modified: Thu, 02 May 2024 05:10:41 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a0729679d1fcc5f7acedd7d714a66bd56bb48c3c6abe0487bf875c50f0dd54`  
		Last Modified: Thu, 02 May 2024 05:14:01 GMT  
		Size: 12.5 MB (12450588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312672c759d3013011289a3b9de90374e3d1f7281594b752593b05277fae64c3`  
		Last Modified: Thu, 02 May 2024 05:14:00 GMT  
		Size: 487.6 KB (487592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081b6629f78560d1ad35778635647774af8f0788f0e69cd1b5e5360cf9a4f81a`  
		Last Modified: Thu, 02 May 2024 05:13:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre11-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:b87c53eb2bba59e0264c4ead26220b91575213361b7403be78cf5c828c5b528e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95303255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346769e1790433fb87ebfd003a8244ac82eecdc7848417e92c8aa60b0f69fd59`
-	Default Command: `["catalina.sh","run"]`

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
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7290ace47a030d89ea023c28e7aa555c9da72b4194f73b39ec9d058011bf06dd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='786a72296189ba8e43999532aa73730d87ec1fce558eb3c4e98b611b423375e3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='025f994549708f7291ce3b0fa7c41f7e78ec3af3eae3f85fffe9c5fa4a54889f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='3b3fbd324620fd914bd8462e292124493fcf846fd69195c4b9a231131dc68d5f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='25abb7f74f55847b0d509402111084bd7a244d904744f3bfffa89528bc3b8a69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 May 2024 03:20:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 02 May 2024 03:20:08 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 03:20:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 02 May 2024 03:20:09 GMT
WORKDIR /usr/local/tomcat
# Thu, 02 May 2024 03:20:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 03:20:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 03:24:31 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 02 May 2024 03:24:31 GMT
ENV TOMCAT_MAJOR=9
# Thu, 02 May 2024 03:24:32 GMT
ENV TOMCAT_VERSION=9.0.88
# Thu, 02 May 2024 03:24:32 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Thu, 02 May 2024 03:24:33 GMT
COPY dir:000d87c40e1383f8e84a3e84c8f0b372e949f58b393af9050b0f0efdbc406632 in /usr/local/tomcat 
# Thu, 02 May 2024 03:24:37 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 03:24:38 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 02 May 2024 03:24:38 GMT
EXPOSE 8080
# Thu, 02 May 2024 03:24:39 GMT
ENTRYPOINT []
# Thu, 02 May 2024 03:24:39 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:a87d72ea3ad5a1c65ebc51da64f2792990ad0a6ccf88986140df26141f03de0f`  
		Last Modified: Thu, 02 May 2024 01:45:32 GMT  
		Size: 40.8 MB (40799639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb122ea51a33483f6033413c51eb6bfe63220c2c3e6ac41d65c0dc2d4638439`  
		Last Modified: Thu, 02 May 2024 01:45:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd66f2d7f07c5e7bc4037ae1642e4dd4e18df5c03bfe010abcea899ee93b3516`  
		Last Modified: Thu, 02 May 2024 01:45:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002d62854c60c0f55c77f3a22389a82b88395f89fb76252d412ec8624010b669`  
		Last Modified: Thu, 02 May 2024 03:30:14 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9063cf1bb06f0481a59b2038d1bad232c3b3441bfe948ca45a07626f179442e1`  
		Last Modified: Thu, 02 May 2024 03:32:44 GMT  
		Size: 12.4 MB (12420134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df0a0554ff68c5615ab4abd7e9104f7c1c75de5d3efc6044c3e2a6d702e6fe6`  
		Last Modified: Thu, 02 May 2024 03:32:43 GMT  
		Size: 457.9 KB (457886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c591031c14666b19b590df7de96d00eda64b3e1930b211ff13596e61094785a`  
		Last Modified: Thu, 02 May 2024 03:32:43 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
