## `xwiki:stable-postgres`

```console
$ docker pull xwiki@sha256:d439c7ffd0753b62ef19e76ba6ec8cbd6a4b40d35df38c4dc15a6456740a704c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:0987a57cc0f089dbcac6a30a321f1ca9f96997a9254ee4a5a08bab94d505023d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.9 MB (647874584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6fc20e351483e322e98089aef04ef8a414a42c9220a01639c673b734f3e7ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:20:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:20:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:20:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:20:23 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:20:23 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Feb 2026 20:20:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:20:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:20:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:20:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:55:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 21:55:43 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:55:43 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 21:55:43 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 21:55:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:55:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:55:43 GMT
ENV TOMCAT_MAJOR=10
# Tue, 17 Feb 2026 21:55:43 GMT
ENV TOMCAT_VERSION=10.1.52
# Tue, 17 Feb 2026 21:55:43 GMT
ENV TOMCAT_SHA512=241183fe5dec15936205ec495b65e04218117affc10e90c5fbc56bce0b4f031ee944d468c128f0ae484fd1d5bd9bec22b65a95a8cfd94cb7fc1f12c7ef434d99
# Tue, 17 Feb 2026 21:56:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 21:56:30 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:56:31 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 21:56:31 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 21:56:31 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 21:56:31 GMT
CMD ["catalina.sh" "run"]
# Mon, 23 Feb 2026 21:34:16 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 23 Feb 2026 21:34:16 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 23 Feb 2026 21:34:16 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 23 Feb 2026 21:34:16 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 23 Feb 2026 21:34:16 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 23 Feb 2026 21:34:16 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 23 Feb 2026 21:34:16 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 21:34:16 GMT
ENV XWIKI_VERSION=18.1.0
# Mon, 23 Feb 2026 21:34:16 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.1.0
# Mon, 23 Feb 2026 21:34:16 GMT
ENV XWIKI_DOWNLOAD_SHA256=0f7d70d190ebf20483b3afd79b006050bbe4618ca1dab02bc74e1c3202bd63c0
# Mon, 23 Feb 2026 21:34:38 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 23 Feb 2026 21:34:38 GMT
ENV POSTGRES_JDBC_VERSION=42.7.9
# Mon, 23 Feb 2026 21:34:38 GMT
ENV POSTGRES_JDBC_SHA256=88f1fc3992e80ec3b048f798030e9a014aa4783c40afb56d3e7a87ee0adf166f
# Mon, 23 Feb 2026 21:34:38 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.9
# Mon, 23 Feb 2026 21:34:38 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.9.jar
# Mon, 23 Feb 2026 21:34:38 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.9.jar
# Mon, 23 Feb 2026 21:34:38 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 23 Feb 2026 21:34:38 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 23 Feb 2026 21:34:38 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 23 Feb 2026 21:34:38 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 23 Feb 2026 21:34:38 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 23 Feb 2026 21:34:38 GMT
VOLUME [/usr/local/xwiki]
# Mon, 23 Feb 2026 21:34:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Feb 2026 21:34:38 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51024d09d55a0dd2db21ee0f8a82228dad25451936f15c7e5cb068e070498470`  
		Last Modified: Tue, 17 Feb 2026 20:20:39 GMT  
		Size: 17.0 MB (16980576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4247047ab404fa4e57d2dd23d30a1976f874414ce7c7fc6d40f81316270c411`  
		Last Modified: Tue, 17 Feb 2026 20:20:40 GMT  
		Size: 53.0 MB (52985486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23efddf26cd7c89f1e3c4284aaff43578b788402aad535c0d7582d61993ae0c`  
		Last Modified: Tue, 17 Feb 2026 20:20:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ec7c6edf1e7d89c9950ef904e2f16a2b5bb4e43375a62b8ebb6231dfa4eb96`  
		Last Modified: Tue, 17 Feb 2026 20:20:39 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477a6ec40f87af23842d29f2bca43453af69fdf3a3e04131c23ec2d5f927a005`  
		Last Modified: Tue, 17 Feb 2026 21:56:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4dec3e7a3bbe3578273238c2f2440ebeb1e6d0b9a286bf8e83771737a34726`  
		Last Modified: Tue, 17 Feb 2026 21:56:39 GMT  
		Size: 14.3 MB (14284416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fcdfacb5e2b63ec13fe71e47dc5ce6d8010918a5e57cc81eb46607219b4512`  
		Last Modified: Tue, 17 Feb 2026 21:56:39 GMT  
		Size: 224.8 KB (224756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed47512fbb0fc28a91b1631cd48c3556b540dea8fa77471a7b03afcb4e4cc6f`  
		Last Modified: Mon, 23 Feb 2026 21:35:20 GMT  
		Size: 192.3 MB (192309627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac7061facbf0ba0b226dfbe85c4e6110037c05abc03015cad4a928e80fe925e`  
		Last Modified: Mon, 23 Feb 2026 21:35:23 GMT  
		Size: 340.3 MB (340287322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd079ddfebdfefaf2a09e471f1ab6e3705efa9ff1adc9814407ca87315f0cd5`  
		Last Modified: Mon, 23 Feb 2026 21:35:11 GMT  
		Size: 1.1 MB (1055026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995777969ba2304e8a4602b313d54f2d54dda09a3f4bf925b507cb88f0ad37c0`  
		Last Modified: Mon, 23 Feb 2026 21:35:11 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c236ede356a39390a2a905e0b651622d03ddea4df45a21b3aee57e806c75a26`  
		Last Modified: Mon, 23 Feb 2026 21:35:13 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8385d0bc7206a8f10623893cf86fa3bb70bc95840b8bfaf228270e9ca8760cd`  
		Last Modified: Mon, 23 Feb 2026 21:35:13 GMT  
		Size: 10.9 KB (10903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea505b991908ef3a67a20bdd6ef872725de195de452359aaca50cf12e4916976`  
		Last Modified: Mon, 23 Feb 2026 21:35:14 GMT  
		Size: 2.4 KB (2414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:5be0d58b7736d03f39e55cada56d03ca35041010897b97b9aca1645200fae365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9230531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb0453b6734020020dd53d22902e60f5b23f6b676c4a20643ae397b7afed4ea`

```dockerfile
```

-	Layers:
	-	`sha256:6c8e7cef2818decbf66c17ed0f6fcaf2bc04caccc31c8541eac8bd7ade540a65`  
		Last Modified: Mon, 23 Feb 2026 21:35:11 GMT  
		Size: 9.2 MB (9189791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d6f8878e1f0e4cff06fe73903a111ec8a60bbf8c7060a2764a75e747acb4c0`  
		Last Modified: Mon, 23 Feb 2026 21:35:11 GMT  
		Size: 40.7 KB (40740 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:4ad7e536a87696ebf084120c67e5ff5bc990e17d08e5514cab6c9a55c2ba803c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.8 MB (643809605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877d64ccd3bd07a040e85f9f5b9080a4f974a7387a422038ac66f42e309633b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:18:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 20:18:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:18:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:18:48 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:18:48 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 17 Feb 2026 20:19:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='991be6ac6725e76109ecbd131d658f992dcbeacba3a8b4b6650302c8012b52fb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        arm64)          ESUM='3ca84da7c4f57eee8d7e7f0645dc904a3a06456d32b37a4dd57a5e7527245250';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64el)          ESUM='1a49cffcb348a28c017cf0deeb9322b7296dbfb002a8e43bd7f65ad671e10eb7';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        riscv64)          ESUM='02cf763836c14bad4d689eb3b4efd691657de753dba07193cd1fb8691c8fe7b8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='48f8529714c90c6cc61aa729cf8952f2fc47f2f2890551ba7f9e1c061b04be13';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Feb 2026 20:19:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Feb 2026 20:19:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:19:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Feb 2026 21:56:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 17 Feb 2026 21:56:31 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:56:31 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 17 Feb 2026 21:56:31 GMT
WORKDIR /usr/local/tomcat
# Tue, 17 Feb 2026 21:56:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:56:31 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 17 Feb 2026 21:56:31 GMT
ENV TOMCAT_MAJOR=10
# Tue, 17 Feb 2026 21:56:31 GMT
ENV TOMCAT_VERSION=10.1.52
# Tue, 17 Feb 2026 21:56:31 GMT
ENV TOMCAT_SHA512=241183fe5dec15936205ec495b65e04218117affc10e90c5fbc56bce0b4f031ee944d468c128f0ae484fd1d5bd9bec22b65a95a8cfd94cb7fc1f12c7ef434d99
# Tue, 17 Feb 2026 21:56:32 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 17 Feb 2026 21:56:39 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:56:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 17 Feb 2026 21:56:39 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 17 Feb 2026 21:56:39 GMT
ENTRYPOINT []
# Tue, 17 Feb 2026 21:56:39 GMT
CMD ["catalina.sh" "run"]
# Mon, 23 Feb 2026 21:34:04 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 23 Feb 2026 21:34:04 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 23 Feb 2026 21:34:04 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 23 Feb 2026 21:34:04 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 23 Feb 2026 21:34:04 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 23 Feb 2026 21:34:04 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 23 Feb 2026 21:34:04 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 21:34:04 GMT
ENV XWIKI_VERSION=18.1.0
# Mon, 23 Feb 2026 21:34:04 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.1.0
# Mon, 23 Feb 2026 21:34:04 GMT
ENV XWIKI_DOWNLOAD_SHA256=0f7d70d190ebf20483b3afd79b006050bbe4618ca1dab02bc74e1c3202bd63c0
# Mon, 23 Feb 2026 21:34:27 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 23 Feb 2026 21:34:27 GMT
ENV POSTGRES_JDBC_VERSION=42.7.9
# Mon, 23 Feb 2026 21:34:27 GMT
ENV POSTGRES_JDBC_SHA256=88f1fc3992e80ec3b048f798030e9a014aa4783c40afb56d3e7a87ee0adf166f
# Mon, 23 Feb 2026 21:34:27 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.9
# Mon, 23 Feb 2026 21:34:27 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.9.jar
# Mon, 23 Feb 2026 21:34:27 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.9.jar
# Mon, 23 Feb 2026 21:34:27 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 23 Feb 2026 21:34:27 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 23 Feb 2026 21:34:27 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 23 Feb 2026 21:34:27 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 23 Feb 2026 21:34:27 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 23 Feb 2026 21:34:27 GMT
VOLUME [/usr/local/xwiki]
# Mon, 23 Feb 2026 21:34:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Feb 2026 21:34:27 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9a0a02907fdd6dd960abed9cafcbf879106f66849dda4f7a233bccb4434ec8`  
		Last Modified: Tue, 17 Feb 2026 20:19:14 GMT  
		Size: 17.0 MB (16994433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49ce0a2c26f9793abda89ce481106d5c6459e59db6ae2021f4155548525089d`  
		Last Modified: Tue, 17 Feb 2026 20:19:40 GMT  
		Size: 52.2 MB (52155649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19874336137573e037a93514b5a832458da45456d5638a41ab1eacfbd793fd4`  
		Last Modified: Tue, 17 Feb 2026 20:19:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427ef353aae734ae9d1def619d9120bd7093b573a0c56fc2db6fabefa3313b8c`  
		Last Modified: Tue, 17 Feb 2026 20:19:39 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52ed4bcf62ca9f4672435f7b72ed8d2eae9bfb78de8c6198c4e403f5e1e8970`  
		Last Modified: Tue, 17 Feb 2026 21:56:48 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7655edb001eb586396ea1033971e28b9a0fa6c36503a055b924745837b8827f9`  
		Last Modified: Tue, 17 Feb 2026 21:56:49 GMT  
		Size: 14.3 MB (14288050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68708eb889667beddc5b8db265b052f3b060c0bc69fdfac27ab091c4d71f7067`  
		Last Modified: Tue, 17 Feb 2026 21:56:48 GMT  
		Size: 225.2 KB (225239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd75970882e9b5dcbf57f913926d156d3c351af6f25cd34a15197c98ddc404a`  
		Last Modified: Mon, 23 Feb 2026 21:35:07 GMT  
		Size: 189.9 MB (189918954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e6abd0e151612cd700deacf38d7ec3ac5c2f44684218b3a8eb877d4e26574c`  
		Last Modified: Mon, 23 Feb 2026 21:35:10 GMT  
		Size: 340.3 MB (340287364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0305502f1dfe96205e60d0c68f7e82d1fe576c8b59dbd5601276710f51d7f1a`  
		Last Modified: Mon, 23 Feb 2026 21:35:01 GMT  
		Size: 1.1 MB (1055028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d40e03d561ace28629c1ad24f026b0c0a8a0db436701d911a6c7c5757650def`  
		Last Modified: Mon, 23 Feb 2026 21:35:01 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bfc1018cc3b5e5015a6873251d5d2d7eb7a4c8d51005e624f2c58b0c5ae251`  
		Last Modified: Mon, 23 Feb 2026 21:35:02 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fa36a232dc399682828ec88a3f01f5db8482b0cd22d57cd163c965fff1b950`  
		Last Modified: Mon, 23 Feb 2026 21:35:02 GMT  
		Size: 10.9 KB (10905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c8c83d70a1cff34d15e286bf78dcc384265c63abeed132e284b9aac946b53b`  
		Last Modified: Mon, 23 Feb 2026 21:35:03 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:a4df7e2f560428fe355c10248861797ae2ccd8363f9b8c6664b71b597b50692b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9231458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf5f224f6b9fa0004734fed5b090a0e0401bad73c78eae464b164b250adef36`

```dockerfile
```

-	Layers:
	-	`sha256:a29755c578d9dc66f830358b435a60d1cafe81cb820378ee3bb023fb6c8eb6bd`  
		Last Modified: Mon, 23 Feb 2026 21:35:01 GMT  
		Size: 9.2 MB (9190544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da457c0e8b97ff5c08d8fb85f887247ef60da1669efa955b98dfc571e64b7016`  
		Last Modified: Mon, 23 Feb 2026 21:35:00 GMT  
		Size: 40.9 KB (40914 bytes)  
		MIME: application/vnd.in-toto+json
