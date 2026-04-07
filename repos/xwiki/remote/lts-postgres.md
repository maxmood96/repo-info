## `xwiki:lts-postgres`

```console
$ docker pull xwiki@sha256:77eb79cdab2c7b259cf04ce31aed34ee51ba89e83aad4d9a633e8d0b7579514c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:846b522d2de7f7c11770a44cbe57d9e5fb15d53191751f56bf03bbde0d36f128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 MB (637807280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8374c810c71e1ace5f37b54d79db8ebbdadafaef8702fbb5549a5cfda7b30a`
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
# Tue, 07 Apr 2026 05:04:24 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 07 Apr 2026 05:04:24 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 07 Apr 2026 05:04:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 07 Apr 2026 05:04:24 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 07 Apr 2026 05:04:24 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 07 Apr 2026 05:04:24 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 07 Apr 2026 05:04:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:04:24 GMT
ENV XWIKI_VERSION=17.10.5
# Tue, 07 Apr 2026 05:04:24 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.5
# Tue, 07 Apr 2026 05:04:24 GMT
ENV XWIKI_DOWNLOAD_SHA256=686d7d548e801b061add84e58be1f015a1949f0899cfb230435e0f3dbdf8aaa2
# Tue, 07 Apr 2026 05:04:44 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 07 Apr 2026 05:04:44 GMT
ENV POSTGRES_JDBC_VERSION=42.7.10
# Tue, 07 Apr 2026 05:04:44 GMT
ENV POSTGRES_JDBC_SHA256=cab1cd67cfa25c25de4348e532298028288a877ba01c77d1619fe45416193387
# Tue, 07 Apr 2026 05:04:44 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.10
# Tue, 07 Apr 2026 05:04:44 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.10.jar
# Tue, 07 Apr 2026 05:04:44 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.10.jar
# Tue, 07 Apr 2026 05:04:45 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 07 Apr 2026 05:04:45 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 07 Apr 2026 05:04:45 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 07 Apr 2026 05:04:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 07 Apr 2026 05:04:45 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:04:45 GMT
VOLUME [/usr/local/xwiki]
# Tue, 07 Apr 2026 05:04:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:04:45 GMT
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
	-	`sha256:e846a1dd6f01e245c0dead513cfa69aa1e7f12b5dd24c729d45808e26f2c485d`  
		Last Modified: Tue, 07 Apr 2026 05:05:25 GMT  
		Size: 191.2 MB (191192573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a186dcdc7c05864fbc6a198a3cb48592cea09d1b540dd25788c2d290f3e0d61`  
		Last Modified: Tue, 07 Apr 2026 05:05:28 GMT  
		Size: 331.3 MB (331304821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f042dfac7694c6c8c6ee567a20f9b08b723e3b68ec6520a28393355c9c6aae`  
		Last Modified: Tue, 07 Apr 2026 05:05:19 GMT  
		Size: 1.1 MB (1061590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccebfe0680fb9c4b7fa4efae61d168c6c016d86fd2e6879d46411c77a0b2d8b`  
		Last Modified: Tue, 07 Apr 2026 05:05:19 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cbc1a160c442c44b67df9eebc8fc10a8e59abe1d436e3e4196b5a67b1831f3`  
		Last Modified: Tue, 07 Apr 2026 05:05:20 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f991067003aa23be3edcd204a3a24b43cdfba57afe2c6c3d49c05e5b926290a1`  
		Last Modified: Tue, 07 Apr 2026 05:05:20 GMT  
		Size: 10.7 KB (10673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28c92ccaa5a6704e1864b2a6090481e56f6262bc1b478e2a20d9cbf530ecf57`  
		Last Modified: Tue, 07 Apr 2026 05:05:21 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:82cd0d7c10a83d8237e1742e741decf43c0d5772bf9a819cbf607b81d4b79adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9220197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd6af93d51d404f637ed4f204ccf5fe186353f7d8e5a8471e047ce6aa0758f2`

```dockerfile
```

-	Layers:
	-	`sha256:4c23339fae1eec41e9be8ae6bbba02adbadb4afdca409d29513a09f0286a86ba`  
		Last Modified: Tue, 07 Apr 2026 05:05:19 GMT  
		Size: 9.2 MB (9179764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd3f18d67ba598043d72efe00bad25569fdee8556504c1573350d925b78f3d9e`  
		Last Modified: Tue, 07 Apr 2026 05:05:18 GMT  
		Size: 40.4 KB (40433 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:e78056ba67ccb34d91ff57e792752e0b19b3e88d3dddf29090fbe2a0970cc9d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.8 MB (633792860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a02b2cdd79e085eb6d7bf99d920f5ce0eed033434e9a9c52407d9d42d907a05b`
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
# Tue, 07 Apr 2026 05:24:50 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 07 Apr 2026 05:24:50 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 07 Apr 2026 05:24:50 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 07 Apr 2026 05:24:50 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 07 Apr 2026 05:24:50 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 07 Apr 2026 05:24:50 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 07 Apr 2026 05:24:50 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 05:24:50 GMT
ENV XWIKI_VERSION=17.10.5
# Tue, 07 Apr 2026 05:24:50 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.5
# Tue, 07 Apr 2026 05:24:50 GMT
ENV XWIKI_DOWNLOAD_SHA256=686d7d548e801b061add84e58be1f015a1949f0899cfb230435e0f3dbdf8aaa2
# Tue, 07 Apr 2026 05:25:11 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 07 Apr 2026 05:25:11 GMT
ENV POSTGRES_JDBC_VERSION=42.7.10
# Tue, 07 Apr 2026 05:25:11 GMT
ENV POSTGRES_JDBC_SHA256=cab1cd67cfa25c25de4348e532298028288a877ba01c77d1619fe45416193387
# Tue, 07 Apr 2026 05:25:11 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.10
# Tue, 07 Apr 2026 05:25:11 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.10.jar
# Tue, 07 Apr 2026 05:25:11 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.10.jar
# Tue, 07 Apr 2026 05:25:11 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Tue, 07 Apr 2026 05:25:11 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 07 Apr 2026 05:25:12 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 07 Apr 2026 05:25:12 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 07 Apr 2026 05:25:12 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:25:12 GMT
VOLUME [/usr/local/xwiki]
# Tue, 07 Apr 2026 05:25:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 05:25:12 GMT
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
	-	`sha256:12364a0c32220f8099fab364e526fdeff585acee480f0edd7f55b194c43d69c0`  
		Last Modified: Tue, 07 Apr 2026 05:25:50 GMT  
		Size: 188.9 MB (188852231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f515e000ef29e423188ed470c2f08ab40b157fce8c95348d88bb56fffe87379`  
		Last Modified: Tue, 07 Apr 2026 05:25:53 GMT  
		Size: 331.3 MB (331304866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e65913f82c9a7f2f099db9739fb3888138753db1a8da28dfa0212b596cc779`  
		Last Modified: Tue, 07 Apr 2026 05:25:44 GMT  
		Size: 1.1 MB (1061584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2d37a4525a0bc8a6abef3cfb88573f4a6e908c97474a204888767368b3c1a`  
		Last Modified: Tue, 07 Apr 2026 05:25:44 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeac048f5eb25c41ffcae0cbb6f7d87f1eadf57c900c620ea6173219afdf25cf`  
		Last Modified: Tue, 07 Apr 2026 05:25:45 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187b846941e83f22ce0107e9e2968d3b587eedb7fc83637abdcd063cc880e8af`  
		Last Modified: Tue, 07 Apr 2026 05:25:45 GMT  
		Size: 10.7 KB (10673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901075d8c7c2fc2b7de1ba9c6b7058249f8be144a8792cf890e5210937adb140`  
		Last Modified: Tue, 07 Apr 2026 05:25:47 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:8d4b377c4d59e10ea61dab37524d4c2372f21cb2aff6d62980ff05a8b8665541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9221103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65433f3cd88fcaaccb9b51546285000c39ddbab11533a3d655b75924c00c0a7f`

```dockerfile
```

-	Layers:
	-	`sha256:4c0ade3a318e25a6292e5079077dadeb39b1cc06ee6af7a589c771f01ed09775`  
		Last Modified: Tue, 07 Apr 2026 05:25:44 GMT  
		Size: 9.2 MB (9180505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918d2f75eb873631c9eabe324ef0e0db27df52d26e0ca8e061354e9b09cd0e3b`  
		Last Modified: Tue, 07 Apr 2026 05:25:44 GMT  
		Size: 40.6 KB (40598 bytes)  
		MIME: application/vnd.in-toto+json
