## `xwiki:17-postgres-tomcat`

```console
$ docker pull xwiki@sha256:9d3002f434792cadde6d927b72a9b12e9127c59a62ac55e755e238cdf88f28a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:17-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:52f5a36fe39948cbb1223bd7cd7c17f0ee38dfb05d8e4e6a48f9b6ca440db26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.4 MB (630415288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2aca2ab8f3f3909f8f969866b8848238d86984f4a8ef45ce1ef54ff82280bdb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:19:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:19:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:19:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:19:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:19:12 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 15 Jan 2026 22:20:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='bf821d8240e5d660f0c7e1ffa4f62e4b2dbf72c3d2245d9371160f61389b5fa4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:20:01 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:20:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:20:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 02:26:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Jan 2026 02:26:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:26:13 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 16 Jan 2026 02:26:13 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Jan 2026 02:26:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 02:26:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 02:26:13 GMT
ENV TOMCAT_MAJOR=10
# Fri, 16 Jan 2026 02:26:13 GMT
ENV TOMCAT_VERSION=10.1.50
# Fri, 16 Jan 2026 02:26:13 GMT
ENV TOMCAT_SHA512=c7702b0304257d80dc5bd615005fe037bd0c518e3fe77d22a58e5313fe53e6af6f4a2cf00790e3e9a669d1ae5470fb11177c9ef42f8c846d2b20dfac93e2d551
# Fri, 16 Jan 2026 02:27:03 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 16 Jan 2026 02:27:09 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:27:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 16 Jan 2026 02:27:09 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 16 Jan 2026 02:27:09 GMT
ENTRYPOINT []
# Fri, 16 Jan 2026 02:27:09 GMT
CMD ["catalina.sh" "run"]
# Fri, 16 Jan 2026 03:19:18 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 16 Jan 2026 03:19:18 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 16 Jan 2026 03:19:18 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 16 Jan 2026 03:19:18 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 16 Jan 2026 03:19:18 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 16 Jan 2026 03:19:18 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 16 Jan 2026 03:19:18 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 03:19:18 GMT
ENV XWIKI_VERSION=17.10.2
# Fri, 16 Jan 2026 03:19:18 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.2
# Fri, 16 Jan 2026 03:19:18 GMT
ENV XWIKI_DOWNLOAD_SHA256=36bec1ea5f82f70f32e4488d8a58e9e44ed952e8657b3f83caf783d30c21a0ee
# Fri, 16 Jan 2026 03:19:39 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 16 Jan 2026 03:19:39 GMT
ENV POSTGRES_JDBC_VERSION=42.7.8
# Fri, 16 Jan 2026 03:19:39 GMT
ENV POSTGRES_JDBC_SHA256=2a32a9dcbc42d67a50ad3a0de5efd102c8d2be46720045f2cbd6689f160ab7c7
# Fri, 16 Jan 2026 03:19:39 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.8
# Fri, 16 Jan 2026 03:19:39 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.8.jar
# Fri, 16 Jan 2026 03:19:39 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.8.jar
# Fri, 16 Jan 2026 03:19:39 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 16 Jan 2026 03:19:39 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 16 Jan 2026 03:19:39 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 16 Jan 2026 03:19:40 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 16 Jan 2026 03:19:40 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 03:19:40 GMT
VOLUME [/usr/local/xwiki]
# Fri, 16 Jan 2026 03:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 03:19:40 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996467dfb4d0179a2f091bc2a9d9749646d7fc320067d1147a6df2b4833f1c82`  
		Last Modified: Thu, 15 Jan 2026 22:19:34 GMT  
		Size: 17.0 MB (16975950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c9275308302d364422df0f3e02503135621d8a4b49a0c18580cf9220532743`  
		Last Modified: Thu, 15 Jan 2026 22:20:14 GMT  
		Size: 53.0 MB (52978745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac4b4cf16a8ad1b819f8041978350794113eb509aba19c5cd47bd77a053c335`  
		Last Modified: Thu, 15 Jan 2026 22:20:12 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb78f73258bc413aae5281eb128ee526870ba076049a4526b38041362fe99c6`  
		Last Modified: Thu, 15 Jan 2026 22:20:12 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fec13224de65dfa79e6804ced41c67dd5d754642880b9b42d7164695021fdc`  
		Last Modified: Fri, 16 Jan 2026 02:26:33 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33efa15d9b8242b2e1e2cee890a222831f506e71dd0747c7d36c6af8ea371ed`  
		Last Modified: Fri, 16 Jan 2026 02:27:23 GMT  
		Size: 14.3 MB (14268344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95086209acd013db2ae7aefe9774e7c0259eb3027b1779233c1186e42b4d18f`  
		Last Modified: Fri, 16 Jan 2026 02:27:16 GMT  
		Size: 224.8 KB (224847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765eee9e93169180eedd160287a6e3b8c8944d802c623cbed6d080133350825f`  
		Last Modified: Fri, 16 Jan 2026 07:09:41 GMT  
		Size: 191.2 MB (191173216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2655c0b123dcd78d3192689f04d4551611d69b413e1773f5e6b1913ab055e0`  
		Last Modified: Fri, 16 Jan 2026 03:20:22 GMT  
		Size: 324.0 MB (324005590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847df6aab78b5e4a991b1d7a1827cad34673f6dd86fb9faec18c2622d20f0e79`  
		Last Modified: Fri, 16 Jan 2026 03:20:14 GMT  
		Size: 1.0 MB (1043005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8cba077ecd0755767bb5cd799c34e0a13f0bebc69f28466e5fe56f6a83dc307`  
		Last Modified: Fri, 16 Jan 2026 03:20:35 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb6a030dbb2920ee3fd39ffcba763f58ff05f57c56272fa7bda919bd74587b1`  
		Last Modified: Fri, 16 Jan 2026 03:20:15 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae79ec003ee229b2872b0df4c50fbc2bb4558562b0626f281b01ab82df4a3ce4`  
		Last Modified: Fri, 16 Jan 2026 03:20:35 GMT  
		Size: 10.7 KB (10727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18072040127b4b7651dc4ac0ecf13b7a91fcdbef4ff748a7c64c8ac9bbb5cda`  
		Last Modified: Fri, 16 Jan 2026 03:20:35 GMT  
		Size: 2.4 KB (2412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:94038e8b6423be9e37ad5b4dfb85b655ab2cc2b90012d79fc4273534a9d47b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9216755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990a7dc5117f8985aa648b771beae9417784775d435f7997202adc485d1fc326`

```dockerfile
```

-	Layers:
	-	`sha256:fba7278f8f1ee65dd479ebb13ff7669aba5a3b7c68c1a120c82205860ee3a00a`  
		Last Modified: Fri, 16 Jan 2026 03:20:14 GMT  
		Size: 9.2 MB (9175374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94ba02a06c5b9b2dee69aeb94fe182d360f076fc1ca0071a13b14858ee3c6776`  
		Last Modified: Fri, 16 Jan 2026 07:08:35 GMT  
		Size: 41.4 KB (41381 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:17-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:cf296c6d602555610ac33b35e0b458c402fc7c2cb9b57057c925bec933b463a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.4 MB (626406953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59d1419362d6f1af077c64b9607ae13967e61c74fba8f82f3502d15cc1f61a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:21:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 22:21:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 22:21:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jan 2026 22:21:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:21:25 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 15 Jan 2026 22:21:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='bf821d8240e5d660f0c7e1ffa4f62e4b2dbf72c3d2245d9371160f61389b5fa4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 15 Jan 2026 22:21:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Jan 2026 22:21:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:21:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 16 Jan 2026 02:42:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Jan 2026 02:42:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:42:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 16 Jan 2026 02:42:21 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Jan 2026 02:42:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 02:42:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Jan 2026 02:42:21 GMT
ENV TOMCAT_MAJOR=10
# Fri, 16 Jan 2026 02:42:21 GMT
ENV TOMCAT_VERSION=10.1.50
# Fri, 16 Jan 2026 02:42:21 GMT
ENV TOMCAT_SHA512=c7702b0304257d80dc5bd615005fe037bd0c518e3fe77d22a58e5313fe53e6af6f4a2cf00790e3e9a669d1ae5470fb11177c9ef42f8c846d2b20dfac93e2d551
# Fri, 16 Jan 2026 02:43:22 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 16 Jan 2026 02:43:27 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:43:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 16 Jan 2026 02:43:28 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 16 Jan 2026 02:43:28 GMT
ENTRYPOINT []
# Fri, 16 Jan 2026 02:43:28 GMT
CMD ["catalina.sh" "run"]
# Fri, 16 Jan 2026 03:23:26 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 16 Jan 2026 03:23:26 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 16 Jan 2026 03:23:26 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 16 Jan 2026 03:23:26 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 16 Jan 2026 03:23:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 16 Jan 2026 03:23:26 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 16 Jan 2026 03:23:26 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 03:23:26 GMT
ENV XWIKI_VERSION=17.10.2
# Fri, 16 Jan 2026 03:23:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.2
# Fri, 16 Jan 2026 03:23:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=36bec1ea5f82f70f32e4488d8a58e9e44ed952e8657b3f83caf783d30c21a0ee
# Fri, 16 Jan 2026 03:23:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 16 Jan 2026 03:23:48 GMT
ENV POSTGRES_JDBC_VERSION=42.7.8
# Fri, 16 Jan 2026 03:23:48 GMT
ENV POSTGRES_JDBC_SHA256=2a32a9dcbc42d67a50ad3a0de5efd102c8d2be46720045f2cbd6689f160ab7c7
# Fri, 16 Jan 2026 03:23:48 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.8
# Fri, 16 Jan 2026 03:23:48 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.8.jar
# Fri, 16 Jan 2026 03:23:48 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.8.jar
# Fri, 16 Jan 2026 03:23:48 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 16 Jan 2026 03:23:48 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 16 Jan 2026 03:23:48 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 16 Jan 2026 03:23:48 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 16 Jan 2026 03:23:48 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 03:23:48 GMT
VOLUME [/usr/local/xwiki]
# Fri, 16 Jan 2026 03:23:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 03:23:48 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066d9c7316405755c4355dfd9b742623829c8c1c49462c4e6c938a83b810b7c8`  
		Last Modified: Thu, 15 Jan 2026 22:21:41 GMT  
		Size: 17.0 MB (16991549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f94c82a8ac7fd54191a08fd6e2afc54327165fa15aabd600b27aeb40409383`  
		Last Modified: Thu, 15 Jan 2026 22:21:57 GMT  
		Size: 52.1 MB (52148637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb0eb06dfa687a3659cfda05b90257c82298acab510f78e070b4bc6d3286e0a`  
		Last Modified: Thu, 15 Jan 2026 22:21:40 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6456b4703cbd2d5d7bfc1f46fa116f62a97af321aea424d90a4899ad64cdaff1`  
		Last Modified: Thu, 15 Jan 2026 22:21:40 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6091cc43c1281c8d2525d40367d4af00af406225d29030bdb8afa4f0c487ea7`  
		Last Modified: Fri, 16 Jan 2026 02:42:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16bd8af2c227b0893244b0394138e5e16282db1f86beac0734a122979776c94`  
		Last Modified: Fri, 16 Jan 2026 02:43:36 GMT  
		Size: 14.3 MB (14271548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2d055352eaf464b735f3f306ff8f77c4dc357afd9a2141b7775d6b09c04866`  
		Last Modified: Fri, 16 Jan 2026 02:43:39 GMT  
		Size: 225.2 KB (225196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6cc5b01c56e73bf290861d6e25fb6a3e5079ddbc0e5e2198d1014bdc84ad8fe`  
		Last Modified: Fri, 16 Jan 2026 03:24:27 GMT  
		Size: 188.8 MB (188837942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d1b939c8b4eb5aa599376c1b9a169dc297fb7a881e56e513ee8b919b8dad52`  
		Last Modified: Fri, 16 Jan 2026 03:24:30 GMT  
		Size: 324.0 MB (324005652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96e724336350bc57b904c8e03c694563f6c4b1e3b78aa8a2856a9022f8f30ae`  
		Last Modified: Fri, 16 Jan 2026 03:24:21 GMT  
		Size: 1.0 MB (1043011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a76e24052c68236c3a6349e3fa68436d4037ac4c60795b0255a4517502eaad0`  
		Last Modified: Fri, 16 Jan 2026 03:24:46 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660dee4de7bb1314c381b76349a805a91f2902ff885be34c9ad5a8462455b626`  
		Last Modified: Fri, 16 Jan 2026 03:24:46 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04ebf957bfeceacf1c8b484ee3fd5c64758be7429ba6aee30ed1b30bd261566`  
		Last Modified: Fri, 16 Jan 2026 03:24:46 GMT  
		Size: 10.7 KB (10728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96c5226fb50f0376f4975438e484af858a338326205084b5fc831f258900dfe`  
		Last Modified: Fri, 16 Jan 2026 03:24:24 GMT  
		Size: 2.4 KB (2419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:51fbc6bfd1f89fb3dc0f2d6605c4ce214cdf4bf42f848aeeb307e15a3fe39b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9217729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5caf6caba7dd0a04401535734a1e6d0a74fcb88bc2f03e3847e906d707e50965`

```dockerfile
```

-	Layers:
	-	`sha256:da68082928823a938478207aaf6009298af6e9214559312e76db1bb53e8bff07`  
		Last Modified: Fri, 16 Jan 2026 03:24:21 GMT  
		Size: 9.2 MB (9176151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae945ab4c3a43b7195f2b68497c2f208a848637b97a0245a0788d22a9e70ba97`  
		Last Modified: Fri, 16 Jan 2026 07:08:48 GMT  
		Size: 41.6 KB (41578 bytes)  
		MIME: application/vnd.in-toto+json
