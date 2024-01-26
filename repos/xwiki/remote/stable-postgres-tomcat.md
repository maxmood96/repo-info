## `xwiki:stable-postgres-tomcat`

```console
$ docker pull xwiki@sha256:2d064939a8db074f8a984a2e3649a0e66d037272d069e157ec4ca4d5abcf5374
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:stable-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:5c9ded2605ecdaa07a24aca3972d34d0b30007ef533c76056dcc348a6639a05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.7 MB (597654162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b382fdb896404cf0bbf261086a2491baf3bf3116c743e0d5832d5ed64aa208`
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
# Wed, 17 Jan 2024 13:37:13 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 17 Jan 2024 13:37:13 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 17 Jan 2024 13:37:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 17 Jan 2024 13:37:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 17 Jan 2024 13:37:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 13:37:13 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 17 Jan 2024 13:37:13 GMT
WORKDIR /usr/local/tomcat
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 17 Jan 2024 13:37:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 17 Jan 2024 13:37:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_MAJOR=9
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_VERSION=9.0.85
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Wed, 17 Jan 2024 13:37:13 GMT
COPY dir:1bee2d998c4b0025af1d580e21f991f073286c0707dae4c43e5c36179f29e522 in /usr/local/tomcat 
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 17 Jan 2024 13:37:13 GMT
EXPOSE 8080
# Wed, 17 Jan 2024 13:37:13 GMT
ENTRYPOINT []
# Wed, 17 Jan 2024 13:37:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 17 Jan 2024 13:37:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_VERSION=15.10.5
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.5
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=3775334377ae7fb8bcf6a21e6eb099a8cfbea43044dc0716c01cb3b5117988a2
# Wed, 17 Jan 2024 13:37:13 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
VOLUME [/usr/local/xwiki]
# Wed, 17 Jan 2024 13:37:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jan 2024 13:37:13 GMT
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
	-	`sha256:c04e953936ac8d76ef880470fb114f9ec9e7f74eedec9abd4ca5d4d468ad3759`  
		Last Modified: Fri, 26 Jan 2024 00:50:14 GMT  
		Size: 179.3 MB (179291667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87428dd39c60570cd64711bae76cd736457ba761ad90105995364c87cfeb2e16`  
		Last Modified: Fri, 26 Jan 2024 00:50:15 GMT  
		Size: 307.0 MB (306967036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3b1d9027956c3ac6e4d506cc9ca2763e77cc5143239d98a62c0ebef652a681`  
		Last Modified: Fri, 26 Jan 2024 00:50:11 GMT  
		Size: 936.8 KB (936849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6277d11bdc15fab1949caa194de60fd19bd88eefd1929161cee08f0f234b06a3`  
		Last Modified: Fri, 26 Jan 2024 00:50:10 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c144eed4011c54628b7b62562c7f4fcaeecb91291eb02087a276d39a4293cf2`  
		Last Modified: Fri, 26 Jan 2024 00:50:11 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758aa78f6e9a41032c2d6d045ef3ca49b68f164af021c415da6700b425cc09c7`  
		Last Modified: Fri, 26 Jan 2024 00:50:13 GMT  
		Size: 6.4 KB (6415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039f88d12597ed489feace026d97ff0c5c04f2530cd29ca26197b4d184b72f0a`  
		Last Modified: Fri, 26 Jan 2024 00:50:12 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:a45b3877c89bea9aef766b05d1b79ba93eb42eb8e93e44362511b6c24d492ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8088985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a8c1a4516ed1f8a6e4f89299e2d4e77226702774c3eb25ed8c50727471b1af`

```dockerfile
```

-	Layers:
	-	`sha256:834d73c3da216959cb7f9046e10a7291693e056fb5412c29efec7186ec1eca39`  
		Last Modified: Fri, 26 Jan 2024 00:50:11 GMT  
		Size: 8.0 MB (8048240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f79b19f64207e3bc2ce05c1a535cd7c2c65207bfb9a550256a01c55b4172451`  
		Last Modified: Fri, 26 Jan 2024 00:50:10 GMT  
		Size: 40.7 KB (40745 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:stable-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:c93ad3d09d73fdea7ad24c46f7ddde278f42d706e405cfc8ad0ac17759602705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.0 MB (589015659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80de26c475d45d02cbc447b0940ecc26a5991f1fe08cb33a53577ce8848983ea`
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
# Wed, 17 Jan 2024 13:37:13 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Wed, 17 Jan 2024 13:37:13 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 17 Jan 2024 13:37:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 17 Jan 2024 13:37:13 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 17 Jan 2024 13:37:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 13:37:13 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 17 Jan 2024 13:37:13 GMT
WORKDIR /usr/local/tomcat
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 17 Jan 2024 13:37:13 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 17 Jan 2024 13:37:13 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_MAJOR=9
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_VERSION=9.0.85
# Wed, 17 Jan 2024 13:37:13 GMT
ENV TOMCAT_SHA512=06e239d15ff7b72017c1d0752ddb1be4651374f7c1391631ec5619f4981cb2911267bc6b044d6c71a2a74738f70d433b96418951439848121f1d874862ddd3de
# Wed, 17 Jan 2024 13:37:13 GMT
COPY dir:01149f705b11bd925d2257a4c044a76a91f790695e8b24d81462905489e4c34e in /usr/local/tomcat 
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 13:37:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 17 Jan 2024 13:37:13 GMT
EXPOSE 8080
# Wed, 17 Jan 2024 13:37:13 GMT
ENTRYPOINT []
# Wed, 17 Jan 2024 13:37:13 GMT
CMD ["catalina.sh" "run"]
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 17 Jan 2024 13:37:13 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 17 Jan 2024 13:37:13 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_VERSION=15.10.5
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.5
# Wed, 17 Jan 2024 13:37:13 GMT
ENV XWIKI_DOWNLOAD_SHA256=3775334377ae7fb8bcf6a21e6eb099a8cfbea43044dc0716c01cb3b5117988a2
# Wed, 17 Jan 2024 13:37:13 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
RUN cp /usr/share/java/postgresql-jdbc4.jar /usr/local/tomcat/webapps/ROOT/WEB-INF/lib/ # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 17 Jan 2024 13:37:13 GMT
VOLUME [/usr/local/xwiki]
# Wed, 17 Jan 2024 13:37:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jan 2024 13:37:13 GMT
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
	-	`sha256:30939200340c61d5e4fee7758c3c9ee34908388deb18ebd4162984289a9ac9a9`  
		Last Modified: Wed, 24 Jan 2024 20:52:19 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688f6e70b9d26932dbb7152c1323de603d3a2ead4ef95d8d213fc31cda78aa10`  
		Last Modified: Thu, 25 Jan 2024 01:31:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04170470340b531d039e82608ff775379eff1be33cfa80c4e981e937d2f31ba5`  
		Last Modified: Thu, 25 Jan 2024 01:34:29 GMT  
		Size: 12.4 MB (12412641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0745a0f06b29610f98021b910e00fd940179601abee8372581f2207c8bf61f77`  
		Last Modified: Thu, 25 Jan 2024 01:34:28 GMT  
		Size: 457.3 KB (457278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5495a30442c3a358dbd0aa3c88528038fe95612ab4b4fd29cb5870f8442eccd`  
		Last Modified: Thu, 25 Jan 2024 01:34:28 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14363b294dba44eb7965b53fb6b07bc74d6e697afff81b17b6c4973381102df`  
		Last Modified: Thu, 25 Jan 2024 05:32:36 GMT  
		Size: 174.3 MB (174328953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24431c3f8f2a525c6ce34eb030070e457f8e501546b46146a775691303417897`  
		Last Modified: Thu, 25 Jan 2024 05:32:39 GMT  
		Size: 307.0 MB (306967037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07e65776604d7d93b0406f36b1f357178296b8020274ee0d6fafa38adcf3c6f`  
		Last Modified: Thu, 25 Jan 2024 05:32:32 GMT  
		Size: 936.9 KB (936852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4735cfd48d0b333dac54343dcac7a7f4e819f8786da500994599106a04340d6b`  
		Last Modified: Thu, 25 Jan 2024 05:32:32 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2323e87d2a9f0b0b8f5305b942375b240934d5fe3f004f9170bdefbd13f8851b`  
		Last Modified: Thu, 25 Jan 2024 05:32:33 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddbe4a2188c8170d9d77e0030c1e835cce6318b322d4ea67c11a6634382ab70`  
		Last Modified: Thu, 25 Jan 2024 05:32:33 GMT  
		Size: 6.4 KB (6414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822ee76967f911afa916b98895bacf5776a70c02cb624473e01b730cb13100b6`  
		Last Modified: Thu, 25 Jan 2024 05:32:34 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:stable-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:3efb72af61f2c17c76eb0c21182604456a0ee091ec758d8508c53bfb2b870a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8169814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de60c8c19f86134859f289fb593b6a27bf23e21340cdc86340b0fb7cf7f5c4b`

```dockerfile
```

-	Layers:
	-	`sha256:c03f55ca7c6ba3eb41208ce235a0f9d1fa52ec47075487b4459304a8de0ef277`  
		Last Modified: Thu, 25 Jan 2024 05:32:32 GMT  
		Size: 8.1 MB (8130525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63d4ff1f6269356f679475204f478e5d0849dc2f4180dd7d6ee18bb10984543d`  
		Last Modified: Thu, 25 Jan 2024 05:32:31 GMT  
		Size: 39.3 KB (39289 bytes)  
		MIME: application/vnd.in-toto+json
