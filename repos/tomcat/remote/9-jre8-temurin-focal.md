## `tomcat:9-jre8-temurin-focal`

```console
$ docker pull tomcat@sha256:eec98fdd711ec7194f610c17ed2d2ce9b2bd48cfcc16e5ba94b2d2c6f91adf77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:9-jre8-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:643831521e3ad934bf872d7dad71acbd75976f06710cee055f8e455ed8c2fe28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.3 MB (100338722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902dd73a1c29b181e9ed0b9123d03cfe2ea2d87f66f79016f0db62947046926b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
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
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='17550a6a4ddf71ac81ba8f276467bc58f036c123c0f1bafcafd69f70e3e49cf5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8d994332a2ff15d48bf04405c3b2f6bd331a928dd96639b15e62891f7172363';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='1a6b470ac83b241223447a1e6cb55c4a8f78af0146b9387e9842625041226654';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='d3157230c01b320e47ad6df650e83b15f8f76294d0df9f1c03867d07fe2883c9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 May 2024 07:02:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 02 May 2024 07:02:34 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 07:02:35 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 02 May 2024 07:02:35 GMT
WORKDIR /usr/local/tomcat
# Thu, 02 May 2024 07:02:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 07:02:35 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 07:02:35 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 02 May 2024 07:02:35 GMT
ENV TOMCAT_MAJOR=9
# Tue, 07 May 2024 21:45:35 GMT
ENV TOMCAT_VERSION=9.0.89
# Tue, 07 May 2024 21:45:36 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Tue, 07 May 2024 21:45:36 GMT
COPY dir:693826105fceaacca918c25366aa71f33bda5a8214400a9a855e98e2d23d6bfc in /usr/local/tomcat 
# Tue, 07 May 2024 21:45:41 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 21:45:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 07 May 2024 21:45:43 GMT
EXPOSE 8080
# Tue, 07 May 2024 21:45:43 GMT
ENTRYPOINT []
# Tue, 07 May 2024 21:45:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eb874ca572c30548f8b3ccb6743465ceb027c1547a6159c7e8c0cfd9d2990c`  
		Last Modified: Thu, 02 May 2024 01:15:11 GMT  
		Size: 16.9 MB (16921162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23859a692cd747ee418e461369d4413735811672bf0d509304a6190a2894396d`  
		Last Modified: Thu, 02 May 2024 01:15:56 GMT  
		Size: 41.9 MB (41878889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8bf32075646da2b1e005c4cc7b1f8daf5fefeb424ac9c270b9c89d9178dd24`  
		Last Modified: Thu, 02 May 2024 01:15:51 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8631b71d7ecdb91b430009ca3ae466872e2ad1007bf0d96a559c6ea4278cc4b9`  
		Last Modified: Thu, 02 May 2024 01:15:51 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62aa2d5c077bb12ab1bb2185fde57f59d3bf2b05046a807405ded7e59716efd1`  
		Last Modified: Thu, 02 May 2024 07:12:38 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148cb59a7eb3c9fb9026e1af435d40fbfbdecaee76acadae60c74b3475bae704`  
		Last Modified: Tue, 07 May 2024 21:54:02 GMT  
		Size: 12.5 MB (12503442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6933ba9014c28c45186e8f92ba986b998eed46d00b06dd1faa1a13acef54b0`  
		Last Modified: Tue, 07 May 2024 21:54:02 GMT  
		Size: 449.7 KB (449735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474a906079183f30e5f6eecff41c75abedcb0a6b9fd4ea3e3afc100ad5b6311c`  
		Last Modified: Tue, 07 May 2024 21:54:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:1e9b88f41ad465c2541115ad0c03e8de2f1f631668dbceb815d0f42495383edb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92715921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846d6156df1a450e032d887d3cbfd17c864f6971e1a100d1e2cf1d9ac58c2438`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 03 Jun 2024 16:44:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:44:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:44:23 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:44:26 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Mon, 03 Jun 2024 16:44:26 GMT
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
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='17550a6a4ddf71ac81ba8f276467bc58f036c123c0f1bafcafd69f70e3e49cf5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8d994332a2ff15d48bf04405c3b2f6bd331a928dd96639b15e62891f7172363';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='1a6b470ac83b241223447a1e6cb55c4a8f78af0146b9387e9842625041226654';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='d3157230c01b320e47ad6df650e83b15f8f76294d0df9f1c03867d07fe2883c9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 05 Jun 2024 05:43:37 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 05 Jun 2024 05:43:37 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jun 2024 05:43:37 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 05 Jun 2024 05:43:37 GMT
WORKDIR /usr/local/tomcat
# Wed, 05 Jun 2024 05:43:37 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jun 2024 05:43:37 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 05 Jun 2024 05:43:38 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 05 Jun 2024 05:43:38 GMT
ENV TOMCAT_MAJOR=9
# Wed, 05 Jun 2024 05:43:38 GMT
ENV TOMCAT_VERSION=9.0.89
# Wed, 05 Jun 2024 05:43:38 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Wed, 05 Jun 2024 05:43:39 GMT
COPY dir:bea5a34e5f130582fa3e5d23bb4e55debba7f9b7a8640ea52b7c50ca97aef66c in /usr/local/tomcat 
# Wed, 05 Jun 2024 05:43:43 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:43:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 05 Jun 2024 05:43:44 GMT
EXPOSE 8080
# Wed, 05 Jun 2024 05:43:44 GMT
ENTRYPOINT []
# Wed, 05 Jun 2024 05:43:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd806615dd9e79fe2050b42062de2990cd11200b6ffc1fa232a301bdbba22f2`  
		Last Modified: Wed, 05 Jun 2024 03:59:31 GMT  
		Size: 15.7 MB (15665820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03e132bcd7cd63ba6e6db01a02a26f1328e0ac2ac080d5e899e2aa1927e89b3`  
		Last Modified: Wed, 05 Jun 2024 04:00:13 GMT  
		Size: 39.6 MB (39565664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d225ffdd47c6d0b28176e8221a3ab2edfa570efffbdf02e8ed2d7d50e6ea1578`  
		Last Modified: Wed, 05 Jun 2024 04:00:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b776c35dc6081b86cdabc23ddcca87615bfead004f5845cd7bba5b2b9c8521c9`  
		Last Modified: Wed, 05 Jun 2024 04:00:08 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b579f44c40831c22b7fc54bc21df3df561a1baaf00d5fbcd4a3cc221aa6d7f74`  
		Last Modified: Wed, 05 Jun 2024 05:49:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7282405ddff837c7a388b9a8bf540e96f4b072e677fe97d615789f087c758d5`  
		Last Modified: Wed, 05 Jun 2024 05:49:42 GMT  
		Size: 12.5 MB (12451928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30185b4b74fff9aa5bd92fcb0e0974cc7356bcc87045de78ff44040deb48049a`  
		Last Modified: Wed, 05 Jun 2024 05:49:41 GMT  
		Size: 427.6 KB (427562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a85e48e4bf6bd248b3c50ce3338437783762bcbcc470dfbaf89fc92f2feccb`  
		Last Modified: Wed, 05 Jun 2024 05:49:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:a39939525b6104fdc79f37a4fa210ea3f26aae9b25a31af026102f82369fdc97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97807682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51163eab0f42ca7e84d177ff16d771ea8681d5711622a8652ed7da4ff5de3656`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
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
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='17550a6a4ddf71ac81ba8f276467bc58f036c123c0f1bafcafd69f70e3e49cf5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8d994332a2ff15d48bf04405c3b2f6bd331a928dd96639b15e62891f7172363';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='1a6b470ac83b241223447a1e6cb55c4a8f78af0146b9387e9842625041226654';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='d3157230c01b320e47ad6df650e83b15f8f76294d0df9f1c03867d07fe2883c9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 May 2024 07:40:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 02 May 2024 07:40:55 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 07:40:56 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 02 May 2024 07:40:56 GMT
WORKDIR /usr/local/tomcat
# Thu, 02 May 2024 07:40:56 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 07:40:56 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 07:40:56 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 02 May 2024 07:40:56 GMT
ENV TOMCAT_MAJOR=9
# Tue, 07 May 2024 23:26:12 GMT
ENV TOMCAT_VERSION=9.0.89
# Tue, 07 May 2024 23:26:12 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Tue, 07 May 2024 23:26:13 GMT
COPY dir:a7f0ffb31232d60e2960a9a2e576c27ae349e0b8b727c2e9a3bc7996f4708e6c in /usr/local/tomcat 
# Tue, 07 May 2024 23:26:17 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 23:26:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 07 May 2024 23:26:18 GMT
EXPOSE 8080
# Tue, 07 May 2024 23:26:19 GMT
ENTRYPOINT []
# Tue, 07 May 2024 23:26:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:83049506c6eb6b11ef1a8774b3486a01a1804f7d13bd230b44788bc63248282d`  
		Last Modified: Mon, 29 Apr 2024 19:12:05 GMT  
		Size: 27.2 MB (27206145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3510597c9954b37f646e357b476e00ba683391a190199312f9fd3f1344ca2d`  
		Last Modified: Thu, 02 May 2024 04:17:12 GMT  
		Size: 16.8 MB (16777842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e2349abfb53036431ab29e50e0651545f571e51745f35f28af4ac747858d88`  
		Last Modified: Thu, 02 May 2024 04:17:50 GMT  
		Size: 40.9 MB (40851490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b025fe7ebdf8ad4105e270a410d86464ab5e7649f7d1086ac62dce12d8651d86`  
		Last Modified: Thu, 02 May 2024 04:17:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c89ae9f0747abaf85afbe988be280954937076a5b86f498d7fe38f1cb6ebf2`  
		Last Modified: Thu, 02 May 2024 04:17:46 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bf5131c5b4d5f7872243b1b3f5ce403f57a6acbb32efa7f6e80a1ffb6a54a9`  
		Last Modified: Thu, 02 May 2024 07:50:41 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5873b3106232a755e7f258662113ee6fb14630fd3e1f4f9aca1ed4e210d9359`  
		Last Modified: Tue, 07 May 2024 23:34:11 GMT  
		Size: 12.5 MB (12521219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b9ffccef50550356593a2296ca121a86db96cbe7ce730b5232076d7065dfa0`  
		Last Modified: Tue, 07 May 2024 23:34:10 GMT  
		Size: 449.8 KB (449797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fe25fbeb3af8bc459fab0f471ec70b06cd8abef88c5d3bf7e6aca4d6d7097c`  
		Last Modified: Tue, 07 May 2024 23:34:10 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:08786ea8a369cb4fe6b88959b4732800c568ba291a782ccdda25634bbdecb732
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.8 MB (105803291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40c16b993960e4dce5e756107158e4c7712dd25828f6eb5382c19a86b3c5d70`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 27 Apr 2024 13:33:02 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:33:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:33:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:33:02 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 13:33:06 GMT
ADD file:de463dcd7b30faec6d782106816b443697c99747238015d4d992786da4888987 in / 
# Sat, 27 Apr 2024 13:33:06 GMT
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
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='17550a6a4ddf71ac81ba8f276467bc58f036c123c0f1bafcafd69f70e3e49cf5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8d994332a2ff15d48bf04405c3b2f6bd331a928dd96639b15e62891f7172363';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='1a6b470ac83b241223447a1e6cb55c4a8f78af0146b9387e9842625041226654';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='d3157230c01b320e47ad6df650e83b15f8f76294d0df9f1c03867d07fe2883c9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 May 2024 05:05:01 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 02 May 2024 05:05:01 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:05:03 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 02 May 2024 05:05:03 GMT
WORKDIR /usr/local/tomcat
# Thu, 02 May 2024 05:05:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 05:05:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 05:05:05 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 02 May 2024 05:05:05 GMT
ENV TOMCAT_MAJOR=9
# Tue, 07 May 2024 22:55:32 GMT
ENV TOMCAT_VERSION=9.0.89
# Tue, 07 May 2024 22:55:33 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Tue, 07 May 2024 22:55:33 GMT
COPY dir:abaf583a0c38f89fcfaeee71d08e7827fac6fad622c24b1fde1861ee86fd496b in /usr/local/tomcat 
# Tue, 07 May 2024 22:55:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 22:55:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 07 May 2024 22:55:43 GMT
EXPOSE 8080
# Tue, 07 May 2024 22:55:43 GMT
ENTRYPOINT []
# Tue, 07 May 2024 22:55:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:842f501e2541cf3af2b2c183cb8bc0e8ee178240b7a31e44ca04a5741c69410b`  
		Last Modified: Thu, 02 May 2024 01:51:19 GMT  
		Size: 33.3 MB (33316011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a680bfbe33125da457ff9d39f64548e1fcd6e34c4da44faa1039f934edc56adc`  
		Last Modified: Thu, 02 May 2024 01:51:19 GMT  
		Size: 18.2 MB (18222362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684fb564478531ac94f84cde39af86d5e97c5742ed0021dd88bad329e8fb92ef`  
		Last Modified: Thu, 02 May 2024 01:52:05 GMT  
		Size: 41.2 MB (41244355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289ac01ba630def53b56eac6a2fa4dfd0e6f13ad478dad44f5cfab895e841188`  
		Last Modified: Thu, 02 May 2024 01:51:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dd9c3dd700b818f39cb09e6bfd2062df82b2a53968450402bdcc35fa305b43`  
		Last Modified: Thu, 02 May 2024 01:51:58 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a39ecd938a8659788423dfde03d0f8f0e98e8fbce907392ce8028082eb1aff`  
		Last Modified: Thu, 02 May 2024 05:16:01 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65feea63bd927eb39d60eb6e862649db3ed1c476072676998350a54ffd6a7ee8`  
		Last Modified: Tue, 07 May 2024 23:02:39 GMT  
		Size: 12.5 MB (12544087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8845c3bcf0f1847ad9da67578b963e287b769060493984dc6f73dc7ade524456`  
		Last Modified: Tue, 07 May 2024 23:02:38 GMT  
		Size: 475.3 KB (475281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d131b9da0f99b573abac2477b92c57f77f164d4d654363849c63d0b0fbcf7e6`  
		Last Modified: Tue, 07 May 2024 23:02:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
