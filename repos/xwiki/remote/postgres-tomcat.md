## `xwiki:postgres-tomcat`

```console
$ docker pull xwiki@sha256:2cc00c726c9be077f5aa5c01f0de87c4b1620c9673d8663c91ec312e3473d78b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:f52ad1cd84599dea0b51e97416a70bb5800fc28c2f9849a333e0bc9e8edafe4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.1 MB (623122443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0f04ff3795661ac04ccdf85e7f4105c5f491e57a1c1c509d31eb2b8e2efd64`
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
ENV POSTGRES_JDBC_VERSION=42.7.4
# Mon, 14 Apr 2025 12:16:51 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Mon, 14 Apr 2025 12:16:51 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Mon, 14 Apr 2025 12:16:51 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Mon, 14 Apr 2025 12:16:51 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Mon, 14 Apr 2025 12:16:51 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:1ca3736ccf54a00c795dbd9c5f4292ac7853cc78f48a957c88e5c52870e1c9bb`  
		Last Modified: Mon, 14 Apr 2025 21:12:45 GMT  
		Size: 191.2 MB (191162487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beec5c93b27575a035eab52d18d5613939aea9b23189c3a444b5686532106c7`  
		Last Modified: Mon, 14 Apr 2025 21:12:48 GMT  
		Size: 317.3 MB (317315192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00afb576eb2b75ccd4fb1505946bfa020a7f023952249b17cf89177f536ce54`  
		Last Modified: Mon, 14 Apr 2025 21:12:42 GMT  
		Size: 1.0 MB (1013643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0331f2b0f5dd28855be4e14e82cd4588a9f5eb0d1d20f97febcc92807d6304`  
		Last Modified: Mon, 14 Apr 2025 21:12:42 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7637ddc257d22f9120abc55cfc663e84700d1b55ae73fb045d82f4c1c183e900`  
		Last Modified: Mon, 14 Apr 2025 21:12:43 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c150216fc1d301ed1079ad9209581106da82ce9436bb5e576ee5ce2f35cbb30d`  
		Last Modified: Mon, 14 Apr 2025 21:12:43 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f9c8d47027e03c29b0d23b96ec6e5076056ec4071f57200551d54da4eb56f6`  
		Last Modified: Mon, 14 Apr 2025 21:12:43 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:3a168348dcba54e3fe766c1ae63509d988f4df8a8c360ef92a0579920343fda3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8810061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b3f8982b46f3d1dfc5979ca7bd8836bde9e00bb94aad9a7442858fae4d1692`

```dockerfile
```

-	Layers:
	-	`sha256:0beb3a38e7e9bb21b6a1da57fa9e34c65a909465fa5fa4ca4a7478289a53fb90`  
		Last Modified: Mon, 14 Apr 2025 21:12:42 GMT  
		Size: 8.8 MB (8769283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c32925dd7ff4edd4b024f007e24271d2fd3b83313ba286e2d73d0f5cb4203a75`  
		Last Modified: Mon, 14 Apr 2025 21:12:42 GMT  
		Size: 40.8 KB (40778 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:863067577e8c777cfcc5bb6256eb5115267ef63d7b8c3d0e9e9d880449d54d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.1 MB (619130642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06117d0d07666860c9eff1cb205339383246eb04c5b43d7205d419717e359e29`
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
ENV POSTGRES_JDBC_VERSION=42.7.4
# Mon, 14 Apr 2025 12:16:51 GMT
ENV POSTGRES_JDBC_SHA256=188976721ead8e8627eb6d8389d500dccc0c9bebd885268a3047180274a6031e
# Mon, 14 Apr 2025 12:16:51 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.4
# Mon, 14 Apr 2025 12:16:51 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.4.jar
# Mon, 14 Apr 2025 12:16:51 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.4.jar
# Mon, 14 Apr 2025 12:16:51 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:ce9f999fad10d916c85af816f699291f84c0c3c55936be154d9871b43064c8f6`  
		Last Modified: Mon, 14 Apr 2025 21:13:20 GMT  
		Size: 1.0 MB (1013640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357e72dab463531e581cb6de100aefc4aa62413cfe18f0c982e3dc3c88962fea`  
		Last Modified: Mon, 14 Apr 2025 21:13:20 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602a20d5ab4da1206b3ab20ab163692878d1e3ad9351072fb8fabf0baa027b66`  
		Last Modified: Mon, 14 Apr 2025 21:13:20 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b208d35c24940f402d000b5101c86726a0d4b0dc9219440aa1105d41e0d0ff4`  
		Last Modified: Mon, 14 Apr 2025 21:13:20 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18167d1c228bb9c9b642d0595fd05ae28d9112087719fb0b2fd19b8a04855a19`  
		Last Modified: Mon, 14 Apr 2025 21:13:21 GMT  
		Size: 2.4 KB (2419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:416a543f7df5d497c1a0f7d2cef7af649b142a315d5e919be3af066f81c2390c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8810987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e14772b0a6af58e5ac64bae80397f72aa9a49824ea0eb8ee11017c57505411`

```dockerfile
```

-	Layers:
	-	`sha256:73b7519c6e0e63e9ce6a0adb4a1cb3756548bfcbfc9e0c186994cb9ab1c24af4`  
		Last Modified: Mon, 14 Apr 2025 21:13:20 GMT  
		Size: 8.8 MB (8770036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c89a4fd78b13834fa9dbab50feabc4ef38c1b88f0fe49fdae0e7c46b006fcd7`  
		Last Modified: Mon, 14 Apr 2025 21:13:20 GMT  
		Size: 41.0 KB (40951 bytes)  
		MIME: application/vnd.in-toto+json
