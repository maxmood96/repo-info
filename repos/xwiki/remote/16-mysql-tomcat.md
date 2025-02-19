## `xwiki:16-mysql-tomcat`

```console
$ docker pull xwiki@sha256:29074ada1ab34cd218d2a86e23d1acd81d2d46de9297cd47bbdb60edfa559860
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:16-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:6fe48bb31833af8a25012d928c57c94957b215f48a65ed48c9d4925a2ececa6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.3 MB (630328942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dace3ae39d3ded7a3dce817b3c891e3fb54a6f5187508076fa0865c3283005f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 16:59:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 Jan 2025 16:59:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 16:59:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 28 Jan 2025 16:59:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 28 Jan 2025 16:59:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 Jan 2025 16:59:47 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 28 Jan 2025 16:59:47 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 16:59:47 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
WORKDIR /usr/local/tomcat
# Tue, 28 Jan 2025 16:59:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2025 16:59:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2025 16:59:47 GMT
ENV TOMCAT_MAJOR=9
# Tue, 28 Jan 2025 16:59:47 GMT
ENV TOMCAT_VERSION=9.0.100
# Tue, 28 Jan 2025 16:59:47 GMT
ENV TOMCAT_SHA512=e0b1379866d09b54f2743afb382c32a33bca9652c379467c1fa0a5b15a1b98830ae23fb1d8f96c43148844ce95b6c1d22a66db3f8efaf41f225b158c3cb71c92
# Tue, 28 Jan 2025 16:59:47 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 28 Jan 2025 16:59:47 GMT
ENTRYPOINT []
# Tue, 28 Jan 2025 16:59:47 GMT
CMD ["catalina.sh" "run"]
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 28 Jan 2025 16:59:47 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
ENV XWIKI_VERSION=16.10.3
# Tue, 28 Jan 2025 16:59:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.3
# Tue, 28 Jan 2025 16:59:47 GMT
ENV XWIKI_DOWNLOAD_SHA256=bf1f77ad964b2285c5a7695ae279bbb26f23df01ea83982bcc644af45a658405
# Tue, 28 Jan 2025 16:59:47 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_VERSION=9.1.0
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Tue, 28 Jan 2025 16:59:47 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
VOLUME [/usr/local/xwiki]
# Tue, 28 Jan 2025 16:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 16:59:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 03 Feb 2025 23:00:26 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46403441ac2f7f78a779417c34f07529970491dc25499a9f2321772006f90`  
		Last Modified: Tue, 04 Feb 2025 07:26:46 GMT  
		Size: 17.0 MB (16962484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f4ee04af8786c03105915946c5bf4d14aa3901749a6e7e6f54d94d23bdab7c`  
		Last Modified: Tue, 04 Feb 2025 07:17:34 GMT  
		Size: 47.0 MB (46952663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3da94a33fa1bc27770bb6588ff1cbef17c2cb37284348caf2ac38adc859173a`  
		Last Modified: Tue, 04 Feb 2025 07:23:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03e4717322c01c3bff3cfcbbfebaf8330f4f418957eac816b99ca0494b7bbd8`  
		Last Modified: Tue, 04 Feb 2025 07:15:16 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905cb609a532e57eb7d137a61a15305430b94f7c17e544c137e7d3beb6b367d0`  
		Last Modified: Wed, 19 Feb 2025 01:08:36 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72b585023bd07955738df8ad3ba67700d5ec22f2fd530cf30a7a48f95b68b03`  
		Last Modified: Wed, 19 Feb 2025 01:08:38 GMT  
		Size: 13.5 MB (13459670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eb6669c47a8716893b10087861481e0cd7a59eceae2d19ace71a169c108b4f`  
		Last Modified: Wed, 19 Feb 2025 01:08:41 GMT  
		Size: 12.8 MB (12832316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f994ad569330e835f183b7ad250b33323f25776e9ae019bbfd11f24aa593474`  
		Last Modified: Wed, 19 Feb 2025 04:10:25 GMT  
		Size: 191.2 MB (191195862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5eaa81e1572f29c2f3c1dad275fa9654d4063dadeca19022996ef83d7862313`  
		Last Modified: Wed, 19 Feb 2025 04:10:29 GMT  
		Size: 316.7 MB (316721987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293fe125f708daa296231cc64fd2d28990206dfe359620580f5341824e5425f5`  
		Last Modified: Wed, 19 Feb 2025 02:10:20 GMT  
		Size: 2.4 MB (2434180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0b089a193e381bf7b059ccd649875a5d329e11315184fd391b170bb4b12bdb`  
		Last Modified: Wed, 19 Feb 2025 02:10:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcca3793391d6b3d78ec0586d7887d02e332af57af0b004fa6229b5fceb7333d`  
		Last Modified: Wed, 19 Feb 2025 02:10:15 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744cd011a86b7e89253889e87419f997285d5a943ecb2a39366ed132219f132d`  
		Last Modified: Wed, 19 Feb 2025 02:10:15 GMT  
		Size: 6.6 KB (6622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4d4e148ffd104978aaec4a199e9c033d4ee7386eb67809b48d1679c4490352`  
		Last Modified: Wed, 19 Feb 2025 02:10:14 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:30c0876b528df7ac584d32b2db2b9687ce77772cc27c4a6d7062bd8f7e3c7f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3e1859560c5dff0f877d21789c72cee175eb1b53c7c19ed390f0ecc895b88e`

```dockerfile
```

-	Layers:
	-	`sha256:6290d970e7427fb03b0844535c2c89b98c446225e2cd1c3d75ea06917c608c99`  
		Last Modified: Wed, 19 Feb 2025 04:07:45 GMT  
		Size: 8.8 MB (8754210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dbe4f6a1459f6368ac4211abd728e12704080e3427a1d02963edac089ce5530`  
		Last Modified: Wed, 19 Feb 2025 04:07:45 GMT  
		Size: 41.5 KB (41547 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:16-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:f07378a9948a3bdfbd01a593fd75f87a12591c2ed5b6beb38eda77fd0e2195d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.4 MB (626442348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c790065c53ca985dac3bf3561afcd9527ea7099afad871ce64b8d4fd50c510`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2025 16:59:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 Jan 2025 16:59:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 16:59:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 28 Jan 2025 16:59:47 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Tue, 28 Jan 2025 16:59:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 28 Jan 2025 16:59:47 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 28 Jan 2025 16:59:47 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2025 16:59:47 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
WORKDIR /usr/local/tomcat
# Tue, 28 Jan 2025 16:59:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2025 16:59:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jan 2025 16:59:47 GMT
ENV TOMCAT_MAJOR=9
# Tue, 28 Jan 2025 16:59:47 GMT
ENV TOMCAT_VERSION=9.0.99
# Tue, 28 Jan 2025 16:59:47 GMT
ENV TOMCAT_SHA512=bf406b3e288e1732d82d08f54e160095451a6cc969f72adf395c074d6d08893ef1ccd2afcd55f01ca8e54131f587c88055832f36330a1ede0cc2f84440cf54df
# Tue, 28 Jan 2025 16:59:47 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 28 Jan 2025 16:59:47 GMT
ENTRYPOINT []
# Tue, 28 Jan 2025 16:59:47 GMT
CMD ["catalina.sh" "run"]
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 28 Jan 2025 16:59:47 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 28 Jan 2025 16:59:47 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
ENV XWIKI_VERSION=16.10.3
# Tue, 28 Jan 2025 16:59:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.3
# Tue, 28 Jan 2025 16:59:47 GMT
ENV XWIKI_DOWNLOAD_SHA256=bf1f77ad964b2285c5a7695ae279bbb26f23df01ea83982bcc644af45a658405
# Tue, 28 Jan 2025 16:59:47 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_VERSION=9.1.0
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Tue, 28 Jan 2025 16:59:47 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 28 Jan 2025 16:59:47 GMT
VOLUME [/usr/local/xwiki]
# Tue, 28 Jan 2025 16:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 16:59:47 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Tue, 04 Feb 2025 06:04:53 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff9d366153192dfa76bdef5a62c6b04854405cf3bc86816a7e84cc79dc5744`  
		Last Modified: Tue, 04 Feb 2025 10:15:57 GMT  
		Size: 17.0 MB (16977404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646bfcab524deb99e432714a7a838a5f6b98e7a47faa95240fd0168282b7a09d`  
		Last Modified: Tue, 04 Feb 2025 13:15:37 GMT  
		Size: 46.5 MB (46463804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01542aefa0dab0f76d7350aedf449d8ea2544f3d8946d83898cc3f5f2a2bcf8`  
		Last Modified: Tue, 04 Feb 2025 14:59:44 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80fc1fa5adda672381a8947ac048a52838f4e7b8997a299cf54cb5e941da78`  
		Last Modified: Tue, 04 Feb 2025 14:04:57 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce464ad2f9aa344c63dd6298b049e6735ab8811a212af369191b7fa918ee6e7`  
		Last Modified: Wed, 05 Feb 2025 08:33:17 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2bb3d2ad3e4cdde9a094bed962f4f1d29b7d3ecd58f2bb1f9bbb0e5a5e81e6`  
		Last Modified: Tue, 11 Feb 2025 05:26:47 GMT  
		Size: 13.5 MB (13466521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8063526302da3e6e692d7c7dd0789db5ddc973d1c9bca57c530c6b28398f4c`  
		Last Modified: Tue, 11 Feb 2025 05:26:46 GMT  
		Size: 12.6 MB (12601542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee194781a4eee0ddd42b7edd1a6accab6df09078dd4ee0b3b907a9f03d691cc`  
		Last Modified: Tue, 11 Feb 2025 17:29:05 GMT  
		Size: 188.9 MB (188867828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4e8e66ceb9f14cba7c20a3944abda195b375452a8f6b2e95656b9d0b547534`  
		Last Modified: Tue, 11 Feb 2025 21:59:21 GMT  
		Size: 316.7 MB (316721988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c7e63e2d73075b842bfc0c1fd201d33aa435e6d84fda785903af3d225ebde5`  
		Last Modified: Tue, 11 Feb 2025 22:02:56 GMT  
		Size: 2.4 MB (2434176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1965f38563fa433f7eda65688de4c7f9217f6f513002a1505745e8a6e28ddc`  
		Last Modified: Tue, 11 Feb 2025 22:50:21 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d7b432a35333a67c9699fc66fca215b8200eeb8a79d677c8b98d9a3b18058c`  
		Last Modified: Tue, 11 Feb 2025 22:01:18 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cde12206e7fcdf0a837e30c581ec6ed844a86be9ec07a33af0fb7140dcf6211`  
		Last Modified: Tue, 11 Feb 2025 23:03:45 GMT  
		Size: 6.6 KB (6623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8303bb6ffb2d65892dff67b9e8c02fc198e7d6495b19b4d956b1e5c4cb31ce1`  
		Last Modified: Tue, 11 Feb 2025 22:01:22 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:c5369d1e2f42e54c5d1897e46c09fd7682f3b5e3ff7e23fd5fb09249e7e88c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8796694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2926346b3c2498bf54ba992c02a8d43016f2889b771a2e605c1dea07e04f2f4`

```dockerfile
```

-	Layers:
	-	`sha256:46e650be62b44b41d15dc813b5d2118fae1b48205087ed7f04ec1c2e36031907`  
		Last Modified: Wed, 19 Feb 2025 04:07:54 GMT  
		Size: 8.8 MB (8754943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fea8bb1c78b74159a5eaf3f8da041f2600b918d068e9bfd6f711706e2a98208`  
		Last Modified: Wed, 19 Feb 2025 04:07:55 GMT  
		Size: 41.8 KB (41751 bytes)  
		MIME: application/vnd.in-toto+json
