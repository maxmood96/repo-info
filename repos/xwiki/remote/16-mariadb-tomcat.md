## `xwiki:16-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:dd8b866d2f3e2b77eafa6d1949dc9f8abb5bdf381d6144dc4cf72262052363ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:16-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:2ee89e8f9ec66a5fc9f9879a68263d68b08f460a8d51e489b9426a2cba8ff9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.4 MB (622421840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d480f2f07fe1f316d355b8044fe90dd8949193ae3e6a33b9618f29294f999bc1`
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
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
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
# Wed, 14 May 2025 13:55:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 14 May 2025 13:55:26 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 13:55:26 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 14 May 2025 13:55:26 GMT
WORKDIR /usr/local/tomcat
# Wed, 14 May 2025 13:55:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 14 May 2025 13:55:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 14 May 2025 13:55:26 GMT
ENV TOMCAT_MAJOR=9
# Wed, 14 May 2025 13:55:26 GMT
ENV TOMCAT_VERSION=9.0.106
# Wed, 14 May 2025 13:55:26 GMT
ENV TOMCAT_SHA512=0b316af119fd9a69761c20bc7f9959513884002fc60f490af6335380a3a62549777bf35a1e8dd3c448e56da8ddcb9dc2301d3b01bba304537ca40456c650c25a
# Wed, 14 May 2025 13:55:26 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 14 May 2025 13:55:26 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 13:55:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 14 May 2025 13:55:26 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 14 May 2025 13:55:26 GMT
ENTRYPOINT []
# Wed, 14 May 2025 13:55:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 14 May 2025 13:55:26 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 13:55:26 GMT
ENV XWIKI_VERSION=16.10.8
# Wed, 14 May 2025 13:55:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.8
# Wed, 14 May 2025 13:55:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=559644b36d96d9daf64bec12559899a525e9f6dc164f7c2dcb1ca6c3a0613a62
# Wed, 14 May 2025 13:55:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_VERSION=3.5.3
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_SHA256=85c4ba2f221d0dfd439c26affbb294f784960763544263c65aba9c2c76858706
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.3
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.3.jar
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.3.jar
# Wed, 14 May 2025 13:55:26 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 14 May 2025 13:55:26 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 14 May 2025 13:55:26 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 14 May 2025 13:55:26 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 14 May 2025 13:55:26 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 14 May 2025 13:55:26 GMT
VOLUME [/usr/local/xwiki]
# Wed, 14 May 2025 13:55:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 May 2025 13:55:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35394ce74242c5b7ece149865352a48182efc427381c78444f4d0d8eb1f42de6`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 17.0 MB (16969509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a156ac8fc59e1707c9f501f0739b750edf0a7eee174a746f875ff6095203a864`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 52.9 MB (52891018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d570382bab9a8f261ccabe2287081c1d484a97c6ea8d4fc6225bfe706ccb3b`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b894632d8872eed0f9df445b209dd701a6186ce7c4df92157736141508657d61`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1ec87299755c3521b672bc05e7815b68e9b95be1f9f7ef9ea801f3562807ea`  
		Last Modified: Tue, 10 Jun 2025 18:08:33 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86a23f101ea68a7dd176cb78136ec1f4f6604bbc619244f1a23063ddd28b50e`  
		Last Modified: Tue, 10 Jun 2025 18:08:35 GMT  
		Size: 13.7 MB (13692752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f74ce3dbfb4598a6a24ee37ca0bdeee893d20e5ac17ce2d77036ecd20cb4ba`  
		Last Modified: Tue, 10 Jun 2025 18:08:34 GMT  
		Size: 224.7 KB (224710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b75ae5d59221e130fbe288f46b1c945557641115dcb80c569a462bd92c43a5`  
		Last Modified: Tue, 10 Jun 2025 18:28:48 GMT  
		Size: 191.2 MB (191165272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9f0553d8b78ffdcee220d4d8e7a48c7cf9e6b085e5c7551b605d64a339641e`  
		Last Modified: Tue, 10 Jun 2025 21:44:27 GMT  
		Size: 317.1 MB (317056196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e60ae8309b00b5db9b0db04dfaca149dabc420ab60e00a1792f354ec925828`  
		Last Modified: Tue, 10 Jun 2025 18:29:05 GMT  
		Size: 691.6 KB (691649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17898aceaee75cd33d553cee9c508ad2f9874c4829491e8490f23426cdf9d8ad`  
		Last Modified: Tue, 10 Jun 2025 18:29:03 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1750712f5ee24291c0da34d97fc7f5b4592eece5b6cf9607309cb973832204`  
		Last Modified: Tue, 10 Jun 2025 18:29:04 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df329b7e6521e5e4ba2ca09da8139cb7d7ce913fc4726fc25903c41a59d2ca76`  
		Last Modified: Tue, 10 Jun 2025 18:29:04 GMT  
		Size: 6.6 KB (6631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3af546e6afabf653f13b1e23e18603440e7d992d3e18e193699199ffd9a686`  
		Last Modified: Tue, 10 Jun 2025 18:29:04 GMT  
		Size: 2.5 KB (2473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:329dd23402121d7787625fbee5174bee5f2ea09bd2e8d8deabef07c29c632dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9143731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15662d73c41e855bee5fe3b497173dc9667e3746f4c3aec33a11734e311a6464`

```dockerfile
```

-	Layers:
	-	`sha256:be6c88e672cac17f6b7218f14a31d4ecbefd766c54076e5f2cf375b9ba4a66ec`  
		Last Modified: Tue, 10 Jun 2025 21:07:27 GMT  
		Size: 9.1 MB (9103250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1948cd00bcdc52803ab7552e5d88b792dab523810ef7321ac9f0d399bede9a8c`  
		Last Modified: Tue, 10 Jun 2025 21:07:28 GMT  
		Size: 40.5 KB (40481 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:16-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:d69db487463d7882e7b675e03e3d8d78603ffd849edc55b986d4231226dcca0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.4 MB (618435574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8211c6d2500d92cc83ad62ae6af375cca2ee18b0df965746d0ab59c67604547`
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
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
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
# Wed, 14 May 2025 13:55:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 14 May 2025 13:55:26 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 May 2025 13:55:26 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 14 May 2025 13:55:26 GMT
WORKDIR /usr/local/tomcat
# Wed, 14 May 2025 13:55:26 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 14 May 2025 13:55:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 14 May 2025 13:55:26 GMT
ENV TOMCAT_MAJOR=9
# Wed, 14 May 2025 13:55:26 GMT
ENV TOMCAT_VERSION=9.0.106
# Wed, 14 May 2025 13:55:26 GMT
ENV TOMCAT_SHA512=0b316af119fd9a69761c20bc7f9959513884002fc60f490af6335380a3a62549777bf35a1e8dd3c448e56da8ddcb9dc2301d3b01bba304537ca40456c650c25a
# Wed, 14 May 2025 13:55:26 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 14 May 2025 13:55:26 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 13:55:26 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 14 May 2025 13:55:26 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 14 May 2025 13:55:26 GMT
ENTRYPOINT []
# Wed, 14 May 2025 13:55:26 GMT
CMD ["catalina.sh" "run"]
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 14 May 2025 13:55:26 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 14 May 2025 13:55:26 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 May 2025 13:55:26 GMT
ENV XWIKI_VERSION=16.10.8
# Wed, 14 May 2025 13:55:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.8
# Wed, 14 May 2025 13:55:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=559644b36d96d9daf64bec12559899a525e9f6dc164f7c2dcb1ca6c3a0613a62
# Wed, 14 May 2025 13:55:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_VERSION=3.5.3
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_SHA256=85c4ba2f221d0dfd439c26affbb294f784960763544263c65aba9c2c76858706
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.3
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.3.jar
# Wed, 14 May 2025 13:55:26 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.3.jar
# Wed, 14 May 2025 13:55:26 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 14 May 2025 13:55:26 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 14 May 2025 13:55:26 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 14 May 2025 13:55:26 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 14 May 2025 13:55:26 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 14 May 2025 13:55:26 GMT
VOLUME [/usr/local/xwiki]
# Wed, 14 May 2025 13:55:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 May 2025 13:55:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb5cdde15082c2c264c46bd2f1aa0a8ad43d7590dd7374853ce1748ae4259a4`  
		Last Modified: Tue, 03 Jun 2025 13:30:28 GMT  
		Size: 17.0 MB (16988306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5911347bfc36c43690c78dbee1e4214c6e79e6c2b6bae6572423040611ba80da`  
		Last Modified: Tue, 03 Jun 2025 13:30:30 GMT  
		Size: 52.1 MB (52070812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06763e1dbf3e148227fb25ab13d25e10e5ae8fcef8987f96fed0240d4ddc176b`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720d536b8cff2c9920c7cc9f8410384ff797ae6e3f12ba749e6295cc4c780c62`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd2c3debe0b0a3a6a9052f48e560d43e668d79c600e030367fef057dd4ce52c`  
		Last Modified: Tue, 03 Jun 2025 14:38:44 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e95367e3d6924ca9e0ddc8261660489231093a70b1cd2d9a09449734e2d4a8`  
		Last Modified: Tue, 10 Jun 2025 19:20:13 GMT  
		Size: 13.7 MB (13705100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c79dcfdcec117345591706387efa7095e736ca774109b93968cd0cb89efb050`  
		Last Modified: Tue, 10 Jun 2025 19:20:12 GMT  
		Size: 225.2 KB (225155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69015c55e45c06e040948a8bb4b37eaad82e6bf272dd07355aadc09f729c1f3d`  
		Last Modified: Tue, 10 Jun 2025 21:16:07 GMT  
		Size: 188.8 MB (188830979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2106748c60a309f3b00f3a24bcb7b0eb137f4a3824a423177763ad2fcff8ecb`  
		Last Modified: Tue, 10 Jun 2025 21:15:51 GMT  
		Size: 317.1 MB (317056280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee1ea3a01c01c84d76d5dc487f5b69a6169c6f6903ac4b27e128578535bcd49`  
		Last Modified: Tue, 10 Jun 2025 20:10:09 GMT  
		Size: 691.7 KB (691651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce9e50024f18b2f77c0d96ca4abc59bcaec6072a3e9419d5ba963a72acff8ad`  
		Last Modified: Tue, 10 Jun 2025 20:10:09 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8318cb2601f70b886b7a830c8f7795354c3b97351a229dac20dc28f6ed7cb`  
		Last Modified: Tue, 10 Jun 2025 20:10:09 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3febb1148de0a1708a6a59d4b3b110a617546db19bb8253cca053e5a22252e61`  
		Last Modified: Tue, 10 Jun 2025 20:10:10 GMT  
		Size: 6.6 KB (6632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3616006de25b9749e9b7771767a49ef9aceaf5143f25059043a1f2d54b5ca6ce`  
		Last Modified: Tue, 10 Jun 2025 20:10:10 GMT  
		Size: 2.5 KB (2468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:0956d87e0745861d2fbd538128e94d2934c3f3dcae0de5c924b5a40c8493f4c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9144634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cabd6535291c66ec9060cd6b6e8ad5d12a6bdab29530e093a200d098df3f59a`

```dockerfile
```

-	Layers:
	-	`sha256:8425b025c1ad850d892ad880e64cf23961a5c967759f54f37ba2a12cedc7e25e`  
		Last Modified: Tue, 10 Jun 2025 21:08:35 GMT  
		Size: 9.1 MB (9103991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32acdbdfc41c6b0c9c5fabeb1d91b2f37ca54f288951a215ecfffe619712da6f`  
		Last Modified: Tue, 10 Jun 2025 21:08:36 GMT  
		Size: 40.6 KB (40643 bytes)  
		MIME: application/vnd.in-toto+json
