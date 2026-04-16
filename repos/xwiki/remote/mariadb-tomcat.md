## `xwiki:mariadb-tomcat`

```console
$ docker pull xwiki@sha256:c33d66d7ce639f972a0f319adf84851bb15b63bcb8d044c6f275a32f0605ff97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:5b4f71ff009beed9d61b536ad4b0081ea1082ff468e1f8a6cf6155a35820eac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.4 MB (644391627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3ce623320b28fd5696e7efcbe3d02b0b87673c391c81cc147a9570d8e01451`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:15 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:33:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 15 Apr 2026 22:33:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:33:25 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 15 Apr 2026 22:33:25 GMT
WORKDIR /usr/local/tomcat
# Wed, 15 Apr 2026 22:33:25 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 15 Apr 2026 22:33:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 15 Apr 2026 22:33:25 GMT
ENV TOMCAT_MAJOR=10
# Wed, 15 Apr 2026 22:33:25 GMT
ENV TOMCAT_VERSION=10.1.54
# Wed, 15 Apr 2026 22:33:25 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Wed, 15 Apr 2026 22:33:26 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 15 Apr 2026 22:33:32 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:33:33 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 15 Apr 2026 22:33:33 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 22:33:33 GMT
ENTRYPOINT []
# Wed, 15 Apr 2026 22:33:33 GMT
CMD ["catalina.sh" "run"]
# Wed, 15 Apr 2026 23:17:09 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 15 Apr 2026 23:17:09 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 15 Apr 2026 23:17:09 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 15 Apr 2026 23:17:09 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 15 Apr 2026 23:17:09 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 15 Apr 2026 23:17:09 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 15 Apr 2026 23:17:09 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:17:09 GMT
ENV XWIKI_VERSION=18.2.1
# Wed, 15 Apr 2026 23:17:09 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.2.1
# Wed, 15 Apr 2026 23:17:09 GMT
ENV XWIKI_DOWNLOAD_SHA256=d18d8d16f39d6a37ba11c0015dbafced57183a9bdbdf35ed1103191e24dac7b2
# Wed, 15 Apr 2026 23:17:37 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 15 Apr 2026 23:17:37 GMT
ENV MARIADB_JDBC_VERSION=3.5.7
# Wed, 15 Apr 2026 23:17:37 GMT
ENV MARIADB_JDBC_SHA256=07bb1229dc184f3313a5aef4c5a6b3207c8dbaa09db4a26814c936f004b4c526
# Wed, 15 Apr 2026 23:17:37 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.7
# Wed, 15 Apr 2026 23:17:37 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.7.jar
# Wed, 15 Apr 2026 23:17:37 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.7.jar
# Wed, 15 Apr 2026 23:17:37 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 15 Apr 2026 23:17:37 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 15 Apr 2026 23:17:37 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 15 Apr 2026 23:17:37 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 15 Apr 2026 23:17:37 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 23:17:37 GMT
VOLUME [/usr/local/xwiki]
# Wed, 15 Apr 2026 23:17:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 23:17:37 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166e3ac40fcac6c067aeb2526197d059af1ae4fbadf54b828f5dd81987af050c`  
		Last Modified: Wed, 15 Apr 2026 20:34:31 GMT  
		Size: 17.0 MB (16983398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a89ec8f5419f9af7b5bebf84595d9fadf8482375c3d8e56a7b5f6877cdb14e2`  
		Last Modified: Wed, 15 Apr 2026 20:34:32 GMT  
		Size: 53.0 MB (52985497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea035da72e5f5703c867853ddef78ebc7f9e1a36c5dc6e3fb9d52ac5d4e88408`  
		Last Modified: Wed, 15 Apr 2026 20:34:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5d8083e928e6b185b981f8eacd53e2978658f685409fd506f96b73fee282e0`  
		Last Modified: Wed, 15 Apr 2026 20:34:30 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c386aabe50ea9001b7d60fc42a908ed739d9f42c1de6c3e3266cc6bedcad93`  
		Last Modified: Wed, 15 Apr 2026 22:33:41 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815e75efbdfc357ea1c282bc46d0c05078cc39f8542ecdaa316aa419d2a035c7`  
		Last Modified: Wed, 15 Apr 2026 22:33:42 GMT  
		Size: 14.3 MB (14301294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65b8fbfc6e446502597cdfd6721e6481b592b818e40e9e23ec92d692a5e7834`  
		Last Modified: Wed, 15 Apr 2026 22:33:42 GMT  
		Size: 224.7 KB (224743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee99073e9f493f6249fbdc42f9673e0f90d949a10c74779aba0c9165b3d4972`  
		Last Modified: Wed, 15 Apr 2026 23:18:18 GMT  
		Size: 191.2 MB (191192451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38f68ebe6953ff6e25758b626f8c8e58082fea9122f0b0a631d62d5c2722c50`  
		Last Modified: Wed, 15 Apr 2026 23:18:21 GMT  
		Size: 338.2 MB (338242969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24032bb521f34d396c73e171878f225823b7cc022b932d104a4046cd9838ff7d`  
		Last Modified: Wed, 15 Apr 2026 23:18:09 GMT  
		Size: 708.5 KB (708548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63b2cf69c61c3b5902698ca30531229bcf2179554b3a5c56a825433a376d171`  
		Last Modified: Wed, 15 Apr 2026 23:18:09 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50810a5edceefb183c2b50d82dc5ce55aad9d21c8d0d7dfb6173db51cfe7720b`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ff012e5981520a21d61b93b611276d67de477dbf7306eddc764e18d27d7fbb`  
		Last Modified: Wed, 15 Apr 2026 23:18:11 GMT  
		Size: 11.0 KB (10955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1854967526c2b46d0867cb6662cfb408565307772065977c24b71f254b7c62ef`  
		Last Modified: Wed, 15 Apr 2026 23:18:12 GMT  
		Size: 2.5 KB (2497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:310954550ce3d0eff31a6e1ae3e33e1fea4eaeecbf296abe5de40de4669b2c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9233519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ec65b093b856dc1d94bb18c8ef002325fa8f68656c14463cdebfff2bea2f54`

```dockerfile
```

-	Layers:
	-	`sha256:c0f9eaeff7b34cca59873fd825dbc210a7eee83502fc6370d6583ce45ed016a0`  
		Last Modified: Wed, 15 Apr 2026 23:18:10 GMT  
		Size: 9.2 MB (9192755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b083e3ad89196cd6f6f64c98b1ef1f706633aef2d974c8194d7b6e365d15ac2`  
		Last Modified: Wed, 15 Apr 2026 23:18:09 GMT  
		Size: 40.8 KB (40764 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:e8d71b9a0fff365d5b789fc9917ba30aa06f7e640306fedc1b313d06a1b619b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.4 MB (640379719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87fe0cf562815401a3da6406366bb402ebb1a2ca08bdaf65dbd64479a505734`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:34:21 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 15 Apr 2026 20:34:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:42:07 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 15 Apr 2026 22:42:07 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:42:07 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 15 Apr 2026 22:42:07 GMT
WORKDIR /usr/local/tomcat
# Wed, 15 Apr 2026 22:42:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 15 Apr 2026 22:42:07 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 15 Apr 2026 22:42:07 GMT
ENV TOMCAT_MAJOR=10
# Wed, 15 Apr 2026 22:42:07 GMT
ENV TOMCAT_VERSION=10.1.54
# Wed, 15 Apr 2026 22:42:07 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Wed, 15 Apr 2026 22:42:09 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 15 Apr 2026 22:42:16 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:42:17 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 15 Apr 2026 22:42:17 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 15 Apr 2026 22:42:17 GMT
ENTRYPOINT []
# Wed, 15 Apr 2026 22:42:17 GMT
CMD ["catalina.sh" "run"]
# Wed, 15 Apr 2026 23:14:52 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 15 Apr 2026 23:14:52 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 15 Apr 2026 23:14:52 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 15 Apr 2026 23:14:52 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 15 Apr 2026 23:14:52 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 15 Apr 2026 23:14:52 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 15 Apr 2026 23:14:52 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:14:52 GMT
ENV XWIKI_VERSION=18.2.1
# Wed, 15 Apr 2026 23:14:52 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.2.1
# Wed, 15 Apr 2026 23:14:52 GMT
ENV XWIKI_DOWNLOAD_SHA256=d18d8d16f39d6a37ba11c0015dbafced57183a9bdbdf35ed1103191e24dac7b2
# Wed, 15 Apr 2026 23:15:16 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 15 Apr 2026 23:15:16 GMT
ENV MARIADB_JDBC_VERSION=3.5.7
# Wed, 15 Apr 2026 23:15:16 GMT
ENV MARIADB_JDBC_SHA256=07bb1229dc184f3313a5aef4c5a6b3207c8dbaa09db4a26814c936f004b4c526
# Wed, 15 Apr 2026 23:15:16 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.7
# Wed, 15 Apr 2026 23:15:16 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.7.jar
# Wed, 15 Apr 2026 23:15:16 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.7.jar
# Wed, 15 Apr 2026 23:15:16 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 15 Apr 2026 23:15:16 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 15 Apr 2026 23:15:16 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 15 Apr 2026 23:15:16 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 15 Apr 2026 23:15:16 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 23:15:16 GMT
VOLUME [/usr/local/xwiki]
# Wed, 15 Apr 2026 23:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 23:15:16 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486a631f69c80b7795b8fcf134dbf766e684abb5f464f7f30c96e9875066a00e`  
		Last Modified: Wed, 15 Apr 2026 20:34:38 GMT  
		Size: 17.0 MB (16996216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f83e74af606fee97adef59c5c51391a86142bddd1eb4f5dc49b67c7ce855ed6`  
		Last Modified: Wed, 15 Apr 2026 20:34:39 GMT  
		Size: 52.2 MB (52155661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbbab386f637266b7f19044839d529552165a7c76252310b921b5eceae7c31a`  
		Last Modified: Wed, 15 Apr 2026 20:34:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df7fb31528c8565b18b86816315d1be1846c63b50782910b07e8df7b77c5fea`  
		Last Modified: Wed, 15 Apr 2026 20:34:38 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f257f30df764150a5589d300f5da1a40c3ced8ccdb5f2ccbc5bf4f0653ddd0e8`  
		Last Modified: Wed, 15 Apr 2026 22:42:25 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd178cecdcc11ad6d0cf4af9f2287b1c7a57b1e20fc91e4f50616ccffdc32b4`  
		Last Modified: Wed, 15 Apr 2026 22:42:26 GMT  
		Size: 14.3 MB (14303388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6cf75b8e1ed519c92739e54319fc713315690c62bf14ab011b5b168252f061`  
		Last Modified: Wed, 15 Apr 2026 22:42:25 GMT  
		Size: 225.2 KB (225215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a10203c020b59b933abc3ec0a4170ee40acf8bf257b0f324b91ced3bf105d3c`  
		Last Modified: Wed, 15 Apr 2026 23:15:59 GMT  
		Size: 188.9 MB (188852165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07f02194b70e30f1e4265580ad7a670cba8ce2e3a70642e73902bd49d93551f`  
		Last Modified: Wed, 15 Apr 2026 23:16:01 GMT  
		Size: 338.2 MB (338242988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce5484266c122ada5fd49c4fc143a40723683684754264066d134a7970be7ad`  
		Last Modified: Wed, 15 Apr 2026 23:15:51 GMT  
		Size: 708.5 KB (708549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2064931c8b89b4178707e3faaf81d4f257a5202a1eb69e8c7e250e0579ba646`  
		Last Modified: Wed, 15 Apr 2026 23:15:51 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e3a8fb708f73a5222d2204d9637a666bcacd53a5a164d9f6e8bad085346ea8`  
		Last Modified: Wed, 15 Apr 2026 23:15:53 GMT  
		Size: 2.3 KB (2313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a854f2691d4221d8f0ad6ca8ed4cb30a256bc2698c51ad04485858ea8196a5ae`  
		Last Modified: Wed, 15 Apr 2026 23:15:53 GMT  
		Size: 11.0 KB (10957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2187e16ca293b2ae9c9ca65f3f7e67bb859bb1b8b6ebe9dd45d02b9e2e00c0`  
		Last Modified: Wed, 15 Apr 2026 23:15:54 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:349d35ee1eae67e42bff942b1b20cc4d8af736937b6e98cdd538adef4a4ff600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b373d4a71f77caf43ea5b36782ffe338de62f8de385cdedb11c210e870627d`

```dockerfile
```

-	Layers:
	-	`sha256:11ceac4616bca42c227cc2ecaeb7b10c5f2b6dc89d74b74ba9eed354b9078276`  
		Last Modified: Wed, 15 Apr 2026 23:15:51 GMT  
		Size: 9.2 MB (9193508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60a3215ebfbbb64b58fbd48cbf21cb08872ef1b0545114e8f4b621d42f0d1ca`  
		Last Modified: Wed, 15 Apr 2026 23:15:51 GMT  
		Size: 40.9 KB (40937 bytes)  
		MIME: application/vnd.in-toto+json
