## `xwiki:stable-mysql-tomcat`

```console
$ docker pull xwiki@sha256:f88ebf212a1f9984542932cebe3e6999d3448a77c8df20fa94edf015c82514df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:68f6f041806d04b365f8f7e4696f8f34cdba2ba946c218379a1745b0c76885d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612905044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ba4797eb7d00a047c54cd14d18989012ada88be8875268915eefb85b52a966`
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
# Mon, 28 Oct 2024 15:53:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 28 Oct 2024 15:53:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 15:53:54 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
WORKDIR /usr/local/tomcat
# Mon, 28 Oct 2024 15:53:54 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 28 Oct 2024 15:53:54 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 28 Oct 2024 15:53:54 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 28 Oct 2024 15:53:54 GMT
ENV TOMCAT_MAJOR=9
# Mon, 28 Oct 2024 15:53:54 GMT
ENV TOMCAT_VERSION=9.0.97
# Mon, 28 Oct 2024 15:53:54 GMT
ENV TOMCAT_SHA512=537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9
# Mon, 28 Oct 2024 15:53:54 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 28 Oct 2024 15:53:54 GMT
ENTRYPOINT []
# Mon, 28 Oct 2024 15:53:54 GMT
CMD ["catalina.sh" "run"]
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 28 Oct 2024 15:53:54 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
ENV XWIKI_VERSION=16.9.0
# Mon, 28 Oct 2024 15:53:54 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.9.0
# Mon, 28 Oct 2024 15:53:54 GMT
ENV XWIKI_DOWNLOAD_SHA256=9a66ce45c49863c0e8cbdae0fb5e5dfab317a1c0c3a45e7c33fb61b09b39fe23
# Mon, 28 Oct 2024 15:53:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MYSQL_JDBC_VERSION=9.1.0
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Mon, 28 Oct 2024 15:53:54 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
VOLUME [/usr/local/xwiki]
# Mon, 28 Oct 2024 15:53:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 15:53:54 GMT
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
	-	`sha256:63204e1d13f1957c50b1af875a2a9777c260d80a962738d126541db343e52f20`  
		Last Modified: Sat, 16 Nov 2024 06:50:43 GMT  
		Size: 191.1 MB (191147066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6305cdd2dfe35378729bbf8f4718ffa666f4013ff4d0a2da6155bebfbacb99`  
		Last Modified: Sat, 16 Nov 2024 06:50:46 GMT  
		Size: 312.0 MB (312017824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195bdce8f6ddedfe8eaa61e9a2311a12c83ebb2ec4e2a32d948a6d2823b0e1e5`  
		Last Modified: Sat, 16 Nov 2024 06:50:41 GMT  
		Size: 2.4 MB (2434180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb5d5d08136715afb880623791f150a6b2f671f8b1299e860fc293fe4019527`  
		Last Modified: Sat, 16 Nov 2024 06:50:41 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14d11b717c579d2fd48f667a5c4da79e5e6de6f6949e63688cbc80be7da539d`  
		Last Modified: Sat, 16 Nov 2024 06:50:41 GMT  
		Size: 2.4 KB (2367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5260b5a52f83cca379951a31933815d7a2c010f03c95e5b5d2c05ccd1adce00e`  
		Last Modified: Sat, 16 Nov 2024 06:50:42 GMT  
		Size: 6.6 KB (6591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a274c7601f88918d07649f805d486296d2bb958d1f25c529c1f5b4ae7cf10383`  
		Last Modified: Sat, 16 Nov 2024 06:50:42 GMT  
		Size: 2.5 KB (2508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:e9f4bdcff9e1ed8c2d2477cc70fd61736e6e282867119bc2fdeef042e2f5d7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8832451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20dade21050a104586ed6c1e3ccf9ab32cefb797ebfd5d72ad776f18ddfd30a4`

```dockerfile
```

-	Layers:
	-	`sha256:f9a84300f0a2b7e9f333515f41f4deda127c46376573dc6e99e66bd69b28a2dc`  
		Last Modified: Sat, 16 Nov 2024 06:50:41 GMT  
		Size: 8.8 MB (8789780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21e8f70ae3fc9f72549e5418614e5f15385f9e14e1eb2c20e8cc4718d4628929`  
		Last Modified: Sat, 16 Nov 2024 06:50:41 GMT  
		Size: 42.7 KB (42671 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:4da1a831faf37da1d1ef60b01aa00b1a31c383ec4ae19190301499891e23475b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.2 MB (609213815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74818507881393572fe5ac3fec337ca4bd4707a6fae5590daf92584872e341c4`
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
# Mon, 28 Oct 2024 15:53:54 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 28 Oct 2024 15:53:54 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 15:53:54 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
WORKDIR /usr/local/tomcat
# Mon, 28 Oct 2024 15:53:54 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 28 Oct 2024 15:53:54 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 28 Oct 2024 15:53:54 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 28 Oct 2024 15:53:54 GMT
ENV TOMCAT_MAJOR=9
# Mon, 28 Oct 2024 15:53:54 GMT
ENV TOMCAT_VERSION=9.0.97
# Mon, 28 Oct 2024 15:53:54 GMT
ENV TOMCAT_SHA512=537dbbfc03b37312c2ec282c6906828298cb74e42aca6e3e6835d44bf6923fd8c5db77e98bf6ce9ef19e1922729de53b20546149176e07ac04087df786a62fd9
# Mon, 28 Oct 2024 15:53:54 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 28 Oct 2024 15:53:54 GMT
ENTRYPOINT []
# Mon, 28 Oct 2024 15:53:54 GMT
CMD ["catalina.sh" "run"]
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 28 Oct 2024 15:53:54 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 28 Oct 2024 15:53:54 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
ENV XWIKI_VERSION=16.9.0
# Mon, 28 Oct 2024 15:53:54 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.9.0
# Mon, 28 Oct 2024 15:53:54 GMT
ENV XWIKI_DOWNLOAD_SHA256=9a66ce45c49863c0e8cbdae0fb5e5dfab317a1c0c3a45e7c33fb61b09b39fe23
# Mon, 28 Oct 2024 15:53:54 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MYSQL_JDBC_VERSION=9.1.0
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Mon, 28 Oct 2024 15:53:54 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Mon, 28 Oct 2024 15:53:54 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 28 Oct 2024 15:53:54 GMT
VOLUME [/usr/local/xwiki]
# Mon, 28 Oct 2024 15:53:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 15:53:54 GMT
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
	-	`sha256:9273fed003af261679e273d742d4e75bdafcc7de9d09fa27cace6d34c6d578d9`  
		Last Modified: Sat, 16 Nov 2024 06:52:02 GMT  
		Size: 312.0 MB (312017805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96727bff90dad70a0b3b3897a20723a5bf25a15fe3e6ff1ff8f08b84bad959ae`  
		Last Modified: Sat, 16 Nov 2024 06:51:55 GMT  
		Size: 2.4 MB (2434184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ead911d200816dc4ab7a0142b8fd05d6b0a6f3b0176ac43f3a54015905822d2`  
		Last Modified: Sat, 16 Nov 2024 06:51:55 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526ca7f01d7478f39ccb91f6044dcb9d56969252d3069bf52c14231f9726088a`  
		Last Modified: Sat, 16 Nov 2024 06:51:56 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95a2f58fe2f89690947894a80239eea7c3d143beed782d5c1946e258e7f4b90`  
		Last Modified: Sat, 16 Nov 2024 06:51:56 GMT  
		Size: 6.6 KB (6592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05712f0ae690fdf0eb83c4264a32bb5617cafb63dad5b4b3a9dff91e9cc9d8a`  
		Last Modified: Sat, 16 Nov 2024 06:51:57 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:f92d7f43e7e228d0b12cc871219c8cbc5f3204e8402bd356623f5b3e887a3410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8833496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03679b436c854adf9e661652cd1153f1121c712fa642f4368aba6160c015730a`

```dockerfile
```

-	Layers:
	-	`sha256:ea50eb290a05fcb02c8bab336fca89020aa63459f0ac2a6c65ff60123a5474c3`  
		Last Modified: Sat, 16 Nov 2024 06:51:55 GMT  
		Size: 8.8 MB (8790592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4f4b52da23f29ff820df62a42e388e21c7225955d83f03ee2227b4fa58c048d`  
		Last Modified: Sat, 16 Nov 2024 06:51:54 GMT  
		Size: 42.9 KB (42904 bytes)  
		MIME: application/vnd.in-toto+json
