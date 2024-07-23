## `xwiki:lts-postgres`

```console
$ docker pull xwiki@sha256:2aec8976879ce34697b39d019ae0ad82451e2f41b260d94ffc3494e70cec8b2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-postgres` - linux; amd64

```console
$ docker pull xwiki@sha256:4471dcae31a21fbe273c5544f6b6d74bc9302c7a5633f3c6693b63a8fc1d442b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.6 MB (590629331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120a6eec7f6dff8554fe00a00015cd3b1b8b5ba6ccf8bc1634a007a059d2b2f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 27 Jun 2024 13:08:28 GMT
ARG RELEASE
# Thu, 27 Jun 2024 13:08:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 13:08:28 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 13:08:28 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 13:08:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 13:08:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 13:08:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='0e8088d7a3a7496faba7ac8787db09dc0264c2bc6f568ea8024fd775a783e13c';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='9dfe4c56463690ae67d22268980d8861eb46b907d7914f8f2e6fc7b25778c8ec';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='f093094abe0cb2bb5a255d8180810030321073520541f289926c4682eda76136';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='2759c48e1e56117871b04c851af18b92b6992cf67590f602949b96c3cff15c73';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='cb1a3857d10e9353862761ce3c6b45573a736ea95cea44bc02dc3a703e57255a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 27 Jun 2024 13:08:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Jun 2024 13:08:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 13:08:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jun 2024 13:08:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jun 2024 13:08:28 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_MAJOR=9
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_VERSION=9.0.91
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Thu, 27 Jun 2024 13:08:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT []
# Thu, 27 Jun 2024 13:08:28 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 27 Jun 2024 13:08:28 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_VERSION=15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=b69de0d6ae0d2cdd10efcd1913065f750de62b5147f553bc6772e42cc66e2e2c
# Thu, 27 Jun 2024 13:08:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Thu, 27 Jun 2024 13:08:28 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
VOLUME [/usr/local/xwiki]
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jun 2024 13:08:28 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf881a8778e586cc575307291b6a464d2b9094a7f860e441327a33b60571d26`  
		Last Modified: Tue, 23 Jul 2024 01:08:49 GMT  
		Size: 47.3 MB (47280164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342b032acb4f06f0d04884742ab170848be23d22f65c5cad2ae083c63f87a724`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4e485fb305a744f5c14c75e3aca62600470492c3c43ad509e511f8c2b7dce`  
		Last Modified: Tue, 23 Jul 2024 01:08:43 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccc9be229b8d310bdbc0c56be88a51fcc3fef5ae00018e0fd6bf858815b580f`  
		Last Modified: Tue, 23 Jul 2024 03:03:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53291f71fa4fa224a3226b40732d633057bff07aa88b9abc039444330c5ae954`  
		Last Modified: Tue, 23 Jul 2024 03:03:43 GMT  
		Size: 12.4 MB (12442361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88315142089f582df33ea249461d313af8d5e3fc61ea8bd3f487cd8915c3aa3d`  
		Last Modified: Tue, 23 Jul 2024 03:03:43 GMT  
		Size: 217.8 KB (217820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34425331c01b78822150460c77b11db4b75d1a253a733199c02c7e728e0445d`  
		Last Modified: Tue, 23 Jul 2024 06:13:47 GMT  
		Size: 179.4 MB (179383450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b29ee3aeeebe21078fe38518ca27434e0729327faee1b5660c378852b379ec`  
		Last Modified: Tue, 23 Jul 2024 06:13:51 GMT  
		Size: 307.0 MB (306968161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5d3aac773466bd24b96da983b1b67a377e4a44f1e79e06508b56a217dfa8a7`  
		Last Modified: Tue, 23 Jul 2024 06:13:43 GMT  
		Size: 1.0 MB (1011976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70510a2efa6bcf8ed4bcfe2091a84f69c84f0cc491b9344b5971012f588692c6`  
		Last Modified: Tue, 23 Jul 2024 06:13:43 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b598276a872d79b52cc112543600a4ac435cb2133d5a340fa5f0be51e912b8`  
		Last Modified: Tue, 23 Jul 2024 06:13:44 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4cb93669575f28705dbf71793cf75646036691a8b094aeb7fcd293125b24ac`  
		Last Modified: Tue, 23 Jul 2024 06:13:44 GMT  
		Size: 6.4 KB (6432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3d9979267e7ceaf75803a2f3fe04e8b439c58b276b363555120a4a962991d9`  
		Last Modified: Tue, 23 Jul 2024 06:13:45 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:8ac04f8640b57693a822ed93d043f482b1492a4f235f5ced1d1f9b3eb5356d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9116798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf332194e38fc13b5fbe73fd934abfda45116e4e984922d886f68f124e32333a`

```dockerfile
```

-	Layers:
	-	`sha256:3d88f4f438f772ce5164f41f2fd0b562bbb0f529f02a5b176cae1773b8f7189d`  
		Last Modified: Tue, 23 Jul 2024 06:13:43 GMT  
		Size: 9.1 MB (9075723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38bccb86cd3df6e8c27f9afb87442caf8e51606736fff1c2b1fa0918610f8ec4`  
		Last Modified: Tue, 23 Jul 2024 06:13:42 GMT  
		Size: 41.1 KB (41075 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-postgres` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:17161ebcad45de7265b887e680d08f79081fd7aea22efe6923e4cc8fbb6231ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.0 MB (583013669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f143b60cd3d027d69ed962fd6889ba13de0b649a086833e3e35d720310f682e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Thu, 27 Jun 2024 13:08:28 GMT
ARG RELEASE
# Thu, 27 Jun 2024 13:08:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 13:08:28 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 13:08:28 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        armhf|arm)          ESUM='2e06401aa3aa7a825d73a6af8e9462449b1a86e7705b793dc8ec90423b602ee2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 27 Jun 2024 13:08:28 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 27 Jun 2024 13:08:28 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 13:08:28 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
WORKDIR /usr/local/tomcat
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jun 2024 13:08:28 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 27 Jun 2024 13:08:28 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_MAJOR=9
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_VERSION=9.0.91
# Thu, 27 Jun 2024 13:08:28 GMT
ENV TOMCAT_SHA512=b22054c9141782232a693765d23d944f0f50774af17dd8968331e020b425e71459b5877a7ba8c2121246a5ce47e6b6a31c3f4215ef133e942da45b49cb534948
# Thu, 27 Jun 2024 13:08:28 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
EXPOSE map[8080/tcp:{}]
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT []
# Thu, 27 Jun 2024 13:08:28 GMT
CMD ["catalina.sh" "run"]
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Thu, 27 Jun 2024 13:08:28 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Thu, 27 Jun 2024 13:08:28 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps     libpostgresql-jdbc-java &&   rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_VERSION=15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/15.10.11
# Thu, 27 Jun 2024 13:08:28 GMT
ENV XWIKI_DOWNLOAD_SHA256=b69de0d6ae0d2cdd10efcd1913065f750de62b5147f553bc6772e42cc66e2e2c
# Thu, 27 Jun 2024 13:08:28 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_VERSION=42.7.3
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_SHA256=a2644cbfba1baa145ff7e8c8ef582a6eed7a7ec4ca792f7f054122bdec756268
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.3
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.3.jar
# Thu, 27 Jun 2024 13:08:28 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.3.jar
# Thu, 27 Jun 2024 13:08:28 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 13:08:28 GMT
VOLUME [/usr/local/xwiki]
# Thu, 27 Jun 2024 13:08:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Jun 2024 13:08:28 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bcba8e4ae31e5690436469ea0cbe8b0380eac630b99dd454816782517fe3ed`  
		Last Modified: Tue, 02 Jul 2024 04:35:53 GMT  
		Size: 46.7 MB (46716436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1bee0a5ee9a69e90c6a18762b53d2f3872890196bef46a24a14c7e8cd7efe8`  
		Last Modified: Tue, 02 Jul 2024 04:35:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e2fe8e514adf85f13f482dc533f6a54a31ca0f7e9f593af808c0a45b5eb036`  
		Last Modified: Tue, 02 Jul 2024 04:35:48 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355ef1e0f99365b94e982dcf733d5b5e6077c1c7ae3dd76c1cfe2fad8ac5dc9e`  
		Last Modified: Wed, 03 Jul 2024 08:28:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13464cb8a587e80daafd7e18cadae4063525294e0c93353099f32e6fc605ca4f`  
		Last Modified: Tue, 09 Jul 2024 00:04:31 GMT  
		Size: 12.4 MB (12448796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88c61d4f4e1df824a1cdb3e0065815aa48c0e6e12aea98c596c5218ac2fd1fa`  
		Last Modified: Tue, 09 Jul 2024 00:04:31 GMT  
		Size: 216.8 KB (216770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2c57fe73ff4e80ce3b7a14e5c19c69996335ce2b9df512a3f1a1ebeaa32f6b`  
		Last Modified: Tue, 09 Jul 2024 01:41:11 GMT  
		Size: 174.4 MB (174423715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df9859026cfb46d98fc4ff8390ffef9754b32f25c35f879693e0dbb905515c2`  
		Last Modified: Tue, 09 Jul 2024 01:44:38 GMT  
		Size: 307.0 MB (306968123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3073e06bf318b3403367ceb00bcda3902672db55f9c12087c71c1646715647`  
		Last Modified: Tue, 09 Jul 2024 01:44:31 GMT  
		Size: 1.0 MB (1011973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d24d0567c880dec4427bc133ba1c7b1ff528c033c83159a73b7e8d0e7c7d016`  
		Last Modified: Tue, 09 Jul 2024 01:44:31 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add408fbe01310d34553d6591aa006269dc950d2cd091e72b279a7a6e6fd8f57`  
		Last Modified: Tue, 09 Jul 2024 01:44:31 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa33723ce2effa0a61ffbf411b6d92b8bbf29b73964db7cce6b47bc4f6638ff`  
		Last Modified: Tue, 09 Jul 2024 01:44:32 GMT  
		Size: 6.4 KB (6430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fecc0d66e4dfdc4e4d3bbeba84a2450aa75e753df8acdf5513cd3632978d7a2`  
		Last Modified: Tue, 09 Jul 2024 01:44:32 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-postgres` - unknown; unknown

```console
$ docker pull xwiki@sha256:2b4b39b542e4a73be15b591596f8435f531f051f187c7fdba865ed9ec3fcc2cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8943301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4655171b9f59490969bb2d26852b67b8ee5c5d9f09b62572596a77849f1cf63`

```dockerfile
```

-	Layers:
	-	`sha256:df2af1a1cb7290b84d05acc0107d882c9796115cf9cafc71dd8563bd13683fc8`  
		Last Modified: Tue, 09 Jul 2024 01:44:31 GMT  
		Size: 8.9 MB (8901597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:827b19be2ceacc806397fa29a9f61bff183c06d1915e486009294b9a31221730`  
		Last Modified: Tue, 09 Jul 2024 01:44:31 GMT  
		Size: 41.7 KB (41704 bytes)  
		MIME: application/vnd.in-toto+json
