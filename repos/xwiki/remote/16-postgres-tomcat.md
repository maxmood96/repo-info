## `xwiki:16-postgres-tomcat`

```console
$ docker pull xwiki@sha256:a8f2f47dfd19c2b275d9fde8801de5a196a318716cad0df1ebe0e4d70ecf32ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:16-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:75fa08cfd0865f272841635295632bd27ea2a003968afb5636781be5311cbda3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.9 MB (594936332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d861d32345bf35e46908d6015c23e3c25cefcb7364062faddff4ec221dbc73d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 29 Jan 2024 16:20:26 GMT
ARG RELEASE
# Mon, 29 Jan 2024 16:20:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 29 Jan 2024 16:20:26 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Mon, 29 Jan 2024 16:20:26 GMT
CMD ["/bin/bash"]
# Mon, 29 Jan 2024 16:20:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 29 Jan 2024 16:20:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jan 2024 16:20:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Jan 2024 16:20:26 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 29 Jan 2024 16:20:26 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Mon, 29 Jan 2024 16:20:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 29 Jan 2024 16:20:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 29 Jan 2024 16:20:26 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 29 Jan 2024 16:20:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 29 Jan 2024 16:20:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 29 Jan 2024 16:20:26 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jan 2024 16:20:26 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 29 Jan 2024 16:20:26 GMT
WORKDIR /usr/local/tomcat
# Mon, 29 Jan 2024 16:20:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 29 Jan 2024 16:20:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 29 Jan 2024 16:20:26 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 29 Jan 2024 16:20:26 GMT
ENV TOMCAT_MAJOR=9
# Mon, 29 Jan 2024 16:20:26 GMT
ENV TOMCAT_VERSION=9.0.86
# Mon, 29 Jan 2024 16:20:26 GMT
ENV TOMCAT_SHA512=e8a8000dbeba5ee266ec4bf77217574364ffd114c8b913816f2e7a5e4eab4d01d0be3f05c8fccefcb5c5d770308efe1983be80279b6ef6d122d6183288a8ee9c
# Mon, 29 Jan 2024 16:20:26 GMT
COPY dir:1817f6b73a6fe4d923d7f6cf1aa21c95626eef42af1889e1d0a51c69d1ecc970 in /usr/local/tomcat 
# Mon, 29 Jan 2024 16:20:26 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Jan 2024 16:20:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 29 Jan 2024 16:20:26 GMT
EXPOSE 8080
# Mon, 29 Jan 2024 16:20:26 GMT
ENTRYPOINT []
# Mon, 29 Jan 2024 16:20:26 GMT
CMD ["catalina.sh" "run"]
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 29 Jan 2024 16:20:26 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_VERSION=16.0.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.0.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=955c175d0ac0e7039eeafd8569d87ad8a7967092ad8d018decb80a42a7eb941f
# Mon, 29 Jan 2024 16:20:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
VOLUME [/usr/local/xwiki]
# Mon, 29 Jan 2024 16:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jan 2024 16:20:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f947fdc0fc4be68d9f9c4c3912a92df875230cdd8267c01077167a69114f54`  
		Last Modified: Fri, 16 Feb 2024 01:44:10 GMT  
		Size: 17.5 MB (17458484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5374706a264d34f054909a042d958bf140f3624be56e6ca8ee2bd40c4650ae91`  
		Last Modified: Fri, 16 Feb 2024 01:44:40 GMT  
		Size: 47.2 MB (47163245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9aeff6b625d796ae065d95dd069d3f2c999314b436332616a6e3b9397038891`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82faf7b7220dc5dd434962b0d3b1d9f4630792cabb13615559a9cf093d4afb88`  
		Last Modified: Fri, 16 Feb 2024 01:44:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b633af09da77b3268755d4a1d9c430a50ad0a131e1b2ecdb997e3ee6a86978f`  
		Last Modified: Fri, 16 Feb 2024 05:02:20 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fc5dc00b8a0ff1c4c96565d5c87fa8e9aa254b3047454ba5a19d4a2a834043`  
		Last Modified: Wed, 21 Feb 2024 01:34:35 GMT  
		Size: 12.4 MB (12411786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f377b6536232adf2c23b2d9282473726a58f99a99ec67aed49905d42011cec4`  
		Last Modified: Wed, 21 Feb 2024 01:34:33 GMT  
		Size: 458.6 KB (458584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b56a51973ca9dedb84d83b0b25381985672720d95f8f56997161fbbb86c6d18`  
		Last Modified: Wed, 21 Feb 2024 01:34:33 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405e104d27c3c49c14c4afaa48e83ebf9e4ddc005dd1fb3100796b44a0ca9ad8`  
		Last Modified: Wed, 21 Feb 2024 02:50:38 GMT  
		Size: 179.3 MB (179291729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36b594ab160f11d22b08bd95a9a4adc898b09b45d52fbdfff9bc32632ff7604`  
		Last Modified: Wed, 21 Feb 2024 02:50:42 GMT  
		Size: 306.8 MB (306751733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075236b219d68d63b12badf3d03522b462e33dce79efe42fbcb7dc86603c521b`  
		Last Modified: Wed, 21 Feb 2024 02:50:35 GMT  
		Size: 936.8 KB (936848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb99ca6829c70f66e5a08c9231c25527c4eaaff592e3f5d3cc3f9b861d9abe1`  
		Last Modified: Wed, 21 Feb 2024 02:50:35 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a610906c0e7aa582a044dc24dc2a3781d4ac8b3708a605cc1fb2021cde50a48`  
		Last Modified: Wed, 21 Feb 2024 02:50:36 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec2521b8e7c79584c9ff6fa0533be5ca2d348e0a484976132ddf122bf6cf4ef`  
		Last Modified: Wed, 21 Feb 2024 02:50:36 GMT  
		Size: 6.4 KB (6422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96060e5e207bceb8ac507f2ea75199b4a644c0ac8433571b13589217a8b1bc91`  
		Last Modified: Wed, 21 Feb 2024 02:50:37 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:e2ef577789bfa6f6d9de72bc32306d60518f05eb1878f2bffb05bbdba0bc52a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9103666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ada15034e186261a7fa47742eaf058e54b8a93fceb6195fc147ad8a3084fa4c`

```dockerfile
```

-	Layers:
	-	`sha256:44fae8cb45191dae15b4d7cef952c48ff62a1da8db0b6e53b2bbe0b7398a68fa`  
		Last Modified: Wed, 21 Feb 2024 02:50:35 GMT  
		Size: 9.1 MB (9063570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca192f4db1cf42af39e68ca29177a0a4d9108d14029c4267c3b9d67ab8a1e29`  
		Last Modified: Wed, 21 Feb 2024 02:50:35 GMT  
		Size: 40.1 KB (40096 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:16-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:ab8017b750b7ad8cf830b48767442811303388a3ebd4f32d2971df5258011cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.8 MB (588799987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc42a1fb8067334d0bc7dc8824e025f5389e0d632ffd20a1d9bb57797e5f865`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 29 Jan 2024 16:20:26 GMT
ARG RELEASE
# Mon, 29 Jan 2024 16:20:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 29 Jan 2024 16:20:26 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Mon, 29 Jan 2024 16:20:26 GMT
CMD ["/bin/bash"]
# Mon, 29 Jan 2024 16:20:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 29 Jan 2024 16:20:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jan 2024 16:20:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 29 Jan 2024 16:20:26 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 29 Jan 2024 16:20:26 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Mon, 29 Jan 2024 16:20:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 29 Jan 2024 16:20:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 29 Jan 2024 16:20:26 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 29 Jan 2024 16:20:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 29 Jan 2024 16:20:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 29 Jan 2024 16:20:26 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jan 2024 16:20:26 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 29 Jan 2024 16:20:26 GMT
WORKDIR /usr/local/tomcat
# Mon, 29 Jan 2024 16:20:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 29 Jan 2024 16:20:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 29 Jan 2024 16:20:26 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 29 Jan 2024 16:20:26 GMT
ENV TOMCAT_MAJOR=9
# Mon, 29 Jan 2024 16:20:26 GMT
ENV TOMCAT_VERSION=9.0.85
# Mon, 29 Jan 2024 16:20:26 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Mon, 29 Jan 2024 16:20:26 GMT
COPY dir:ea4ea4ebeec43f8c7e59aba9121653d67d7027fc1f6250035bf8eec59a105266 in /usr/local/tomcat 
# Mon, 29 Jan 2024 16:20:26 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Jan 2024 16:20:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 29 Jan 2024 16:20:26 GMT
EXPOSE 8080
# Mon, 29 Jan 2024 16:20:26 GMT
ENTRYPOINT []
# Mon, 29 Jan 2024 16:20:26 GMT
CMD ["catalina.sh" "run"]
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 29 Jan 2024 16:20:26 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_VERSION=16.0.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.0.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=955c175d0ac0e7039eeafd8569d87ad8a7967092ad8d018decb80a42a7eb941f
# Mon, 29 Jan 2024 16:20:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
VOLUME [/usr/local/xwiki]
# Mon, 29 Jan 2024 16:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jan 2024 16:20:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bac6b544c281c39df6cde20776732e9b89dbfbbbb49870c60c9af5ef1df471`  
		Last Modified: Fri, 16 Feb 2024 04:55:46 GMT  
		Size: 18.9 MB (18860590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244992bb9e51f456f3e5c927182054789a275d47eba65099182705a8e1952dc2`  
		Last Modified: Fri, 16 Feb 2024 04:56:12 GMT  
		Size: 46.6 MB (46639325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e543faa97f71ea4edea5a6153e1b82e4e9143354356435ca0a085c427b9b07e`  
		Last Modified: Fri, 16 Feb 2024 04:56:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b734e973751dd4636bc278f0ef5ee31fc8e10cc65a07ebd5ef57aa728870187`  
		Last Modified: Fri, 16 Feb 2024 04:56:06 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834bcd95e101783ee58afe3b6ea7c1050d27b18b749f6b70e0bcbce490b2298e`  
		Last Modified: Fri, 16 Feb 2024 07:41:13 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e9ecca7fdca869b6198fc0e1a5dd2e4aa7ff97e813214f25b0e5b7b71e2b3e`  
		Last Modified: Fri, 16 Feb 2024 07:43:55 GMT  
		Size: 12.4 MB (12412613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e27672d62713a445feae140b1fe12d2a0de35bf9a20c27839f96ea451fadb29`  
		Last Modified: Fri, 16 Feb 2024 07:43:54 GMT  
		Size: 457.1 KB (457122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11cf46d1d66d0380702e7dda5fb16077dd696befc697e707524ddfed5d083fac`  
		Last Modified: Fri, 16 Feb 2024 07:43:54 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ddf7aea74707479be79b7dc70123fb1bfdd7d25c1f2619547d48cab9bb3d0b`  
		Last Modified: Fri, 16 Feb 2024 15:25:24 GMT  
		Size: 174.3 MB (174327631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02767f82bb4d6fbb83951c650ee2f4c7a59deb3f616d8f46a35fe9ccb9644d98`  
		Last Modified: Fri, 16 Feb 2024 15:25:26 GMT  
		Size: 306.8 MB (306751680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2073b1cf8888d276bd59f7de8ed344b61fe590c5784f3fd208a8d621a91c54f`  
		Last Modified: Fri, 16 Feb 2024 15:25:19 GMT  
		Size: 936.8 KB (936848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a76acbe7306efa4a85ba9c78a278b46be26e078b054e56a200dbbfd322429`  
		Last Modified: Fri, 16 Feb 2024 15:25:19 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989d92b38c7418eeafe9ac88eaeea011b8cbe236efcd124badc64bd88f0cb3ed`  
		Last Modified: Fri, 16 Feb 2024 15:25:20 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abbaafc80288a308415fe973353cde9997042102ce9c904db8ec66ef34ca142`  
		Last Modified: Fri, 16 Feb 2024 15:25:21 GMT  
		Size: 6.4 KB (6424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee9584297f7f2d68b8b127ad1ce0e60eec3a95dfde746c76bf76629a1f632c3`  
		Last Modified: Fri, 16 Feb 2024 15:25:22 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:d94c25680c8f46c3a7f98737a569cbddb7f5b2735aca7f16d27178c88cb02b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8187933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947f10cc4fc504fbba41ae0aae3e1b69ed1d0e76df97ec1cafe9cba07baa9ac1`

```dockerfile
```

-	Layers:
	-	`sha256:21062a5f02363c29e1644cbf6abe6d5c2b8617ac6b2b29634c4d011f7ebf8ee9`  
		Last Modified: Fri, 16 Feb 2024 15:25:20 GMT  
		Size: 8.1 MB (8149288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c88dfcd36081c8cc612df2530f13dc95cd4cfccb2572bcc670dc55cbd6da480`  
		Last Modified: Fri, 16 Feb 2024 15:25:19 GMT  
		Size: 38.6 KB (38645 bytes)  
		MIME: application/vnd.in-toto+json
