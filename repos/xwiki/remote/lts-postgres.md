## `xwiki:lts-postgres`

```console
$ docker pull xwiki@sha256:43f7e2ff8c570a6c246cdb1032de863933dc8784ffcf45791f245c43afefc48d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:a4cb9e50fd08f0ed7b10b78e60bf392962a3b3d46071f517e19dfc87d72a8f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.9 MB (590886105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5014255cbf408bdfc339fffcc1d5da9c4a9dbcc638618e67057292f6d57041a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 27 Mar 2024 12:37:20 GMT
ARG RELEASE
# Wed, 27 Mar 2024 12:37:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 27 Mar 2024 12:37:20 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 27 Mar 2024 12:37:20 GMT
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
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 27 Mar 2024 12:37:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
ENV TOMCAT_VERSION=9.0.88
# Wed, 27 Mar 2024 12:37:20 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Wed, 27 Mar 2024 12:37:20 GMT
COPY dir:321162520ae1ac7bf5a33989c20e77ddafcbac999c2a428a5a1e688f9f492091 in /usr/local/tomcat 
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
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dddff65ed2408fb8512cf4a5e475bc56396102dc76b9968c1f68a06414767b`  
		Last Modified: Tue, 16 Apr 2024 04:03:41 GMT  
		Size: 12.9 MB (12905145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9237e630c9059227029d3a2c6320abc1ad352451cdbba394df5cea43f717a40`  
		Last Modified: Wed, 24 Apr 2024 19:15:21 GMT  
		Size: 47.3 MB (47256245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9806fc018a0ccea71d8dd3aea7840b69561254fea0089c8986197083008a1fa8`  
		Last Modified: Wed, 24 Apr 2024 19:15:14 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1777ab1b0fade4b94003ca25e3c169cdcc094ee8f05a46100e143b407d556ef1`  
		Last Modified: Wed, 24 Apr 2024 19:15:14 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c470bfc7eb097a1cd4c0353ab8e8d2b23e5f252c7236d0aae4311d227f3a9a`  
		Last Modified: Wed, 24 Apr 2024 23:32:17 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1b6745753793cfde5d78cefc4b83ef85e582f35783a0e182731b678a5317a4`  
		Last Modified: Wed, 24 Apr 2024 23:35:08 GMT  
		Size: 12.4 MB (12423152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdee809697513d49fdc8f4055f1a0f8d7ae98af2f347a3454f57ca234c02e8ca`  
		Last Modified: Wed, 24 Apr 2024 23:35:07 GMT  
		Size: 456.3 KB (456327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b4e246cd9e60aadc9038dec915e4f0b147dc7815e881b8a55d60c1ced25e2`  
		Last Modified: Wed, 24 Apr 2024 23:35:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f5f3b0a9690f2d917e477e3eff46ca6039ce5424fa936e398fe46cf4c7c39b`  
		Last Modified: Thu, 25 Apr 2024 00:57:15 GMT  
		Size: 179.4 MB (179369002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380a50530ef472e61f8f2f15cf17458e1716b3a5ed3b32b14bca8c376574a491`  
		Last Modified: Thu, 25 Apr 2024 00:57:18 GMT  
		Size: 307.0 MB (307010854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb3d0c214508adab350187371f61b638d44c7588c559f1d8eacaed1704b6716`  
		Last Modified: Thu, 25 Apr 2024 00:57:13 GMT  
		Size: 1.0 MB (1011768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f621bbac9cb72347a506ae9469ed7e9621d979de5b500c2b2bc243fa203f59f`  
		Last Modified: Thu, 25 Apr 2024 00:57:13 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d8c3cc8ded8bce60d96eac06617d48ff71f8815394f1cb9b6197091a8919f6`  
		Last Modified: Thu, 25 Apr 2024 00:57:14 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c0c11de8527303c42d24efd860dbcff9b8cc44ae1e4c3a2aa2ae22cffb01c1`  
		Last Modified: Thu, 25 Apr 2024 00:57:14 GMT  
		Size: 6.4 KB (6414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c05d9ef0dec566f1b4c17fd2f13a3e10a1b4bcb69d5aed31c2cf31a58599182`  
		Last Modified: Thu, 25 Apr 2024 00:57:15 GMT  
		Size: 2.4 KB (2429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:d53b17a416f208188aea269616f93008e063c45095c9a35c795ba1e0b460bcc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8944753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5088a4c88724e2e8f00971db2ca87eb7b8f87324f0a862204323f086cbf56e6e`

```dockerfile
```

-	Layers:
	-	`sha256:15bb7eb055aa92be53dd83a4d30d40a03a5a7e063624d38989bd6d5e045bdcf2`  
		Last Modified: Thu, 25 Apr 2024 00:57:13 GMT  
		Size: 8.9 MB (8903276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98321aa7deafa8a5eb1f412b46c38cca367bdf8feb572bbd706f8bb5eb0a0829`  
		Last Modified: Thu, 25 Apr 2024 00:57:13 GMT  
		Size: 41.5 KB (41477 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:0c9781687566e4fad463dacc601dff7bf4d20c09f265bcb634c4061bce62cf76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.2 MB (583232370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883d6305898a1fd5188ec93f3e9a6d1f15de4c1c2f3634412fcb5c99dc24eb0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 27 Mar 2024 12:37:20 GMT
ARG RELEASE
# Wed, 27 Mar 2024 12:37:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 27 Mar 2024 12:37:20 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 27 Mar 2024 12:37:20 GMT
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
ENV TOMCAT_VERSION=9.0.88
# Wed, 27 Mar 2024 12:37:20 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Wed, 27 Mar 2024 12:37:20 GMT
COPY dir:ba3e33ed23284380cd070ee082efc56bd4e069281d5d61e5fd722562420f4b69 in /usr/local/tomcat 
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
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62af4570e03cd18721264dca7618ad8bfe7fc52046caf98dd92dbd19a11ae3bf`  
		Last Modified: Tue, 16 Apr 2024 02:55:33 GMT  
		Size: 12.8 MB (12847096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9331e6965ccd210b6fd21419523ddc450c72626bd5ca5b0672bb8c0a1cb596ad`  
		Last Modified: Tue, 16 Apr 2024 02:58:28 GMT  
		Size: 46.6 MB (46639080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af58a4038ec765397b1ef467a9d6da1d336353f28df5cc32c5516aa471e4bb4e`  
		Last Modified: Tue, 16 Apr 2024 02:58:22 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8322d102061cd226429f20602d322142091650639e707df1fc051fbc869c138e`  
		Last Modified: Tue, 16 Apr 2024 02:58:22 GMT  
		Size: 732.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e02da29e0dc36cfae157626956d709192018538adafffbf45caf04e6a5125bc`  
		Last Modified: Tue, 16 Apr 2024 08:41:00 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05628a793e4710e8b8b6ff5020fc155e6fb4b9f57abb6a53107c4a9063206fd2`  
		Last Modified: Wed, 17 Apr 2024 01:03:32 GMT  
		Size: 12.4 MB (12430998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80252592221cd05095a4d105203d89f19cca649dfcbdd8fa72e81b2032a32a25`  
		Last Modified: Wed, 17 Apr 2024 01:03:31 GMT  
		Size: 455.7 KB (455662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db2f7057439ac6773bf8cae77e2fb8b772c8eb0dbcc9e4ec133d1d9642a32b1`  
		Last Modified: Wed, 17 Apr 2024 01:03:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a534a520fb36d08e2fbb6e0490ec5a2a853cedbeba3f6e08838dc1ca417b7c04`  
		Last Modified: Thu, 18 Apr 2024 18:49:16 GMT  
		Size: 174.4 MB (174422729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f50ac4f4d97d9a7e66c0e0f3aeb762b5402db15c2cc7a16c293eeb46291bf97`  
		Last Modified: Thu, 18 Apr 2024 18:50:31 GMT  
		Size: 307.0 MB (307010896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9840fc709e522a24b563a164cbb23cb971874be01b56c027dd6217fac3ca6ee0`  
		Last Modified: Thu, 18 Apr 2024 18:50:24 GMT  
		Size: 1.0 MB (1011767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc763531717b409ef830bb873f9afe21c865b3c153a2e8aee724fa07b2ffdee2`  
		Last Modified: Thu, 18 Apr 2024 18:50:24 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2baaa6c3999b3b55dbf74d2e53a6bcdb6ac312347fe918514fb6c19c3bb06f7b`  
		Last Modified: Thu, 18 Apr 2024 18:50:24 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e39009313f71a7e8afd770386463239294a65b9364aabfc36f1f3bafba5c19`  
		Last Modified: Thu, 18 Apr 2024 18:50:25 GMT  
		Size: 6.4 KB (6414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b757b149f7331dd0297be01ee865409c63a554761f66c5097368b4e9a3312d7a`  
		Last Modified: Thu, 18 Apr 2024 18:50:25 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:4e26794c9733b566c266c922b05c6dee15840771c969a0f8ea6de1aaa85b1ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8943806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c0668f46ea659aafbb3998baae2698b0dd6cd044486b2adf71c3915b6d1186`

```dockerfile
```

-	Layers:
	-	`sha256:547afdd7ef005716263db880b07ac02c37136972e3306b5b8606b37b30128794`  
		Last Modified: Thu, 18 Apr 2024 18:50:24 GMT  
		Size: 8.9 MB (8903783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:341af70055656c7e47efb25156765723d94138b7a79d53808c63b684657adf0e`  
		Last Modified: Thu, 18 Apr 2024 18:50:23 GMT  
		Size: 40.0 KB (40023 bytes)  
		MIME: application/vnd.in-toto+json
