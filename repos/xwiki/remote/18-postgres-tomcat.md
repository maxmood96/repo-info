## `xwiki:18-postgres-tomcat`

```console
$ docker pull xwiki@sha256:e8569199e2d2b736d1ba92694e9114dd63ed0d227a758e635785b3c048b0402b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:18-postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:576aa3529740be91712990b72071a50e293bc123741ea9a705a9c9b318cd1e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.2 MB (651225075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99949e4505725f767040a5f6b9b7a4cc5866a962314fdf309a34eabb216a3f03`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Fri, 08 May 2026 00:00:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:00:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:00:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:00:33 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:00:33 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:00:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='f3d8843c5a1b77ded3353e0df85d803d84b9faa5ece20673564e7c47fc4591d9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:00:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:00:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:00:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:38:01 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 23:38:01 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:38:01 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 23:38:01 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 23:38:01 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:38:01 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:38:01 GMT
ENV TOMCAT_MAJOR=10
# Tue, 12 May 2026 23:38:01 GMT
ENV TOMCAT_VERSION=10.1.55
# Tue, 12 May 2026 23:38:01 GMT
ENV TOMCAT_SHA512=f36af12391a277e5c3a802a8e1a2a1e4354cd461b547d2e1a33ac0ab88d707d3fb2591e034a17b7d3a6b965a4c977a97dbf29bb81a3867e85aeec3d8d189e22e
# Tue, 12 May 2026 23:38:01 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 23:38:05 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 23:38:06 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 23:38:06 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 23:38:06 GMT
ENTRYPOINT []
# Tue, 12 May 2026 23:38:06 GMT
CMD ["catalina.sh" "run"]
# Wed, 13 May 2026 00:14:22 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 13 May 2026 00:14:22 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 13 May 2026 00:14:22 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 13 May 2026 00:14:22 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 13 May 2026 00:14:22 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 13 May 2026 00:14:22 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 13 May 2026 00:14:22 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 00:14:22 GMT
ENV XWIKI_VERSION=18.3.0
# Wed, 13 May 2026 00:14:22 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.3.0
# Wed, 13 May 2026 00:14:22 GMT
ENV XWIKI_DOWNLOAD_SHA256=3a0594e4260bc832c8a42f9ea1d6f47d9da7c8ffb7bbe65b7c363e7e8308051a
# Wed, 13 May 2026 00:14:43 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 13 May 2026 00:14:43 GMT
ENV POSTGRES_JDBC_VERSION=42.7.10
# Wed, 13 May 2026 00:14:43 GMT
ENV POSTGRES_JDBC_SHA256=cab1cd67cfa25c25de4348e532298028288a877ba01c77d1619fe45416193387
# Wed, 13 May 2026 00:14:43 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.10
# Wed, 13 May 2026 00:14:43 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.10.jar
# Wed, 13 May 2026 00:14:43 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.10.jar
# Wed, 13 May 2026 00:14:43 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 13 May 2026 00:14:44 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 13 May 2026 00:14:44 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 13 May 2026 00:14:44 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 13 May 2026 00:14:44 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 13 May 2026 00:14:44 GMT
VOLUME [/usr/local/xwiki]
# Wed, 13 May 2026 00:14:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 00:14:44 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddba20b57055d40e461149d994ec0cb413acb11933063fb067bef26d04f19e5`  
		Last Modified: Fri, 08 May 2026 00:00:50 GMT  
		Size: 17.0 MB (16984109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86efa879232eb8f00c346e19b20f3574da2aae8c03b7832a9790ff45be526d2d`  
		Last Modified: Fri, 08 May 2026 00:00:51 GMT  
		Size: 53.1 MB (53123205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a6536d8fe0f97af211732b2a2398d9c3fa5f0cceaaaec494787b95b8e710ce`  
		Last Modified: Fri, 08 May 2026 00:00:49 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b19a677a848917cae6512f190c51a8df85b683b2d4e390d33f8d71f637bb734`  
		Last Modified: Fri, 08 May 2026 00:00:49 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a298a176ea43fc8b3f9a3ff8e5995270b38de11b4bbfa28e14d2bbce0815285`  
		Last Modified: Tue, 12 May 2026 23:38:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a19875ad1cc202378242948ab997dd2d8f720e8de8445955ecdb6551a244410`  
		Last Modified: Tue, 12 May 2026 23:38:14 GMT  
		Size: 14.3 MB (14311217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20fb52c4c87467e26e3b535e06d71dbd3957ae03200794c46ed3c1ea49fe954`  
		Last Modified: Tue, 12 May 2026 23:38:14 GMT  
		Size: 224.7 KB (224738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1a475890f631667eca4b2fe9b46a337b94741cca2b970e2546188f173bd349`  
		Last Modified: Wed, 13 May 2026 00:15:28 GMT  
		Size: 191.2 MB (191245007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a292f253e886daed7705ec45eeee94ec3802714635e458c6a435c0b4a0758a`  
		Last Modified: Wed, 13 May 2026 00:15:31 GMT  
		Size: 344.5 MB (344522336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003300b10d0804433daa0014b33fea6f4939200e52ed15c8d24d6ee3a2c2bfe0`  
		Last Modified: Wed, 13 May 2026 00:15:20 GMT  
		Size: 1.1 MB (1061593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a17eedcab2b4e96a668f2230a34088615f43feb4f39f0abb2aab81bdd62a23c`  
		Last Modified: Wed, 13 May 2026 00:15:20 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4349e0f2d1c3393ebc224ed682060dfc3fd02e4204499f65dc10254f8b519c50`  
		Last Modified: Wed, 13 May 2026 00:15:21 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4b5bcbf8d639b7bb8307c119b0e86be211fd9e0df21ea2ece0492ae7066039`  
		Last Modified: Wed, 13 May 2026 00:15:22 GMT  
		Size: 11.0 KB (11009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345a03615a739ba57d4454ff32f751538ff75021a161200dcf593986eec4e4e4`  
		Last Modified: Wed, 13 May 2026 00:15:23 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:18-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:4b33b3f2d7a02628684222c6551d542c221cceecb876c5fc8b9c78ece8f5ae9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d6c374b078cfa000782158b2884e5cc0b26da8e77d235cf49caedfe9062d33`

```dockerfile
```

-	Layers:
	-	`sha256:700d94b39bf38e41856838dfc461bafd928fe25f34135c985ace2b4522c21107`  
		Last Modified: Wed, 13 May 2026 00:15:20 GMT  
		Size: 9.2 MB (9198919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5463f756e5ce8c0e643bfa820ca2f217e8062cc314e57a4fd893a4ec8cfa92c`  
		Last Modified: Wed, 13 May 2026 00:15:20 GMT  
		Size: 40.8 KB (40753 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:18-postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:fd444eb7274e1daf52da8d938a1ce4bdf6b2d2f24c586e2487d532b64e5defea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.2 MB (647247990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47e72ef2f9c08464aecc22ee06d13ae97a47e285ac27466a7ae377f97147904`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Fri, 08 May 2026 00:00:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:00:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:00:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:00:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:00:03 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 00:00:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e5038aae3ca9ff670bc696496b0728dbd23d280026bad30291cb919221ecfdcb';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        arm64)          ESUM='fa23d9d9945053e67bcc7638410eabf1e17a7672c7c95a24f70cd08b8407d36e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64el)          ESUM='fefb53c4bd687e7a91a9a9809ec80e0862e829cd20513839ad1a9988ddc89482';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        riscv64)          ESUM='f3d8843c5a1b77ded3353e0df85d803d84b9faa5ece20673564e7c47fc4591d9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='45736e9e14d52619133900a077b4f72d1ebee0fd0bb053da0bca9dce9fc4d916';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:00:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:00:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:00:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:37:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 12 May 2026 23:37:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:37:33 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Tue, 12 May 2026 23:37:33 GMT
WORKDIR /usr/local/tomcat
# Tue, 12 May 2026 23:37:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:37:33 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 12 May 2026 23:37:33 GMT
ENV TOMCAT_MAJOR=10
# Tue, 12 May 2026 23:37:33 GMT
ENV TOMCAT_VERSION=10.1.55
# Tue, 12 May 2026 23:37:33 GMT
ENV TOMCAT_SHA512=f36af12391a277e5c3a802a8e1a2a1e4354cd461b547d2e1a33ac0ab88d707d3fb2591e034a17b7d3a6b965a4c977a97dbf29bb81a3867e85aeec3d8d189e22e
# Tue, 12 May 2026 23:37:34 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Tue, 12 May 2026 23:37:42 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 23:37:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Tue, 12 May 2026 23:37:43 GMT
EXPOSE map[8080/tcp:{}]
# Tue, 12 May 2026 23:37:43 GMT
ENTRYPOINT []
# Tue, 12 May 2026 23:37:43 GMT
CMD ["catalina.sh" "run"]
# Wed, 13 May 2026 00:14:39 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Wed, 13 May 2026 00:14:39 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Wed, 13 May 2026 00:14:39 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Wed, 13 May 2026 00:14:39 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Wed, 13 May 2026 00:14:39 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Wed, 13 May 2026 00:14:39 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Wed, 13 May 2026 00:14:39 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 00:14:39 GMT
ENV XWIKI_VERSION=18.3.0
# Wed, 13 May 2026 00:14:39 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/18.3.0
# Wed, 13 May 2026 00:14:39 GMT
ENV XWIKI_DOWNLOAD_SHA256=3a0594e4260bc832c8a42f9ea1d6f47d9da7c8ffb7bbe65b7c363e7e8308051a
# Wed, 13 May 2026 00:15:01 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Wed, 13 May 2026 00:15:01 GMT
ENV POSTGRES_JDBC_VERSION=42.7.10
# Wed, 13 May 2026 00:15:01 GMT
ENV POSTGRES_JDBC_SHA256=cab1cd67cfa25c25de4348e532298028288a877ba01c77d1619fe45416193387
# Wed, 13 May 2026 00:15:01 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.10
# Wed, 13 May 2026 00:15:01 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.10.jar
# Wed, 13 May 2026 00:15:01 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.10.jar
# Wed, 13 May 2026 00:15:01 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Wed, 13 May 2026 00:15:01 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Wed, 13 May 2026 00:15:01 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Wed, 13 May 2026 00:15:01 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Wed, 13 May 2026 00:15:01 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 13 May 2026 00:15:01 GMT
VOLUME [/usr/local/xwiki]
# Wed, 13 May 2026 00:15:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 00:15:01 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38815cba44dccf952747a068e6817ab567111a1c108b6dcd5c0b012d0f109b97`  
		Last Modified: Fri, 08 May 2026 00:00:24 GMT  
		Size: 17.0 MB (16997471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deedef5af075591feecaed06bc515c816989687a293e4bb0831646d46420af2`  
		Last Modified: Fri, 08 May 2026 00:00:25 GMT  
		Size: 52.3 MB (52314893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62335cfc5fbef6fb489815953e6ae3eca5ab0be8a983b3a23657e220be53e087`  
		Last Modified: Fri, 08 May 2026 00:00:23 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0308dfed5f9175f77174db7f0b8419872cd497212c4a39110d8d4c35707627d2`  
		Last Modified: Fri, 08 May 2026 00:00:23 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2294bfa5ed9e69b6ed7e3a2ddb7dda944403b5c5706104d873f9df7da349da5`  
		Last Modified: Tue, 12 May 2026 23:37:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ad49dc75be6c83ae7cb60f8ab63fcda1c6b32a2e54a839a7823f6852531baa`  
		Last Modified: Tue, 12 May 2026 23:37:52 GMT  
		Size: 14.3 MB (14314819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb72bbc785bb1cca21fea474a6e61c9f1b0c098c46032d554c8f8dbf6d03b265`  
		Last Modified: Tue, 12 May 2026 23:37:52 GMT  
		Size: 225.3 KB (225256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff32ffec16b05ef6ff2f7fa4c19c4be1e2a8ea104ded7e8902f9b8e5ee0bfb0`  
		Last Modified: Wed, 13 May 2026 00:15:42 GMT  
		Size: 188.9 MB (188916048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360988e3beb190823854c87c9f1e9b14ec127fae9b27e1d4bd9be22be98b2832`  
		Last Modified: Wed, 13 May 2026 00:15:44 GMT  
		Size: 344.5 MB (344522228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87feaa112ad4bde5238227a69416e8b9c8bf0f73e20d3aafc468c3efd411c65e`  
		Last Modified: Wed, 13 May 2026 00:15:35 GMT  
		Size: 1.1 MB (1061590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d2b7a86b22560d51a8e9a649e76c503198c4bf55388f960a467f9c54fb7ef7`  
		Last Modified: Wed, 13 May 2026 00:15:35 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283c876d9c987bec8552353c81f69e67b07b520ecf3803b352c6aedeaac20365`  
		Last Modified: Wed, 13 May 2026 00:15:37 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e907d5efdc7b1d4561ff81f4443dfb625d95569267f24cc9ef473ac29389067`  
		Last Modified: Wed, 13 May 2026 00:15:35 GMT  
		Size: 11.0 KB (11012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b821815f61d4ddad1a60f82f27d2480c9776a75077d9459f26ddbecb26971a`  
		Last Modified: Wed, 13 May 2026 00:15:37 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:18-postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:6c636ef30d4992d9eaf7f44f3c50a0175cfd2188457cf994aa77274075f592b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9240598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f454c1fe9078ecc1602f5959b6cf1cfe18a37a997d41a1204c46ffc9c4fe93d2`

```dockerfile
```

-	Layers:
	-	`sha256:ff620f40f92d2ce77f538f185af716fece2ddc73feb6a92ed34994ad661c1400`  
		Last Modified: Wed, 13 May 2026 00:15:35 GMT  
		Size: 9.2 MB (9199672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55fd3fca0d5b97614c50613222213e16d8d34dab42c094d6daf456b2be106f0d`  
		Last Modified: Wed, 13 May 2026 00:15:35 GMT  
		Size: 40.9 KB (40926 bytes)  
		MIME: application/vnd.in-toto+json
