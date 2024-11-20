## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:dc454ab2aae33416a87605d682ba0877968a3a8642eeb8a0ba4828f17d93d69b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:08de6b30b6410ac569053c58758dd5b05f620cc34bc19736d3b0a2c1c2dcc870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.8 MB (606819749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69881ad7f8ec279e7d007e2ae7df2ccd8dea36f305050140dddeb66247de2c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 09 Nov 2024 15:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 09 Nov 2024 15:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Nov 2024 15:03:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 09 Nov 2024 15:03:40 GMT
WORKDIR /usr/local/tomcat
# Sat, 09 Nov 2024 15:03:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 09 Nov 2024 15:03:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 09 Nov 2024 15:03:40 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 09 Nov 2024 15:03:40 GMT
ENV TOMCAT_MAJOR=9
# Sat, 09 Nov 2024 15:03:40 GMT
ENV TOMCAT_VERSION=9.0.97
# Sat, 09 Nov 2024 15:03:40 GMT
ENV TOMCAT_SHA512=537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9
# Sat, 09 Nov 2024 15:03:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 09 Nov 2024 15:03:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 Nov 2024 15:03:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 09 Nov 2024 15:03:40 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 09 Nov 2024 15:03:40 GMT
ENTRYPOINT []
# Sat, 09 Nov 2024 15:03:40 GMT
CMD ["catalina.sh" "run"]
# Tue, 19 Nov 2024 13:46:43 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 19 Nov 2024 13:46:43 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 19 Nov 2024 13:46:43 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 19 Nov 2024 13:46:43 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 19 Nov 2024 13:46:43 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 19 Nov 2024 13:46:43 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 19 Nov 2024 13:46:43 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Nov 2024 13:46:43 GMT
ENV XWIKI_VERSION=15.10.14
# Tue, 19 Nov 2024 13:46:43 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.14
# Tue, 19 Nov 2024 13:46:43 GMT
ENV XWIKI_DOWNLOAD_SHA256=ce7be89c0be406c3cf54b1ab521a6f573bc94c98130d267ed846c6fc3bcae0e5
# Tue, 19 Nov 2024 13:46:43 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 19 Nov 2024 13:46:43 GMT
ENV MARIADB_JDBC_VERSION=3.5.0
# Tue, 19 Nov 2024 13:46:43 GMT
ENV MARIADB_JDBC_SHA256=10b777716f1597aed6612abf1985987089fa5446c3bdea2fa4f48a326929f3f5
# Tue, 19 Nov 2024 13:46:43 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.0
# Tue, 19 Nov 2024 13:46:43 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.0.jar
# Tue, 19 Nov 2024 13:46:43 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.0.jar
# Tue, 19 Nov 2024 13:46:43 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 19 Nov 2024 13:46:43 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 19 Nov 2024 13:46:43 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 19 Nov 2024 13:46:43 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 19 Nov 2024 13:46:43 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 19 Nov 2024 13:46:43 GMT
VOLUME [/usr/local/xwiki]
# Tue, 19 Nov 2024 13:46:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Nov 2024 13:46:43 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cdce4894a71f973fa9abc3e2c1d469dfd4621fe70e355f32d79ca115dfee4a`  
		Last Modified: Sat, 16 Nov 2024 02:56:56 GMT  
		Size: 17.0 MB (16966061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719ac7aa71697a2320c1fe4ead00f2444c7300ce5bea68a3d2c7ce45bd1ddd7a`  
		Last Modified: Sat, 16 Nov 2024 02:56:56 GMT  
		Size: 46.9 MB (46941772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e405f17e3562bd1874c952ff62356307897e8b88dc986da2e761728ee91631`  
		Last Modified: Sat, 16 Nov 2024 02:56:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1cc78034c3680aaf89f46cf86bf07a1afacebe58652cf7cd204a1c5a8e2bc`  
		Last Modified: Sat, 16 Nov 2024 02:56:55 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7e5ec0c25b25eabe3df5cdb7cae354ad25d9659e1482f119594b937cad38a2`  
		Last Modified: Sat, 16 Nov 2024 05:48:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd7b6876613aa82f8282321e0f9590b80468ebdc4e0063aa107f3a8f031dfaa`  
		Last Modified: Sat, 16 Nov 2024 05:48:43 GMT  
		Size: 13.4 MB (13407596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71947a54d29bf0c8bba737fb91a6155405b882ab2e3864b38bca030f2cea4329`  
		Last Modified: Sat, 16 Nov 2024 05:48:43 GMT  
		Size: 223.3 KB (223315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23652730b0af382f417b737345670e5f654249ceefaa59e07477d43f17c853df`  
		Last Modified: Tue, 19 Nov 2024 20:27:08 GMT  
		Size: 191.7 MB (191709219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd35c302407de41d6b3610c1a84d65eed9189822fbdc32d4e4ef724c91cfe01`  
		Last Modified: Tue, 19 Nov 2024 20:27:09 GMT  
		Size: 307.1 MB (307142489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad94804404a9446d1b2d3a058a55d6dff6d89276b41f5bcd15c8054ae8e1ca7d`  
		Last Modified: Tue, 19 Nov 2024 20:27:05 GMT  
		Size: 662.3 KB (662284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb67dd4060e45975f67aeb5f854e703263bf7e18fe7179b91e111b0a3b718739`  
		Last Modified: Tue, 19 Nov 2024 20:27:05 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e0d6afb34abd44f0eda3d3aab841311915510640853ee815431d8ac25d3163`  
		Last Modified: Tue, 19 Nov 2024 20:27:06 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35d4e2159c9577ef0efcf1e532832a2e5f67e3250f34cccf9b31f8313ea3978`  
		Last Modified: Tue, 19 Nov 2024 20:27:06 GMT  
		Size: 6.5 KB (6465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7333059f294accea4056b029a10b7174806fcb750cea94b373eabbe394525b4`  
		Last Modified: Tue, 19 Nov 2024 20:27:07 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:3bc77942a9023658d0d71b4d008bda4802236d2fe43e3a6526097b611982a541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8824562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cccd470b4050249a6f03b1444209b4d7988358e6953132bd44d156bdb9058bbc`

```dockerfile
```

-	Layers:
	-	`sha256:93f4bf72a1871b11b2c62dda15a9f7e7c6c92613f5ea08a83515eeb409c9b2e3`  
		Last Modified: Tue, 19 Nov 2024 20:27:05 GMT  
		Size: 8.8 MB (8783532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38faa72a2f36f1eb7c703a0b9009fd481cd576f671bad055bec7a6aecf830b63`  
		Last Modified: Tue, 19 Nov 2024 20:27:05 GMT  
		Size: 41.0 KB (41030 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:a3bcce4b2cb53ad756481957db9e08cb1bf87c431e0cac3b477a6ce0fbed1109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.6 MB (602566417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fff8249af8a2ecb964effe34487fa113cbca68f608839bf3e953644cb0bc7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-17.0.13+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4086cc7cb2d9e7810141f255063caad10a8a018db5e6b47fa5394c506ab65bff';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_x64_linux_hotspot_17.0.13_11.tar.gz';          ;;        arm64)          ESUM='97c4fb748eaa1292fb2f28fec90a3eba23e35974ef67f8b3aa304ad4db2ba162';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.13_11.tar.gz';          ;;        armhf)          ESUM='f9c4008680db016c9cab26cc2739d4553898911522f6a78a611fafa1f5270c88';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_arm_linux_hotspot_17.0.13_11.tar.gz';          ;;        ppc64el)          ESUM='790f53fcc95cc76ed8f27d3146cf789fc354a2afb7148cffd197ca61a643212f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.13_11.tar.gz';          ;;        riscv64)          ESUM='f6f3e71e5452b764aad47e6ffa4f0b26fcfe69bd9eb07fbd468343f9dd5f17b5';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_riscv64_linux_hotspot_17.0.13_11.tar.gz';          ;;        s390x)          ESUM='0f46246643b6543c097d6eda4db03dbe5c8372217e06d661ac0fb3882eab007d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.13%2B11/OpenJDK17U-jre_s390x_linux_hotspot_17.0.13_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 09 Nov 2024 15:03:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 09 Nov 2024 15:03:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Nov 2024 15:03:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Sat, 09 Nov 2024 15:03:40 GMT
WORKDIR /usr/local/tomcat
# Sat, 09 Nov 2024 15:03:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 09 Nov 2024 15:03:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 09 Nov 2024 15:03:40 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 09 Nov 2024 15:03:40 GMT
ENV TOMCAT_MAJOR=9
# Sat, 09 Nov 2024 15:03:40 GMT
ENV TOMCAT_VERSION=9.0.97
# Sat, 09 Nov 2024 15:03:40 GMT
ENV TOMCAT_SHA512=537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9
# Sat, 09 Nov 2024 15:03:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Sat, 09 Nov 2024 15:03:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 Nov 2024 15:03:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Sat, 09 Nov 2024 15:03:40 GMT
EXPOSE map[8080/tcp:{}]
# Sat, 09 Nov 2024 15:03:40 GMT
ENTRYPOINT []
# Sat, 09 Nov 2024 15:03:40 GMT
CMD ["catalina.sh" "run"]
# Tue, 19 Nov 2024 13:46:43 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 19 Nov 2024 13:46:43 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 19 Nov 2024 13:46:43 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 19 Nov 2024 13:46:43 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 19 Nov 2024 13:46:43 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 19 Nov 2024 13:46:43 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 19 Nov 2024 13:46:43 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Nov 2024 13:46:43 GMT
ENV XWIKI_VERSION=15.10.14
# Tue, 19 Nov 2024 13:46:43 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.14
# Tue, 19 Nov 2024 13:46:43 GMT
ENV XWIKI_DOWNLOAD_SHA256=ce7be89c0be406c3cf54b1ab521a6f573bc94c98130d267ed846c6fc3bcae0e5
# Tue, 19 Nov 2024 13:46:43 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 19 Nov 2024 13:46:43 GMT
ENV MARIADB_JDBC_VERSION=3.5.0
# Tue, 19 Nov 2024 13:46:43 GMT
ENV MARIADB_JDBC_SHA256=10b777716f1597aed6612abf1985987089fa5446c3bdea2fa4f48a326929f3f5
# Tue, 19 Nov 2024 13:46:43 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.0
# Tue, 19 Nov 2024 13:46:43 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.0.jar
# Tue, 19 Nov 2024 13:46:43 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.0.jar
# Tue, 19 Nov 2024 13:46:43 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 19 Nov 2024 13:46:43 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 19 Nov 2024 13:46:43 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 19 Nov 2024 13:46:43 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 19 Nov 2024 13:46:43 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 19 Nov 2024 13:46:43 GMT
VOLUME [/usr/local/xwiki]
# Tue, 19 Nov 2024 13:46:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Nov 2024 13:46:43 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bc18bc29eb715bf1a5f404a45956786287384c81d8f10b7a98a9c7b8ff8c11`  
		Last Modified: Sat, 16 Nov 2024 03:07:33 GMT  
		Size: 17.0 MB (16980979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e9645c74eb59d3dc798c961d1d23973795136cdd64d274b2eba5d7b6070728`  
		Last Modified: Sat, 16 Nov 2024 03:10:59 GMT  
		Size: 46.4 MB (46430937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e42cee9f192b8f6883387f85980e69d95d0c9d1c397285374ae3738062a650b`  
		Last Modified: Sat, 16 Nov 2024 03:10:57 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09343514b98c9ec6bd4ef0d351d9d5375c6f53ec935eee85e8a6bf4dca1282d`  
		Last Modified: Sat, 16 Nov 2024 03:10:57 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06398caad27ac3b1b1d703e77c12b3389ff212c0e494ab2bf92715d37b72f1f`  
		Last Modified: Sat, 16 Nov 2024 06:11:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3362270679e4b7256160fc1ae6e3ba5d3edbf9945fb77c8bb1cf13606fafed`  
		Last Modified: Sat, 16 Nov 2024 06:13:31 GMT  
		Size: 13.4 MB (13418503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c4598ecb397d336be2fae94cd2167684e9858ef0712ea1f8f75b165e247f66`  
		Last Modified: Sat, 16 Nov 2024 06:13:31 GMT  
		Size: 223.7 KB (223749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d380a77132e2902798ece73850196ebe2ff4df0160ce7164027978375ad366c8`  
		Last Modified: Sat, 16 Nov 2024 06:51:59 GMT  
		Size: 188.8 MB (188799771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ca06958252642011b4029c0aeecd68645dfee518bd14a027d587df48f8652f`  
		Last Modified: Tue, 19 Nov 2024 20:36:44 GMT  
		Size: 307.1 MB (307142534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986d352bd40db7a79b3dab3d2fb03152ba57790b7c6bce3c99dd771b27199d6b`  
		Last Modified: Tue, 19 Nov 2024 20:42:00 GMT  
		Size: 662.3 KB (662286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409efd09ee79ebc9f8caaef804a50e62679668aabb6a0c240d07590b52b8b07`  
		Last Modified: Tue, 19 Nov 2024 20:42:00 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce85c269d3e683438f7c7346bec80df558727ce5a51ec371cb902e339bb7d563`  
		Last Modified: Tue, 19 Nov 2024 20:42:00 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5dba5ee053cd228108b418c5fed35001beda1f3d150756a2deb2ce050e38a4`  
		Last Modified: Tue, 19 Nov 2024 20:42:00 GMT  
		Size: 6.5 KB (6466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f86f5d4e3a45f839935f4bbc3abd1e29838ff0a3b0e14ddb31fee3fe24aa52`  
		Last Modified: Tue, 19 Nov 2024 20:42:01 GMT  
		Size: 2.5 KB (2475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:7a60494e64c0e887e514e1c2dcee542d6a62dcc69720918ae3ff9c571fcd3df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8825463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:460854a0f1ab7f7cb866831385f53e598990e9abd420bb6c17e62c9e0ddb2a84`

```dockerfile
```

-	Layers:
	-	`sha256:82485dde226ec152b942bfa5d73596b38efad8377d8495589eaaef13d7e034a7`  
		Last Modified: Tue, 19 Nov 2024 20:42:00 GMT  
		Size: 8.8 MB (8784272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9ff91f15dbc3d03cb5230072bd88d3a5528b64b6a98153e18695f8567109873`  
		Last Modified: Tue, 19 Nov 2024 20:41:59 GMT  
		Size: 41.2 KB (41191 bytes)  
		MIME: application/vnd.in-toto+json
