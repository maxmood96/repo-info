## `xwiki:stable-postgres`

```console
$ docker pull xwiki@sha256:682a68d96e3d7007ca3ec5ecb997bc590eaddae5730fccfa3efaaa7159d899dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:ebf1c13863ed7618a6f433cff65ebcc59175a01bcee510f7f8ed2d05c6e9659c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.9 MB (577898454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f2d6d1ec63b37b0ae5dacfc584c9bfd733dfec12d8124ac9175a4fb7c663cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 19 Jun 2024 14:03:42 GMT
ARG RELEASE
# Wed, 19 Jun 2024 14:03:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Jun 2024 14:03:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Jun 2024 14:03:42 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 19 Jun 2024 14:03:42 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Wed, 19 Jun 2024 14:03:42 GMT
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
# Wed, 19 Jun 2024 14:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 19 Jun 2024 14:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Jun 2024 14:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
WORKDIR /usr/local/tomcat
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jun 2024 14:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jun 2024 14:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_MAJOR=9
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_VERSION=9.0.90
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
# Wed, 19 Jun 2024 14:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 19 Jun 2024 14:03:42 GMT
ENTRYPOINT []
# Wed, 19 Jun 2024 14:03:42 GMT
CMD ["catalina.sh" "run"]
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 26 Jun 2024 09:06:21 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_VERSION=16.5.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.5.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_DOWNLOAD_SHA256=0997ff4cfe16928996218963fad74d7a564c1aa75c7e8434e7cd25bd471ecd5a
# Wed, 26 Jun 2024 09:06:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Wed, 26 Jun 2024 09:06:21 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
VOLUME [/usr/local/xwiki]
# Wed, 26 Jun 2024 09:06:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jun 2024 09:06:21 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ea69141092d083d2011e4bef99d88179238845830f3d13a4e385c22865b7d3`  
		Last Modified: Tue, 02 Jul 2024 06:02:20 GMT  
		Size: 47.3 MB (47256035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d590beb7c559e52929bdee57763bf9b4d6993efef2a777ce420cefdbefbf6fc`  
		Last Modified: Tue, 02 Jul 2024 06:02:13 GMT  
		Size: 162.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb850744c99279a291a7993996d6f9a8b25a5cec4bfad603897080ded3217e1b`  
		Last Modified: Tue, 02 Jul 2024 06:02:13 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a7afe74b6fed6887c816a067579be91ed25ca75523bf75fcfad98cef52543f`  
		Last Modified: Tue, 02 Jul 2024 09:33:31 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76d6552fe8eceff7e6e34f9e939690a80683bd6c24bb7bdfbc93c59a2a7f562`  
		Last Modified: Tue, 02 Jul 2024 09:33:31 GMT  
		Size: 12.4 MB (12448230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f204c7216753af1cfefc04ec89965a3dddc744bc44e0ffed00d1d786c73bc3`  
		Last Modified: Tue, 02 Jul 2024 09:33:31 GMT  
		Size: 217.8 KB (217827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2968176d2f4a21eff44450006f6d2181ddced8cf628fd38119299eb4c41b6ca`  
		Last Modified: Tue, 02 Jul 2024 10:05:58 GMT  
		Size: 179.4 MB (179373887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd7141309db62eda65c0550eccd4b0bd6fec5a4e4b33ee254a7eac5e985205`  
		Last Modified: Tue, 02 Jul 2024 10:05:59 GMT  
		Size: 294.3 MB (294265702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f571ca970a29b0e237adf6a612e2bc9ef999257403d234bb9cf953ad0109ca5`  
		Last Modified: Tue, 02 Jul 2024 10:05:54 GMT  
		Size: 1.0 MB (1011978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3977685e2eb6240cd4b6f82951397f89866472211ee6d695eb19b97565552126`  
		Last Modified: Tue, 02 Jul 2024 10:05:54 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f307992ac6344959b64a8331f8312315f492d3c09636e2063a5d420911aa08a7`  
		Last Modified: Tue, 02 Jul 2024 10:05:55 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae999f2b14329b3afde56f75e0e51e3cadef2020ba5204cc26eb8b48a23729fa`  
		Last Modified: Tue, 02 Jul 2024 10:05:56 GMT  
		Size: 6.5 KB (6526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8454265447b7e4432b23983bb2fb5889216503394e228a834effacc2ab3374a8`  
		Last Modified: Tue, 02 Jul 2024 10:05:56 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:b492bfa87f0e95cbf0c15fb6751c5f6046b34ee11ddc6825f65137ee200f3552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8934420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6418fa7c830e71c82dde020bdb772968d6655fe833f92ddf7db34626a4d0f1`

```dockerfile
```

-	Layers:
	-	`sha256:178957c346861fb12e6be89a9213a2bb26dfa606deb744bd8bbf9aa57870e9d0`  
		Last Modified: Tue, 02 Jul 2024 10:05:55 GMT  
		Size: 8.9 MB (8893045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13150dec105cc91f28744b1110c570ccc62a0e6ebdb9a612dcdba1d85656bb0c`  
		Last Modified: Tue, 02 Jul 2024 10:05:54 GMT  
		Size: 41.4 KB (41375 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:51b3ce83dd81263ecd35b8ca1230e83cb100566470775e987fc8abd0f503c3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.9 MB (572944562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d977c213647cf5703ba5952f7f3ca0455f04331fa686134d188d086896235a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
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
# Wed, 19 Jun 2024 14:03:42 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 19 Jun 2024 14:03:42 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Jun 2024 14:03:42 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
WORKDIR /usr/local/tomcat
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jun 2024 14:03:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 19 Jun 2024 14:03:42 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_MAJOR=9
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_VERSION=9.0.90
# Wed, 19 Jun 2024 14:03:42 GMT
ENV TOMCAT_SHA512=e77b47d7ded86da81018d38c4f728f5f804c1a65bb941a138a7989b69c859031e88d113ccf4fc3a409062ee24511fa5ccf15dfad333f570838ee2a36dae23e19
# Wed, 19 Jun 2024 14:03:42 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 19 Jun 2024 14:03:42 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 19 Jun 2024 14:03:42 GMT
ENTRYPOINT []
# Wed, 19 Jun 2024 14:03:42 GMT
CMD ["catalina.sh" "run"]
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 26 Jun 2024 09:06:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 26 Jun 2024 09:06:21 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_VERSION=16.5.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.5.0
# Wed, 26 Jun 2024 09:06:21 GMT
ENV XWIKI_DOWNLOAD_SHA256=0997ff4cfe16928996218963fad74d7a564c1aa75c7e8434e7cd25bd471ecd5a
# Wed, 26 Jun 2024 09:06:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Wed, 26 Jun 2024 09:06:21 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Wed, 26 Jun 2024 09:06:21 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 26 Jun 2024 09:06:21 GMT
VOLUME [/usr/local/xwiki]
# Wed, 26 Jun 2024 09:06:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jun 2024 09:06:21 GMT
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
	-	`sha256:be592c65af922b27726abd96af5a0cfe9be1a73f8bf397b7088c1a3fa9f04a44`  
		Last Modified: Fri, 28 Jun 2024 22:00:21 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76799d6c646f3750c8e6a7264d880633888d1e2ba50241c0e50817f4417ac73c`  
		Last Modified: Fri, 28 Jun 2024 22:01:46 GMT  
		Size: 12.5 MB (12454654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6550921e61de2eb092056a96013235258b488c63295d9f955bec3605a9719637`  
		Last Modified: Fri, 28 Jun 2024 22:01:46 GMT  
		Size: 2.8 MB (2806589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdec19cf815f741a28393d4b0bcd2e03f834afc3220ef75b499e0e30ab8474e8`  
		Last Modified: Fri, 28 Jun 2024 22:56:48 GMT  
		Size: 174.4 MB (174425231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8734f2a882b1616200c3839deac4f21033138cb66e77d216ba0f86eca157fd`  
		Last Modified: Fri, 28 Jun 2024 22:56:50 GMT  
		Size: 294.3 MB (294265709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10617a17c12ded885cc0de65d88c7bd9f4e3ede40f218ac7923995af9738d8b7`  
		Last Modified: Fri, 28 Jun 2024 22:56:44 GMT  
		Size: 1.0 MB (1011978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595628ea9d1d5f97781551a511ab33a1974bd9d40e5fd58d917c5c3c661fd1b5`  
		Last Modified: Fri, 28 Jun 2024 22:56:44 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496c93e56fd66c4c0667c0b408482b48d8cb51b6c6f1747eaeb2663aa52ccfbc`  
		Last Modified: Fri, 28 Jun 2024 22:56:45 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e652fb53ea770108a4b89a7cfd70d5a6466fab5b45f8d9da2903ead0ba5fa6`  
		Last Modified: Fri, 28 Jun 2024 22:56:45 GMT  
		Size: 6.5 KB (6527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4ff22d5d441f84987afd24975dd0bac265bc18702ba4cc82859187f1154851`  
		Last Modified: Fri, 28 Jun 2024 22:56:46 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:e0e246ec9819c7d91324d1a3dd67f9664b645a3750862674fd4dbc09fde7b2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8937392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a53bcd39e2232965beba7e744a5ed9ec72fe927d6c14d70bd9497a7dcd4113`

```dockerfile
```

-	Layers:
	-	`sha256:d7e1fb458ccf69011c0076b6426120a21747369940b9ea15675ee99f8230da77`  
		Last Modified: Fri, 28 Jun 2024 22:56:44 GMT  
		Size: 8.9 MB (8895360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c7359902b05876b52f80cf810b67d30db797dded3f26eb6e831a294fef49932`  
		Last Modified: Fri, 28 Jun 2024 22:56:44 GMT  
		Size: 42.0 KB (42032 bytes)  
		MIME: application/vnd.in-toto+json
