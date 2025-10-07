## `xwiki:lts-mariadb-tomcat`

```console
$ docker pull xwiki@sha256:eed85a8bb8428d2f4ec9b7672254cc81290c177c4988423de6c5f91a1a4626d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:lts-mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:5051c994f4dd79e70b7c5566546638bd47bc8f180c17da7743afaddc40b982fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.5 MB (625540973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f35035277838a72abc5df5e68488f5fe60f1bf997794aa453ea2112a476b52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Oct 2025 14:43:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Oct 2025 14:43:49 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Oct 2025 14:43:49 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Oct 2025 14:43:49 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Oct 2025 14:43:49 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Oct 2025 14:43:49 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Oct 2025 14:43:49 GMT
ENV TOMCAT_VERSION=9.0.110
# Fri, 03 Oct 2025 14:43:49 GMT
ENV TOMCAT_SHA512=5783b88b4bb2fc1dbd10be072deccec0ec96c35b8de09d65b96a8f846e84f4655ddfa43a22e58ace6bf02a653d80629039c733c4b1ff628fa9501048318537f0
# Fri, 03 Oct 2025 14:43:49 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Oct 2025 14:43:49 GMT
ENTRYPOINT []
# Fri, 03 Oct 2025 14:43:49 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Oct 2025 14:43:49 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
ENV XWIKI_VERSION=16.10.12
# Fri, 03 Oct 2025 14:43:49 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.12
# Fri, 03 Oct 2025 14:43:49 GMT
ENV XWIKI_DOWNLOAD_SHA256=2a0a3f6eb12177b87d2b15e6fc8b955d171a36c6b9e6acfb32f8c4b980652846
# Fri, 03 Oct 2025 14:43:49 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_VERSION=3.5.6
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_SHA256=a129703efd7b0f334564d46753de999f09b3a361489a2eb647e6020390981cc9
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.6
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.6.jar
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.6.jar
# Fri, 03 Oct 2025 14:43:49 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Oct 2025 14:43:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 14:43:49 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2569d95ac3cad1e081eb0cadd06ec41b066fe85885c6d0c029833d09bdeb785`  
		Last Modified: Thu, 02 Oct 2025 05:02:06 GMT  
		Size: 19.4 MB (19377145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99162d145ed15eaef231c1152439075a98c43e224a7d3378dd3569f8132a5557`  
		Last Modified: Thu, 02 Oct 2025 05:02:25 GMT  
		Size: 53.0 MB (52968889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b650b1a0903a78b1352f908bc1ab1a88148d74932ae66ac697b9c7fcfb1ce17`  
		Last Modified: Thu, 02 Oct 2025 05:02:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0474e363db68b6324a1fcffcfbfac1b9084bb1c4e2bfb0df7557e9c92fc7bc5a`  
		Last Modified: Thu, 02 Oct 2025 05:02:09 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fb40671422160c013c637074f14e6c967c6f3d785ef72bd37cce9469ad4d6e`  
		Last Modified: Tue, 07 Oct 2025 00:11:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56afccf4451b3bccf50e570e88bf19d4fe55d2cb2e6a99db124f2d48d4d1a8ba`  
		Last Modified: Tue, 07 Oct 2025 00:11:07 GMT  
		Size: 13.7 MB (13726712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d02b3d47134573cb2270333e1a5892856dae7c4d35e20274d98a931f2da547`  
		Last Modified: Tue, 07 Oct 2025 00:11:06 GMT  
		Size: 224.8 KB (224760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dc86e0ebde5bdb045b9db8e501d5b2e8e4d9e4b3edf8128d1430416a0d636e`  
		Last Modified: Tue, 07 Oct 2025 04:00:52 GMT  
		Size: 191.2 MB (191181263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc7f4e55da6ddc3be613c7ac2410314c7124bbffcc2b7b7bdc32ad18c660704`  
		Last Modified: Tue, 07 Oct 2025 03:33:07 GMT  
		Size: 317.6 MB (317618854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341df925f95dad47c214ca7bedb955b95d9f9a91eaa693736a5ce2d806aa5d4c`  
		Last Modified: Tue, 07 Oct 2025 01:16:01 GMT  
		Size: 705.0 KB (704955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32589d83b4ac0f5a6dc2249182b78b601a47d9c3951d78fe0b1f8cfe954fe2b`  
		Last Modified: Tue, 07 Oct 2025 01:16:01 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b1c8e772b4e70fa15eb66166acc73e031a3bf9c71dc47297b533f42d89a82d`  
		Last Modified: Tue, 07 Oct 2025 01:16:01 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6196c2d309a5704c3c75e8e562cb043a5ca1d53cb4a04e5ff875a9317f7f5b`  
		Last Modified: Tue, 07 Oct 2025 01:16:01 GMT  
		Size: 6.6 KB (6621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132b8d54a44a460a5047f5f7e598a228812eb5667d9c44fe0d757cecce0884ed`  
		Last Modified: Tue, 07 Oct 2025 01:16:03 GMT  
		Size: 2.5 KB (2473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:bae55f05eed8299e71ec25ef36f30442899edd7412d892745d87a3604ffefa14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9150025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de69a3b19c3e7534b18de1d94299ceac77390b2cb8430f0f1f00f35195016ab6`

```dockerfile
```

-	Layers:
	-	`sha256:0263233261bb07b58897dd0a35b0212a5ba72e89281df104880ede7755123095`  
		Last Modified: Tue, 07 Oct 2025 03:07:34 GMT  
		Size: 9.1 MB (9109535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af6e88adc6ff8b0322fa5b820bfa536aef3085526d2a5bcd7ad771940d730a33`  
		Last Modified: Tue, 07 Oct 2025 03:07:35 GMT  
		Size: 40.5 KB (40490 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:lts-mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:365425b8d0fe99ccb3098e7877d68a25709c63e81ee7dee1d8a3d0e60246f5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.4 MB (621366563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf36eaac79079058087b7f510362a233909d0239ef1040c7125b221e85295c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ARG RELEASE
# Fri, 01 Aug 2025 11:04:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 01 Aug 2025 11:04:34 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 03 Oct 2025 14:43:49 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 03 Oct 2025 14:43:49 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Oct 2025 14:43:49 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
WORKDIR /usr/local/tomcat
# Fri, 03 Oct 2025 14:43:49 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 03 Oct 2025 14:43:49 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 03 Oct 2025 14:43:49 GMT
ENV TOMCAT_MAJOR=9
# Fri, 03 Oct 2025 14:43:49 GMT
ENV TOMCAT_VERSION=9.0.110
# Fri, 03 Oct 2025 14:43:49 GMT
ENV TOMCAT_SHA512=5783b88b4bb2fc1dbd10be072deccec0ec96c35b8de09d65b96a8f846e84f4655ddfa43a22e58ace6bf02a653d80629039c733c4b1ff628fa9501048318537f0
# Fri, 03 Oct 2025 14:43:49 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 03 Oct 2025 14:43:49 GMT
ENTRYPOINT []
# Fri, 03 Oct 2025 14:43:49 GMT
CMD ["catalina.sh" "run"]
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 03 Oct 2025 14:43:49 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 03 Oct 2025 14:43:49 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
ENV XWIKI_VERSION=16.10.12
# Fri, 03 Oct 2025 14:43:49 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/16.10.12
# Fri, 03 Oct 2025 14:43:49 GMT
ENV XWIKI_DOWNLOAD_SHA256=2a0a3f6eb12177b87d2b15e6fc8b955d171a36c6b9e6acfb32f8c4b980652846
# Fri, 03 Oct 2025 14:43:49 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_VERSION=3.5.6
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_SHA256=a129703efd7b0f334564d46753de999f09b3a361489a2eb647e6020390981cc9
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.6
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.6.jar
# Fri, 03 Oct 2025 14:43:49 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.6.jar
# Fri, 03 Oct 2025 14:43:49 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 03 Oct 2025 14:43:49 GMT
VOLUME [/usr/local/xwiki]
# Fri, 03 Oct 2025 14:43:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 14:43:49 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419aaa52607f6ef7a03a295c57fe451241093bacec0b8cbd975e95351624d644`  
		Last Modified: Thu, 02 Oct 2025 01:17:02 GMT  
		Size: 19.2 MB (19206364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6e0e7ba59c46747fca6b4371f060d57be2b74f88c20ab65b86093a904721df`  
		Last Modified: Thu, 02 Oct 2025 01:18:05 GMT  
		Size: 52.1 MB (52148465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f043a2b7ac7283aed8cbd3c5f15d2ea54efec6b3caaee6c9aa3604381c49e35`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8638ac656cf58a686e913d6ff24b9568968c949eb31951f04bdfa835ef450334`  
		Last Modified: Thu, 02 Oct 2025 01:17:59 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d950d3655f723c74f7109f2ae096e011e67cc0739d0865b06550b30f5de8b1`  
		Last Modified: Tue, 07 Oct 2025 00:11:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebcb7575817ebfeef1ffdac3d240a6daf2409446b3af4668d40b6d81e6deaec`  
		Last Modified: Tue, 07 Oct 2025 00:11:00 GMT  
		Size: 13.7 MB (13735579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be71b2b3a8457f6888a885f0ca3acdcb141ca45fc072e93151bfd6387eb15752`  
		Last Modified: Tue, 07 Oct 2025 00:11:00 GMT  
		Size: 225.2 KB (225236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb5412acfb53336b59ad72f153bf4431df654061d3687578f2bfb2eccc25a27`  
		Last Modified: Tue, 07 Oct 2025 01:12:53 GMT  
		Size: 188.9 MB (188850268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f61d0b938189ecdd3e705254a66afc7c4bb2d7f1cff6759d59fa83636853ec`  
		Last Modified: Tue, 07 Oct 2025 02:08:52 GMT  
		Size: 317.6 MB (317618721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199aca729053dc71be28776fb0628eef632c5f34aabfd63644f72ca5752feea3`  
		Last Modified: Tue, 07 Oct 2025 01:13:03 GMT  
		Size: 705.0 KB (704957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e99bbfd4d431a098d7eda1e5e5962fdc0d83dd7819e60e7b91d266e12f444c`  
		Last Modified: Tue, 07 Oct 2025 01:13:03 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb9649e7bb8eb56a24762b23d6f58dadde6e6b6aba9bc99184aa9b5da784eac`  
		Last Modified: Tue, 07 Oct 2025 01:13:03 GMT  
		Size: 2.3 KB (2311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed67ca9edb4be358ca974649e823435b40d210dd47197db3ef52c865fb72545`  
		Last Modified: Tue, 07 Oct 2025 01:13:03 GMT  
		Size: 6.6 KB (6624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3fd0f8456fc817454e5d69a7ff05238e271ce32e14851eb2cf33e152fa6317`  
		Last Modified: Tue, 07 Oct 2025 01:13:03 GMT  
		Size: 2.5 KB (2477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:lts-mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:5772ecdb41cedd6e161a5cd97d3bc6676ef012f47f542d51bd4c0c93903a8e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9150927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7133ced5c66311155205cf509e7de66c4ad5fe3aaa241caac6bc04a06656f27d`

```dockerfile
```

-	Layers:
	-	`sha256:343e383a301d0526a2fc1a5601b8b8e33eb18e70189d3d4383fc9eb0243ef440`  
		Last Modified: Tue, 07 Oct 2025 03:07:41 GMT  
		Size: 9.1 MB (9110276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec6697f9ee0aa605db91919eef01216cd78e031c2fcb4b01655bba40a7d1339e`  
		Last Modified: Tue, 07 Oct 2025 03:07:41 GMT  
		Size: 40.7 KB (40651 bytes)  
		MIME: application/vnd.in-toto+json
