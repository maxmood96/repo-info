## `xwiki:mysql-tomcat`

```console
$ docker pull xwiki@sha256:df890a6f34cd8e3b41a2b47f67728dbaab3285e7f71f6947dca9cd26783053c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:d1d9dbbcd404f1cc9530f40d444f72f47bfe1d287b07b8bb8581a8a9681bf5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.1 MB (628101884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cbee60139c40399a51c5b7ebed0ef97dfa790aefeff7a81cfab66b175c9384`
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
# Thu, 28 Aug 2025 10:13:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 28 Aug 2025 10:13:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 10:13:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 28 Aug 2025 10:13:21 GMT
WORKDIR /usr/local/tomcat
# Thu, 28 Aug 2025 10:13:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 28 Aug 2025 10:13:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 28 Aug 2025 10:13:21 GMT
ENV TOMCAT_MAJOR=10
# Thu, 28 Aug 2025 10:13:21 GMT
ENV TOMCAT_VERSION=10.1.45
# Thu, 28 Aug 2025 10:13:21 GMT
ENV TOMCAT_SHA512=2ebff699600c7a11c26e2d166eea3fa4851f894784b87f58555c6f53f4240cec836eef042fc74426959a58d41e68525f015c5f86ca35231b3d19dee07e82abc0
# Thu, 28 Aug 2025 10:13:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 28 Aug 2025 10:13:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 10:13:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 28 Aug 2025 10:13:21 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 28 Aug 2025 10:13:21 GMT
ENTRYPOINT []
# Thu, 28 Aug 2025 10:13:21 GMT
CMD ["catalina.sh" "run"]
# Thu, 28 Aug 2025 10:13:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 28 Aug 2025 10:13:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 28 Aug 2025 10:13:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 28 Aug 2025 10:13:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 28 Aug 2025 10:13:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 28 Aug 2025 10:13:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 28 Aug 2025 10:13:21 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 10:13:21 GMT
ENV XWIKI_VERSION=17.7.0
# Thu, 28 Aug 2025 10:13:21 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.7.0
# Thu, 28 Aug 2025 10:13:21 GMT
ENV XWIKI_DOWNLOAD_SHA256=709d599c0312d23e21dedcb69e8756b05c5085caea78c268fc9806f2a3957edc
# Thu, 28 Aug 2025 10:13:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 28 Aug 2025 10:13:21 GMT
ENV MYSQL_JDBC_VERSION=9.4.0
# Thu, 28 Aug 2025 10:13:21 GMT
ENV MYSQL_JDBC_SHA256=49ed93c8b2bea9cb0929b85a8a28837b191d0f8eac6919fdcef16e36e2cd53b3
# Thu, 28 Aug 2025 10:13:21 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.4.0
# Thu, 28 Aug 2025 10:13:21 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.4.0.jar
# Thu, 28 Aug 2025 10:13:21 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.4.0.jar
# Thu, 28 Aug 2025 10:13:21 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 28 Aug 2025 10:13:21 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 28 Aug 2025 10:13:21 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 28 Aug 2025 10:13:21 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 28 Aug 2025 10:13:21 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 10:13:21 GMT
VOLUME [/usr/local/xwiki]
# Thu, 28 Aug 2025 10:13:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 10:13:21 GMT
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
	-	`sha256:498d622aef1f0defb601d33ceff84d8c2ed9df5c055de2afd7dcf4c9ca1b1ce2`  
		Last Modified: Mon, 08 Sep 2025 22:13:57 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fbe92740ca978a4b88631e1ad6d9d4a458bc847bdf04022a19c23161185153`  
		Last Modified: Mon, 08 Sep 2025 22:13:59 GMT  
		Size: 14.1 MB (14085647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e9dee6b90b5e2ec45e55946a0bfdef6f8eb46ee435ec8112d577aae98d5d76`  
		Last Modified: Mon, 08 Sep 2025 22:13:57 GMT  
		Size: 224.7 KB (224688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d021e477a0b2a0797efeb960bcd1dd3ef1dbf558d69939ad30f2dbdf85c1f05`  
		Last Modified: Tue, 09 Sep 2025 00:11:15 GMT  
		Size: 191.2 MB (191178860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76467f8dcfc8b49b90470d68899d5a0d502bff9ca2db0b15b8308a1f1b19549`  
		Last Modified: Tue, 09 Sep 2025 00:09:39 GMT  
		Size: 320.5 MB (320503217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d031b14268114ce89c823e2b31cc4956ba84849e31d1992d2b6a7dde339e7170`  
		Last Modified: Mon, 08 Sep 2025 22:48:47 GMT  
		Size: 2.4 MB (2430452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfa2ebc00e09cfa68334b702fe7c373cf38567a1710378532a0436926d58493`  
		Last Modified: Mon, 08 Sep 2025 22:48:51 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5534c428b96237773d2e7847c25e8577e617c575aeb09dc6e8fb39264b1c9d77`  
		Last Modified: Mon, 08 Sep 2025 22:48:56 GMT  
		Size: 2.4 KB (2374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc07762a66242a3f4adf05a751013637f536c5c2cbad1c7f649b35e07d84ecd`  
		Last Modified: Mon, 08 Sep 2025 22:48:59 GMT  
		Size: 6.6 KB (6551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a4b4002bdcf1b0069014242748d97b090179ee03b8492dc5ff0b0727186ab9`  
		Last Modified: Mon, 08 Sep 2025 22:49:02 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:66792be433a32bd8897bf67a3009fbc7f976eb3e02bedbf77be410c17d3e9ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9196592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b63d89953310b0600c5afaff8e655c41e2c783cc0f04e02a54b18e6de3607c`

```dockerfile
```

-	Layers:
	-	`sha256:9a4882093d1674b5e544b6e695687765513b343835ad430afbe91d7ae845de2c`  
		Last Modified: Tue, 09 Sep 2025 00:07:24 GMT  
		Size: 9.2 MB (9154452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9c1d4d7dd03a0d3cb273b0f435a86157887e62af63577d8e918d8a425a7100`  
		Last Modified: Tue, 09 Sep 2025 00:07:25 GMT  
		Size: 42.1 KB (42140 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:cb3773e6705562a6ba158ca3a2de9a9fad2c2a0357c9e0ab8d315c159ca7f8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.1 MB (624094673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e4024adae38f3111f00716d770c824a515458bafed2f69b59ab89b9bebe77f`
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
# Thu, 07 Aug 2025 16:46:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 07 Aug 2025 16:46:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Aug 2025 16:46:24 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
WORKDIR /usr/local/tomcat
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 07 Aug 2025 16:46:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_MAJOR=10
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_VERSION=10.1.44
# Thu, 07 Aug 2025 16:46:24 GMT
ENV TOMCAT_SHA512=efc5f010d2c35c7f930b8d53e809eb72ac95675e739c9678e617f42c704ebe6410676071b1118c429cc84eb651e50241fd8fe4bf21be8f3a12d00e9fb28e1610
# Thu, 07 Aug 2025 16:46:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 07 Aug 2025 16:46:24 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 07 Aug 2025 16:46:24 GMT
ENTRYPOINT []
# Thu, 07 Aug 2025 16:46:24 GMT
CMD ["catalina.sh" "run"]
# Thu, 28 Aug 2025 10:13:21 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 28 Aug 2025 10:13:21 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 28 Aug 2025 10:13:21 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 28 Aug 2025 10:13:21 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 28 Aug 2025 10:13:21 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 28 Aug 2025 10:13:21 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 28 Aug 2025 10:13:21 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 10:13:21 GMT
ENV XWIKI_VERSION=17.7.0
# Thu, 28 Aug 2025 10:13:21 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.7.0
# Thu, 28 Aug 2025 10:13:21 GMT
ENV XWIKI_DOWNLOAD_SHA256=709d599c0312d23e21dedcb69e8756b05c5085caea78c268fc9806f2a3957edc
# Thu, 28 Aug 2025 10:13:21 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 28 Aug 2025 10:13:21 GMT
ENV MYSQL_JDBC_VERSION=9.4.0
# Thu, 28 Aug 2025 10:13:21 GMT
ENV MYSQL_JDBC_SHA256=49ed93c8b2bea9cb0929b85a8a28837b191d0f8eac6919fdcef16e36e2cd53b3
# Thu, 28 Aug 2025 10:13:21 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.4.0
# Thu, 28 Aug 2025 10:13:21 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.4.0.jar
# Thu, 28 Aug 2025 10:13:21 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.4.0.jar
# Thu, 28 Aug 2025 10:13:21 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 28 Aug 2025 10:13:21 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 28 Aug 2025 10:13:21 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 28 Aug 2025 10:13:21 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 28 Aug 2025 10:13:21 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 10:13:21 GMT
VOLUME [/usr/local/xwiki]
# Thu, 28 Aug 2025 10:13:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Aug 2025 10:13:21 GMT
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
	-	`sha256:58f6680c6dc5a30aa9c76929111a70948018f1661ee099200b6a26a071fdd05a`  
		Last Modified: Tue, 02 Sep 2025 09:41:40 GMT  
		Size: 14.1 MB (14083912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe31871bfc68e4339e1df38296e202fd5015c18fb92ec3d17b9fa58df1e2bfa`  
		Last Modified: Tue, 02 Sep 2025 09:41:39 GMT  
		Size: 225.1 KB (225056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a58b30e44cc8c68011d5b00ce08023b3aadccdde9bca2918d87d1a5eaff9ce`  
		Last Modified: Tue, 02 Sep 2025 15:58:33 GMT  
		Size: 188.8 MB (188839164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89031b881465b6c94b7d64e8e9ef28607f0ed8bc67db2a3767ed66e2629f8a4`  
		Last Modified: Tue, 02 Sep 2025 15:59:14 GMT  
		Size: 320.5 MB (320503155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a857cbe19a4e4b2e2237b2106608877251956d97f837e20fd4dd05b479d7c377`  
		Last Modified: Tue, 02 Sep 2025 10:57:13 GMT  
		Size: 2.4 MB (2430455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b9fe79ebd784d79e765b2c02277525d9df269b257a84a2b1891ef9f5ac0f6e`  
		Last Modified: Tue, 02 Sep 2025 10:57:13 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c217992e55f0510c270f5e0a9d6d52ab695f43587082b41f009d4f70ba92d98`  
		Last Modified: Tue, 02 Sep 2025 10:57:13 GMT  
		Size: 2.4 KB (2373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d4ca994739b4bb40eb04cccf8e6d59d0e478275de34569fb0ee3a3e5dfb48b`  
		Last Modified: Tue, 02 Sep 2025 10:57:13 GMT  
		Size: 6.6 KB (6553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dee79127c2d060c74b14ea66e94ac11a08043e42712525a9507facc26fe4fa`  
		Last Modified: Tue, 02 Sep 2025 10:57:13 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:891b3e43c6bec733dda0c3a0fa513023b8918aa3fa027eef486cffdd710107a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9197638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:215f93c167bfc0689b9bc3eeca1b33a5bc42a80282b900c8cac612a8fceb3979`

```dockerfile
```

-	Layers:
	-	`sha256:05d2c402d50ce11af8629b33b3320b22fa82b643b396d8ac8a4ede4adda0e9e6`  
		Last Modified: Tue, 02 Sep 2025 12:07:59 GMT  
		Size: 9.2 MB (9155265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02bcc72550195acad3c66bb04a9fba3fcb0feaacef7ac6f8058b624fd9c46d79`  
		Last Modified: Tue, 02 Sep 2025 12:08:00 GMT  
		Size: 42.4 KB (42373 bytes)  
		MIME: application/vnd.in-toto+json
