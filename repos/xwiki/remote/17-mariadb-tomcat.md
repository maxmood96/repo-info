## `xwiki:17-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:8ff0efdf62774f1ae18a06c55df273d50006a7acca7d3a6efb1adc3588751c89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:17-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:321202cd751af464d3ae04d8e5192765410dbe085395537be89499d7a6b64a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.5 MB (626512481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a602b2d0823803b40cf42161eea1ae7d6cb51fed2e0d995a7234e5098f96ab`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
# Tue, 14 Oct 2025 02:03:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 14 Oct 2025 02:03:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 02:03:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 14 Oct 2025 02:03:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 14 Oct 2025 02:03:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 14 Oct 2025 02:03:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 14 Oct 2025 02:03:18 GMT
ENV TOMCAT_MAJOR=10
# Tue, 14 Oct 2025 02:03:18 GMT
ENV TOMCAT_VERSION=10.1.48
# Tue, 14 Oct 2025 02:03:18 GMT
ENV TOMCAT_SHA512=aecbc4ae16f6783e3f80696fe936c8201fd74a708be18a2512864c0141eeec91180b8c8274f60a0e28390d932344a15c5ef3b3e6fbb819b3d2db244d4f562998
# Tue, 14 Oct 2025 02:03:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 14 Oct 2025 02:03:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 02:03:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 14 Oct 2025 02:03:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 14 Oct 2025 02:03:18 GMT
ENTRYPOINT []
# Tue, 14 Oct 2025 02:03:18 GMT
CMD ["catalina.sh" "run"]
# Tue, 28 Oct 2025 16:40:25 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 28 Oct 2025 16:40:25 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 28 Oct 2025 16:40:25 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 28 Oct 2025 16:40:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 28 Oct 2025 16:40:25 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 28 Oct 2025 16:40:25 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 28 Oct 2025 16:40:25 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Oct 2025 16:40:25 GMT
ENV XWIKI_VERSION=17.9.0
# Tue, 28 Oct 2025 16:40:25 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.9.0
# Tue, 28 Oct 2025 16:40:25 GMT
ENV XWIKI_DOWNLOAD_SHA256=917d927f03630cb7b7811ecca76bb4a3681e55b47ee262ae27c55f4e751439ce
# Tue, 28 Oct 2025 16:40:46 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 28 Oct 2025 16:40:46 GMT
ENV MARIADB_JDBC_VERSION=3.5.6
# Tue, 28 Oct 2025 16:40:46 GMT
ENV MARIADB_JDBC_SHA256=a129703efd7b0f334564d46753de999f09b3a361489a2eb647e6020390981cc9
# Tue, 28 Oct 2025 16:40:46 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.6
# Tue, 28 Oct 2025 16:40:46 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.6.jar
# Tue, 28 Oct 2025 16:40:46 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.6.jar
# Tue, 28 Oct 2025 16:41:38 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 28 Oct 2025 16:41:38 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 28 Oct 2025 16:41:38 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 28 Oct 2025 16:41:38 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 28 Oct 2025 16:41:38 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 28 Oct 2025 16:41:38 GMT
VOLUME [/usr/local/xwiki]
# Tue, 28 Oct 2025 16:41:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Oct 2025 16:41:38 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f38e2e092670ef283f8cef3be87ca664b534a953c460e93cfc9ffeebbc8224`  
		Last Modified: Thu, 09 Oct 2025 21:13:36 GMT  
		Size: 17.0 MB (16971757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c474f64746d27f2879d262f6299fbbf510deb0689105ba567ba62c6760583d3`  
		Last Modified: Thu, 09 Oct 2025 21:14:09 GMT  
		Size: 53.0 MB (52968909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1e9704d175f236f24573f3263c46c98ce312c06751ec7feb8aa18adda6c39e`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2326993b9fe603f4efecedec459c92a6f5cbddca94dc55593db837055ac2e4e8`  
		Last Modified: Thu, 09 Oct 2025 21:14:00 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d341d21aec0e325aa93e6e34c1e94774544bf1e9f2285d83b2461f5479e5b2`  
		Last Modified: Tue, 14 Oct 2025 18:12:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71479bdef7ae9f3fc44e73ef82fbba06577241313f9391ae029efeae35f28ddb`  
		Last Modified: Tue, 14 Oct 2025 18:12:45 GMT  
		Size: 14.1 MB (14089493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b33f75a112c344238bab99a8a9a805229970dcf36638a014f7cdbce5d6bada1`  
		Last Modified: Tue, 14 Oct 2025 18:12:43 GMT  
		Size: 224.7 KB (224715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8233a1e502624b43cfbe9d71b67dc64c0a8278f13a020583b49ab24fbf1515`  
		Last Modified: Tue, 28 Oct 2025 16:42:19 GMT  
		Size: 191.2 MB (191181449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e3022d94af346b048d95f9c49c7c86a84fdb283f5c4997e236523f201e9b16`  
		Last Modified: Tue, 28 Oct 2025 18:10:05 GMT  
		Size: 320.6 MB (320632724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a058bd3764c52077b8d4fb0a538d3632cf6954c2b1f7f637c5b5c0039632fcd4`  
		Last Modified: Tue, 28 Oct 2025 16:41:58 GMT  
		Size: 705.0 KB (704960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56d4525acf5be92826db9d3ce1fa999be21c21ba840eedeaa2a7cc3c4113f39`  
		Last Modified: Tue, 28 Oct 2025 16:41:58 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d07923f8f426da13ab2780ec9e87e722cbe3191bb8c39fbe5c0805c2cc43c7`  
		Last Modified: Tue, 28 Oct 2025 16:41:58 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15ee03aa11b5c1822de1ed68835f7adbc57b2cea2ee116e94b3905ba73d1c06`  
		Last Modified: Tue, 28 Oct 2025 16:41:58 GMT  
		Size: 6.6 KB (6568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ac8cb3806adc1f48661a32254e789f36d5f173427123534f78e7f226577312`  
		Last Modified: Tue, 28 Oct 2025 16:41:58 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:4118f28ac7136a122f2a98a904221bbeeea7843672e1921a72f3fd6dbd088fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9196398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcb99410e41bd7bd3c47f0a10867fa3579bd1517312bf4ea20aead857ad26de`

```dockerfile
```

-	Layers:
	-	`sha256:a9da68dafe70d0993eae5b4684c51d9fe01080ba4f19214e1cfed9dcbffdfd04`  
		Last Modified: Tue, 28 Oct 2025 18:07:42 GMT  
		Size: 9.2 MB (9155640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45208c857fefc0d7284513943840a5c125687179492feaf1c5af69a367298d7d`  
		Last Modified: Tue, 28 Oct 2025 18:07:43 GMT  
		Size: 40.8 KB (40758 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:17-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:d8d8ea06953e9eea99e32a1184237333e3b98564899f99c56887177453fc7a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.5 MB (622521085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ce90ab19fcb8bced5f3dfd8121e5ca54f6d2c9edcd4abc71939030d5afcd2b`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
# Tue, 14 Oct 2025 02:03:18 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 14 Oct 2025 02:03:18 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Oct 2025 02:03:18 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 14 Oct 2025 02:03:18 GMT
WORKDIR /usr/local/tomcat
# Tue, 14 Oct 2025 02:03:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 14 Oct 2025 02:03:18 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 14 Oct 2025 02:03:18 GMT
ENV TOMCAT_MAJOR=10
# Tue, 14 Oct 2025 02:03:18 GMT
ENV TOMCAT_VERSION=10.1.48
# Tue, 14 Oct 2025 02:03:18 GMT
ENV TOMCAT_SHA512=aecbc4ae16f6783e3f80696fe936c8201fd74a708be18a2512864c0141eeec91180b8c8274f60a0e28390d932344a15c5ef3b3e6fbb819b3d2db244d4f562998
# Tue, 14 Oct 2025 02:03:18 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 14 Oct 2025 02:03:18 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 14 Oct 2025 02:03:18 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 14 Oct 2025 02:03:18 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 14 Oct 2025 02:03:18 GMT
ENTRYPOINT []
# Tue, 14 Oct 2025 02:03:18 GMT
CMD ["catalina.sh" "run"]
# Tue, 28 Oct 2025 16:40:08 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 28 Oct 2025 16:40:08 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 28 Oct 2025 16:40:08 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 28 Oct 2025 16:40:08 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 28 Oct 2025 16:40:08 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 28 Oct 2025 16:40:08 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 28 Oct 2025 16:40:08 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Oct 2025 16:40:08 GMT
ENV XWIKI_VERSION=17.9.0
# Tue, 28 Oct 2025 16:40:08 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.9.0
# Tue, 28 Oct 2025 16:40:08 GMT
ENV XWIKI_DOWNLOAD_SHA256=917d927f03630cb7b7811ecca76bb4a3681e55b47ee262ae27c55f4e751439ce
# Tue, 28 Oct 2025 16:40:29 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 28 Oct 2025 16:40:29 GMT
ENV MARIADB_JDBC_VERSION=3.5.6
# Tue, 28 Oct 2025 16:40:29 GMT
ENV MARIADB_JDBC_SHA256=a129703efd7b0f334564d46753de999f09b3a361489a2eb647e6020390981cc9
# Tue, 28 Oct 2025 16:40:29 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.6
# Tue, 28 Oct 2025 16:40:29 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.6.jar
# Tue, 28 Oct 2025 16:40:29 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.6.jar
# Tue, 28 Oct 2025 16:41:20 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 28 Oct 2025 16:41:20 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 28 Oct 2025 16:41:20 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 28 Oct 2025 16:41:20 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 28 Oct 2025 16:41:20 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 28 Oct 2025 16:41:20 GMT
VOLUME [/usr/local/xwiki]
# Tue, 28 Oct 2025 16:41:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Oct 2025 16:41:20 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf670432170ff54aa7d7fec54b27ad51dc4b767bc00a3178b28176173ef130c`  
		Last Modified: Thu, 09 Oct 2025 21:14:24 GMT  
		Size: 17.0 MB (16989173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d3072b7ee41b26a0c52ffc0714ce586e836d00c7f9936e7f5c4219d8993682`  
		Last Modified: Thu, 09 Oct 2025 21:15:03 GMT  
		Size: 52.1 MB (52148484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd18b9ed8f5e6430b2e5b01ce34688a7c375b5a5ab76ed710e24a610e354cc1e`  
		Last Modified: Thu, 09 Oct 2025 21:14:59 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a452d8b8a38c043118d3c800c54e6273302aa0642a20b0df0f628b8d0e8866ce`  
		Last Modified: Thu, 09 Oct 2025 21:14:59 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524d06d0cbe3d99b6b7d54c6e789f61c6d5fa4426208bf5293bfbb58d068693f`  
		Last Modified: Tue, 14 Oct 2025 18:09:44 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983e321bae79dd772225834401922be14aba20de0ea4883b5c74afce6357e1c3`  
		Last Modified: Tue, 14 Oct 2025 18:09:47 GMT  
		Size: 14.1 MB (14092652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8661434d6f4fd08444ba9de05c8db423abe72da5da75220c30384dc1184a0c5`  
		Last Modified: Tue, 14 Oct 2025 18:09:44 GMT  
		Size: 225.4 KB (225393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9023cf73c62f8f0cdcb6e56f2c4acccc0d6a8fa2bd1d0617aa2a8cc0d2c6353f`  
		Last Modified: Tue, 28 Oct 2025 16:41:09 GMT  
		Size: 188.9 MB (188850619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5436c7ea78adacec5510dd006e9b29fa85846b23fd11893172bb9f08372d89a`  
		Last Modified: Tue, 28 Oct 2025 16:41:11 GMT  
		Size: 320.6 MB (320632761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48791e7146c94ed0f501cb120a82e165a9f035299f7d17890c1faf156cde5add`  
		Last Modified: Tue, 28 Oct 2025 16:41:43 GMT  
		Size: 705.0 KB (704958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a5f4d5809b1cdfce9a79bc0ab68cfe75c0bb3c6b3f1a248ce3ae7decdf02f7`  
		Last Modified: Tue, 28 Oct 2025 16:41:42 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e45fca413d4cf69a3d4dd20c880427c8d8810e747087b3a7b07219fe1cbb7f`  
		Last Modified: Tue, 28 Oct 2025 16:41:42 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a2902982bf89353b5dd5c5e048a51a3da3ea4d8a3672cf7e53d35b3efb38a1`  
		Last Modified: Tue, 28 Oct 2025 16:41:43 GMT  
		Size: 6.6 KB (6571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98d2c44b9d8624eb4c3c0d6c880172286fa987307175c13bb719b05e7e0800d`  
		Last Modified: Tue, 28 Oct 2025 16:41:42 GMT  
		Size: 2.5 KB (2473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:0339df03b3556f47b30e142a5cbc0c879db6cb3c4f5a5440597a573d82d531e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9197324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f8d1c12996c5663016623d985670be2190544a533e91b6ec78c766b149cf1b`

```dockerfile
```

-	Layers:
	-	`sha256:69bbcfcf4d21e81d48c30ba28a4a53e0113e65e896d0086ab0678bab6108c4d2`  
		Last Modified: Tue, 28 Oct 2025 18:07:52 GMT  
		Size: 9.2 MB (9156393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2d4090c80486c47ec283abe5eb2644186eeb9d44520d0834554205cab66171d`  
		Last Modified: Tue, 28 Oct 2025 18:07:53 GMT  
		Size: 40.9 KB (40931 bytes)  
		MIME: application/vnd.in-toto+json
