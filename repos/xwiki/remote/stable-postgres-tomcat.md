## `xwiki:stable-postgres-tomcat`

```console
$ docker pull xwiki@sha256:c4c8a3a7540d568fc97199b8eb6e2dd5e81a4ba4d307df9a12207a91725bbf91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:53e2d0e2ecdeef05d8c612821544c56196eaed32383cd4202934b421f9d6fa0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **629.4 MB (629364470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f78ed240a226344506483326b409de84caa189eb177645c3de43baa4eef7df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:59 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:59 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='bf821d8240e5d660f0c7e1ffa4f62e4b2dbf72c3d2245d9371160f61389b5fa4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Dec 2025 22:17:56 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Dec 2025 22:17:56 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:17:56 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Dec 2025 22:17:56 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Dec 2025 22:17:56 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 22:17:56 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 22:17:56 GMT
ENV TOMCAT_MAJOR=10
# Mon, 08 Dec 2025 22:17:56 GMT
ENV TOMCAT_VERSION=10.1.50
# Mon, 08 Dec 2025 22:17:56 GMT
ENV TOMCAT_SHA512=c7702b0304257d80dc5bd615005fe037bd0c518e3fe77d22a58e5313fe53e6af6f4a2cf00790e3e9a669d1ae5470fb11177c9ef42f8c846d2b20dfac93e2d551
# Mon, 08 Dec 2025 22:17:56 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Dec 2025 22:18:02 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:18:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Dec 2025 22:18:02 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 22:18:02 GMT
ENTRYPOINT []
# Mon, 08 Dec 2025 22:18:02 GMT
CMD ["catalina.sh" "run"]
# Mon, 08 Dec 2025 23:46:42 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 08 Dec 2025 23:46:42 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 08 Dec 2025 23:46:42 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 08 Dec 2025 23:46:42 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 08 Dec 2025 23:46:42 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 08 Dec 2025 23:46:42 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 08 Dec 2025 23:46:42 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:46:42 GMT
ENV XWIKI_VERSION=17.10.0
# Mon, 08 Dec 2025 23:46:42 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.0
# Mon, 08 Dec 2025 23:46:42 GMT
ENV XWIKI_DOWNLOAD_SHA256=7a1942782a74736ec4ebe654ede31a4454cff230bab6818a78db09452a2d1656
# Mon, 08 Dec 2025 23:47:03 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 08 Dec 2025 23:47:03 GMT
ENV POSTGRES_JDBC_VERSION=42.7.8
# Mon, 08 Dec 2025 23:47:03 GMT
ENV POSTGRES_JDBC_SHA256=2a32a9dcbc42d67a50ad3a0de5efd102c8d2be46720045f2cbd6689f160ab7c7
# Mon, 08 Dec 2025 23:47:03 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.8
# Mon, 08 Dec 2025 23:47:03 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.8.jar
# Mon, 08 Dec 2025 23:47:03 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.8.jar
# Mon, 08 Dec 2025 23:47:03 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 08 Dec 2025 23:47:03 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 08 Dec 2025 23:47:03 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 08 Dec 2025 23:47:03 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 08 Dec 2025 23:47:03 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:47:03 GMT
VOLUME [/usr/local/xwiki]
# Mon, 08 Dec 2025 23:47:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:47:03 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f878172f1ac3121519dd1795c821097cda557a10d8ac4526d248f9fe1738b942`  
		Last Modified: Thu, 13 Nov 2025 23:21:35 GMT  
		Size: 17.0 MB (16972399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b92fa77023f1881e077b68fb149d30aade157324fdc1181dacf19b57e1313b9`  
		Last Modified: Thu, 13 Nov 2025 23:22:21 GMT  
		Size: 53.0 MB (52978772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1321ce5b3e3ab111f1a88d34df69fbf748e96e3338e9f3d403b062e3e26d99d9`  
		Last Modified: Thu, 13 Nov 2025 23:22:07 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0e444f3c26062a0908ef59f39a3b8894225b2faef3d5b877c11441d3a52713`  
		Last Modified: Thu, 13 Nov 2025 23:22:06 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1722591eb2ac562c109fdbf18fdc802dceb50a86ba43d715ee3e285bfeaa7b3d`  
		Last Modified: Mon, 08 Dec 2025 22:18:16 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a46070902b77172dac56dc910bb17f8a17e684378fc6878532553812e0a41a`  
		Last Modified: Mon, 08 Dec 2025 22:18:17 GMT  
		Size: 14.3 MB (14268356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edd638e1267734e0c97d4d5dc44661467b35eecb29fcd714f84d2ffede32698`  
		Last Modified: Mon, 08 Dec 2025 22:18:16 GMT  
		Size: 224.7 KB (224734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e6ef55c9cae3692757ac492ea1805a7bf8fe056d1a09f3ad5b1a8cbda61bab`  
		Last Modified: Tue, 09 Dec 2025 04:09:18 GMT  
		Size: 191.2 MB (191164599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30843009515e837a7f62d367634b87fea62daf105139df2c331a92b8398f7c07`  
		Last Modified: Mon, 08 Dec 2025 23:49:22 GMT  
		Size: 323.0 MB (322968365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a9acac3e54a41358196e349ae4398cc5e32148267a3c6a6744fd59b4a7a54d`  
		Last Modified: Mon, 08 Dec 2025 23:47:53 GMT  
		Size: 1.0 MB (1043010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3f865e68039a3788664f043d4dcec150089a50f918cea94948fd33aabc07f5`  
		Last Modified: Mon, 08 Dec 2025 23:47:53 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fac6dca49d798a9e3939dae8d8469cd3d40fd669b234221257747159a207af8`  
		Last Modified: Mon, 08 Dec 2025 23:47:53 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86259e98700f0e59efc911e74ba98146804d0539e0b9ce48dbba8fa9b3b8a09c`  
		Last Modified: Mon, 08 Dec 2025 23:47:53 GMT  
		Size: 10.7 KB (10678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8979e91870f154517c705bc8fc09c8634e1232de8afbe2946ee2bb0e93ff22f`  
		Last Modified: Mon, 08 Dec 2025 23:47:53 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:64416a885b1579b2aab8d42eb0879feccfcd84effed17b76c20ba050ed949541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9207688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19069b40e7a43e41b042ccf646a07a56212e235e06e4edec18e3ef3d909f9f65`

```dockerfile
```

-	Layers:
	-	`sha256:539b338e3d6d1d215a691bc4f99fab45231508f811bdb277cf3093622183f603`  
		Last Modified: Tue, 09 Dec 2025 04:08:03 GMT  
		Size: 9.2 MB (9166938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a7218ca8291fd40097fb67a41188c155791a9c1dcea1ad028910509b82bfe04`  
		Last Modified: Tue, 09 Dec 2025 04:08:03 GMT  
		Size: 40.8 KB (40750 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:ef2aa67175f5a49563bf76ea42424ffe10d467d145cd52cdd8283a1420fb46d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.4 MB (625370765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c40ec617fe19847373703bf9f68184f69241f41c050ed993975358c197585ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:20:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 13 Nov 2025 23:20:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:20:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:20:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:20:42 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 13 Nov 2025 23:21:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='bf821d8240e5d660f0c7e1ffa4f62e4b2dbf72c3d2245d9371160f61389b5fa4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 13 Nov 2025 23:21:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 13 Nov 2025 23:21:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:21:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 08 Dec 2025 22:17:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 08 Dec 2025 22:17:39 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:17:39 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 08 Dec 2025 22:17:39 GMT
WORKDIR /usr/local/tomcat
# Mon, 08 Dec 2025 22:17:39 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 22:17:39 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 08 Dec 2025 22:17:39 GMT
ENV TOMCAT_MAJOR=10
# Mon, 08 Dec 2025 22:17:39 GMT
ENV TOMCAT_VERSION=10.1.50
# Mon, 08 Dec 2025 22:17:39 GMT
ENV TOMCAT_SHA512=c7702b0304257d80dc5bd615005fe037bd0c518e3fe77d22a58e5313fe53e6af6f4a2cf00790e3e9a669d1ae5470fb11177c9ef42f8c846d2b20dfac93e2d551
# Mon, 08 Dec 2025 22:17:39 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 08 Dec 2025 22:17:48 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:17:48 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 08 Dec 2025 22:17:48 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 22:17:48 GMT
ENTRYPOINT []
# Mon, 08 Dec 2025 22:17:48 GMT
CMD ["catalina.sh" "run"]
# Mon, 08 Dec 2025 23:55:24 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 08 Dec 2025 23:55:24 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 08 Dec 2025 23:55:24 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 08 Dec 2025 23:55:24 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 08 Dec 2025 23:55:24 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 08 Dec 2025 23:55:24 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 08 Dec 2025 23:55:24 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:55:24 GMT
ENV XWIKI_VERSION=17.10.0
# Mon, 08 Dec 2025 23:55:24 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.10.0
# Mon, 08 Dec 2025 23:55:24 GMT
ENV XWIKI_DOWNLOAD_SHA256=7a1942782a74736ec4ebe654ede31a4454cff230bab6818a78db09452a2d1656
# Mon, 08 Dec 2025 23:55:45 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 08 Dec 2025 23:55:45 GMT
ENV POSTGRES_JDBC_VERSION=42.7.8
# Mon, 08 Dec 2025 23:55:45 GMT
ENV POSTGRES_JDBC_SHA256=2a32a9dcbc42d67a50ad3a0de5efd102c8d2be46720045f2cbd6689f160ab7c7
# Mon, 08 Dec 2025 23:55:45 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.8
# Mon, 08 Dec 2025 23:55:45 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.8.jar
# Mon, 08 Dec 2025 23:55:45 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.8.jar
# Mon, 08 Dec 2025 23:55:45 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 08 Dec 2025 23:55:45 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 08 Dec 2025 23:55:45 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 08 Dec 2025 23:55:45 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 08 Dec 2025 23:55:45 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 08 Dec 2025 23:55:45 GMT
VOLUME [/usr/local/xwiki]
# Mon, 08 Dec 2025 23:55:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:55:45 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e052f7b40adf3e6b8172dd9f3385e9469f4dcfbea63c3518933c4239901bcc`  
		Last Modified: Thu, 13 Nov 2025 23:21:05 GMT  
		Size: 17.0 MB (16989179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07df04fa133324a49bb96c54d2b02e9d4463a8a2ba701459d09aac3d20984431`  
		Last Modified: Thu, 13 Nov 2025 23:21:47 GMT  
		Size: 52.1 MB (52148635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3225358e001b3b4abaaa7eddcf1179402e80dd7e5627430be9ec054cf2e309`  
		Last Modified: Thu, 13 Nov 2025 23:21:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e329fb7a0e143a03a99f87ec4d7acded1e81048017d71ea84307eb3c34a052`  
		Last Modified: Thu, 13 Nov 2025 23:21:42 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074475fef476608b1476703a5f15235d6ef4877a9e34a200deceb4ec683392b7`  
		Last Modified: Mon, 08 Dec 2025 22:18:01 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b227523dc0770557e82f6f85852240268739e4f055dab16f13423e8b97d5930`  
		Last Modified: Mon, 08 Dec 2025 22:18:10 GMT  
		Size: 14.3 MB (14271559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799fd81d25790f90f3846cda3ede8af805735a2c1f792772137a668f71410d7e`  
		Last Modified: Mon, 08 Dec 2025 22:18:03 GMT  
		Size: 225.2 KB (225186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b42d8efda156781185391fba5b1d1ac77d6194341c2d0c61c17cf01faad789`  
		Last Modified: Mon, 08 Dec 2025 23:56:57 GMT  
		Size: 188.8 MB (188843280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b86bb6fc515f3b5c6dbfb6afcec20cf34e8e5bad16bb3fc3d86aff51da70620`  
		Last Modified: Mon, 08 Dec 2025 23:57:30 GMT  
		Size: 323.0 MB (322968410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0fb1f3aa2104d45c42593550bfbcb1a270e32ff7e74098dd8e54b75a3d406d`  
		Last Modified: Mon, 08 Dec 2025 23:56:34 GMT  
		Size: 1.0 MB (1043012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170f406733f2ba1400521f0069c4ff80c884f19be5de9be349277f2065621da9`  
		Last Modified: Mon, 08 Dec 2025 23:56:34 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9c7ebbf75d6b80fb7c8810e6d818c5db25d5c1c500efee2b294b00770df190`  
		Last Modified: Mon, 08 Dec 2025 23:56:34 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ec1aefb0289bc4a11ca28e6c5da2338a3e56c082a17426ada4fec47716a70c`  
		Last Modified: Mon, 08 Dec 2025 23:56:34 GMT  
		Size: 10.7 KB (10677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090232c783a73a2b19b62a018b52929cb6531bcf905d578f0a4f2579723b46d9`  
		Last Modified: Mon, 08 Dec 2025 23:56:35 GMT  
		Size: 2.4 KB (2419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:dcf912eb1a7e758621aa8e93fdf75c98e4e0ea4fcc5e97b5f44b1acb09a00b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9208615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8789b41c738f033dd54e645ef0e7d7675d825a29792578a93dc4ec44f75c82ec`

```dockerfile
```

-	Layers:
	-	`sha256:68f5b32af9ba1215a528a6ebe87b6a3af3dfb7b9d5152357c9f85da0be66314d`  
		Last Modified: Tue, 09 Dec 2025 04:08:10 GMT  
		Size: 9.2 MB (9167691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:532372c208e9bc7ba2f0fe11563ebbc0d061ddf65e2b2ba9d5f9397d8fefeade`  
		Last Modified: Tue, 09 Dec 2025 04:08:10 GMT  
		Size: 40.9 KB (40924 bytes)  
		MIME: application/vnd.in-toto+json
