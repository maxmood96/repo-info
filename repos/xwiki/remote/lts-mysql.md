## `xwiki:lts-mysql`

```console
$ docker pull xwiki@sha256:f697b5b389fe75aad4a70ed8922c88a5a3be4e1a7a3fc261fa836f73ad7b309a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mysql` - linux; amd64

```console
$ docker pull xwiki@sha256:1f6b45a992754e9d624b4b4fe4cf85e086e227ee27f351255fbdec10dc35c6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.7 MB (623673170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523970c3625473c8f490dfe73336685f4a4db987394d17d6e6d3899c42bb2eff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 11 Mar 2025 16:16:28 GMT
ARG RELEASE
# Tue, 11 Mar 2025 16:16:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 11 Mar 2025 16:16:28 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 11 Mar 2025 16:16:28 GMT
CMD ["/bin/bash"]
# Tue, 11 Mar 2025 16:16:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 11 Mar 2025 16:16:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 16:16:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 11 Mar 2025 16:16:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Tue, 11 Mar 2025 16:16:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='6d48379e00d47e6fdd417e96421e973898ac90765ea8ff2d09ae0af6d5d6a1c6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_x64_linux_hotspot_21.0.7_6.tar.gz';          ;;        arm64)          ESUM='ab455a401d25e0cd20e652d2ee72e9f56beba0d9faac5a5c62c9b27a19df804b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.7_6.tar.gz';          ;;        ppc64el)          ESUM='721d3b374cb333269d487e7f99e2d247576c989d2e08a2842738ef62f432bcbd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.7_6.tar.gz';          ;;        riscv64)          ESUM='8fd14594d0ad8576ba9b698fd10df4a297c548cfdc81cfbe52ac660aeaf5e2b2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.7_6.tar.gz';          ;;        s390x)          ESUM='24dddeebdf350d6e0bd6e68176c8eee0a4ff9a5c84efd0fd456848d7ad4c1791';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jre_s390x_linux_hotspot_21.0.7_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 11 Mar 2025 16:16:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 11 Mar 2025 16:16:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 16:16:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
WORKDIR /usr/local/tomcat
# Tue, 11 Mar 2025 16:16:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 11 Mar 2025 16:16:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 11 Mar 2025 16:16:28 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Mar 2025 16:16:28 GMT
ENV TOMCAT_VERSION=9.0.104
# Tue, 11 Mar 2025 16:16:28 GMT
ENV TOMCAT_SHA512=b387fae59f1eda13a5c2336243514d9568057815689057ff920be696548ea6afbcfc0933934d3d6f8c4e2b5108322dc7509bfe934c49d05905c6ce87f1dff53c
# Tue, 11 Mar 2025 16:16:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 11 Mar 2025 16:16:28 GMT
ENTRYPOINT []
# Tue, 11 Mar 2025 16:16:28 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Mar 2025 16:16:28 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
ENV XWIKI_VERSION=16.10.5
# Tue, 11 Mar 2025 16:16:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.5
# Tue, 11 Mar 2025 16:16:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=ecc2d3e639273eff8ecb441aa55a8baefb87ec02826d178fb1e3aff1223dee4d
# Tue, 11 Mar 2025 16:16:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MYSQL_JDBC_VERSION=9.1.0
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Tue, 11 Mar 2025 16:16:28 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Mar 2025 16:16:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 16:16:28 GMT
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
	-	`sha256:bf4abb4ef438e48a41283bd12f494c647983ac21073f78765755f6eb2bbaaa42`  
		Last Modified: Wed, 23 Apr 2025 18:52:15 GMT  
		Size: 191.2 MB (191163274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5a25880a728b3a3a0134871c050f0d09cf19ad9aa0655deb91c7af645c1ec3`  
		Last Modified: Wed, 23 Apr 2025 18:52:18 GMT  
		Size: 316.8 MB (316790020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a48956e8ed74006474357c26f1193e7bb740f2c0e4fe32675e96f210d3d6be6`  
		Last Modified: Wed, 23 Apr 2025 18:52:13 GMT  
		Size: 2.4 MB (2434165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8f515e669cc26ed516249fab0b898da0b243a66af6ca75d711bd651be0819e`  
		Last Modified: Wed, 23 Apr 2025 18:52:13 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885622a5e45a515ec0e4cb7b211e8a57c71fc5b943a1b32afe58f223736608f0`  
		Last Modified: Wed, 23 Apr 2025 18:52:13 GMT  
		Size: 2.4 KB (2374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ad2d03ab489ea2276cd9c4cbfbfe29fdbe9465f23b4889cb42d723b95abdff`  
		Last Modified: Wed, 23 Apr 2025 18:52:14 GMT  
		Size: 6.6 KB (6626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c775c9df6d71d05a6f5ad96b7417ea277c51787165330a437c657ebcbb5248`  
		Last Modified: Wed, 23 Apr 2025 18:52:14 GMT  
		Size: 2.5 KB (2513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mysql` - unknown; unknown

```console
$ docker pull xwiki@sha256:ecf28a78770a9489f3be5c0195cb3de37fa638113f2c1847ddf62a80d6d867e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8801944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb599a3fd2468ba00718fe3521d9bc58eead9a801e07f70cf6dc409e50bbcb8d`

```dockerfile
```

-	Layers:
	-	`sha256:3ab7b1ab8fbbc2b8bbb81438ea49cfa13a5a9d339ff260c1952c1c3baa7fad00`  
		Last Modified: Wed, 23 Apr 2025 18:52:13 GMT  
		Size: 8.8 MB (8760418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:985c05fa547bb5c461fe6da0a9500629c8aebeca122b00b17e56f72c73cf3de5`  
		Last Modified: Wed, 23 Apr 2025 18:52:13 GMT  
		Size: 41.5 KB (41526 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mysql` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:f91160fac956e71c0aa4a19b45f572108522915671e1a89ade1413de4867fc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.7 MB (619672232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f54522afb4e2ddd9b60b82126fc4ae9cde7a0576b5aad8f571b9026181d0271`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
ARG RELEASE
# Thu, 30 Jan 2025 14:32:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 Jan 2025 14:32:57 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='7fc9d6837da5fa1f12e0f41901fd70a73154914b8c8ecbbcad2d44176a989937';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        arm64)          ESUM='f1b78f2bd6d505d5e0539261737740ad11ade3233376b4ca52e6c72fbefd2bf6';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64el)          ESUM='381e31581af3858d4c471829c3da3263e83dfe8ac5d36b58403babb57f6e202c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        riscv64)          ESUM='a8d219a4a97f9c53ba88cb8927910005d4f3d08a87ab1bdebff921ef41afa93d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='7165f6df22dcd8d5bb351560fb0eb0a507d2fc12897b3c8163a36f4eb34e47ce';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 11 Mar 2025 16:16:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 11 Mar 2025 16:16:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 16:16:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
WORKDIR /usr/local/tomcat
# Tue, 11 Mar 2025 16:16:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 11 Mar 2025 16:16:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 11 Mar 2025 16:16:28 GMT
ENV TOMCAT_MAJOR=9
# Tue, 11 Mar 2025 16:16:28 GMT
ENV TOMCAT_VERSION=9.0.104
# Tue, 11 Mar 2025 16:16:28 GMT
ENV TOMCAT_SHA512=b387fae59f1eda13a5c2336243514d9568057815689057ff920be696548ea6afbcfc0933934d3d6f8c4e2b5108322dc7509bfe934c49d05905c6ce87f1dff53c
# Tue, 11 Mar 2025 16:16:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 11 Mar 2025 16:16:28 GMT
ENTRYPOINT []
# Tue, 11 Mar 2025 16:16:28 GMT
CMD ["catalina.sh" "run"]
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 11 Mar 2025 16:16:28 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 11 Mar 2025 16:16:28 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
ENV XWIKI_VERSION=16.10.5
# Tue, 11 Mar 2025 16:16:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.5
# Tue, 11 Mar 2025 16:16:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=ecc2d3e639273eff8ecb441aa55a8baefb87ec02826d178fb1e3aff1223dee4d
# Tue, 11 Mar 2025 16:16:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MYSQL_JDBC_VERSION=9.1.0
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MYSQL_JDBC_SHA256=8776e2ebc46072c9a47ea59d98298c4273bd9f16a7b26b5dfa4744535aa26c62
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MYSQL_JDBC_PREFIX=https://repo1.maven.org/maven2/com/mysql/mysql-connector-j/9.1.0
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MYSQL_JDBC_ARTIFACT=mysql-connector-j-9.1.0.jar
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MYSQL_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mysql-connector-j-9.1.0.jar
# Tue, 11 Mar 2025 16:16:28 GMT
RUN curl -fSL "${MYSQL_JDBC_PREFIX}/${MYSQL_JDBC_ARTIFACT}" -o $MYSQL_JDBC_TARGET &&   echo "$MYSQL_JDBC_SHA256 $MYSQL_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 11 Mar 2025 16:16:28 GMT
VOLUME [/usr/local/xwiki]
# Tue, 11 Mar 2025 16:16:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 16:16:28 GMT
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
	-	`sha256:4f16692c778676906d73d822ec619e2970ded47b269622846a4c7933b754b87b`  
		Last Modified: Wed, 09 Apr 2025 07:08:54 GMT  
		Size: 52.1 MB (52058673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8f51bd58eed49767ea3bf421cf280e982985b1a5bb7a1eba0db547371b75af`  
		Last Modified: Wed, 09 Apr 2025 07:08:52 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffc1b509e96871f44ef99b101d7e6f3b14a1a9894545bc33e960517fef95012`  
		Last Modified: Wed, 09 Apr 2025 07:08:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d2b057f1bfe56ba11c3dd3c937c9fbc1dc3d5bb20e58429fede0aef76ea3d5`  
		Last Modified: Wed, 09 Apr 2025 19:58:25 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c974ee7a4f24a92beb5c7cc2ae1c169f4eb5a3ae6d12d0c64cc006483cf215b1`  
		Last Modified: Thu, 10 Apr 2025 02:10:13 GMT  
		Size: 13.5 MB (13479080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc762f194458b5b50df571710c78667e4717caaffbe23cc6242b718037ed79d`  
		Last Modified: Thu, 10 Apr 2025 02:10:12 GMT  
		Size: 225.0 KB (224966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6ebac42f2722d064d64e43fb80d9e660c3482ff296b31ee5089e322d74dda7`  
		Last Modified: Thu, 10 Apr 2025 03:09:58 GMT  
		Size: 188.8 MB (188835736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26902b986e90ac2e4b812673052e4a7fe33332293bebadcdbf98eea7e248d1a3`  
		Last Modified: Thu, 10 Apr 2025 03:10:00 GMT  
		Size: 316.8 MB (316789912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9598072f5d9c05998f2e01bf2e6323a84aa0c37cebcda083c4a86656fe8da1`  
		Last Modified: Thu, 10 Apr 2025 03:09:54 GMT  
		Size: 2.4 MB (2434168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f44571f99d4092e86463e2aef76b43d521dd63e92eb3552826467c94c0ece10`  
		Last Modified: Thu, 10 Apr 2025 03:09:53 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599f126bf4475d104aeddc7d140e6dff718f256acbbba0d020ac8dd662dc01e9`  
		Last Modified: Thu, 10 Apr 2025 03:09:54 GMT  
		Size: 2.4 KB (2374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49224c7b59b76b0400a973eeb7bd459a568982bb8875020ef057108167fb8118`  
		Last Modified: Thu, 10 Apr 2025 03:09:55 GMT  
		Size: 6.6 KB (6624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91451aae07f2dedc6e96c4a2c0088426775c5aae889852752c8dc50671ab39bd`  
		Last Modified: Thu, 10 Apr 2025 03:09:56 GMT  
		Size: 2.5 KB (2510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mysql` - unknown; unknown

```console
$ docker pull xwiki@sha256:190ca7953ea2058d6f29f2a71876a66fc238dde7443825b313e7841e8e422c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8802943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441755d90841b0b146852e2ba81c8ffe34755e5c68dcfcdf2d190ad9493551d4`

```dockerfile
```

-	Layers:
	-	`sha256:4c0c9138849f15f205778a89035d6f31896545f007968e64f326a71a1ec275e8`  
		Last Modified: Thu, 10 Apr 2025 03:09:53 GMT  
		Size: 8.8 MB (8761207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5e1439b9fd2b0bd0a8cb95e2747abe11a276c316ef99a933334c6a86f4b08f`  
		Last Modified: Thu, 10 Apr 2025 03:09:53 GMT  
		Size: 41.7 KB (41736 bytes)  
		MIME: application/vnd.in-toto+json
