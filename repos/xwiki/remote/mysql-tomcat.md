## `xwiki:mysql-tomcat`

```console
$ docker pull xwiki@sha256:81e77892e7f0098acd67a0e8e34c0171d4e17fb2337b0a67176d8856d22ac4e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:mysql-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:58c842ce4a81e9e25d39cc9f3695fef9076508a853841ddaf69e3654c818465a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.1 MB (628097666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b752227a7a79530e7a908e00a705a4ecae710d68874dcdec71eff08c762d5dab`
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
	-	`sha256:a76cd16ec985c7b07706f5f4887296e399971f7190c18ffd02dcd86d413682ce`  
		Last Modified: Thu, 28 Aug 2025 18:08:31 GMT  
		Size: 191.2 MB (191179024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0e2cab7683b944ea31b967b868259676a7aab951c1958c540c60d6f6e430d8`  
		Last Modified: Thu, 28 Aug 2025 18:08:46 GMT  
		Size: 320.5 MB (320503177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b13fd3a603c5262f26fbb3a92ea8affe8e0e69d007fb2a5c608d0b95d77ee5`  
		Last Modified: Thu, 28 Aug 2025 17:58:20 GMT  
		Size: 2.4 MB (2430453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0671e2c218d88cc85633c96885c1454cc1bbe381c0192dbb1af00a5898f9191`  
		Last Modified: Thu, 28 Aug 2025 17:58:27 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b8c643412d4dbb0f60a50a455143219f3572b8577099fc85bacd76ab0ea795`  
		Last Modified: Thu, 28 Aug 2025 17:58:30 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a90b252f49baf97c0b3056d9888bc7d45a5813a395c4b3cf69b28da7747524`  
		Last Modified: Thu, 28 Aug 2025 17:58:33 GMT  
		Size: 6.6 KB (6551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6041aaef459277e7b6372e77670ba38cf9e1fdf6fc51acb268cfb9de50b7f7f6`  
		Last Modified: Thu, 28 Aug 2025 17:58:36 GMT  
		Size: 2.5 KB (2511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:06c4e9502e6f923dba282ce2776360be33371963047cc9e2e7e264ea6f8d8055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9196591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:385991deb352f9d3fc02d0832b17d922fd934dba0f05bf9ee73ee4b8c850ae0e`

```dockerfile
```

-	Layers:
	-	`sha256:a6ec1abb946a7592b199a30805ec57c51f02a92b2106235d1645f36e746578cc`  
		Last Modified: Thu, 28 Aug 2025 18:07:57 GMT  
		Size: 9.2 MB (9154452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f349a76ca75720916aac0d64935c8bebe8ae8d2f937bf4198051183c90e5114e`  
		Last Modified: Thu, 28 Aug 2025 18:07:58 GMT  
		Size: 42.1 KB (42139 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:mysql-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:c73691e3735e57da576565a24aa1664abccc7d1bcedaf04701fca66ada8241ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.8 MB (623825195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b64759596cd438dee38f68d155ccd536ae5d197a4f0570a19c0e8c9c09d2b63`
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
ENV MYSQL_JDBC_VERSION=9.3.0
# Mon, 28 Jul 2025 13:28:25 GMT
ENV MYSQL_JDBC_SHA256=6c8e6692b521376d89bc5618c16cdeaf8c61854329f4fa25677ed08776c5bb76
# Mon, 28 Jul 2025 13:28:25 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.3.0
# Mon, 28 Jul 2025 13:28:25 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.3.0.jar
# Mon, 28 Jul 2025 13:28:25 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.3.0.jar
# Mon, 28 Jul 2025 13:28:25 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:d0392d604f2bbe25ddf07d1770727a682a2fa8c7e484bc336cdce59362429020`  
		Last Modified: Wed, 13 Aug 2025 19:19:15 GMT  
		Size: 2.4 MB (2431601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f360bcf30eb80957127442f9e095e4a26fabaa6125c85091560bc3f952953ca`  
		Last Modified: Wed, 13 Aug 2025 19:19:20 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c17b99e3bfd50840a4cd51ecb29fd0126d0a1e89f8625df3aa1d3b751b19939`  
		Last Modified: Wed, 13 Aug 2025 19:19:22 GMT  
		Size: 2.4 KB (2371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289c3bea6f8069ff8dff03dcf82c3c6185cb6125888aaf134a6b03393fe3db92`  
		Last Modified: Wed, 13 Aug 2025 19:19:24 GMT  
		Size: 6.5 KB (6533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1fb956aea68d4c543d00073df7e16621accfdc1c79e50636b954c0e0a06404`  
		Last Modified: Wed, 13 Aug 2025 19:19:28 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mysql-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:8a19b4c5d2cd38bb27606cf0e73ed629a95ca95d27228686b6db398a23085590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9197617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d0641d5cce0b73ba4e05639f36cbe7436a38928cd240ff0fb9ad99a1aa370b`

```dockerfile
```

-	Layers:
	-	`sha256:440833a6c6bb09fe86a20120cf5f0d905759dcd3cfac91258d44dca3f167cbff`  
		Last Modified: Wed, 13 Aug 2025 21:08:12 GMT  
		Size: 9.2 MB (9155244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0271a3be9fe9b3b3b9e82806b050f3170b83109d571a2f555cecfa7d5a3232b8`  
		Last Modified: Wed, 13 Aug 2025 21:08:13 GMT  
		Size: 42.4 KB (42373 bytes)  
		MIME: application/vnd.in-toto+json
