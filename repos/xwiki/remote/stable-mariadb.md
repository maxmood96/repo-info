## `xwiki:stable-mariadb`

```console
$ docker pull xwiki@sha256:2f7b46832fb0394ef3bb070dd1bab2bbb74c9703f1f16b1716bd38ddac018968
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:7f845529dd6e239b218af996c32c1aaae5b6b345041152bc8bec65ea2ab1f16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.4 MB (644392484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99600bae0d5e480f09cd9c7a529becf297efab3062c4511d52fb51fa1a13d938`
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
# Thu, 09 Apr 2026 22:23:14 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 09 Apr 2026 22:23:14 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 09 Apr 2026 22:23:14 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 09 Apr 2026 22:23:14 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 09 Apr 2026 22:23:14 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 09 Apr 2026 22:23:14 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 09 Apr 2026 22:23:14 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:23:14 GMT
ENV XWIKI_VERSION=18.2.1
# Thu, 09 Apr 2026 22:23:14 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.2.1
# Thu, 09 Apr 2026 22:23:14 GMT
ENV XWIKI_DOWNLOAD_SHA256=d18d8d16f39d6a37ba11c0015dbafced57183a9bdbdf35ed1103191e24dac7b2
# Thu, 09 Apr 2026 22:23:35 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 09 Apr 2026 22:23:35 GMT
ENV MARIADB_JDBC_VERSION=3.5.7
# Thu, 09 Apr 2026 22:23:35 GMT
ENV MARIADB_JDBC_SHA256=07bb1229dc184f3313a5aef4c5a6b3207c8dbaa09db4a26814c936f004b4c526
# Thu, 09 Apr 2026 22:23:35 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.7
# Thu, 09 Apr 2026 22:23:35 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.7.jar
# Thu, 09 Apr 2026 22:23:35 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.7.jar
# Thu, 09 Apr 2026 22:23:35 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 09 Apr 2026 22:23:35 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 09 Apr 2026 22:23:36 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 09 Apr 2026 22:23:36 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 09 Apr 2026 22:23:36 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 09 Apr 2026 22:23:36 GMT
VOLUME [/usr/local/xwiki]
# Thu, 09 Apr 2026 22:23:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2026 22:23:36 GMT
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
	-	`sha256:2ac27493d4202eec4afe454eb31c0b2a8b0f7b4be2cfa9ef14e93dbc4cc95a44`  
		Last Modified: Thu, 09 Apr 2026 22:24:18 GMT  
		Size: 191.2 MB (191192385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f016d26d1b4337444504499b396c1229ab4be94bfb917e2ef5f8eb5df2f0467d`  
		Last Modified: Thu, 09 Apr 2026 22:24:21 GMT  
		Size: 338.2 MB (338243065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f924396aaf060ebd2222b21b2fc2b60e7c6baa7c3c0940a23caf5aff224c88c`  
		Last Modified: Thu, 09 Apr 2026 22:24:12 GMT  
		Size: 708.5 KB (708546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994f4e25fb3ea19f23ad2a8d56c7a8af1f6eec0bd342a6804bcc74353db582f2`  
		Last Modified: Thu, 09 Apr 2026 22:24:12 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3704314d67659afee8af05ebcd29916a9c38bfe6b49df3e5043b1b86483f53c9`  
		Last Modified: Thu, 09 Apr 2026 22:24:13 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995e6e40781dc9ad85886c45e18c8c8484eaa0ac9c9309eb1e3a4f94c5fb647c`  
		Last Modified: Thu, 09 Apr 2026 22:24:14 GMT  
		Size: 11.0 KB (10951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11aca9dcc74cbfea7c8785ba33ad988bb849f5fc14c7f8252fe74a29ba5d054f`  
		Last Modified: Thu, 09 Apr 2026 22:24:15 GMT  
		Size: 2.5 KB (2496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:56edc12b6e37bc72fbd2acfdd6646f4ceda9abc7cb6423f72e70dd5e33267a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9233518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f441cb06f536403dcc6b3429e61b9aafb8e0e4f877c8ba599346df21f7a4948`

```dockerfile
```

-	Layers:
	-	`sha256:5c00d65fb1481e6e70d7c99f21360114a0ea923fbd6f85f287a634837873de35`  
		Last Modified: Thu, 09 Apr 2026 22:24:12 GMT  
		Size: 9.2 MB (9192755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cb31448128770abf74c5b34fafb352ed380d9a2aa6041cac186f85ad71c8eb5`  
		Last Modified: Thu, 09 Apr 2026 22:24:12 GMT  
		Size: 40.8 KB (40763 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:b13b45722cecf651d8e233bac6edf7016acd4f108e9b8cfb7dc9fc0cfaed6b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **640.4 MB (640378092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6f16e6f8fdd44c1779a62bd994a2297693da5de1176ccae5e7dce1f6076706`
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
# Thu, 09 Apr 2026 22:24:47 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 09 Apr 2026 22:24:47 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 09 Apr 2026 22:24:47 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 09 Apr 2026 22:24:47 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 09 Apr 2026 22:24:47 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 09 Apr 2026 22:24:47 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 09 Apr 2026 22:24:47 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Apr 2026 22:24:47 GMT
ENV XWIKI_VERSION=18.2.1
# Thu, 09 Apr 2026 22:24:47 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.2.1
# Thu, 09 Apr 2026 22:24:47 GMT
ENV XWIKI_DOWNLOAD_SHA256=d18d8d16f39d6a37ba11c0015dbafced57183a9bdbdf35ed1103191e24dac7b2
# Thu, 09 Apr 2026 22:25:10 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 09 Apr 2026 22:25:10 GMT
ENV MARIADB_JDBC_VERSION=3.5.7
# Thu, 09 Apr 2026 22:25:10 GMT
ENV MARIADB_JDBC_SHA256=07bb1229dc184f3313a5aef4c5a6b3207c8dbaa09db4a26814c936f004b4c526
# Thu, 09 Apr 2026 22:25:10 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.7
# Thu, 09 Apr 2026 22:25:10 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.7.jar
# Thu, 09 Apr 2026 22:25:10 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.7.jar
# Thu, 09 Apr 2026 22:25:10 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 09 Apr 2026 22:25:10 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 09 Apr 2026 22:25:10 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 09 Apr 2026 22:25:10 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 09 Apr 2026 22:25:10 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 09 Apr 2026 22:25:10 GMT
VOLUME [/usr/local/xwiki]
# Thu, 09 Apr 2026 22:25:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2026 22:25:10 GMT
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
	-	`sha256:7138705fc18cbf1f01ce7fa0c86bf7b78199e805cd67f83b34341bed6665e884`  
		Last Modified: Thu, 09 Apr 2026 22:25:50 GMT  
		Size: 188.9 MB (188852257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93dfb9c13c1a63a280a43be79ea97cec3bf1fd65c1a3262cbe4217ac0631671`  
		Last Modified: Thu, 09 Apr 2026 22:25:53 GMT  
		Size: 338.2 MB (338242922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b0ca8ba7114b163b8212d7713b455592e46e72dcc53fc57b668f2c0026af43`  
		Last Modified: Thu, 09 Apr 2026 22:25:44 GMT  
		Size: 708.5 KB (708547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c687fcdd47be17835a04f568f977d2d5d9d4f4b9cb2e06abddbd7fb70c441a5c`  
		Last Modified: Thu, 09 Apr 2026 22:25:43 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431f576ce0199d963e945de2258990132b1bdbe4c80f625dc2da12fc9510b550`  
		Last Modified: Thu, 09 Apr 2026 22:25:45 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18a97f27a0055c2e0c043f8125c5dcb20e9ffbecd6321951d49acdb2fbba196`  
		Last Modified: Thu, 09 Apr 2026 22:25:45 GMT  
		Size: 11.0 KB (10957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed36abd95650841f9c5f59e37c081cdf5d2f51dc6f865902ead59c496bf6cd4`  
		Last Modified: Thu, 09 Apr 2026 22:25:46 GMT  
		Size: 2.5 KB (2498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:8338e29aebd4aaab075bccf3331edba1464b418a0e7452763583a4194eed5d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d76975db5fdb2fd17c82b040962f2272aeb1346178ef759b04b7974f841883`

```dockerfile
```

-	Layers:
	-	`sha256:468adf1134aa3cc689ac4c31c05cd10c9867661f4f59da4d5656d69bb3e05bfb`  
		Last Modified: Thu, 09 Apr 2026 22:25:44 GMT  
		Size: 9.2 MB (9193508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c53c355bf660b3feaeeae74ebc4ec1ff70f14c0a261682e31d054b43392a441`  
		Last Modified: Thu, 09 Apr 2026 22:25:43 GMT  
		Size: 40.9 KB (40937 bytes)  
		MIME: application/vnd.in-toto+json
