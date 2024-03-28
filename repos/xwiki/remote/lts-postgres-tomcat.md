## `xwiki:lts-postgres-tomcat`

```console
$ docker pull xwiki@sha256:59ba0ce152f30868be3b2d1c66f9c41b67f98fdff335df13f4b996561d66243f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:f38b83b2aed32c4d40671265d94dabd2f13785b2c87e17bc442c10381861e2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 MB (590746807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1bf14a1adc81d4c2a57fc68397719bf1b12905db2daf959fe9b853f30207ae`
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
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
ENV XWIKI_VERSION=15.10.8
# Wed, 27 Mar 2024 12:37:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.8
# Wed, 27 Mar 2024 12:37:20 GMT
ENV XWIKI_DOWNLOAD_SHA256=20bfda3e0a694df904cab1f0291ff40761cf3461117654c5dc4860ba6397fd85
# Wed, 27 Mar 2024 12:37:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
ENV POSTGRES_JDBC_VERSION=42.7.2
# Wed, 27 Mar 2024 12:37:20 GMT
ENV POSTGRES_JDBC_SHA256=0c244ac7d02cf89d8e29852eace6595d75bc4d78581b85b2768460081646a57b
# Wed, 27 Mar 2024 12:37:20 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.2
# Wed, 27 Mar 2024 12:37:20 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.2.jar
# Wed, 27 Mar 2024 12:37:20 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.2.jar
# Wed, 27 Mar 2024 12:37:20 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:1ee7def01c01a73f331a4d0fa0b142b35fa92093fbb5512eb32b2e48448c0d49`  
		Last Modified: Thu, 28 Mar 2024 06:50:33 GMT  
		Size: 179.3 MB (179289215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed37f2a7babcf541836dfdee26a3ca2506d07c0741d9de1586cc3b46aaea3a0`  
		Last Modified: Thu, 28 Mar 2024 06:50:36 GMT  
		Size: 307.0 MB (307010855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b338c46a96025e9a4eedadc4f8d305110683ab242349eeb060ad4522302437`  
		Last Modified: Thu, 28 Mar 2024 06:50:29 GMT  
		Size: 1.0 MB (1011767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b655441155f0319b1fa0580dde4c55a8336b851b587f88ec1e46714e162ebab`  
		Last Modified: Thu, 28 Mar 2024 06:50:29 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb0fb5bfca8d270efe9cd60c7ea4df75ba54bdab8a91403c6477fea57c1bc0c`  
		Last Modified: Thu, 28 Mar 2024 06:50:30 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851643b39d22fd630f39fe67636c5659dddf5e6829b3de65b875432e67358134`  
		Last Modified: Thu, 28 Mar 2024 06:50:30 GMT  
		Size: 6.4 KB (6416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69af061b1129f97150f9c8d1611bf7c0b575f04623eae60f899251fdf4e14484`  
		Last Modified: Thu, 28 Mar 2024 06:50:31 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:4d10ac39a68c5013d31e52e72ff33e8c02923c9644ed1e39ba7a5f05446ea116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8946082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6c95ebcec3682b98126a7c0e1c648c88fec08313b75c58bf328c42eb3c4211`

```dockerfile
```

-	Layers:
	-	`sha256:b40d9e5893ea2bfdc514f2ca71a465b721ce2d7af5feff93700cac007ebc4801`  
		Last Modified: Thu, 28 Mar 2024 06:50:29 GMT  
		Size: 8.9 MB (8904609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5bbf34d5b5d1b98a5fc19b902fb24158bc2da7064f125109bf9f3e22d6eb418`  
		Last Modified: Thu, 28 Mar 2024 06:50:28 GMT  
		Size: 41.5 KB (41473 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:cd0b4e951806483979597ccc741ad21ea05e5774cf3adbfd6c0c214d8c267d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.1 MB (589137578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aded3a9f71dbf188c5d963cb2af664cce338ddfdfb0ccf7da1af8a7ed2cb1788`
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
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
ENV XWIKI_VERSION=15.10.7
# Fri, 08 Mar 2024 08:40:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.7
# Fri, 08 Mar 2024 08:40:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=7333e4459754a78b655ed6bdf7633229a750dbe9e92f7dd46fa217f4cf817669
# Fri, 08 Mar 2024 08:40:14 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 08 Mar 2024 08:40:14 GMT
ENV POSTGRES_JDBC_VERSION=42.7.2
# Fri, 08 Mar 2024 08:40:14 GMT
ENV POSTGRES_JDBC_SHA256=0c244ac7d02cf89d8e29852eace6595d75bc4d78581b85b2768460081646a57b
# Fri, 08 Mar 2024 08:40:14 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.2
# Fri, 08 Mar 2024 08:40:14 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.2.jar
# Fri, 08 Mar 2024 08:40:14 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.2.jar
# Fri, 08 Mar 2024 08:40:14 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:fa774a46917965174cd3aee75b24bd75d50bbb00d6c81ec17114bd8b0e27b527`  
		Last Modified: Fri, 15 Mar 2024 01:57:51 GMT  
		Size: 174.3 MB (174329932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6c540cfba58f6f1cc47b11231a5bb9b38dff38be9e1e9622b9c1a514eec83b`  
		Last Modified: Fri, 15 Mar 2024 02:01:42 GMT  
		Size: 307.0 MB (306998741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5273197581bcdab21ab133c687effb078ef46023b6efcabbf71e3fe137352fca`  
		Last Modified: Fri, 15 Mar 2024 02:01:35 GMT  
		Size: 1.0 MB (1011777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0729ab6f3bc4cba6a467bb994df8679cd4794453059eae09e82fa2e8f4d52cf4`  
		Last Modified: Fri, 15 Mar 2024 02:01:35 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3ce61c1f9e8b78ea4f6fcbc8a176823499b86def6d1bf21a46f77181f5255f`  
		Last Modified: Fri, 15 Mar 2024 02:01:35 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa86d1cf99908890f8e29b5831b754beea811363e77f3efd64b20d6c9ec016f3`  
		Last Modified: Fri, 15 Mar 2024 02:01:36 GMT  
		Size: 6.4 KB (6416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1dc19292e0ae57750b5e53d93e2aff1f7da7258bd3388afe46a53783336337`  
		Last Modified: Fri, 15 Mar 2024 02:01:36 GMT  
		Size: 2.4 KB (2430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:63b3a4d71434514e4f4a5ab018093c25c0d4135807e3b7db817f3776894e034a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9202765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6431b9cc262e7c94cb1dacfc486a293b2ebc0ecc6d45e73a1309b610ded81743`

```dockerfile
```

-	Layers:
	-	`sha256:ea863d25d9275d7e9b373b291d902c9692bb991aead17be3f6b128c35f1303a7`  
		Last Modified: Fri, 15 Mar 2024 02:01:35 GMT  
		Size: 9.2 MB (9162745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63de074d6c7a60dcc7874f84d4a9369ca48a9f42c0f63cc217840331dc7ef3f7`  
		Last Modified: Fri, 15 Mar 2024 02:01:34 GMT  
		Size: 40.0 KB (40020 bytes)  
		MIME: application/vnd.in-toto+json
