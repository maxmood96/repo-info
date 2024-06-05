## `xwiki:15-postgres-tomcat`

```console
$ docker pull xwiki@sha256:5b80e22933d11d522b21fe158c7608f72ecfa7a0fd287a50f5d9533c2439c49f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:15-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:4a26e18de8994b7a3b987e0beab14f9702fa48c6f229e28147c05eaf75d91643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.8 MB (590841011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a395c82a61ce152f8110a4db38e6bf7ad32a06c4b3b3240eae70c095a0b25d`
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
ENV TOMCAT_VERSION=9.0.89
# Mon, 27 May 2024 13:30:04 GMT
ENV TOMCAT_SHA512=aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0
# Mon, 27 May 2024 13:30:04 GMT
COPY dir:0b3a96ac60d75fdf26c7de1d52191df4fd550034e1462b3aee30307d4473afec in /usr/local/tomcat 
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
	-	`sha256:a417853c5a27753acb394c9d8a63a418942da8287f4fda72b474c156e23b27a6`  
		Last Modified: Wed, 05 Jun 2024 09:09:45 GMT  
		Size: 179.4 MB (179373542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1252b76b01385e5bee351a56b19fd648ced61ffc17f713952672cdd23bafc2`  
		Last Modified: Wed, 05 Jun 2024 09:09:48 GMT  
		Size: 306.9 MB (306948778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6943131743795371a6ba20c021aa132495d1394f4d3f781c6f9ba7e6ab59ed45`  
		Last Modified: Wed, 05 Jun 2024 09:09:41 GMT  
		Size: 1.0 MB (1011980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7f54c2d8c2716d20745be4223c480237285dc9b64cd857f304709818ef7254`  
		Last Modified: Wed, 05 Jun 2024 09:09:40 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2273bcea34bfb8fa07d13940d875076452c6dcaa32f0c97a9c010b753c738e`  
		Last Modified: Wed, 05 Jun 2024 09:09:41 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fcf03f67beb02929b8297741ae2ce3495f3923e9961328fe0a975e10846adb`  
		Last Modified: Wed, 05 Jun 2024 09:09:42 GMT  
		Size: 6.4 KB (6418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c91f06c43656045aa3adab206059d0c2881cd3fb129836330c6478c45180c`  
		Last Modified: Wed, 05 Jun 2024 09:09:43 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:15-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:0d0deb036b5225e0863477509ac522e772faa1ca1bd200035b9f1f9ca4a61993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8942218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23ebf64667b5a9d558c3883190b0bfbc0c49ad3545489698621dd2c17ede343`

```dockerfile
```

-	Layers:
	-	`sha256:4c970a1ff5be6ef31924ada519cd1b2a116f80a9b255d5101d0da050675bd9ea`  
		Last Modified: Wed, 05 Jun 2024 09:09:41 GMT  
		Size: 8.9 MB (8902198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a680a14fd41ee3761b63c0c0c1c017233a76befe03510da0ec7cd6aa8de1287`  
		Last Modified: Wed, 05 Jun 2024 09:09:40 GMT  
		Size: 40.0 KB (40020 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:15-postgres-tomcat` - linux; arm64 variant v8

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

### `xwiki:15-postgres-tomcat` - unknown; unknown

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
