## `xwiki:16-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:3d32162d4ce55ec13d92c3a6111b6a4c503edd103923cddca722923f86f8789d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:16-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:a6620e34939fbb9d2d7e6250085fe7fc97d3883cea2922093acaf81d76e21080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.7 MB (622691737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6bd77c1ad55bd67b00e0a0684a3db4f7aebdf82b30292d4402b5ebe599e5744`
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
# Thu, 31 Jul 2025 08:06:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Jul 2025 08:06:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 08:06:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Jul 2025 08:06:53 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 31 Jul 2025 08:06:53 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 08:06:53 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
WORKDIR /usr/local/tomcat
# Thu, 31 Jul 2025 08:06:53 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 31 Jul 2025 08:06:53 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 31 Jul 2025 08:06:53 GMT
ENV TOMCAT_MAJOR=9
# Thu, 31 Jul 2025 08:06:53 GMT
ENV TOMCAT_VERSION=9.0.108
# Thu, 31 Jul 2025 08:06:53 GMT
ENV TOMCAT_SHA512=243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7
# Thu, 31 Jul 2025 08:06:53 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 31 Jul 2025 08:06:53 GMT
ENTRYPOINT []
# Thu, 31 Jul 2025 08:06:53 GMT
CMD ["catalina.sh" "run"]
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 31 Jul 2025 08:06:53 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
ENV XWIKI_VERSION=16.10.10
# Thu, 31 Jul 2025 08:06:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.10
# Thu, 31 Jul 2025 08:06:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=85dee4db22bb98bde66c4f7b379251f2d86f6ac3e6e92449e3b79a921e0192fd
# Thu, 31 Jul 2025 08:06:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MARIADB_JDBC_VERSION=3.5.4
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MARIADB_JDBC_SHA256=9cac1a01e3b2bac18f826d48475b93e6bdb5c16d31f7227f9653c7c8f1b378e7
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.4
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.4.jar
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.4.jar
# Thu, 31 Jul 2025 08:06:53 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
VOLUME [/usr/local/xwiki]
# Thu, 31 Jul 2025 08:06:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Jul 2025 08:06:53 GMT
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
	-	`sha256:048acea221768da20725347d2ca1930edd926946b945247a95c036f37ac46d36`  
		Last Modified: Tue, 12 Aug 2025 18:08:53 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4039141278925b609c33ca139b6e0b13dd6ab0d4b1ac9fe4f6e58436a9eea9a7`  
		Last Modified: Tue, 12 Aug 2025 18:08:58 GMT  
		Size: 13.7 MB (13714791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7118dfe85abe7d4fd72eb30fb7ea3047bae30f860b6f613c14e52e5bb20ba948`  
		Last Modified: Tue, 12 Aug 2025 18:08:56 GMT  
		Size: 224.7 KB (224673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01af44570234734090797642e8e934c6c10736f3fd53edf6466f3b470e0eb2b7`  
		Last Modified: Wed, 13 Aug 2025 02:00:20 GMT  
		Size: 191.2 MB (191178655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a527e918b098b35d97c33c525d5c6bd3351d6a914d2fd9441932ebb24bc52066`  
		Last Modified: Wed, 13 Aug 2025 02:00:24 GMT  
		Size: 317.2 MB (317199456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621c2b7bf8148e7fb89c432fe6aa1fdadb3f61a79a7ab4fa3a6c6ca4ff870e33`  
		Last Modified: Tue, 12 Aug 2025 18:25:36 GMT  
		Size: 695.0 KB (694959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d614cb0cceccf1061e6bebf0c08dae55ee855713d564241951b886a5c96ea2`  
		Last Modified: Tue, 12 Aug 2025 18:25:33 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34a252bc0a755273c794fd6315871c3ae8a63522f2e92048174fb890d2a6f7f`  
		Last Modified: Tue, 12 Aug 2025 18:25:33 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e054334b29fe19d36845d943de70a0537e3b1d8b587a6af25b79f1c36e6b9`  
		Last Modified: Tue, 12 Aug 2025 18:25:34 GMT  
		Size: 6.6 KB (6628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e0a8124c1b75c97ce4e9921381476788c06624f2e10c4414f6f8893d3772ed`  
		Last Modified: Tue, 12 Aug 2025 18:25:33 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:8e895c23b0b101a84158c8baf1bb33e884d5e55e547e1766d0440d60a48c894b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9144804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0007433362f4dacd3673d496cb534f4de724800d9838afe7c5f1a635eff6ef6`

```dockerfile
```

-	Layers:
	-	`sha256:e7d9f526c6d11eb72e0bd06c308ba3114fae0735a12722ef93bd8f0a6c178409`  
		Last Modified: Tue, 12 Aug 2025 21:07:24 GMT  
		Size: 9.1 MB (9104315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa00516eea3f2109240fbd4a22d28493821cecd6efd30bbb594136c575e22d7`  
		Last Modified: Tue, 12 Aug 2025 21:07:25 GMT  
		Size: 40.5 KB (40489 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:16-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:1a497ac0092c2eca78cc8ed0d41c96d2dfa8c8f1b3bc06b4a471139cfc31f153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.7 MB (618699423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d2278070490da44486e3ad752c7283a191c9597b5a9070687bf0826309fd7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 08:06:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Jul 2025 08:06:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 08:06:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Jul 2025 08:06:53 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 31 Jul 2025 08:06:53 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 08:06:53 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
WORKDIR /usr/local/tomcat
# Thu, 31 Jul 2025 08:06:53 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 31 Jul 2025 08:06:53 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 31 Jul 2025 08:06:53 GMT
ENV TOMCAT_MAJOR=9
# Thu, 31 Jul 2025 08:06:53 GMT
ENV TOMCAT_VERSION=9.0.108
# Thu, 31 Jul 2025 08:06:53 GMT
ENV TOMCAT_SHA512=243474cd54d8589c97f2db964b13b36920500a298b190370a8c58306db786bb30101c33d9ca85eddd8014c5d7f53fec1685beeb4fb7f3037ffcc2f4124c6c6b7
# Thu, 31 Jul 2025 08:06:53 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 31 Jul 2025 08:06:53 GMT
ENTRYPOINT []
# Thu, 31 Jul 2025 08:06:53 GMT
CMD ["catalina.sh" "run"]
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 31 Jul 2025 08:06:53 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 31 Jul 2025 08:06:53 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
ENV XWIKI_VERSION=16.10.10
# Thu, 31 Jul 2025 08:06:53 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.10
# Thu, 31 Jul 2025 08:06:53 GMT
ENV XWIKI_DOWNLOAD_SHA256=85dee4db22bb98bde66c4f7b379251f2d86f6ac3e6e92449e3b79a921e0192fd
# Thu, 31 Jul 2025 08:06:53 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MARIADB_JDBC_VERSION=3.5.4
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MARIADB_JDBC_SHA256=9cac1a01e3b2bac18f826d48475b93e6bdb5c16d31f7227f9653c7c8f1b378e7
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.4
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.4.jar
# Thu, 31 Jul 2025 08:06:53 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.4.jar
# Thu, 31 Jul 2025 08:06:53 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 31 Jul 2025 08:06:53 GMT
VOLUME [/usr/local/xwiki]
# Thu, 31 Jul 2025 08:06:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Jul 2025 08:06:53 GMT
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
	-	`sha256:745e7b18fef68c2dc0727ebca6a566adfbcf521cd41c00458a712681effe3eb0`  
		Last Modified: Wed, 13 Aug 2025 14:36:03 GMT  
		Size: 13.7 MB (13728952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dadd24cb1a7cf3a62f14194b36c6a42b20a1c57d6cd0680e1c3658f6a65be91`  
		Last Modified: Wed, 13 Aug 2025 14:36:01 GMT  
		Size: 225.1 KB (225136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219819923fb989a7f43488cca289ed02e2602c2f14b3e4a53f2a926ef1761709`  
		Last Modified: Wed, 13 Aug 2025 21:55:08 GMT  
		Size: 188.8 MB (188837856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bb3794cde91907e61b44269b1dcc6e73f715e229912970ea22a65e6fb22c65`  
		Last Modified: Wed, 13 Aug 2025 21:55:38 GMT  
		Size: 317.2 MB (317199458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786fe5f12684d434e23b09071be61b05853484c6e5e16d5a2eeef032acac4700`  
		Last Modified: Wed, 13 Aug 2025 19:59:36 GMT  
		Size: 695.0 KB (694959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57319dce4ffe37295a0fcbe6db2f2822e1aa095d605ac8bae45fd3a7b2ae975c`  
		Last Modified: Wed, 13 Aug 2025 19:59:36 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c663129b91c622148080282ed5075a0495d318370e9af463386377d84244678b`  
		Last Modified: Wed, 13 Aug 2025 19:59:37 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00317303f16340bd0b1869fa7a749b4c6df85d139fc6c8cb55c0a8053901c3b1`  
		Last Modified: Wed, 13 Aug 2025 19:59:36 GMT  
		Size: 6.6 KB (6629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1ca1328c63ee5202fd317ca86e90c3e09631dce8b8ff2cb5feca3ebfff65b9`  
		Last Modified: Wed, 13 Aug 2025 19:59:37 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:89c7225c68abbe9460f07516fab3d0116d0329bbdbf7542c4d796af24f6d0300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9145705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827de439a773b38fe618b14f730e52f0358e02f5c74361d086b59d1002de32a8`

```dockerfile
```

-	Layers:
	-	`sha256:2f807161487741dedb4999297d87e9ba6d21aa07dcaf70025e8bf7e0712026a0`  
		Last Modified: Wed, 13 Aug 2025 21:07:50 GMT  
		Size: 9.1 MB (9105056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27007c40ab54c47171d0276734b64dbe7515736dc3941fb22bd8b33f40310526`  
		Last Modified: Wed, 13 Aug 2025 21:07:50 GMT  
		Size: 40.6 KB (40649 bytes)  
		MIME: application/vnd.in-toto+json
