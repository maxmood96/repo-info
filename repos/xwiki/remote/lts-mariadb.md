## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:d4061ec4131610da7166edd7ae8a55ded50bfd9324184710c5cdf258ab0a8240
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:295a24be0b25a21046656f2c1b4ea8c68d66eb823304a175bd4e1ca3da3c2b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.5 MB (637454162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9f16236af15ca54c69447edf31cddce326a3a188b44653b1f2672405369a1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:51:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:51:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:51:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:51:36 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:51:36 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 07 Apr 2026 01:52:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 01:52:07 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:52:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:52:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:30:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Apr 2026 03:30:05 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:30:05 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Apr 2026 03:30:05 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Apr 2026 03:30:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 03:30:05 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 03:30:05 GMT
ENV TOMCAT_MAJOR=10
# Tue, 07 Apr 2026 03:30:05 GMT
ENV TOMCAT_VERSION=10.1.54
# Tue, 07 Apr 2026 03:30:05 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Tue, 07 Apr 2026 03:30:30 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Apr 2026 03:30:37 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:30:37 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Apr 2026 03:30:37 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Apr 2026 03:30:37 GMT
ENTRYPOINT []
# Tue, 07 Apr 2026 03:30:37 GMT
CMD ["catalina.sh" "run"]
# Tue, 07 Apr 2026 05:04:30 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 07 Apr 2026 05:04:30 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 07 Apr 2026 05:04:30 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 07 Apr 2026 05:04:30 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 07 Apr 2026 05:04:30 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 07 Apr 2026 05:04:30 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 07 Apr 2026 05:04:30 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:04:30 GMT
ENV XWIKI_VERSION=17.10.5
# Tue, 07 Apr 2026 05:04:30 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.5
# Tue, 07 Apr 2026 05:04:30 GMT
ENV XWIKI_DOWNLOAD_SHA256=686d7d548e801b061add84e58be1f015a1949f0899cfb230435e0f3dbdf8aaa2
# Tue, 07 Apr 2026 05:04:51 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 07 Apr 2026 05:04:51 GMT
ENV MARIADB_JDBC_VERSION=3.5.7
# Tue, 07 Apr 2026 05:04:51 GMT
ENV MARIADB_JDBC_SHA256=07bb1229dc184f3313a5aef4c5a6b3207c8dbaa09db4a26814c936f004b4c526
# Tue, 07 Apr 2026 05:04:51 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.7
# Tue, 07 Apr 2026 05:04:51 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.7.jar
# Tue, 07 Apr 2026 05:04:51 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.7.jar
# Tue, 07 Apr 2026 05:04:51 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 07 Apr 2026 05:04:51 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 07 Apr 2026 05:04:51 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 07 Apr 2026 05:04:52 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 07 Apr 2026 05:04:52 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:04:52 GMT
VOLUME [/usr/local/xwiki]
# Tue, 07 Apr 2026 05:04:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:04:52 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b68b8ef47fdb988fb4023edbb2a8d6a19ba659a4921fc9f25c496fe28ae1ef1`  
		Last Modified: Tue, 07 Apr 2026 01:51:50 GMT  
		Size: 17.0 MB (16983568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c9370ed7c35a22ef566a4d1ee7eb152dc6f37abe64e4fc7df70647fa0499dc`  
		Last Modified: Tue, 07 Apr 2026 01:52:20 GMT  
		Size: 53.0 MB (52985505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ef302449c04c900de9660d789c58e12374e181f0204d02016bf10d05a2ea02`  
		Last Modified: Tue, 07 Apr 2026 01:52:19 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9425bf26e9ee5e1bdec0dd158e59f754d3f4b3866a00a320bf3dafdf1a133d42`  
		Last Modified: Tue, 07 Apr 2026 01:52:19 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c9795ba8e7d43886e47c9f28f417b2ad6594c5ba4081bd0f3079a1a17c92b3`  
		Last Modified: Tue, 07 Apr 2026 03:30:23 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415216d03967c36779ab9218ed04e2d48721c138ee3007af7305157c05d21243`  
		Last Modified: Tue, 07 Apr 2026 03:30:45 GMT  
		Size: 14.3 MB (14301303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298a021259cbe800fc2783c266cf2edbfe485bf898fa08ccf32f52653362586a`  
		Last Modified: Tue, 07 Apr 2026 03:30:45 GMT  
		Size: 224.9 KB (224915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c3c9b3fbcf0cb6b89140cc9472102844dca1017ca97298dd47c11d292e3bf9`  
		Last Modified: Tue, 07 Apr 2026 05:05:34 GMT  
		Size: 191.2 MB (191192609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fc8879c15f4ee794c17913aa8ea937ea4f232497b2ee9690c02eba7efbd80c`  
		Last Modified: Tue, 07 Apr 2026 05:05:37 GMT  
		Size: 331.3 MB (331304800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2a665c9f69c863980036c8ab0a949b5ad39b1633702bc6b123bfa84e6e06c6`  
		Last Modified: Tue, 07 Apr 2026 05:05:26 GMT  
		Size: 708.5 KB (708547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1df8104a6811eaa69cae5ce98ee96f7fcb6affca05fc06f3586595aa1611143`  
		Last Modified: Tue, 07 Apr 2026 05:05:26 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687ac257f3ec849a8783b36e076d973f604c864240d6e16394aef79c471e720f`  
		Last Modified: Tue, 07 Apr 2026 05:05:28 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a755ef7c4d3b8ff2b86d4675bc181dcfeeb98574e1c4b8d20829861496a22ef`  
		Last Modified: Tue, 07 Apr 2026 05:05:28 GMT  
		Size: 10.7 KB (10672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca666bdfe917f640a5a9902e83c60acbb996f26dd1a5ed8833fea57e71b86f2c`  
		Last Modified: Tue, 07 Apr 2026 05:05:29 GMT  
		Size: 2.5 KB (2495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:e142bb9e7cb55a9f1de411db876d802bb81fb9fd4683a115c2bcea47cf7faffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9220196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b0c1163de3719f058c6040e6f1c15aa92532928a08f3411ce0ae96af61dfba`

```dockerfile
```

-	Layers:
	-	`sha256:38225648cc744f3e54ca3d09284e7d93f507d2e3402c6de3cab5f39874c781b8`  
		Last Modified: Tue, 07 Apr 2026 05:05:27 GMT  
		Size: 9.2 MB (9179746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bda82d7cf076f4310fe64d731ae658d463c7d22cb90d840684f8b50cf9153ce3`  
		Last Modified: Tue, 07 Apr 2026 05:05:26 GMT  
		Size: 40.5 KB (40450 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:555c0d46eef2458c48b4e5e7c27a0c7626962aab19dba10defe12d93a9090867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.4 MB (633439732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423e09f483d32909d5d16ea290bc87405773555438776441bd6cd04e72ef1a91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:54:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:54:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:54:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:54:52 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:54:52 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 07 Apr 2026 01:55:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 01:55:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:55:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:55:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 05:10:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 07 Apr 2026 05:10:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:10:00 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 07 Apr 2026 05:10:00 GMT
WORKDIR /usr/local/tomcat
# Tue, 07 Apr 2026 05:10:00 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 05:10:00 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 07 Apr 2026 05:10:00 GMT
ENV TOMCAT_MAJOR=10
# Tue, 07 Apr 2026 05:10:00 GMT
ENV TOMCAT_VERSION=10.1.54
# Tue, 07 Apr 2026 05:10:00 GMT
ENV TOMCAT_SHA512=8694b94324cf6f62ab032fa2438d7334518dcfcbf7878361b147246c46eb1e558c327f32c05fb4b7705c01fcca92fde392ce320934410f1169ff4ab36a1c7139
# Tue, 07 Apr 2026 05:10:01 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 07 Apr 2026 05:10:08 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:10:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 07 Apr 2026 05:10:09 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 07 Apr 2026 05:10:09 GMT
ENTRYPOINT []
# Tue, 07 Apr 2026 05:10:09 GMT
CMD ["catalina.sh" "run"]
# Tue, 07 Apr 2026 05:24:52 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 07 Apr 2026 05:24:52 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 07 Apr 2026 05:24:52 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 07 Apr 2026 05:24:52 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 07 Apr 2026 05:24:52 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 07 Apr 2026 05:24:52 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 07 Apr 2026 05:24:52 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:24:52 GMT
ENV XWIKI_VERSION=17.10.5
# Tue, 07 Apr 2026 05:24:52 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.5
# Tue, 07 Apr 2026 05:24:52 GMT
ENV XWIKI_DOWNLOAD_SHA256=686d7d548e801b061add84e58be1f015a1949f0899cfb230435e0f3dbdf8aaa2
# Tue, 07 Apr 2026 05:25:13 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 07 Apr 2026 05:25:13 GMT
ENV MARIADB_JDBC_VERSION=3.5.7
# Tue, 07 Apr 2026 05:25:13 GMT
ENV MARIADB_JDBC_SHA256=07bb1229dc184f3313a5aef4c5a6b3207c8dbaa09db4a26814c936f004b4c526
# Tue, 07 Apr 2026 05:25:13 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.7
# Tue, 07 Apr 2026 05:25:13 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.7.jar
# Tue, 07 Apr 2026 05:25:13 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.7.jar
# Tue, 07 Apr 2026 05:25:13 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 07 Apr 2026 05:25:13 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 07 Apr 2026 05:25:14 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 07 Apr 2026 05:25:14 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 07 Apr 2026 05:25:14 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:25:14 GMT
VOLUME [/usr/local/xwiki]
# Tue, 07 Apr 2026 05:25:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:25:14 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc1fe49c2f79e04d9e562ce4ee017e874bf7e23feea81b6df6f351ab993d9b5`  
		Last Modified: Tue, 07 Apr 2026 01:55:07 GMT  
		Size: 17.0 MB (16996238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538e758f95d8493adbf608ecfa760b05bb49d3ceee0f1e637ca69598f3434ea6`  
		Last Modified: Tue, 07 Apr 2026 01:55:40 GMT  
		Size: 52.2 MB (52155642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e0252f321812c22ad7139fe93995a4ab816f331d23ab15579dedbc1027f1ca`  
		Last Modified: Tue, 07 Apr 2026 01:55:39 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f199c35f5162fea3c8f07eef1e388cab02e2e3f619c9b2842b8bcd77a768e1e`  
		Last Modified: Tue, 07 Apr 2026 01:55:39 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac5f94c5bcca79f12bddc6c46eb7fa6c04e4e0e9ed03895d1a50ef57c72bb4b`  
		Last Modified: Tue, 07 Apr 2026 05:10:17 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908a696e504aba798cd3c2d7427bb96e96f3b09202e8c8142034cb000c030d62`  
		Last Modified: Tue, 07 Apr 2026 05:10:18 GMT  
		Size: 14.3 MB (14303384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f112508064b8beb36c4dfc19b3697a983e5ded489ff63aef3a3905f0f61481`  
		Last Modified: Tue, 07 Apr 2026 05:10:18 GMT  
		Size: 225.3 KB (225282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b01a1dc77228b6664268456a5c8dbffc9700ed4c0ea8d53ce887988bc6d686`  
		Last Modified: Tue, 07 Apr 2026 05:25:52 GMT  
		Size: 188.9 MB (188852287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389eb21d230ccb78f476f87762f4ed4a3ff79c67222c1647e8edc3e71c48374a`  
		Last Modified: Tue, 07 Apr 2026 05:25:54 GMT  
		Size: 331.3 MB (331304822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb81fa017d63eca5dcd5f7c8691c45a55a82946404a1916fad40ec374d6c6bd3`  
		Last Modified: Tue, 07 Apr 2026 05:25:46 GMT  
		Size: 708.5 KB (708545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d572af8d5d187d1820453734de60b110cf21cc1dfb43cc847ca44cc4fa8c57`  
		Last Modified: Tue, 07 Apr 2026 05:25:46 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a85d055fb3b170825e12ed524c8edc05fbc242441e2e8f090f1d37b47afe579`  
		Last Modified: Tue, 07 Apr 2026 05:25:47 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5db7f6655809518d454742c4161fa048cd7c4b5a3e7ae26980260a50185b9ac`  
		Last Modified: Tue, 07 Apr 2026 05:25:47 GMT  
		Size: 10.7 KB (10674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebf450de3b2ab07ac0189c05f68d5de22d260c71640972f14b2b21cccef12cb`  
		Last Modified: Tue, 07 Apr 2026 05:25:48 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:024b53528bf3184360de91b52d8b85b00069fbbe4b40177d0df58fa4b89e0ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9221098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e86063932e083d13be0c5ef27d1da422004cd10fde29592d4cf4cd7dfb61a43`

```dockerfile
```

-	Layers:
	-	`sha256:ec51a81b19417bcc4606fbcabc8af92d9c423af56361e03b8b82ac035616cbe0`  
		Last Modified: Tue, 07 Apr 2026 05:25:46 GMT  
		Size: 9.2 MB (9180487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:946635b6578e7159f3cde14c57a2d5bd41f8175db55a1c5827e63688aab7b503`  
		Last Modified: Tue, 07 Apr 2026 05:25:46 GMT  
		Size: 40.6 KB (40611 bytes)  
		MIME: application/vnd.in-toto+json
