## `xwiki:lts`

```console
$ docker pull xwiki@sha256:5f59943851f5b6f188b20d8cdbf1eee6d1f8068b5efb68b3a65a502c885eb163
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts` - linux; amd64

```console
$ docker pull xwiki@sha256:62f342fe4be010e205d1fdd7fc2c8b50d8edb8075c57ea752a65e5cabd578a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.6 MB (608551497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea38e7d99ae429c5329a30406a4a8f2527a8f0fb66721f3f75f7b6c96146cbe`
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
ENV MYSQL_JDBC_VERSION=8.4.0
# Tue, 19 Nov 2024 13:46:43 GMT
ENV MYSQL_JDBC_SHA256=d77962877d010777cff997015da90ee689f0f4bb76848340e1488f2b83332af5
# Tue, 19 Nov 2024 13:46:43 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.4.0
# Tue, 19 Nov 2024 13:46:43 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.4.0.jar
# Tue, 19 Nov 2024 13:46:43 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.4.0.jar
# Tue, 19 Nov 2024 13:46:43 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:be85375b74d5e16d338d266c3c356c3fdc5d3ed00259e97235b4bff1390057fc`  
		Last Modified: Tue, 19 Nov 2024 20:27:14 GMT  
		Size: 191.7 MB (191709571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34ddeea86e8abc69b1c712caf0d11fef1b3d1293cdeb920debc5ffca8f63cab`  
		Last Modified: Tue, 19 Nov 2024 20:27:16 GMT  
		Size: 307.1 MB (307142508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b6a2a57bf925df0f006c1e116b73fca6458c1201738f2050d4bfe0ab554fa7`  
		Last Modified: Tue, 19 Nov 2024 20:27:12 GMT  
		Size: 2.4 MB (2393567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291e15a19f7722298c3d1dee5f8b3de70c2934b91e97b80250aeb654c8c664f0`  
		Last Modified: Tue, 19 Nov 2024 20:27:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6084ec67fa296313becf06955477fdb9b7e973706f6d7b259d80e967dff6bac`  
		Last Modified: Tue, 19 Nov 2024 20:27:13 GMT  
		Size: 2.4 KB (2369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7fd59f320dec2f6656d44bcfe777ea3218f9e355aa0783cc5c4d4322b66b96`  
		Last Modified: Tue, 19 Nov 2024 20:27:13 GMT  
		Size: 6.5 KB (6463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be4202e2ba7517cfc397eaa3cdbf55585e003be98bc5cb92401d1fe815afdde`  
		Last Modified: Tue, 19 Nov 2024 20:27:13 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts` - unknown; unknown

```console
$ docker pull xwiki@sha256:83fdaf4ee0d900b9e77e5e5d31889e4ec0097a6b440112fa04f0786ea12ac3f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8826789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3fe4c40bb3a113769bdf8856bb1a27505f80a24668a596d60bc21b4bd8bbb2`

```dockerfile
```

-	Layers:
	-	`sha256:67bd20f3fe270b96d89d459016febe5a724ee7e759c867562bb9d696bf8ba7d1`  
		Last Modified: Tue, 19 Nov 2024 20:27:12 GMT  
		Size: 8.8 MB (8784712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eef8b7412bb6fce93a7e091dac138d14586b4976879da128933412ddb0157977`  
		Last Modified: Tue, 19 Nov 2024 20:27:12 GMT  
		Size: 42.1 KB (42077 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:fa9432fd77e89b143c95cda54c7f1fe16e5a612da5f470ca07c8b864ba9020df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.3 MB (604297801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4284c7c9a51ca2148c87b2c9948240c81bc5f8734b3ae8acc70cd7940cb55f`
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
ENV MYSQL_JDBC_VERSION=8.4.0
# Tue, 19 Nov 2024 13:46:43 GMT
ENV MYSQL_JDBC_SHA256=d77962877d010777cff997015da90ee689f0f4bb76848340e1488f2b83332af5
# Tue, 19 Nov 2024 13:46:43 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/8.4.0
# Tue, 19 Nov 2024 13:46:43 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-8.4.0.jar
# Tue, 19 Nov 2024 13:46:43 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-8.4.0.jar
# Tue, 19 Nov 2024 13:46:43 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:b3f98eb244fd45ac2e3b1c71b328b5828d16278e56e83b4817ad75318f1be1ac`  
		Last Modified: Tue, 19 Nov 2024 20:36:33 GMT  
		Size: 2.4 MB (2393576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a60575320947ed1415e47faf9e9186e076454e48b8361cc48e602b23699c1ff`  
		Last Modified: Tue, 19 Nov 2024 20:36:32 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e84356dcdf3ce12bef16417d223101f337b972db183158f26b346a6efda3187`  
		Last Modified: Tue, 19 Nov 2024 20:36:32 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8091efe521653542ed22e3f173e89bab82f37de4c5efe41b42139bfc2f7a36`  
		Last Modified: Tue, 19 Nov 2024 20:36:33 GMT  
		Size: 6.5 KB (6464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7183b03f2b5c8a285def6c8f5c574e8c4dcba6de6f65a047b45d13d9d8f2e5`  
		Last Modified: Tue, 19 Nov 2024 20:36:33 GMT  
		Size: 2.5 KB (2509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts` - unknown; unknown

```console
$ docker pull xwiki@sha256:b015cd974b872b968d45d12540e1ec35c27a92da0c9782cb91d870b196d41d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8827785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fba5c83dfa8c119333960786c62b9f0f0e154f11497e065584bf093d37a6d71`

```dockerfile
```

-	Layers:
	-	`sha256:6c75f83b6991f837bc10a6e855d0910a8ad498ccde6ba75e45c2a585355ad887`  
		Last Modified: Tue, 19 Nov 2024 20:36:32 GMT  
		Size: 8.8 MB (8785500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b2cc0a1565e2eadd3f91f6ca3e8a39b6fa4b1e401775547f1afc1848aadf3d`  
		Last Modified: Tue, 19 Nov 2024 20:36:31 GMT  
		Size: 42.3 KB (42285 bytes)  
		MIME: application/vnd.in-toto+json
