## `xwiki:lts`

```console
$ docker pull xwiki@sha256:8fe94a8c55e4e917056d90d0c35c5f8af78e381d07e858345792627ca61e8270
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts` - linux; amd64

```console
$ docker pull xwiki@sha256:0610710ebc0725c605903843256d607a7a660b30c15d610d8e9a92e3fc197854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.9 MB (623939059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59202a27835ada12d3c50d869374ea7ecce33eb8826166930017dd5e9f6bfe66`
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
ENV MYSQL_JDBC_VERSION=9.1.0
# Fri, 25 Apr 2025 08:12:38 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Fri, 25 Apr 2025 08:12:38 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Fri, 25 Apr 2025 08:12:38 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Fri, 25 Apr 2025 08:12:38 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Fri, 25 Apr 2025 08:12:38 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:c141aa23c0c9533f86f061c5c9940fce8f6ec03c85857e78f7a72a8e8c06bf89`  
		Last Modified: Wed, 23 Apr 2025 18:11:14 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111f8859b4f9faed6c8b9b8a205360d387cd70750c6c22cea8a781d0c6d365bb`  
		Last Modified: Wed, 23 Apr 2025 18:11:14 GMT  
		Size: 13.5 MB (13469231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2a4087ca9dfb5fa6da7f638d1fe538f4b4469e0ff4ce3e49ff04e9e7917077`  
		Last Modified: Wed, 23 Apr 2025 18:11:14 GMT  
		Size: 224.5 KB (224472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee764bd94a809894dd8a1831e51c5fe9f7fb98fd5c6385fea1742006608e83a`  
		Last Modified: Fri, 25 Apr 2025 17:42:43 GMT  
		Size: 191.2 MB (191163334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c96d6a302600d6ada8c3418b1e01a3796848f8ecf8cd5e201baaf425886232`  
		Last Modified: Fri, 25 Apr 2025 17:42:45 GMT  
		Size: 317.1 MB (317055837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69add01e323ef89c08f6ba886f5e0633948af43250d2512791c0fe5c53473a9`  
		Last Modified: Fri, 25 Apr 2025 17:42:40 GMT  
		Size: 2.4 MB (2434168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb7072259fd20cf14845ee9f767ae9cd19945dc1337bfeef7bc17bfd956d5b9`  
		Last Modified: Fri, 25 Apr 2025 17:42:40 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5deb15b451e321e4a0cae8c56d5d82cf25dc745df80e424d27e9fb506fb30a`  
		Last Modified: Fri, 25 Apr 2025 17:42:41 GMT  
		Size: 2.4 KB (2375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e42ac6149112d0502fa753c6db7593305e456385289bc976110c141c38810a`  
		Last Modified: Fri, 25 Apr 2025 17:42:41 GMT  
		Size: 6.6 KB (6632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e2d9884169706af66e4fea313c5586b36aa77b1d47f0311a0735fd7882b9fa`  
		Last Modified: Fri, 25 Apr 2025 17:42:42 GMT  
		Size: 2.5 KB (2514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts` - unknown; unknown

```console
$ docker pull xwiki@sha256:97c4d449f6761017d33ae017cd5339b63645a61313586d1269e35c69c3c949d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8801961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decdc772600c26d502c27765b56f1ec7ec2e01776b1c13ba2e5865ecce3ba922`

```dockerfile
```

-	Layers:
	-	`sha256:8b4927b3e5b13fe6266148f02b60a142709414d0e551b53a0ca1c29bb85a6b59`  
		Last Modified: Fri, 25 Apr 2025 17:42:40 GMT  
		Size: 8.8 MB (8760434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0889f0e2ba72747508f483ead4bc98d7cb5b1363eb279ee69e7132fa33493d0f`  
		Last Modified: Fri, 25 Apr 2025 17:42:40 GMT  
		Size: 41.5 KB (41527 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:913f4ae482c53f61846e1fd1453118f3ec691d0387d733327b1116dfb6191611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.0 MB (619950454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fb4309ebaba92bfc1758bc5d0d3ae6b75762c5bc16d49dadd4abe75f3e0fd0`
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
ENV MYSQL_JDBC_VERSION=9.1.0
# Fri, 25 Apr 2025 08:12:38 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Fri, 25 Apr 2025 08:12:38 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Fri, 25 Apr 2025 08:12:38 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Fri, 25 Apr 2025 08:12:38 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Fri, 25 Apr 2025 08:12:38 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:a8631052c0359c88d81dfe241343b1153b176793df73209cfe35e2f8eefd5cb7`  
		Last Modified: Wed, 23 Apr 2025 20:42:47 GMT  
		Size: 13.5 MB (13479146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c654948bc94a9ff4c1b1c2526b2943998144ce512c4945a340388a187ebbf352`  
		Last Modified: Wed, 23 Apr 2025 20:42:46 GMT  
		Size: 225.0 KB (224994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a78c0bca61b9df92577eadce8414bdf04a7734b54fd408be26c48c4b53fe0d`  
		Last Modified: Wed, 23 Apr 2025 21:14:19 GMT  
		Size: 188.8 MB (188835704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5876cb984a1b833b8e3929a9a60f2497b5964e87625e56e766f6f00c4dbbb009`  
		Last Modified: Fri, 25 Apr 2025 17:41:48 GMT  
		Size: 317.1 MB (317055901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1670716a1d511e2d893b950d7e32bfcdb98e92fc243670ed95b0bdf564add76c`  
		Last Modified: Fri, 25 Apr 2025 17:41:41 GMT  
		Size: 2.4 MB (2434167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a934af8235c2846494ab3531be629526d93d4cbe69926b06bbbe6e9e9958ca`  
		Last Modified: Fri, 25 Apr 2025 17:41:40 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b597907aadbda52fc78487704a59b05fbe639706dd9e671a875fedf7ee9d4069`  
		Last Modified: Fri, 25 Apr 2025 17:41:40 GMT  
		Size: 2.4 KB (2372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf1e9d679e058d4f1b78642790ebf797cbf8ed584f3752f2d4c046c65adcb4f`  
		Last Modified: Fri, 25 Apr 2025 17:41:41 GMT  
		Size: 6.6 KB (6629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfdd88929b66b82da9413f27eb78491b0c75ae8b962abaa973f418eb40817c8`  
		Last Modified: Fri, 25 Apr 2025 17:41:41 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts` - unknown; unknown

```console
$ docker pull xwiki@sha256:debc10f6c5244e0ad29b096aea36f3abbc02af298774018c83aca6cee5bd1c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8802958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7c60f269f87b41fefdbe72953fd6cdf1fadc6ba1a797e078dbbc8b7e19c149`

```dockerfile
```

-	Layers:
	-	`sha256:113a284fcadb0f22c6764da124550c5ce42f7ca649bd3c9af1e5423c28a4e6e1`  
		Last Modified: Fri, 25 Apr 2025 17:41:41 GMT  
		Size: 8.8 MB (8761223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:224bd668016dd2644749445b7035d24e972b60130dcc765da1c266d3f2b56bb4`  
		Last Modified: Fri, 25 Apr 2025 17:41:40 GMT  
		Size: 41.7 KB (41735 bytes)  
		MIME: application/vnd.in-toto+json
