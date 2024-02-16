## `xwiki:15-postgres-tomcat`

```console
$ docker pull xwiki@sha256:0ac0be5bdbca38da82e76ecb035f27b7fd031c7bcb855203719e61d94bd76e1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:15-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:4e4a3e410bc7ac236e42a82fce61f6ce0cbcfdb2127256469c51bb20ff36e5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.2 MB (595158719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd78149eb215e6e208e778991e0d44ed84aaf45bcc616bf2597f50fa96bdba0f`
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
ENV TOMCAT_VERSION=9.0.85
# Fri, 09 Feb 2024 16:20:44 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Fri, 09 Feb 2024 16:20:44 GMT
COPY dir:94cee7dcaaa773ae17516dae4a134e512f2456915402e9096b3ca75cc8eb4773 in /usr/local/tomcat 
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
	-	`sha256:1d215d74c3520fb2b77de895508f50445846f3674eeb1f4cfa79753f2fc40b38`  
		Last Modified: Fri, 16 Feb 2024 05:05:07 GMT  
		Size: 12.4 MB (12404652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9957b08ee0ea8b5d9cb12f4d51f0984c2ba5b746f4229ea31272e8151af788`  
		Last Modified: Fri, 16 Feb 2024 05:05:06 GMT  
		Size: 458.6 KB (458580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9e5b1ff9bbf71d294f435ba64396478565ad9aba1cc3fbbc62f6e8ace82066`  
		Last Modified: Fri, 16 Feb 2024 05:05:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5920aad692757436d82712cd9c26926304ef15d2ef1c98e6d16b0132fca2280a`  
		Last Modified: Fri, 16 Feb 2024 05:50:50 GMT  
		Size: 179.3 MB (179291765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7b8f815d5f33eec8f9099f9a43c6b08003aa3ec401278fd5ceff78a5933194`  
		Last Modified: Fri, 16 Feb 2024 05:50:54 GMT  
		Size: 307.0 MB (306981214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac1eb8cd834c15317d39f57b6d91d4c3acdc286bd7470432460e343c1ccde70`  
		Last Modified: Fri, 16 Feb 2024 05:50:48 GMT  
		Size: 936.9 KB (936851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab7bb9576cb07698da4c81c674faf2dc6db3bc5d10b55c27d0919dee47a0ccd`  
		Last Modified: Fri, 16 Feb 2024 05:50:48 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ab2f6926521be640cb334f85fbfbf3b07ec231f0a0c21a974a8d4ae5115cf6`  
		Last Modified: Fri, 16 Feb 2024 05:50:49 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22115f3037dcda82be4c58f838b9a9cbda7598eabefb01b7e858b6c39e0ba6e2`  
		Last Modified: Fri, 16 Feb 2024 05:50:49 GMT  
		Size: 6.4 KB (6416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69efa8195c89d4df3adef9689ee48455cf2a3a98a21dafa140692e18f02a5c10`  
		Last Modified: Fri, 16 Feb 2024 05:50:50 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:cfbbbd171965330f9f085a7ce6f3126c2089a8922530d9f1b6c7e9c83af1da3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8107799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847654bf4c4e1989414ee49d2e142c127cccb77774018d46d17b558d6f22d530`

```dockerfile
```

-	Layers:
	-	`sha256:d6b4c82c054f2dcff20193d236db17e0cd1e128a142b8b4c34dbcd5b1c858d03`  
		Last Modified: Fri, 16 Feb 2024 05:50:47 GMT  
		Size: 8.1 MB (8068019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58901889bee832c912876af920a017ad874b62b2e5d02e4dcedd5c6c0159c68c`  
		Last Modified: Fri, 16 Feb 2024 05:50:47 GMT  
		Size: 39.8 KB (39780 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:15-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:22a11965cc6f12f2c820b563c442ca8dcba88a7639a7f3196169a2330f90143e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.0 MB (589029451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4511cce79d03685c95e11e05ddfb29b13f69c2dbf0fbae5d6adcf9a54e5d6ced`
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
ENV TOMCAT_VERSION=9.0.85
# Fri, 09 Feb 2024 16:20:44 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Fri, 09 Feb 2024 16:20:44 GMT
COPY dir:ea4ea4ebeec43f8c7e59aba9121653d67d7027fc1f6250035bf8eec59a105266 in /usr/local/tomcat 
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
	-	`sha256:e63ea14d1e9476617d5727994a9ac2d4142d459ebb517184af78c08132c1b8f7`  
		Last Modified: Fri, 16 Feb 2024 15:29:55 GMT  
		Size: 307.0 MB (306981163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bbc1ab936ebdb1e197c69a4873494a3ddc66fe6f0a06cf057e65b6abef9cc3`  
		Last Modified: Fri, 16 Feb 2024 15:29:49 GMT  
		Size: 936.9 KB (936851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0cdafcafcb446dfd11dbc59c53c767fd0ef89d365717d06e53d325f2e18721`  
		Last Modified: Fri, 16 Feb 2024 15:29:48 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af45ddfeb7cea4488852934369b05c2bd9668e1b0b66498f50f96a0b28b8fc3`  
		Last Modified: Fri, 16 Feb 2024 15:29:49 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120ac1a9ab334c00fabf5224b4800d24e2b922b8f98a808b2f979471189bd16d`  
		Last Modified: Fri, 16 Feb 2024 15:29:50 GMT  
		Size: 6.4 KB (6418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e99ea77ac6eec7a681ad1e6a5a69fd96e84e2dcebb26317ef87a34f066af3c`  
		Last Modified: Fri, 16 Feb 2024 15:29:50 GMT  
		Size: 2.4 KB (2426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:2a7b1e55208c9586685f1344dafc7d752d8ace86cfda2a4f974d8323016cf4e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8190370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1f78a7862bffd9f9bf8de31c42c9d0ea57aabcf8312f202f878a0a83310d12`

```dockerfile
```

-	Layers:
	-	`sha256:c9ee391e99ffb0d02b202171f38cbadec509d1d135f6b50948d7f0e2d086e491`  
		Last Modified: Fri, 16 Feb 2024 15:29:48 GMT  
		Size: 8.2 MB (8152043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dcb175c5c220b4bb8e69783d1b4c7513a91335858d8a5a6b43982d4389fbf51`  
		Last Modified: Fri, 16 Feb 2024 15:29:48 GMT  
		Size: 38.3 KB (38327 bytes)  
		MIME: application/vnd.in-toto+json
