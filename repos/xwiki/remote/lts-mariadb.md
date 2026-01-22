## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:84c473a9c64b99c754ba65e8eddaee92064332e74578b387677e8ef5c8318e3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:21b2b345bb8edca2e2191b4aa420676024dcd5c357813fa06b79eb118805c164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.1 MB (630079993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf40c09a1e3f34d9ef4bb7774a19abfc46133fd541e63976052ddd763c39e988`
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
# Fri, 16 Jan 2026 03:19:14 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 16 Jan 2026 03:19:14 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 16 Jan 2026 03:19:14 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 16 Jan 2026 03:19:14 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 16 Jan 2026 03:19:14 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 16 Jan 2026 03:19:14 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 16 Jan 2026 03:19:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 03:19:14 GMT
ENV XWIKI_VERSION=17.10.2
# Fri, 16 Jan 2026 03:19:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.2
# Fri, 16 Jan 2026 03:19:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=36bec1ea5f82f70f32e4488d8a58e9e44ed952e8657b3f83caf783d30c21a0ee
# Fri, 16 Jan 2026 03:19:36 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 16 Jan 2026 03:19:36 GMT
ENV MARIADB_JDBC_VERSION=3.5.7
# Fri, 16 Jan 2026 03:19:36 GMT
ENV MARIADB_JDBC_SHA256=07bb1229dc184f3313a5aef4c5a6b3207c8dbaa09db4a26814c936f004b4c526
# Fri, 16 Jan 2026 03:19:36 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.7
# Fri, 16 Jan 2026 03:19:36 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.7.jar
# Fri, 16 Jan 2026 03:19:36 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.7.jar
# Fri, 16 Jan 2026 03:20:45 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 16 Jan 2026 03:20:45 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 16 Jan 2026 03:20:45 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 16 Jan 2026 03:20:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 16 Jan 2026 03:20:45 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 03:20:45 GMT
VOLUME [/usr/local/xwiki]
# Fri, 16 Jan 2026 03:20:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 03:20:45 GMT
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
		Last Modified: Thu, 15 Jan 2026 22:20:25 GMT  
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
		Last Modified: Fri, 16 Jan 2026 02:26:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33efa15d9b8242b2e1e2cee890a222831f506e71dd0747c7d36c6af8ea371ed`  
		Last Modified: Fri, 16 Jan 2026 02:27:17 GMT  
		Size: 14.3 MB (14268344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95086209acd013db2ae7aefe9774e7c0259eb3027b1779233c1186e42b4d18f`  
		Last Modified: Fri, 16 Jan 2026 02:27:22 GMT  
		Size: 224.8 KB (224847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9f1bbaf05c593015c226ae709d80997ff49fdc59565fc6be4251d0e6e25166`  
		Last Modified: Fri, 16 Jan 2026 07:10:14 GMT  
		Size: 191.2 MB (191172412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c3bf106adffe0ee8185f4b56da0aa934802ce806045b4ed70fead4824c03dc`  
		Last Modified: Fri, 16 Jan 2026 03:23:21 GMT  
		Size: 324.0 MB (324005643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edba901c4c9d858eeb8643579b83619f036d2504101a65dcf05e42dd4ceb045`  
		Last Modified: Fri, 16 Jan 2026 03:21:06 GMT  
		Size: 708.5 KB (708549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120bd02c469ae9fd69f97cb2b92420104efebcac630d830ffceb4d5419d5644f`  
		Last Modified: Fri, 16 Jan 2026 03:20:59 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9d386e3c8519a3abf89eb9a0f21f66b5dc7bd755b1148635e5c44afe2e0f32`  
		Last Modified: Fri, 16 Jan 2026 03:20:59 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284be3a79fef23aaa68c2fa1f8a5e910f2fbb52e420aada7369501d2421185eb`  
		Last Modified: Fri, 16 Jan 2026 03:21:06 GMT  
		Size: 10.7 KB (10728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ff650719be3d1244ddd49012fd7fc09c7c24981b2179516a79554a76caedc9`  
		Last Modified: Fri, 16 Jan 2026 03:21:06 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:fcc5ca9a8599d1935318096c0422367db6448d8262c0d4dbe08f9b42f0212154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9216753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d57423e6f7e2c8882d81f5817f328ec6588be3fb8c4cef739826c74669610b`

```dockerfile
```

-	Layers:
	-	`sha256:3269deaa96e7b85c866e47e11f9adb8b47319f24af6410e436d3c704beffa9bf`  
		Last Modified: Fri, 16 Jan 2026 03:20:59 GMT  
		Size: 9.2 MB (9175353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dc481e1c11701c0d3439d9c4259d6d78db9d32521ca5f7685c95e312a344a50`  
		Last Modified: Fri, 16 Jan 2026 07:08:27 GMT  
		Size: 41.4 KB (41400 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:e3d7ea455f86c7dc9becb082c15acb8a951dd3544065f0f3738fd5802599685f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.1 MB (626072437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e1ae7902cc752928cc0c67e06c1ee3bb917c919539986ccf3c33cb57334cda`
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
# Fri, 16 Jan 2026 03:23:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 16 Jan 2026 03:23:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 16 Jan 2026 03:23:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 16 Jan 2026 03:23:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 16 Jan 2026 03:23:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 16 Jan 2026 03:23:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 16 Jan 2026 03:23:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 03:23:13 GMT
ENV XWIKI_VERSION=17.10.2
# Fri, 16 Jan 2026 03:23:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.2
# Fri, 16 Jan 2026 03:23:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=36bec1ea5f82f70f32e4488d8a58e9e44ed952e8657b3f83caf783d30c21a0ee
# Fri, 16 Jan 2026 03:23:34 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 16 Jan 2026 03:23:34 GMT
ENV MARIADB_JDBC_VERSION=3.5.7
# Fri, 16 Jan 2026 03:23:34 GMT
ENV MARIADB_JDBC_SHA256=07bb1229dc184f3313a5aef4c5a6b3207c8dbaa09db4a26814c936f004b4c526
# Fri, 16 Jan 2026 03:23:34 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.7
# Fri, 16 Jan 2026 03:23:34 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.7.jar
# Fri, 16 Jan 2026 03:23:34 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.7.jar
# Fri, 16 Jan 2026 03:23:34 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 16 Jan 2026 03:23:34 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 16 Jan 2026 03:23:34 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 16 Jan 2026 03:23:35 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 16 Jan 2026 03:23:35 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 03:23:35 GMT
VOLUME [/usr/local/xwiki]
# Fri, 16 Jan 2026 03:23:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 03:23:35 GMT
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
		Last Modified: Fri, 16 Jan 2026 02:42:37 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16bd8af2c227b0893244b0394138e5e16282db1f86beac0734a122979776c94`  
		Last Modified: Fri, 16 Jan 2026 02:43:36 GMT  
		Size: 14.3 MB (14271548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2d055352eaf464b735f3f306ff8f77c4dc357afd9a2141b7775d6b09c04866`  
		Last Modified: Fri, 16 Jan 2026 02:43:36 GMT  
		Size: 225.2 KB (225196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f13a99d26bbb7f5188b2323b6f4e01130d21b16590d3196155efcc3de7b3a53`  
		Last Modified: Fri, 16 Jan 2026 03:24:13 GMT  
		Size: 188.8 MB (188837985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6765dffbc5a03acd26f079e62b972e515407728092ac6c99e28cebfc4a56da5`  
		Last Modified: Fri, 16 Jan 2026 03:24:15 GMT  
		Size: 324.0 MB (324005650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd2a8aacb7c76aa7c059f0a4ab2315ae0790a832b1ec59ea0c9bbe3a22598fd`  
		Last Modified: Fri, 16 Jan 2026 03:24:07 GMT  
		Size: 708.5 KB (708549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a308cd8f2b29e30e790c2d1c82c30d75d6b270ce08637742bddcb6e8ca9661`  
		Last Modified: Fri, 16 Jan 2026 03:24:31 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d72441eb8cfcb6a0ea67458fc0ac03bff5c15abdf66bb4cd0e8c029f1aba8a2`  
		Last Modified: Fri, 16 Jan 2026 03:24:08 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d031e3bd3e3fad76fc8184b10bb999efb44cc60e19c069426ce79ef138a9e3eb`  
		Last Modified: Fri, 16 Jan 2026 03:24:08 GMT  
		Size: 10.7 KB (10728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eff8d70e05461c6e2d03f3144b9d953b0c51d3f96d69285035747ef8e9095b2`  
		Last Modified: Fri, 16 Jan 2026 03:24:31 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:c844b1cf74b0fa6f0af6621f654c4aaf93368aaa7a9d4883817bc113305436f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9217727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718b1523b64e758bcb88600fe342d46317366a8216baeaeaf138d1adf7245b29`

```dockerfile
```

-	Layers:
	-	`sha256:735922fc95901c30a24e1504acb2706400188b874ef9252a1a5eb57737e354f2`  
		Last Modified: Fri, 16 Jan 2026 07:08:35 GMT  
		Size: 9.2 MB (9176130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b54f52953993fbaef6eea5cd0cb00968405778da1f77e21fe7b8699f60b0215`  
		Last Modified: Fri, 16 Jan 2026 03:24:07 GMT  
		Size: 41.6 KB (41597 bytes)  
		MIME: application/vnd.in-toto+json
