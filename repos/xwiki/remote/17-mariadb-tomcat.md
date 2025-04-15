## `xwiki:17-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:f22ce4ae3db0fb1df204cdae61c479d7bb08cbd44188f6e8465a4098e3d88df2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:17-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:1f7cc46b874c11b05c5e196cb5f8089ef7664837d3c8f77fb8461ea1850e9c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.8 MB (622800133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb301e0c397d666bf45e2d640ce8a3ea03ba6e0b7e09e4194122cb28670ec794`
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
# Mon, 14 Apr 2025 12:16:51 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 14 Apr 2025 12:16:51 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 14 Apr 2025 12:16:51 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 14 Apr 2025 12:16:51 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 14 Apr 2025 12:16:51 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 14 Apr 2025 12:16:51 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 14 Apr 2025 12:16:51 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 12:16:51 GMT
ENV XWIKI_VERSION=17.2.1
# Mon, 14 Apr 2025 12:16:51 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.2.1
# Mon, 14 Apr 2025 12:16:51 GMT
ENV XWIKI_DOWNLOAD_SHA256=333fd344762ae820a4bcb8cdbb2b2c62dfd567aac9382d2e896ff46c1fca5632
# Mon, 14 Apr 2025 12:16:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 14 Apr 2025 12:16:51 GMT
ENV MARIADB_JDBC_VERSION=3.5.3
# Mon, 14 Apr 2025 12:16:51 GMT
ENV MARIADB_JDBC_SHA256=85c4ba2f221d0dfd439c26affbb294f784960763544263c65aba9c2c76858706
# Mon, 14 Apr 2025 12:16:51 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.3
# Mon, 14 Apr 2025 12:16:51 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.3.jar
# Mon, 14 Apr 2025 12:16:51 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.3.jar
# Mon, 14 Apr 2025 12:16:51 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 14 Apr 2025 12:16:51 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 14 Apr 2025 12:16:51 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 14 Apr 2025 12:16:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 14 Apr 2025 12:16:51 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 14 Apr 2025 12:16:51 GMT
VOLUME [/usr/local/xwiki]
# Mon, 14 Apr 2025 12:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 12:16:51 GMT
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
	-	`sha256:73d7aa9422b09dba2e0f062dd20ec4a3dc69feafc069a9c37bb903689f117b65`  
		Last Modified: Wed, 09 Apr 2025 03:11:17 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113211f9a6aac869da5f42af6576d21295758d65a6fcef6d05df1dd40ba3be71`  
		Last Modified: Wed, 09 Apr 2025 03:11:20 GMT  
		Size: 13.8 MB (13829786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68ee9fe8c965f64d6810d8d7c97714c7a3c7d8a200be104b971022ce254e921`  
		Last Modified: Wed, 09 Apr 2025 03:11:19 GMT  
		Size: 224.5 KB (224476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeed4d9c09360e1854a78f771186290b02a26e4abf3e762bf35d72276a95d1b`  
		Last Modified: Mon, 14 Apr 2025 21:12:58 GMT  
		Size: 191.2 MB (191162195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370b3cb5d35990e9e105d78f1f731ec687544348a7e0e3fa0a87821cf631941b`  
		Last Modified: Mon, 14 Apr 2025 21:13:03 GMT  
		Size: 317.3 MB (317315259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce247aa5d5761303ee02f3029df47c7583e2370129630014f128f74fee5592c`  
		Last Modified: Mon, 14 Apr 2025 21:12:54 GMT  
		Size: 691.6 KB (691649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b0f585bbead95849bef44adfcd6ec709783bfcf596d05372788567b9c54632`  
		Last Modified: Mon, 14 Apr 2025 21:12:54 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ff50738f416410f7c63419b64663103d911bbfa11d8afa550a06c4f513aa41`  
		Last Modified: Mon, 14 Apr 2025 21:12:55 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb24f4b1ad088338cfbc0af0a1de33cdd531f0300a340fe9125be04cc5d98b4`  
		Last Modified: Mon, 14 Apr 2025 21:12:56 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d397104c20464f9789c2dd08e94374a0370f59daed31beac1d005a38c6ab9f`  
		Last Modified: Mon, 14 Apr 2025 21:12:56 GMT  
		Size: 2.5 KB (2473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:343ed8fbe72cc68fcfec277b12a1084ac1d8a23e3c70caeb91a1dea18c839b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8810067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a841f1e5361834e154c75e9e2b82a9cd8ba438ecf08176630c1dea610775cec1`

```dockerfile
```

-	Layers:
	-	`sha256:7576d4174f9c6a888a4d5a7669454514f46ce3573d8ac0174846b0d828f6cedd`  
		Last Modified: Mon, 14 Apr 2025 21:12:54 GMT  
		Size: 8.8 MB (8769266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47f4b510109c0334bfa61c3c7094e60fe999490650db62548df70700c9bafae0`  
		Last Modified: Mon, 14 Apr 2025 21:12:54 GMT  
		Size: 40.8 KB (40801 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:17-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:bf0341658244bb0fe0eb1ea87edbf26c6b275c8c514088a5f22abd20d3dbfe9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.8 MB (618808555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fad7a0c1980343cf7b5995c514ae61b5266a011e13263e7928795bd7469ff89`
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
# Mon, 14 Apr 2025 12:16:51 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 14 Apr 2025 12:16:51 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 14 Apr 2025 12:16:51 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 14 Apr 2025 12:16:51 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 14 Apr 2025 12:16:51 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 14 Apr 2025 12:16:51 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 14 Apr 2025 12:16:51 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 12:16:51 GMT
ENV XWIKI_VERSION=17.2.1
# Mon, 14 Apr 2025 12:16:51 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.2.1
# Mon, 14 Apr 2025 12:16:51 GMT
ENV XWIKI_DOWNLOAD_SHA256=333fd344762ae820a4bcb8cdbb2b2c62dfd567aac9382d2e896ff46c1fca5632
# Mon, 14 Apr 2025 12:16:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 14 Apr 2025 12:16:51 GMT
ENV MARIADB_JDBC_VERSION=3.5.3
# Mon, 14 Apr 2025 12:16:51 GMT
ENV MARIADB_JDBC_SHA256=85c4ba2f221d0dfd439c26affbb294f784960763544263c65aba9c2c76858706
# Mon, 14 Apr 2025 12:16:51 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.3
# Mon, 14 Apr 2025 12:16:51 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.3.jar
# Mon, 14 Apr 2025 12:16:51 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.3.jar
# Mon, 14 Apr 2025 12:16:51 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 14 Apr 2025 12:16:51 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 14 Apr 2025 12:16:51 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 14 Apr 2025 12:16:51 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 14 Apr 2025 12:16:51 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 14 Apr 2025 12:16:51 GMT
VOLUME [/usr/local/xwiki]
# Mon, 14 Apr 2025 12:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Apr 2025 12:16:51 GMT
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
	-	`sha256:0182870468cecabacf784077b3bcd5e1ae569ded8633d974d8abe253235258ad`  
		Last Modified: Wed, 09 Apr 2025 19:58:26 GMT  
		Size: 13.8 MB (13832502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30d1ad11d2c5eafc4e836202b600fde88fc7adbff2643f2c9ab40845638f36d`  
		Last Modified: Wed, 09 Apr 2025 19:58:25 GMT  
		Size: 225.0 KB (224974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e8763975c56b2f000f6d42d70c46191c413c068027ff235e896f31d1cdb12a`  
		Last Modified: Wed, 09 Apr 2025 23:50:12 GMT  
		Size: 188.8 MB (188835939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fd33a3ddcf45de46b10fc095a6ccb3e77de5dc5fd7b497de6cb928b59924d1`  
		Last Modified: Mon, 14 Apr 2025 21:12:47 GMT  
		Size: 317.3 MB (317315234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc1839a841ffe522d93cf34e9946604e2c6a82a9c5a310a2c5bbb259bfe703a`  
		Last Modified: Mon, 14 Apr 2025 21:13:49 GMT  
		Size: 691.7 KB (691652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2dfc8c12986e2faf197acec34b083ad703ce3329b1e5e2c1905e1dcd5714f34`  
		Last Modified: Mon, 14 Apr 2025 21:13:48 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1804bffe85b6166a209241aa68e4bf0cd2f8ae4a70e64ad97515e57e44653f17`  
		Last Modified: Mon, 14 Apr 2025 21:13:48 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84056fc8c69934a68a97d2108a90305a87e752a437025d5805f173d7dd7d45a9`  
		Last Modified: Mon, 14 Apr 2025 21:13:48 GMT  
		Size: 6.6 KB (6609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3122281f380758fcecfaecde5ae8be028ea1d4e320bdfbfaf1ec25982be5ec9`  
		Last Modified: Mon, 14 Apr 2025 21:13:49 GMT  
		Size: 2.5 KB (2476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:17-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:b1a0978c5acd8d612896a8625b2eaac07490747685d2fa8f90b79b6542811e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8810993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6851386956f6ce9c0321626fdef88335bd1e6266ac0eb64fa0eebee98c88e04a`

```dockerfile
```

-	Layers:
	-	`sha256:4cb351fa1bf99b5b809286e5a48876d28197efac6f5fcf8e291b67e56e44c0ab`  
		Last Modified: Mon, 14 Apr 2025 21:13:48 GMT  
		Size: 8.8 MB (8770019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57dfae89e361f4f1ec5a65a6f0d8113e101986d99b05937ab54f34f0cd231f59`  
		Last Modified: Mon, 14 Apr 2025 21:13:48 GMT  
		Size: 41.0 KB (40974 bytes)  
		MIME: application/vnd.in-toto+json
