## `xwiki:lts-postgres-tomcat`

```console
$ docker pull xwiki@sha256:dcde63d0d01aa854f22761ba08ad9db2f6449883d0f9b59261bf8a92909a4397
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:2e6356f635f112bd1786b2fe65c136639a87546b31e660465bff6e0d22b31b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.9 MB (590853293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b65f5f76fb3131fdb0cdd27dc4d24bb5e44dff261c53d51b797cedf4c510617`
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
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_VERSION=15.10.10
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.10
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_DOWNLOAD_SHA256=fda9b5b4c1f471dc47e8cf2cb72b7550dbe6d6772887201be94c522a13b6078e
# Mon, 27 May 2024 13:30:04 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 27 May 2024 13:30:04 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Mon, 27 May 2024 13:30:04 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Mon, 27 May 2024 13:30:04 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Mon, 27 May 2024 13:30:04 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Mon, 27 May 2024 13:30:04 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Mon, 27 May 2024 13:30:04 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:2d1cc394f3f96226e6f333afb2414af27dd24a302c12451d27b933e2ed1ad75e`  
		Last Modified: Fri, 21 Jun 2024 04:01:08 GMT  
		Size: 179.4 MB (179374104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf40ac1860175003d5ade21beb26b5f7163d513cbb3e5a667a898327893592b`  
		Last Modified: Fri, 21 Jun 2024 04:01:09 GMT  
		Size: 306.9 MB (306948769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aecd7abe6a32cfc440ea94568b4c85fd01da7bccb2f33428d7a4c32d346ee4f`  
		Last Modified: Fri, 21 Jun 2024 04:01:05 GMT  
		Size: 1.0 MB (1011973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f99c619fd22ba09738ae9608230f9fd9cdf45f8943260a9891b22ea063fcc9`  
		Last Modified: Fri, 21 Jun 2024 04:01:05 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0892bb8640b30bb6b6fd9862d1f7c1624b9be613bde4332a7615e5b2ab938818`  
		Last Modified: Fri, 21 Jun 2024 04:01:06 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d87711165cf8d636c4ef3b9a2362c5b5376ade26ce194530cff4baca354cfd9`  
		Last Modified: Fri, 21 Jun 2024 04:01:06 GMT  
		Size: 6.4 KB (6412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996360a45581c0b13695312fa15f23c1a691a21bdebc5a029c18f163baf2f280`  
		Last Modified: Fri, 21 Jun 2024 04:01:07 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:f1f59d475cd1e4149f51c6056311bd9a3fd822107912e3a099f84771cd28a4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8942268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019e7ec49f79640a180b6c6345f1b4fa4c44a51b96da1d73e0bf8883dc6eea66`

```dockerfile
```

-	Layers:
	-	`sha256:368bb4bf5c54d6efe4fe0e08ecb50c54adc03efc6e30a1cd71be2c88c1f6ab5b`  
		Last Modified: Fri, 21 Jun 2024 04:01:05 GMT  
		Size: 8.9 MB (8902199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72d82f28189a77efa60a5db5b308f63771c1c7863f7162408e61cbf289d7d32d`  
		Last Modified: Fri, 21 Jun 2024 04:01:05 GMT  
		Size: 40.1 KB (40069 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:c91eed10788362998eaf719fa6dd07eb301889544b2fcf18922ce0e301b2e66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583268619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b65c6932d340d8646b61822400fff191d23e2add287f99361ae455c0413eb2`
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
ENV TOMCAT_VERSION=9.0.89
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Mon, 27 May 2024 13:30:04 GMT
COPY dir:58ad55bab575cab028cf8b426107fdedda2ac4d0f3638bd518c64d50c26f920e in /usr/local/tomcat 
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
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_VERSION=15.10.10
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.10
# Mon, 27 May 2024 13:30:04 GMT
ENV XWIKI_DOWNLOAD_SHA256=fda9b5b4c1f471dc47e8cf2cb72b7550dbe6d6772887201be94c522a13b6078e
# Mon, 27 May 2024 13:30:04 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 27 May 2024 13:30:04 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Mon, 27 May 2024 13:30:04 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Mon, 27 May 2024 13:30:04 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Mon, 27 May 2024 13:30:04 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Mon, 27 May 2024 13:30:04 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Mon, 27 May 2024 13:30:04 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:98d5ba69c26277dd2d6d15ef91ff232ffd0253fbe365b9430101220e6909bcae`  
		Last Modified: Wed, 05 Jun 2024 18:27:53 GMT  
		Size: 306.9 MB (306948733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354a6b9836e4fa58aaedb4b27f87c88d754a8b3a464cbba76028d8914fd55039`  
		Last Modified: Wed, 05 Jun 2024 18:27:45 GMT  
		Size: 1.0 MB (1011977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb37523b581dd793ad019c7dcd83c75f495a0e09e830fac66721a4e5d0534a17`  
		Last Modified: Wed, 05 Jun 2024 18:27:45 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8677807ba0b5a4c2315bdc63c9c8cc6c6d7eadab931159ee095415f8ea41633`  
		Last Modified: Wed, 05 Jun 2024 18:27:45 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873088be184f3111ec18f20b66d80d3f54bdf474c9d939c42b32e80eff20e27f`  
		Last Modified: Wed, 05 Jun 2024 18:27:46 GMT  
		Size: 6.4 KB (6415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b64a0a2bb807c5d6a4798635978bafb3720b7b70e5c42466343d44740c8eb1d`  
		Last Modified: Wed, 05 Jun 2024 18:27:46 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:68253dbf3adbf92ff32925f7ac48747a899fe8934885271bc05ad2a09bfa6b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8943095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e6b6605bcbf779a94079cfe88a21764e7bf8846b8460cbb9eb0099fc230abe`

```dockerfile
```

-	Layers:
	-	`sha256:57b062aa98cb0e57ab5d612b119530c9beda357b6c3d47df4eac334e0e09c665`  
		Last Modified: Wed, 05 Jun 2024 18:27:45 GMT  
		Size: 8.9 MB (8902760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:472d203dc2e1228251a7cae4024dd21637f63af922d323b73bbb620fc8dfbe38`  
		Last Modified: Wed, 05 Jun 2024 18:27:45 GMT  
		Size: 40.3 KB (40335 bytes)  
		MIME: application/vnd.in-toto+json
