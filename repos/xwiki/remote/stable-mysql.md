## `xwiki:stable-mysql`

```console
$ docker pull xwiki@sha256:d30ace3b401c387a9915fd44b5949d2ff5fd78e578a0bbb1538c6e17b0402021
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:c060f855a7f79866a714e1d88611c445086873d2ecc03c93ea1b79f6a63c667d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.4 MB (595400852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54e9042d5b43e42641f8e9f678ec31c6a6217838a2e383ddb7d8ca170c54074`
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
ENV TOMCAT_VERSION=9.0.85
# Mon, 29 Jan 2024 16:20:26 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Mon, 29 Jan 2024 16:20:26 GMT
COPY dir:94cee7dcaaa773ae17516dae4a134e512f2456915402e9096b3ca75cc8eb4773 in /usr/local/tomcat 
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
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_VERSION=16.0.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.0.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=955c175d0ac0e7039eeafd8569d87ad8a7967092ad8d018decb80a42a7eb941f
# Mon, 29 Jan 2024 16:20:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MYSQL_JDBC_VERSION=8.2.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MYSQL_JDBC_SHA256=06f14fbd664d0e382347489e66495ca27ab7e6c2e1d9969a496931736197465f
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.2.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.2.0.jar
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.2.0.jar
# Mon, 29 Jan 2024 16:20:26 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:4555d0dea7b595dd4bb0d4e1722859b72882e0916a712c063bc881110f163e3e`  
		Last Modified: Fri, 16 Feb 2024 05:50:53 GMT  
		Size: 178.3 MB (178349361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0550051e358306dddc6c2351505c50a8ab47a0adfa3f69c332aaf6d3e4f5d5`  
		Last Modified: Fri, 16 Feb 2024 05:50:56 GMT  
		Size: 306.8 MB (306751682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecefe66ad27cf11470125d69409a38017a30abb7ae7ea4e7fee682b3aff5d4a6`  
		Last Modified: Fri, 16 Feb 2024 05:50:51 GMT  
		Size: 2.4 MB (2350958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c045e7fd4348d4ba370cb2bb7bc21dcc8cd8736094ae151aa1731dfc562c8ef`  
		Last Modified: Fri, 16 Feb 2024 05:50:50 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f826503e9b1fb3e547866c0ef257e1386dd937085463bf71c08950e02b89fed`  
		Last Modified: Fri, 16 Feb 2024 05:50:52 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145f0c5373a650c1b3b216167d53bdc5c8c97f08d8aaec3699fea54a1d63b0b3`  
		Last Modified: Fri, 16 Feb 2024 05:50:52 GMT  
		Size: 6.4 KB (6423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b54d7ea40dea794fbd48a23ebf78b767108f4148c23da8add12f88d36c0548`  
		Last Modified: Fri, 16 Feb 2024 05:50:53 GMT  
		Size: 2.5 KB (2480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mysql` - unknown; unknown

```console
$ docker pull xwiki@sha256:d457f426c5e35b68c7a83b478e7cd6ef30bb06e9ba8c6a9ac5e4f280684bce1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8101042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04aff2c341cc7b5517a385feab61837c3eac0fab4d1e763cd0910d7540f16bf`

```dockerfile
```

-	Layers:
	-	`sha256:be6eaca61ca4967e876070f3852b05c956c068775653eb234657e343df1e1589`  
		Last Modified: Fri, 16 Feb 2024 05:50:51 GMT  
		Size: 8.1 MB (8058043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c776205e2b7a7891e430f2f030c5fbf97563780e2206ea36f7632611f07e797`  
		Last Modified: Fri, 16 Feb 2024 05:50:50 GMT  
		Size: 43.0 KB (42999 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-mysql` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:a988f1d9c678d6bd20244e3666a3e071a50306ec9cbff2c95fee265e02e61915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.3 MB (589272912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f5b4818e9700914db76c290a36b075c9e28d42cf1dcb9bc77756c4364f92e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
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
COPY dir:101a21f8290e4b799c9f99499662dfc86926aa66787150c02f8bb6cc272d7fbd in /usr/local/tomcat 
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
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_VERSION=16.0.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.0.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=955c175d0ac0e7039eeafd8569d87ad8a7967092ad8d018decb80a42a7eb941f
# Mon, 29 Jan 2024 16:20:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MYSQL_JDBC_VERSION=8.2.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MYSQL_JDBC_SHA256=06f14fbd664d0e382347489e66495ca27ab7e6c2e1d9969a496931736197465f
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.2.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.2.0.jar
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.2.0.jar
# Mon, 29 Jan 2024 16:20:26 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d031894e4c0411af099ca88f2f4707adffb7144d8d3dc5d40457cededf240b5`  
		Last Modified: Fri, 02 Feb 2024 02:16:39 GMT  
		Size: 18.9 MB (18860666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0007a9ef9bab7b317a14a0d8594647e9c47755fcb79f9fa388e560fab31690`  
		Last Modified: Fri, 02 Feb 2024 02:17:22 GMT  
		Size: 46.6 MB (46639311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917c6cc534cfc01e73da456384906c210ffa86f1df265b8ee7255561e2a7c5fa`  
		Last Modified: Fri, 02 Feb 2024 02:17:17 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7a0f038262842ffcfdab428e9f3a7a1d0dc2e49da53bdde76335cbc0c02b48`  
		Last Modified: Fri, 02 Feb 2024 02:17:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a15ffd3ea890ff20384b9803dee407357a8063bb1239abcfde036e1a2a22e17`  
		Last Modified: Fri, 02 Feb 2024 04:11:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fe4808aaf16dbfd9e06055aba830d84eeb10946e56fb1429c81250ccce8836`  
		Last Modified: Fri, 02 Feb 2024 04:14:44 GMT  
		Size: 12.4 MB (12412651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222ea8a7cf368a3f03e7389c6a6b4e2bcfe1618378bd14046880ee212f0336f7`  
		Last Modified: Fri, 02 Feb 2024 04:14:43 GMT  
		Size: 457.1 KB (457148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c004c0bb331fe8e89ab0554e93da2d81f4f5482a473b6c68864b87330da9ab`  
		Last Modified: Fri, 02 Feb 2024 04:14:43 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13506acde03095dd098999f7ae244afce46a3267d8ffc50f8ffa00a9db5e332`  
		Last Modified: Sat, 03 Feb 2024 11:31:21 GMT  
		Size: 173.4 MB (173386548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ba72dc025c2b4160b65f3c08215d9cafdcfd9203cd9047faa0746168c21a79`  
		Last Modified: Sat, 03 Feb 2024 11:31:24 GMT  
		Size: 306.8 MB (306751712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8327761cd03454dbf3b533c16078d839de57f0dd643ebd2d02034cb8102fcd5f`  
		Last Modified: Sat, 03 Feb 2024 11:31:17 GMT  
		Size: 2.4 MB (2350959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff53991b4cf5c8353c4742428065977490415c7a0a78ed1ca432779e1decf00`  
		Last Modified: Sat, 03 Feb 2024 11:31:18 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127fdf562a6e0bf2d5df8b4f1a604c26bca70e3b76efe75ac69f6f5f823ef7b3`  
		Last Modified: Sat, 03 Feb 2024 11:31:18 GMT  
		Size: 2.4 KB (2373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619777786f7880cb68f6ec741f79f1180ddfb8a34487a2f6002d303ab0981833`  
		Last Modified: Sat, 03 Feb 2024 11:31:19 GMT  
		Size: 6.4 KB (6426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cca0c9dec516be3bc59bf262d87752c46de942674d3af29461ea8f63cdabdfd`  
		Last Modified: Sat, 03 Feb 2024 11:31:19 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mysql` - unknown; unknown

```console
$ docker pull xwiki@sha256:f32e7634d148e6c6591ab22732cf510365405f7d9f60c99d81efffb63867fc9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8185098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2df06307fbc609ce9f564a4c515cf21c6c6ba7e953e0d60a7dd62c52a252f1`

```dockerfile
```

-	Layers:
	-	`sha256:ef7cb2fb1aa5393a49ad3d941f1963ac844fe02ffb3b92c5685f08ce30d63a86`  
		Last Modified: Sat, 03 Feb 2024 11:31:16 GMT  
		Size: 8.1 MB (8142075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf32ccf94313ff2c64aaa01235176261ad51f552e1ad898fef569e0f48ed7ef3`  
		Last Modified: Sat, 03 Feb 2024 11:31:16 GMT  
		Size: 43.0 KB (43023 bytes)  
		MIME: application/vnd.in-toto+json
