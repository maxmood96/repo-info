## `xwiki:16-postgres-tomcat`

```console
$ docker pull xwiki@sha256:aaaa063558028c5f718345e55527abb34f00beb943e1832cc7b779098a7b89e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:16-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:742613c5cf4c9fa828533549b53c016d143e6da7ee9556f9b953745f38e83217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.5 MB (622519082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe92a17a390332eb7da78c8e6dd77ddd7629da90dd9dd85e70110e126892034`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 09 Apr 2025 20:03:41 GMT
ARG RELEASE
# Wed, 09 Apr 2025 20:03:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Apr 2025 20:03:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Apr 2025 20:03:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Apr 2025 20:03:41 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["/bin/bash"]
# Wed, 09 Apr 2025 20:03:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Apr 2025 20:03:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 20:03:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='8fd14594d0ad8576ba9b698fd10df4a297c548cfdc81cfbe52ac660aeaf5e2b2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Apr 2025 20:03:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Apr 2025 20:03:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 20:03:41 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 20:03:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_MAJOR=9
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_VERSION=9.0.104
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_SHA512=b387fae59f1eda13a5c2336243514d9568057815689057ff920be696548ea6afbcfc0933934d3d6f8c4e2b5108322dc7509bfe934c49d05905c6ce87f1dff53c
# Wed, 09 Apr 2025 20:03:41 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Apr 2025 20:03:41 GMT
ENTRYPOINT []
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["catalina.sh" "run"]
# Fri, 25 Apr 2025 08:12:38 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 25 Apr 2025 08:12:38 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 25 Apr 2025 08:12:38 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 25 Apr 2025 08:12:38 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 25 Apr 2025 08:12:38 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 25 Apr 2025 08:12:38 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 25 Apr 2025 08:12:38 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 08:12:38 GMT
ENV XWIKI_VERSION=16.10.6
# Fri, 25 Apr 2025 08:12:38 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.6
# Fri, 25 Apr 2025 08:12:38 GMT
ENV XWIKI_DOWNLOAD_SHA256=b36e814a766e72ce0774a752f5c595ff144f712b36de34fd6869388b3c5f800e
# Fri, 25 Apr 2025 08:12:38 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 25 Apr 2025 08:12:38 GMT
ENV POSTGRES_JDBC_VERSION=42.7.4
# Fri, 25 Apr 2025 08:12:38 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Fri, 25 Apr 2025 08:12:38 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Fri, 25 Apr 2025 08:12:38 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Fri, 25 Apr 2025 08:12:38 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Fri, 25 Apr 2025 08:12:38 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 25 Apr 2025 08:12:38 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 25 Apr 2025 08:12:38 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 25 Apr 2025 08:12:38 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 25 Apr 2025 08:12:38 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 25 Apr 2025 08:12:38 GMT
VOLUME [/usr/local/xwiki]
# Fri, 25 Apr 2025 08:12:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 08:12:38 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b37af7090fe748226651b75e9eff059c91046da0e4d304f742c24a4437fb81`  
		Last Modified: Thu, 08 May 2025 17:04:56 GMT  
		Size: 17.0 MB (16967882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32efa2d47a978264cf9a212886396adff5e076f0390cdf2bfebcfad4c6347d3`  
		Last Modified: Thu, 08 May 2025 17:04:58 GMT  
		Size: 52.9 MB (52891102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f6621fedbae0a518f88bd221b3bcd6c0cba45111f49a0076d9646b9a125f3e`  
		Last Modified: Thu, 08 May 2025 17:04:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141779bd67f4ce6dfe1c84578df8cfa3a860859d4ed985965e00660f8404b05f`  
		Last Modified: Thu, 08 May 2025 17:04:56 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bac99a65b373e8d8a339bdb4c95f7be35fcaaa6339b60d4c98f2996fc78f57`  
		Last Modified: Thu, 08 May 2025 19:05:27 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e106bbeb2fa3d6748db7a35d1eace5b3f250907a8106f35c640c1b75663a7c`  
		Last Modified: Thu, 08 May 2025 19:05:31 GMT  
		Size: 13.5 MB (13469241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5b82b3bed42992db0347ea7ee686886520efd96132fc8c6d808168256e02a5`  
		Last Modified: Thu, 08 May 2025 19:05:29 GMT  
		Size: 224.6 KB (224581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48373d028fddee95ab42654cf31c1a4397d95246debc23fcfcd87898256ed98`  
		Last Modified: Thu, 08 May 2025 22:02:10 GMT  
		Size: 191.2 MB (191163696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b714b98954ec171c5290db6538b804aa40f627f56f7281bf08a2a4fd3daf6d6`  
		Last Modified: Thu, 08 May 2025 22:02:12 GMT  
		Size: 317.1 MB (317055907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce8f240f475722785261a3fa4b5b812e922586674e329622c32e59874d85855`  
		Last Modified: Thu, 08 May 2025 22:01:52 GMT  
		Size: 1.0 MB (1013643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d5a30d2ccb5771352e3a6781aaa6f7779855cad02db55f4ac614153a3eb71b`  
		Last Modified: Thu, 08 May 2025 22:01:53 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f93c1e61de0e78f10c276a85df5382476dd385e420f969a660f73ef48dad44`  
		Last Modified: Thu, 08 May 2025 22:01:53 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572dee1246a2e807442788ca84dd0ee3d14da8839e7ade24903c625b49854d7e`  
		Last Modified: Thu, 08 May 2025 22:01:54 GMT  
		Size: 6.6 KB (6630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08af56434635990c97b6ec5efe1e078886acd2d1219481d5f1125194fbc8fe73`  
		Last Modified: Thu, 08 May 2025 22:01:55 GMT  
		Size: 2.4 KB (2421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:ea57319ac8d4fa4a68f11a69ea9adfa6db2e56a6955b310b8808b985aed0ff24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8799688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c1615f1c20d5f28f51918ebe9afcb2a43986c8222c6fda8c6576fa465014dc`

```dockerfile
```

-	Layers:
	-	`sha256:cc0f90e9cb4a0fea5ddb49b058986ca10e3ed3112b92f7026ea78b78ed2aab0f`  
		Last Modified: Mon, 05 May 2025 17:16:27 GMT  
		Size: 8.8 MB (8759232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3b6ba0984c112c103c378000a7de4d80cd3668b3807e51eb2f75c7dbb350112`  
		Last Modified: Mon, 05 May 2025 17:16:27 GMT  
		Size: 40.5 KB (40456 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:16-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:6fa87077a9d193fed8ff687e93ed1085d5250903e85db169a94021ee9d55e1e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.5 MB (618532004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71be91f9002cd1cf5db6acdd4e9ec5168ecf983d20c0c2401fcd39cf3e6bbda6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 09 Apr 2025 20:03:41 GMT
ARG RELEASE
# Wed, 09 Apr 2025 20:03:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Apr 2025 20:03:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Apr 2025 20:03:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Apr 2025 20:03:41 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["/bin/bash"]
# Wed, 09 Apr 2025 20:03:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 09 Apr 2025 20:03:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 20:03:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='8fd14594d0ad8576ba9b698fd10df4a297c548cfdc81cfbe52ac660aeaf5e2b2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 09 Apr 2025 20:03:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 09 Apr 2025 20:03:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 20:03:41 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
WORKDIR /usr/local/tomcat
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 20:03:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_MAJOR=9
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_VERSION=9.0.104
# Wed, 09 Apr 2025 20:03:41 GMT
ENV TOMCAT_SHA512=b387fae59f1eda13a5c2336243514d9568057815689057ff920be696548ea6afbcfc0933934d3d6f8c4e2b5108322dc7509bfe934c49d05905c6ce87f1dff53c
# Wed, 09 Apr 2025 20:03:41 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Wed, 09 Apr 2025 20:03:41 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 09 Apr 2025 20:03:41 GMT
ENTRYPOINT []
# Wed, 09 Apr 2025 20:03:41 GMT
CMD ["catalina.sh" "run"]
# Fri, 25 Apr 2025 08:12:38 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 25 Apr 2025 08:12:38 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 25 Apr 2025 08:12:38 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 25 Apr 2025 08:12:38 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 25 Apr 2025 08:12:38 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 25 Apr 2025 08:12:38 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 25 Apr 2025 08:12:38 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 08:12:38 GMT
ENV XWIKI_VERSION=16.10.6
# Fri, 25 Apr 2025 08:12:38 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.6
# Fri, 25 Apr 2025 08:12:38 GMT
ENV XWIKI_DOWNLOAD_SHA256=b36e814a766e72ce0774a752f5c595ff144f712b36de34fd6869388b3c5f800e
# Fri, 25 Apr 2025 08:12:38 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 25 Apr 2025 08:12:38 GMT
ENV POSTGRES_JDBC_VERSION=42.7.4
# Fri, 25 Apr 2025 08:12:38 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Fri, 25 Apr 2025 08:12:38 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Fri, 25 Apr 2025 08:12:38 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Fri, 25 Apr 2025 08:12:38 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Fri, 25 Apr 2025 08:12:38 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 25 Apr 2025 08:12:38 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 25 Apr 2025 08:12:38 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 25 Apr 2025 08:12:38 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 25 Apr 2025 08:12:38 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 25 Apr 2025 08:12:38 GMT
VOLUME [/usr/local/xwiki]
# Fri, 25 Apr 2025 08:12:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Apr 2025 08:12:38 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44030c5633c35d5105714bc1403c988244c1f643b1d66f623b7e1beade4140a0`  
		Last Modified: Thu, 08 May 2025 17:05:03 GMT  
		Size: 17.0 MB (16987252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1edce5df06912fb7c1f943a4fdcc192ed2282e8a795c800db4cd61fb8f5935`  
		Last Modified: Thu, 08 May 2025 17:06:23 GMT  
		Size: 52.1 MB (52070835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e295f77fb1bd212dd73e0301b0b5cff71e9564d4a487bf64c2b88759daae55d`  
		Last Modified: Thu, 08 May 2025 17:06:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e7a787b9c4da917cc3eb5f7e0cf9f791850f69f59f064f405c346749840d09`  
		Last Modified: Thu, 08 May 2025 17:06:20 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c91c72e07b6db4896190bfe41b8904dd6d4236b3c3b40c752b68dee87652a2`  
		Last Modified: Thu, 08 May 2025 17:36:25 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2f5394530a86b35307fdcba0f00699aa58aee87d3d496ca1fcb7f70c23f7da`  
		Last Modified: Tue, 06 May 2025 02:11:36 GMT  
		Size: 13.5 MB (13479214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36dac692b7891efc29a55495deece859be529a0aa06e674296a19451bf394b53`  
		Last Modified: Tue, 06 May 2025 02:11:36 GMT  
		Size: 225.0 KB (224956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f50094e45cc23e1077bb8934d62e06e378bc7f91ce131a81bc992bca3229a33`  
		Last Modified: Tue, 06 May 2025 04:10:41 GMT  
		Size: 188.8 MB (188837873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91824d2c10f89db8ff8ee63c12a3e7d673394aca64a1375b661163b4302f02d`  
		Last Modified: Tue, 06 May 2025 04:10:45 GMT  
		Size: 317.1 MB (317055856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b065ea9c6ca3af21cf992ea2205e98e42c627ab8d07b5044b2d1b372ce6729b9`  
		Last Modified: Tue, 06 May 2025 04:11:22 GMT  
		Size: 1.0 MB (1013640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00ccf0a4466e18459ed220e224e1de6a204f29cbad57e2ef8491d2b5304323e`  
		Last Modified: Tue, 06 May 2025 04:11:21 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca5186a3ee3fd4ac0f92c7746b5821f67d9f634beb08ac21ec7ced6356ace3f`  
		Last Modified: Tue, 06 May 2025 04:11:22 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b1ea832b2da20c6bfefb4ad7a5de48da3cd848172590b7f6fceb6fb3dbd10b`  
		Last Modified: Tue, 06 May 2025 04:11:22 GMT  
		Size: 6.6 KB (6633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a44180df54a30873774e13d9c4b54405963add2218567334031c38a2fb03ea`  
		Last Modified: Tue, 06 May 2025 04:11:22 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:8912c88c07a4ab98bef80565b70f0ffeec4aea00bca3eb1a2ef0457c1b315f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8800591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6cdb4def4e0f93036ac9b65dd3a36c9ae260b3adb998d198e1e392ae08ee57`

```dockerfile
```

-	Layers:
	-	`sha256:2948aafbf2197e8060fbc34dbcfd774c11e6ed3f332ff1b9d15ce923c7e82d5c`  
		Last Modified: Tue, 06 May 2025 04:11:22 GMT  
		Size: 8.8 MB (8759973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f93ff0a8302e719d054ee0c5340aeb0f7d217ad127c823e7615bce4b1a655e2`  
		Last Modified: Tue, 06 May 2025 04:11:21 GMT  
		Size: 40.6 KB (40618 bytes)  
		MIME: application/vnd.in-toto+json
