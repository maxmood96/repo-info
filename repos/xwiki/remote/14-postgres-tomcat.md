## `xwiki:14-postgres-tomcat`

```console
$ docker pull xwiki@sha256:49aef3644a651137f9fecf86985d872f59e59a8a1aae2b4d403453003fb18284
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:14-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:cb3bdc95df798116f125dc124176a3e5e74ac168e2510f459cdeec7e696de3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.3 MB (590339004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea6b4702120ce5af2fc925109fcd1e5246972479864c7969025c1188a3a05e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 13 Feb 2024 09:10:03 GMT
ARG RELEASE
# Tue, 13 Feb 2024 09:10:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 09:10:03 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 13 Feb 2024 09:10:03 GMT
WORKDIR /usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_MAJOR=9
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_VERSION=9.0.88
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Tue, 13 Feb 2024 09:10:03 GMT
COPY dir:008c1e737cb1d7c32c9c864d02bf0b16431c32c3c39b5b68188e5f3c48a90ec8 in /usr/local/tomcat 
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 13 Feb 2024 09:10:03 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT []
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["catalina.sh" "run"]
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 13 Feb 2024 09:10:03 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_VERSION=14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=72a634e2aeb085878dce2629a3e5e6136887d0c22712dcee5a284be8143135ea
# Tue, 13 Feb 2024 09:10:03 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
VOLUME [/usr/local/xwiki]
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
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
	-	`sha256:553a66c75a5a9104a7671a9f643b7741296b806a59c4dc2c9a2b4d2c5bb07d80`  
		Last Modified: Fri, 26 Apr 2024 03:53:20 GMT  
		Size: 179.4 MB (179369214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a064c84c72ead5af5945a798be20a6b4a87ec37fac9783ed2c135254a298cb0a`  
		Last Modified: Fri, 26 Apr 2024 03:53:22 GMT  
		Size: 306.5 MB (306538817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f840e234ed12bc81df8bfca2426722f253b75e255d6b36456a129e2d164f607`  
		Last Modified: Fri, 26 Apr 2024 03:53:17 GMT  
		Size: 936.8 KB (936847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01136aedc1a136fae1bdb3928624d4462dc47ca3316ecdd67347cedde4e5725`  
		Last Modified: Fri, 26 Apr 2024 03:53:17 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b1891e16be17f50818e74bc3ed921a1eaef9a7431a30edc8b62a43211021f4`  
		Last Modified: Fri, 26 Apr 2024 03:53:18 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64fc7c4dea3d8b5a3c5ff8cb175b2ac906dc1ccb3ebb67ed33673a779aec991`  
		Last Modified: Fri, 26 Apr 2024 03:53:18 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb6e6a9b027addc119ddfecc7f949857a7f5eca65010ff18318ab4530ac12e3`  
		Last Modified: Fri, 26 Apr 2024 03:53:19 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:14-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:b8c70b161d97fc4128bb5ca240507c22ac8d16410d9046058f3563d6df142701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8929334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01aaa9dad1d531d22d88137496596297a2c6da5f8417fc7bfdb9836d304373bd`

```dockerfile
```

-	Layers:
	-	`sha256:3c5150a62b833244c6be555c59cd669710d315f1c567feae8ad70990c16beadf`  
		Last Modified: Fri, 26 Apr 2024 03:53:17 GMT  
		Size: 8.9 MB (8890170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3a4cc003a3ead11945dcf35435cbac268e3260bafcb986dbcddaac9cf5e076d`  
		Last Modified: Fri, 26 Apr 2024 03:53:17 GMT  
		Size: 39.2 KB (39164 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:14-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:a98d93f6cac18db3d8404241293262ef2101f5d0681f0b1bd0ed3f3708b00722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.8 MB (582761715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6e9b9235dfecb4cddc5206a4dbdc8a92460a750a1939b13c0e7f0ac465e032`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Tue, 13 Feb 2024 09:10:03 GMT
ARG RELEASE
# Tue, 13 Feb 2024 09:10:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 09:10:03 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 09:10:03 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 13 Feb 2024 09:10:03 GMT
WORKDIR /usr/local/tomcat
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 13 Feb 2024 09:10:03 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_MAJOR=9
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_VERSION=9.0.88
# Tue, 13 Feb 2024 09:10:03 GMT
ENV TOMCAT_SHA512=b2668f50339afdd266dbdf3ff20a98632a5552910179eda272b65ea0b18be4bef8fa9988e3cfc77e4eae4b74ae1e7abe2483b0e427a07628ed50fed3a13eefb9
# Tue, 13 Feb 2024 09:10:03 GMT
COPY dir:949b638e0bd71c40d1afd6181bc6d9f0fc46ee6d705abc4af012e6d15a18c62d in /usr/local/tomcat 
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 09:10:03 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 13 Feb 2024 09:10:03 GMT
EXPOSE 8080
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT []
# Tue, 13 Feb 2024 09:10:03 GMT
CMD ["catalina.sh" "run"]
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Tue, 13 Feb 2024 09:10:03 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Tue, 13 Feb 2024 09:10:03 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_VERSION=14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/14.10.21
# Tue, 13 Feb 2024 09:10:03 GMT
ENV XWIKI_DOWNLOAD_SHA256=72a634e2aeb085878dce2629a3e5e6136887d0c22712dcee5a284be8143135ea
# Tue, 13 Feb 2024 09:10:03 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 13 Feb 2024 09:10:03 GMT
VOLUME [/usr/local/xwiki]
# Tue, 13 Feb 2024 09:10:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 09:10:03 GMT
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
	-	`sha256:11224cecaaf754fac2cb2352ba2979e0c39ab26169bd9c65d2a7073ed54d1863`  
		Last Modified: Fri, 26 Apr 2024 10:28:40 GMT  
		Size: 306.5 MB (306538789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d1258307c944476df6d13fcf10f26d177d855a40c36664f322273329caec56`  
		Last Modified: Fri, 26 Apr 2024 10:28:33 GMT  
		Size: 936.9 KB (936854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1b5350ebde6f44f3ec69c7343a01f1b815ff608a6333f4dfcb6c53b34c6484`  
		Last Modified: Fri, 26 Apr 2024 10:28:32 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7e273a4695f05da3ffe96cb4b58f9064d08112ca18a23fbac8eece59e2df86`  
		Last Modified: Fri, 26 Apr 2024 10:28:32 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e1c2ca57991535868c6503eb63f579d6d6688719b839858c671d1447458ed7`  
		Last Modified: Fri, 26 Apr 2024 10:28:33 GMT  
		Size: 6.1 KB (6137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5f445866e98c5dd1dae98388b968e3633833abc5c698bd1ddd7351989ad64a`  
		Last Modified: Fri, 26 Apr 2024 10:28:33 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:14-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:5782ea5539400b1386a036790a47d773595876a5d23c378585e8ceb7c563ab45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8928382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f189003af182dda273d43494e8b580cb5d30597e6262210f38add004dc0b35d2`

```dockerfile
```

-	Layers:
	-	`sha256:87c9c3b206c4528c05faa11cf922196d0626e76ed83b84cdb33c2a03db529508`  
		Last Modified: Fri, 26 Apr 2024 10:28:33 GMT  
		Size: 8.9 MB (8890673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d344b0aa1ec114c85de9ea33f95f63db99a394e328eba61bd741510746520add`  
		Last Modified: Fri, 26 Apr 2024 10:28:32 GMT  
		Size: 37.7 KB (37709 bytes)  
		MIME: application/vnd.in-toto+json
