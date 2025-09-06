## `xwiki:lts-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:4c99901da9e254cc05feeef2d56155e224b14349cc106205be126754fbc63552
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:7f2454d35008cc76764196a34aadd014d72119e554426d10365207d74e3fc7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.8 MB (622825153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be177356edb5b9fd5b6ca1fa33206bde33f55728e161fc7f6bd2affd36e61609`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 28 Aug 2025 16:09:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 28 Aug 2025 16:09:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 16:09:51 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
WORKDIR /usr/local/tomcat
# Thu, 28 Aug 2025 16:09:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 28 Aug 2025 16:09:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 28 Aug 2025 16:09:51 GMT
ENV TOMCAT_MAJOR=9
# Thu, 28 Aug 2025 16:09:51 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 28 Aug 2025 16:09:51 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 28 Aug 2025 16:09:51 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 28 Aug 2025 16:09:51 GMT
ENTRYPOINT []
# Thu, 28 Aug 2025 16:09:51 GMT
CMD ["catalina.sh" "run"]
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 28 Aug 2025 16:09:51 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
ENV XWIKI_VERSION=16.10.11
# Thu, 28 Aug 2025 16:09:51 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.11
# Thu, 28 Aug 2025 16:09:51 GMT
ENV XWIKI_DOWNLOAD_SHA256=9c1d464e35ed8f58f7b47213220db7528cd10732a7428eb9f7ee7c29adc83bbd
# Thu, 28 Aug 2025 16:09:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MARIADB_JDBC_VERSION=3.5.5
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MARIADB_JDBC_SHA256=81b9b10dbbd823e5dc9d81bc48435c76d7e92297a8515cfb75bc620917df9baa
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.5
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.5.jar
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.5.jar
# Thu, 28 Aug 2025 16:09:51 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
VOLUME [/usr/local/xwiki]
# Thu, 28 Aug 2025 16:09:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 16:09:51 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f706b5aed643a2746ecfc921e7ee171f3fcda18376f6f8f6b7b86c19198b882f`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 17.0 MB (16971637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929e753abe01a9e7d3af83d05bdc847c5e9a63254f3229de0c0f8e2487a6a389`  
		Last Modified: Mon, 01 Sep 2025 23:08:52 GMT  
		Size: 53.0 MB (52968896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb9a804483712f6cd22000b35e52c918077cb0e199f58858259d849136dd9b5`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a1fad70283ec0319650ea1d3601145209f75ca5b0b26f9e55b61604e68f3a`  
		Last Modified: Mon, 01 Sep 2025 23:08:48 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea5075a8a8386ed6ea8848e61e98d424dba590703cd78eb3461a42fab7c6fdb`  
		Last Modified: Fri, 05 Sep 2025 22:08:44 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9828b77ffce28ff8e71ca5d908ea2e4c48246872225c168e1b476399a1926434`  
		Last Modified: Fri, 05 Sep 2025 22:08:47 GMT  
		Size: 13.7 MB (13721814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d55a7328a548ce186175c6b9a93b4e556f26fb0617336f07b11719fe67f654`  
		Last Modified: Fri, 05 Sep 2025 22:08:44 GMT  
		Size: 224.7 KB (224698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a4cd641a872671431a9cbfaa1b076ba0bd2e940fcc02124f0e5362c5ff4081`  
		Last Modified: Sat, 06 Sep 2025 00:08:00 GMT  
		Size: 191.2 MB (191179021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07124acbdddabd656aaa4f049a202441f3331cd457d7b8cf8bf4d25cb3f0a544`  
		Last Modified: Sat, 06 Sep 2025 00:09:00 GMT  
		Size: 317.3 MB (317325738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9fe31a1794817ea3984f54cbf672502a8abc2178ddb52116dec5a192264307`  
		Last Modified: Fri, 05 Sep 2025 23:09:06 GMT  
		Size: 694.9 KB (694905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8454df5bae01f1a5c0809c5e69d0ca7b2fda2a5e5cb02709e5d926d1ca6b5109`  
		Last Modified: Fri, 05 Sep 2025 23:09:06 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431c5fd24ec6423ce854a01510e6afee0267ee5dfea6a8ce726cb2fb565e65cf`  
		Last Modified: Fri, 05 Sep 2025 23:09:06 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185ad08324f0aeec0b74e7c2e755c02ec757de4f800ae28b7f31e96b5363682e`  
		Last Modified: Fri, 05 Sep 2025 23:09:06 GMT  
		Size: 6.6 KB (6624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac2f80edddb8634d803931ed3800b5ebc173e9895b224d2227d03fb9c2cd69e`  
		Last Modified: Fri, 05 Sep 2025 23:09:06 GMT  
		Size: 2.5 KB (2469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:925b0f8b00ce679833b31afb52b53b4a424d7c81b4d5e88a5a06578d181db98d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9150009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a596dbf71ed41950398914b0c7b1a19c2dbbf5ac723d660f8c7f4d23a27b37f8`

```dockerfile
```

-	Layers:
	-	`sha256:4880a1a2d958d2a52da915374aeb3b4626ee8219e8558f38dfffd699f1ea9fc2`  
		Last Modified: Sat, 06 Sep 2025 00:07:32 GMT  
		Size: 9.1 MB (9109519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9053715998d0cd8619f134f4eab3cd8822703b7d26a12d0a5348bade5d3a8197`  
		Last Modified: Sat, 06 Sep 2025 00:07:33 GMT  
		Size: 40.5 KB (40490 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:2d99b3d9acc5bb98ecca5ed75c286ded4308cd66d465892e5033269fc9c262f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.8 MB (618829496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec9f01a4a4f81d9d3f193b6dea2665a7055d1600d7ce2a6247d9f751f7a37a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 28 Aug 2025 16:09:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 28 Aug 2025 16:09:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 16:09:51 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
WORKDIR /usr/local/tomcat
# Thu, 28 Aug 2025 16:09:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 28 Aug 2025 16:09:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 28 Aug 2025 16:09:51 GMT
ENV TOMCAT_MAJOR=9
# Thu, 28 Aug 2025 16:09:51 GMT
ENV TOMCAT_VERSION=9.0.109
# Thu, 28 Aug 2025 16:09:51 GMT
ENV TOMCAT_SHA512=29341c17d92b8f72700c7e0626405a63f3ba30737019fbe6a25cafbd929c5e14aa99817e1d4990da11593400e8e5977da9f9f7f9c097d95f820783f33a3cf9b7
# Thu, 28 Aug 2025 16:09:51 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 28 Aug 2025 16:09:51 GMT
ENTRYPOINT []
# Thu, 28 Aug 2025 16:09:51 GMT
CMD ["catalina.sh" "run"]
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 28 Aug 2025 16:09:51 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 28 Aug 2025 16:09:51 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
ENV XWIKI_VERSION=16.10.11
# Thu, 28 Aug 2025 16:09:51 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.11
# Thu, 28 Aug 2025 16:09:51 GMT
ENV XWIKI_DOWNLOAD_SHA256=9c1d464e35ed8f58f7b47213220db7528cd10732a7428eb9f7ee7c29adc83bbd
# Thu, 28 Aug 2025 16:09:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MARIADB_JDBC_VERSION=3.5.5
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MARIADB_JDBC_SHA256=81b9b10dbbd823e5dc9d81bc48435c76d7e92297a8515cfb75bc620917df9baa
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.5
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.5.jar
# Thu, 28 Aug 2025 16:09:51 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.5.jar
# Thu, 28 Aug 2025 16:09:51 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:09:51 GMT
VOLUME [/usr/local/xwiki]
# Thu, 28 Aug 2025 16:09:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 16:09:51 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82cb5b65623a0098d812fc3093e05fc877923cbe33814d2fdf26bfedfdc87fd`  
		Last Modified: Tue, 02 Sep 2025 01:00:01 GMT  
		Size: 17.0 MB (16988801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72895f8f6f6835766f4384b901cd9c849917e812386a716749233cc434286843`  
		Last Modified: Tue, 02 Sep 2025 01:07:12 GMT  
		Size: 52.1 MB (52148466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45da3a415496054b89e56e8796d3666d99d3a2023fd8d8f06b08fdba77c007a0`  
		Last Modified: Tue, 02 Sep 2025 01:07:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7646f1148db19c8d26d28f2132c9793bee48765609d023530dff185a5a6a36`  
		Last Modified: Tue, 02 Sep 2025 01:07:03 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0cea438020fce42ff4149bf9876824d674dc04264b5bc85f2ce081df667f21`  
		Last Modified: Tue, 02 Sep 2025 09:39:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642c294e71fa997ceec26887bda9de5baead8aec2b84536194381b97cb9df173`  
		Last Modified: Fri, 05 Sep 2025 22:31:46 GMT  
		Size: 13.7 MB (13731842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f52c04ec7fc61894de65a60fcb2a64f115749d8911465cd6d08686677f3232a`  
		Last Modified: Fri, 05 Sep 2025 22:31:44 GMT  
		Size: 225.1 KB (225103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7eabb4d43e300ac39ec042a44fa85627a31465c4503f513c8bf7eefec6189`  
		Last Modified: Sat, 06 Sep 2025 14:38:23 GMT  
		Size: 188.8 MB (188839121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc30aae9b8629c163612b0d60dc89fb235191b9b6d5b64dc33efcc704d5f5b5`  
		Last Modified: Sat, 06 Sep 2025 14:39:02 GMT  
		Size: 317.3 MB (317325606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c144f21cfe287f3919d6d351f5bb078f9fd3de747f80863ded8f5c5894ebbc6d`  
		Last Modified: Fri, 05 Sep 2025 23:11:50 GMT  
		Size: 694.9 KB (694914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3fc13be5059c9a0c577785bb17e3ecae5178dcce318d1768aa51eae35592f5`  
		Last Modified: Fri, 05 Sep 2025 23:11:49 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4765f8c67d5834b66f5e4953be2ad8ba00eaa26828220112b22a71ceb8095b2`  
		Last Modified: Fri, 05 Sep 2025 23:11:49 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cac1dd45df7f5789eb29b9ac5a241d7e9ae9257afb2eed1c5737b3f71a2d359`  
		Last Modified: Fri, 05 Sep 2025 23:11:50 GMT  
		Size: 6.6 KB (6628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de327921177ca0132d4b1b973d5d0d08eb8c288f5bc28a76cd8d2c586665c41b`  
		Last Modified: Fri, 05 Sep 2025 23:11:50 GMT  
		Size: 2.5 KB (2476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:0a4ec6de8a96721d93864b00371dc1aa0f137bd56f3e1d302b21e53e13efae64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9150911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec22ccc88ff2636d1149f674e9f0692471e5cf5c41542a44ad14ec8848d8b12`

```dockerfile
```

-	Layers:
	-	`sha256:616b020dd11d291667cca8e4a9c72319123d04cbdcb5977ce6d3b9b2e9bd9c60`  
		Last Modified: Sat, 06 Sep 2025 00:08:04 GMT  
		Size: 9.1 MB (9110260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea67028f249796e1cc5df79f8d634f05eb1110353d4760afc4da211118dcac8`  
		Last Modified: Sat, 06 Sep 2025 00:08:05 GMT  
		Size: 40.7 KB (40651 bytes)  
		MIME: application/vnd.in-toto+json
