## `xwiki:lts-postgres-tomcat`

```console
$ docker pull xwiki@sha256:86c6996606514ff7c7821b35a1289304ace3fc2861b9b15104906e8e8854d365
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:58dcf883fd6f00a0948e2cb624cd1a41124f287d959e7fc7bd69e906923a324f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.9 MB (590886649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f42ed3940f5157ef24778a4c718403d8305eafdb9bd7dff12a45abe9440d90`
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
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
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
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 27 Mar 2024 12:37:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
COPY dir:008c1e737cb1d7c32c9c864d02bf0b16431c32c3c39b5b68188e5f3c48a90ec8 in /usr/local/tomcat 
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
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
ENV XWIKI_VERSION=15.10.8
# Wed, 27 Mar 2024 12:37:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.8
# Wed, 27 Mar 2024 12:37:20 GMT
ENV XWIKI_DOWNLOAD_SHA256=20bfda3e0a694df904cab1f0291ff40761cf3461117654c5dc4860ba6397fd85
# Wed, 27 Mar 2024 12:37:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
ENV POSTGRES_JDBC_VERSION=42.7.2
# Wed, 27 Mar 2024 12:37:20 GMT
ENV POSTGRES_JDBC_SHA256=0c244ac7d02cf89d8e29852eace6595d75bc4d78581b85b2768460081646a57b
# Wed, 27 Mar 2024 12:37:20 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.2
# Wed, 27 Mar 2024 12:37:20 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.2.jar
# Wed, 27 Mar 2024 12:37:20 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.2.jar
# Wed, 27 Mar 2024 12:37:20 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:c36016ef2108e83f089bfa29d0ca20ccdf96a37f9ef242aac2da1ee7ce771b53`  
		Last Modified: Fri, 26 Apr 2024 03:51:36 GMT  
		Size: 179.4 MB (179369637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712a8aa6b4b8afbd81a651a14a27b01095d993833a1350d84b1cc02d4b98177b`  
		Last Modified: Fri, 26 Apr 2024 03:51:38 GMT  
		Size: 307.0 MB (307010830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4553fbaf305a37de0762b6506bd50cc48f2582554ae3c33613fb5b4a0736b6`  
		Last Modified: Fri, 26 Apr 2024 03:51:34 GMT  
		Size: 1.0 MB (1011770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a91caa07683daa11401bd0225edf816cce94b4945c3d46ef9df6709edce1c2`  
		Last Modified: Fri, 26 Apr 2024 03:51:34 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4914b5ac6f10f414ac82ba6d31a690d09b630ff508d0fc2d9c6b309794cb9ab8`  
		Last Modified: Fri, 26 Apr 2024 03:51:35 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fa0d85b9aa5a822a5841811b9cd49d9b949f91833a80f8fe81a3d80dd8476d`  
		Last Modified: Fri, 26 Apr 2024 03:51:35 GMT  
		Size: 6.4 KB (6415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bf12c9ecfe70e1acd7319d8e2d90c25265907bb2aa79ec184b132ec29343d7`  
		Last Modified: Fri, 26 Apr 2024 03:51:36 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:e445a80a3e22c32928507394f127c2be0a3902cca07d86aa0808e553c753b94c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8946187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a94db1a0077c8293534807cdb70c0225dd1f2101e482987da463f6bb40c5712f`

```dockerfile
```

-	Layers:
	-	`sha256:41a50da8530a574c936d2fa4655409cc1b5bc74b88d57d8554f216d1ce65a453`  
		Last Modified: Fri, 26 Apr 2024 03:51:34 GMT  
		Size: 8.9 MB (8904710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:469ffc7c994dc31a1b71f85f75e415a1dbd87fb48e11cb3e04897b1a7d98e170`  
		Last Modified: Fri, 26 Apr 2024 03:51:34 GMT  
		Size: 41.5 KB (41477 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:a32d2d13cdf3a8fbfa833bb71f38b1e2633dcf856b9561c61531162350a56712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.3 MB (583308951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c048bfbc05cd6141253502c09743fb3a41f7e0ac2a19399b3a17022044ed62`
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
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
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
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 27 Mar 2024 12:37:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
COPY dir:949b638e0bd71c40d1afd6181bc6d9f0fc46ee6d705abc4af012e6d15a18c62d in /usr/local/tomcat 
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
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
ENV XWIKI_VERSION=15.10.8
# Wed, 27 Mar 2024 12:37:20 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.8
# Wed, 27 Mar 2024 12:37:20 GMT
ENV XWIKI_DOWNLOAD_SHA256=20bfda3e0a694df904cab1f0291ff40761cf3461117654c5dc4860ba6397fd85
# Wed, 27 Mar 2024 12:37:20 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 27 Mar 2024 12:37:20 GMT
ENV POSTGRES_JDBC_VERSION=42.7.2
# Wed, 27 Mar 2024 12:37:20 GMT
ENV POSTGRES_JDBC_SHA256=0c244ac7d02cf89d8e29852eace6595d75bc4d78581b85b2768460081646a57b
# Wed, 27 Mar 2024 12:37:20 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.2
# Wed, 27 Mar 2024 12:37:20 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.2.jar
# Wed, 27 Mar 2024 12:37:20 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.2.jar
# Wed, 27 Mar 2024 12:37:20 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
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
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f037ef0398100188bd636ef3da1525cc5cc7f04347a802ecc28ba3240408631`  
		Last Modified: Thu, 25 Apr 2024 21:59:12 GMT  
		Size: 12.8 MB (12846901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a9d01cdbea836fa98a88c869097ca339c17dd29480bc1c936f937840fbde4d`  
		Last Modified: Thu, 25 Apr 2024 22:02:15 GMT  
		Size: 46.7 MB (46716123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e659b60df2e1030cfa0f2df9583f9aab145276e83a37490b983bbcfa9322fde3`  
		Last Modified: Thu, 25 Apr 2024 22:02:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f320f164b70019d3de719bb4a4b380f596330be1d584f5d935f80a4344b5b48`  
		Last Modified: Thu, 25 Apr 2024 22:02:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a446eed99bcbdadbc8fe6082bd87759257142f6d07e8e65462a2afa53b44ae8b`  
		Last Modified: Fri, 26 Apr 2024 02:12:04 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b36432c64716cedc0b26bc0ac1a29cc3cbb5de0c2e6cb309bd8d77b43c8dff`  
		Last Modified: Fri, 26 Apr 2024 02:14:58 GMT  
		Size: 12.4 MB (12430989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fb8413e5a27c1d4ad9f81efe9ecb3ed87a3243ee0e336f72f37d4dd928bc12`  
		Last Modified: Fri, 26 Apr 2024 02:14:57 GMT  
		Size: 455.4 KB (455391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a274afb70bd1a8e5276e866357759fb36d695550825e2aa970a162bd4fe46eef`  
		Last Modified: Fri, 26 Apr 2024 02:14:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a360008dc0bf4194895f648e9fdee6789f144886eb06aafe84143b718ac9d45d`  
		Last Modified: Fri, 26 Apr 2024 10:19:36 GMT  
		Size: 174.4 MB (174422103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd19e79a16821d109c3d20107ee590c4cceecb5fcd0a2e3f4faabec957fa1ed`  
		Last Modified: Fri, 26 Apr 2024 10:23:27 GMT  
		Size: 307.0 MB (307010831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdf3776bbffdce1066b8bcf806e3931a0d74cd9d25a67ffa5c2ec5b1ba82ec4`  
		Last Modified: Fri, 26 Apr 2024 10:23:20 GMT  
		Size: 1.0 MB (1011775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2fc1ab2a5583cb0ba36fa9ce8c82ec17be14fd4f0e1a9f411a2d2323abc625`  
		Last Modified: Fri, 26 Apr 2024 10:23:20 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6deb71cc68550ce448895d7388115e8053907408e8c13ff8f0b9e9ad7328911`  
		Last Modified: Fri, 26 Apr 2024 10:23:20 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27a3c75e0dbd99b3ea121ada38490f2dafd20c5934ccfb33331673cb1abe43d`  
		Last Modified: Fri, 26 Apr 2024 10:23:21 GMT  
		Size: 6.4 KB (6416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a03355f3268019ac45cdbd2629d0f8313cdc59a23d558d057f47d613d8f902a`  
		Last Modified: Fri, 26 Apr 2024 10:23:21 GMT  
		Size: 2.4 KB (2428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:e7c01cc11a0f24e66e04a184e3565421bd63023ed3785e67c9ab1a85a5261389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8945241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5d3050ac61a274f667ca57bef891b106688e8bdc8a7de7349575bbffecbe42`

```dockerfile
```

-	Layers:
	-	`sha256:714b9bf9815eba7914b3ecd221875e10630205995feb59de0f00bd822b492819`  
		Last Modified: Fri, 26 Apr 2024 10:23:20 GMT  
		Size: 8.9 MB (8905217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e617128b40181e48a20a6f8acc903d3ecfe73185a581d7afd8f23a658d8bf8e`  
		Last Modified: Fri, 26 Apr 2024 10:23:19 GMT  
		Size: 40.0 KB (40024 bytes)  
		MIME: application/vnd.in-toto+json
