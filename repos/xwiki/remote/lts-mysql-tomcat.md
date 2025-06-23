## `xwiki:lts-mysql-tomcat`

```console
$ docker pull xwiki@sha256:55732efa56132620fdd461618779e9a22358a81d84c5a9d1fbf7f5aa24fab36e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:d52ca48be10bd541349866db75efa366444f92ac7b3b7df7757f60b8f3c55eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.2 MB (624161914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80c6bd9c3bee4d1c8b8d9508a6e88d0060a25353b5243f73ae19c42fd64c463`
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
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
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
# Wed, 14 May 2025 13:55:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 14 May 2025 13:55:26 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 13:55:26 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 14 May 2025 13:55:26 GMT
WORKDIR /usr/local/tomcat
# Wed, 14 May 2025 13:55:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 14 May 2025 13:55:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 14 May 2025 13:55:26 GMT
ENV TOMCAT_MAJOR=9
# Wed, 14 May 2025 13:55:26 GMT
ENV TOMCAT_VERSION=9.0.106
# Wed, 14 May 2025 13:55:26 GMT
ENV TOMCAT_SHA512=0b316af119fd9a69761c20bc7f9959513884002fc60f490af6335380a3a62549777bf35a1e8dd3c448e56da8ddcb9dc2301d3b01bba304537ca40456c650c25a
# Wed, 14 May 2025 13:55:26 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 14 May 2025 13:55:26 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 13:55:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 14 May 2025 13:55:26 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 14 May 2025 13:55:26 GMT
ENTRYPOINT []
# Wed, 14 May 2025 13:55:26 GMT
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
ENV MYSQL_JDBC_VERSION=9.3.0
# Wed, 14 May 2025 13:55:26 GMT
ENV MYSQL_JDBC_SHA256=6c8e6692b521376d89bc5618c16cdeaf8c61854329f4fa25677ed08776c5bb76
# Wed, 14 May 2025 13:55:26 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.3.0
# Wed, 14 May 2025 13:55:26 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.3.0.jar
# Wed, 14 May 2025 13:55:26 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.3.0.jar
# Wed, 14 May 2025 13:55:26 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35394ce74242c5b7ece149865352a48182efc427381c78444f4d0d8eb1f42de6`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 17.0 MB (16969509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a156ac8fc59e1707c9f501f0739b750edf0a7eee174a746f875ff6095203a864`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 52.9 MB (52891018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d570382bab9a8f261ccabe2287081c1d484a97c6ea8d4fc6225bfe706ccb3b`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b894632d8872eed0f9df445b209dd701a6186ce7c4df92157736141508657d61`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1ec87299755c3521b672bc05e7815b68e9b95be1f9f7ef9ea801f3562807ea`  
		Last Modified: Tue, 10 Jun 2025 18:08:33 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86a23f101ea68a7dd176cb78136ec1f4f6604bbc619244f1a23063ddd28b50e`  
		Last Modified: Tue, 10 Jun 2025 18:08:35 GMT  
		Size: 13.7 MB (13692752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f74ce3dbfb4598a6a24ee37ca0bdeee893d20e5ac17ce2d77036ecd20cb4ba`  
		Last Modified: Tue, 10 Jun 2025 18:08:34 GMT  
		Size: 224.7 KB (224710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3db9ec35a59c92ba1a510b8efa33c4f7abc3fb587768b2deb81008339965a52`  
		Last Modified: Tue, 10 Jun 2025 21:09:23 GMT  
		Size: 191.2 MB (191165269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9266a2e6e875d7d7c4417c6fc81ecd43e2a19dd81f2f00cffde1b3daa83103`  
		Last Modified: Tue, 10 Jun 2025 21:09:18 GMT  
		Size: 317.1 MB (317056220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe41f687e674595ae961ed998ffdbbb9eacd4c5655f77b6fadaa17643574724`  
		Last Modified: Tue, 10 Jun 2025 18:29:27 GMT  
		Size: 2.4 MB (2431603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6619b99c7828085c552c8fe04884f6c1cc918c698012de63d159b6f3724dc3f`  
		Last Modified: Tue, 10 Jun 2025 18:29:27 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908fb77a208ae8949ac10f6e5e143f5ca9ee23f58ca8504bc69c130034dc583`  
		Last Modified: Tue, 10 Jun 2025 18:29:27 GMT  
		Size: 2.4 KB (2370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a99e342d376d5cc0400a08f9a7b99d694133ec0c4fb9996098e7f75924cb04`  
		Last Modified: Tue, 10 Jun 2025 18:29:28 GMT  
		Size: 6.6 KB (6630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68b7a13305bf6b270b73cbdec0db0ca2fccea64db75118a37d13c88dc78fbe0`  
		Last Modified: Tue, 10 Jun 2025 18:29:27 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:f07c8c0a5074423830190c64c3515fe7f77032c3387bfed2a15caa41b024e066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9145998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cefd428986e7f3b1fe77ef1dc2f07a237c6f7e76931b9dd1fbd1254f0fd50e59`

```dockerfile
```

-	Layers:
	-	`sha256:2b79cdeac22e95c4d3de3806dc4bdbe629454b6c8f17751afb6a2482ef8e40fa`  
		Last Modified: Tue, 10 Jun 2025 21:07:20 GMT  
		Size: 9.1 MB (9104471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e932bbb154df0a529d516ee1d1bfab152c586e92c5bcb6cab5d8ca6cc9fb4808`  
		Last Modified: Tue, 10 Jun 2025 21:07:21 GMT  
		Size: 41.5 KB (41527 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:138d6ee580b8709e1dc468d36a34c3441eae4c8430e3ebe0011c7cefe4185d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.3 MB (620283797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42863eb4ec0c51ed0d6a13f7cc26aca58caa0c85dad0559d9ad617f901aeb181`
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
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
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
# Tue, 10 Jun 2025 08:03:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 10 Jun 2025 08:03:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Jun 2025 08:03:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
WORKDIR /usr/local/tomcat
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 08:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_MAJOR=9
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_VERSION=9.0.106
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_SHA512=0b316af119fd9a69761c20bc7f9959513884002fc60f490af6335380a3a62549777bf35a1e8dd3c448e56da8ddcb9dc2301d3b01bba304537ca40456c650c25a
# Tue, 10 Jun 2025 08:03:44 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Jun 2025 08:03:44 GMT
ENTRYPOINT []
# Tue, 10 Jun 2025 08:03:44 GMT
CMD ["catalina.sh" "run"]
# Mon, 23 Jun 2025 09:43:20 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 23 Jun 2025 09:43:20 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 23 Jun 2025 09:43:20 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 23 Jun 2025 09:43:20 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 23 Jun 2025 09:43:20 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 23 Jun 2025 09:43:20 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 23 Jun 2025 09:43:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
ENV XWIKI_VERSION=16.10.9
# Mon, 23 Jun 2025 09:43:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.9
# Mon, 23 Jun 2025 09:43:20 GMT
ENV XWIKI_DOWNLOAD_SHA256=5941a1f25e53d9dec1d387891ce9920e80c29f70edb18c4d8522f5c29519da1e
# Mon, 23 Jun 2025 09:43:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
ENV MYSQL_JDBC_VERSION=9.3.0
# Mon, 23 Jun 2025 09:43:20 GMT
ENV MYSQL_JDBC_SHA256=6c8e6692b521376d89bc5618c16cdeaf8c61854329f4fa25677ed08776c5bb76
# Mon, 23 Jun 2025 09:43:20 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.3.0
# Mon, 23 Jun 2025 09:43:20 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.3.0.jar
# Mon, 23 Jun 2025 09:43:20 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.3.0.jar
# Mon, 23 Jun 2025 09:43:20 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
VOLUME [/usr/local/xwiki]
# Mon, 23 Jun 2025 09:43:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Jun 2025 09:43:20 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb5cdde15082c2c264c46bd2f1aa0a8ad43d7590dd7374853ce1748ae4259a4`  
		Last Modified: Tue, 03 Jun 2025 13:30:28 GMT  
		Size: 17.0 MB (16988306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5911347bfc36c43690c78dbee1e4214c6e79e6c2b6bae6572423040611ba80da`  
		Last Modified: Tue, 03 Jun 2025 13:30:30 GMT  
		Size: 52.1 MB (52070812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06763e1dbf3e148227fb25ab13d25e10e5ae8fcef8987f96fed0240d4ddc176b`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720d536b8cff2c9920c7cc9f8410384ff797ae6e3f12ba749e6295cc4c780c62`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd2c3debe0b0a3a6a9052f48e560d43e668d79c600e030367fef057dd4ce52c`  
		Last Modified: Tue, 03 Jun 2025 14:38:44 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e95367e3d6924ca9e0ddc8261660489231093a70b1cd2d9a09449734e2d4a8`  
		Last Modified: Tue, 10 Jun 2025 19:20:13 GMT  
		Size: 13.7 MB (13705100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c79dcfdcec117345591706387efa7095e736ca774109b93968cd0cb89efb050`  
		Last Modified: Tue, 10 Jun 2025 19:20:12 GMT  
		Size: 225.2 KB (225155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da93005499f3f05af0181b96ca12cb8619dcb385df3f8189f663eb33b71cfd72`  
		Last Modified: Mon, 23 Jun 2025 18:16:10 GMT  
		Size: 188.8 MB (188836042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0b944eb6507365fae968025b8b672e253fc5ffad13b753b57bcb032989cca2`  
		Last Modified: Mon, 23 Jun 2025 18:16:18 GMT  
		Size: 317.2 MB (317159385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f33fa26d3726e346a1c1e61d9eefffd86932b2d6466c95a375272872c7e9ddc`  
		Last Modified: Mon, 23 Jun 2025 18:16:00 GMT  
		Size: 2.4 MB (2431597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b2ce0e69c9c34a1d6f3e26e5a926ce75455e33241c2126047de5a4baa9a5d6`  
		Last Modified: Mon, 23 Jun 2025 18:16:03 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fdf34949b468dcabf221019d1a66f6079da81fca049d1c2f285e7eaeda2c20`  
		Last Modified: Mon, 23 Jun 2025 18:16:05 GMT  
		Size: 2.4 KB (2373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c05377a6f9d7e6989d784d2520260cac900fcb64ef4cc3fbfdb6f345d9a3afa`  
		Last Modified: Mon, 23 Jun 2025 18:16:10 GMT  
		Size: 6.6 KB (6631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329c882eeb5cd0896d9c571f7ab919ec5a0644ba54ac8f0ca3b7e2d8f70dfec4`  
		Last Modified: Mon, 23 Jun 2025 18:16:12 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:1adea9a1738c133e3a0fdec6ebe328ed3142056fb82df654f9a994c8209c5431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9147005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f34252176cce47bb043b42f7c9d76d6917ca37d66d902636fa6570468713b54`

```dockerfile
```

-	Layers:
	-	`sha256:65bf94966d7d80d4bc8c38020f8a24e014c6b35cf79afdd12c6ca55961ac8e43`  
		Last Modified: Mon, 23 Jun 2025 18:07:32 GMT  
		Size: 9.1 MB (9105269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0683eea3ddba706857e503a6f23632aa682d5fbd3e9dc66b96a74a9e85871eec`  
		Last Modified: Mon, 23 Jun 2025 18:07:33 GMT  
		Size: 41.7 KB (41736 bytes)  
		MIME: application/vnd.in-toto+json
