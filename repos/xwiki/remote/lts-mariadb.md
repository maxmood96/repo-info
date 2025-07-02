## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:37cdd0c50903ddc4278b33a3bd707108f225e3e5ff075591a7c35a44d40bb98c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:0005b1f6c44c3f5c1050185c996de10418597292ceba1a17b84169e3d9968467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.5 MB (622540333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c94b7a682b7b495a8b6add4ffe5fa38e50030f1a9afad3556d5fa14674aca2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='8fd14594d0ad8576ba9b698fd10df4a297c548cfdc81cfbe52ac660aeaf5e2b2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 10 Jun 2025 08:03:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 10 Jun 2025 08:03:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Jun 2025 08:03:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
WORKDIR /usr/local/tomcat
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 08:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_MAJOR=9
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_VERSION=9.0.106
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_SHA512=0b316af119fd9a69761c20bc7f9959513884002fc60f490af6335380a3a62549777bf35a1e8dd3c448e56da8ddcb9dc2301d3b01bba304537ca40456c650c25a
# Tue, 10 Jun 2025 08:03:44 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Jun 2025 08:03:44 GMT
ENTRYPOINT []
# Tue, 10 Jun 2025 08:03:44 GMT
CMD ["catalina.sh" "run"]
# Mon, 23 Jun 2025 09:43:20 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 23 Jun 2025 09:43:20 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 23 Jun 2025 09:43:20 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 23 Jun 2025 09:43:20 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 23 Jun 2025 09:43:20 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 23 Jun 2025 09:43:20 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 23 Jun 2025 09:43:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
ENV XWIKI_VERSION=16.10.9
# Mon, 23 Jun 2025 09:43:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.9
# Mon, 23 Jun 2025 09:43:20 GMT
ENV XWIKI_DOWNLOAD_SHA256=5941a1f25e53d9dec1d387891ce9920e80c29f70edb18c4d8522f5c29519da1e
# Mon, 23 Jun 2025 09:43:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
ENV MARIADB_JDBC_VERSION=3.5.3
# Mon, 23 Jun 2025 09:43:20 GMT
ENV MARIADB_JDBC_SHA256=85c4ba2f221d0dfd439c26affbb294f784960763544263c65aba9c2c76858706
# Mon, 23 Jun 2025 09:43:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.3
# Mon, 23 Jun 2025 09:43:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.3.jar
# Mon, 23 Jun 2025 09:43:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.3.jar
# Mon, 23 Jun 2025 09:43:20 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
VOLUME [/usr/local/xwiki]
# Mon, 23 Jun 2025 09:43:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Jun 2025 09:43:20 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c435c063d543b912f39fc6e178600f6b62187fd7a34ab8dc5b5fcb1206dd2dd`  
		Last Modified: Wed, 02 Jul 2025 03:10:36 GMT  
		Size: 17.0 MB (16969494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6798510c0a2db2aee23c3cd77ae21513d0e29201f5a7b1fccea8c428beaf4905`  
		Last Modified: Wed, 02 Jul 2025 03:10:38 GMT  
		Size: 52.9 MB (52891084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5cadd8df76d038e3f113d905144cd7efa62929be4d443f95b87cc6f107a91e`  
		Last Modified: Wed, 02 Jul 2025 03:10:34 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491b99df4756a56b22d3dc6b877cdd97b034981ce870e7f2313ccc3f63cc5ebe`  
		Last Modified: Wed, 02 Jul 2025 03:10:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee75a17b5521c5294b2625e3074f698e016912bc7f4542bd23a1585bc7919150`  
		Last Modified: Wed, 02 Jul 2025 05:12:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214f6e565d0f5285fab00b2304a6a74da1ee9439729bdf0e39cfe07abd2ea2f9`  
		Last Modified: Wed, 02 Jul 2025 05:12:17 GMT  
		Size: 13.7 MB (13692745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd40efcddd78cf2e424cd5eb03a626cb24e9d0b35e6a4d5c44dcb5bec3e6cd5`  
		Last Modified: Wed, 02 Jul 2025 05:12:16 GMT  
		Size: 224.6 KB (224600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56f7d5cb657d803cd98df9063f955fbada32d020da546c3a84d3267e77dfefa`  
		Last Modified: Wed, 02 Jul 2025 09:09:36 GMT  
		Size: 191.2 MB (191177627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c92b1fc670c14bc7461ff7f7042f8ca31c423374037bcbe96730e2dd1f1239`  
		Last Modified: Wed, 02 Jul 2025 09:09:30 GMT  
		Size: 317.2 MB (317159368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce20c29b9f310c107eaf07f6c0bd49ddd50672a5b92cdcd051c4326075f245a4`  
		Last Modified: Wed, 02 Jul 2025 06:14:10 GMT  
		Size: 691.6 KB (691650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be332d65f180c680d0a696d02b8aac750f78190c2b6cf6244d4c6847198dda8e`  
		Last Modified: Wed, 02 Jul 2025 06:14:10 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebbcd0d2b8ec379fd8005e241947b9e693725ccd13bc9172a672483310fae0d`  
		Last Modified: Wed, 02 Jul 2025 06:14:10 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782a3a381cf69471005cb1d95baad2bdc8e7473a9192592a859baf402465b50a`  
		Last Modified: Wed, 02 Jul 2025 06:14:10 GMT  
		Size: 6.6 KB (6632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b784018034e52c708c86c50689861e6dd6eee021dc3b6d4f4d617a1461514af`  
		Last Modified: Wed, 02 Jul 2025 06:14:10 GMT  
		Size: 2.5 KB (2473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:47dcb423f2d26ba538a6fe5b88274dc3e00c4982f9ef394f04d74d64eb9e2537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9143741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ba10add034b49b3fe419f84606aa8f06f07a98c96dcec8bfdecfe8c03c3d32`

```dockerfile
```

-	Layers:
	-	`sha256:6b01beaec1a9025269f3d705497a36bde85d8c001d450a81bd05d46e66d21a1f`  
		Last Modified: Wed, 02 Jul 2025 09:07:25 GMT  
		Size: 9.1 MB (9103259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92eb4510b117a99a40e85660bff42da976ba4ea66cca48c5eda83a1add3a6111`  
		Last Modified: Wed, 02 Jul 2025 09:07:26 GMT  
		Size: 40.5 KB (40482 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:f606b4718741c22ccd4e3fdd98cc71ce41725d3f695a4c893923a02103683802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.5 MB (618548493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27113ae62732e0c0febe66d2c4f26ef83aabb64e5d06c49c74d5141363dbe79f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
ARG RELEASE
# Wed, 23 Apr 2025 14:48:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 23 Apr 2025 14:48:05 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='8fd14594d0ad8576ba9b698fd10df4a297c548cfdc81cfbe52ac660aeaf5e2b2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 10 Jun 2025 08:03:44 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 10 Jun 2025 08:03:44 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Jun 2025 08:03:44 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
WORKDIR /usr/local/tomcat
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 08:03:44 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_MAJOR=9
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_VERSION=9.0.106
# Tue, 10 Jun 2025 08:03:44 GMT
ENV TOMCAT_SHA512=0b316af119fd9a69761c20bc7f9959513884002fc60f490af6335380a3a62549777bf35a1e8dd3c448e56da8ddcb9dc2301d3b01bba304537ca40456c650c25a
# Tue, 10 Jun 2025 08:03:44 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 10 Jun 2025 08:03:44 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 10 Jun 2025 08:03:44 GMT
ENTRYPOINT []
# Tue, 10 Jun 2025 08:03:44 GMT
CMD ["catalina.sh" "run"]
# Mon, 23 Jun 2025 09:43:20 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 23 Jun 2025 09:43:20 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 23 Jun 2025 09:43:20 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 23 Jun 2025 09:43:20 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 23 Jun 2025 09:43:20 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 23 Jun 2025 09:43:20 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 23 Jun 2025 09:43:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
ENV XWIKI_VERSION=16.10.9
# Mon, 23 Jun 2025 09:43:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.9
# Mon, 23 Jun 2025 09:43:20 GMT
ENV XWIKI_DOWNLOAD_SHA256=5941a1f25e53d9dec1d387891ce9920e80c29f70edb18c4d8522f5c29519da1e
# Mon, 23 Jun 2025 09:43:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
ENV MARIADB_JDBC_VERSION=3.5.3
# Mon, 23 Jun 2025 09:43:20 GMT
ENV MARIADB_JDBC_SHA256=85c4ba2f221d0dfd439c26affbb294f784960763544263c65aba9c2c76858706
# Mon, 23 Jun 2025 09:43:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.3
# Mon, 23 Jun 2025 09:43:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.3.jar
# Mon, 23 Jun 2025 09:43:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.3.jar
# Mon, 23 Jun 2025 09:43:20 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 23 Jun 2025 09:43:20 GMT
VOLUME [/usr/local/xwiki]
# Mon, 23 Jun 2025 09:43:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Jun 2025 09:43:20 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2fa422bbd08bc40d85a4e1666805f0d0f323a1834f9494578f07cf2106f303`  
		Last Modified: Wed, 02 Jul 2025 05:07:14 GMT  
		Size: 17.0 MB (16988217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5debe69a504b4c2ab882ec6fcf7d2d47a2d074939b121a43f2d1594752b52463`  
		Last Modified: Wed, 02 Jul 2025 05:14:27 GMT  
		Size: 52.1 MB (52070804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffeee2216863cde6c6647a5098b5e4d04aad2a026305d5359e92a4b1bf9e46e`  
		Last Modified: Wed, 02 Jul 2025 05:14:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c8c5490283483e487a7dadfce6ab28484599ac9809b53dedc827f0f3f0e9ed`  
		Last Modified: Wed, 02 Jul 2025 05:14:24 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e010e8775cc784ff60e30bbab722ebf0ae7c4d744ece09db549c8cdc748af0`  
		Last Modified: Wed, 02 Jul 2025 14:33:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69e48da0a008b1763eb37d63edcf94967e36ab9db67ff461e494dd422c5dd12`  
		Last Modified: Wed, 02 Jul 2025 14:37:15 GMT  
		Size: 13.7 MB (13705172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d220edda577d517cadbdc99dc43dcdf30481b43b1758b034116775bd21e0682`  
		Last Modified: Wed, 02 Jul 2025 14:37:14 GMT  
		Size: 225.0 KB (225036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ca51cd7fe5643a7d2d1ec232812b2dada05cefb078968b34bc3b8ccc372d66`  
		Last Modified: Wed, 02 Jul 2025 16:34:55 GMT  
		Size: 188.8 MB (188836782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38432659f5beab662414a3f36a4e323443be73587184795427eff83ad1648a1`  
		Last Modified: Wed, 02 Jul 2025 16:34:57 GMT  
		Size: 317.2 MB (317159405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377da497ddf052e19d4d69dcd48b442c71bc5b709d21c430894aabdb46a9f05d`  
		Last Modified: Wed, 02 Jul 2025 16:36:01 GMT  
		Size: 691.7 KB (691653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4abf63cd877cdca3a961786ee660858edb14d331d77010e1d031d372107786d`  
		Last Modified: Wed, 02 Jul 2025 16:36:01 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e4d114f22292efc82e7af1de98e4de9c4d3ad70c11bf57308157aa7c27fbc4`  
		Last Modified: Wed, 02 Jul 2025 16:36:01 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dbf8ae13d60a638ef323d7cbc26c0d5d2a551b717cef724c40f803a904621c`  
		Last Modified: Wed, 02 Jul 2025 16:36:01 GMT  
		Size: 6.6 KB (6632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5a1359bbbe7dac390871c77819e9c004bf79194cd78391a5522cf438caa946`  
		Last Modified: Wed, 02 Jul 2025 16:36:01 GMT  
		Size: 2.5 KB (2475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:c99c7814b916c83597e0d72811c7117ce588dc512c2aea96bffe4b9cda520944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9144643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660f18e0aafea0f07fed9b161828cce5e7e25580e848c75ceb936e4b468e0e0d`

```dockerfile
```

-	Layers:
	-	`sha256:38ea2dcadfb71f3cd6a318d375f5e654076c2ed989555629c0162c8dd19b07db`  
		Last Modified: Wed, 02 Jul 2025 18:07:38 GMT  
		Size: 9.1 MB (9104000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d539b9eb1c826d08e4db2503113137908ab25f592039117dc095f6b47aa8ca0`  
		Last Modified: Wed, 02 Jul 2025 18:07:39 GMT  
		Size: 40.6 KB (40643 bytes)  
		MIME: application/vnd.in-toto+json
