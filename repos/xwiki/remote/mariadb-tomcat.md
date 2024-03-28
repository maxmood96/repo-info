## `xwiki:mariadb-tomcat`

```console
$ docker pull xwiki@sha256:73d303ec2270d622e6a9752a896335f4cb14fb47c6830300ef1d418189405ea3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:2b2611043857867222544e4012570b4062ccd096aeb6021f58f85781ff6d19bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.0 MB (575958173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7788f021e1315d0c21c30423d1135b8bed2c844f6297b057b2a4f022c5a92df2`
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
# Mon, 25 Mar 2024 15:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 25 Mar 2024 15:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Mar 2024 15:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 25 Mar 2024 15:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 25 Mar 2024 15:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Mar 2024 15:14:20 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 25 Mar 2024 15:14:20 GMT
WORKDIR /usr/local/tomcat
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 25 Mar 2024 15:14:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 25 Mar 2024 15:14:20 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_MAJOR=9
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_VERSION=9.0.87
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_SHA512=71a64fe805aab89ef4798571d860a3c9a4f751f808921559a9249305abb205836de33ab89bb33b625a77f799f193d6bffbe94aadf293866df756d708f5bfb933
# Mon, 25 Mar 2024 15:14:20 GMT
COPY dir:1b7eb8910bc8098ccd23704e6363c1d0223ae894023590ed66576796ee44f567 in /usr/local/tomcat 
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 25 Mar 2024 15:14:20 GMT
EXPOSE 8080
# Mon, 25 Mar 2024 15:14:20 GMT
ENTRYPOINT []
# Mon, 25 Mar 2024 15:14:20 GMT
CMD ["catalina.sh" "run"]
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 25 Mar 2024 15:14:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENV XWIKI_VERSION=16.2.0
# Mon, 25 Mar 2024 15:14:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.2.0
# Mon, 25 Mar 2024 15:14:20 GMT
ENV XWIKI_DOWNLOAD_SHA256=7d355ae1c88691b19af9658e3f042083d57c08d5e52e1ade25536536ad72fb3f
# Mon, 25 Mar 2024 15:14:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MARIADB_JDBC_VERSION=3.3.3
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MARIADB_JDBC_SHA256=89d71a6ffd800c032b23e588108688d391631f0aba962ba2381cc82cb111b796
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.3
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.3.jar
# Mon, 25 Mar 2024 15:14:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.3.jar
# Mon, 25 Mar 2024 15:14:20 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
VOLUME [/usr/local/xwiki]
# Mon, 25 Mar 2024 15:14:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Mar 2024 15:14:20 GMT
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
	-	`sha256:7957bda1bcdf9c365c72458bf6669334a09940e5e376df4212b819ee17b70b74`  
		Last Modified: Thu, 28 Mar 2024 06:50:05 GMT  
		Size: 178.3 MB (178346471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5491e71575df8168e9b54216ed18a257982c0dd0b65e7f993284ca2dc75ae67b`  
		Last Modified: Thu, 28 Mar 2024 06:50:07 GMT  
		Size: 293.6 MB (293556788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee903cf077a2d613e442aa32211fffbfcb08cce5ba4f70a782d210300396c7d`  
		Last Modified: Thu, 28 Mar 2024 06:50:03 GMT  
		Size: 620.0 KB (619999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f201d563ae53f9109e90f27feddb2c034ca6155d7c5b8c24b0afbb3b9bcdfc5f`  
		Last Modified: Thu, 28 Mar 2024 06:50:05 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d9bfda1d6f22c553337fc5bddc3f14e5f0fe820dca032cc0ad28f00f293164`  
		Last Modified: Thu, 28 Mar 2024 06:50:04 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce9ff56903a2f43fcffc911c1b3b86b3bc9a36b0283b05368d61f962b3d714a`  
		Last Modified: Thu, 28 Mar 2024 06:50:05 GMT  
		Size: 6.5 KB (6509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8650562795fa47d912f2e3a6e70349ac1d911ed0306af789a53bc35cb1106fc`  
		Last Modified: Thu, 28 Mar 2024 06:50:05 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:a9fa8c56c4c416cbb9d3c9f31b955ac6ba1935d3f64836e92bce9e119906a1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8925706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9810842950230a3f93feaa6908cbc4fd9b6f4234d9ae3f2f716606484fa60d2b`

```dockerfile
```

-	Layers:
	-	`sha256:c6b7ef5d69f734533948a46e68f7b63400ad656f3c02789ebae623fe5e1970ec`  
		Last Modified: Thu, 28 Mar 2024 06:50:02 GMT  
		Size: 8.9 MB (8884002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cedaff261151a1d7ae69b9f13c8fb65731c64f5632df6521396dd1fc5edaa561`  
		Last Modified: Thu, 28 Mar 2024 06:50:02 GMT  
		Size: 41.7 KB (41704 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:94cad8caa8a16b81a9cc14e5d72adc0034b2ab6bae1bd1b76a818bd262c53cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.7 MB (587683450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72611c58f5884863ad40a688c40e687c96e4c40e1bfe6d1ee6d461d4b7a84f66`
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
ENV TOMCAT_VERSION=9.0.87
# Mon, 26 Feb 2024 13:14:55 GMT
ENV TOMCAT_SHA512=71a64fe805aab89ef4798571d860a3c9a4f751f808921559a9249305abb205836de33ab89bb33b625a77f799f193d6bffbe94aadf293866df756d708f5bfb933
# Mon, 26 Feb 2024 13:14:55 GMT
COPY dir:a438b3922681c6646cb859c6691b163ee551beeceefb652b5380a78c74ba3266 in /usr/local/tomcat 
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
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_VERSION=16.1.0
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.1.0
# Mon, 26 Feb 2024 13:14:55 GMT
ENV XWIKI_DOWNLOAD_SHA256=e236fc101710a0bfefed2328cc66652e265f21ab40dd30e6b7ce52300da744d5
# Mon, 26 Feb 2024 13:14:55 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MARIADB_JDBC_VERSION=3.3.2
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MARIADB_JDBC_SHA256=2a67ef3cc1ca481965a0e7f2d4174d126f3464d02b4055a441261fad8c196769
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.2
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.2.jar
# Mon, 26 Feb 2024 13:14:55 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.2.jar
# Mon, 26 Feb 2024 13:14:55 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:51ba967c5130211c007fa344d7fd198e690a3531033260a6120aa2ecc42e3420`  
		Last Modified: Fri, 15 Mar 2024 01:55:52 GMT  
		Size: 306.9 MB (306883025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854a07c126f65e40a53248a7948f28fcb2fc600639adcc14ab2c1934eddf59b3`  
		Last Modified: Fri, 15 Mar 2024 01:58:28 GMT  
		Size: 615.1 KB (615138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cc331c9148f0f936e6d6c0de3d588c5631cdbfd25328d2debcab837a82e50f`  
		Last Modified: Fri, 15 Mar 2024 01:58:28 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b2cca63d81addd46bd54669f814c40620ca1f1dcc505e0c14ce494cf16b5c8`  
		Last Modified: Fri, 15 Mar 2024 01:58:29 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bb0bffc0d607ce1a031583074039d61ce62e1b018dd87a7bceba8bda8e4574`  
		Last Modified: Fri, 15 Mar 2024 01:58:29 GMT  
		Size: 6.4 KB (6408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ca8cd6399c9242cb4781a3c1847ce9348298d8a1e8799bf5c78daff1d6a96e`  
		Last Modified: Fri, 15 Mar 2024 01:58:29 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:c2f09408c3579a518c855d23cb8924e7b6f635b56f854a28fbd712e9de28bac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9191991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c456a35d6db1723aa1ec49b7e40441121e47463f568aeabe202644d2cd97db`

```dockerfile
```

-	Layers:
	-	`sha256:90ab595f43f713bf54100a75031147dd0d50ba87ce9923218396409a4be11727`  
		Last Modified: Fri, 15 Mar 2024 01:58:28 GMT  
		Size: 9.2 MB (9151818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8460a99e64e4ca769960dafeff36e44be7b89802c29f2c243841f27f74bbb89`  
		Last Modified: Fri, 15 Mar 2024 01:58:28 GMT  
		Size: 40.2 KB (40173 bytes)  
		MIME: application/vnd.in-toto+json
