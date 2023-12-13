## `xwiki:lts-postgres-tomcat`

```console
$ docker pull xwiki@sha256:7a00453464764ed13569898ebedde021d85ffb533a377a6a988dbe6566701642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `xwiki:lts-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:5071aab2bc1f5df00e21862dfd63db312bc0be2cc998b4a853080ede34101eda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.8 MB (597791247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a77b009defeeff730d1e831b1fcc13bd8f18b998199106c41fd39bd04c904ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 01:58:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 01:58:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 01:58:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 02:01:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 02:01:05 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 02 Dec 2023 02:01:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 02 Dec 2023 02:01:44 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 02 Dec 2023 02:01:44 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Dec 2023 02:01:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Dec 2023 08:19:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Dec 2023 08:19:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 08:19:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Dec 2023 08:19:43 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Dec 2023 08:19:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 08:19:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 08:22:07 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 02 Dec 2023 08:22:07 GMT
ENV TOMCAT_MAJOR=9
# Wed, 13 Dec 2023 02:02:03 GMT
ENV TOMCAT_VERSION=9.0.84
# Wed, 13 Dec 2023 02:02:04 GMT
ENV TOMCAT_SHA512=85a42ab5e7e4cb1923888e96a78a0f277a870d06e76147a95457878c124001c9a317eade4ad69c249a460ffe2cbefe894022b84389cdf33038bc456e3699c8e3
# Wed, 13 Dec 2023 02:02:04 GMT
COPY dir:207feb1b68100e536beb2118e3d4075a1a6295d24b1358e7b8b4586db2003d06 in /usr/local/tomcat 
# Wed, 13 Dec 2023 02:02:08 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2023 02:02:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Dec 2023 02:02:10 GMT
EXPOSE 8080
# Wed, 13 Dec 2023 02:02:10 GMT
ENTRYPOINT []
# Wed, 13 Dec 2023 02:02:10 GMT
CMD ["catalina.sh" "run"]
# Wed, 13 Dec 2023 03:05:12 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 13 Dec 2023 03:05:12 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 13 Dec 2023 03:05:12 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 13 Dec 2023 03:05:12 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 13 Dec 2023 03:05:12 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 13 Dec 2023 03:05:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 13 Dec 2023 03:10:03 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2023 03:11:54 GMT
ENV XWIKI_VERSION=14.10.20
# Wed, 13 Dec 2023 03:11:54 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.20
# Wed, 13 Dec 2023 03:11:55 GMT
ENV XWIKI_DOWNLOAD_SHA256=c418601676d61893ccb9e066b1f2bcce56717b49e5c2456656b6960db6bd6e4c
# Wed, 13 Dec 2023 03:12:32 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 13 Dec 2023 03:12:34 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 13 Dec 2023 03:12:34 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 13 Dec 2023 03:12:34 GMT
COPY file:98c6046d1b5e77229fc6e67481d24fd005196575f4e4fd725e7d3db07bd9601b in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 13 Dec 2023 03:12:35 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 13 Dec 2023 03:12:35 GMT
COPY file:9cbfa36f41bbf2137b768a707fab0bad1de6eef9a2d12e7c0fc0565ffdfeb1d4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 13 Dec 2023 03:12:35 GMT
VOLUME [/usr/local/xwiki]
# Wed, 13 Dec 2023 03:12:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Dec 2023 03:12:35 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd63fc495d1a4839e5239c716fa5a6ec48209bff26db1e7d7af7b0701ac4ee7`  
		Last Modified: Sat, 02 Dec 2023 02:06:15 GMT  
		Size: 17.5 MB (17455452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c42674dea4fe1d59945de1102de69ceb99f21310cb6b7f6fcccdd43b07a8acf`  
		Last Modified: Sat, 02 Dec 2023 02:06:58 GMT  
		Size: 47.1 MB (47149362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a992519bbaeefaec0b90db8a0d65735dd823a054e2f332d4dade7315733bf084`  
		Last Modified: Sat, 02 Dec 2023 02:06:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506583e9517b9e597323949bc904a17f5054f4ac1e7a64d3bd587a9b87226f61`  
		Last Modified: Sat, 02 Dec 2023 02:06:52 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76eec8f511751601d4c750c85aae4e5ccbb964961e9b9eb29220a58a53680b6`  
		Last Modified: Sat, 02 Dec 2023 08:38:09 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61257167b8ec71da183848e82ccc7da9990f615303e6469564f6842c110f382`  
		Last Modified: Wed, 13 Dec 2023 02:29:24 GMT  
		Size: 12.4 MB (12398192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727a95ba686e4aa441b9a13ce1855debabac3e4db02b1c6f9c33e0b55ff5eacc`  
		Last Modified: Wed, 13 Dec 2023 02:29:23 GMT  
		Size: 458.5 KB (458492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2452d12a8e6f96fed8f2fd31f925baa8b99c26383edb94f96beef0f7569b50a`  
		Last Modified: Wed, 13 Dec 2023 02:29:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1db303da261d3a374f727f47098bc29ac9cef06fa77c5ee1ae13cb312528b5e`  
		Last Modified: Wed, 13 Dec 2023 03:16:22 GMT  
		Size: 179.8 MB (179783624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0207f59a9f63b4880148ed0a25596fbf00c817ce7671025227a29cf8a6a98ccf`  
		Last Modified: Wed, 13 Dec 2023 03:18:03 GMT  
		Size: 309.1 MB (309149399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b85171d702f2a418ecf7013a627e04c1d7907ec202acaa3e0e9e414a2b52d96`  
		Last Modified: Wed, 13 Dec 2023 03:17:47 GMT  
		Size: 936.8 KB (936844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfab1b1998f5d3dfee1e3cee2b6b5753f89040e1396806ca8a43345957b4d580`  
		Last Modified: Wed, 13 Dec 2023 03:17:46 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80226ef470d4f8b80243bc974e1b3648651207fa6f07f1c351c6b0d30041a2e5`  
		Last Modified: Wed, 13 Dec 2023 03:17:47 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0ccf3ec76b5d6930a03731e8787d5cc502ef56bce3429cb5c6c359b3502e18`  
		Last Modified: Wed, 13 Dec 2023 03:17:47 GMT  
		Size: 6.1 KB (6128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6addccb173430e84a96b27d832a4e80dcf52940f958f524e1a2743de1ea59f2`  
		Last Modified: Wed, 13 Dec 2023 03:17:47 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `xwiki:lts-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2a85fa895f1417a186e209745a59422e38e8f505e77fca5d8d668f9540651087
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.6 MB (591636750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e8740a86ca91c1055dd88fd4c9c1fd6cbec1ec675129e8b1941ceb54005a87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Dec 2023 07:43:19 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:43:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:43:20 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:43:21 GMT
ADD file:891dcab0c4ce2880c4dca013d326a3efd7601003b6f5076938d678101e301b79 in / 
# Fri, 01 Dec 2023 07:43:22 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:30:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 05:30:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 05:30:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 05:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 05:32:58 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 02 Dec 2023 05:33:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 02 Dec 2023 05:33:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 02 Dec 2023 05:33:24 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Dec 2023 05:33:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Dec 2023 10:28:30 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Dec 2023 10:28:30 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 10:28:31 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Dec 2023 10:28:31 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Dec 2023 10:28:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 10:28:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Dec 2023 10:30:26 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 02 Dec 2023 10:30:26 GMT
ENV TOMCAT_MAJOR=9
# Wed, 13 Dec 2023 01:55:46 GMT
ENV TOMCAT_VERSION=9.0.84
# Wed, 13 Dec 2023 01:55:46 GMT
ENV TOMCAT_SHA512=85a42ab5e7e4cb1923888e96a78a0f277a870d06e76147a95457878c124001c9a317eade4ad69c249a460ffe2cbefe894022b84389cdf33038bc456e3699c8e3
# Wed, 13 Dec 2023 01:55:46 GMT
COPY dir:d9322ad19f3aadab89229d19460ab3fb136a2ce98f5be97a657d70e7e03f9439 in /usr/local/tomcat 
# Wed, 13 Dec 2023 01:55:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2023 01:55:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 13 Dec 2023 01:55:51 GMT
EXPOSE 8080
# Wed, 13 Dec 2023 01:55:51 GMT
ENTRYPOINT []
# Wed, 13 Dec 2023 01:55:51 GMT
CMD ["catalina.sh" "run"]
# Wed, 13 Dec 2023 03:07:18 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 13 Dec 2023 03:07:18 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 13 Dec 2023 03:07:18 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 13 Dec 2023 03:07:18 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 13 Dec 2023 03:07:18 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 13 Dec 2023 03:07:18 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 13 Dec 2023 03:10:51 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/*
# Wed, 13 Dec 2023 03:12:41 GMT
ENV XWIKI_VERSION=14.10.20
# Wed, 13 Dec 2023 03:12:41 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.20
# Wed, 13 Dec 2023 03:12:41 GMT
ENV XWIKI_DOWNLOAD_SHA256=c418601676d61893ccb9e066b1f2bcce56717b49e5c2456656b6960db6bd6e4c
# Wed, 13 Dec 2023 03:13:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war
# Wed, 13 Dec 2023 03:13:24 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/
# Wed, 13 Dec 2023 03:13:24 GMT
COPY file:0a1be11e2eb610a1dbcd415404e3a592641110b93090030cb831e3a19a163017 in /usr/local/tomcat/bin/ 
# Wed, 13 Dec 2023 03:13:24 GMT
COPY file:98c6046d1b5e77229fc6e67481d24fd005196575f4e4fd725e7d3db07bd9601b in /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml 
# Wed, 13 Dec 2023 03:13:24 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed
# Wed, 13 Dec 2023 03:13:24 GMT
COPY file:9cbfa36f41bbf2137b768a707fab0bad1de6eef9a2d12e7c0fc0565ffdfeb1d4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 13 Dec 2023 03:13:25 GMT
VOLUME [/usr/local/xwiki]
# Wed, 13 Dec 2023 03:13:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Dec 2023 03:13:25 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:aeb9f260d781cd1e09daf0d0a9e5bcb581efce5b33b221f2f4a27de8db66e463`  
		Last Modified: Thu, 30 Nov 2023 02:35:43 GMT  
		Size: 28.4 MB (28399939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c3988b1198250f931d321166ff7a5f1bbd03b8fa06eae348c92ef639a62393`  
		Last Modified: Sat, 02 Dec 2023 05:37:12 GMT  
		Size: 18.9 MB (18857837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0451cfbb70a802ae4861e4e9957e778b9fd0d5072b981d80950164d639df6ecb`  
		Last Modified: Sat, 02 Dec 2023 05:37:50 GMT  
		Size: 46.6 MB (46624045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332ede580b745c8969408589f1921b71bdf198c6aefc33463d3d2dc815df73e8`  
		Last Modified: Sat, 02 Dec 2023 05:37:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b8f9c326b7dd6d03972c72e618e72c738e042baf084b2b2be95c25203c6ca0`  
		Last Modified: Sat, 02 Dec 2023 05:37:44 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3f0afaced9459acf9df8ee72f1e9c5d5b2b83bfd4c230f016dd8f2d3792a9b`  
		Last Modified: Sat, 02 Dec 2023 10:43:28 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245978d592d8bbfebc82f0c516439d70e7c8577f0288be9032b3830e4fb3eb59`  
		Last Modified: Wed, 13 Dec 2023 02:19:10 GMT  
		Size: 12.4 MB (12407527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d43e808368ce2a6bec77bca1f1f890ebe3bccce2b69ccefa51fb75352a649c`  
		Last Modified: Wed, 13 Dec 2023 02:19:09 GMT  
		Size: 458.2 KB (458189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd25beb03eaa9c2f745d5ba4f1900139b9077e1f8c648f748a39cb7b43584162`  
		Last Modified: Wed, 13 Dec 2023 02:19:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e65ef80808bdbed0d2a0cce61375edb45929ef5bc594242cab60e673d5fba3f`  
		Last Modified: Wed, 13 Dec 2023 03:16:44 GMT  
		Size: 174.8 MB (174789406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c56d023283885d7d266b636d57daa5bf43ef4700221afdbdfe20882d0f2b2006`  
		Last Modified: Wed, 13 Dec 2023 03:18:19 GMT  
		Size: 309.1 MB (309149398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12db78260da7611318f476e272841f5c78c8180d9e0787f7d11f434f8543addd`  
		Last Modified: Wed, 13 Dec 2023 03:18:05 GMT  
		Size: 936.9 KB (936852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849860690ea941e669f77ab23200191e9079f0d5cb3bcad68a6c93c62dbfa804`  
		Last Modified: Wed, 13 Dec 2023 03:18:04 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af65667bc77a23a32ded396ee3f4299cf58a7628ac3decbb50ace2d60d9207ff`  
		Last Modified: Wed, 13 Dec 2023 03:18:04 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59042914b4164384b8ad8b983aeb85acc054f07c6c0172db764e3aaa9e0f7bc2`  
		Last Modified: Wed, 13 Dec 2023 03:18:04 GMT  
		Size: 6.1 KB (6129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15db849f967891bf1cef05a7bd13904e99e0ce386b83edbf1dabcf5ffb7e4b9`  
		Last Modified: Wed, 13 Dec 2023 03:18:04 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
