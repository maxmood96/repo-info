## `xwiki:16-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:39830bac1d7293e9533274163f9c65a44f6a6397a010eb113901e81aac40f6d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:16-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:ccd39695e9afd5c96427d7271b04c3d3d7b5ac7a4c2d333705be78f96fa3aead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.4 MB (622418850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30a981fb0031ab3a7732a5a0797853ace568c9007c64344379c9135d5bfa765`
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
# Tue, 13 May 2025 00:08:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 13 May 2025 00:08:31 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 00:08:31 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 13 May 2025 00:08:31 GMT
WORKDIR /usr/local/tomcat
# Tue, 13 May 2025 00:08:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 13 May 2025 00:08:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 13 May 2025 00:08:31 GMT
ENV TOMCAT_MAJOR=9
# Tue, 13 May 2025 00:08:31 GMT
ENV TOMCAT_VERSION=9.0.105
# Tue, 13 May 2025 00:08:31 GMT
ENV TOMCAT_SHA512=904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956
# Tue, 13 May 2025 00:08:31 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 13 May 2025 00:08:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 May 2025 00:08:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 13 May 2025 00:08:31 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 13 May 2025 00:08:31 GMT
ENTRYPOINT []
# Tue, 13 May 2025 00:08:31 GMT
CMD ["catalina.sh" "run"]
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 14 May 2025 13:55:26 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 13:55:26 GMT
ENV XWIKI_VERSION=16.10.8
# Wed, 14 May 2025 13:55:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.8
# Wed, 14 May 2025 13:55:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=559644b36d96d9daf64bec12559899a525e9f6dc164f7c2dcb1ca6c3a0613a62
# Wed, 14 May 2025 13:55:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_VERSION=3.5.3
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_SHA256=85c4ba2f221d0dfd439c26affbb294f784960763544263c65aba9c2c76858706
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.3
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.3.jar
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.3.jar
# Wed, 14 May 2025 13:55:26 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 14 May 2025 13:55:26 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 14 May 2025 13:55:26 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 14 May 2025 13:55:26 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 14 May 2025 13:55:26 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 14 May 2025 13:55:26 GMT
VOLUME [/usr/local/xwiki]
# Wed, 14 May 2025 13:55:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 May 2025 13:55:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b37af7090fe748226651b75e9eff059c91046da0e4d304f742c24a4437fb81`  
		Last Modified: Mon, 05 May 2025 16:34:56 GMT  
		Size: 17.0 MB (16967882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32efa2d47a978264cf9a212886396adff5e076f0390cdf2bfebcfad4c6347d3`  
		Last Modified: Mon, 05 May 2025 16:34:57 GMT  
		Size: 52.9 MB (52891102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f6621fedbae0a518f88bd221b3bcd6c0cba45111f49a0076d9646b9a125f3e`  
		Last Modified: Mon, 05 May 2025 16:34:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141779bd67f4ce6dfe1c84578df8cfa3a860859d4ed985965e00660f8404b05f`  
		Last Modified: Mon, 05 May 2025 16:34:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6869599e1601f4b6fc4997fb370a893aa1dd96a251b7bc4ed1ce407c111050`  
		Last Modified: Tue, 13 May 2025 19:08:07 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab35935ef37e068287db5a91fa1649f81ec1f858dd75f8972278cb5cac4c5d8`  
		Last Modified: Tue, 13 May 2025 19:08:08 GMT  
		Size: 13.7 MB (13688590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44ecbd7f3ad3ecd724a2325263dcf0dbf1cdba477e1396059a8606e542a87c9`  
		Last Modified: Tue, 13 May 2025 19:08:08 GMT  
		Size: 224.5 KB (224547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0364ede8743f58343ecc8ec0302f0d8d442b9839c8d48f312c1c19ec452a8a78`  
		Last Modified: Wed, 14 May 2025 19:26:36 GMT  
		Size: 191.2 MB (191165874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d70aa6b93be3ba4cb10f904bdf7de19d45546e620fa02ad9d4edf0d8db353f`  
		Last Modified: Wed, 14 May 2025 19:26:38 GMT  
		Size: 317.1 MB (317056276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e70fb794162ca07a674a46236219f2bdbad77b2129c0fda591711236e7cd996`  
		Last Modified: Wed, 14 May 2025 19:26:33 GMT  
		Size: 691.6 KB (691649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f92808f115416ec7f9b1d1684f8a1ae5d30ca9fd2752af1e2ffeea12718d5f2`  
		Last Modified: Wed, 14 May 2025 19:26:33 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a597fcb91df6e76b63490d92a181aaacf12870d3575a80ce5865df0d4f59871`  
		Last Modified: Wed, 14 May 2025 19:26:34 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d693a306f1093e46202627dbfffb669c8614a106a19ea445f7fb21f956cfcfc9`  
		Last Modified: Wed, 14 May 2025 19:26:34 GMT  
		Size: 6.6 KB (6631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edf7d0b032e371481db9ac9e7267675e7b35267f64c2d4014f9b44d238a011a`  
		Last Modified: Wed, 14 May 2025 19:26:35 GMT  
		Size: 2.5 KB (2475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:ae3d904edee236b6e147112c93694a47a593a8d435c752de6e39260c67774fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8799707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77abb7551f46d019d786d0fd41388274000a74d425e13223528f1b7cde37cf4`

```dockerfile
```

-	Layers:
	-	`sha256:c7048f24cb04b43a542e0386c4561dd095f63fdf17ab304c3cb681d6d3bfc2b6`  
		Last Modified: Wed, 14 May 2025 19:26:33 GMT  
		Size: 8.8 MB (8759225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe3f73b9fe05d64a21100c3cfd0b2d254b5148d016fa42f5b889467888ac7c30`  
		Last Modified: Wed, 14 May 2025 19:26:33 GMT  
		Size: 40.5 KB (40482 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:16-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:0c459e92fbb9c02f22864628e98d1ab7775bf367df1eb479f5a4ef46eea8b797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.4 MB (618423179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0980188dfb9144c01e78a89ed3deac1b3c22f61e7a5e0455f6102226f23bd3b`
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
# Tue, 13 May 2025 00:08:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 13 May 2025 00:08:31 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 00:08:31 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 13 May 2025 00:08:31 GMT
WORKDIR /usr/local/tomcat
# Tue, 13 May 2025 00:08:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 13 May 2025 00:08:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 13 May 2025 00:08:31 GMT
ENV TOMCAT_MAJOR=9
# Tue, 13 May 2025 00:08:31 GMT
ENV TOMCAT_VERSION=9.0.105
# Tue, 13 May 2025 00:08:31 GMT
ENV TOMCAT_SHA512=904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956
# Tue, 13 May 2025 00:08:31 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 13 May 2025 00:08:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 May 2025 00:08:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 13 May 2025 00:08:31 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 13 May 2025 00:08:31 GMT
ENTRYPOINT []
# Tue, 13 May 2025 00:08:31 GMT
CMD ["catalina.sh" "run"]
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 14 May 2025 13:55:26 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 13:55:26 GMT
ENV XWIKI_VERSION=16.10.8
# Wed, 14 May 2025 13:55:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.8
# Wed, 14 May 2025 13:55:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=559644b36d96d9daf64bec12559899a525e9f6dc164f7c2dcb1ca6c3a0613a62
# Wed, 14 May 2025 13:55:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_VERSION=3.5.3
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_SHA256=85c4ba2f221d0dfd439c26affbb294f784960763544263c65aba9c2c76858706
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.3
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.3.jar
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.3.jar
# Wed, 14 May 2025 13:55:26 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 14 May 2025 13:55:26 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 14 May 2025 13:55:26 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 14 May 2025 13:55:26 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 14 May 2025 13:55:26 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 14 May 2025 13:55:26 GMT
VOLUME [/usr/local/xwiki]
# Wed, 14 May 2025 13:55:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 May 2025 13:55:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44030c5633c35d5105714bc1403c988244c1f643b1d66f623b7e1beade4140a0`  
		Last Modified: Mon, 05 May 2025 16:50:36 GMT  
		Size: 17.0 MB (16987252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1edce5df06912fb7c1f943a4fdcc192ed2282e8a795c800db4cd61fb8f5935`  
		Last Modified: Mon, 05 May 2025 16:58:33 GMT  
		Size: 52.1 MB (52070835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e295f77fb1bd212dd73e0301b0b5cff71e9564d4a487bf64c2b88759daae55d`  
		Last Modified: Mon, 05 May 2025 16:58:31 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e7a787b9c4da917cc3eb5f7e0cf9f791850f69f59f064f405c346749840d09`  
		Last Modified: Mon, 05 May 2025 16:58:31 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c91c72e07b6db4896190bfe41b8904dd6d4236b3c3b40c752b68dee87652a2`  
		Last Modified: Tue, 06 May 2025 02:07:47 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38ae39a297f0c08d68e2455c74615f37e5e861d1b82474a8e9d4393bbf8ab8c`  
		Last Modified: Tue, 13 May 2025 20:39:31 GMT  
		Size: 13.7 MB (13698686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1b1460ec2bacc3c54269c87e744f82b6651dbc67c5f39d6309dffbbaf81eea`  
		Last Modified: Tue, 13 May 2025 20:39:30 GMT  
		Size: 225.0 KB (224979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe90620a77614cabaae788d137e2e58dee48aaab39f7a6f0fa880e224182ce4`  
		Last Modified: Tue, 13 May 2025 21:13:12 GMT  
		Size: 188.8 MB (188831228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84cf5d714d1cc5919b57c6ff0370ecf1859bbc14b1631b5899cdb479f520710`  
		Last Modified: Wed, 14 May 2025 19:30:52 GMT  
		Size: 317.1 MB (317056275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a07455c90a9651e41fc5dd17733584521cbcd7656381fa4f0de86db378640f`  
		Last Modified: Wed, 14 May 2025 19:31:56 GMT  
		Size: 691.6 KB (691649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561f078827b1c7acc179e2a0e400d5e494594a5f0c7292f220ff0a04aec0f703`  
		Last Modified: Wed, 14 May 2025 19:31:55 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee9fe514e29dddec13849b841294e4015cf74b4d19933be71a286b3377cdf9c`  
		Last Modified: Wed, 14 May 2025 19:31:55 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8570ea2e451af6cfcdc23aaaaf8d766f20e275c604a11423d3972c110ef4b8`  
		Last Modified: Wed, 14 May 2025 19:31:55 GMT  
		Size: 6.6 KB (6633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24f1fd58361dc450d6abe7515a742c78a54bcc2e0efff7ba4351691eaec6528`  
		Last Modified: Wed, 14 May 2025 19:31:56 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:7b8ed6c015292098937134d5ff330d187f23e6177fa84cd2523b329f21e75345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8800609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f87cc89270d848c2012ab81df77080786f19d5d73d468723e9a318bc2334f2`

```dockerfile
```

-	Layers:
	-	`sha256:8b002da992fe9f40b2f1efdedff473eb985e373b7671f43dfcd71ef358cd4c49`  
		Last Modified: Wed, 14 May 2025 19:31:56 GMT  
		Size: 8.8 MB (8759966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a3a3a5863907030f9d18241b72989ce8d188054527cd6f187e9243349959844`  
		Last Modified: Wed, 14 May 2025 19:31:55 GMT  
		Size: 40.6 KB (40643 bytes)  
		MIME: application/vnd.in-toto+json
