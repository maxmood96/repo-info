## `xwiki:18-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:467271dd1ee5ac78a846f590fa1cd1b972fdb5026c621dfe5387e0a5cf585f03
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:18-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:bd04d13fa0819a2293ec24c4e141392f5995e5aa35fb9387ba1eb6fe19e300a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.8 MB (653819641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aedeae063160629afdd46516ba99db8f6148cd412f1a3c4fcb4588629379006`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:14:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:14:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:14:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:14:19 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:14:19 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 08:14:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='f3d8843c5a1b77ded3353e0df85d803d84b9faa5ece20673564e7c47fc4591d9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:14:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:14:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:14:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jun 2026 02:13:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 25 Jun 2026 02:13:22 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 02:13:22 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 25 Jun 2026 02:13:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 25 Jun 2026 02:13:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jun 2026 02:13:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jun 2026 02:13:22 GMT
ENV TOMCAT_MAJOR=10
# Thu, 25 Jun 2026 02:13:22 GMT
ENV TOMCAT_VERSION=10.1.56
# Thu, 25 Jun 2026 02:13:22 GMT
ENV TOMCAT_SHA512=8fae99273615eb9d7fbe7ed80abda0ca27647a80f6fcfda98459c5b412d5ef555740b4c4d4af5afae2eb150f1f5bede21ab007ab8cc1f407f508d8908a81b7cc
# Thu, 25 Jun 2026 02:13:22 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 25 Jun 2026 02:13:26 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 02:13:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 25 Jun 2026 02:13:26 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 25 Jun 2026 02:13:26 GMT
ENTRYPOINT []
# Thu, 25 Jun 2026 02:13:26 GMT
CMD ["catalina.sh" "run"]
# Thu, 25 Jun 2026 04:11:55 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 25 Jun 2026 04:11:55 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 25 Jun 2026 04:11:55 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 25 Jun 2026 04:11:55 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 25 Jun 2026 04:11:55 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 25 Jun 2026 04:11:55 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 25 Jun 2026 04:11:55 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 04:11:55 GMT
ENV XWIKI_VERSION=18.4.1
# Thu, 25 Jun 2026 04:11:55 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.4.1
# Thu, 25 Jun 2026 04:11:55 GMT
ENV XWIKI_DOWNLOAD_SHA256=568d3aa4708a5c75d141a978491d800a90d8485afd06e1eb203d003a5a6f8ede
# Thu, 25 Jun 2026 04:12:17 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 25 Jun 2026 04:12:17 GMT
ENV MARIADB_JDBC_VERSION=3.5.8
# Thu, 25 Jun 2026 04:12:17 GMT
ENV MARIADB_JDBC_SHA256=6127dc7858047b3d4482899139640b0e2ab2b8abdeb708cfb8c011117771cddf
# Thu, 25 Jun 2026 04:12:17 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.8
# Thu, 25 Jun 2026 04:12:17 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.8.jar
# Thu, 25 Jun 2026 04:12:17 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.8.jar
# Thu, 25 Jun 2026 04:12:17 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 25 Jun 2026 04:12:17 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 25 Jun 2026 04:12:17 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 25 Jun 2026 04:12:18 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 25 Jun 2026 04:12:18 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 25 Jun 2026 04:12:18 GMT
VOLUME [/usr/local/xwiki]
# Thu, 25 Jun 2026 04:12:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Jun 2026 04:12:18 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9e436cd644d0619bdfd1c8d1dce9e824e836e6102bf4a4c26919785ffe2a7c`  
		Last Modified: Tue, 02 Jun 2026 08:14:35 GMT  
		Size: 17.0 MB (16984112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87482ed64d79af651c4c12177abc09ecb3e56b9d8d0f50a562d2f590d06f86d4`  
		Last Modified: Tue, 02 Jun 2026 08:15:02 GMT  
		Size: 53.1 MB (53123212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc789882cf0d5dbeb8bc4705a9265f34e7a07d131d29a28ab214e03c5848204d`  
		Last Modified: Tue, 02 Jun 2026 08:15:00 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61623c08676d47596865bd7b800628bf28592b0b9ffaedb68600f7ce6243b27`  
		Last Modified: Tue, 02 Jun 2026 08:15:00 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0511e9999bcd27a02849550499c434bf5a04b85d448b6edea21a693ec20faffc`  
		Last Modified: Thu, 25 Jun 2026 02:13:35 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aff57e488da9dbb54d8c18a5b7a7c3afd121063fb34d981a71843516dfee90`  
		Last Modified: Thu, 25 Jun 2026 02:13:35 GMT  
		Size: 14.3 MB (14349294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50ded7df386c999094d43699b85d64540a1b6a56d8dfefc2192ae52a7b99192`  
		Last Modified: Thu, 25 Jun 2026 02:13:35 GMT  
		Size: 3.0 MB (3030334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb42a3abc2dd5f901006d8529b1920d6d4b872985d2737e89105cd112095dd7b`  
		Last Modified: Thu, 25 Jun 2026 04:13:02 GMT  
		Size: 191.2 MB (191223027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c1f75f213c2b17c8cdaf082717771da14e9424663b17fa9bbdd3e6a36bdfdb`  
		Last Modified: Thu, 25 Jun 2026 04:13:06 GMT  
		Size: 344.6 MB (344644625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a184a1ca4dee7ce8c16291221f6c175f96742c44a9045a5479523dccc0fd54a2`  
		Last Modified: Thu, 25 Jun 2026 04:12:55 GMT  
		Size: 712.4 KB (712446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97487dee32df1da2ae90fc4dac1849a511b8d95cc10c8381f93b08b763c281d0`  
		Last Modified: Thu, 25 Jun 2026 04:12:56 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53667505e46c258d805892ed35192a20a5c5c7525baa99109aeae1fa55a12fe5`  
		Last Modified: Thu, 25 Jun 2026 04:12:57 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9239218f448a3511b37b3229649447ad8d4e10f313b155ba4c4ffa672f6f6eb`  
		Last Modified: Thu, 25 Jun 2026 04:12:57 GMT  
		Size: 11.0 KB (10985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d084a60e7ed21a96520933d40edc245076225170dbb803acf0cd5f043131ecf`  
		Last Modified: Thu, 25 Jun 2026 04:12:59 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:18-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:a9d43fe7acaa73a8bda6e494304f860e6e3fc982f9786f87d369c2149ab7bad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9239707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e0f5c58cd26044e6dd6dd3d995ba5249920b2b39fcd8da4e215a2ddc250caa`

```dockerfile
```

-	Layers:
	-	`sha256:f1277e0f95ff360bb6907d2f7c79da9d896ddea62bedcf1574129f5e22c9f734`  
		Last Modified: Thu, 25 Jun 2026 04:12:56 GMT  
		Size: 9.2 MB (9198931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7eef2d5bceb8fc25d31127fb68b5529c535927e20d91c0d1d62c26996595907`  
		Last Modified: Thu, 25 Jun 2026 04:12:55 GMT  
		Size: 40.8 KB (40776 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:18-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:434afea4126f376d9ebdf3561002236c5d0480f9c7703746f851de6270e917f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.9 MB (649912853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce108878c5c786f779400ea4a8f02ba08abd4361659aee33a5938f5945e0563`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:16:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 08:16:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:16:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 08:16:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:16:15 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 02 Jun 2026 08:16:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='f3d8843c5a1b77ded3353e0df85d803d84b9faa5ece20673564e7c47fc4591d9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 02 Jun 2026 08:16:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 08:16:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:16:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jun 2026 02:12:48 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 25 Jun 2026 02:12:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 02:12:48 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 25 Jun 2026 02:12:48 GMT
WORKDIR /usr/local/tomcat
# Thu, 25 Jun 2026 02:12:48 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jun 2026 02:12:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jun 2026 02:12:48 GMT
ENV TOMCAT_MAJOR=10
# Thu, 25 Jun 2026 02:12:48 GMT
ENV TOMCAT_VERSION=10.1.56
# Thu, 25 Jun 2026 02:12:48 GMT
ENV TOMCAT_SHA512=8fae99273615eb9d7fbe7ed80abda0ca27647a80f6fcfda98459c5b412d5ef555740b4c4d4af5afae2eb150f1f5bede21ab007ab8cc1f407f508d8908a81b7cc
# Thu, 25 Jun 2026 02:12:48 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 25 Jun 2026 02:12:53 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 02:12:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 25 Jun 2026 02:12:54 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 25 Jun 2026 02:12:54 GMT
ENTRYPOINT []
# Thu, 25 Jun 2026 02:12:54 GMT
CMD ["catalina.sh" "run"]
# Mon, 29 Jun 2026 19:09:54 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 29 Jun 2026 19:09:54 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 29 Jun 2026 19:09:54 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 29 Jun 2026 19:09:54 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 29 Jun 2026 19:09:54 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 29 Jun 2026 19:09:54 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 29 Jun 2026 19:09:54 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jun 2026 19:09:54 GMT
ENV XWIKI_VERSION=18.5.0
# Mon, 29 Jun 2026 19:09:54 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.5.0
# Mon, 29 Jun 2026 19:09:54 GMT
ENV XWIKI_DOWNLOAD_SHA256=649a5c53bc7ca02d80b3a3dcd1c03a7534ff868b6fe4f6eafa198602bc31c6df
# Mon, 29 Jun 2026 19:10:17 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 29 Jun 2026 19:10:17 GMT
ENV MARIADB_JDBC_VERSION=3.5.9
# Mon, 29 Jun 2026 19:10:17 GMT
ENV MARIADB_JDBC_SHA256=11e3bb5bbf8ef0e806ae4d6c5d5033fedf7262cc777f0190bde8a2f3c8e6bd8d
# Mon, 29 Jun 2026 19:10:17 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.9
# Mon, 29 Jun 2026 19:10:17 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.9.jar
# Mon, 29 Jun 2026 19:10:17 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.9.jar
# Mon, 29 Jun 2026 19:11:09 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 29 Jun 2026 19:11:09 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 29 Jun 2026 19:11:09 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 29 Jun 2026 19:11:09 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 29 Jun 2026 19:11:09 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 29 Jun 2026 19:11:09 GMT
VOLUME [/usr/local/xwiki]
# Mon, 29 Jun 2026 19:11:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:09 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c56d3b03f3eed5e9e98720fc008e29f5ad7edffbb3d0095a9751486b593905e`  
		Last Modified: Tue, 02 Jun 2026 08:16:32 GMT  
		Size: 17.0 MB (16997505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad87a7c029e17f2ca0e18faf162ffda9b94bff8a6c53017932eea8e9d7c8d257`  
		Last Modified: Tue, 02 Jun 2026 08:16:33 GMT  
		Size: 52.3 MB (52314907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a42fa743e77cd7a6e3837c86c2a0c4d959a29959bad6ce7730b2a3c45b1c838`  
		Last Modified: Tue, 02 Jun 2026 08:16:31 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7229c6fba250cd9ec9dea9d2580e679f6a3e697d45386c7d8e63d493bf8134fa`  
		Last Modified: Tue, 02 Jun 2026 08:16:31 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384e21c77bf8435eca6b03f134c29c283a4cc58758713f928a217ee1029073e0`  
		Last Modified: Thu, 25 Jun 2026 02:13:02 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17306b9dbf994913c9c2774b349038212546a1558f34aaf094bc26b9f2b59037`  
		Last Modified: Thu, 25 Jun 2026 02:13:03 GMT  
		Size: 14.4 MB (14352031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461465510cdd039be85c0c637eae3a3d19183c82d849f758283f1b15090458cc`  
		Last Modified: Thu, 25 Jun 2026 02:13:02 GMT  
		Size: 2.8 MB (2829997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be7f43223c38a233456c94e7c731bab898916e321dfeb19b875f3a0b4ddf945`  
		Last Modified: Mon, 29 Jun 2026 19:10:57 GMT  
		Size: 188.9 MB (188876798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06335764f07d681c8a7c9c030c1dca3cecc22de0f14e7764700c7c6388ab4982`  
		Last Modified: Mon, 29 Jun 2026 19:11:00 GMT  
		Size: 344.9 MB (344916504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21ef04b4ce3ac73e8c7b33cd238c33c15aad82ed6698b9478568c032fb3f281`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 728.9 KB (728937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e380a8427f96155d2793644f983a3fd97dfa12cb6837be1e8dcfe63efe9c3fb`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e32286ec2f509ab342d4ffc84a2c6303ad14c2b88626e04aae2281005b34f0`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11cdcfb6383d9dd86ac38c9757082528b1de24057b437c7110c646d9568af3d`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 11.0 KB (10979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf0dc670d5a6c81e1b0501402ec45dbf027349ee067ecf6a9b7a439736d0565`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:18-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:32cb739fcc02aaee8464241800e16c7229a6c6cf4e9d04936f9e443a4dae9fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9242010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9171c40a68bdebbe1e62ec9b1171fdf067611a15f8812cd1d9df807dd987e513`

```dockerfile
```

-	Layers:
	-	`sha256:6382a8bdd78f869e9c96e7ee70674d0e940aeb799af053ffadeb07bd0d260e1d`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 9.2 MB (9201061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b079aaa4e59fbb3e96353cdd32baaaf22d03083a8dda15f6e438d94b6ea0b0`  
		Last Modified: Mon, 29 Jun 2026 19:11:23 GMT  
		Size: 40.9 KB (40949 bytes)  
		MIME: application/vnd.in-toto+json
