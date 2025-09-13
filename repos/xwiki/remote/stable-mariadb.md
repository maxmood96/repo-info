## `xwiki:stable-mariadb`

```console
$ docker pull xwiki@sha256:7301fbacbc7835893169aff5302fd1e0cf8596e3cae200007ba4b5008c16c1f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:d2da5b7b5c3c32a4a4b98a5467f6060adfe56dcb16ef60441dc75b5b51097916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.4 MB (626372336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c30732a099ec1ff88bb2eb8fb9f91ac2ea677e1404415812ee6e27d16a540b`
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
ENV MARIADB_JDBC_VERSION=3.5.5
# Wed, 10 Sep 2025 10:32:40 GMT
ENV MARIADB_JDBC_SHA256=81b9b10dbbd823e5dc9d81bc48435c76d7e92297a8515cfb75bc620917df9baa
# Wed, 10 Sep 2025 10:32:40 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.5
# Wed, 10 Sep 2025 10:32:40 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.5.jar
# Wed, 10 Sep 2025 10:32:40 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.5.jar
# Wed, 10 Sep 2025 10:32:40 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:06f75e6f67d9cb032b7109df1b96be764e92cdaf5d21d4b0020154f486fec8e8`  
		Last Modified: Sat, 13 Sep 2025 03:29:23 GMT  
		Size: 191.2 MB (191179576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92c1b85169da7c3ef53d363a0cab211fd0af1d15d0d581f5af4a67ad1522dd5`  
		Last Modified: Sat, 13 Sep 2025 03:29:38 GMT  
		Size: 320.5 MB (320503144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbfa478ce70cdffb9592f1446173bac3fea99c6d8ef6ecc649ee6bcfaad3294`  
		Last Modified: Sat, 13 Sep 2025 00:10:48 GMT  
		Size: 694.9 KB (694912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b834e7d2f8aa253bdc4af8d32ba9fa4d40d75911bfb66b447a0d2a78eb133cb`  
		Last Modified: Sat, 13 Sep 2025 00:10:48 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cc163d5fd91817701a4a3fd996877210ec98d6927224428c367b8eae626b84`  
		Last Modified: Sat, 13 Sep 2025 00:10:49 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fedc2a075fa1354ea0ac7ef45187df8ccf2635b056059575a4b258f7f8f72c`  
		Last Modified: Sat, 13 Sep 2025 00:10:48 GMT  
		Size: 6.5 KB (6548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d9a32e51ddbd9bfc3c69fe0f57e04065d1c50f7e38bbf9bd1467083f0306ed`  
		Last Modified: Sat, 13 Sep 2025 00:10:48 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:5c716d362745fccc9d20f26a96c5a01c4d667c31a0abb18a23ca1b5526c794bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9193738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b1c4ed737ad6963eb7bb910c534b75dbffab5f0de1e71ed166a73ac2d81ed2`

```dockerfile
```

-	Layers:
	-	`sha256:8a73fd8203453eeaa78a1fbf305a64e9fbb395a18a4d06fb1c023c5bf9b7fc42`  
		Last Modified: Sat, 13 Sep 2025 03:07:38 GMT  
		Size: 9.2 MB (9152937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50aa4270fe3d2b2890a5943fd9d68bedf7c37eccfc336ea5280a83eb1f84745e`  
		Last Modified: Sat, 13 Sep 2025 03:07:39 GMT  
		Size: 40.8 KB (40801 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:3071e7a17e49ecf89925dcc152e0612536e4b54d472f7f296363d0fe1c25503d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.4 MB (622379124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60dd71bdd2eea4566e2f8463d69580d9c40e67866035562b56e5610c7fd823f`
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
ENV MARIADB_JDBC_VERSION=3.5.5
# Wed, 10 Sep 2025 10:32:40 GMT
ENV MARIADB_JDBC_SHA256=81b9b10dbbd823e5dc9d81bc48435c76d7e92297a8515cfb75bc620917df9baa
# Wed, 10 Sep 2025 10:32:40 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.5
# Wed, 10 Sep 2025 10:32:40 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.5.jar
# Wed, 10 Sep 2025 10:32:40 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.5.jar
# Wed, 10 Sep 2025 10:32:40 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:11bf07389485832f58034e13dc5c9ad5f23ca282ed8f23f0565112f9b89e5c45`  
		Last Modified: Sat, 13 Sep 2025 02:09:56 GMT  
		Size: 188.8 MB (188848305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164bfd18e66d07e001277435f2412d480c9c06940f024cb5cd0753f76269f38d`  
		Last Modified: Sat, 13 Sep 2025 02:10:35 GMT  
		Size: 320.5 MB (320503231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c8d5683b653cd3c452b5a5ee543d33b83dac80c1e8e71429ab970ad4ff3afe`  
		Last Modified: Sat, 13 Sep 2025 01:13:39 GMT  
		Size: 694.9 KB (694914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae1e9ae61d9267dccc0b897d75bdcba0b1bc223f68bf958b7cddad744723c21`  
		Last Modified: Sat, 13 Sep 2025 01:13:38 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f50bc1581ea60ca26c0efb98fe1d5211c9e06d66c1b8261a8d6ca5c2beb1ce2`  
		Last Modified: Sat, 13 Sep 2025 01:13:39 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79b121bf250ac514bd0eaecaeecf0463292f6aa1f5ff621f4e7b6784f70d053`  
		Last Modified: Sat, 13 Sep 2025 01:13:39 GMT  
		Size: 6.6 KB (6551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec1e1fb0cc08faee426dc3dd97c989e60161c8f39bf25e5e191aef86f215f33`  
		Last Modified: Sat, 13 Sep 2025 01:13:39 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:226ffa9eb15c91469c6fd2c62d1eecf049c8302013a7ce51dbcc7469377f1899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9194664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09c9d0e19d63d682fb7cf18465f6804b8eebecadcd227f7eb7b082e14e027aa`

```dockerfile
```

-	Layers:
	-	`sha256:1da9f3ba0e2b03b39de51d4b4ab3e1d01ab813310066c8ac915fe3e066063626`  
		Last Modified: Sat, 13 Sep 2025 03:07:45 GMT  
		Size: 9.2 MB (9153690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d84bf9f60728770995a71314c921bf494bdb9360ade53376154605e3df6f01aa`  
		Last Modified: Sat, 13 Sep 2025 03:07:46 GMT  
		Size: 41.0 KB (40974 bytes)  
		MIME: application/vnd.in-toto+json
