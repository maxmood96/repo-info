## `xwiki:postgres-tomcat`

```console
$ docker pull xwiki@sha256:ec11188e6e0a7c3fc6e94f1e1411e82e9ffb916349a16deccb11a641d69c154e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:efbbbb4f696ee7f6c4bbea84f01f2e3b5379be107b195d2cf7ee9f5af0455d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.4 MB (577432178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e485f0fec22b40314c278c930d6d8761615678233ce068a423bbe8f141de8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 25 Mar 2024 15:14:20 GMT
ARG RELEASE
# Mon, 25 Mar 2024 15:14:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Mar 2024 15:14:20 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Mon, 25 Mar 2024 15:14:20 GMT
CMD ["/bin/bash"]
# Mon, 25 Mar 2024 15:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 25 Mar 2024 15:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Mar 2024 15:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 25 Mar 2024 15:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 25 Mar 2024 15:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Mar 2024 15:14:20 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 25 Mar 2024 15:14:20 GMT
WORKDIR /usr/local/tomcat
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 25 Mar 2024 15:14:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 25 Mar 2024 15:14:20 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_MAJOR=9
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_VERSION=9.0.88
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Mon, 25 Mar 2024 15:14:20 GMT
COPY dir:008c1e737cb1d7c32c9c864d02bf0b16431c32c3c39b5b68188e5f3c48a90ec8 in /usr/local/tomcat 
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 25 Mar 2024 15:14:20 GMT
EXPOSE 8080
# Mon, 25 Mar 2024 15:14:20 GMT
ENTRYPOINT []
# Mon, 25 Mar 2024 15:14:20 GMT
CMD ["catalina.sh" "run"]
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 25 Mar 2024 15:14:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENV XWIKI_VERSION=16.2.0
# Mon, 25 Mar 2024 15:14:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.2.0
# Mon, 25 Mar 2024 15:14:20 GMT
ENV XWIKI_DOWNLOAD_SHA256=7d355ae1c88691b19af9658e3f042083d57c08d5e52e1ade25536536ad72fb3f
# Mon, 25 Mar 2024 15:14:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENV POSTGRES_JDBC_VERSION=42.7.2
# Mon, 25 Mar 2024 15:14:20 GMT
ENV POSTGRES_JDBC_SHA256=0c244ac7d02cf89d8e29852eace6595d75bc4d78581b85b2768460081646a57b
# Mon, 25 Mar 2024 15:14:20 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.2
# Mon, 25 Mar 2024 15:14:20 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.2.jar
# Mon, 25 Mar 2024 15:14:20 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.2.jar
# Mon, 25 Mar 2024 15:14:20 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
VOLUME [/usr/local/xwiki]
# Mon, 25 Mar 2024 15:14:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Mar 2024 15:14:20 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d7c5a42f2fad87126e0a61b4605e0b8b0b8100485fbffb0fa0e14e87400873`  
		Last Modified: Thu, 25 Apr 2024 22:13:22 GMT  
		Size: 12.9 MB (12905143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7fcad56b7f8a33a6681a9ae067f80cc8ad2a08502172c8dda569c1338752bc`  
		Last Modified: Thu, 25 Apr 2024 22:16:38 GMT  
		Size: 47.3 MB (47256188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75513697e6ba945551856344dc1f1c94b25b9b98458dd13e8f1a25811e2424cc`  
		Last Modified: Thu, 25 Apr 2024 22:16:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e30da527722230ddaac2aa5e9ae62f333caa596c7853ae2b516c06d2d6f321f`  
		Last Modified: Thu, 25 Apr 2024 22:16:31 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbe592fe48d6c084fee6f5aacb2b9e6f82e7ca9df70e0b07d90293f5b63c3ce`  
		Last Modified: Fri, 26 Apr 2024 02:41:36 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444245f0d6247cb9dad7dfebf1c48a211ada161bfe718b510dcff4ace7db8b3d`  
		Last Modified: Fri, 26 Apr 2024 02:44:24 GMT  
		Size: 12.4 MB (12423161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b89b597525467f9c190aacd6e15109dd30104ea9f42c0012416b47528154d5`  
		Last Modified: Fri, 26 Apr 2024 02:44:23 GMT  
		Size: 456.3 KB (456347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84795a15235ec76f356d76ebe4b2c1bead01104cfc31262df94c8abca13321e0`  
		Last Modified: Fri, 26 Apr 2024 02:44:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc6410add4b4989f116effddf5a85168ce821cbe76050795ce7c6134dcaf776`  
		Last Modified: Fri, 26 Apr 2024 04:51:34 GMT  
		Size: 179.4 MB (179369169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718d53c46b8f8a0784582e2da352bd19ece197f8ddc1cdce88be60a9a157d49b`  
		Last Modified: Fri, 26 Apr 2024 04:51:34 GMT  
		Size: 293.6 MB (293556741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367865c0d14a9c52d48b370a725d3cbdf528037a29cc3516a32623fa88a11891`  
		Last Modified: Fri, 26 Apr 2024 04:51:30 GMT  
		Size: 1.0 MB (1011768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e47f411f8fece3d7629b40c79c69d4932584ba9306634d62fa242e67069d0b1`  
		Last Modified: Fri, 26 Apr 2024 04:51:29 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e0846323830919779ecaa0783f071b3300a44f09eb6ea756f4a57b493b14c2`  
		Last Modified: Fri, 26 Apr 2024 04:51:30 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d387509f7ebfc47319712a727c03082871065fcf52d3328a473a4e67940a44c3`  
		Last Modified: Fri, 26 Apr 2024 04:51:31 GMT  
		Size: 6.5 KB (6507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374959a6ad4bf3dd02b84fa9e343cbeacd6d035470a5505f0bdd48809448065d`  
		Last Modified: Fri, 26 Apr 2024 04:51:31 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:428fd91c02fc0181f1551136a67c30f143f3e6b9d919a2b962e3c8ac8484ab16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8935198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2b89b3f987e99583869b19b6eba9b51264c3384904935dc610f990e6e6cbf5`

```dockerfile
```

-	Layers:
	-	`sha256:5fddebf1914560cbed351b48423315b2ace9975f9ea3719c227b053a4c883886`  
		Last Modified: Fri, 26 Apr 2024 04:51:30 GMT  
		Size: 8.9 MB (8893405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee108581c6d93e0267e96e65a950c8ae1c5e783e81a55c6b9436835f7d4d0dd2`  
		Last Modified: Fri, 26 Apr 2024 04:51:30 GMT  
		Size: 41.8 KB (41793 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:19c91ef9135de9b4825075eb5b0a568d437e9c2cedfa5ea7fd86ba324803780b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.8 MB (569778350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c5749bf691c917983a1c1a33ab4cfb5791c909f216d77755f7d63dcd6df65c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 25 Mar 2024 15:14:20 GMT
ARG RELEASE
# Mon, 25 Mar 2024 15:14:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Mar 2024 15:14:20 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Mon, 25 Mar 2024 15:14:20 GMT
CMD ["/bin/bash"]
# Mon, 25 Mar 2024 15:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 25 Mar 2024 15:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Mar 2024 15:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 25 Mar 2024 15:14:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 25 Mar 2024 15:14:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Mar 2024 15:14:20 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 25 Mar 2024 15:14:20 GMT
WORKDIR /usr/local/tomcat
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 25 Mar 2024 15:14:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 25 Mar 2024 15:14:20 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_MAJOR=9
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_VERSION=9.0.88
# Mon, 25 Mar 2024 15:14:20 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Mon, 25 Mar 2024 15:14:20 GMT
COPY dir:ba3e33ed23284380cd070ee082efc56bd4e069281d5d61e5fd722562420f4b69 in /usr/local/tomcat 
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Mar 2024 15:14:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 25 Mar 2024 15:14:20 GMT
EXPOSE 8080
# Mon, 25 Mar 2024 15:14:20 GMT
ENTRYPOINT []
# Mon, 25 Mar 2024 15:14:20 GMT
CMD ["catalina.sh" "run"]
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 25 Mar 2024 15:14:20 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 25 Mar 2024 15:14:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENV XWIKI_VERSION=16.2.0
# Mon, 25 Mar 2024 15:14:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.2.0
# Mon, 25 Mar 2024 15:14:20 GMT
ENV XWIKI_DOWNLOAD_SHA256=7d355ae1c88691b19af9658e3f042083d57c08d5e52e1ade25536536ad72fb3f
# Mon, 25 Mar 2024 15:14:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
ENV POSTGRES_JDBC_VERSION=42.7.2
# Mon, 25 Mar 2024 15:14:20 GMT
ENV POSTGRES_JDBC_SHA256=0c244ac7d02cf89d8e29852eace6595d75bc4d78581b85b2768460081646a57b
# Mon, 25 Mar 2024 15:14:20 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.2
# Mon, 25 Mar 2024 15:14:20 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.2.jar
# Mon, 25 Mar 2024 15:14:20 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.2.jar
# Mon, 25 Mar 2024 15:14:20 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 25 Mar 2024 15:14:20 GMT
VOLUME [/usr/local/xwiki]
# Mon, 25 Mar 2024 15:14:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 25 Mar 2024 15:14:20 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62af4570e03cd18721264dca7618ad8bfe7fc52046caf98dd92dbd19a11ae3bf`  
		Last Modified: Tue, 16 Apr 2024 02:55:33 GMT  
		Size: 12.8 MB (12847096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9331e6965ccd210b6fd21419523ddc450c72626bd5ca5b0672bb8c0a1cb596ad`  
		Last Modified: Tue, 16 Apr 2024 02:58:28 GMT  
		Size: 46.6 MB (46639080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af58a4038ec765397b1ef467a9d6da1d336353f28df5cc32c5516aa471e4bb4e`  
		Last Modified: Tue, 16 Apr 2024 02:58:22 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8322d102061cd226429f20602d322142091650639e707df1fc051fbc869c138e`  
		Last Modified: Tue, 16 Apr 2024 02:58:22 GMT  
		Size: 732.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e02da29e0dc36cfae157626956d709192018538adafffbf45caf04e6a5125bc`  
		Last Modified: Tue, 16 Apr 2024 08:41:00 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05628a793e4710e8b8b6ff5020fc155e6fb4b9f57abb6a53107c4a9063206fd2`  
		Last Modified: Wed, 17 Apr 2024 01:03:32 GMT  
		Size: 12.4 MB (12430998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80252592221cd05095a4d105203d89f19cca649dfcbdd8fa72e81b2032a32a25`  
		Last Modified: Wed, 17 Apr 2024 01:03:31 GMT  
		Size: 455.7 KB (455662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db2f7057439ac6773bf8cae77e2fb8b772c8eb0dbcc9e4ec133d1d9642a32b1`  
		Last Modified: Wed, 17 Apr 2024 01:03:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a534a520fb36d08e2fbb6e0490ec5a2a853cedbeba3f6e08838dc1ca417b7c04`  
		Last Modified: Thu, 18 Apr 2024 18:49:16 GMT  
		Size: 174.4 MB (174422729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa0f773c7eeb7cae31856411b4d1562fc8532b787a3a67ae6511161eb5a6664`  
		Last Modified: Thu, 18 Apr 2024 18:49:16 GMT  
		Size: 293.6 MB (293556771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8bdf93892e26d3dca371cb8fe78e106260153580710566ffd496a2c27365e`  
		Last Modified: Thu, 18 Apr 2024 18:49:10 GMT  
		Size: 1.0 MB (1011773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e5825c2f67d5eb8950486ba643d5b4cd525f63c83e930fb2c44c66cabaf655`  
		Last Modified: Thu, 18 Apr 2024 18:49:10 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceaf4dec1568ec3fa02041c86c2b21696344408b777b38b9ff8b88f51f7820a6`  
		Last Modified: Thu, 18 Apr 2024 18:49:11 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cbc985f1e2000864d438e4362e84aa6a337e49773d13ef4318a064dcf04a86`  
		Last Modified: Thu, 18 Apr 2024 18:49:11 GMT  
		Size: 6.5 KB (6508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213717fc42a878d828e71f2342d09a1bffc23f98b6f780194cb9b1eb629a499b`  
		Last Modified: Thu, 18 Apr 2024 18:49:12 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:b87b5198f4fccf7284408897d6cefa4e230435eed7db09f3fef2882bea00be8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8932822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6c75dbbe0176511d1471b52577be2c1b3f6457f04b428f47a8f800fd48ae51`

```dockerfile
```

-	Layers:
	-	`sha256:01dd3a5078f1f166a1a045ac935d62ec3277898a01d84b888c15f10ad6a9f0f1`  
		Last Modified: Thu, 18 Apr 2024 18:49:10 GMT  
		Size: 8.9 MB (8892480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10470370cd28585c27b0a9174855d0d967ec6bb4bc341ca5960e68b1e236f44a`  
		Last Modified: Thu, 18 Apr 2024 18:49:09 GMT  
		Size: 40.3 KB (40342 bytes)  
		MIME: application/vnd.in-toto+json
