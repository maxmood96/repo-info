## `xwiki:lts-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:120436e6707fa4a61beb84c3036511b65741bc0c687a2e112c0ceb47b0b2c2a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:c692ef7bef22b6fd4f5881d47aef28cc022f1cd65f9d4312430156499b5bb89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.4 MB (622420276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4611dbb9e09d6d0c8f58001f828adb664654f42c9901980398d9e8c332823ec7`
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
# Fri, 09 May 2025 14:55:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 09 May 2025 14:55:49 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 May 2025 14:55:49 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 09 May 2025 14:55:49 GMT
WORKDIR /usr/local/tomcat
# Fri, 09 May 2025 14:55:49 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 09 May 2025 14:55:49 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 09 May 2025 14:55:49 GMT
ENV TOMCAT_MAJOR=9
# Fri, 09 May 2025 14:55:49 GMT
ENV TOMCAT_VERSION=9.0.105
# Fri, 09 May 2025 14:55:49 GMT
ENV TOMCAT_SHA512=904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956
# Fri, 09 May 2025 14:55:49 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 09 May 2025 14:55:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 May 2025 14:55:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 09 May 2025 14:55:49 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 09 May 2025 14:55:49 GMT
ENTRYPOINT []
# Fri, 09 May 2025 14:55:49 GMT
CMD ["catalina.sh" "run"]
# Fri, 09 May 2025 14:55:49 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 09 May 2025 14:55:49 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 09 May 2025 14:55:49 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 09 May 2025 14:55:49 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 09 May 2025 14:55:49 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 09 May 2025 14:55:49 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 09 May 2025 14:55:49 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 May 2025 14:55:49 GMT
ENV XWIKI_VERSION=16.10.7
# Fri, 09 May 2025 14:55:49 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.7
# Fri, 09 May 2025 14:55:49 GMT
ENV XWIKI_DOWNLOAD_SHA256=819af797c94c1918cc3a4bbdf1f0c3c0f83e017c173c02a5ae4d7e42a2a2fb86
# Fri, 09 May 2025 14:55:49 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 09 May 2025 14:55:49 GMT
ENV MARIADB_JDBC_VERSION=3.5.3
# Fri, 09 May 2025 14:55:49 GMT
ENV MARIADB_JDBC_SHA256=85c4ba2f221d0dfd439c26affbb294f784960763544263c65aba9c2c76858706
# Fri, 09 May 2025 14:55:49 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.3
# Fri, 09 May 2025 14:55:49 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.3.jar
# Fri, 09 May 2025 14:55:49 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.3.jar
# Fri, 09 May 2025 14:55:49 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 09 May 2025 14:55:49 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 09 May 2025 14:55:49 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 09 May 2025 14:55:49 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 09 May 2025 14:55:49 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 09 May 2025 14:55:49 GMT
VOLUME [/usr/local/xwiki]
# Fri, 09 May 2025 14:55:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 May 2025 14:55:49 GMT
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
	-	`sha256:8fed70838178066e87d3e681857700e5210136414061eb3cf75d8a4da316732c`  
		Last Modified: Tue, 13 May 2025 19:56:05 GMT  
		Size: 191.2 MB (191165631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc8fc4a411094e85a38e4580ff257507ef56038ee2528de222599e3f0b22703`  
		Last Modified: Tue, 13 May 2025 19:56:07 GMT  
		Size: 317.1 MB (317057938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f96ecdfd4473853f0f6e19a1f3801af5e8ccc5294823d32dd356fdbdd3d9450`  
		Last Modified: Tue, 13 May 2025 19:56:01 GMT  
		Size: 691.6 KB (691650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7911135a8480729064e125202a1189f46b97b2f36a52013a14834f607c608b6`  
		Last Modified: Tue, 13 May 2025 19:56:01 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb1ab7f057f18ddb9f243b8bc26ade34acdbe5ecfdd3d66080d3f9ad096ac63`  
		Last Modified: Tue, 13 May 2025 19:56:02 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ea92e171d47d52020f4c5d1965ba64e023da9691547aef116a3a7aa909f49c`  
		Last Modified: Tue, 13 May 2025 19:56:03 GMT  
		Size: 6.6 KB (6631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9378071ecce1e5833652b571d920ade2efadf8f2c20266ea94cf88ca0795592`  
		Last Modified: Tue, 13 May 2025 19:56:03 GMT  
		Size: 2.5 KB (2478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:894e3700c49e5eeb233756c800e8afbf97473e777835345492ae37cbde6c2eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8799704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b8ee1a2662eab8185878a006b416c74b3fc3d8e6eadd567918d01bdb7f714e`

```dockerfile
```

-	Layers:
	-	`sha256:fcfe77c66949fbc782d78a07cf6487ecb57769d05497f28137863338703d93c9`  
		Last Modified: Tue, 13 May 2025 19:56:01 GMT  
		Size: 8.8 MB (8759225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:070dbe76cf4c2a77edb3501ba42334122a47b363f8b5357af073f0af3eeef028`  
		Last Modified: Tue, 13 May 2025 19:56:00 GMT  
		Size: 40.5 KB (40479 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:a6dbf08252f75b492b07fa3ae76b334d6fbf71d544c0af36d54ff9aa3e865f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.4 MB (618424844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dba99e1d1b9cc635d6a4c1bff74cff3826d632d638b369278710daf387844fa`
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
# Fri, 09 May 2025 14:55:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 09 May 2025 14:55:49 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 May 2025 14:55:49 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 09 May 2025 14:55:49 GMT
WORKDIR /usr/local/tomcat
# Fri, 09 May 2025 14:55:49 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 09 May 2025 14:55:49 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 09 May 2025 14:55:49 GMT
ENV TOMCAT_MAJOR=9
# Fri, 09 May 2025 14:55:49 GMT
ENV TOMCAT_VERSION=9.0.105
# Fri, 09 May 2025 14:55:49 GMT
ENV TOMCAT_SHA512=904f10378ee2c7c68529edfefcba50c77eb677aa4586cfac0603e44703b0278f71f683b0295774f3cdcb027229d146490ef2c8868d8c2b5a631cf3db61ff9956
# Fri, 09 May 2025 14:55:49 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 09 May 2025 14:55:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 May 2025 14:55:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 09 May 2025 14:55:49 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 09 May 2025 14:55:49 GMT
ENTRYPOINT []
# Fri, 09 May 2025 14:55:49 GMT
CMD ["catalina.sh" "run"]
# Fri, 09 May 2025 14:55:49 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 09 May 2025 14:55:49 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 09 May 2025 14:55:49 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 09 May 2025 14:55:49 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 09 May 2025 14:55:49 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 09 May 2025 14:55:49 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 09 May 2025 14:55:49 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 May 2025 14:55:49 GMT
ENV XWIKI_VERSION=16.10.7
# Fri, 09 May 2025 14:55:49 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.7
# Fri, 09 May 2025 14:55:49 GMT
ENV XWIKI_DOWNLOAD_SHA256=819af797c94c1918cc3a4bbdf1f0c3c0f83e017c173c02a5ae4d7e42a2a2fb86
# Fri, 09 May 2025 14:55:49 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 09 May 2025 14:55:49 GMT
ENV MARIADB_JDBC_VERSION=3.5.3
# Fri, 09 May 2025 14:55:49 GMT
ENV MARIADB_JDBC_SHA256=85c4ba2f221d0dfd439c26affbb294f784960763544263c65aba9c2c76858706
# Fri, 09 May 2025 14:55:49 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.3
# Fri, 09 May 2025 14:55:49 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.3.jar
# Fri, 09 May 2025 14:55:49 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.3.jar
# Fri, 09 May 2025 14:55:49 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 09 May 2025 14:55:49 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 09 May 2025 14:55:49 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 09 May 2025 14:55:49 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 09 May 2025 14:55:49 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 09 May 2025 14:55:49 GMT
VOLUME [/usr/local/xwiki]
# Fri, 09 May 2025 14:55:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 May 2025 14:55:49 GMT
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
	-	`sha256:16ed501b183c6ca7ac532f5f8444b0e08e0508937df76eab98cf31721151ae46`  
		Last Modified: Tue, 13 May 2025 21:13:15 GMT  
		Size: 317.1 MB (317057925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d94a9f167757b567c4bd035483abf4979dfc25e4e613312f6c888a02a6a310`  
		Last Modified: Tue, 13 May 2025 21:14:19 GMT  
		Size: 691.7 KB (691652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f22a4b769a071af56e2cdce288cada22776074df8f8163761b8d37a13bbc97`  
		Last Modified: Tue, 13 May 2025 21:14:19 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c6ecd5735a8d32c63cf29b73e2368268b95ebc6009b450f5b623343482bb1e`  
		Last Modified: Tue, 13 May 2025 21:14:19 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672aaa23a28dde729b97b46d49d8c03396bc21539f3d34df08beb79418244a57`  
		Last Modified: Tue, 13 May 2025 21:14:19 GMT  
		Size: 6.6 KB (6634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2834fa76644814ae28c2946859a0ac6c2405bfd33cac38f8c01e11e90b90caa2`  
		Last Modified: Tue, 13 May 2025 21:14:20 GMT  
		Size: 2.5 KB (2476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:196d7b21fc0c5d9329c6e888e67edaefec8ddc5cf239acd873aa1450c91e7593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8800609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ae2415f45b46b7b105b6895947e34fed6c86fb139970c303890ea853a9fa88`

```dockerfile
```

-	Layers:
	-	`sha256:95ddbbcfbcfbf660bc1ffe6cb6db81030c258d9f8ed1be0a6643563c4577ec19`  
		Last Modified: Tue, 13 May 2025 21:14:19 GMT  
		Size: 8.8 MB (8759966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7beb3ec0d76b4883f01c776f50449118a0405936b4785ffd9e67d968d90a000e`  
		Last Modified: Tue, 13 May 2025 21:14:19 GMT  
		Size: 40.6 KB (40643 bytes)  
		MIME: application/vnd.in-toto+json
