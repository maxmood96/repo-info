## `xwiki:lts-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:24faebe6f75569aba213b9967a5671dc5f682178ede3a414511e334be2530dd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:aee054ded21cfe7043ee5e4cd275b45a26d77fa5674f2515fa02750ccb24feef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.4 MB (622417816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31148ccb2c20a5b9b3dbe34ab8fe601b120ca7da903d8e2eeb1ad4d87c90e5e5`
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
	-	`sha256:5d89a0252baba2eb828778b72ca4b1697d805bd148eb5151510e070cfacf1896`  
		Last Modified: Tue, 03 Jun 2025 13:47:24 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8f6445d9e6a840a92480392fcff890ad31dcd6ad37bbdec5fb9a08f1a2616c`  
		Last Modified: Tue, 03 Jun 2025 13:47:26 GMT  
		Size: 13.7 MB (13688598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffd3ca1b11eb143d472f0c07608994fa490a52a327180317c4b154cb2f83b09`  
		Last Modified: Tue, 03 Jun 2025 13:47:25 GMT  
		Size: 224.7 KB (224655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d84998ad6ad4513439bcc684059cd9ead8cdc3da735db1f3dce821e4b9043c4`  
		Last Modified: Tue, 03 Jun 2025 13:59:18 GMT  
		Size: 191.2 MB (191165413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74db55a8a6a001ae80420174f30c61e49d15db224c23fa210ae3156d24ea765`  
		Last Modified: Tue, 03 Jun 2025 13:59:20 GMT  
		Size: 317.1 MB (317056249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8a72a082c07308a98a8e6ad374df28b80e91272f2de7bce15c18fa2511d84a`  
		Last Modified: Tue, 03 Jun 2025 13:59:19 GMT  
		Size: 691.6 KB (691646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f847d1e84a6283b08d090b32669a225ecf4156dd20f29c07dbb6f9271f3029`  
		Last Modified: Tue, 03 Jun 2025 13:59:20 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fd3db57812cf644af5c3957adb8982e2e36354dc21ba5042de6ab036eae74f`  
		Last Modified: Tue, 03 Jun 2025 13:59:22 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9258728ceec9754f3a9282f938918302e09f6d7abd7f66e6ff4045c421c8ca39`  
		Last Modified: Tue, 03 Jun 2025 13:59:24 GMT  
		Size: 6.6 KB (6629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26be1cdb5f12a0d297bfb69d2c00d4266c81c6bbaa8ce99a7fe95e907f912fb`  
		Last Modified: Tue, 03 Jun 2025 13:59:24 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:0e7191d7a0bb41e0c59cdc5082b7419eda1e953db2af1dd66edca03ad0bd5152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8869270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a321b8c19f55d7ce0611e9912ee4ff83398a561b10180f02b4b2d902303cdc8`

```dockerfile
```

-	Layers:
	-	`sha256:5be79036ce49733f1f95ad242d7e3ba1789ce6f1281bf21ea85e657c9df70c32`  
		Last Modified: Tue, 03 Jun 2025 15:07:47 GMT  
		Size: 8.8 MB (8828788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bfb95e3daa2fca1dec6c9ad946dbbdf652f794f23ba6c0a9f22a7e3d8fd43b5`  
		Last Modified: Tue, 03 Jun 2025 15:07:48 GMT  
		Size: 40.5 KB (40482 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:02b3c57185a535c44f3b8632b029e12a18eed1d2e030ca49122fd4832f258c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.4 MB (618429234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370913e4c75d49d8fc210b595c85b1d444d62bd5cb5f716baeda3c1353e7d4ed`
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
	-	`sha256:d64f62085f800a7fc9261f42992e1846418134a316fd2ed1b976436211c6c1ea`  
		Last Modified: Tue, 03 Jun 2025 14:42:13 GMT  
		Size: 13.7 MB (13698659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc735a32415c1662d75fc316dd34122eee975251b5f9071ea23ca080f5062a5`  
		Last Modified: Tue, 03 Jun 2025 14:42:16 GMT  
		Size: 225.1 KB (225131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85f0ac60a341d2421e83315e242700534942539cd90a7de69ad9fb2bc6c0448`  
		Last Modified: Tue, 03 Jun 2025 12:43:25 GMT  
		Size: 188.8 MB (188831154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c21508e8d1710ee6599a97f744d2a81af80e3e0428d4ec9bdcfb138389aca`  
		Last Modified: Tue, 03 Jun 2025 12:43:27 GMT  
		Size: 317.1 MB (317056219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557c19bf09d37accee3fc220df1c4b171966d3ae14d6e2415fab1ed5a149fa94`  
		Last Modified: Tue, 03 Jun 2025 12:44:31 GMT  
		Size: 691.6 KB (691650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993f3a5c2f3453c22cf68b372d4f637b5f829ef4151b47b803a9c62854230160`  
		Last Modified: Tue, 03 Jun 2025 12:44:31 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f5d00d45fa08bd0b1e46f25e5c075f66e74ca8b32f041e9a1952d01066d0f7`  
		Last Modified: Tue, 03 Jun 2025 12:44:31 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d740df089f48b1ef70111caa19e4b176876a02fef0c773e096e72f3552e3ca00`  
		Last Modified: Tue, 03 Jun 2025 12:44:31 GMT  
		Size: 6.6 KB (6634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bc6c2a684046c211077726f63f59d7522137bd5589a6afc525a73a3b652a30`  
		Last Modified: Tue, 03 Jun 2025 12:44:32 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:ae51fb629e715e2c982c6af1bf404d94cd93b2a3737852957334175abe20aa72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8870172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddeae8a06e7c864c9580111481f9859e2656488a2bb408705caece40038a063e`

```dockerfile
```

-	Layers:
	-	`sha256:f8196ba6cbb4c606a182a02604c746faaa2c2954385558e68cc6605c38bb9cff`  
		Last Modified: Tue, 03 Jun 2025 15:07:58 GMT  
		Size: 8.8 MB (8829529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d3e624f176cff10a4adf655e00e1c23494840fe0ef3e8c07d1af31ad27516ca`  
		Last Modified: Tue, 03 Jun 2025 15:07:59 GMT  
		Size: 40.6 KB (40643 bytes)  
		MIME: application/vnd.in-toto+json
