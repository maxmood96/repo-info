## `tomcat:9-jre8-temurin`

```console
$ docker pull tomcat@sha256:2279936abf26b55e9ad6bd2b3c0c68001aeacaf5ef2775f8810bee7994276a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:9-jre8-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:892f5e4df2d10e2205db4c8c2558ced115c3b2bc1c34a0a1f636a8db83eaf061
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98115742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee650b8131f734da4c613026fa8b711b01428f4461b3c8b75eda633788a1ef6e`
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
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='17550a6a4ddf71ac81ba8f276467bc58f036c123c0f1bafcafd69f70e3e49cf5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8d994332a2ff15d48bf04405c3b2f6bd331a928dd96639b15e62891f7172363';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='1a6b470ac83b241223447a1e6cb55c4a8f78af0146b9387e9842625041226654';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='d3157230c01b320e47ad6df650e83b15f8f76294d0df9f1c03867d07fe2883c9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 May 2024 07:01:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 02 May 2024 07:01:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 07:01:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 02 May 2024 07:01:41 GMT
WORKDIR /usr/local/tomcat
# Thu, 02 May 2024 07:01:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 07:01:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 07:01:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 02 May 2024 07:01:42 GMT
ENV TOMCAT_MAJOR=9
# Tue, 07 May 2024 21:44:44 GMT
ENV TOMCAT_VERSION=9.0.89
# Tue, 07 May 2024 21:44:44 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Tue, 07 May 2024 21:44:44 GMT
COPY dir:5f8e24594900e3f35f7c557bc7c9761b19919d0939c2e021524c6d23171a0f27 in /usr/local/tomcat 
# Tue, 07 May 2024 21:44:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 07 May 2024 21:44:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 07 May 2024 21:44:51 GMT
EXPOSE 8080
# Tue, 07 May 2024 21:44:51 GMT
ENTRYPOINT []
# Tue, 07 May 2024 21:44:51 GMT
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
	-	`sha256:e915201eb1e46d17fdde5575ee5c77755bb6706a1144b92222e09a2bce9a7af3`  
		Last Modified: Thu, 02 May 2024 01:16:10 GMT  
		Size: 41.9 MB (41877276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2cd90d5914d0a35085906967d900466e444b12ca8ebde10f85b3ed45f4afd3`  
		Last Modified: Thu, 02 May 2024 01:16:05 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd43359ac97a730d0ba68158017979bb844ef04f3f0fb0ceb7fc7a6554ea63c`  
		Last Modified: Thu, 02 May 2024 01:16:05 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68cad482b6dbf87c201196c8d356205ba6a2090b8804c97817a99324aab4877`  
		Last Modified: Thu, 02 May 2024 07:12:03 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7e701bc661c035896add68434d6f08e0ae5129a596f7776a0880e75d9eb8e1`  
		Last Modified: Tue, 07 May 2024 21:53:26 GMT  
		Size: 12.4 MB (12435707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f09ace31925dbb5c50b79734eac99a072951fa126f0573ad9adb43df89c1b6`  
		Last Modified: Tue, 07 May 2024 21:53:25 GMT  
		Size: 456.3 KB (456308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02b3a43cf6ff7ef1a90444a1923fbd652c9be551b533e66971745eb2175b1bf`  
		Last Modified: Tue, 07 May 2024 21:53:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:6b42b95fe21749663e57d788dc82461239197cd439e2a64e72fa7a81f846c813
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92384434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a812c8c99161c51a5fb0561d061370b3de70c13a343d825a5b7992c49958107d`
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
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='17550a6a4ddf71ac81ba8f276467bc58f036c123c0f1bafcafd69f70e3e49cf5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8d994332a2ff15d48bf04405c3b2f6bd331a928dd96639b15e62891f7172363';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='1a6b470ac83b241223447a1e6cb55c4a8f78af0146b9387e9842625041226654';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='d3157230c01b320e47ad6df650e83b15f8f76294d0df9f1c03867d07fe2883c9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 May 2024 02:20:17 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 02 May 2024 02:20:17 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 02:20:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 02 May 2024 02:20:17 GMT
WORKDIR /usr/local/tomcat
# Thu, 02 May 2024 02:20:17 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 02:20:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 02:20:18 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 02 May 2024 02:20:18 GMT
ENV TOMCAT_MAJOR=9
# Thu, 02 May 2024 02:20:18 GMT
ENV TOMCAT_VERSION=9.0.88
# Thu, 02 May 2024 02:20:18 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Thu, 02 May 2024 02:20:18 GMT
COPY dir:f092d34aa0df72b61febf34598f788b85350b61ae3cc53b5e6fd57ea25d51a5d in /usr/local/tomcat 
# Thu, 02 May 2024 02:20:23 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 02:20:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 02 May 2024 02:20:25 GMT
EXPOSE 8080
# Thu, 02 May 2024 02:20:25 GMT
ENTRYPOINT []
# Thu, 02 May 2024 02:20:25 GMT
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
	-	`sha256:8a50186107569e96ee2815fe9b1a8883efa40aa4094775da5662c145a2d71516`  
		Last Modified: Thu, 02 May 2024 01:28:36 GMT  
		Size: 39.6 MB (39564665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ad94ba4960a8848c4a067d12d55a5f1b11e9dcc90a5610993de7a6b702c65a`  
		Last Modified: Thu, 02 May 2024 01:28:31 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf557da0bc1e710e7343dbdd3c3d3e741bd72be61111361923f6a195c65c7dc`  
		Last Modified: Thu, 02 May 2024 01:28:31 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3be495a47158c2755855a54bfedfd9d171fa979f64d8883f2bc46e1e60d0027`  
		Last Modified: Thu, 02 May 2024 02:26:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89449d48cf27277d5dbcf30ed34e36a46548163ae8a99b6418c2a5d076ded3a`  
		Last Modified: Thu, 02 May 2024 02:27:00 GMT  
		Size: 12.4 MB (12357132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60f8c6fb0210e1e3680c89aa1dd772c9daa6bbff4830eb73d81b474eeff26e3`  
		Last Modified: Thu, 02 May 2024 02:26:59 GMT  
		Size: 430.9 KB (430945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27075db89cf74ed83548e277a051dce4b6c8167b85a44baa10e50baf60d0956c`  
		Last Modified: Thu, 02 May 2024 02:26:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:76c01cfa3c184938b02c433eaa666279b48bd336410c6677184f0ae341ae920e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94984690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2bb65e2d99d78d1cc759f5a18f73cdd163bad1da7a93324748e2524398042d`
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
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='17550a6a4ddf71ac81ba8f276467bc58f036c123c0f1bafcafd69f70e3e49cf5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8d994332a2ff15d48bf04405c3b2f6bd331a928dd96639b15e62891f7172363';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='1a6b470ac83b241223447a1e6cb55c4a8f78af0146b9387e9842625041226654';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='d3157230c01b320e47ad6df650e83b15f8f76294d0df9f1c03867d07fe2883c9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 May 2024 07:40:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 02 May 2024 07:40:19 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 07:40:19 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 02 May 2024 07:40:20 GMT
WORKDIR /usr/local/tomcat
# Thu, 02 May 2024 07:40:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 07:40:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 07:40:20 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 02 May 2024 07:40:20 GMT
ENV TOMCAT_MAJOR=9
# Thu, 02 May 2024 07:40:20 GMT
ENV TOMCAT_VERSION=9.0.88
# Thu, 02 May 2024 07:40:20 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Thu, 02 May 2024 07:40:20 GMT
COPY dir:4a9d07b3a24d70e6d3bbeaa310d027eef704b5afe7ad48f71cd42cccc990ac54 in /usr/local/tomcat 
# Thu, 02 May 2024 07:40:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 07:40:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 02 May 2024 07:40:25 GMT
EXPOSE 8080
# Thu, 02 May 2024 07:40:25 GMT
ENTRYPOINT []
# Thu, 02 May 2024 07:40:25 GMT
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
	-	`sha256:fc8ffd1866b98a447cd5ac5e11f530c8e4e0b4c3e320e58f158c2403c75a9996`  
		Last Modified: Thu, 02 May 2024 04:18:01 GMT  
		Size: 40.9 MB (40850775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982c183ea9ee8e6185f12a87b90ba8f16a5753a9a6d66a79b16d5b7286bd5875`  
		Last Modified: Thu, 02 May 2024 04:17:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c7c0f4d6a870839c6546dc4f99fe0d4bb0ac6904fd708e335476bf1525f2b4`  
		Last Modified: Thu, 02 May 2024 04:17:58 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36da5dd301262ace1a1dd73d4659529725cda80e66aa5efd0ad221c347d5e8bb`  
		Last Modified: Thu, 02 May 2024 07:50:07 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ec059bbb8ae3838b90f2d6d72e4e6a00aa53317485f54c6a8500f92b9a9716`  
		Last Modified: Thu, 02 May 2024 07:50:08 GMT  
		Size: 12.4 MB (12428955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409f52f7dd27f2c4be0650c87503f5d4f2d9ed9f1c04331da666d33ded198e63`  
		Last Modified: Thu, 02 May 2024 07:50:07 GMT  
		Size: 455.5 KB (455548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136ea3b31a09f09b3b172ae500d09e95cac5cfcf41d3c5517315819c6152853e`  
		Last Modified: Thu, 02 May 2024 07:50:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:06bd78c0c4e463bd95e92630b5b945b6b27789effa93d36aaa4dfd88e8eae4dc
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103537676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a3066fc0134580ac0267ac469896d0510ddba18b47b1c0482aff95811a8ed1`
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
ENV JAVA_VERSION=jdk8u412-b08
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='17550a6a4ddf71ac81ba8f276467bc58f036c123c0f1bafcafd69f70e3e49cf5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u412b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8d994332a2ff15d48bf04405c3b2f6bd331a928dd96639b15e62891f7172363';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_x64_linux_hotspot_8u412b08.tar.gz';          ;;        armhf|arm)          ESUM='1a6b470ac83b241223447a1e6cb55c4a8f78af0146b9387e9842625041226654';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_arm_linux_hotspot_8u412b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='d3157230c01b320e47ad6df650e83b15f8f76294d0df9f1c03867d07fe2883c9';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u412-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u412b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 02 May 2024 05:02:57 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 02 May 2024 05:02:57 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:02:59 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 02 May 2024 05:02:59 GMT
WORKDIR /usr/local/tomcat
# Thu, 02 May 2024 05:03:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 05:03:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 02 May 2024 05:03:01 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 02 May 2024 05:03:01 GMT
ENV TOMCAT_MAJOR=9
# Thu, 02 May 2024 05:03:02 GMT
ENV TOMCAT_VERSION=9.0.88
# Thu, 02 May 2024 05:03:02 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Thu, 02 May 2024 05:03:03 GMT
COPY dir:73c73c1e6c0c3a82d246e8af63b34e971cf626187b5372da5ae5c0671780d0b5 in /usr/local/tomcat 
# Thu, 02 May 2024 05:03:11 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 05:03:16 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 02 May 2024 05:03:16 GMT
EXPOSE 8080
# Thu, 02 May 2024 05:03:17 GMT
ENTRYPOINT []
# Thu, 02 May 2024 05:03:17 GMT
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
	-	`sha256:1f1617169fdad167df0c97043f1e11c576804eb7f27246f9c1a679c97b46376e`  
		Last Modified: Thu, 02 May 2024 01:52:19 GMT  
		Size: 41.2 MB (41242448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ac1d2348b265519f2f164f6d38edf7c5480c1840c66d32619097ad68a3d21c`  
		Last Modified: Thu, 02 May 2024 01:52:13 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad657d7cdb67b2055e621134f25d6ed7cd3382965b2e2f3b5cb6d34b22c0e28`  
		Last Modified: Thu, 02 May 2024 01:52:13 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa401d59802d209c075f63fe0a472df7cfb89bcd831506e6447e93f1ffec2042`  
		Last Modified: Thu, 02 May 2024 05:15:22 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575b166f8f9e99157c858415104dfe0dee163a771f0711c91aade43a7ecae5b4`  
		Last Modified: Thu, 02 May 2024 05:15:23 GMT  
		Size: 12.5 MB (12450485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07804943d65dc86b19790901cacf340abc2dc3f9b7be887883c0625b573d4a36`  
		Last Modified: Thu, 02 May 2024 05:15:22 GMT  
		Size: 487.6 KB (487570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1fa95d8ff790885b49121b77cad20b296846edef0239f6248ee71476b0d502`  
		Last Modified: Thu, 02 May 2024 05:15:21 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
