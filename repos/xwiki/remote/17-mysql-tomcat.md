## `xwiki:17-mysql-tomcat`

```console
$ docker pull xwiki@sha256:7c10a4540bf1de0d7eb57435c095b8a24d803625ac00e08f9f36b7650877919b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:17-mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:5dc434441b8000d585ab1a57b53f946c74888dd0c7bb6c9abe515cab213df883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.1 MB (628107612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a04670c1fe916bbcd05eb4cb1a61665d6e5a700cce9e2cbfd72ff55757b44d3`
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
# Wed, 10 Sep 2025 10:32:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 10 Sep 2025 10:32:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 10:32:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
WORKDIR /usr/local/tomcat
# Wed, 10 Sep 2025 10:32:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 10 Sep 2025 10:32:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 10 Sep 2025 10:32:40 GMT
ENV TOMCAT_MAJOR=10
# Wed, 10 Sep 2025 10:32:40 GMT
ENV TOMCAT_VERSION=10.1.46
# Wed, 10 Sep 2025 10:32:40 GMT
ENV TOMCAT_SHA512=20da89fa77fb8d4dbfccf6c68383751348169542aad9d3cbcaf82011337355b9847b883cc71678fa6cc71ef3f55e8d5d7a09a53238b86011816fa989f9c4ff5e
# Wed, 10 Sep 2025 10:32:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 10 Sep 2025 10:32:40 GMT
ENTRYPOINT []
# Wed, 10 Sep 2025 10:32:40 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 Sep 2025 10:32:40 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 Sep 2025 10:32:40 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 Sep 2025 10:32:40 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 Sep 2025 10:32:40 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 Sep 2025 10:32:40 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 Sep 2025 10:32:40 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 Sep 2025 10:32:40 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
ENV XWIKI_VERSION=17.7.0
# Wed, 10 Sep 2025 10:32:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.7.0
# Wed, 10 Sep 2025 10:32:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=709d599c0312d23e21dedcb69e8756b05c5085caea78c268fc9806f2a3957edc
# Wed, 10 Sep 2025 10:32:40 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
ENV MYSQL_JDBC_VERSION=9.4.0
# Wed, 10 Sep 2025 10:32:40 GMT
ENV MYSQL_JDBC_SHA256=49ed93c8b2bea9cb0929b85a8a28837b191d0f8eac6919fdcef16e36e2cd53b3
# Wed, 10 Sep 2025 10:32:40 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.4.0
# Wed, 10 Sep 2025 10:32:40 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.4.0.jar
# Wed, 10 Sep 2025 10:32:40 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.4.0.jar
# Wed, 10 Sep 2025 10:32:40 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 Sep 2025 10:32:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 10:32:40 GMT
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
	-	`sha256:1d42cb012e2113b424c87c2249d4fdb3372ca43a9d9d000e3737ad6d6fb2e603`  
		Last Modified: Fri, 12 Sep 2025 23:57:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904b0ebfa358b8794450754ced153ea95fcf91685ee90162daab8864edca4af5`  
		Last Modified: Fri, 12 Sep 2025 23:57:49 GMT  
		Size: 14.1 MB (14091113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac01ab15a8e153842249f48bcbebba1b2d743d7cf61a2eda3341c1553491dce`  
		Last Modified: Fri, 12 Sep 2025 23:57:46 GMT  
		Size: 224.7 KB (224686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec3eef5eae7be9051c971a3450f003947181bddff1e476ba5851738aa30aebf`  
		Last Modified: Sat, 13 Sep 2025 00:10:41 GMT  
		Size: 191.2 MB (191179122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ca8055dea8c00c2e22dea89684f203381165cc6eea6a21f03dad8b1adfa6a8`  
		Last Modified: Sat, 13 Sep 2025 00:11:40 GMT  
		Size: 320.5 MB (320503218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9eef4275dca72ea7ab24b9a7b3dcd003cecca453ff37406b838445ab24b217`  
		Last Modified: Sat, 13 Sep 2025 00:10:25 GMT  
		Size: 2.4 MB (2430458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224e06271801371f03d6e76904b3bd976dd1a3d9e3501e9e139abd72e804f11d`  
		Last Modified: Sat, 13 Sep 2025 00:10:24 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2404b235416626ce4683dfc1c1b7e943b2319eb81908896cdba6057e33c8ba8`  
		Last Modified: Sat, 13 Sep 2025 00:10:24 GMT  
		Size: 2.4 KB (2373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317a2c05c0d677696f2fa38503256be0b2d2767827728d55e07c0aa033366b7c`  
		Last Modified: Sat, 13 Sep 2025 00:10:27 GMT  
		Size: 6.6 KB (6551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654ad0fae1bdd67900dfa07993a58c972108665e9d7c69f42eea5d40d51294a2`  
		Last Modified: Sat, 13 Sep 2025 00:10:24 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:998bbcc79b6aaa6087aea5e11cb195b6ceb7b0ba0c57dedbdd1663ec51c74447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9196592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7339d6b88fe9c3baa5f8c792e10ae2c560e58b3ff76c15b63336bc3eb3e8246`

```dockerfile
```

-	Layers:
	-	`sha256:e35d7180655b9ae7ac49ee95290d23e1e12606139037cf18cacdce2c20177cf2`  
		Last Modified: Sat, 13 Sep 2025 03:07:33 GMT  
		Size: 9.2 MB (9154452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d74546a9802a7516b254d297ab084ec6e895cbfd6e81d7576f474db6d0c3f53`  
		Last Modified: Sat, 13 Sep 2025 03:07:34 GMT  
		Size: 42.1 KB (42140 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:17-mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:77f95cb9cd2575afc8d295e704b0dadaea122f838e92a8ae11c095fc639398a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.1 MB (624114655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1bf4eba3a2984e68c8e78ba9ee9ca61639d601d8bbee76824dd39b0c2228c0`
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
# Wed, 10 Sep 2025 10:32:40 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 10 Sep 2025 10:32:40 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Sep 2025 10:32:40 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
WORKDIR /usr/local/tomcat
# Wed, 10 Sep 2025 10:32:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 10 Sep 2025 10:32:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 10 Sep 2025 10:32:40 GMT
ENV TOMCAT_MAJOR=10
# Wed, 10 Sep 2025 10:32:40 GMT
ENV TOMCAT_VERSION=10.1.46
# Wed, 10 Sep 2025 10:32:40 GMT
ENV TOMCAT_SHA512=20da89fa77fb8d4dbfccf6c68383751348169542aad9d3cbcaf82011337355b9847b883cc71678fa6cc71ef3f55e8d5d7a09a53238b86011816fa989f9c4ff5e
# Wed, 10 Sep 2025 10:32:40 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 10 Sep 2025 10:32:40 GMT
ENTRYPOINT []
# Wed, 10 Sep 2025 10:32:40 GMT
CMD ["catalina.sh" "run"]
# Wed, 10 Sep 2025 10:32:40 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 10 Sep 2025 10:32:40 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 10 Sep 2025 10:32:40 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 10 Sep 2025 10:32:40 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 10 Sep 2025 10:32:40 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 10 Sep 2025 10:32:40 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 10 Sep 2025 10:32:40 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
ENV XWIKI_VERSION=17.7.0
# Wed, 10 Sep 2025 10:32:40 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.7.0
# Wed, 10 Sep 2025 10:32:40 GMT
ENV XWIKI_DOWNLOAD_SHA256=709d599c0312d23e21dedcb69e8756b05c5085caea78c268fc9806f2a3957edc
# Wed, 10 Sep 2025 10:32:40 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
ENV MYSQL_JDBC_VERSION=9.4.0
# Wed, 10 Sep 2025 10:32:40 GMT
ENV MYSQL_JDBC_SHA256=49ed93c8b2bea9cb0929b85a8a28837b191d0f8eac6919fdcef16e36e2cd53b3
# Wed, 10 Sep 2025 10:32:40 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.4.0
# Wed, 10 Sep 2025 10:32:40 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.4.0.jar
# Wed, 10 Sep 2025 10:32:40 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.4.0.jar
# Wed, 10 Sep 2025 10:32:40 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 10 Sep 2025 10:32:40 GMT
VOLUME [/usr/local/xwiki]
# Wed, 10 Sep 2025 10:32:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Sep 2025 10:32:40 GMT
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
	-	`sha256:e0743cc3c68c67c9a8a1dacde1be1488a51f0850d654c457f8065ac6d79d738b`  
		Last Modified: Sat, 13 Sep 2025 00:08:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee57fecc3eb4b1890d12af13395e23c791258988bec7e1620c271b583f72ee3`  
		Last Modified: Sat, 13 Sep 2025 00:08:33 GMT  
		Size: 14.1 MB (14094774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10044cc6484e4c9e516c2bc9c399a591f51045de9ae3c71f0c667727ab7bc03`  
		Last Modified: Sat, 13 Sep 2025 00:08:32 GMT  
		Size: 225.1 KB (225072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99e816be2bf313252f79dd1a7b65a5f209eeb73a08294cf97d163b2324802d1`  
		Last Modified: Sat, 13 Sep 2025 03:07:53 GMT  
		Size: 188.8 MB (188848280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957ac5db66d511d2a9b781a794eab0344d21e51b9121f3ed89f4d9dee2317e10`  
		Last Modified: Sat, 13 Sep 2025 03:08:43 GMT  
		Size: 320.5 MB (320503151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee124c63034ac1cf627e69565073d095b10251f77ef3550cb179c6f9f5d1726`  
		Last Modified: Sat, 13 Sep 2025 01:12:49 GMT  
		Size: 2.4 MB (2430456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009450c86faa47710e9a5c9ec556de23f05e4b61a5aec643f2355cb2537f8431`  
		Last Modified: Sat, 13 Sep 2025 01:12:49 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7d280c815ac5412566bde2204875430b9f7cb41704fa6108005947200f45be`  
		Last Modified: Sat, 13 Sep 2025 01:12:49 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f4458d0b2a285c9639373d51cc73faf74e6794ea1127d7b630abe6944dc51e`  
		Last Modified: Sat, 13 Sep 2025 01:12:49 GMT  
		Size: 6.5 KB (6549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4173c9f380d48d0f07c44e6ba5867ea80cbf0a0992156f2cf848743c0ed387b3`  
		Last Modified: Sat, 13 Sep 2025 01:12:49 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:d9beeab7ca205fe83b30b5cef5702c99082a56f1403d7c583fe2c4e6faae022b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9197638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2955b3dee0bd853b3d76672f213abc9c6e3f828a4b73efe86894bc99d4fbecfe`

```dockerfile
```

-	Layers:
	-	`sha256:5a7078025ff979aea6f59b05e651adcefcfd29dab2ae427b3919968764ffd07b`  
		Last Modified: Sat, 13 Sep 2025 03:07:40 GMT  
		Size: 9.2 MB (9155265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea060322e84f280b1407a8fd8efa22868152fc641c33a4e652cdd13802543268`  
		Last Modified: Sat, 13 Sep 2025 03:07:40 GMT  
		Size: 42.4 KB (42373 bytes)  
		MIME: application/vnd.in-toto+json
