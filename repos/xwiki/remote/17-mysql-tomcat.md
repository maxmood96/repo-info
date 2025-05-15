## `xwiki:17-mysql-tomcat`

```console
$ docker pull xwiki@sha256:43b0e2055d553b8b3cf627fa2282a024400adb0c0384beb071610278ff7ec5b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:17-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:607ff505811f01fae2bff30d28058c46b13ed35450deeb069bdce7d768383595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.9 MB (624866745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e697b151fe0b4393f83baab11a8298b4ff6b8f43f04c02a1da5e596f48ff1a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='8fd14594d0ad8576ba9b698fd10df4a297c548cfdc81cfbe52ac660aeaf5e2b2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Apr 2025 15:52:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 28 Apr 2025 15:52:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 15:52:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
WORKDIR /usr/local/tomcat
# Mon, 28 Apr 2025 15:52:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 28 Apr 2025 15:52:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 28 Apr 2025 15:52:06 GMT
ENV TOMCAT_MAJOR=10
# Mon, 28 Apr 2025 15:52:06 GMT
ENV TOMCAT_VERSION=10.1.41
# Mon, 28 Apr 2025 15:52:06 GMT
ENV TOMCAT_SHA512=bba43488c1fbcaeaaee1c7c6f3bb2464f10bb1c23f35444d7df1e4d55a6b1838d7d2ca20289f294322f181a6b6e58691d1f75dc50e0f57c2d93eb2fccd35e795
# Mon, 28 Apr 2025 15:52:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 28 Apr 2025 15:52:06 GMT
ENTRYPOINT []
# Mon, 28 Apr 2025 15:52:06 GMT
CMD ["catalina.sh" "run"]
# Mon, 28 Apr 2025 15:52:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 28 Apr 2025 15:52:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 28 Apr 2025 15:52:06 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 28 Apr 2025 15:52:06 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 28 Apr 2025 15:52:06 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 28 Apr 2025 15:52:06 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 28 Apr 2025 15:52:06 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
ENV XWIKI_VERSION=17.3.0
# Mon, 28 Apr 2025 15:52:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.3.0
# Mon, 28 Apr 2025 15:52:06 GMT
ENV XWIKI_DOWNLOAD_SHA256=ec6e09a392b5f0928fee68f40ffe218ceecad3113597127a0ecd8c67d7d8ce00
# Mon, 28 Apr 2025 15:52:06 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
ENV MYSQL_JDBC_VERSION=9.1.0
# Mon, 28 Apr 2025 15:52:06 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Mon, 28 Apr 2025 15:52:06 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Mon, 28 Apr 2025 15:52:06 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Mon, 28 Apr 2025 15:52:06 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Mon, 28 Apr 2025 15:52:06 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
VOLUME [/usr/local/xwiki]
# Mon, 28 Apr 2025 15:52:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Apr 2025 15:52:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b37af7090fe748226651b75e9eff059c91046da0e4d304f742c24a4437fb81`  
		Last Modified: Thu, 08 May 2025 17:04:56 GMT  
		Size: 17.0 MB (16967882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32efa2d47a978264cf9a212886396adff5e076f0390cdf2bfebcfad4c6347d3`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 52.9 MB (52891102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f6621fedbae0a518f88bd221b3bcd6c0cba45111f49a0076d9646b9a125f3e`  
		Last Modified: Thu, 08 May 2025 17:04:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141779bd67f4ce6dfe1c84578df8cfa3a860859d4ed985965e00660f8404b05f`  
		Last Modified: Thu, 08 May 2025 17:04:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5402938344761b4a3893e985b6b34e641452a8d720cc0404558d1bfb5f083930`  
		Last Modified: Tue, 13 May 2025 19:08:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b09fe100af1f6dd48911bd2b8f8ebf813094a31ae86f15b4234ca23d8a37f6`  
		Last Modified: Tue, 13 May 2025 19:08:11 GMT  
		Size: 14.0 MB (14049779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123bf1e3ed06b0d676a2885d65afa8afac5fa09f83a4de7f0202c6884551a4bc`  
		Last Modified: Tue, 13 May 2025 19:08:09 GMT  
		Size: 224.6 KB (224551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba623cef79f351a08083e58e5258abe0772add3fd781ae0e1bd34becba68b181`  
		Last Modified: Tue, 13 May 2025 19:55:33 GMT  
		Size: 191.2 MB (191165674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d0964c45361c0ebcae5eecbce1041b0d71ef991fed67bbe86c23cb2c52013e`  
		Last Modified: Tue, 13 May 2025 19:55:35 GMT  
		Size: 317.4 MB (317400568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6fc91f49b5321fbb3113cd57790b98a23fa5e0f3f28ad0c52d1d3aff6a5f95`  
		Last Modified: Tue, 13 May 2025 19:55:31 GMT  
		Size: 2.4 MB (2434172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc82235f00168631b3163eb168f6ef08502c8d75d952b5b667b5b3cfee08ba31`  
		Last Modified: Tue, 13 May 2025 19:55:30 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dcf3489a2d0b6530b20c90470f5191df93d0e73e0d08999d3853f7b272da8c`  
		Last Modified: Tue, 13 May 2025 19:55:32 GMT  
		Size: 2.4 KB (2374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8e65475e88ecd5f985bfbfb2aadd5b205dbff71c7cd5ecced918047e8cb04d`  
		Last Modified: Tue, 13 May 2025 19:55:32 GMT  
		Size: 6.6 KB (6614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e495ce30e48e225ada8569b67b237c1b4f6aae8b16ecf1db113c778aeb40b96f`  
		Last Modified: Tue, 13 May 2025 19:55:33 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:79c5769f720d22967e2415a8dd08c5d1343c9ddc4e9df204b28f908f77af7ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8816808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2374c730733f2b30493397e5d58ad5b16f3e1ee50377434b70df98a0e854ad9`

```dockerfile
```

-	Layers:
	-	`sha256:4e6dfb2bfacfcde135f582941289896d5be1fe50fda48296b3ba3249cb7609b5`  
		Last Modified: Tue, 13 May 2025 19:55:30 GMT  
		Size: 8.8 MB (8774668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b46fe6dc0686e71fdc4c0703c9414c8b7ce7a35e440a126344c6c3b8049d5fc`  
		Last Modified: Tue, 13 May 2025 19:55:30 GMT  
		Size: 42.1 KB (42140 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:17-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:0b4e27085ee9cd8e2b1c6276491e8c073512c1aaf0851ac562869906574dc827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.9 MB (620865066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd35b7ba8a5551ba43ee4dce1ad9f6a55ed6359af2d475e9053263739578700c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='8fd14594d0ad8576ba9b698fd10df4a297c548cfdc81cfbe52ac660aeaf5e2b2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Apr 2025 15:52:06 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 28 Apr 2025 15:52:06 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 15:52:06 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
WORKDIR /usr/local/tomcat
# Mon, 28 Apr 2025 15:52:06 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 28 Apr 2025 15:52:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 28 Apr 2025 15:52:06 GMT
ENV TOMCAT_MAJOR=10
# Mon, 28 Apr 2025 15:52:06 GMT
ENV TOMCAT_VERSION=10.1.41
# Mon, 28 Apr 2025 15:52:06 GMT
ENV TOMCAT_SHA512=bba43488c1fbcaeaaee1c7c6f3bb2464f10bb1c23f35444d7df1e4d55a6b1838d7d2ca20289f294322f181a6b6e58691d1f75dc50e0f57c2d93eb2fccd35e795
# Mon, 28 Apr 2025 15:52:06 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 28 Apr 2025 15:52:06 GMT
ENTRYPOINT []
# Mon, 28 Apr 2025 15:52:06 GMT
CMD ["catalina.sh" "run"]
# Mon, 28 Apr 2025 15:52:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 28 Apr 2025 15:52:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 28 Apr 2025 15:52:06 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 28 Apr 2025 15:52:06 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 28 Apr 2025 15:52:06 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 28 Apr 2025 15:52:06 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 28 Apr 2025 15:52:06 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
ENV XWIKI_VERSION=17.3.0
# Mon, 28 Apr 2025 15:52:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.3.0
# Mon, 28 Apr 2025 15:52:06 GMT
ENV XWIKI_DOWNLOAD_SHA256=ec6e09a392b5f0928fee68f40ffe218ceecad3113597127a0ecd8c67d7d8ce00
# Mon, 28 Apr 2025 15:52:06 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
ENV MYSQL_JDBC_VERSION=9.1.0
# Mon, 28 Apr 2025 15:52:06 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Mon, 28 Apr 2025 15:52:06 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Mon, 28 Apr 2025 15:52:06 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Mon, 28 Apr 2025 15:52:06 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Mon, 28 Apr 2025 15:52:06 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
VOLUME [/usr/local/xwiki]
# Mon, 28 Apr 2025 15:52:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Apr 2025 15:52:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44030c5633c35d5105714bc1403c988244c1f643b1d66f623b7e1beade4140a0`  
		Last Modified: Thu, 08 May 2025 17:05:03 GMT  
		Size: 17.0 MB (16987252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1edce5df06912fb7c1f943a4fdcc192ed2282e8a795c800db4cd61fb8f5935`  
		Last Modified: Thu, 08 May 2025 17:06:23 GMT  
		Size: 52.1 MB (52070835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e295f77fb1bd212dd73e0301b0b5cff71e9564d4a487bf64c2b88759daae55d`  
		Last Modified: Thu, 08 May 2025 17:06:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e7a787b9c4da917cc3eb5f7e0cf9f791850f69f59f064f405c346749840d09`  
		Last Modified: Thu, 08 May 2025 17:06:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c91c72e07b6db4896190bfe41b8904dd6d4236b3c3b40c752b68dee87652a2`  
		Last Modified: Thu, 08 May 2025 17:36:25 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20e7d4dafe75bb95ce7dd2c2c64838ba40e9cefde41621597f9e1067980a08d`  
		Last Modified: Thu, 15 May 2025 19:40:17 GMT  
		Size: 14.1 MB (14053659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655c3fd3e061c7cad4710e5a57acf7158dc9e40c232e08a48ef9b4de4d70b6c8`  
		Last Modified: Thu, 15 May 2025 19:40:16 GMT  
		Size: 225.0 KB (224957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc21d87292c8818b3d4fc58fa85b7a5f336d90506f07d68065c964de27ae162`  
		Last Modified: Tue, 13 May 2025 21:10:24 GMT  
		Size: 188.8 MB (188831217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78036564e9257038909a61ad8de8e7f47541118d484fdaebb1666ab876e80beb`  
		Last Modified: Tue, 13 May 2025 21:10:26 GMT  
		Size: 317.4 MB (317400615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed6a4d236e6f5403ec112d36b85902488b47907088dc2e05eeb8c086fc37360`  
		Last Modified: Tue, 13 May 2025 21:10:20 GMT  
		Size: 2.4 MB (2434173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eadbaa6faf1b22f8bfaba04d17bf2bb79a3c8b68d2938de33738df3d294aac2`  
		Last Modified: Tue, 13 May 2025 21:10:20 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1339b9664d971583b8f4c1336325f010a74107bfe45cd53598f98512a3277d`  
		Last Modified: Tue, 13 May 2025 21:10:21 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf24a6b798221eca4b90d3f6e1841ca2463cc7d1e7a067a14a5ce980a4e6089f`  
		Last Modified: Tue, 13 May 2025 21:10:21 GMT  
		Size: 6.6 KB (6609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf312c808be8834ae4c2f658b4aac950d1939cdfff028748c024cc83cc0edf78`  
		Last Modified: Tue, 13 May 2025 21:10:22 GMT  
		Size: 2.5 KB (2515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:c17a5b21218865a7a372b1fd5ed3dc1fb6b788a07780aee47d03a3d24ee4d815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8817854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be85601924f3164b21a1482ee1510603afdc219eda2bfffdc39f16a269c92f5b`

```dockerfile
```

-	Layers:
	-	`sha256:0accd53a9a7a29510e09da498286cae94fdf49b44eae5a5d14665987820de0d7`  
		Last Modified: Tue, 13 May 2025 21:10:20 GMT  
		Size: 8.8 MB (8775481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c918c48bac71c9dbd49017a09de64392df61e845d0dd2970aa9f4c322e3533d5`  
		Last Modified: Tue, 13 May 2025 21:10:19 GMT  
		Size: 42.4 KB (42373 bytes)  
		MIME: application/vnd.in-toto+json
