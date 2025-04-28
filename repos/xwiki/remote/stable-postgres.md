## `xwiki:stable-postgres`

```console
$ docker pull xwiki@sha256:21b674c52cd35340c0b7115c2b57f34a9905e5029c45da98dd6044dd2223c8f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:f222d104c7f43f3c611fd1b2281c901dfdf9383e14548a4cdd62f03246df68af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.2 MB (623223451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65983035da8e9539328e8690ff88edc428c2ca9e0d0e000b96a988050f0acdfa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
CMD ["/bin/bash"]
# Tue, 08 Apr 2025 20:03:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Apr 2025 20:03:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 20:03:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='8fd14594d0ad8576ba9b698fd10df4a297c548cfdc81cfbe52ac660aeaf5e2b2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Apr 2025 20:03:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Apr 2025 20:03:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 20:03:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Apr 2025 20:03:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_MAJOR=10
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_VERSION=10.1.40
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_SHA512=2bde772acf2e6f300f0f8341eb4de7da5d59af6a95f607bcdb92e4c22e0a253d437ea9a423d7d3e334af1c608f33489f32d32d346fbef5b0abef1dee666895ea
# Tue, 08 Apr 2025 20:03:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Apr 2025 20:03:21 GMT
ENTRYPOINT []
# Tue, 08 Apr 2025 20:03:21 GMT
CMD ["catalina.sh" "run"]
# Mon, 28 Apr 2025 15:52:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 28 Apr 2025 15:52:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 28 Apr 2025 15:52:06 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 28 Apr 2025 15:52:06 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 28 Apr 2025 15:52:06 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 28 Apr 2025 15:52:06 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 28 Apr 2025 15:52:06 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
ENV XWIKI_VERSION=17.3.0
# Mon, 28 Apr 2025 15:52:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.3.0
# Mon, 28 Apr 2025 15:52:06 GMT
ENV XWIKI_DOWNLOAD_SHA256=ec6e09a392b5f0928fee68f40ffe218ceecad3113597127a0ecd8c67d7d8ce00
# Mon, 28 Apr 2025 15:52:06 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
ENV POSTGRES_JDBC_VERSION=42.7.4
# Mon, 28 Apr 2025 15:52:06 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Mon, 28 Apr 2025 15:52:06 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Mon, 28 Apr 2025 15:52:06 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Mon, 28 Apr 2025 15:52:06 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Mon, 28 Apr 2025 15:52:06 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 28 Apr 2025 15:52:06 GMT
VOLUME [/usr/local/xwiki]
# Mon, 28 Apr 2025 15:52:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Apr 2025 15:52:06 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e234c1654a40863255a62f504e30c6694c9fb70e2389306d5384af64337312`  
		Last Modified: Wed, 23 Apr 2025 16:32:09 GMT  
		Size: 17.0 MB (16967805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ac8da3c61b20e48f291d8eb8d7d19d8e11683fe8976dc87255d9f81cfd25f6`  
		Last Modified: Wed, 23 Apr 2025 16:32:10 GMT  
		Size: 52.9 MB (52891051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ade5f85b8cc443b182ffa8554d5ea88c0e7e9e652ac881dd15c98b301c002d`  
		Last Modified: Wed, 23 Apr 2025 16:32:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f02b181578076f6735394e80f8e39ded2df19f6a04e02edf90548c3322d858`  
		Last Modified: Wed, 23 Apr 2025 16:32:09 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225bcf668b860f82474ee20a88cdad47ca4d066ac8d1193f6e086faa9cc0624b`  
		Last Modified: Wed, 23 Apr 2025 18:11:08 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a4a43df0d988028e9414fe7bfdaacf45b678f31bdefcc1cd1d7b62a34676c2`  
		Last Modified: Wed, 23 Apr 2025 18:11:08 GMT  
		Size: 13.8 MB (13829814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebcbc7a75a1da3e6e9852777018148073ca05a6c77081789a381296af0ce625`  
		Last Modified: Wed, 23 Apr 2025 18:11:08 GMT  
		Size: 224.5 KB (224464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d90d14070d0c490497f85f126dbf3436df3986e313281ac1aaeb4e4de4fbc70`  
		Last Modified: Mon, 28 Apr 2025 18:03:11 GMT  
		Size: 191.2 MB (191162914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62391ce90b2b7310dfb088a0d0648d2eb89c1bed8f8d8c8fd2ad855bc8955409`  
		Last Modified: Mon, 28 Apr 2025 18:03:13 GMT  
		Size: 317.4 MB (317400630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319124111e6628a6837fc96e963a1d53d5e43ba0d5c5caaaac0e74081ca96a11`  
		Last Modified: Mon, 28 Apr 2025 18:03:05 GMT  
		Size: 1.0 MB (1013639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52cabe865a97316572b2a590c9b7cfb5b9b6542031b6e6879623d28b94e292a`  
		Last Modified: Mon, 28 Apr 2025 18:03:05 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0028e4292afb02e1fd415409a9d0f7c79c7ebdf9fc9fdee4f94a49dfa1a28f6`  
		Last Modified: Mon, 28 Apr 2025 18:03:06 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec52f64b54403912434eca08152a2a676da6656237109b4be7a1f9f6dcf0d77e`  
		Last Modified: Mon, 28 Apr 2025 18:03:06 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d85fe9c687cddeaf1751068fd8fcc9afbba988d04e7272cf15d089132ad888`  
		Last Modified: Mon, 28 Apr 2025 18:03:07 GMT  
		Size: 2.4 KB (2421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:1e7257460aeb89ae40034decfd37ec4df7919d54b629ccf9c29d5f38fcf36a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8813936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf93189d3070401d4db13039f491530e5e91b7a7fc999ae2bcfe9cb21c4a3a5b`

```dockerfile
```

-	Layers:
	-	`sha256:77252714c3277dc26a6d7803058614b8fa742406803d72e4abacdea0cc42cba4`  
		Last Modified: Mon, 28 Apr 2025 18:03:05 GMT  
		Size: 8.8 MB (8773158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dce81512b0857bce4d829f23620a5054a18e8919a985ff24b5400522ee30c253`  
		Last Modified: Mon, 28 Apr 2025 18:03:05 GMT  
		Size: 40.8 KB (40778 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:e9e44f4a4e46f5eaed507a638f7ffb9aa793854a84edc59b85423197decae565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.1 MB (619141416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f4b8af3e2b20f4aa18a9f4710467715977e1f0695c61371e9815ebc67dd452`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Tue, 08 Apr 2025 20:03:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Apr 2025 20:03:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 20:03:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='8fd14594d0ad8576ba9b698fd10df4a297c548cfdc81cfbe52ac660aeaf5e2b2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 08 Apr 2025 20:03:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 08 Apr 2025 20:03:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Apr 2025 20:03:21 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
WORKDIR /usr/local/tomcat
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 08 Apr 2025 20:03:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_MAJOR=10
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_VERSION=10.1.40
# Tue, 08 Apr 2025 20:03:21 GMT
ENV TOMCAT_SHA512=2bde772acf2e6f300f0f8341eb4de7da5d59af6a95f607bcdb92e4c22e0a253d437ea9a423d7d3e334af1c608f33489f32d32d346fbef5b0abef1dee666895ea
# Tue, 08 Apr 2025 20:03:21 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 08 Apr 2025 20:03:21 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 08 Apr 2025 20:03:21 GMT
ENTRYPOINT []
# Tue, 08 Apr 2025 20:03:21 GMT
CMD ["catalina.sh" "run"]
# Thu, 17 Apr 2025 12:33:22 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 17 Apr 2025 12:33:22 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 17 Apr 2025 12:33:22 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 17 Apr 2025 12:33:22 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 17 Apr 2025 12:33:22 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 17 Apr 2025 12:33:22 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 17 Apr 2025 12:33:22 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 12:33:22 GMT
ENV XWIKI_VERSION=17.2.2
# Thu, 17 Apr 2025 12:33:22 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.2.2
# Thu, 17 Apr 2025 12:33:22 GMT
ENV XWIKI_DOWNLOAD_SHA256=257501fc3cccfcaf7f82f252410aa6cbf080c1ea55a8e158ac9728c29959a992
# Thu, 17 Apr 2025 12:33:22 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 17 Apr 2025 12:33:22 GMT
ENV POSTGRES_JDBC_VERSION=42.7.4
# Thu, 17 Apr 2025 12:33:22 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Thu, 17 Apr 2025 12:33:22 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Thu, 17 Apr 2025 12:33:22 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Thu, 17 Apr 2025 12:33:22 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Thu, 17 Apr 2025 12:33:22 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 17 Apr 2025 12:33:22 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 17 Apr 2025 12:33:22 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 17 Apr 2025 12:33:22 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 17 Apr 2025 12:33:22 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 17 Apr 2025 12:33:22 GMT
VOLUME [/usr/local/xwiki]
# Thu, 17 Apr 2025 12:33:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 12:33:22 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787aea36c8936222fd96cbbd68c43aadaafb0e67fe9615a7545f05fd317f522d`  
		Last Modified: Wed, 09 Apr 2025 06:58:50 GMT  
		Size: 17.0 MB (16987241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4546c95edfbe66ad1c1421b519b2f352df191ae09d09e23373db31e1a3b5b17`  
		Last Modified: Wed, 23 Apr 2025 16:44:36 GMT  
		Size: 52.1 MB (52070843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed393d26aa82fa228d8e57c1dc771ec5cf3e895a66c4a31536ae9b9d2c6d0dd6`  
		Last Modified: Wed, 23 Apr 2025 16:44:34 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64816aa81205a885ebffe5176cdda52a33136c9a0a3dcd7bdfc91a7733cd4c6d`  
		Last Modified: Wed, 23 Apr 2025 16:44:35 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1c215ced66c053aae4349a1c40ab25c210a592b9f8d3f453d6f82f83c8bc0d`  
		Last Modified: Wed, 23 Apr 2025 20:39:13 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc5b7a46bbf3ccf6d2cbb1dfae16fbcbbee0e8492b55029713004cd2051c958`  
		Last Modified: Wed, 23 Apr 2025 20:40:44 GMT  
		Size: 13.8 MB (13832549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2100a72c0a8fd3e298ad75351d4b951b7c752fcf9b5aa57bf6b6a2a99ccd0259`  
		Last Modified: Wed, 23 Apr 2025 20:40:44 GMT  
		Size: 225.0 KB (225007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66c9a792601ce70ed1fe87b191ef2d84dd10c2689567c1245a1ae1c76f9a9e4`  
		Last Modified: Wed, 23 Apr 2025 21:11:36 GMT  
		Size: 188.8 MB (188835856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0e9a8803ebea10dae8127ed5e39682b2e1d0ada7f4b336787ca1300305c44d`  
		Last Modified: Wed, 23 Apr 2025 21:11:36 GMT  
		Size: 317.3 MB (317313832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b58d5fa1c72e55da783397358e8f54b7d00b669d1f30e4873e8d01f3f037e7`  
		Last Modified: Wed, 23 Apr 2025 21:12:05 GMT  
		Size: 1.0 MB (1013641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fa8e4fa1e4f0be2c5e670d554645d420d6d0573c1d98af77b551e2dfb06146`  
		Last Modified: Wed, 23 Apr 2025 21:12:05 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9067b9424cbac67bc23db1d5491f0e6556291491359309de381277483aa2bf9c`  
		Last Modified: Wed, 23 Apr 2025 21:12:05 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e591667239a0a4c6ca0039f688f8576d292700a957a0f72a242df41ddb96dc5a`  
		Last Modified: Wed, 23 Apr 2025 21:12:05 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4a2e2d6b856a525fcd739f664a68ef5224ed50d5d213236d9459db3aa2f29a`  
		Last Modified: Wed, 23 Apr 2025 21:12:06 GMT  
		Size: 2.4 KB (2423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:77ecf3d24b589d2a6edf5ea0eb837a5bbe859f8a02b6f9cef208e09e81ba5c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8810986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a91b8455dfe9f078123b11f278e6cc4926681d50043f18403fe6bd1e3616118`

```dockerfile
```

-	Layers:
	-	`sha256:7489f6c30045c04a3bfaee1e0f422d57316a5dfd032d451b7ffa4e176924d6ad`  
		Last Modified: Wed, 23 Apr 2025 21:12:05 GMT  
		Size: 8.8 MB (8770036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e00186e5cb4da387414017ee6043bbe15c2c3f66f0b1dca82c985dc6431d8c9`  
		Last Modified: Wed, 23 Apr 2025 21:12:05 GMT  
		Size: 41.0 KB (40950 bytes)  
		MIME: application/vnd.in-toto+json
