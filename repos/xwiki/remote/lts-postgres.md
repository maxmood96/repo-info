## `xwiki:lts-postgres`

```console
$ docker pull xwiki@sha256:75cd1821433bd364aa29f8c3933694f16fd53286fb27f21c499b50198f00af43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:b2bf0b17b8b843913309c5892f4b11bb571f26f745c37fe1c24c08a8096e94b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.6 MB (590601240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c686ed41d9f85124951468f3f9aefce8f8121b99bcae23f779632adfa5bd51`
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
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 27 Jun 2024 13:08:28 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_VERSION=15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=b69de0d6ae0d2cdd10efcd1913065f750de62b5147f553bc6772e42cc66e2e2c
# Thu, 27 Jun 2024 13:08:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Thu, 27 Jun 2024 13:08:28 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
VOLUME [/usr/local/xwiki]
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jun 2024 13:08:28 GMT
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
	-	`sha256:a102715abca93e239540ce3acc68c02bbb30787818d3ba1e7669cf202517cb11`  
		Last Modified: Tue, 02 Jul 2024 10:05:41 GMT  
		Size: 179.4 MB (179374382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f513d8546002369560a608a99b01a1a07bf1b6387de3e315018eb982ccfab17`  
		Last Modified: Tue, 02 Jul 2024 10:05:43 GMT  
		Size: 307.0 MB (306968094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f343150fda69f5afa3af6b799f1b2fd726e82f366d1597d94c8c094cc98a8d`  
		Last Modified: Tue, 02 Jul 2024 10:05:39 GMT  
		Size: 1.0 MB (1011975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057dad98a7793d99544b88523a760b987d2dd412d64c2606f9543332ad3be934`  
		Last Modified: Tue, 02 Jul 2024 10:05:38 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d074ffe185c0516cb1cb056761d84862e914e34c3c2a1cd457bfe0ee2cc0b51e`  
		Last Modified: Tue, 02 Jul 2024 10:05:40 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc18ba9eb685aabf75ccd9d8aeaa47986bd40b55192c85fe403758883211daa5`  
		Last Modified: Tue, 02 Jul 2024 10:05:39 GMT  
		Size: 6.4 KB (6432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783ab680debaf88284c5cea1411d6541b5b070040f6cb1eb0621be9155bc9595`  
		Last Modified: Tue, 02 Jul 2024 10:05:40 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:fcd9a4441538aef14c9db06f3e20a0a7e4c934d73d1a22d84d884dbddbbea8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8943281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0612d7d11ded09a43b00447a6ac16e831a587282b5c7c1de52b8b6932b7667`

```dockerfile
```

-	Layers:
	-	`sha256:fac0f274c6c973ed55b95d7b032547f9ec21c4fdd8a916f270c86515b3798705`  
		Last Modified: Tue, 02 Jul 2024 10:05:39 GMT  
		Size: 8.9 MB (8902214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2e95503e657930a9918f4bb0cfbc85420d93363427ff910316867c87cf6d7b9`  
		Last Modified: Tue, 02 Jul 2024 10:05:38 GMT  
		Size: 41.1 KB (41067 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:028aa3e1b63c5c9cf1ea1c4c02148121cfe769610e524497c10778878b5f9fe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **585.6 MB (585646861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f2c470d77d317f22ee1ba3b578afc46db0a3182891565940ddf55ecc0315b8`
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
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 27 Jun 2024 13:08:28 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_VERSION=15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=b69de0d6ae0d2cdd10efcd1913065f750de62b5147f553bc6772e42cc66e2e2c
# Thu, 27 Jun 2024 13:08:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Thu, 27 Jun 2024 13:08:28 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
VOLUME [/usr/local/xwiki]
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jun 2024 13:08:28 GMT
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
	-	`sha256:ba7096cc9e92e884d3be88aafb14290348d4dcda2f62df61774fb0681efe24fc`  
		Last Modified: Fri, 28 Jun 2024 23:00:06 GMT  
		Size: 307.0 MB (306968120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ca13eef82c8b975d1f00860cffdda66e7a10f62748b17181fab5d2b69656ea`  
		Last Modified: Fri, 28 Jun 2024 22:59:57 GMT  
		Size: 1.0 MB (1011977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8e0f8912156635ffa80906a857612284703c18f81741354e3ad76481569b59`  
		Last Modified: Fri, 28 Jun 2024 22:59:57 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0629ff3dee80fb39894fd9cc92bf40e1d1944494a7e1b18fa069adb3fd36dcf7`  
		Last Modified: Fri, 28 Jun 2024 22:59:57 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef112cf5ba4455068df0dd159f59bc344e73556bb04812f111bbdb5c071747d`  
		Last Modified: Fri, 28 Jun 2024 22:59:58 GMT  
		Size: 6.4 KB (6431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3df401590667b31964edd653e5b98b4ba888f18d863a47d4a975692803b2c47`  
		Last Modified: Fri, 28 Jun 2024 22:59:58 GMT  
		Size: 2.4 KB (2428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:e13332e7b01eb0ee75ec405066c84d09fe867046186a57fc345e388af3ca84b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8946228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0143fd072923332cb4765b571a058c103203ef0a16381225e101f86f071432cc`

```dockerfile
```

-	Layers:
	-	`sha256:2ec84c69e16ecea00c6d3f1a8da6c82a67f5914979dbb764062d29d4e51d66ef`  
		Last Modified: Fri, 28 Jun 2024 22:59:57 GMT  
		Size: 8.9 MB (8904517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c185964eaaba53c22e2390feeb7c2d6e5027e14d1e3b917443c3bdc5d02bbce8`  
		Last Modified: Fri, 28 Jun 2024 22:59:57 GMT  
		Size: 41.7 KB (41711 bytes)  
		MIME: application/vnd.in-toto+json
