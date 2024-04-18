## `xwiki:lts-mariadb`

```console
$ docker pull xwiki@sha256:04202847e50031547f9ae604e98ffcd5a78de8dde7b11f2e3ec14dc9867df267
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb` - linux; amd64

```console
$ docker pull xwiki@sha256:0c6ea5c9ec0c825b3ea47ac23e802b5a2d5ba93efd80d0573513983e2306bca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 MB (589463297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bbb10ced229172c63b07ffb384f68d90cf6a3e1f027279cb5de058303acaff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 27 Mar 2024 12:37:20 GMT
ARG RELEASE
# Wed, 27 Mar 2024 12:37:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 27 Mar 2024 12:37:20 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 27 Mar 2024 12:37:20 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 12:37:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 12:37:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 12:37:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 12:37:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 27 Mar 2024 12:37:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 Mar 2024 12:37:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 27 Mar 2024 12:37:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 12:37:20 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 27 Mar 2024 12:37:20 GMT
WORKDIR /usr/local/tomcat
# Wed, 27 Mar 2024 12:37:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 27 Mar 2024 12:37:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 27 Mar 2024 12:37:20 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 27 Mar 2024 12:37:20 GMT
ENV TOMCAT_MAJOR=9
# Wed, 27 Mar 2024 12:37:20 GMT
ENV TOMCAT_VERSION=9.0.88
# Wed, 27 Mar 2024 12:37:20 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Wed, 27 Mar 2024 12:37:20 GMT
COPY dir:21b598d99845ff41cfddd8ebdf74c402718bd40914bc352e03188c0e23998855 in /usr/local/tomcat 
# Wed, 27 Mar 2024 12:37:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Mar 2024 12:37:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 27 Mar 2024 12:37:20 GMT
EXPOSE 8080
# Wed, 27 Mar 2024 12:37:20 GMT
ENTRYPOINT []
# Wed, 27 Mar 2024 12:37:20 GMT
CMD ["catalina.sh" "run"]
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 27 Mar 2024 12:37:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
ENV XWIKI_VERSION=15.10.8
# Wed, 27 Mar 2024 12:37:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.8
# Wed, 27 Mar 2024 12:37:20 GMT
ENV XWIKI_DOWNLOAD_SHA256=20bfda3e0a694df904cab1f0291ff40761cf3461117654c5dc4860ba6397fd85
# Wed, 27 Mar 2024 12:37:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
ENV MARIADB_JDBC_VERSION=3.3.3
# Wed, 27 Mar 2024 12:37:20 GMT
ENV MARIADB_JDBC_SHA256=89d71a6ffd800c032b23e588108688d391631f0aba962ba2381cc82cb111b796
# Wed, 27 Mar 2024 12:37:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.3
# Wed, 27 Mar 2024 12:37:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.3.jar
# Wed, 27 Mar 2024 12:37:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.3.jar
# Wed, 27 Mar 2024 12:37:20 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
VOLUME [/usr/local/xwiki]
# Wed, 27 Mar 2024 12:37:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Mar 2024 12:37:20 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dddff65ed2408fb8512cf4a5e475bc56396102dc76b9968c1f68a06414767b`  
		Last Modified: Tue, 16 Apr 2024 04:03:41 GMT  
		Size: 12.9 MB (12905145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1799e72eec6b835f4f493ec08eef7c0de31e3d1e4b3265db1d346a5282630e16`  
		Last Modified: Tue, 16 Apr 2024 04:06:54 GMT  
		Size: 47.2 MB (47163386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e489940d10c0f286533ea7999e045f2ff1188baa6aad2d676349e3e72c5e8b`  
		Last Modified: Tue, 16 Apr 2024 04:06:48 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34382f6b019ca012a4b3f974b3039a24f169585e6ae8fa737cf539791d51ea1f`  
		Last Modified: Tue, 16 Apr 2024 04:06:48 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3fe4efe3c3e9e7b9015cc8ea7e8520be3c126dc915b4987e9d8ab966fa0faf`  
		Last Modified: Tue, 16 Apr 2024 10:17:56 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e461cc60d5d721b03cd0896f718040546e37022620703bb4023e13abc6ff6f`  
		Last Modified: Wed, 17 Apr 2024 00:53:32 GMT  
		Size: 12.4 MB (12423174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0fc3af8030aac4ada24c5100acd6056729ce68b5a05a36b5ce3a4ce43c7823`  
		Last Modified: Wed, 17 Apr 2024 00:53:32 GMT  
		Size: 456.3 KB (456267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69fa22e2f846057d0e21a57835b0ce44f5b1af95d2144074ba9dc386f18dcfa`  
		Last Modified: Wed, 17 Apr 2024 00:53:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16597cdceb2be9673124c02a299af32ec20a32d9b557e901dbfa55fae50aefce`  
		Last Modified: Wed, 17 Apr 2024 01:50:55 GMT  
		Size: 178.4 MB (178431001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ef7f0d48f84788d2069296f9907dd60e3b2a1a2af5b743e49ef0e0469433a`  
		Last Modified: Wed, 17 Apr 2024 01:50:57 GMT  
		Size: 307.0 MB (307010852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f248f45639018d27ab1058d2b6b38887250b4e5d18889118c278ec5680ee94c8`  
		Last Modified: Wed, 17 Apr 2024 01:50:50 GMT  
		Size: 620.0 KB (619999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a690b3bfcb56f3f9343474850f9865dfe53e7df6b41115bb8bb2c2a637e0c4`  
		Last Modified: Wed, 17 Apr 2024 01:50:50 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b817c4132b7bdc192fd352e864e408aad27d904e36f3466f1bfaa41ef5504a41`  
		Last Modified: Wed, 17 Apr 2024 01:50:51 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec9864f7257cd137d88572bf161361c2b699af98c45fd16e689ac47703f6ccb`  
		Last Modified: Wed, 17 Apr 2024 01:50:52 GMT  
		Size: 6.4 KB (6415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ea2356689a0e3eb0dd3000f505ed17c440f819c7451cc36cb5d72615b2745a`  
		Last Modified: Wed, 17 Apr 2024 01:50:52 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:0b6a931e4875fa3eadafb063875319c84a1b9c2e5ef53062164320d4af30d605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8935370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54734bf0c34e600f7ba886abcbbfba36f2a2bb0a523a5abcae1fc79acc9909ca`

```dockerfile
```

-	Layers:
	-	`sha256:5c73e30aa0c5080a9529d0851efefcdb8c44eb40ef59c6a655b78981ad3c2f64`  
		Last Modified: Wed, 17 Apr 2024 01:50:50 GMT  
		Size: 8.9 MB (8893976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4279ce472e4a71ab8821c7f91335459b1ae49756fa31114d96f32fff99c349e`  
		Last Modified: Wed, 17 Apr 2024 01:50:50 GMT  
		Size: 41.4 KB (41394 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:10d7c9eae1ae2b21498d1ca3f77a5254031d0df272c6dec88f1464ca245985e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.9 MB (581903163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80dcc57b4a67d73164f8d52b02078ae4af1c9a0e79a610f3faeb8e1c52bffa40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 27 Mar 2024 12:37:20 GMT
ARG RELEASE
# Wed, 27 Mar 2024 12:37:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 27 Mar 2024 12:37:20 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 27 Mar 2024 12:37:20 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 12:37:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 12:37:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 12:37:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 12:37:20 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 27 Mar 2024 12:37:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 Mar 2024 12:37:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 27 Mar 2024 12:37:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 12:37:20 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 27 Mar 2024 12:37:20 GMT
WORKDIR /usr/local/tomcat
# Wed, 27 Mar 2024 12:37:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 27 Mar 2024 12:37:20 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 27 Mar 2024 12:37:20 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 27 Mar 2024 12:37:20 GMT
ENV TOMCAT_MAJOR=9
# Wed, 27 Mar 2024 12:37:20 GMT
ENV TOMCAT_VERSION=9.0.88
# Wed, 27 Mar 2024 12:37:20 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Wed, 27 Mar 2024 12:37:20 GMT
COPY dir:ba3e33ed23284380cd070ee082efc56bd4e069281d5d61e5fd722562420f4b69 in /usr/local/tomcat 
# Wed, 27 Mar 2024 12:37:20 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Mar 2024 12:37:20 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 27 Mar 2024 12:37:20 GMT
EXPOSE 8080
# Wed, 27 Mar 2024 12:37:20 GMT
ENTRYPOINT []
# Wed, 27 Mar 2024 12:37:20 GMT
CMD ["catalina.sh" "run"]
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 27 Mar 2024 12:37:20 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 27 Mar 2024 12:37:20 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
ENV XWIKI_VERSION=15.10.8
# Wed, 27 Mar 2024 12:37:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.8
# Wed, 27 Mar 2024 12:37:20 GMT
ENV XWIKI_DOWNLOAD_SHA256=20bfda3e0a694df904cab1f0291ff40761cf3461117654c5dc4860ba6397fd85
# Wed, 27 Mar 2024 12:37:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
ENV MARIADB_JDBC_VERSION=3.3.3
# Wed, 27 Mar 2024 12:37:20 GMT
ENV MARIADB_JDBC_SHA256=89d71a6ffd800c032b23e588108688d391631f0aba962ba2381cc82cb111b796
# Wed, 27 Mar 2024 12:37:20 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.3.3
# Wed, 27 Mar 2024 12:37:20 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.3.3.jar
# Wed, 27 Mar 2024 12:37:20 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.3.3.jar
# Wed, 27 Mar 2024 12:37:20 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
VOLUME [/usr/local/xwiki]
# Wed, 27 Mar 2024 12:37:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Mar 2024 12:37:20 GMT
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
	-	`sha256:a0cae0fda705047354692cc1a8f026d0611d4f05e02a33f2d60cc610292093d1`  
		Last Modified: Thu, 18 Apr 2024 18:48:47 GMT  
		Size: 173.5 MB (173485383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31ca320fbda07ea305c82f2d5d27ab1054a47c1cf3cca58630dcb4b62c02401`  
		Last Modified: Thu, 18 Apr 2024 18:50:03 GMT  
		Size: 307.0 MB (307010934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8944433474a63c6f508693ef11cb76caafa17c8f4529aeb9cd187537f49951`  
		Last Modified: Thu, 18 Apr 2024 18:50:51 GMT  
		Size: 620.0 KB (620000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfbae0cd4cbd545ff23c72a42ff00d60759853be6d7534728e1a6e14b7318c5`  
		Last Modified: Thu, 18 Apr 2024 18:50:51 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05799d3c339bde6d3d7f80de277611a82eb67956917e620b789dc3d1d9b5907`  
		Last Modified: Thu, 18 Apr 2024 18:50:51 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e451a587513c014bb6a6e6ceea5d0152547215938b7c646c12fca180d2449de`  
		Last Modified: Thu, 18 Apr 2024 18:50:51 GMT  
		Size: 6.4 KB (6417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac2b594c18be9ec167590d6857a6a5001c3dd69d58f05fc7b17bc5fcb115746`  
		Last Modified: Thu, 18 Apr 2024 18:50:52 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb` - unknown; unknown

```console
$ docker pull xwiki@sha256:b85752cdf46b6aa54f531a55a334ea821d13855516f887d3a673caba4f09cdfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8934424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bffea4e22fe6fb754c13f9de85b3298740b56c04dafba075f5c5c6deb6d306`

```dockerfile
```

-	Layers:
	-	`sha256:3e25b833b8f5ee928ac819acabc25908f5152d347c7b3a9ef43ffd28834b3eed`  
		Last Modified: Thu, 18 Apr 2024 18:50:51 GMT  
		Size: 8.9 MB (8894483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e41bb6236a3f6261f0349a9ffc724f9de84a5c23494590d000a49b421133e6`  
		Last Modified: Thu, 18 Apr 2024 18:50:51 GMT  
		Size: 39.9 KB (39941 bytes)  
		MIME: application/vnd.in-toto+json
