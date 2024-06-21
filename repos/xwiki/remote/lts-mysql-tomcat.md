## `xwiki:lts-mysql-tomcat`

```console
$ docker pull xwiki@sha256:8bdfb4fc77e5d078ed4f5482e9ebd0523fc0e758fd6b499d432bf7bdce313bf9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7df33b7d50bcc0d9d9a92b67dd884ee254e1c436102c4775bea923988c112b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.3 MB (591260428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2487dad97a820c29b9e0b91d0b62aa646147cd09c79adfc2dab70444b9e6df9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 27 May 2024 13:30:04 GMT
ARG RELEASE
# Mon, 27 May 2024 13:30:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 May 2024 13:30:04 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 27 May 2024 13:30:04 GMT
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
# Mon, 27 May 2024 13:30:04 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 27 May 2024 13:30:04 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 May 2024 13:30:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 27 May 2024 13:30:04 GMT
WORKDIR /usr/local/tomcat
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 27 May 2024 13:30:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 27 May 2024 13:30:04 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_MAJOR=9
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_VERSION=9.0.90
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
# Mon, 27 May 2024 13:30:04 GMT
COPY dir:2df9bb79b245ef48cbc57c6bf2da0649de462747be0398216fa4b2b0a49e8963 in /usr/local/tomcat 
# Mon, 27 May 2024 13:30:04 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 27 May 2024 13:30:04 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 27 May 2024 13:30:04 GMT
EXPOSE 8080
# Mon, 27 May 2024 13:30:04 GMT
ENTRYPOINT []
# Mon, 27 May 2024 13:30:04 GMT
CMD ["catalina.sh" "run"]
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 27 May 2024 13:30:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_VERSION=15.10.10
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.10
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_DOWNLOAD_SHA256=fda9b5b4c1f471dc47e8cf2cb72b7550dbe6d6772887201be94c522a13b6078e
# Mon, 27 May 2024 13:30:04 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 27 May 2024 13:30:04 GMT
ENV MYSQL_JDBC_VERSION=8.3.0
# Mon, 27 May 2024 13:30:04 GMT
ENV MYSQL_JDBC_SHA256=94e7fa815370cdcefed915db7f53f88445fac110f8c3818392b992ec9ee6d295
# Mon, 27 May 2024 13:30:04 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.3.0
# Mon, 27 May 2024 13:30:04 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.3.0.jar
# Mon, 27 May 2024 13:30:04 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.3.0.jar
# Mon, 27 May 2024 13:30:04 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 27 May 2024 13:30:04 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 27 May 2024 13:30:04 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 27 May 2024 13:30:04 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 27 May 2024 13:30:04 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 27 May 2024 13:30:04 GMT
VOLUME [/usr/local/xwiki]
# Mon, 27 May 2024 13:30:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 May 2024 13:30:04 GMT
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
	-	`sha256:3289f0dc9efb9a233e7c32866a8007a228e6cc682c3873ec69060c9211202303`  
		Last Modified: Fri, 21 Jun 2024 04:00:55 GMT  
		Size: 178.4 MB (178436261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a9b3d758ebd51c2a59242adaa19b1f3442ae708b5a6aad0505b16f1195f70c`  
		Last Modified: Fri, 21 Jun 2024 04:00:56 GMT  
		Size: 306.9 MB (306948792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25648a651d3066bce017c400131d284dcd5c6f28808269446da02598a1a32a77`  
		Last Modified: Fri, 21 Jun 2024 04:00:52 GMT  
		Size: 2.4 MB (2356958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38d2684f370fae4866465404e8b68caec0484a733155cb23118deacf2c10b92`  
		Last Modified: Fri, 21 Jun 2024 04:00:52 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ea67c89776716c417554bd1630c8fb9f39af82908aa7048d7f1e9e3b50a0c3`  
		Last Modified: Fri, 21 Jun 2024 04:00:53 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96da76c14da9c9d08e6a1c1e9fde24bdda58094544b63c4e07558dc833d01330`  
		Last Modified: Fri, 21 Jun 2024 04:00:53 GMT  
		Size: 6.4 KB (6416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a18f13d7b8f5ef05cef300b92b3ed807899ffffe10d32c68d17d9fb55fbed7e`  
		Last Modified: Fri, 21 Jun 2024 04:00:54 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:ada743c6a9f67ac4698e703e76f641009b44ee00c35d1b584e93cadd2acd035b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8935098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5db31b5352cafa92402c7155ac7dbd16e03eaa312702575809a3abd0572bf11`

```dockerfile
```

-	Layers:
	-	`sha256:4755ce286b1083883dd8fd72938e8e88ab6fd55dd9796587bd17a0cb673034c2`  
		Last Modified: Fri, 21 Jun 2024 04:00:52 GMT  
		Size: 8.9 MB (8894065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e84bdb48a77cd3fae7676cdfc03038ac114f776f87e086f6a675993976116e57`  
		Last Modified: Fri, 21 Jun 2024 04:00:52 GMT  
		Size: 41.0 KB (41033 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:a4d4a5f7d097a1b6de1fc9465ebf0821287990de3ef3d0314888ea5204e53c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.7 MB (583683923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540ad8fb6a5868ab2de8ea0d118bf086ad8cd944babf29e460239a33219c3ae3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 27 May 2024 13:30:04 GMT
ARG RELEASE
# Mon, 27 May 2024 13:30:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 May 2024 13:30:04 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 27 May 2024 13:30:04 GMT
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
# Mon, 27 May 2024 13:30:04 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 27 May 2024 13:30:04 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 May 2024 13:30:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 27 May 2024 13:30:04 GMT
WORKDIR /usr/local/tomcat
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 27 May 2024 13:30:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 27 May 2024 13:30:04 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_MAJOR=9
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_VERSION=9.0.90
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
# Mon, 27 May 2024 13:30:04 GMT
COPY dir:f1c8ea4bbef7f8fcbb6baccde13eb9f00f71605c817e41238c6fdc3ab9036a00 in /usr/local/tomcat 
# Mon, 27 May 2024 13:30:04 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 27 May 2024 13:30:04 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 27 May 2024 13:30:04 GMT
EXPOSE 8080
# Mon, 27 May 2024 13:30:04 GMT
ENTRYPOINT []
# Mon, 27 May 2024 13:30:04 GMT
CMD ["catalina.sh" "run"]
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 27 May 2024 13:30:04 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 27 May 2024 13:30:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_VERSION=15.10.10
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.10
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_DOWNLOAD_SHA256=fda9b5b4c1f471dc47e8cf2cb72b7550dbe6d6772887201be94c522a13b6078e
# Mon, 27 May 2024 13:30:04 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 27 May 2024 13:30:04 GMT
ENV MYSQL_JDBC_VERSION=8.3.0
# Mon, 27 May 2024 13:30:04 GMT
ENV MYSQL_JDBC_SHA256=94e7fa815370cdcefed915db7f53f88445fac110f8c3818392b992ec9ee6d295
# Mon, 27 May 2024 13:30:04 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.3.0
# Mon, 27 May 2024 13:30:04 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.3.0.jar
# Mon, 27 May 2024 13:30:04 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.3.0.jar
# Mon, 27 May 2024 13:30:04 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 27 May 2024 13:30:04 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 27 May 2024 13:30:04 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 27 May 2024 13:30:04 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 27 May 2024 13:30:04 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 27 May 2024 13:30:04 GMT
VOLUME [/usr/local/xwiki]
# Mon, 27 May 2024 13:30:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 May 2024 13:30:04 GMT
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
	-	`sha256:a31be934b42c9438aabd8a3bf297a8128769973fb30856ff874bf74cfdbec92c`  
		Last Modified: Fri, 21 Jun 2024 01:40:29 GMT  
		Size: 12.5 MB (12454566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583af122ce35b5b703ea987b6b2abaf0bb387ca16647aff6f5743631487a2182`  
		Last Modified: Fri, 21 Jun 2024 01:40:28 GMT  
		Size: 456.8 KB (456818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51db09b79e04b8e82902c0ad98a2ce9d236e0dab599a4eaab3f45332e4f844c`  
		Last Modified: Fri, 21 Jun 2024 01:40:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3644095e00f1a3c270391eaad23c2370ee890d62b70f938a76c7b52c42afa90c`  
		Last Modified: Fri, 21 Jun 2024 12:01:56 GMT  
		Size: 173.5 MB (173486544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e1827967fb8596f0e2232b304e2933505c121409964899ab9d7c35c5d9147a`  
		Last Modified: Fri, 21 Jun 2024 12:05:48 GMT  
		Size: 306.9 MB (306948748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450ef375f17b56ab10522a8ff494a75af6baf70fe420d9a7c94688bc437b85f5`  
		Last Modified: Fri, 21 Jun 2024 12:05:42 GMT  
		Size: 2.4 MB (2356943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2388420b9462d05ca10941c5696c26597d216e9b9598bb76f97270d9e2b2552`  
		Last Modified: Fri, 21 Jun 2024 12:05:41 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486a5f5713e509ff20d22fbfa734ee846a581c2ac81d106c99ce6ebbc0e351e7`  
		Last Modified: Fri, 21 Jun 2024 12:05:41 GMT  
		Size: 2.4 KB (2367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153fd05d8136ae42b040d4082068de0685ae09b72c79a47370937b80828267da`  
		Last Modified: Fri, 21 Jun 2024 12:05:42 GMT  
		Size: 6.4 KB (6412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18032744e7401b752f644e94deafe90c2bbff7e8dfa923c85c9617bb6a21765`  
		Last Modified: Fri, 21 Jun 2024 12:05:42 GMT  
		Size: 2.5 KB (2479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:b249ca47efd23d49bb1240a5f0606fd3a3d4f72b3b45fb7239c9f230fa4dfcb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8936071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19116529b8bc10bed4870a18cb700df0c280aaf0b197e7beb6f4834429f8e288`

```dockerfile
```

-	Layers:
	-	`sha256:17b39f280bbed0a50febf2f8d7f1552bd18dd2673249fe85712195df7bf4dd7c`  
		Last Modified: Fri, 21 Jun 2024 12:05:41 GMT  
		Size: 8.9 MB (8894675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590e981b17c0db6b67034187451b3d7a5fdf437fe90168494edf9c89c43c0bd7`  
		Last Modified: Fri, 21 Jun 2024 12:05:41 GMT  
		Size: 41.4 KB (41396 bytes)  
		MIME: application/vnd.in-toto+json
