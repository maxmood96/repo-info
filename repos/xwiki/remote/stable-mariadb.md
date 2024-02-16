## `xwiki:stable-mariadb`

```console
$ docker pull xwiki@sha256:dada8035ddea47700e0cb6b1c9b5df3842b0083496ae8167caf2328954052298
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:c770fcb2be454a3805fc7c42a3566892610f3fd76fdb2a64872285a182fab8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.7 MB (593664859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ed4b9a107eb3ecf045c3f62b3fb8e8b3412932cc9e02bd5b1ea0ed91656603`
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
ENV MARIADB_JDBC_VERSION=3.3.2
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MARIADB_JDBC_SHA256=2a67ef3cc1ca481965a0e7f2d4174d126f3464d02b4055a441261fad8c196769
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.2
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.2.jar
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.2.jar
# Mon, 29 Jan 2024 16:20:26 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:7570d2dc2336db9e0d8098867d6f3f9234f2d1223fccf3bdf1164b2a0dbc9d45`  
		Last Modified: Fri, 16 Feb 2024 05:51:13 GMT  
		Size: 178.3 MB (178349329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b712f6070e190957d006f375f1788cb51eef7dde73ee1cd44e6a56488281108`  
		Last Modified: Fri, 16 Feb 2024 05:51:16 GMT  
		Size: 306.8 MB (306751644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c050a0cefbe1bfb4838aed0532c838365f8ecd8712f2ce679a6a4d9eeba5a3`  
		Last Modified: Fri, 16 Feb 2024 05:51:09 GMT  
		Size: 615.1 KB (615138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f8b6425cc4bb82e40aecc49dba83e4c52bce0f8f47d624163277857913d457`  
		Last Modified: Fri, 16 Feb 2024 05:51:09 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6da7b0e9cdb013a8f1bdd5a37421999f9196a74cf84f45d03af168f65ebc12`  
		Last Modified: Fri, 16 Feb 2024 05:51:10 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd244a804d8b37749341b69729d80c36e5dcae78be3ee23d99246689218e03de`  
		Last Modified: Fri, 16 Feb 2024 05:51:11 GMT  
		Size: 6.4 KB (6423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ccd225b5fa1544400583bf6b253eaa2e4eacb8cea2be20227925c6c19f5839`  
		Last Modified: Fri, 16 Feb 2024 05:51:11 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:160a737a6d080c81bf9afdd0f56003be841aa4c72efbb947f30d01b6c6ca94f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8098209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634ea753fc3c12c0b9f9bc7442b86e4350fa5cc9645d271b401e3715e55a7446`

```dockerfile
```

-	Layers:
	-	`sha256:6e29a66ed5ceb9051b3977144d14e1903f19966917a5a99afda52e8d14c60d12`  
		Last Modified: Fri, 16 Feb 2024 05:51:09 GMT  
		Size: 8.1 MB (8056585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd1fdc8bd404ca38c552c136dd31f76c2c7fc2b03c95f430f4b2c603edc58f38`  
		Last Modified: Fri, 16 Feb 2024 05:51:09 GMT  
		Size: 41.6 KB (41624 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:1faf8fb58164024b40c6afa88b7678b692b664d2d82c20b6ead9b0756b0a04d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.5 MB (587537096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ce4697b45fdec264a4f2bfb119b89ed986f2a8825669d473e1328faca4ad20`
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
ENV MARIADB_JDBC_VERSION=3.3.2
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MARIADB_JDBC_SHA256=2a67ef3cc1ca481965a0e7f2d4174d126f3464d02b4055a441261fad8c196769
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.2
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.2.jar
# Mon, 29 Jan 2024 16:20:26 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.2.jar
# Mon, 29 Jan 2024 16:20:26 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:a2a544ade5159c7a3e2d43ec44aea35a6519d89ca31d435879ad234365bb6786`  
		Last Modified: Fri, 16 Feb 2024 15:23:22 GMT  
		Size: 173.4 MB (173386663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5897e3a3d4b93301d123c02a990abee73656cde5b02097ae0a89e49a46a4e795`  
		Last Modified: Fri, 16 Feb 2024 15:23:25 GMT  
		Size: 306.8 MB (306751610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f36bbf1b7ad0840b4db457b5168dbf36863fa23eb77f7d4662015c1dab8f55d`  
		Last Modified: Fri, 16 Feb 2024 15:26:49 GMT  
		Size: 615.1 KB (615139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23f0e79c509b50edd47488fe7690ca9287338a79b514a81c4d9ed892878b575`  
		Last Modified: Fri, 16 Feb 2024 15:26:49 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fbabae3fc03749eee94ae2d24dc637a3a1e51df6d35fa4e8aa0958d66d789b`  
		Last Modified: Fri, 16 Feb 2024 15:26:49 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822e70d58e33e0df2b7ac3adecaecd777c8481e9dff6949b527bbbf4c86bc67f`  
		Last Modified: Fri, 16 Feb 2024 15:26:49 GMT  
		Size: 6.4 KB (6425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd1a6cfb625b34cf89e5502d2da0ebac4154926bf591f6c2c39885b0504f367`  
		Last Modified: Fri, 16 Feb 2024 15:26:50 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:57d34d506e3e1f92e8cb84c6c4159b967fe46e1143b47f5c4327b9fb73a17525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8180783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6944da35cb4818ab6c373d5ef1cfe1a8e3aab968524e389bca324df942eeae3`

```dockerfile
```

-	Layers:
	-	`sha256:fe141f1c8d76a78f5dbadd22c67def2436b8068889a151329bf2dcb983c53fe2`  
		Last Modified: Fri, 16 Feb 2024 15:26:49 GMT  
		Size: 8.1 MB (8140611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0536ce62eae4b84e7806021932062710b0f7d1fc4a104798748c6fa2eb41cba4`  
		Last Modified: Fri, 16 Feb 2024 15:26:48 GMT  
		Size: 40.2 KB (40172 bytes)  
		MIME: application/vnd.in-toto+json
