## `xwiki:lts-mysql`

```console
$ docker pull xwiki@sha256:a16840ad3328d1388543252c0e4d33f6b791eb51ec5d64f82d7ee293f90162df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:14dce9a8960e7bb856cd52e723d68efe0aca74d3c27ba197e9eceddf1b94e87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.7 MB (595660285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f89d50f56aa9a176bdc1b7f3c6245b8c70d478c42f8f8bf3a2b49ef5a31930f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 06:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 06:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 06:02:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 06:04:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 06:04:59 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 06:05:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 06:05:33 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 06:05:33 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 06:05:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 14:44:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Mar 2024 14:44:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:44:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 06 Mar 2024 14:44:04 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Mar 2024 14:44:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Mar 2024 14:44:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Mar 2024 14:46:31 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 06 Mar 2024 14:46:31 GMT
ENV TOMCAT_MAJOR=9
# Wed, 06 Mar 2024 14:46:31 GMT
ENV TOMCAT_VERSION=9.0.86
# Wed, 06 Mar 2024 14:46:31 GMT
ENV TOMCAT_SHA512=e8a8000dbeba5ee266ec4bf77217574364ffd114c8b913816f2e7a5e4eab4d01d0be3f05c8fccefcb5c5d770308efe1983be80279b6ef6d122d6183288a8ee9c
# Wed, 06 Mar 2024 14:46:32 GMT
COPY dir:a1b18cd4173fc89867b3684c0bcb6ed5fd2f800394449b55a0ac4e5f96c33c28 in /usr/local/tomcat 
# Wed, 06 Mar 2024 14:46:37 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 14:46:38 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 06 Mar 2024 14:46:38 GMT
EXPOSE 8080
# Wed, 06 Mar 2024 14:46:38 GMT
ENTRYPOINT []
# Wed, 06 Mar 2024 14:46:38 GMT
CMD ["catalina.sh" "run"]
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 08 Mar 2024 08:40:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
ENV XWIKI_VERSION=15.10.7
# Fri, 08 Mar 2024 08:40:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.7
# Fri, 08 Mar 2024 08:40:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=7333e4459754a78b655ed6bdf7633229a750dbe9e92f7dd46fa217f4cf817669
# Fri, 08 Mar 2024 08:40:14 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
ENV MYSQL_JDBC_VERSION=8.3.0
# Fri, 08 Mar 2024 08:40:14 GMT
ENV MYSQL_JDBC_SHA256=94e7fa815370cdcefed915db7f53f88445fac110f8c3818392b992ec9ee6d295
# Fri, 08 Mar 2024 08:40:14 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.3.0
# Fri, 08 Mar 2024 08:40:14 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.3.0.jar
# Fri, 08 Mar 2024 08:40:14 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.3.0.jar
# Fri, 08 Mar 2024 08:40:14 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
VOLUME [/usr/local/xwiki]
# Fri, 08 Mar 2024 08:40:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Mar 2024 08:40:14 GMT
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
	-	`sha256:6de2afe3955eb333e1ecd4572565a1a823168a9db04588f0c54eaa3cd29e4d2d`  
		Last Modified: Fri, 08 Mar 2024 19:49:51 GMT  
		Size: 178.3 MB (178349615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62057e0b7c75e85e3d77f04903656dc86594be333672118b054082e1444cc728`  
		Last Modified: Fri, 08 Mar 2024 19:49:54 GMT  
		Size: 307.0 MB (306998686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5068a3f9ac84ef3155577e87c38308381a1d0c1d62ac570693c8630e5b694324`  
		Last Modified: Fri, 08 Mar 2024 19:49:48 GMT  
		Size: 2.4 MB (2356946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5823b9547cf8fa9656683e3faea5dfa8ed3429f08b7f87b81bac04eea851e9`  
		Last Modified: Fri, 08 Mar 2024 19:49:48 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4ccf0234af3c29d0e69f2be56c94461f7f2e44d529a591f13b0417cc9bafe4`  
		Last Modified: Fri, 08 Mar 2024 19:49:49 GMT  
		Size: 2.4 KB (2370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fe05894f6b5164399753d219ba439dcae8087dc958c8629c06b3db8056ad9d`  
		Last Modified: Fri, 08 Mar 2024 19:49:49 GMT  
		Size: 6.4 KB (6415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a4d175f1432d7babdce402231892b4dd60f410fcebf7551b09f356bf9b783a`  
		Last Modified: Fri, 08 Mar 2024 19:49:50 GMT  
		Size: 2.5 KB (2481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mysql` - unknown; unknown

```console
$ docker pull xwiki@sha256:26f5683554f56a61812d1c1c1cbb455835349310b7e141e555e6e5083ebea386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9100618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409781360e98740034cd4537c1f58a2687fe5edaec95f1abb7f0178c7fb0ca7a`

```dockerfile
```

-	Layers:
	-	`sha256:fb177a366bdd478bac4f8516101cb2e7201782e017a5ff627e0cc5637fea8c53`  
		Last Modified: Fri, 08 Mar 2024 19:49:48 GMT  
		Size: 9.1 MB (9058183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05a09e63da330ae70772a535315cc1d65b40c83eff2fa6d91bc882d6cfa90af1`  
		Last Modified: Fri, 08 Mar 2024 19:49:48 GMT  
		Size: 42.4 KB (42435 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mysql` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:eaa56aa3ed7fba729471e9118b8226596feaf7e88ba84129ef7fecaddf19bf97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 MB (589529817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051f787ec9eb91f151fa7fe57896e682b3cc3afa5d154f1492b5d4daab378043`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 04:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 04:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 04:01:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 04:03:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 04:03:41 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 06 Mar 2024 04:04:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 06 Mar 2024 04:04:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 06 Mar 2024 04:04:08 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 06 Mar 2024 04:04:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 Mar 2024 11:26:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Mar 2024 11:26:10 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 11:26:10 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 06 Mar 2024 11:26:10 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Mar 2024 11:26:11 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Mar 2024 11:26:11 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Mar 2024 11:28:09 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 06 Mar 2024 11:28:09 GMT
ENV TOMCAT_MAJOR=9
# Wed, 06 Mar 2024 11:28:09 GMT
ENV TOMCAT_VERSION=9.0.86
# Wed, 06 Mar 2024 11:28:09 GMT
ENV TOMCAT_SHA512=e8a8000dbeba5ee266ec4bf77217574364ffd114c8b913816f2e7a5e4eab4d01d0be3f05c8fccefcb5c5d770308efe1983be80279b6ef6d122d6183288a8ee9c
# Wed, 06 Mar 2024 11:28:09 GMT
COPY dir:28b6e0807ab1afc14ce8a00cdcc0b2974f83fc2610eb66e632a1e50cf924f4d1 in /usr/local/tomcat 
# Wed, 06 Mar 2024 11:28:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Mar 2024 11:28:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 06 Mar 2024 11:28:14 GMT
EXPOSE 8080
# Wed, 06 Mar 2024 11:28:14 GMT
ENTRYPOINT []
# Wed, 06 Mar 2024 11:28:14 GMT
CMD ["catalina.sh" "run"]
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 08 Mar 2024 08:40:14 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 08 Mar 2024 08:40:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
ENV XWIKI_VERSION=15.10.7
# Fri, 08 Mar 2024 08:40:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.7
# Fri, 08 Mar 2024 08:40:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=7333e4459754a78b655ed6bdf7633229a750dbe9e92f7dd46fa217f4cf817669
# Fri, 08 Mar 2024 08:40:14 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
ENV MYSQL_JDBC_VERSION=8.3.0
# Fri, 08 Mar 2024 08:40:14 GMT
ENV MYSQL_JDBC_SHA256=94e7fa815370cdcefed915db7f53f88445fac110f8c3818392b992ec9ee6d295
# Fri, 08 Mar 2024 08:40:14 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.3.0
# Fri, 08 Mar 2024 08:40:14 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.3.0.jar
# Fri, 08 Mar 2024 08:40:14 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.3.0.jar
# Fri, 08 Mar 2024 08:40:14 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
VOLUME [/usr/local/xwiki]
# Fri, 08 Mar 2024 08:40:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Mar 2024 08:40:14 GMT
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
	-	`sha256:84d2716dc193947443b4076411c7be42b6193da2fef7865bab47581d1b667c0e`  
		Last Modified: Wed, 06 Mar 2024 19:09:21 GMT  
		Size: 173.4 MB (173387332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f721f1b59f0dddf83676baaa9825bf579367dce3dd097672521447fd488c968`  
		Last Modified: Fri, 08 Mar 2024 20:02:59 GMT  
		Size: 307.0 MB (306998695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb6d22b989bfc9d70e4e6b646135c150f53c3258d4ab3925dd76972f027e05e`  
		Last Modified: Fri, 08 Mar 2024 20:02:52 GMT  
		Size: 2.4 MB (2356953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c8eefeb4d561ebc35865b86395025f862fce5a911099350cae6c6b581de66`  
		Last Modified: Fri, 08 Mar 2024 20:02:52 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15e2dd2446a50b0dddcf4a06f49ab8e16f1f25f21446b75379b99c5823c51b7`  
		Last Modified: Fri, 08 Mar 2024 20:02:52 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe5af3028ed6ed690a076a181b1c0ddd3ff57772db4d13260f8272488dc4c90`  
		Last Modified: Fri, 08 Mar 2024 20:02:53 GMT  
		Size: 6.4 KB (6416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856c93cfff0c477645f59f8fb1fa92c1c2d895121183f2e2ed39cc23ae743ef2`  
		Last Modified: Fri, 08 Mar 2024 20:02:53 GMT  
		Size: 2.5 KB (2476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mysql` - unknown; unknown

```console
$ docker pull xwiki@sha256:51038299202aec490f3c6bf899d178e696942de49d9d7613ac37ea0e4f604c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9195606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa673845a07c8d3878d0a4ccb1af2df5918be140bfb2403aed127d45fa066fa`

```dockerfile
```

-	Layers:
	-	`sha256:ff7cfb2daafc5c1d3b1c6f4cad869083b675418448a92973f054580ee8fd38d5`  
		Last Modified: Fri, 08 Mar 2024 20:02:52 GMT  
		Size: 9.2 MB (9154617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee4f3809c10eba8a642459ba5305a20b645a311f714dfcb13e4935de09a7baf`  
		Last Modified: Fri, 08 Mar 2024 20:02:51 GMT  
		Size: 41.0 KB (40989 bytes)  
		MIME: application/vnd.in-toto+json
