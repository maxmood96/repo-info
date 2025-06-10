## `xwiki:stable-mariadb`

```console
$ docker pull xwiki@sha256:251e41a0ed98d27bded011cf9fa5bdd18a9ecd15963651c2f5f69aae5fb4dab5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:4994f48e4c118bb6d783bbc8a0e23aebfd06852b0381d73150c354a9240c8aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.0 MB (625965906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a967241db503d93d38e706cf44dab86a28290191ca2caa88ff9c68ef2fff0ba8`
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
# Mon, 26 May 2025 14:18:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 26 May 2025 14:18:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 14:18:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 26 May 2025 14:18:21 GMT
WORKDIR /usr/local/tomcat
# Mon, 26 May 2025 14:18:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 26 May 2025 14:18:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 26 May 2025 14:18:21 GMT
ENV TOMCAT_MAJOR=10
# Mon, 26 May 2025 14:18:21 GMT
ENV TOMCAT_VERSION=10.1.42
# Mon, 26 May 2025 14:18:21 GMT
ENV TOMCAT_SHA512=eb09be6df829ebc1fb8851282888966101e878b2c4a507623f3acabc2a1337b89271b4ad7b9361f0bf4bcfe7b5cfec93617bd716043c68afef029c080fff6546
# Mon, 26 May 2025 14:18:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 26 May 2025 14:18:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 14:18:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 26 May 2025 14:18:21 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 26 May 2025 14:18:21 GMT
ENTRYPOINT []
# Mon, 26 May 2025 14:18:21 GMT
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
ENV MARIADB_JDBC_VERSION=3.5.3
# Mon, 26 May 2025 14:18:21 GMT
ENV MARIADB_JDBC_SHA256=85c4ba2f221d0dfd439c26affbb294f784960763544263c65aba9c2c76858706
# Mon, 26 May 2025 14:18:21 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.3
# Mon, 26 May 2025 14:18:21 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.3.jar
# Mon, 26 May 2025 14:18:21 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.3.jar
# Mon, 26 May 2025 14:18:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:c3f1bf3f44e60a6291f511d328cff79513f89d600ecad628cf3eb49c719e4cc1`  
		Last Modified: Tue, 10 Jun 2025 17:39:28 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede6d46ebff305e59c539ef8a0b682eac31df4f5e83112e9040292d4ee1b68a3`  
		Last Modified: Tue, 10 Jun 2025 17:39:29 GMT  
		Size: 14.1 MB (14057680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5589f9155133263156afeae952f440176002e766962495de3b5493dee8643af`  
		Last Modified: Tue, 10 Jun 2025 17:39:28 GMT  
		Size: 224.7 KB (224695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714d2bec39dbb7d185126f5c7e06553f8c816506c41ec266b9f0360975f31740`  
		Last Modified: Tue, 10 Jun 2025 21:36:20 GMT  
		Size: 191.2 MB (191165082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7def434915ef61de2196d907c29e56be9ffd7f60958d1178166b079b9d75f76`  
		Last Modified: Tue, 10 Jun 2025 21:10:02 GMT  
		Size: 320.2 MB (320235592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ed6599712aa0a5fc6c326eb874f610341dd12ae8ef7a94d790f842fab9e1d6`  
		Last Modified: Tue, 10 Jun 2025 17:44:31 GMT  
		Size: 691.6 KB (691649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36849ea74b00570ae16835018e993ba233c65021e28cc5ac2dd456dde27f1fe7`  
		Last Modified: Tue, 10 Jun 2025 17:44:31 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c4a63568caa7c782bb431ba269d0d86a97b2a41077f6fe6ee4151108cdd136`  
		Last Modified: Tue, 10 Jun 2025 17:44:32 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88704ae7eafcec47aad8b9a0812bfb02f18e795ffdf889cddc9d759c499d03d`  
		Last Modified: Tue, 10 Jun 2025 17:44:31 GMT  
		Size: 6.6 KB (6580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1223bc585e7ad52bc2a632c004ee5d5f4be1899d1aa3f88c96151a8bc4099293`  
		Last Modified: Tue, 10 Jun 2025 17:44:32 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:be83c329c768ffff853542a50cf04576af3ad500e3cad6a1522d9b56dc778a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9194139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f135d527eecfdcdb568eb8a0c35464556c072d6bf39d3001a28326dcb71471d`

```dockerfile
```

-	Layers:
	-	`sha256:01d0f53f9bd435f397888f8d3eec06bab1e2f5912d81bc6c65ff097ec996a54a`  
		Last Modified: Tue, 10 Jun 2025 21:08:02 GMT  
		Size: 9.2 MB (9153338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1e19289a70ddef1faaf1c6baf6b25dce0cf429efbfd7e2b3ce3deb7748c4e00`  
		Last Modified: Tue, 10 Jun 2025 21:08:03 GMT  
		Size: 40.8 KB (40801 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:a5e22e50b47651d4bd95c8bc9181f5ac8f74d4dc5bec48a11e19368fc35d659b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.0 MB (621971879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6521421ffe9596121ace9ba395687c776fcc8cd9fed5c032e8005e0c9475773f`
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
# Mon, 26 May 2025 14:18:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 26 May 2025 14:18:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 May 2025 14:18:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 26 May 2025 14:18:21 GMT
WORKDIR /usr/local/tomcat
# Mon, 26 May 2025 14:18:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 26 May 2025 14:18:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 26 May 2025 14:18:21 GMT
ENV TOMCAT_MAJOR=10
# Mon, 26 May 2025 14:18:21 GMT
ENV TOMCAT_VERSION=10.1.42
# Mon, 26 May 2025 14:18:21 GMT
ENV TOMCAT_SHA512=eb09be6df829ebc1fb8851282888966101e878b2c4a507623f3acabc2a1337b89271b4ad7b9361f0bf4bcfe7b5cfec93617bd716043c68afef029c080fff6546
# Mon, 26 May 2025 14:18:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 26 May 2025 14:18:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 14:18:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 26 May 2025 14:18:21 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 26 May 2025 14:18:21 GMT
ENTRYPOINT []
# Mon, 26 May 2025 14:18:21 GMT
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
ENV MARIADB_JDBC_VERSION=3.5.3
# Mon, 26 May 2025 14:18:21 GMT
ENV MARIADB_JDBC_SHA256=85c4ba2f221d0dfd439c26affbb294f784960763544263c65aba9c2c76858706
# Mon, 26 May 2025 14:18:21 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.3
# Mon, 26 May 2025 14:18:21 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.3.jar
# Mon, 26 May 2025 14:18:21 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.3.jar
# Mon, 26 May 2025 14:18:21 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:9698196856a34cc538189aa52cfc35855758df48e1faa44fddacb4313351d6e8`  
		Last Modified: Tue, 10 Jun 2025 18:45:31 GMT  
		Size: 14.1 MB (14062195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c1a601a3d2daf10b65241b8f4b7780e9ecdf6b243d2e4fefbd5719e626f589`  
		Last Modified: Tue, 10 Jun 2025 18:45:29 GMT  
		Size: 225.1 KB (225124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf2924b00421cc935bd06c5d6b4fefebc6eefdf64ef4cde6855937d2b57c22d`  
		Last Modified: Tue, 10 Jun 2025 19:25:03 GMT  
		Size: 188.8 MB (188831029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcca59c63d738fac37e9cd2f450972fad0daf6022f2d4e6f01d8dc96a90eae7e`  
		Last Modified: Tue, 10 Jun 2025 19:25:06 GMT  
		Size: 320.2 MB (320235527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a4b205f20163ec1e95647eb9a1d5ffa83ebab3a2d29cadea4d9631eafa4fac`  
		Last Modified: Tue, 10 Jun 2025 19:26:15 GMT  
		Size: 691.7 KB (691651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5806d11672539ba45af092eeb45a0e836b775427f0d37c765635dedd21e82ebe`  
		Last Modified: Tue, 10 Jun 2025 19:26:13 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7548d2188de78ee47eb7045119ef086adc5b8b8721afabba17790924dd4dd0e`  
		Last Modified: Tue, 10 Jun 2025 19:26:13 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546dbe2e9e93289ac1a878753ef6db3b5158447bc1876078e1e0d18c77d4742d`  
		Last Modified: Tue, 10 Jun 2025 19:26:13 GMT  
		Size: 6.6 KB (6582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12313d238c7985fc4f73c44fdf4eb727e8ff3fe53b685ff60351d3c26801d1b8`  
		Last Modified: Tue, 10 Jun 2025 19:26:13 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:d23be1c6d581598d3d33b93056615e89981fdf674b9b7b8af874e0f3cea0fcf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9195065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949f411833e68a8e5783a6be0ac9dc3d73ef95e990a7324fe11a7a8c98ebaa04`

```dockerfile
```

-	Layers:
	-	`sha256:29da51d9d9320e7f066db084ab781a9d9612fc143898d51d6197d513cfd4b428`  
		Last Modified: Tue, 10 Jun 2025 21:08:10 GMT  
		Size: 9.2 MB (9154091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7aacee2aeb87a5742289c8907430565ed2e9555f5db46a3d08927166562523c`  
		Last Modified: Tue, 10 Jun 2025 21:08:11 GMT  
		Size: 41.0 KB (40974 bytes)  
		MIME: application/vnd.in-toto+json
