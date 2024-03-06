## `xwiki:15-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:acfea76c56369c956138eefad345a04c1d850c9b38350245a6d3725f871ab586
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:15-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:185873747363f66855dfb05d651bc1947e86d30bca13dce9334766e78e3acdab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.9 MB (593900755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ed3bbe3b145e20bd8010e0825743e358a011db26c6e56d174cd27e7c7ffc87`
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
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
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
COPY dir:a1b18cd4173fc89867b3684c0bcb6ed5fd2f800394449b55a0ac4e5f96c33c28 in /usr/local/tomcat 
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
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
ENV XWIKI_VERSION=15.10.6
# Fri, 09 Feb 2024 16:20:44 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.6
# Fri, 09 Feb 2024 16:20:44 GMT
ENV XWIKI_DOWNLOAD_SHA256=1491cbfd91d8fe7362c65d01ade6ce36ce7a8adfa4b99e4f339783771d8ab675
# Fri, 09 Feb 2024 16:20:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MARIADB_JDBC_VERSION=3.3.2
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MARIADB_JDBC_SHA256=2a67ef3cc1ca481965a0e7f2d4174d126f3464d02b4055a441261fad8c196769
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.2
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.2.jar
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.2.jar
# Fri, 09 Feb 2024 16:20:44 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2670537dcebc0b445ca47e68b31667f3572b8758b8388e24d8a6770e860ecc8`  
		Last Modified: Wed, 06 Mar 2024 06:09:59 GMT  
		Size: 17.5 MB (17456336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c059ccfa41820fb3f1472c4358304407b00e3eed15933f067b1d4957a40bfc3`  
		Last Modified: Wed, 06 Mar 2024 06:10:45 GMT  
		Size: 47.2 MB (47163248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23d33d59f2ab52fa44e6fbd4e629813614bb753bb3ccac98940e981a3b13c4e`  
		Last Modified: Wed, 06 Mar 2024 06:10:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a648f54390edf0b921f43c547b5d6d6b937e58728be46796f6aefcd4735fb`  
		Last Modified: Wed, 06 Mar 2024 06:10:39 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abdfee857c0074fe5c75f39fbbf37551ccbc0d9509a3a5fea060b4beafa4ec7`  
		Last Modified: Wed, 06 Mar 2024 15:02:53 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5f7b6e8ca72c71914be68652c1d9d21fe4d11d3258c55cbfbd7f43e6427a55`  
		Last Modified: Wed, 06 Mar 2024 15:06:00 GMT  
		Size: 12.4 MB (12411761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73969ab971ee89d66abcc9270b522fac62871788fcc65712f84c2ef0c7962f0`  
		Last Modified: Wed, 06 Mar 2024 15:05:59 GMT  
		Size: 458.6 KB (458590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1831643cd49257da268e364edf6c6b53b8fe8ced3e3095325777f16866823d8`  
		Last Modified: Wed, 06 Mar 2024 15:05:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa96e81e53df8548cfce23e676de856af0b7889b23375ca506b999724e0f1ea4`  
		Last Modified: Wed, 06 Mar 2024 15:50:18 GMT  
		Size: 178.3 MB (178349513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e078da10b94e1996bd8b463391d237acc9be6c52fdc8969171203122bfe1320b`  
		Last Modified: Wed, 06 Mar 2024 15:50:20 GMT  
		Size: 307.0 MB (306981149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095b782fc3eca9267dfb149561926c74f655d418e5016d2760f986b152f96404`  
		Last Modified: Wed, 06 Mar 2024 15:50:16 GMT  
		Size: 615.1 KB (615145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fd56dffec1245eeba381742c3a31c8799ba5cb8e4ed09b8b070f8e7ee4e6c9`  
		Last Modified: Wed, 06 Mar 2024 15:50:16 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5db0928ce0d4270eeed87d6474c7c2c3220f487b8a5359e721912d3cf77159`  
		Last Modified: Wed, 06 Mar 2024 15:50:16 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017f8f8c797166729cce4892ceb025529b3496e9475c53204d2206ef35022599`  
		Last Modified: Wed, 06 Mar 2024 15:50:17 GMT  
		Size: 6.4 KB (6422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d121db669c8e98a62a4194cee0a67a1dea0ecc18e29df987400037e8ec1029`  
		Last Modified: Wed, 06 Mar 2024 15:50:17 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:0a1d1481dfbd2a415b48e2bae6776b29fec7f096980a87813d68d0c51380a66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9098326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5468c88bbc9f1a7fee637f3b28cadbb60bc3bb25b6116d8001f188868230b41d`

```dockerfile
```

-	Layers:
	-	`sha256:18d1ed796883ac2e0986bbed7a486599641c5339ad781039ae1011f2d9a99afd`  
		Last Modified: Wed, 06 Mar 2024 15:50:16 GMT  
		Size: 9.1 MB (9057016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:461190dab29f87bce5907e8025f5eefe2ec45493e432d7de6d68283e97868844`  
		Last Modified: Wed, 06 Mar 2024 15:50:16 GMT  
		Size: 41.3 KB (41310 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:15-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:0a2911c68170f774725ae8b35c0d6e53b3e2a08c93608d6095e9ad4ec8391a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.8 MB (587771984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:570074b09ef698f5f3830081aebde6301a4b3becf259b29b69d4aafb5aca4896`
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
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
ENV XWIKI_VERSION=15.10.6
# Fri, 09 Feb 2024 16:20:44 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.6
# Fri, 09 Feb 2024 16:20:44 GMT
ENV XWIKI_DOWNLOAD_SHA256=1491cbfd91d8fe7362c65d01ade6ce36ce7a8adfa4b99e4f339783771d8ab675
# Fri, 09 Feb 2024 16:20:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MARIADB_JDBC_VERSION=3.3.2
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MARIADB_JDBC_SHA256=2a67ef3cc1ca481965a0e7f2d4174d126f3464d02b4055a441261fad8c196769
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.2
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.2.jar
# Fri, 09 Feb 2024 16:20:44 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.2.jar
# Fri, 09 Feb 2024 16:20:44 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:75f942220408c5601f78916ffb6c0b523503ae28b04b2f8ffa2416021fb769ec`  
		Last Modified: Wed, 21 Feb 2024 05:54:58 GMT  
		Size: 173.4 MB (173386551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3bba94a1776c21cc8d3e5df0f4e9e11430dc99b9eec437284a8fca9a3fd0ee`  
		Last Modified: Wed, 21 Feb 2024 05:59:14 GMT  
		Size: 307.0 MB (306981145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e5f8679877c677d623fef9a9a95aee5d4efb9c68477a6664a78fde76d8105d`  
		Last Modified: Wed, 21 Feb 2024 06:01:27 GMT  
		Size: 615.1 KB (615138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065a99a1e12be21de6ddfe77cb99007f339b54eebb960452ca60140f7951eb96`  
		Last Modified: Wed, 21 Feb 2024 06:01:27 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4a7309f324ed351d275db50388b12e05c80f59ceb8c0a48e91a0d2d4de6b8f`  
		Last Modified: Wed, 21 Feb 2024 06:01:27 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7901cd75e08f232ddd8cd175ab7dbc2a32ab53f9506ea9e65f77ab52ae5b9ad`  
		Last Modified: Wed, 21 Feb 2024 06:01:27 GMT  
		Size: 6.4 KB (6415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea121388c4bc01b7ba09db49f64cd63b6631a1ccef3b8652f2aa90d133912ae`  
		Last Modified: Wed, 21 Feb 2024 06:01:28 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:e2aa76dabeb49944167a0a8a763c4bbcf6ba5417cd6b8fde070f0934d9f0b11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9193299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfe720eee3aac5384d59dc37a741763411361145526fc74cf079c85577ddf01`

```dockerfile
```

-	Layers:
	-	`sha256:930e7102b94626faaa84537d154c60e6ba3266aea6c4a2165092cbb9f0ab90e8`  
		Last Modified: Wed, 21 Feb 2024 06:01:27 GMT  
		Size: 9.2 MB (9153442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1731243a790f6cadf6773acdd23c8af10b4d2fdb5cb491d14c515e017e7a70e8`  
		Last Modified: Wed, 21 Feb 2024 06:01:26 GMT  
		Size: 39.9 KB (39857 bytes)  
		MIME: application/vnd.in-toto+json
