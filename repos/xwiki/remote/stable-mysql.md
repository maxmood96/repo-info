## `xwiki:stable-mysql`

```console
$ docker pull xwiki@sha256:9bed383a4c1dcd1ee2fadefc266173568871a0d4aadfeb46588c1c1d5ba49213
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:82fd6331e3503b8fcd85368ee95206f838689c0ae433a0afe19d72ba16548613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.3 MB (578318774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5612765d915e9b3726e4c2a75ec28c65db005b4d561bf2a6d351baba58d1baf0`
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
ENV TOMCAT_VERSION=9.0.90
# Thu, 30 May 2024 07:53:53 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
# Thu, 30 May 2024 07:53:53 GMT
COPY dir:2df9bb79b245ef48cbc57c6bf2da0649de462747be0398216fa4b2b0a49e8963 in /usr/local/tomcat 
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
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 May 2024 07:53:53 GMT
ENV XWIKI_VERSION=16.4.0
# Thu, 30 May 2024 07:53:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.4.0
# Thu, 30 May 2024 07:53:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=ced263c074f3a61384717cafa192a52aebd34db122e9467f69af2999ab3b600e
# Thu, 30 May 2024 07:53:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 30 May 2024 07:53:53 GMT
ENV MYSQL_JDBC_VERSION=8.3.0
# Thu, 30 May 2024 07:53:53 GMT
ENV MYSQL_JDBC_SHA256=94e7fa815370cdcefed915db7f53f88445fac110f8c3818392b992ec9ee6d295
# Thu, 30 May 2024 07:53:53 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.3.0
# Thu, 30 May 2024 07:53:53 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.3.0.jar
# Thu, 30 May 2024 07:53:53 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.3.0.jar
# Thu, 30 May 2024 07:53:53 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:6824fc91fce6990f3c5461944dc0c65989a6cbc42fcaa2946a347272fb3152f7`  
		Last Modified: Fri, 21 Jun 2024 03:23:39 GMT  
		Size: 12.4 MB (12448147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54fb7690ec1a8b492dfcf461476d39b87855e7e7f6a5e4923e50d310130f5d9`  
		Last Modified: Fri, 21 Jun 2024 03:23:38 GMT  
		Size: 456.3 KB (456339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40439d1d569bf93eea762a027af4886a8863a9775307e07bd2f472f76eeaa115`  
		Last Modified: Fri, 21 Jun 2024 03:23:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3621d53c7841b39c55364d23b95dfc42d5cbf2be1138074841d1e5b67ee0fdc6`  
		Last Modified: Fri, 21 Jun 2024 04:00:56 GMT  
		Size: 178.4 MB (178436731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c840df93fe1bcbe9d78c6d2ebeec3637f03779d6a9423a7475ce2775596c6e46`  
		Last Modified: Fri, 21 Jun 2024 04:00:58 GMT  
		Size: 294.0 MB (294006571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0158f9ff62e9231974c38c0580dfe0b0619c9e5f1b0db92243ba37eaf4ef6456`  
		Last Modified: Fri, 21 Jun 2024 04:00:54 GMT  
		Size: 2.4 MB (2356951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54477b94e7817738fd6f59919dc956c4a89576b86329c02f46f889f88b9799d1`  
		Last Modified: Fri, 21 Jun 2024 04:00:54 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f773733aa16cd5afc0f8c5b0e75d120f9d23304900cf40db57e51b1968e9753c`  
		Last Modified: Fri, 21 Jun 2024 04:00:55 GMT  
		Size: 2.4 KB (2370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc013fbdd0c3bca16ec11268d227186bc5ba327642e48e3beeaa5825b7d6c0`  
		Last Modified: Fri, 21 Jun 2024 04:00:55 GMT  
		Size: 6.5 KB (6520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecac505539564ccfab47012a4039b43c943c1300ec20f91e9bf8411597cb165`  
		Last Modified: Fri, 21 Jun 2024 04:00:55 GMT  
		Size: 2.5 KB (2483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mysql` - unknown; unknown

```console
$ docker pull xwiki@sha256:6f82e277946dc44e7596e687245b81b8cb38d9faec520238084795e197774a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8928040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c798ca87929e400b37b3d6236f1b55b76eaa85d94e4a7658d8dcc4322008af`

```dockerfile
```

-	Layers:
	-	`sha256:0255a0700ccaced015f53ebac8d065bbf86417ace66a6934dcc909bbd5118198`  
		Last Modified: Fri, 21 Jun 2024 04:00:54 GMT  
		Size: 8.9 MB (8886413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e54f7c120a46620b0c1ec53caa1014d54a9b652f38d45d036d26d5333350d2`  
		Last Modified: Fri, 21 Jun 2024 04:00:53 GMT  
		Size: 41.6 KB (41627 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-mysql` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:216b253d530e14085b61e6cebf80da16b2e27758df0ed18232b4f99bcb111434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.7 MB (570731483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510814102cf9522f6eb63a2c25895e16beef470c32d7d7896cd38f4c30eda583`
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
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 May 2024 07:53:53 GMT
ENV XWIKI_VERSION=16.4.0
# Thu, 30 May 2024 07:53:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.4.0
# Thu, 30 May 2024 07:53:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=ced263c074f3a61384717cafa192a52aebd34db122e9467f69af2999ab3b600e
# Thu, 30 May 2024 07:53:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 30 May 2024 07:53:53 GMT
ENV MYSQL_JDBC_VERSION=8.3.0
# Thu, 30 May 2024 07:53:53 GMT
ENV MYSQL_JDBC_SHA256=94e7fa815370cdcefed915db7f53f88445fac110f8c3818392b992ec9ee6d295
# Thu, 30 May 2024 07:53:53 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.3.0
# Thu, 30 May 2024 07:53:53 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.3.0.jar
# Thu, 30 May 2024 07:53:53 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.3.0.jar
# Thu, 30 May 2024 07:53:53 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:46756eb83dcd276f59cb6351aa3127f42354d456260ce2f53e6fd522884960c1`  
		Last Modified: Wed, 05 Jun 2024 18:22:38 GMT  
		Size: 173.5 MB (173486358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1ffa91a697f937b80f84c11d729e83e6a082b97574cd9371bd14c168108a9c`  
		Last Modified: Wed, 05 Jun 2024 18:22:40 GMT  
		Size: 294.0 MB (294006553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e311519d8ae51213822c7322c9edd959a46928ee0d9037507d41595e105c4a0f`  
		Last Modified: Wed, 05 Jun 2024 18:22:34 GMT  
		Size: 2.4 MB (2356948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58492185937dd60172381adf98edb99cd3ee7df47b2fbc6bb2147057f3c0e5f5`  
		Last Modified: Wed, 05 Jun 2024 18:22:35 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb38e992e794cce7e518d08d6c12f953710622e0a6c3dfca1aae54fbe6d16ac`  
		Last Modified: Wed, 05 Jun 2024 18:22:35 GMT  
		Size: 2.4 KB (2373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cda403ff553cf49b659892b63caeb3d3507108b4bef310aa88983398bfd637`  
		Last Modified: Wed, 05 Jun 2024 18:22:36 GMT  
		Size: 6.5 KB (6520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccb986e5226e6dcf36fcd6f99ff49ad94fd7564501d7008529e06f552904804`  
		Last Modified: Wed, 05 Jun 2024 18:22:37 GMT  
		Size: 2.5 KB (2486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mysql` - unknown; unknown

```console
$ docker pull xwiki@sha256:0b42de30fd56c08165dfee213110dd90195283b36a93fd224bd9c42588cf3e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8929011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2276dc1a1e54f851a0179431c035b408bf9c94219d0f9e06f28d052d30c3b477`

```dockerfile
```

-	Layers:
	-	`sha256:54516ba4b09ecca4fdfe367ede833bafa5a88d5eb94d6e7b8746c57cfec7a930`  
		Last Modified: Wed, 05 Jun 2024 18:22:33 GMT  
		Size: 8.9 MB (8887046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d453153ee069b94239cccac11194a47d006e788b96b38f22bb8b793ee4c0a03f`  
		Last Modified: Wed, 05 Jun 2024 18:22:33 GMT  
		Size: 42.0 KB (41965 bytes)  
		MIME: application/vnd.in-toto+json
