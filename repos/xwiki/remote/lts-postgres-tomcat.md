## `xwiki:lts-postgres-tomcat`

```console
$ docker pull xwiki@sha256:98f589fe5aadea23b0184373ccece0136726c6ec0d6973cfab52f0c1d5496092
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:cd93d4930da31266e2b3388780e338f771c6fab1498438df9b15620a4ff36f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.2 MB (595165708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02df1d2174c5853f0fd9075352afee1f1b3838a934070907d9102a952f2bdd64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 09 Feb 2024 16:20:44 GMT
ARG RELEASE
# Fri, 09 Feb 2024 16:20:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Feb 2024 16:20:44 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Fri, 09 Feb 2024 16:20:44 GMT
CMD ["/bin/bash"]
# Fri, 09 Feb 2024 16:20:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Feb 2024 16:20:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 16:20:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 09 Feb 2024 16:20:44 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 09 Feb 2024 16:20:44 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 09 Feb 2024 16:20:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 09 Feb 2024 16:20:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 09 Feb 2024 16:20:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 16:20:44 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 09 Feb 2024 16:20:44 GMT
WORKDIR /usr/local/tomcat
# Fri, 09 Feb 2024 16:20:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 09 Feb 2024 16:20:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 09 Feb 2024 16:20:44 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 09 Feb 2024 16:20:44 GMT
ENV TOMCAT_MAJOR=9
# Fri, 09 Feb 2024 16:20:44 GMT
ENV TOMCAT_VERSION=9.0.86
# Fri, 09 Feb 2024 16:20:44 GMT
ENV TOMCAT_SHA512=e8a8000dbeba5ee266ec4bf77217574364ffd114c8b913816f2e7a5e4eab4d01d0be3f05c8fccefcb5c5d770308efe1983be80279b6ef6d122d6183288a8ee9c
# Fri, 09 Feb 2024 16:20:44 GMT
COPY dir:1817f6b73a6fe4d923d7f6cf1aa21c95626eef42af1889e1d0a51c69d1ecc970 in /usr/local/tomcat 
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 09 Feb 2024 16:20:44 GMT
EXPOSE 8080
# Fri, 09 Feb 2024 16:20:44 GMT
ENTRYPOINT []
# Fri, 09 Feb 2024 16:20:44 GMT
CMD ["catalina.sh" "run"]
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 09 Feb 2024 16:20:44 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
ENV XWIKI_VERSION=15.10.6
# Fri, 09 Feb 2024 16:20:44 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.6
# Fri, 09 Feb 2024 16:20:44 GMT
ENV XWIKI_DOWNLOAD_SHA256=1491cbfd91d8fe7362c65d01ade6ce36ce7a8adfa4b99e4f339783771d8ab675
# Fri, 09 Feb 2024 16:20:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
VOLUME [/usr/local/xwiki]
# Fri, 09 Feb 2024 16:20:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Feb 2024 16:20:44 GMT
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
	-	`sha256:a7ab6d68c40e376522279694dbf18c22a485bc7b3f1be642aeee6f2acd90c748`  
		Last Modified: Wed, 21 Feb 2024 02:50:35 GMT  
		Size: 179.3 MB (179291671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d070dd7692b932b402b513e3f26a6bd970ffc829e52ebbcc9df75107d8819c4`  
		Last Modified: Wed, 21 Feb 2024 02:50:37 GMT  
		Size: 307.0 MB (306981162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f746e9c3da8ead9ab95d563c392f746c5bc55a7aafa1d9e77b12eece34a81931`  
		Last Modified: Wed, 21 Feb 2024 02:50:32 GMT  
		Size: 936.9 KB (936852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095e622ae3d686f71cd06007d8f46f456e3ab6c5cb22e3e5bc5bcb08700414a3`  
		Last Modified: Wed, 21 Feb 2024 02:50:32 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b14400635530a952a5a15a6af61942230a19458ac13f3d29137ee53a34aee7`  
		Last Modified: Wed, 21 Feb 2024 02:50:33 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee388c651f78fe3db1f3407f461ea40cdd3016536689234b20583f47bb28714`  
		Last Modified: Wed, 21 Feb 2024 02:50:33 GMT  
		Size: 6.4 KB (6416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8f48d660fad4fe9262ed14671166c98a8c95871e4a2aff82ed39bb485b2d17`  
		Last Modified: Wed, 21 Feb 2024 02:50:34 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:3518468cc0113875b6496041fcfca3b4b44699ac1e0cd9b41b2ba7257f4ac060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9106107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7123c190eb09aaa1c159328073c79a728d4f7a8ce69fab2c29a64f7dba82a229`

```dockerfile
```

-	Layers:
	-	`sha256:98246a8162c287464b4f5fb7a2d54fbcca3eb972d2b8739ed2e072d45744a2e3`  
		Last Modified: Wed, 21 Feb 2024 02:50:32 GMT  
		Size: 9.1 MB (9066327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92fc48ae23fa6a512a1be7adb88a8636d200b2491e11758b01ae74835c34403e`  
		Last Modified: Wed, 21 Feb 2024 02:50:32 GMT  
		Size: 39.8 KB (39780 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:3e4eff15a7d92fd570b737cc88e23d9540f770976bd51a424640efb7034080ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.0 MB (589036042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f113bbdb0e25012dc7053418fde30a6d28604b34f08571f280317fd43df3f5ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 09 Feb 2024 16:20:44 GMT
ARG RELEASE
# Fri, 09 Feb 2024 16:20:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Feb 2024 16:20:44 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Fri, 09 Feb 2024 16:20:44 GMT
CMD ["/bin/bash"]
# Fri, 09 Feb 2024 16:20:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Feb 2024 16:20:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 16:20:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Fri, 09 Feb 2024 16:20:44 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Fri, 09 Feb 2024 16:20:44 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 09 Feb 2024 16:20:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 09 Feb 2024 16:20:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 09 Feb 2024 16:20:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 16:20:44 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 09 Feb 2024 16:20:44 GMT
WORKDIR /usr/local/tomcat
# Fri, 09 Feb 2024 16:20:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 09 Feb 2024 16:20:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 09 Feb 2024 16:20:44 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 09 Feb 2024 16:20:44 GMT
ENV TOMCAT_MAJOR=9
# Fri, 09 Feb 2024 16:20:44 GMT
ENV TOMCAT_VERSION=9.0.86
# Fri, 09 Feb 2024 16:20:44 GMT
ENV TOMCAT_SHA512=e8a8000dbeba5ee266ec4bf77217574364ffd114c8b913816f2e7a5e4eab4d01d0be3f05c8fccefcb5c5d770308efe1983be80279b6ef6d122d6183288a8ee9c
# Fri, 09 Feb 2024 16:20:44 GMT
COPY dir:52aed3e3fb48dd428e971cb85f8f92f0846f944a70308bc72289f696b56b8f42 in /usr/local/tomcat 
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Feb 2024 16:20:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 09 Feb 2024 16:20:44 GMT
EXPOSE 8080
# Fri, 09 Feb 2024 16:20:44 GMT
ENTRYPOINT []
# Fri, 09 Feb 2024 16:20:44 GMT
CMD ["catalina.sh" "run"]
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 09 Feb 2024 16:20:44 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 09 Feb 2024 16:20:44 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
ENV XWIKI_VERSION=15.10.6
# Fri, 09 Feb 2024 16:20:44 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.6
# Fri, 09 Feb 2024 16:20:44 GMT
ENV XWIKI_DOWNLOAD_SHA256=1491cbfd91d8fe7362c65d01ade6ce36ce7a8adfa4b99e4f339783771d8ab675
# Fri, 09 Feb 2024 16:20:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
VOLUME [/usr/local/xwiki]
# Fri, 09 Feb 2024 16:20:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Feb 2024 16:20:44 GMT
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
	-	`sha256:f08260b115c6a7540dd9078e15a0b3abe0c1e3d241dd8efd8ff6fe43840322f9`  
		Last Modified: Wed, 21 Feb 2024 02:43:35 GMT  
		Size: 12.4 MB (12418084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df99f020bb771bfb916b40a084c375b7b9d6aba87791b0679dd27408096b7e7`  
		Last Modified: Wed, 21 Feb 2024 02:43:34 GMT  
		Size: 457.1 KB (457128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41fe064b4c9bb6147a50153ae6ce913ccec8ecefc141098f8cfa404dccfe968`  
		Last Modified: Wed, 21 Feb 2024 02:43:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c63a4686a5664c9a5a2c2c1a06673cf94284157a820e80626bd51b4a29d437`  
		Last Modified: Wed, 21 Feb 2024 05:57:00 GMT  
		Size: 174.3 MB (174328737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a37319e81755d9bab533de639c58ed5998716dacabe090cd5f77c682ea7c12`  
		Last Modified: Wed, 21 Feb 2024 06:00:50 GMT  
		Size: 307.0 MB (306981170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c36baf45fa7ceb71bc390bf3e44c5f715f07d1f05132283ed554f4986bab530`  
		Last Modified: Wed, 21 Feb 2024 06:00:44 GMT  
		Size: 936.9 KB (936850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2c31bfc1db1a080197b61e23ed5e668627e73e1a5c9fc72228039328fe1714`  
		Last Modified: Wed, 21 Feb 2024 06:00:44 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3804c6e8a4263ba38af9b24fe9c15ebd183a969486d74f099c3a65e74f74d7`  
		Last Modified: Wed, 21 Feb 2024 06:00:44 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50f7293b1f1769f5dd84b2838c7cfe3b9cb15639508d754fbd0d7b7dc0f19a6`  
		Last Modified: Wed, 21 Feb 2024 06:00:45 GMT  
		Size: 6.4 KB (6417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3b6df8e56c4cd4c23d6e9822981b9f4ededb2eeecd6c3d312033f1dab7e5cf`  
		Last Modified: Wed, 21 Feb 2024 06:00:45 GMT  
		Size: 2.4 KB (2429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:be0baedb3c1b56eb260d603bdd072720aebc37e43f1fe4aede650421f1aca762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9201080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d35cac7641a2ce9fb8c2cb16e6f8922eb9318542cf8443cf98f1829fbae9d4`

```dockerfile
```

-	Layers:
	-	`sha256:33186ed8cf86c84c3215382cc63620f0a0528ce99a00fe49c90a8531237686d7`  
		Last Modified: Wed, 21 Feb 2024 06:00:44 GMT  
		Size: 9.2 MB (9162753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e226373505f9f1e898363b33858a1dcedc5b2749e49b4560085bea36afe2587`  
		Last Modified: Wed, 21 Feb 2024 06:00:43 GMT  
		Size: 38.3 KB (38327 bytes)  
		MIME: application/vnd.in-toto+json
