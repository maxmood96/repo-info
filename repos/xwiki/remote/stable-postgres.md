## `xwiki:stable-postgres`

```console
$ docker pull xwiki@sha256:1ae909c327e16eac8da8f11c9c82fe6c9ab5df5b45dfdb5d9c529a3d31fb436a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:ca794874ddd6af077a0d1c16b6ce1f769bb11724c5156d1151c5a4555ee20dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.7 MB (626702945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045df51a2bb33a2a8b8252f856e3cf62bde066989e396c17fb9f031583d91549`
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
ENV POSTGRES_JDBC_VERSION=42.7.7
# Wed, 10 Sep 2025 10:32:40 GMT
ENV POSTGRES_JDBC_SHA256=157963d60ae66d607e09466e8c0cdf8087e9cb20d0159899ffca96bca2528460
# Wed, 10 Sep 2025 10:32:40 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.7
# Wed, 10 Sep 2025 10:32:40 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.7.jar
# Wed, 10 Sep 2025 10:32:40 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.7.jar
# Wed, 10 Sep 2025 10:32:40 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:0e57eb6ea47cb24ae99f823b1872f65edc459bef5d08d49851caaa6f796a52de`  
		Last Modified: Sat, 13 Sep 2025 03:08:59 GMT  
		Size: 191.2 MB (191179683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6830ad39a30498c08f3d3a15dd121ad46812f9500e1c3df3022fc5bebd3858`  
		Last Modified: Sat, 13 Sep 2025 03:09:02 GMT  
		Size: 320.5 MB (320503203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee8049892cb019c1f35940909f302eec1bc0007934dd7cc0956a28d4df6cc4b`  
		Last Modified: Sat, 13 Sep 2025 00:09:24 GMT  
		Size: 1.0 MB (1025254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcd3b4f290ace0c94c918702ec579f7d46648d3215973ba576020c29b0c9094`  
		Last Modified: Sat, 13 Sep 2025 00:09:28 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514eb233c99097603a5bb01d8266d2211be01b97b4342ac07dd8ed1140add255`  
		Last Modified: Sat, 13 Sep 2025 00:09:31 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396a2fbe3744483fa40feda89c7edb99e6e9eb7db1fa6745334b2242f2f87b55`  
		Last Modified: Sat, 13 Sep 2025 00:09:34 GMT  
		Size: 6.5 KB (6549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d6ea56b6f1c9167bad89a1e447d65f5298ae2ec62942c2d8d7c6a9bba054ae`  
		Last Modified: Sat, 13 Sep 2025 00:09:37 GMT  
		Size: 2.4 KB (2419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:dc281d085097594ab1e3e94daf621c4862486faa84682818999521f1032f3ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9193731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d8161f1fa47cb71aadf74abe9b00fabbb5d4d8bd45485d274d580b3f177fa9`

```dockerfile
```

-	Layers:
	-	`sha256:21cdb05a772261fab646ffacd31b6c16c5357f7edd128110e5fa6e66d125e4fc`  
		Last Modified: Sat, 13 Sep 2025 03:07:55 GMT  
		Size: 9.2 MB (9152954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecda25eb038a3abc984a8b90f75d76340b53ebbbb3b0ead8e2c8fe0918126ede`  
		Last Modified: Sat, 13 Sep 2025 03:07:55 GMT  
		Size: 40.8 KB (40777 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:a6da8088cf5de7c42a8d7b62a9ceecd28092f988ecb02889daa56535a6f3b1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.7 MB (622709303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cead638a034b3afe2b48ccde02816c068bacc45e39315a271984f524895a9867`
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
ENV POSTGRES_JDBC_VERSION=42.7.7
# Wed, 10 Sep 2025 10:32:40 GMT
ENV POSTGRES_JDBC_SHA256=157963d60ae66d607e09466e8c0cdf8087e9cb20d0159899ffca96bca2528460
# Wed, 10 Sep 2025 10:32:40 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.7
# Wed, 10 Sep 2025 10:32:40 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.7.jar
# Wed, 10 Sep 2025 10:32:40 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.7.jar
# Wed, 10 Sep 2025 10:32:40 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:3f713f881df0ee640dadb6f42adeceb2ba75578650d859972a2eb70f83408f89`  
		Last Modified: Sat, 13 Sep 2025 01:13:29 GMT  
		Size: 188.8 MB (188848082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb16d16deea89c19fcef1a0c4747db912471d09b48d6d1ead07c97bd5f7a7cf`  
		Last Modified: Sat, 13 Sep 2025 01:13:32 GMT  
		Size: 320.5 MB (320503204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eba3f1e835b69493c8efe77d081bcb236571831cf78ec2255d92c94b5f4ca26`  
		Last Modified: Sat, 13 Sep 2025 01:13:39 GMT  
		Size: 1.0 MB (1025254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975f03e312234f3e7be77b27822d80d8a2f2bcd56c3f19d6db6a6a6be8ddd4a6`  
		Last Modified: Sat, 13 Sep 2025 01:13:38 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaf96ae0912e78c22a0ebb6cd29026b3f93c97b6c324b403d9d56ff99d530d3`  
		Last Modified: Sat, 13 Sep 2025 01:13:38 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f70525f78a86eab2417f8cf9f6fc620af0cda12ead87e7da9fd52c31a39370`  
		Last Modified: Sat, 13 Sep 2025 01:13:38 GMT  
		Size: 6.5 KB (6550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e462c104e6718405c72bc13445d5084127588e2df63d1df1c2cd7f86f1bed10c`  
		Last Modified: Sat, 13 Sep 2025 01:13:38 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:2ff852fe16d07d8793569fd6577dc7ef724fa7e8ee1250f3e00a486ba5815d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9194657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1206a020a9c6185e7d27300cf612aa2ccbaacbd07c0cf991daf48b3aeed4a812`

```dockerfile
```

-	Layers:
	-	`sha256:a62cdac55a24690e9419b54eab56f8215e2ae16d02aba57ba5ddec44efae6585`  
		Last Modified: Sat, 13 Sep 2025 03:08:02 GMT  
		Size: 9.2 MB (9153707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4930a92409dd21cc8599b656782725c4aaed44b20a88afa5f76a1d62f899b63`  
		Last Modified: Sat, 13 Sep 2025 03:08:03 GMT  
		Size: 41.0 KB (40950 bytes)  
		MIME: application/vnd.in-toto+json
