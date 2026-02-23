## `xwiki:18-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:22095a537cd368959cf42f99c3c8742682e64ef58c450d9e530529374008d09a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:18-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:224c6ea13b86cdf7a5b1f52c4113d555b721f0dfadce31d7423715a67d272efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.5 MB (647528177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a47782f06e785358b364896bd557c80c757437fc8714afbb4c2d7c73f61fa1`
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
# Mon, 23 Feb 2026 21:34:06 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 23 Feb 2026 21:34:06 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 23 Feb 2026 21:34:06 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 23 Feb 2026 21:34:06 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 23 Feb 2026 21:34:06 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 23 Feb 2026 21:34:06 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 23 Feb 2026 21:34:06 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 21:34:06 GMT
ENV XWIKI_VERSION=18.1.0
# Mon, 23 Feb 2026 21:34:06 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.1.0
# Mon, 23 Feb 2026 21:34:06 GMT
ENV XWIKI_DOWNLOAD_SHA256=0f7d70d190ebf20483b3afd79b006050bbe4618ca1dab02bc74e1c3202bd63c0
# Mon, 23 Feb 2026 21:34:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 23 Feb 2026 21:34:28 GMT
ENV MARIADB_JDBC_VERSION=3.5.7
# Mon, 23 Feb 2026 21:34:28 GMT
ENV MARIADB_JDBC_SHA256=07bb1229dc184f3313a5aef4c5a6b3207c8dbaa09db4a26814c936f004b4c526
# Mon, 23 Feb 2026 21:34:28 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.7
# Mon, 23 Feb 2026 21:34:28 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.7.jar
# Mon, 23 Feb 2026 21:34:28 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.7.jar
# Mon, 23 Feb 2026 21:34:28 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 23 Feb 2026 21:34:28 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 23 Feb 2026 21:34:28 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 23 Feb 2026 21:34:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 23 Feb 2026 21:34:28 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 23 Feb 2026 21:34:28 GMT
VOLUME [/usr/local/xwiki]
# Mon, 23 Feb 2026 21:34:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Feb 2026 21:34:28 GMT
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
	-	`sha256:a19d4733294e3330f0f1c255b5f83a310bb3ee0917a93303ef033274b9ba8914`  
		Last Modified: Mon, 23 Feb 2026 21:35:10 GMT  
		Size: 192.3 MB (192309755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fcf6187817f15796538c5e3dfde855c04f8a2ace8c3c63b77f2834a5219278`  
		Last Modified: Mon, 23 Feb 2026 21:35:13 GMT  
		Size: 340.3 MB (340287364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5246e302c011c13aa454b3707b004e559938db390c579133c7313cdce8f40153`  
		Last Modified: Mon, 23 Feb 2026 21:35:03 GMT  
		Size: 708.5 KB (708544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8857284fbc3707b45bc46ef684b7ece3a9ad77bbb4feea17a20e4963a6d88bd3`  
		Last Modified: Mon, 23 Feb 2026 21:35:03 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00a601d45fb2c88271717c049071be8a8353d694a2463698f4390922e262947`  
		Last Modified: Mon, 23 Feb 2026 21:35:04 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1bf27c5606138cee81c2c939bb2ff294c94f505871cc6705cc261b2529534e`  
		Last Modified: Mon, 23 Feb 2026 21:35:04 GMT  
		Size: 10.9 KB (10904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734f6c97ac641bb512d875cc3f5b97df83bad04232bb4538f3ae425c268be32`  
		Last Modified: Mon, 23 Feb 2026 21:35:05 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:18-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:0fdc003260c5de537da63aa63336b672b7b017215277312d2fe24caddf857623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9230538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9aaeca3e75608562b7a66de4d98a513d2da2d2fb9c521fdc59826f73dff6d3`

```dockerfile
```

-	Layers:
	-	`sha256:f1aec4f81d7c893cf7b3633f0e4c17dffbf8d1510bda8da9ca8cefd9747a196c`  
		Last Modified: Mon, 23 Feb 2026 21:35:03 GMT  
		Size: 9.2 MB (9189774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55cc7306c479af1842dd94d42fd15ad417442eb514a18fd3fbd70f3ab6886a06`  
		Last Modified: Mon, 23 Feb 2026 21:35:02 GMT  
		Size: 40.8 KB (40764 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:18-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:c46b4e8f906272876833b83fd743318a1acc662848af9c447e7cc20fbcb937d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.5 MB (643463105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e352c5c803c2725833eb9f5ba8a67d42a00bb4c2941305c9ed938d4f1543f20`
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
# Mon, 23 Feb 2026 21:34:05 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 23 Feb 2026 21:34:05 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 23 Feb 2026 21:34:05 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 23 Feb 2026 21:34:05 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 23 Feb 2026 21:34:05 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 23 Feb 2026 21:34:05 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 23 Feb 2026 21:34:05 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 21:34:05 GMT
ENV XWIKI_VERSION=18.1.0
# Mon, 23 Feb 2026 21:34:05 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.1.0
# Mon, 23 Feb 2026 21:34:05 GMT
ENV XWIKI_DOWNLOAD_SHA256=0f7d70d190ebf20483b3afd79b006050bbe4618ca1dab02bc74e1c3202bd63c0
# Mon, 23 Feb 2026 21:34:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 23 Feb 2026 21:34:28 GMT
ENV MARIADB_JDBC_VERSION=3.5.7
# Mon, 23 Feb 2026 21:34:28 GMT
ENV MARIADB_JDBC_SHA256=07bb1229dc184f3313a5aef4c5a6b3207c8dbaa09db4a26814c936f004b4c526
# Mon, 23 Feb 2026 21:34:28 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.7
# Mon, 23 Feb 2026 21:34:28 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.7.jar
# Mon, 23 Feb 2026 21:34:28 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.7.jar
# Mon, 23 Feb 2026 21:34:28 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 23 Feb 2026 21:34:28 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 23 Feb 2026 21:34:28 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 23 Feb 2026 21:34:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 23 Feb 2026 21:34:28 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 23 Feb 2026 21:34:28 GMT
VOLUME [/usr/local/xwiki]
# Mon, 23 Feb 2026 21:34:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Feb 2026 21:34:28 GMT
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
	-	`sha256:6ac1641392fccdc109a15e22d30802d827e2cc5e536835f20f7889429a824755`  
		Last Modified: Mon, 23 Feb 2026 21:35:08 GMT  
		Size: 189.9 MB (189919119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6953a68a675d602221a1428737ff601f8574f19a8afe4b1c73cac9ed42cead9a`  
		Last Modified: Mon, 23 Feb 2026 21:35:11 GMT  
		Size: 340.3 MB (340287289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c690619acb7c4d957dc9874469d1eaba9fa4debb20e2d2a2b88402debf20363`  
		Last Modified: Mon, 23 Feb 2026 21:35:01 GMT  
		Size: 708.5 KB (708544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a78c39a3947e3a0286629a3048287e21a831bf5233580286cf48f894f9d8cbe`  
		Last Modified: Mon, 23 Feb 2026 21:35:02 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deda478bdf0cd2089629cbc629f600854baf54f24e419f75b72bbd22c1a0f92`  
		Last Modified: Mon, 23 Feb 2026 21:35:03 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbeb92dd07663b79e463611bdef51aebbd8435a8a56007ba6b475f6ae3f1005`  
		Last Modified: Mon, 23 Feb 2026 21:35:03 GMT  
		Size: 10.9 KB (10902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68fcf9d78e2d27f59268380c8115a46785556151b28ed20eb1db663f4f1b247`  
		Last Modified: Mon, 23 Feb 2026 21:35:04 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:18-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:1937124e47e81111621ffa2524994ef08398f94933b81d0b81a79fef70a80997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9231464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbb0660bc7aa627c6ab4c5b3ed1462bf6c9d2353431a8ba5aef38d38540676a`

```dockerfile
```

-	Layers:
	-	`sha256:bc4f956fd5b51ee6cfebc30b72bcee837b0fdf1823cfcfd6d71900bc9b20e9de`  
		Last Modified: Mon, 23 Feb 2026 21:35:02 GMT  
		Size: 9.2 MB (9190527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c80176891e64f8b8ba6b0bd9c92b85bd5107cb5402bb32eb838f90bc857688e`  
		Last Modified: Mon, 23 Feb 2026 21:35:01 GMT  
		Size: 40.9 KB (40937 bytes)  
		MIME: application/vnd.in-toto+json
