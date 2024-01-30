## `xwiki:16-postgres-tomcat`

```console
$ docker pull xwiki@sha256:044c67ecd1469bec256eef3c053d25c075ff84e2396ea7ac659a6b27f839bf41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:16-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:22a3cebb12f129ec96fb0caea03d93ea0c1a1e16bd11f59fc19dffe72763ae46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.4 MB (597438624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cee7a2125e9007ade74f26377c861299708eb81ce218d600cdd2f65c48bb0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:14:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 07:14:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 07:14:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 07:16:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:35:35 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:37:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:37:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Thu, 25 Jan 2024 19:32:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 25 Jan 2024 19:32:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 26 Jan 2024 00:01:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 26 Jan 2024 00:01:16 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 00:01:17 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 26 Jan 2024 00:01:17 GMT
WORKDIR /usr/local/tomcat
# Fri, 26 Jan 2024 00:01:17 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 26 Jan 2024 00:01:17 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 26 Jan 2024 00:03:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 26 Jan 2024 00:03:51 GMT
ENV TOMCAT_MAJOR=9
# Fri, 26 Jan 2024 00:03:51 GMT
ENV TOMCAT_VERSION=9.0.85
# Fri, 26 Jan 2024 00:03:51 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Fri, 26 Jan 2024 00:03:51 GMT
COPY dir:1bee2d998c4b0025af1d580e21f991f073286c0707dae4c43e5c36179f29e522 in /usr/local/tomcat 
# Fri, 26 Jan 2024 00:03:56 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Jan 2024 00:03:57 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 26 Jan 2024 00:03:57 GMT
EXPOSE 8080
# Fri, 26 Jan 2024 00:03:58 GMT
ENTRYPOINT []
# Fri, 26 Jan 2024 00:03:58 GMT
CMD ["catalina.sh" "run"]
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 29 Jan 2024 16:20:26 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_VERSION=16.0.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.0.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=955c175d0ac0e7039eeafd8569d87ad8a7967092ad8d018decb80a42a7eb941f
# Mon, 29 Jan 2024 16:20:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
VOLUME [/usr/local/xwiki]
# Mon, 29 Jan 2024 16:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jan 2024 16:20:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c506251a0ae0b836353578bafa8d6aeb266158d3291ba4abbc2f5f8ccda6f742`  
		Last Modified: Wed, 17 Jan 2024 07:20:28 GMT  
		Size: 17.5 MB (17458145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8c673b95895c0efae2a8f0414597595f1d4f6b3e7973d0b99ee9b366580dd1`  
		Last Modified: Wed, 24 Jan 2024 20:48:16 GMT  
		Size: 47.2 MB (47163238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3fdfdbc1541d3276eaff7653137f8be176069196a72c68a0bf735dc617e7a2`  
		Last Modified: Wed, 24 Jan 2024 20:48:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4080cbbe938d7cadb00eda7a89a93f5878d7e968b4e8b23640b11c37ad69ca7b`  
		Last Modified: Thu, 25 Jan 2024 19:36:00 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd72bb2731222e3df918f8465ed5a79df3886adc040a05a285ded7dff6a47371`  
		Last Modified: Fri, 26 Jan 2024 00:20:27 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c699ef9dd39c15da10e119de70cf6a5b9666b608ef854d51e65d4ce9963c14`  
		Last Modified: Fri, 26 Jan 2024 00:23:24 GMT  
		Size: 12.4 MB (12404585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8839fa7b1c9b972fc827f3c8a382ef088c85c9399db36131991f81d7ec8db8d`  
		Last Modified: Fri, 26 Jan 2024 00:23:23 GMT  
		Size: 3.0 MB (2971682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f347f2b057e58d8fd8bf5baa47374306e8009931f8c5b44abb40a67d482e99f6`  
		Last Modified: Fri, 26 Jan 2024 00:23:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6443793148516d1388b1a3850c747c0043d948759a37ca44c7dda646e2a98ce6`  
		Last Modified: Mon, 29 Jan 2024 20:51:47 GMT  
		Size: 179.3 MB (179291559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a38d236b9e643ae57beb562fb754d2a58ffe4ebb81d833b36de50c37c7aa7b`  
		Last Modified: Mon, 29 Jan 2024 20:51:51 GMT  
		Size: 306.8 MB (306751605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679eca49ed00f0a5cf3bc2594a998e015ec5518e991a3d7fdc078e9fa04a56ab`  
		Last Modified: Mon, 29 Jan 2024 20:51:45 GMT  
		Size: 936.8 KB (936848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b6796b6ee805f5d19fd8cbf82d9f06e407d8d20e036db087b15d99670ea838`  
		Last Modified: Mon, 29 Jan 2024 20:51:45 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788695788eab0593012ec7d05595cba63c6491b1661b61c9e273af4c715b1071`  
		Last Modified: Mon, 29 Jan 2024 20:51:46 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0405bfc7e55c23a1bb46ee92c30a97c41ca86a18603b83f5484ba7d0e0c83e30`  
		Last Modified: Mon, 29 Jan 2024 20:51:46 GMT  
		Size: 6.4 KB (6423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f13b2ae1c77feef054d5790c69033f8a7587eda9b2a1bc7f3117b76c75e649e`  
		Last Modified: Mon, 29 Jan 2024 20:51:47 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:aab2d855b00bd01f0ed6e392ce87abb5e754a41209de843d8dbef933f3d417ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8084687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb91452b4b26bad6338e8b6dce0ba079f419d9ad0c71f99a86543c0cb4e7ad7`

```dockerfile
```

-	Layers:
	-	`sha256:a3702a7d93ca85ea35adb64b0fb786964652929e2b36ee677e5a4d88bd9f6ba6`  
		Last Modified: Mon, 29 Jan 2024 20:51:45 GMT  
		Size: 8.0 MB (8044582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8db922ac01b42035a121eb18a62636efcd7f76355733c69a3197b8280532d22d`  
		Last Modified: Mon, 29 Jan 2024 20:51:44 GMT  
		Size: 40.1 KB (40105 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:16-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:918b7c0dd29c6fdfed3143a7f49d782aeb14352e968055df467dde9c64fd0d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.2 MB (591154474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5085372cce621885ed2868cce897968cada66c86687a71dc58bcaf9bf0c5ebc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 06:57:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 06:57:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 06:57:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 17 Jan 2024 06:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Jan 2024 20:42:30 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:43:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 24 Jan 2024 20:43:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Thu, 25 Jan 2024 19:40:09 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 25 Jan 2024 19:40:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jan 2024 21:36:23 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 25 Jan 2024 21:36:23 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 21:36:24 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 25 Jan 2024 21:36:24 GMT
WORKDIR /usr/local/tomcat
# Thu, 25 Jan 2024 21:36:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jan 2024 21:36:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 25 Jan 2024 21:38:22 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 25 Jan 2024 21:38:22 GMT
ENV TOMCAT_MAJOR=9
# Thu, 25 Jan 2024 21:38:22 GMT
ENV TOMCAT_VERSION=9.0.85
# Thu, 25 Jan 2024 21:38:22 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Thu, 25 Jan 2024 21:38:22 GMT
COPY dir:fac5a5afc569d5adf17bf7792973d601dab2d975286add0d651627e7655eba99 in /usr/local/tomcat 
# Thu, 25 Jan 2024 21:38:26 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Jan 2024 21:38:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 25 Jan 2024 21:38:27 GMT
EXPOSE 8080
# Thu, 25 Jan 2024 21:38:27 GMT
ENTRYPOINT []
# Thu, 25 Jan 2024 21:38:28 GMT
CMD ["catalina.sh" "run"]
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 29 Jan 2024 16:20:26 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 29 Jan 2024 16:20:26 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_VERSION=16.0.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.0.0
# Mon, 29 Jan 2024 16:20:26 GMT
ENV XWIKI_DOWNLOAD_SHA256=955c175d0ac0e7039eeafd8569d87ad8a7967092ad8d018decb80a42a7eb941f
# Mon, 29 Jan 2024 16:20:26 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 29 Jan 2024 16:20:26 GMT
VOLUME [/usr/local/xwiki]
# Mon, 29 Jan 2024 16:20:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jan 2024 16:20:26 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6a2be6e4013cffcaae1614f67dca08e0c8d56b9d2da9051ae71c48b43a409a`  
		Last Modified: Wed, 17 Jan 2024 07:02:15 GMT  
		Size: 18.9 MB (18860096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c758562b2b3e61329aca1af5bb5fa0700d9b5f7cf4e68faa8e2235d15dccfd1a`  
		Last Modified: Wed, 24 Jan 2024 20:52:24 GMT  
		Size: 46.6 MB (46639344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12285b9bc0b75c36f5f58bb0cba487613706fb4718325baccbf6a0d2eb157be6`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c24226ebd43098c00c6e2715c22788dde6531777752b1ae35e81c95623edeae`  
		Last Modified: Thu, 25 Jan 2024 19:43:16 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291d1cfe01ca64a1f4b5ce99e3952e5e9f33883e28003c8338a45a3c4591524d`  
		Last Modified: Thu, 25 Jan 2024 21:51:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2409b92e56bb07b3bc3a5f86040c6de2c6d4bb8aff746ebd680937b280c4f9c3`  
		Last Modified: Thu, 25 Jan 2024 21:54:31 GMT  
		Size: 12.4 MB (12412630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fe23bd787b1047bcc544af859234e454dc5cb060fdb6efa3033727bf767ac7`  
		Last Modified: Thu, 25 Jan 2024 21:54:31 GMT  
		Size: 2.8 MB (2811661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6955886a62584457ae226ac9598bdb10f499bb2204bbd2c1999ffc6aa02377`  
		Last Modified: Thu, 25 Jan 2024 21:54:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04013638882503f074e601956bc02b6e38032fa5f6ce9443dcd94aeba04d96c`  
		Last Modified: Fri, 26 Jan 2024 17:49:46 GMT  
		Size: 174.3 MB (174328858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13af8bc2211a13905d3b99d12f6e898d71f9b36091379df8cfd3afdbcf617e78`  
		Last Modified: Mon, 29 Jan 2024 21:40:03 GMT  
		Size: 306.8 MB (306751580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4161759484d6be6aff44bd30d21dbc3540fbe22604c29444a488438d2bf7eb88`  
		Last Modified: Mon, 29 Jan 2024 21:39:57 GMT  
		Size: 936.8 KB (936849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20df3aebd8be58419e252fcb41b951938cc782821f76df2a58d5d6420415740`  
		Last Modified: Mon, 29 Jan 2024 21:39:56 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61794dca2a97971feca727cf667c1d6033cf5e9f580468abe02fa0d4efafab5`  
		Last Modified: Mon, 29 Jan 2024 21:39:56 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663f370caa6d4cbb7b174b6f50806b95e3cffd6cce810f531360ba0d0681b9a5`  
		Last Modified: Mon, 29 Jan 2024 21:39:58 GMT  
		Size: 6.4 KB (6424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47835a4879d656345392fac5eefc4bec7cacf35d8ee72c15eeb35fd3bfa14d4d`  
		Last Modified: Mon, 29 Jan 2024 21:39:58 GMT  
		Size: 2.4 KB (2428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:16-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:dc329a1448b53fd6263498fb91440f73f14094ecd588b6511b06ed2cf80dbaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8167261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30046f8c42add3e1a6ed6c89fdbe86edf9843ea3eda54970aba2c5713dd89b46`

```dockerfile
```

-	Layers:
	-	`sha256:6441d0feb14c6e147ad187b9c9f746879896c7dd110c43f193b4a96a7c69f6bc`  
		Last Modified: Mon, 29 Jan 2024 21:39:57 GMT  
		Size: 8.1 MB (8128608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:738e87e663e68099e764e9ff2c0551bcf6c81f4c9f01c4b78724c5701cda4b29`  
		Last Modified: Mon, 29 Jan 2024 21:39:56 GMT  
		Size: 38.7 KB (38653 bytes)  
		MIME: application/vnd.in-toto+json
