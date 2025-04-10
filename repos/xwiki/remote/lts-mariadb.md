## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:71db1957d1b2f920e81e2831b95b46ba1e1abcecf055f0d84119b1283a759c1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:1d1f89a544d23cc368c7efeeab9086a71646dd389d339de036b106aa89a18828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.9 MB (621911351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a0d6a309a99f7c6a29a8fd9bd15906fa139144278a0d9870e3d205ad5013dd`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
ENV MARIADB_JDBC_VERSION=3.5.2
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MARIADB_JDBC_SHA256=f2f3c3c1a3bdaca69dd1d4e1cd8aed075242fc72ae41463ddb82e367b388f6ad
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.2
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.2.jar
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.2.jar
# Tue, 11 Mar 2025 16:16:28 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:70f077abe239c4b7c52baccfdc40cf1d11599c65c059129059886ba1ce35baf7`  
		Last Modified: Wed, 09 Apr 2025 01:16:40 GMT  
		Size: 17.0 MB (16967596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32015a69421bcce8c43294589f07eede587c47a2a4da89558659befdc27a754`  
		Last Modified: Wed, 09 Apr 2025 01:16:41 GMT  
		Size: 52.9 MB (52876141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b689d8529676c7666da8709db4efbb9cd10fe9e60851b44920556f0057025b23`  
		Last Modified: Wed, 09 Apr 2025 01:16:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b596fb477614cbefc72ad1979a8307c4a41d346ee9db9835a85e6ca807ccb9`  
		Last Modified: Wed, 09 Apr 2025 01:16:39 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002215737f3bd20b883a5ccefeb171f3663734ffbf1b54913e578bb9ac1c32fe`  
		Last Modified: Wed, 09 Apr 2025 22:08:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a677796aeb5a3c9ca1ec86386d1004c9da47f78321b6ca9e29d38417f45c35e7`  
		Last Modified: Wed, 09 Apr 2025 22:08:03 GMT  
		Size: 13.5 MB (13469173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da071d047753acfcd579fe417ea6c8d0e7007b648feb3f0da0f78313639650cf`  
		Last Modified: Wed, 09 Apr 2025 22:08:02 GMT  
		Size: 224.5 KB (224501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4839f47e1a70691fa6643300152ce78484593efac9c8d3161e645f46f5b65cbe`  
		Last Modified: Wed, 09 Apr 2025 23:09:30 GMT  
		Size: 191.2 MB (191162206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7bdc3f68e6e164e6be7ec670a9be56255f3b8668655a96b3da576e9a876e52`  
		Last Modified: Wed, 09 Apr 2025 23:09:50 GMT  
		Size: 316.8 MB (316789959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d81fa693fd5b62fc87181a91df72e9d3dc1edd97de975bfc2428f40567fdbc`  
		Last Modified: Wed, 09 Apr 2025 23:09:19 GMT  
		Size: 688.7 KB (688727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27af77251bbc60919727e037a02b94d438c4efbe88d4ab4e5ad163a0755a4568`  
		Last Modified: Wed, 09 Apr 2025 23:09:19 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899a10078553a5643f118ae7c2faebd19b528257eb906e54a133a590c4a167c8`  
		Last Modified: Wed, 09 Apr 2025 23:09:20 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2270c1e14288cfafa3acae7c48d25799afa01183a8c2328f6c162e6e83769922`  
		Last Modified: Wed, 09 Apr 2025 23:09:21 GMT  
		Size: 6.6 KB (6623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fbd8faf4c9e9469b4d8966170003f61654704175a22cb2bc091caa72374859`  
		Last Modified: Wed, 09 Apr 2025 23:09:21 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:c1d1bc363da792a500612de7fe88d1df98b47c700d7834b2a4e1d573ab9d813d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8799679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10258f0e5dbde7a13ff11407e1a1709c126ce68c5594291da2e7eff0816fe259`

```dockerfile
```

-	Layers:
	-	`sha256:a4851ef0a3136b52fa43ea1c41e4d3463564394391f7f2684dd5991e8247b266`  
		Last Modified: Wed, 09 Apr 2025 23:09:19 GMT  
		Size: 8.8 MB (8759197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:196491cff3eb735385a8c1730caff95ac063716bdfe99ca6a300fc57f1859cb9`  
		Last Modified: Wed, 09 Apr 2025 23:09:19 GMT  
		Size: 40.5 KB (40482 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:ca6719005a95877ce2c37e79a12a8bef707adfd8c10604768239d6a3550e940a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.9 MB (617926693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3ff837b30da15fac085f4b3a776f3284a4ecf4cd32e1a9ed5a83c8fa000aa2`
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
ENV MARIADB_JDBC_VERSION=3.5.2
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MARIADB_JDBC_SHA256=f2f3c3c1a3bdaca69dd1d4e1cd8aed075242fc72ae41463ddb82e367b388f6ad
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.2
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.2.jar
# Tue, 11 Mar 2025 16:16:28 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.2.jar
# Tue, 11 Mar 2025 16:16:28 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:973c87a3f3d37f2ae6484f1b9c710c8a44e4a623f392dc0f352be452895445db`  
		Last Modified: Thu, 10 Apr 2025 03:11:01 GMT  
		Size: 688.7 KB (688728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d4a06fd119d182489bde2fcb5a3e2fdc4acfeb314490bf072935571fa53837`  
		Last Modified: Thu, 10 Apr 2025 03:11:01 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0cc2c7a0aa6dfe12b79ff695c6e1e88d206971cd4b8e7ca07e356ed61901f6`  
		Last Modified: Thu, 10 Apr 2025 03:11:01 GMT  
		Size: 2.3 KB (2312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb95eacb3b6152318c10943c76c3de9e74c27b40612092ad7150e6c402597444`  
		Last Modified: Thu, 10 Apr 2025 03:11:01 GMT  
		Size: 6.6 KB (6626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3375428918a338ddc4f2f911dfef2bb3c6eecf25b8229ea97b26fce8704461`  
		Last Modified: Thu, 10 Apr 2025 03:11:02 GMT  
		Size: 2.5 KB (2474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:936739f1863154934cb49683c77f7a832d28de5690dfe0f844cdc9ffd07309e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8800581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ea200909ed1a388815dd46bcb806d9df7390678baeb98f2f71f07a1a0b2f2a`

```dockerfile
```

-	Layers:
	-	`sha256:300326a8c5a7faf3357dafa28271a9f59ae33ffa9f31b522b6e84ef83d3f50cf`  
		Last Modified: Thu, 10 Apr 2025 03:11:01 GMT  
		Size: 8.8 MB (8759938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c0486eb93d5cc745c71d83e7508e938a960f391d16fdccb6b91d18d195c0d7`  
		Last Modified: Thu, 10 Apr 2025 03:11:00 GMT  
		Size: 40.6 KB (40643 bytes)  
		MIME: application/vnd.in-toto+json
