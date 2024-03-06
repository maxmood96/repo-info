## `xwiki:postgres-tomcat`

```console
$ docker pull xwiki@sha256:eecc308fe152f84c7146273e78a702c07bc4aac1e8b629b940b831f39902bccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:db95330bd7a65dc90707f4d05769183b1fd52dd6d37615175ef5ccca05b3c4fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.1 MB (595066536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103321c39b20ad5e05374792974ea7dfe4de15fa007c90017021d870b214903d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Feb 2024 13:14:55 GMT
ARG RELEASE
# Mon, 26 Feb 2024 13:14:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 26 Feb 2024 13:14:55 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Mon, 26 Feb 2024 13:14:55 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 13:14:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 26 Feb 2024 13:14:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Feb 2024 13:14:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 26 Feb 2024 13:14:55 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 26 Feb 2024 13:14:55 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 26 Feb 2024 13:14:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 26 Feb 2024 13:14:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 26 Feb 2024 13:14:55 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Feb 2024 13:14:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 26 Feb 2024 13:14:55 GMT
WORKDIR /usr/local/tomcat
# Mon, 26 Feb 2024 13:14:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 26 Feb 2024 13:14:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 26 Feb 2024 13:14:55 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 26 Feb 2024 13:14:55 GMT
ENV TOMCAT_MAJOR=9
# Mon, 26 Feb 2024 13:14:55 GMT
ENV TOMCAT_VERSION=9.0.86
# Mon, 26 Feb 2024 13:14:55 GMT
ENV TOMCAT_SHA512=e8a8000dbeba5ee266ec4bf77217574364ffd114c8b913816f2e7a5e4eab4d01d0be3f05c8fccefcb5c5d770308efe1983be80279b6ef6d122d6183288a8ee9c
# Mon, 26 Feb 2024 13:14:55 GMT
COPY dir:a1b18cd4173fc89867b3684c0bcb6ed5fd2f800394449b55a0ac4e5f96c33c28 in /usr/local/tomcat 
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 26 Feb 2024 13:14:55 GMT
EXPOSE 8080
# Mon, 26 Feb 2024 13:14:55 GMT
ENTRYPOINT []
# Mon, 26 Feb 2024 13:14:55 GMT
CMD ["catalina.sh" "run"]
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 26 Feb 2024 13:14:55 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_VERSION=16.1.0
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.1.0
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_DOWNLOAD_SHA256=e236fc101710a0bfefed2328cc66652e265f21ab40dd30e6b7ce52300da744d5
# Mon, 26 Feb 2024 13:14:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
VOLUME [/usr/local/xwiki]
# Mon, 26 Feb 2024 13:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 13:14:55 GMT
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
	-	`sha256:ac7ad2474bc93f34aa8a57345a06ed5fff0c7588173d200f540b2cd5595d506d`  
		Last Modified: Wed, 06 Mar 2024 15:49:46 GMT  
		Size: 179.3 MB (179291657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947261b33448f90e5eb680fc19e3ce6149e3dc89a7882c2b90a5014478169bd`  
		Last Modified: Wed, 06 Mar 2024 15:49:49 GMT  
		Size: 306.9 MB (306882953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28b35c46e2c585338804c28edf375b8d6784eaea50d8463c27bd76326205275`  
		Last Modified: Wed, 06 Mar 2024 15:49:40 GMT  
		Size: 936.9 KB (936853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094506cfe6f23ac5733fabe47003a7cebcddb73e42ed9b48c4143e1169aced76`  
		Last Modified: Wed, 06 Mar 2024 15:49:40 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719c6391ebf29e551bee09171e37bd1531021a50ad46e55d0fced8834347cda0`  
		Last Modified: Wed, 06 Mar 2024 15:49:41 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5383aecbfabf0bb0468809a3f8c1ed493a7f6c554dc4d73fc933066c52755eb8`  
		Last Modified: Wed, 06 Mar 2024 15:49:41 GMT  
		Size: 6.4 KB (6409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fc26c933ea10c99d06ab8b82a6ff4310ca82a070e68556a88fe5997ec4ae7b`  
		Last Modified: Wed, 06 Mar 2024 15:49:42 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:2b62f090ef9d9c5b3ba132309ae77a7406aad60310ab2cfe2bf99af92755b7af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9104799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebbe36b4aee81388f713ae6c8a02481fa8444fca5178d92cc0e36937f29cc82`

```dockerfile
```

-	Layers:
	-	`sha256:2089decbbddc16d5ca6d0e1c7fd60a21c30ec41773448e0ea0385d59de7aee10`  
		Last Modified: Wed, 06 Mar 2024 15:49:41 GMT  
		Size: 9.1 MB (9064703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fefac1057a28e120e63291de515c4665154d61d9ecc8f80b222ff84feb4c890`  
		Last Modified: Wed, 06 Mar 2024 15:49:42 GMT  
		Size: 40.1 KB (40096 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:56999cd0cc2fca827eaa7add0130623af6dbbac17a27b81699a06a213530de97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.9 MB (588936970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb2313266f42a27d66bc4c4399d7d41b93ac83cb3982fb1f45eb7bff6a670c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 26 Feb 2024 13:14:55 GMT
ARG RELEASE
# Mon, 26 Feb 2024 13:14:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 26 Feb 2024 13:14:55 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Mon, 26 Feb 2024 13:14:55 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 13:14:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 26 Feb 2024 13:14:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Feb 2024 13:14:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 26 Feb 2024 13:14:55 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Mon, 26 Feb 2024 13:14:55 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 26 Feb 2024 13:14:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 26 Feb 2024 13:14:55 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 26 Feb 2024 13:14:55 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Feb 2024 13:14:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 26 Feb 2024 13:14:55 GMT
WORKDIR /usr/local/tomcat
# Mon, 26 Feb 2024 13:14:55 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 26 Feb 2024 13:14:55 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 26 Feb 2024 13:14:55 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 26 Feb 2024 13:14:55 GMT
ENV TOMCAT_MAJOR=9
# Mon, 26 Feb 2024 13:14:55 GMT
ENV TOMCAT_VERSION=9.0.86
# Mon, 26 Feb 2024 13:14:55 GMT
ENV TOMCAT_SHA512=e8a8000dbeba5ee266ec4bf77217574364ffd114c8b913816f2e7a5e4eab4d01d0be3f05c8fccefcb5c5d770308efe1983be80279b6ef6d122d6183288a8ee9c
# Mon, 26 Feb 2024 13:14:55 GMT
COPY dir:28b6e0807ab1afc14ce8a00cdcc0b2974f83fc2610eb66e632a1e50cf924f4d1 in /usr/local/tomcat 
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Feb 2024 13:14:55 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 26 Feb 2024 13:14:55 GMT
EXPOSE 8080
# Mon, 26 Feb 2024 13:14:55 GMT
ENTRYPOINT []
# Mon, 26 Feb 2024 13:14:55 GMT
CMD ["catalina.sh" "run"]
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 26 Feb 2024 13:14:55 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 26 Feb 2024 13:14:55 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_VERSION=16.1.0
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.1.0
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_DOWNLOAD_SHA256=e236fc101710a0bfefed2328cc66652e265f21ab40dd30e6b7ce52300da744d5
# Mon, 26 Feb 2024 13:14:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
VOLUME [/usr/local/xwiki]
# Mon, 26 Feb 2024 13:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Feb 2024 13:14:55 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799297b6f9210d0b08ff588516d8ab6fe2169cdda6b76a0b5f854b6e76aec0ce`  
		Last Modified: Wed, 06 Mar 2024 04:08:04 GMT  
		Size: 18.9 MB (18857483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0f6cd036a6aa4998c7a9c375b0e7fb43615f3d03dfcb794b88cff90027fff7`  
		Last Modified: Wed, 06 Mar 2024 04:08:44 GMT  
		Size: 46.6 MB (46639407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30140b6dcdeba2a64a4d96bfde851abee456c368a15a215e1b86e3c0484bce`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13614e023aad4adadb99824ffb722959861646971b8c272a4eaf5b1fe098077e`  
		Last Modified: Wed, 06 Mar 2024 04:08:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d0bd9f41adcd95029b57f6f8cd737a7f7d062a793bf0806caf980bca1af9c1`  
		Last Modified: Wed, 06 Mar 2024 11:41:12 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1382c29b3803a3ed8ad76b10a0f89ac97eec6ffef82efe7a74e17587507deda`  
		Last Modified: Wed, 06 Mar 2024 11:44:01 GMT  
		Size: 12.4 MB (12418173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1780b315b5019fafa9af700eac18080401d8ff7ba4e5f268fa384e0e21aeaa9`  
		Last Modified: Wed, 06 Mar 2024 11:44:01 GMT  
		Size: 457.3 KB (457337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca53784182e5039a7835057ef6cfd2ef8ebd593fa32f4b46916fe4891a02767e`  
		Last Modified: Wed, 06 Mar 2024 11:44:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97fb26bad0e186ff43a86b28a963993c742a0f372821453d5e35e82a191c5c1`  
		Last Modified: Wed, 06 Mar 2024 19:11:23 GMT  
		Size: 174.3 MB (174330201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cb13359b9dc2f2c8736051bc9f47b3fe1114c7b47c2fb67d53bdeb466870c4`  
		Last Modified: Wed, 06 Mar 2024 19:11:25 GMT  
		Size: 306.9 MB (306883040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d970316e9973065c30239db0ddd0a52edb337a5d610ead87fdd2d1b2054cd07d`  
		Last Modified: Wed, 06 Mar 2024 19:11:19 GMT  
		Size: 936.8 KB (936848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ba2819a565de2d9ad995e2291bf912028d7dc0c6c6a3369c251b7b925c8ab8`  
		Last Modified: Wed, 06 Mar 2024 19:11:18 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624c1c4b789bb640ea42e6bc41db4cdf9b7d05197ee4e8e8625b02bf7bdb67fe`  
		Last Modified: Wed, 06 Mar 2024 19:11:19 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be7f115c52875347aa8a030a6413dda940b381c04b88d738154062fbcb05057`  
		Last Modified: Wed, 06 Mar 2024 19:11:20 GMT  
		Size: 6.4 KB (6407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3262d2da89ded62bc73e0fcdf39bbff38964e8576ae22fb792649cb7a5fdaef4`  
		Last Modified: Wed, 06 Mar 2024 19:11:20 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:ad2df95803cd06f7ea1df16f47c9bd4d786280d19d3cf5ab43a31c51badfa3fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9199776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975671e8459e86a0387ea44b264525d01798f4a780a311e93f5815535670cccf`

```dockerfile
```

-	Layers:
	-	`sha256:a80863c947154c96c5c53feb53e8aa015b38ae8cfd95399b0563d5fb34462db7`  
		Last Modified: Wed, 06 Mar 2024 19:11:19 GMT  
		Size: 9.2 MB (9161131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c2468894c965acae8852154e1747cedd7447e1f501b66dea90191d7a49af62c`  
		Last Modified: Wed, 06 Mar 2024 19:11:18 GMT  
		Size: 38.6 KB (38645 bytes)  
		MIME: application/vnd.in-toto+json
