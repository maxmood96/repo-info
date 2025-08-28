## `xwiki:17-postgres-tomcat`

```console
$ docker pull xwiki@sha256:f13b05113230f1c6b54e801251883172dc544daa49084126f18e9819735a3d12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:17-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:8a59e59dbda6cfc8d52c9b564798f8afde9075e957e799776bf1c462607249ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.7 MB (626680819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c28b8785cc1debc4e8731d761fde28a0e489675e5d8678cce198a7bd0ed6c91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
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
ENV POSTGRES_JDBC_VERSION=42.7.4
# Thu, 28 Aug 2025 10:13:21 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Thu, 28 Aug 2025 10:13:21 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Thu, 28 Aug 2025 10:13:21 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Thu, 28 Aug 2025 10:13:21 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Thu, 28 Aug 2025 10:13:21 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1ceb63b80a861ae319235f3b1e3e392279a30c5cc9f0dec5c5582505b55f8`  
		Last Modified: Tue, 12 Aug 2025 17:24:47 GMT  
		Size: 17.0 MB (16971683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62b74addfec2b46a83d8e9d131c7c6563aa4399f142b91d977d506f6c137dcb`  
		Last Modified: Tue, 12 Aug 2025 17:25:01 GMT  
		Size: 53.0 MB (52968913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ac95b0cea99b9ed5ddc084d329fc5e139c2adde65e599e4f9803bd9aa474ef`  
		Last Modified: Tue, 12 Aug 2025 17:24:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cce32af8d45a5194c78928090c5748f048a001dcd13b737c7a2992892753871`  
		Last Modified: Tue, 12 Aug 2025 17:24:49 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26601cb9a1d4d844a296eb3e1788428e0f0ed793b7b7d2c299692fedf35d5740`  
		Last Modified: Tue, 12 Aug 2025 18:08:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858c4b60ed3f0a36f7205bdeca07b3161e5ba5259b116fa63b99c1ae8d741852`  
		Last Modified: Tue, 12 Aug 2025 18:08:45 GMT  
		Size: 14.1 MB (14081081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657236842a194fb380adac21a58c1578dcbac33ce697252d79d5fe9d464ce534`  
		Last Modified: Tue, 12 Aug 2025 18:08:45 GMT  
		Size: 224.7 KB (224702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88be4e42ceb3276d47ca4e456aa115e7e891d8ce72b26fa181a443a29015747`  
		Last Modified: Thu, 28 Aug 2025 18:10:54 GMT  
		Size: 191.2 MB (191179022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617146224632a850ee971d0876e1afdf441c5693946d09c834f054900d4af09a`  
		Last Modified: Thu, 28 Aug 2025 18:10:47 GMT  
		Size: 320.5 MB (320503149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d319690e81515f68b11ffe27e4ead7c3ec1d6685a2f62fc593344e62f959c6`  
		Last Modified: Thu, 28 Aug 2025 17:52:38 GMT  
		Size: 1.0 MB (1013638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ee5fff2c5e0c04267eaf14914e612b44cc799301687601d500575896253237`  
		Last Modified: Thu, 28 Aug 2025 17:52:38 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3ad65e0ff1dc457079faeb5808c157e2f66e429b29da9e784417e584f37a00`  
		Last Modified: Thu, 28 Aug 2025 17:52:38 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95e65c9d8d2f7d462b8c87d12b4a3d72295600b335675a49dc98f8f9e25ba11`  
		Last Modified: Thu, 28 Aug 2025 17:52:38 GMT  
		Size: 6.5 KB (6550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c967acf2eff99ba4e07485d0949354a2885b526ecbd5fe1197aa882676b995d`  
		Last Modified: Thu, 28 Aug 2025 17:52:38 GMT  
		Size: 2.4 KB (2417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:9bb2e5d718e148650118064f5e1a2d9f43c87730fbba8e4dffb05dd202ca2a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9193732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c5138ae3b16fc7beac7dca5f0c680ae6566aeebb9ab46672907d6cd3c5d345`

```dockerfile
```

-	Layers:
	-	`sha256:25bc9e48956c95d2fc59a1010c4646e39865ec5e88cb2c2918831cc69bf2e965`  
		Last Modified: Thu, 28 Aug 2025 18:08:13 GMT  
		Size: 9.2 MB (9152954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d66b2fe5a64e73c9df74035c674dfc279033da0d9dcb92f269c20c72e57dd0`  
		Last Modified: Thu, 28 Aug 2025 18:08:14 GMT  
		Size: 40.8 KB (40778 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:17-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:d1e0af211807b791f6940e2086de7686b6f01a399acdd71a9929d46452940906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.4 MB (622407232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082830e6715002bb56b672279288950ccc25f28ba4c95c9be93f544dc855f0db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 28 Jul 2025 13:28:25 GMT
ARG RELEASE
# Mon, 28 Jul 2025 13:28:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Jul 2025 13:28:25 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Mon, 28 Jul 2025 13:28:25 GMT
CMD ["/bin/bash"]
# Mon, 28 Jul 2025 13:28:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Jul 2025 13:28:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Jul 2025 13:28:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Jul 2025 13:28:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Mon, 28 Jul 2025 13:28:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Jul 2025 13:28:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 28 Jul 2025 13:28:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Jul 2025 13:28:25 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
WORKDIR /usr/local/tomcat
# Mon, 28 Jul 2025 13:28:25 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 28 Jul 2025 13:28:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 28 Jul 2025 13:28:25 GMT
ENV TOMCAT_MAJOR=10
# Mon, 28 Jul 2025 13:28:25 GMT
ENV TOMCAT_VERSION=10.1.44
# Mon, 28 Jul 2025 13:28:25 GMT
ENV TOMCAT_SHA512=efc5f010d2c35c7f930b8d53e809eb72ac95675e739c9678e617f42c704ebe6410676071b1118c429cc84eb651e50241fd8fe4bf21be8f3a12d00e9fb28e1610
# Mon, 28 Jul 2025 13:28:25 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 28 Jul 2025 13:28:25 GMT
ENTRYPOINT []
# Mon, 28 Jul 2025 13:28:25 GMT
CMD ["catalina.sh" "run"]
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 28 Jul 2025 13:28:25 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
ENV XWIKI_VERSION=17.6.0
# Mon, 28 Jul 2025 13:28:25 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.6.0
# Mon, 28 Jul 2025 13:28:25 GMT
ENV XWIKI_DOWNLOAD_SHA256=3a5f30089da81f41e861a90814c82e819daad5fc63d1d112573dd3671e9f3d47
# Mon, 28 Jul 2025 13:28:25 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
ENV POSTGRES_JDBC_VERSION=42.7.4
# Mon, 28 Jul 2025 13:28:25 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Mon, 28 Jul 2025 13:28:25 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Mon, 28 Jul 2025 13:28:25 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Mon, 28 Jul 2025 13:28:25 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Mon, 28 Jul 2025 13:28:25 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
VOLUME [/usr/local/xwiki]
# Mon, 28 Jul 2025 13:28:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Jul 2025 13:28:25 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3eefddfbcab06ca4f10ce56a232d4ec2d822b72ac91b8958abc9acd3c4223c`  
		Last Modified: Tue, 12 Aug 2025 18:31:54 GMT  
		Size: 17.0 MB (16988833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2683f57ecc3239b77668933adbcb066b796b3d8385694028dfa534473428efe9`  
		Last Modified: Tue, 12 Aug 2025 18:39:53 GMT  
		Size: 52.1 MB (52148453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1835951682aea5916d97b15850e70d45156732945ac0dbb2535d8c6306228f`  
		Last Modified: Tue, 12 Aug 2025 18:39:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766ee17d70f62cab7ff1f4f47b0567a37c24335c88c58b652cb5b22e4f7e92e0`  
		Last Modified: Tue, 12 Aug 2025 18:39:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8672b50cb4a092687fe9a28d3978851b924618ac39a15dae4dadfaadaf822e`  
		Last Modified: Wed, 13 Aug 2025 14:31:22 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e52672eb39ed2019c53a3f3603ad519204a0c29fde83143a5a10d3bfa573fe`  
		Last Modified: Wed, 13 Aug 2025 14:31:28 GMT  
		Size: 14.1 MB (14083963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f0c184de15ddea7dc3c1d0573a452b3adbbf330734ecbd820eba457e4c5f7e`  
		Last Modified: Wed, 13 Aug 2025 14:31:22 GMT  
		Size: 225.1 KB (225130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6078cc14a57aeefbb3f0f83c3d945b628b01bbef247cd5904fa8d79f12ad957c`  
		Last Modified: Wed, 13 Aug 2025 20:20:59 GMT  
		Size: 188.8 MB (188838125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc2a62281b4a83f8bea34d6129f4014ec8b8f4d224e739e7e30ec7fe03db7d0`  
		Last Modified: Wed, 13 Aug 2025 20:21:14 GMT  
		Size: 320.2 MB (320233313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e52560d1fdb92138fcf97bb4dd0e2379898357b33a2f13742252f789504177`  
		Last Modified: Wed, 13 Aug 2025 19:06:38 GMT  
		Size: 1.0 MB (1013640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad328545b252c433cd6b7cb4e2191bb6ae8e71e553957f008c6c1b61d0e43b6`  
		Last Modified: Wed, 13 Aug 2025 19:06:39 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237f9be6805b5e99e6aee4cd990de2e01a402d9aa570f4d9b74c04aafaa46b9b`  
		Last Modified: Wed, 13 Aug 2025 19:06:39 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530d412e514619b9c96880247c652e3250ca7367d97334ebab53cf86a15d2fc4`  
		Last Modified: Wed, 13 Aug 2025 19:06:39 GMT  
		Size: 6.5 KB (6536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf29ddb63590dd5653a91970e5bed7a47448e73a81d8c8132091c9b1a714e407`  
		Last Modified: Wed, 13 Aug 2025 19:06:39 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:8e70d7333b718ab8e431d7f7207952bc327fecb6632e6206aaffc7da3f3ecd26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9194637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb9fc457b8ecfa48302c8d8723d56c2171b22a6bb1333b1097c6333e4f57900`

```dockerfile
```

-	Layers:
	-	`sha256:e31adcab1af1afd92817b86ff6e1beceb40f81e74fdc38e5cf5fa09bbb412779`  
		Last Modified: Wed, 13 Aug 2025 21:08:23 GMT  
		Size: 9.2 MB (9153686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b58c105e2d55caf8858fa0fcad4a57aac2dff9865fae18e229b24f0ed7026531`  
		Last Modified: Wed, 13 Aug 2025 21:08:24 GMT  
		Size: 41.0 KB (40951 bytes)  
		MIME: application/vnd.in-toto+json
