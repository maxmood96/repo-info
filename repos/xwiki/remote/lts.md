## `xwiki:lts`

```console
$ docker pull xwiki@sha256:a16437aed8c4967baa2217488c500db077687728f3b8e8929e83cc27a3a158b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts` - linux; amd64

```console
$ docker pull xwiki@sha256:282bcbef5db2bad0405c4d676a542da0c089f65e969126ab3b8a93684c824fd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.1 MB (591149387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a792e4bdde42d9d46155d92dfb9a2304c80676d0ffae5fcbd82dd20a8f5c3506`
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
# Wed, 27 Mar 2024 12:37:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 12:37:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 12:37:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 12:37:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 27 Mar 2024 12:37:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 Mar 2024 12:37:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 27 Mar 2024 12:37:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 12:37:20 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 27 Mar 2024 12:37:20 GMT
WORKDIR /usr/local/tomcat
# Wed, 27 Mar 2024 12:37:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 27 Mar 2024 12:37:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 27 Mar 2024 12:37:20 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 27 Mar 2024 12:37:20 GMT
ENV TOMCAT_MAJOR=9
# Wed, 27 Mar 2024 12:37:20 GMT
ENV TOMCAT_VERSION=9.0.87
# Wed, 27 Mar 2024 12:37:20 GMT
ENV TOMCAT_SHA512=71a64fe805aab89ef4798571d860a3c9a4f751f808921559a9249305abb205836de33ab89bb33b625a77f799f193d6bffbe94aadf293866df756d708f5bfb933
# Wed, 27 Mar 2024 12:37:20 GMT
COPY dir:1b7eb8910bc8098ccd23704e6363c1d0223ae894023590ed66576796ee44f567 in /usr/local/tomcat 
# Wed, 27 Mar 2024 12:37:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Mar 2024 12:37:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 27 Mar 2024 12:37:20 GMT
EXPOSE 8080
# Wed, 27 Mar 2024 12:37:20 GMT
ENTRYPOINT []
# Wed, 27 Mar 2024 12:37:20 GMT
CMD ["catalina.sh" "run"]
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 27 Mar 2024 12:37:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
ENV XWIKI_VERSION=15.10.8
# Wed, 27 Mar 2024 12:37:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.8
# Wed, 27 Mar 2024 12:37:20 GMT
ENV XWIKI_DOWNLOAD_SHA256=20bfda3e0a694df904cab1f0291ff40761cf3461117654c5dc4860ba6397fd85
# Wed, 27 Mar 2024 12:37:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
ENV MYSQL_JDBC_VERSION=8.3.0
# Wed, 27 Mar 2024 12:37:20 GMT
ENV MYSQL_JDBC_SHA256=94e7fa815370cdcefed915db7f53f88445fac110f8c3818392b992ec9ee6d295
# Wed, 27 Mar 2024 12:37:20 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.3.0
# Wed, 27 Mar 2024 12:37:20 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.3.0.jar
# Wed, 27 Mar 2024 12:37:20 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.3.0.jar
# Wed, 27 Mar 2024 12:37:20 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
VOLUME [/usr/local/xwiki]
# Wed, 27 Mar 2024 12:37:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Mar 2024 12:37:20 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcf356fa6e6902e661a53c29cf3b351f284090cb2c0de2ad6c5c238a6fdb9a8`  
		Last Modified: Thu, 28 Mar 2024 02:03:28 GMT  
		Size: 12.9 MB (12904693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b345ba1396e8406df1a417529c91dac4e4802e6b18921719b9022f3dfb3734cf`  
		Last Modified: Thu, 28 Mar 2024 02:10:46 GMT  
		Size: 47.2 MB (47163261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e0a682e40f83e4da859eee85bc3b44b9444d2949261d3f2a475b030d190ecb`  
		Last Modified: Thu, 28 Mar 2024 02:10:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa5752204b57ae4cecf034a16e07738b48b46bfdb2f5aa6981b074fb11f5626`  
		Last Modified: Thu, 28 Mar 2024 02:10:39 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8f1afe60079669368c29402da24b093023b9874a58b5402d46e7e6709b9ac8`  
		Last Modified: Thu, 28 Mar 2024 05:48:07 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2076fd4f33939f872611b30f973b9224fccb39131b3050db010b335b8bb6b0`  
		Last Modified: Thu, 28 Mar 2024 05:50:53 GMT  
		Size: 12.4 MB (12422017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ded95effffe761d3bde95cf09b6a59eb231507f956d0fceb5ca196926a3d0a0`  
		Last Modified: Thu, 28 Mar 2024 05:50:52 GMT  
		Size: 479.8 KB (479845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2a52af66be5132f3fd6a02d586c40e5f65896f45662fc58450801219f0ac8b`  
		Last Modified: Thu, 28 Mar 2024 05:50:52 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3e0089c5c43d4daaf0240b8681c106bf3f0df744cd5cf021fd3cdc1e29679e`  
		Last Modified: Thu, 28 Mar 2024 06:50:11 GMT  
		Size: 178.3 MB (178346620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4720fb789adafb3e61d645952ccf854474acfc69b87904a1ff3c6db2b1d25c1`  
		Last Modified: Thu, 28 Mar 2024 06:50:12 GMT  
		Size: 307.0 MB (307010896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babdc70eb96ceec38bd25313c418f9721b87838301098df51e936e2f61d7a4b4`  
		Last Modified: Thu, 28 Mar 2024 06:50:08 GMT  
		Size: 2.4 MB (2356950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f119313674fb7c69e31e5d9795de8afbbc8ac05ee58a2c1f69603dc5d87705`  
		Last Modified: Thu, 28 Mar 2024 06:50:08 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee55fd0a9157e96d1124fcd15d392cdf01226aa12eb4f94537db1e9af529412b`  
		Last Modified: Thu, 28 Mar 2024 06:50:09 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6991110a6d7cf3377c6a8bed4b72ec9c51d987850e9c102f5649cfdb7dce2dd8`  
		Last Modified: Thu, 28 Mar 2024 06:50:09 GMT  
		Size: 6.4 KB (6417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac456d3bf42ea816420c89a6c8c338bb821eff2daa2392a681e39bf19bcefc9`  
		Last Modified: Thu, 28 Mar 2024 06:50:10 GMT  
		Size: 2.5 KB (2481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts` - unknown; unknown

```console
$ docker pull xwiki@sha256:27037c935c44848d1c3bd5e2bdcf74d534d5a6b256dda0281867d132c60cfc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8938908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f575fddb55d54d988ab1b556c984a550510250f3b84dc651d4360930e3cb53`

```dockerfile
```

-	Layers:
	-	`sha256:0514350a5ac07dce130f4b3d5536be4b33fcfe0a1acafb93a743727d5b72b067`  
		Last Modified: Thu, 28 Mar 2024 06:50:08 GMT  
		Size: 8.9 MB (8896473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d9083e09251c8baf1a5f6033e446b22b7559fe2269391ccb98523cca20dea6f`  
		Last Modified: Thu, 28 Mar 2024 06:50:08 GMT  
		Size: 42.4 KB (42435 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:cf169387264bbc9f5748444f209be7606fa93e014551414b429fdd12b0935642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 MB (589541042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b406fa0aa601c3d0b04fb23d2d2c82ba3055f7958dc72bf6ac58e66e9c59d1`
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
# Fri, 08 Mar 2024 08:40:14 GMT
ENV TOMCAT_VERSION=9.0.87
# Fri, 08 Mar 2024 08:40:14 GMT
ENV TOMCAT_SHA512=71a64fe805aab89ef4798571d860a3c9a4f751f808921559a9249305abb205836de33ab89bb33b625a77f799f193d6bffbe94aadf293866df756d708f5bfb933
# Fri, 08 Mar 2024 08:40:14 GMT
COPY dir:a438b3922681c6646cb859c6691b163ee551beeceefb652b5380a78c74ba3266 in /usr/local/tomcat 
# Fri, 08 Mar 2024 08:40:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 08 Mar 2024 08:40:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 08 Mar 2024 08:40:14 GMT
EXPOSE 8080
# Fri, 08 Mar 2024 08:40:14 GMT
ENTRYPOINT []
# Fri, 08 Mar 2024 08:40:14 GMT
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
	-	`sha256:74e281f727be7fd28fba4819ffdd9ce87f32b51125b9ec925007964e5de10120`  
		Last Modified: Fri, 15 Mar 2024 01:03:45 GMT  
		Size: 12.4 MB (12428440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eac2aa3387dedf25ad21372bea13d10b6f0a6fed373df59d31ad8f5b09de7e5`  
		Last Modified: Fri, 15 Mar 2024 01:03:44 GMT  
		Size: 457.3 KB (457321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684ab03dff227b5ec8e230cdb2d0fd458f091d52e3d8ee4b703fba7694aa2187`  
		Last Modified: Fri, 15 Mar 2024 01:03:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555f2f2efb411e6fb4cdc817013317dd9a304f3b366e6759cf86919293dffa22`  
		Last Modified: Fri, 15 Mar 2024 01:55:48 GMT  
		Size: 173.4 MB (173388300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7db3b5c982f8b81fac57dde6b9ad207fdb902b036262201514e7f2479559d4`  
		Last Modified: Fri, 15 Mar 2024 02:00:06 GMT  
		Size: 307.0 MB (306998696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c811d52f814169180beac7e0493e2c5aeeb748f33da701fa979a1276282fc927`  
		Last Modified: Fri, 15 Mar 2024 01:59:59 GMT  
		Size: 2.4 MB (2356957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bc45be22825c55805a5919e7b2f50fb028dbd636751e6081d30d8f6ee91e1b`  
		Last Modified: Fri, 15 Mar 2024 01:59:59 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e9670bc111f5bfca1310a41d69b78218816bbb2d832b9b63ee6332b3e88639`  
		Last Modified: Fri, 15 Mar 2024 01:59:59 GMT  
		Size: 2.4 KB (2370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df76d224ffc4e3a0b389024782ccf023a2a19b20e9da600413f8574007366d53`  
		Last Modified: Fri, 15 Mar 2024 02:00:00 GMT  
		Size: 6.4 KB (6417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b77646ce72e57f0007c3202e2ddeb914e24ae1c0fb792e97aed0a092cc7903`  
		Last Modified: Fri, 15 Mar 2024 02:00:00 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts` - unknown; unknown

```console
$ docker pull xwiki@sha256:b210310788270fe808656127e2fea0ab489408099141523c4a23bd2a269fc04e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9195607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551443c12c371e9e3e5f28cddde801c45d42a21daff1610400ed1272b0c7f5b9`

```dockerfile
```

-	Layers:
	-	`sha256:4e8dd5d4b7473a5ef0cd6982ddab1be807ebba27f0db5563a7ea09dc4fcd2d14`  
		Last Modified: Fri, 15 Mar 2024 02:00:00 GMT  
		Size: 9.2 MB (9154617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3931e872691aedd9e92b8622ac1ac03cd5c7a64a57011dde0bea8b2792468a7c`  
		Last Modified: Fri, 15 Mar 2024 01:59:59 GMT  
		Size: 41.0 KB (40990 bytes)  
		MIME: application/vnd.in-toto+json
