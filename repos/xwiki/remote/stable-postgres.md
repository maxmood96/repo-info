## `xwiki:stable-postgres`

```console
$ docker pull xwiki@sha256:8cc2ed98594111c3fe6ba95060db061b6e7ef2fb72aa5d406fc3dde3fcc9081b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:6f12002663d449063d0def8b370874d61bfd46bca5b8aa1324f4dff950d208b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.1 MB (623121203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c3590eea126d02cf625fb1d3e37d8aad921cb33e8aa0b24a2220aba883673c`
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
	-	`sha256:d98f0e43fcb4ef180cb718e591f7ae1679898fb207d07247a451b701009e023d`  
		Last Modified: Thu, 17 Apr 2025 18:30:56 GMT  
		Size: 191.2 MB (191162547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e058bd449027364b420cf164d96dc36476a066d5a735787d4d40beff0c399bd`  
		Last Modified: Thu, 17 Apr 2025 18:30:58 GMT  
		Size: 317.3 MB (317313881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a2ac60ae71b746cedb398b6a8a39b588104468124720441a8a886018c061db`  
		Last Modified: Thu, 17 Apr 2025 18:30:50 GMT  
		Size: 1.0 MB (1013642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd30554c58166fef41cb4a67b78d5ad4e15e748aede494e93aa837fcf793d5b0`  
		Last Modified: Thu, 17 Apr 2025 18:30:50 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2761170ee5f5866dff9959b5cd87a635f29b2d97d75a7678bee908ff84fbf720`  
		Last Modified: Thu, 17 Apr 2025 18:30:51 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434db79cbc454d5ae1433b69f767c69ee286dee722ad9af65ebb496726342878`  
		Last Modified: Thu, 17 Apr 2025 18:30:51 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d13d88e7d735472782e8b067fde4d19003ad09f932ad701e215c73c22714f46`  
		Last Modified: Thu, 17 Apr 2025 18:30:52 GMT  
		Size: 2.4 KB (2421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:d166ca93e5e2f3482d509e073e36a7df93705209db946447406667fd613f5b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8810061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d3ab885dfb7516a0db24c8231e78269e041c88577c954e41a59b328718ffbb`

```dockerfile
```

-	Layers:
	-	`sha256:8355ac0a16ee52df8c3cca74506fc13dbb3158f09fdbb906ffe638028e2a7f2d`  
		Last Modified: Thu, 17 Apr 2025 18:30:51 GMT  
		Size: 8.8 MB (8769283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00b3501775fa8be28d807bdde00e222cfbcd43f981e3ff5ac2cd06385a92c5b9`  
		Last Modified: Thu, 17 Apr 2025 18:30:50 GMT  
		Size: 40.8 KB (40778 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:ae61de215b680a0394bbf5fe0c250c0c4b7d66cf8f1100fc8263e8aa49e143cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.1 MB (619129282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bb8f96a8b15b8ec69e5a78cfed746edf4053dbf5dde5d0ef03478f53e60447`
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
	-	`sha256:dec7067cf6f3c60f3afc141297392b7ae4f72490f953dc6e97e87a60cae90865`  
		Last Modified: Thu, 17 Apr 2025 18:55:40 GMT  
		Size: 317.3 MB (317313885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fd2e912c35ca23e466ff0720fb09ed4d39d8a2c8f8385deaca8f39015f9fce`  
		Last Modified: Thu, 17 Apr 2025 18:56:10 GMT  
		Size: 1.0 MB (1013640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa92250a4d775860c33865bb63e31891c28bac7bde2fddbf7fb4da000cd9fac5`  
		Last Modified: Thu, 17 Apr 2025 18:56:09 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b482d1b45b4671ec6dc64cf33cc8e854a25e85da87e18c40064159631266b1`  
		Last Modified: Thu, 17 Apr 2025 18:56:09 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f96b1a834387b457bb2354f821fad40ed9d0e6cc1eccf9b8e2514b607658e6f`  
		Last Modified: Thu, 17 Apr 2025 18:56:10 GMT  
		Size: 6.6 KB (6604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccbcf3714b61514c32b2d1676c6b172159c0318bc5811298ed2ba3369e0df4e`  
		Last Modified: Thu, 17 Apr 2025 18:56:10 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:7c4a37d8ee53636e455a1fe7c27117a3a05fcde7709c3560db3fe34eff0fc401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8810987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927c274858bb4106f2a3f6efb937b1f8e8ed7f13805d8451030f390e7df03b74`

```dockerfile
```

-	Layers:
	-	`sha256:b4c55ba09a965b19d59d0f060a6262446b949c80aaf0adb27000d1c99047f845`  
		Last Modified: Thu, 17 Apr 2025 18:56:10 GMT  
		Size: 8.8 MB (8770036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61294dc1fbad38c063fad90b912392226d46e19e8e6b495985f88c2e0ff64f54`  
		Last Modified: Thu, 17 Apr 2025 18:56:09 GMT  
		Size: 41.0 KB (40951 bytes)  
		MIME: application/vnd.in-toto+json
