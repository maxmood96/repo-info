## `xwiki:stable-postgres-tomcat`

```console
$ docker pull xwiki@sha256:cb9899aa87cbce5a940f45e57a0c61a716f184ca52e73f85e8607965a4001cc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:f5f1140e625a8e8adeb7a14e3a79b49a53c7954bf40cfc94ce8ba782fce350e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.9 MB (577899714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f0e59e2908088cb998307a157bd4672cb0a828d9fc298d9c6fa83ca4203e0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 30 May 2024 07:53:53 GMT
ARG RELEASE
# Thu, 30 May 2024 07:53:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 07:53:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 07:53:53 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 30 May 2024 07:53:53 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Thu, 30 May 2024 07:53:53 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 May 2024 07:53:53 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 30 May 2024 07:53:53 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 07:53:53 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 30 May 2024 07:53:53 GMT
WORKDIR /usr/local/tomcat
# Thu, 30 May 2024 07:53:53 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 30 May 2024 07:53:53 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 30 May 2024 07:53:53 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 30 May 2024 07:53:53 GMT
ENV TOMCAT_MAJOR=9
# Thu, 30 May 2024 07:53:53 GMT
ENV TOMCAT_VERSION=9.0.89
# Thu, 30 May 2024 07:53:53 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Thu, 30 May 2024 07:53:53 GMT
COPY dir:0b3a96ac60d75fdf26c7de1d52191df4fd550034e1462b3aee30307d4473afec in /usr/local/tomcat 
# Thu, 30 May 2024 07:53:53 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 30 May 2024 07:53:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 30 May 2024 07:53:53 GMT
EXPOSE 8080
# Thu, 30 May 2024 07:53:53 GMT
ENTRYPOINT []
# Thu, 30 May 2024 07:53:53 GMT
CMD ["catalina.sh" "run"]
# Thu, 30 May 2024 07:53:53 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 30 May 2024 07:53:53 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 30 May 2024 07:53:53 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 30 May 2024 07:53:53 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 30 May 2024 07:53:53 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 30 May 2024 07:53:53 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 30 May 2024 07:53:53 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 May 2024 07:53:53 GMT
ENV XWIKI_VERSION=16.4.0
# Thu, 30 May 2024 07:53:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.4.0
# Thu, 30 May 2024 07:53:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=ced263c074f3a61384717cafa192a52aebd34db122e9467f69af2999ab3b600e
# Thu, 30 May 2024 07:53:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 30 May 2024 07:53:53 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Thu, 30 May 2024 07:53:53 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Thu, 30 May 2024 07:53:53 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Thu, 30 May 2024 07:53:53 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Thu, 30 May 2024 07:53:53 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Thu, 30 May 2024 07:53:53 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 30 May 2024 07:53:53 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 30 May 2024 07:53:53 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 30 May 2024 07:53:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 30 May 2024 07:53:53 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 30 May 2024 07:53:53 GMT
VOLUME [/usr/local/xwiki]
# Thu, 30 May 2024 07:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 May 2024 07:53:53 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab7f202453ac8b8def634e399240ab2bd7247e2f125fbddd2dbaaa8fa4ce555`  
		Last Modified: Wed, 05 Jun 2024 04:58:06 GMT  
		Size: 12.9 MB (12904817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee59ca42def8dda96caccd58b671902e65195492ee8e5daa263e1e948033adc3`  
		Last Modified: Wed, 05 Jun 2024 05:01:21 GMT  
		Size: 47.3 MB (47256057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce2282f972ff7152adb0a2c757ddd63cf0c38d489c7d7952d7aa88ab1804bc5`  
		Last Modified: Wed, 05 Jun 2024 05:01:15 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a9e456ba828f8cfc067a64b3717c10e4c0709fc1f0b95e5a5efd3ee816e643`  
		Last Modified: Wed, 05 Jun 2024 05:01:15 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf4892f7e4550fc70dba9049d20a75e7eee29216fc7246e9610f72a3bfc77ce`  
		Last Modified: Wed, 05 Jun 2024 08:23:47 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a52c16c9d1baa051c919c53cbd2983dffbeb42c5654bc64c1c0e6459b6bab7`  
		Last Modified: Wed, 05 Jun 2024 08:26:45 GMT  
		Size: 12.4 MB (12436429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada98b1788f7769dac54217993e85011083578a04978203315d894fd2a0b6ce6`  
		Last Modified: Wed, 05 Jun 2024 08:26:44 GMT  
		Size: 456.3 KB (456302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2924b1a39c5ab975ebf002293359197f56ebd98fee88f805581087395bd292c4`  
		Last Modified: Wed, 05 Jun 2024 08:26:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c681a562d61707cd26f06ce324bdfc3cd448b5b8f72362b47caecea4739a39f`  
		Last Modified: Wed, 05 Jun 2024 09:07:26 GMT  
		Size: 179.4 MB (179374406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12faa2b96da785b8b05b62324faf4dfa9f28d1cb4a8ee6c022ed0d803562413d`  
		Last Modified: Wed, 05 Jun 2024 09:07:28 GMT  
		Size: 294.0 MB (294006509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9000fe9ef9258745719e42105b2550e18a06ed950694890dedf21f0108f0d484`  
		Last Modified: Wed, 05 Jun 2024 09:07:24 GMT  
		Size: 1.0 MB (1011982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57826a032c7103390d3f4352e22209de03ec4df373d20d467ca81097dc793f82`  
		Last Modified: Wed, 05 Jun 2024 09:07:24 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de04cb555e93e42e3675d65392757d2e98be5b8a227833381a199e2f02681a5`  
		Last Modified: Wed, 05 Jun 2024 09:07:25 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9faab8670e11ec8268db41ac1519e1aaeda0c01a33d8a881502e2f1fbe83ae`  
		Last Modified: Wed, 05 Jun 2024 09:07:25 GMT  
		Size: 6.5 KB (6524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d8a27d14ea59cedb43e3833b6370908b3dbf383d2e00405d0b0ce83ece4f8b`  
		Last Modified: Wed, 05 Jun 2024 09:07:25 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:9859a32d3670682b116d52e8515e0a319b1d835f76bfea7b9199d245f40263cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8934583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420930974c9287b02cdb1e27986100bde561cc5663d05b824a40f079eb58e177`

```dockerfile
```

-	Layers:
	-	`sha256:500a92c5a4a817c74b82c85bfe45cd05e996942cd7e8f07c353a1e7790c367b1`  
		Last Modified: Wed, 05 Jun 2024 09:07:24 GMT  
		Size: 8.9 MB (8894256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab831c25a7e6e62ff33626ae90de80da6fd923dcfa3972fd0913885cae4b47ab`  
		Last Modified: Wed, 05 Jun 2024 09:07:24 GMT  
		Size: 40.3 KB (40327 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:c9a0f880187a09aff9b835d18ae992ceb0db1c1addfeee6849f670a01f0a1747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.3 MB (570326598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50478a250bf3a42eee585b97bcd238810a25ee18842ad69484e218eef202873c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 30 May 2024 07:53:53 GMT
ARG RELEASE
# Thu, 30 May 2024 07:53:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 07:53:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 07:53:53 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 30 May 2024 07:53:53 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Thu, 30 May 2024 07:53:53 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 May 2024 07:53:53 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 30 May 2024 07:53:53 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 07:53:53 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 30 May 2024 07:53:53 GMT
WORKDIR /usr/local/tomcat
# Thu, 30 May 2024 07:53:53 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 30 May 2024 07:53:53 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 30 May 2024 07:53:53 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 30 May 2024 07:53:53 GMT
ENV TOMCAT_MAJOR=9
# Thu, 30 May 2024 07:53:53 GMT
ENV TOMCAT_VERSION=9.0.89
# Thu, 30 May 2024 07:53:53 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Thu, 30 May 2024 07:53:53 GMT
COPY dir:58ad55bab575cab028cf8b426107fdedda2ac4d0f3638bd518c64d50c26f920e in /usr/local/tomcat 
# Thu, 30 May 2024 07:53:53 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 30 May 2024 07:53:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 30 May 2024 07:53:53 GMT
EXPOSE 8080
# Thu, 30 May 2024 07:53:53 GMT
ENTRYPOINT []
# Thu, 30 May 2024 07:53:53 GMT
CMD ["catalina.sh" "run"]
# Thu, 30 May 2024 07:53:53 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 30 May 2024 07:53:53 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 30 May 2024 07:53:53 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 30 May 2024 07:53:53 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 30 May 2024 07:53:53 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 30 May 2024 07:53:53 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 30 May 2024 07:53:53 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 May 2024 07:53:53 GMT
ENV XWIKI_VERSION=16.4.0
# Thu, 30 May 2024 07:53:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.4.0
# Thu, 30 May 2024 07:53:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=ced263c074f3a61384717cafa192a52aebd34db122e9467f69af2999ab3b600e
# Thu, 30 May 2024 07:53:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 30 May 2024 07:53:53 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Thu, 30 May 2024 07:53:53 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Thu, 30 May 2024 07:53:53 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Thu, 30 May 2024 07:53:53 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Thu, 30 May 2024 07:53:53 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Thu, 30 May 2024 07:53:53 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 30 May 2024 07:53:53 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 30 May 2024 07:53:53 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 30 May 2024 07:53:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 30 May 2024 07:53:53 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 30 May 2024 07:53:53 GMT
VOLUME [/usr/local/xwiki]
# Thu, 30 May 2024 07:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 May 2024 07:53:53 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd918abfec0657ade8aeeffe2722e92948e13fa403fd238ae22b1a9881e9402`  
		Last Modified: Wed, 05 Jun 2024 04:55:01 GMT  
		Size: 12.8 MB (12847839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa963c04773e39efb3eb3c080a80fe1bccbf8410a480f24229a7a06fc307c532`  
		Last Modified: Wed, 05 Jun 2024 04:57:44 GMT  
		Size: 46.7 MB (46716398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382cfd76d96df44a0a5e200f1841a3fc8d1bdbfa5fb655a2f2795bc3b4e16ec3`  
		Last Modified: Wed, 05 Jun 2024 04:57:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0792dc21c67221e401d3c4b78ebea1705a045fbcc6461558ac50bfbe911989a`  
		Last Modified: Wed, 05 Jun 2024 04:57:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d9376e25e5ba92936ed244a6a17f40e0e94193fe0dc8f60206086fbde34bd1`  
		Last Modified: Wed, 05 Jun 2024 07:34:27 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5691ecc99a8f77b5bbea731a32ed78a6cc766bfe44b2e3f4eeab129e2f2daf83`  
		Last Modified: Wed, 05 Jun 2024 07:37:16 GMT  
		Size: 12.4 MB (12444380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1b63586cd37b618e234ed2a73da7b1c927b4c63791efcfdb630d22109cdedb`  
		Last Modified: Wed, 05 Jun 2024 07:37:15 GMT  
		Size: 456.8 KB (456815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da359c1a7d5b25cd7c2be940e7d189a81733ec484209e3da051054b173bde3`  
		Last Modified: Wed, 05 Jun 2024 07:37:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345a9caf50392be2f1c84bb828ce40eafb06b52ebe676aba3304eda51483d4e6`  
		Last Modified: Wed, 05 Jun 2024 18:24:27 GMT  
		Size: 174.4 MB (174426356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd638a3734fec63efdc8021efe11821183ab640ce2b93b762e3fe579a383a76`  
		Last Modified: Wed, 05 Jun 2024 18:24:30 GMT  
		Size: 294.0 MB (294006598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca9b8721a7d9111dbff0a27d5d849d7dbd6ffce80a3318aeb88dc04410042c3`  
		Last Modified: Wed, 05 Jun 2024 18:24:23 GMT  
		Size: 1.0 MB (1011977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83d52071b5cbe70a502bc9394e1cdf07d065754c2ff555308df4b323470f2cb`  
		Last Modified: Wed, 05 Jun 2024 18:24:22 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307e9523582ecce94f4e65cef1405e07fa83296b365a685c3672b1e33824bb76`  
		Last Modified: Wed, 05 Jun 2024 18:24:23 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de7d723f0bd0ecb2d418c6722210c0bcbb2e09f1076a4f808527f70a313124a`  
		Last Modified: Wed, 05 Jun 2024 18:24:24 GMT  
		Size: 6.5 KB (6521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd4ed0ee778c8b25876c6534a40fa0efb26f86ce134c92885eb7e0af51adf4b`  
		Last Modified: Wed, 05 Jun 2024 18:24:25 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:cd3d55b2155531fb462b536021f5d89f97849330cc5cb809d5eedbf0d74cb740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8935485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a69f612085e27189cf567bcbb58aff7014fde8c648be14a05b10a12ef0e8a7c`

```dockerfile
```

-	Layers:
	-	`sha256:066cdf2eab37be0505908d3b58008d7b82b8770835e8715929b04083000280ed`  
		Last Modified: Wed, 05 Jun 2024 18:24:23 GMT  
		Size: 8.9 MB (8894830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174b0450e6d715842b19299b6095e48573da6cef5c49b16ab4d62abb12842959`  
		Last Modified: Wed, 05 Jun 2024 18:24:22 GMT  
		Size: 40.7 KB (40655 bytes)  
		MIME: application/vnd.in-toto+json
