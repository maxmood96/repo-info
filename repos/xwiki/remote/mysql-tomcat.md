## `xwiki:mysql-tomcat`

```console
$ docker pull xwiki@sha256:91f585c06305352e5b5edefb156c9bdfcb1ad4fa40753ea4178f89e08bb5cb40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:632cd6c02d460f5e45199801ce372e49f02b43df3b21ebf474aa87ee6f5e0dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.7 MB (627698346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4dc4240510bbb4a8dea1fcfc95d85e686d086b9d0d35f7b00b8626f739e607`
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
# Mon, 12 May 2025 20:03:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 12 May 2025 20:03:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 20:03:20 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 12 May 2025 20:03:20 GMT
WORKDIR /usr/local/tomcat
# Mon, 12 May 2025 20:03:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 12 May 2025 20:03:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 12 May 2025 20:03:20 GMT
ENV TOMCAT_MAJOR=10
# Mon, 12 May 2025 20:03:20 GMT
ENV TOMCAT_VERSION=10.1.41
# Mon, 12 May 2025 20:03:20 GMT
ENV TOMCAT_SHA512=bba43488c1fbcaeaaee1c7c6f3bb2464f10bb1c23f35444d7df1e4d55a6b1838d7d2ca20289f294322f181a6b6e58691d1f75dc50e0f57c2d93eb2fccd35e795
# Mon, 12 May 2025 20:03:20 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 12 May 2025 20:03:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 May 2025 20:03:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 12 May 2025 20:03:20 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 12 May 2025 20:03:20 GMT
ENTRYPOINT []
# Mon, 12 May 2025 20:03:20 GMT
CMD ["catalina.sh" "run"]
# Mon, 26 May 2025 14:18:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 26 May 2025 14:18:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 26 May 2025 14:18:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 26 May 2025 14:18:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 26 May 2025 14:18:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 26 May 2025 14:18:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 26 May 2025 14:18:21 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 14:18:21 GMT
ENV XWIKI_VERSION=17.4.0
# Mon, 26 May 2025 14:18:21 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.4.0
# Mon, 26 May 2025 14:18:21 GMT
ENV XWIKI_DOWNLOAD_SHA256=a772a15f5e7e355d11e82fde3c910d23a269e317b208e862f923572520c438b6
# Mon, 26 May 2025 14:18:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 26 May 2025 14:18:21 GMT
ENV MYSQL_JDBC_VERSION=9.3.0
# Mon, 26 May 2025 14:18:21 GMT
ENV MYSQL_JDBC_SHA256=6c8e6692b521376d89bc5618c16cdeaf8c61854329f4fa25677ed08776c5bb76
# Mon, 26 May 2025 14:18:21 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.3.0
# Mon, 26 May 2025 14:18:21 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.3.0.jar
# Mon, 26 May 2025 14:18:21 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.3.0.jar
# Mon, 26 May 2025 14:18:21 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 26 May 2025 14:18:21 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 26 May 2025 14:18:21 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 26 May 2025 14:18:21 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 26 May 2025 14:18:21 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 26 May 2025 14:18:21 GMT
VOLUME [/usr/local/xwiki]
# Mon, 26 May 2025 14:18:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 May 2025 14:18:21 GMT
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
	-	`sha256:516174cd99cf4c643236ab50e104c365c29efea9692e2bbaee4ab7df1adc3280`  
		Last Modified: Tue, 03 Jun 2025 13:32:49 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee48731bde602b627b3c76a75825ecc819f5fa3520f22c6123726a258545281`  
		Last Modified: Tue, 03 Jun 2025 13:39:40 GMT  
		Size: 14.0 MB (14049764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59c05e7fc2eb1174be17e6f61f9aa8a5ff27dec065fd01947237a4be5017a3e`  
		Last Modified: Tue, 03 Jun 2025 13:39:39 GMT  
		Size: 224.6 KB (224644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc1c4efc5aed5b1fc48dc057d3a444b3696f55f5ecd9e630dbc8091b944e1a3`  
		Last Modified: Tue, 03 Jun 2025 13:41:13 GMT  
		Size: 191.2 MB (191165426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b61a8a40f4cc0b74b3de2ac06fc017ca7568a07599b96455a8e8aa1c3811a38`  
		Last Modified: Tue, 03 Jun 2025 13:41:23 GMT  
		Size: 320.2 MB (320235610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43935c0f5e7ceb3c4c0eb5dcbce6157591bc049577d5321a0adecc8dc6f780e7`  
		Last Modified: Tue, 03 Jun 2025 13:41:02 GMT  
		Size: 2.4 MB (2431599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c851afc6cb59c568bb01fc4f1bab4dcfedc5359b1932c7be806c756eb654d4`  
		Last Modified: Tue, 03 Jun 2025 13:41:02 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d17bb821f1d6e01a3d982cf5ee30be079c8dd86bbc0266b9913f44c74b84a97`  
		Last Modified: Tue, 03 Jun 2025 13:41:02 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebc85d00221c9c86c836f2e8b51017d38c5e84e238b7c6e4ee0f4033ee34a1f`  
		Last Modified: Tue, 03 Jun 2025 13:41:03 GMT  
		Size: 6.6 KB (6577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bff0c26d3bab4e2ab8011b00c3b1b38943797a0f463a28a53831e851560440`  
		Last Modified: Tue, 03 Jun 2025 13:41:03 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:53f915588536b52d6acd57180602b9a10e3c2f0b8488226c6468126f50d89aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8922531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dcb139c2e995d22c332058b90678170efe96772717f02050a75bc88d92bd613`

```dockerfile
```

-	Layers:
	-	`sha256:9c0c055d798b756723b0b6fe8eb04ef1144627ae08ad85e63e81c718bce1c0dc`  
		Last Modified: Tue, 03 Jun 2025 15:08:06 GMT  
		Size: 8.9 MB (8880391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce57a6f14f0132e5e52e4d338da5e004a4cb9c402a216881aeb968ac4162b84e`  
		Last Modified: Tue, 03 Jun 2025 15:08:07 GMT  
		Size: 42.1 KB (42140 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:cce126d513d4037937db0c6b3f2ea85bff970fd6e1a235befeb7296785eb7550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.7 MB (623703062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32c1cbd28678936d4c11b0e8acb37d0b06ae27887e27f61512a1d32abe18071`
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
# Mon, 12 May 2025 20:03:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 12 May 2025 20:03:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 20:03:20 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 12 May 2025 20:03:20 GMT
WORKDIR /usr/local/tomcat
# Mon, 12 May 2025 20:03:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 12 May 2025 20:03:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 12 May 2025 20:03:20 GMT
ENV TOMCAT_MAJOR=10
# Mon, 12 May 2025 20:03:20 GMT
ENV TOMCAT_VERSION=10.1.41
# Mon, 12 May 2025 20:03:20 GMT
ENV TOMCAT_SHA512=bba43488c1fbcaeaaee1c7c6f3bb2464f10bb1c23f35444d7df1e4d55a6b1838d7d2ca20289f294322f181a6b6e58691d1f75dc50e0f57c2d93eb2fccd35e795
# Mon, 12 May 2025 20:03:20 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 12 May 2025 20:03:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 May 2025 20:03:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 12 May 2025 20:03:20 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 12 May 2025 20:03:20 GMT
ENTRYPOINT []
# Mon, 12 May 2025 20:03:20 GMT
CMD ["catalina.sh" "run"]
# Mon, 26 May 2025 14:18:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 26 May 2025 14:18:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 26 May 2025 14:18:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 26 May 2025 14:18:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 26 May 2025 14:18:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 26 May 2025 14:18:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 26 May 2025 14:18:21 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 14:18:21 GMT
ENV XWIKI_VERSION=17.4.0
# Mon, 26 May 2025 14:18:21 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.4.0
# Mon, 26 May 2025 14:18:21 GMT
ENV XWIKI_DOWNLOAD_SHA256=a772a15f5e7e355d11e82fde3c910d23a269e317b208e862f923572520c438b6
# Mon, 26 May 2025 14:18:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 26 May 2025 14:18:21 GMT
ENV MYSQL_JDBC_VERSION=9.3.0
# Mon, 26 May 2025 14:18:21 GMT
ENV MYSQL_JDBC_SHA256=6c8e6692b521376d89bc5618c16cdeaf8c61854329f4fa25677ed08776c5bb76
# Mon, 26 May 2025 14:18:21 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.3.0
# Mon, 26 May 2025 14:18:21 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.3.0.jar
# Mon, 26 May 2025 14:18:21 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.3.0.jar
# Mon, 26 May 2025 14:18:21 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 26 May 2025 14:18:21 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 26 May 2025 14:18:21 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 26 May 2025 14:18:21 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 26 May 2025 14:18:21 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 26 May 2025 14:18:21 GMT
VOLUME [/usr/local/xwiki]
# Mon, 26 May 2025 14:18:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 May 2025 14:18:21 GMT
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
	-	`sha256:0b707511cc4d5d92edb2e1c393e9737817ac0ec0c652c5a104f5ddfe11a4dd91`  
		Last Modified: Tue, 03 Jun 2025 15:14:16 GMT  
		Size: 14.1 MB (14053603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de097343b33944dab2dc90c34621c85d412ea597f33daf0ebb1dfad7bf1e0ed`  
		Last Modified: Tue, 03 Jun 2025 15:14:15 GMT  
		Size: 225.1 KB (225120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6e87e7203d16e11fdd0a083cf7c0dc75ae3386d92fbaa65f0e43430f001b58`  
		Last Modified: Tue, 03 Jun 2025 12:40:03 GMT  
		Size: 188.8 MB (188830856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441de618a7668c791172c10923438317dc91bf246fdcf85760003db6f27f1983`  
		Last Modified: Tue, 03 Jun 2025 12:40:05 GMT  
		Size: 320.2 MB (320235438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0239ead0029ad8336604c30cffc44052fd84f1f049d5f04a430d8e63c086f06`  
		Last Modified: Tue, 03 Jun 2025 12:39:58 GMT  
		Size: 2.4 MB (2431592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f04b761feb1e11f3d738e05e4dd40b1e00dab725083d029590f96ea981f0ee`  
		Last Modified: Tue, 03 Jun 2025 12:39:58 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746ff07bcab231c73b911573794adf877f692e6415ddcfb490cdbb833eaaf078`  
		Last Modified: Tue, 03 Jun 2025 12:39:59 GMT  
		Size: 2.4 KB (2367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33845be7a7033a2f172404ab155c5aa8192819cf61f9ba0fced70e22037a425`  
		Last Modified: Tue, 03 Jun 2025 12:39:59 GMT  
		Size: 6.6 KB (6577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96840df01d2b8680f28ac7760959efc636278555a3c57481298197f3d09d119c`  
		Last Modified: Tue, 03 Jun 2025 12:40:00 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:fd31b106cadae1a33a8c4ec3e65bf14c126996fac16640b6334b08c59375f93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8923577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3685e35df77da3e464a97ff7291b9903c6ce84a5cb4bc175fa005f03190f805b`

```dockerfile
```

-	Layers:
	-	`sha256:0e8f6e5e2d090d0bca9ddba4c61438580780515491c8de42623893724103a9a8`  
		Last Modified: Tue, 03 Jun 2025 15:08:14 GMT  
		Size: 8.9 MB (8881204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55284ad599b50395eae461535e8d7cbf04f86fd096e39d16c3337719fe50152e`  
		Last Modified: Tue, 03 Jun 2025 15:08:15 GMT  
		Size: 42.4 KB (42373 bytes)  
		MIME: application/vnd.in-toto+json
