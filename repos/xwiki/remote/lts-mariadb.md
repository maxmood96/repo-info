## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:46930008df6904f932f2ae36c67b84d26c2ffdfefc017dec29b7699c6df45299
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:e20296e9b3abc3278e15e4c2230ccb0f197f8138ec4b303f4a1a7210f3a2a46f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.4 MB (617360440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e49f7fb74221487eb045854455cd32c5ff85fb68693d994139cd3e701f191b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        arm64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        armhf)          ESUM='7ac439bce4d5ecddb250b31401b1c1a6da2762f51652eafedd53584a0d9e3130';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64el)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        riscv64)          ESUM='2f77e44aa9fec9cf35b0b1fd492055e7fec0a3ea4d4338def6b42bd46d485e02';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
WORKDIR /usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_MAJOR=9
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_VERSION=9.0.98
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Mon, 06 Jan 2025 23:11:14 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT []
# Mon, 06 Jan 2025 23:11:14 GMT
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
ENV MARIADB_JDBC_VERSION=3.5.1
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MARIADB_JDBC_SHA256=50a50c4a3c13c30dfbd40587f7ad9a496197d285ede0948641d9eee68fdf2106
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.1
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.1.jar
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.1.jar
# Tue, 28 Jan 2025 16:59:47 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6659d18e8896e1d5defd62b936073b270004ee57f721ba7cb7d19ca9a010fb4`  
		Last Modified: Fri, 31 Jan 2025 01:30:49 GMT  
		Size: 17.0 MB (16962267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7151ca38abad3b7a010b992fc48b85782e128c737137eefc7bd906e864bee5bb`  
		Last Modified: Fri, 31 Jan 2025 01:30:49 GMT  
		Size: 47.0 MB (46952673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f3aed9903781edc98b2a47d0562884e8491642cf6ca7e7a2d1535881803615`  
		Last Modified: Fri, 31 Jan 2025 01:30:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85a87ebd918b1d1d1319c5dc4b706d184344dd9047d1e208d0801b3fe3338d7`  
		Last Modified: Fri, 31 Jan 2025 01:30:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03a6d0d268927364f2a7b0771303048272678866676efe8aa5a04ea7dcee63b`  
		Last Modified: Fri, 31 Jan 2025 03:12:02 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328536f3783a30b58beb39b9edfa52ef26214205978d47d4e9246346590f25f4`  
		Last Modified: Fri, 31 Jan 2025 03:12:02 GMT  
		Size: 13.4 MB (13440341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4956c28c3c94179981072b6ee0e4d71500999f91cb4257a57e048e1d3b957262`  
		Last Modified: Fri, 31 Jan 2025 03:12:02 GMT  
		Size: 1.6 MB (1642528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1952e9c8408f4c905ef6803a09e7887379d7f018429838f88b3c0843ede5d1b`  
		Last Modified: Fri, 31 Jan 2025 04:10:17 GMT  
		Size: 191.2 MB (191191972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89531d6724341143c37dab379f0db1dbbe4913e15303fbfaf4c369c252acd68`  
		Last Modified: Fri, 31 Jan 2025 04:10:18 GMT  
		Size: 316.7 MB (316722041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9ea4dc363b289dca236611b86712f426849a2c7e584e79af2bd0a69a8bb5db`  
		Last Modified: Fri, 31 Jan 2025 04:10:14 GMT  
		Size: 681.3 KB (681256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d153c4ec5c6f16fc15e281d1a42360e40b1ee83279d37a6b43c532eca9b22d6`  
		Last Modified: Fri, 31 Jan 2025 04:10:14 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251e7781ff8c1c49b1adeba311069704b0e49fb6184c9217f17bcbda01cabf74`  
		Last Modified: Fri, 31 Jan 2025 04:10:14 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d275319bc912b1abae74e10ed9222e542862bf7ab5c71d1b5039d16a36d8d7`  
		Last Modified: Fri, 31 Jan 2025 04:10:15 GMT  
		Size: 6.6 KB (6623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161f31248acc033e3294d570e632678e3285d94c33d1bb569a1ce1ce6d91e465`  
		Last Modified: Fri, 31 Jan 2025 04:10:15 GMT  
		Size: 2.5 KB (2473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:7f54f633c5dd5bcb69172bbb575b49f25862d031e60757c3b420b84978af8b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8792620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c6bfc3df7676990deb33f0e2adabe3b3b608a089621049d224e4f07b8d53aa`

```dockerfile
```

-	Layers:
	-	`sha256:e5e8a279e4dc2c14495ccfd8c553f8f74f62b03899ddecdc0b06afc3d69e90b1`  
		Last Modified: Fri, 31 Jan 2025 04:10:14 GMT  
		Size: 8.8 MB (8752130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42e4b5123413e59b25912dd72b8ea854d10baac3864867320036ba16f7ef32a3`  
		Last Modified: Fri, 31 Jan 2025 04:10:13 GMT  
		Size: 40.5 KB (40490 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:84220ecfba689814c5864ff733d4f8d83c0963c6d8955b9a60f4f821dda17cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.7 MB (613704572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e1fa6aeb9dee6b4683ab8ae1fee33c9f0d77cbad360f588c8bf13282ddceb2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 06 Jan 2025 23:11:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:11:14 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
WORKDIR /usr/local/tomcat
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_MAJOR=9
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_VERSION=9.0.98
# Mon, 06 Jan 2025 23:11:14 GMT
ENV TOMCAT_SHA512=07d87286e8ee84bb291069c596cf36233e56a14e3ecb6d65eea0fa7c7042ce5e75f5db31f210b96b6b25b80b34e626dd26c5a6ed5c052384a8587d62658b5e16
# Mon, 06 Jan 2025 23:11:14 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 06 Jan 2025 23:11:14 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 06 Jan 2025 23:11:14 GMT
ENTRYPOINT []
# Mon, 06 Jan 2025 23:11:14 GMT
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
ENV MARIADB_JDBC_VERSION=3.5.1
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MARIADB_JDBC_SHA256=50a50c4a3c13c30dfbd40587f7ad9a496197d285ede0948641d9eee68fdf2106
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.1
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.1.jar
# Tue, 28 Jan 2025 16:59:47 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.1.jar
# Tue, 28 Jan 2025 16:59:47 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370f8a7b7cf214f61cc1a2546f38e47ba749cb698659b51aa07e70fcecbd7e2f`  
		Last Modified: Wed, 22 Jan 2025 20:53:10 GMT  
		Size: 17.0 MB (16982856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdecf092a77e3bcc60bf2a2f0d9bb37477afb75ca7c9781f98a76d3722450717`  
		Last Modified: Wed, 22 Jan 2025 21:06:49 GMT  
		Size: 46.4 MB (46430926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46396c1812fff3f42c7bce2cfc29c910045b7fd281e96d27491bddc27a25f4a5`  
		Last Modified: Wed, 22 Jan 2025 21:06:48 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1d9c149d4e66dbbc5d2f77d496f834696346b93887893c1a1b4cd3dbc46ff9`  
		Last Modified: Wed, 22 Jan 2025 21:06:48 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e97be03f8c1ceae9246d08d9cad75d685289df723a3277870c2dfec2f67ff8b`  
		Last Modified: Thu, 23 Jan 2025 03:46:36 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c972788f94ae2ef95aac9270d0d354a6bfc6ef8a362fada80d182525b094aa`  
		Last Modified: Thu, 23 Jan 2025 03:50:46 GMT  
		Size: 13.5 MB (13450951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997c07d109b8193850dba25ad47cb23b7a65987d049595756721eda0e132646a`  
		Last Modified: Thu, 23 Jan 2025 03:50:46 GMT  
		Size: 1.7 MB (1721637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd1006b4347ffe00c828718072676317818810ed8591f616b3d37efbdf98f94`  
		Last Modified: Thu, 23 Jan 2025 04:50:49 GMT  
		Size: 188.8 MB (188806889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc498f2e17d244967b25526d2e1968e716bdc0cabc5ea6b54f64bb46f83ae57c`  
		Last Modified: Tue, 28 Jan 2025 19:29:03 GMT  
		Size: 316.7 MB (316721983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a452e9ba966354a266be244e821f37c6ecaea1a5bf298a19f5f54b0c3c569a9c`  
		Last Modified: Tue, 28 Jan 2025 19:30:29 GMT  
		Size: 681.3 KB (681259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8257959e97655018f4de339a01a90c6053b59af1de07417e72806b3e545c48`  
		Last Modified: Tue, 28 Jan 2025 19:30:29 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754b54165ed0c1bb9f80e6f150b9067b261a16576ae69731dce00c3fb47e2a62`  
		Last Modified: Tue, 28 Jan 2025 19:30:29 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cfb81eddd4ebfcddeb3a2160f0c56d9a4c34baffe086c2bce8db400ad2dadf`  
		Last Modified: Tue, 28 Jan 2025 19:30:29 GMT  
		Size: 6.6 KB (6623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff74b395931b85521fb2eb884c87a9367ee042a7e8ecae9181dd2f7cdcdb2f5a`  
		Last Modified: Tue, 28 Jan 2025 19:30:29 GMT  
		Size: 2.5 KB (2478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:dff51a549547c2bb3189ca38e830397d7ecba97b0471b195799aff3bce786fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8796012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6b8a2c0caa1961c557dc62894ae1ccd9de74fa3ed718a99c367cdba0df1e8d`

```dockerfile
```

-	Layers:
	-	`sha256:de40786aa5a9bde8aa7dce9cd08f7b053cdf6ddf57d98b05747610cb00aad5cd`  
		Last Modified: Tue, 28 Jan 2025 19:30:28 GMT  
		Size: 8.8 MB (8754371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfeef81a792dea67d56c46a690a42a5b44647dc75546378d879584f6ab3a5c3`  
		Last Modified: Tue, 28 Jan 2025 19:30:28 GMT  
		Size: 41.6 KB (41641 bytes)  
		MIME: application/vnd.in-toto+json
