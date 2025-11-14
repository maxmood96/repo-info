## `xwiki:postgres-tomcat`

```console
$ docker pull xwiki@sha256:3c5a6570f0b416c5308df18b4a010c27d9009e3b14c1cfd3a4c545c681d08562
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:postgres-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:74516d73975c03cd730ea303f7ce962021c10fb7d7033acbc869595a9d4e5b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.9 MB (626868538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813a0143da9e74d5fa8389b85e87c510209e1c1d46a6ab7c2fbd2f7506a3bbd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Sat, 08 Nov 2025 17:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:55 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:59:55 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aeab55d064a1a27a3744b0880b9b414077b4ed2b1790817eea3df60aec946431';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        arm64)          ESUM='1d041073c65e834bdb4da732485a54ff829859dcd1549e7992f15bd73341be29';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64el)          ESUM='4973d6a43393854ccabd32bf7a1306788831586166fc8f5fa34a9df428366014';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        riscv64)          ESUM='bf821d8240e5d660f0c7e1ffa4f62e4b2dbf72c3d2245d9371160f61389b5fa4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='951eb9fd40e4478b0a7069b672bc0307f59045d756dd3ca6ed0b1ea12ab41ca2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jre_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 08 Nov 2025 17:59:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 19:11:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 10 Nov 2025 19:11:41 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 19:11:41 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 10 Nov 2025 19:11:41 GMT
WORKDIR /usr/local/tomcat
# Mon, 10 Nov 2025 19:11:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:11:41 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 10 Nov 2025 19:11:41 GMT
ENV TOMCAT_MAJOR=10
# Mon, 10 Nov 2025 19:11:41 GMT
ENV TOMCAT_VERSION=10.1.49
# Mon, 10 Nov 2025 19:11:41 GMT
ENV TOMCAT_SHA512=a46c8e37d4767b56a16dbdd8e81b80f25ad2edd5fba68b5099b9165cfffbe32bc923a601db8bb5cba50e8b1047a7906eb8c30ca176e1c0b8dfd85fbb9c54c6c2
# Mon, 10 Nov 2025 19:11:41 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 10 Nov 2025 19:11:47 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:11:47 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 10 Nov 2025 19:11:47 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 10 Nov 2025 19:11:47 GMT
ENTRYPOINT []
# Mon, 10 Nov 2025 19:11:47 GMT
CMD ["catalina.sh" "run"]
# Mon, 10 Nov 2025 19:32:27 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 10 Nov 2025 19:32:27 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 10 Nov 2025 19:32:27 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 10 Nov 2025 19:32:27 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 10 Nov 2025 19:32:27 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 10 Nov 2025 19:32:27 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 10 Nov 2025 19:32:27 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Nov 2025 19:32:27 GMT
ENV XWIKI_VERSION=17.9.0
# Mon, 10 Nov 2025 19:32:27 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.9.0
# Mon, 10 Nov 2025 19:32:27 GMT
ENV XWIKI_DOWNLOAD_SHA256=917d927f03630cb7b7811ecca76bb4a3681e55b47ee262ae27c55f4e751439ce
# Mon, 10 Nov 2025 19:32:48 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 10 Nov 2025 19:32:48 GMT
ENV POSTGRES_JDBC_VERSION=42.7.8
# Mon, 10 Nov 2025 19:32:48 GMT
ENV POSTGRES_JDBC_SHA256=2a32a9dcbc42d67a50ad3a0de5efd102c8d2be46720045f2cbd6689f160ab7c7
# Mon, 10 Nov 2025 19:32:48 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.8
# Mon, 10 Nov 2025 19:32:48 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.8.jar
# Mon, 10 Nov 2025 19:32:48 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.8.jar
# Mon, 10 Nov 2025 19:32:48 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 10 Nov 2025 19:32:48 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 10 Nov 2025 19:32:48 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 10 Nov 2025 19:32:48 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 10 Nov 2025 19:32:48 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 10 Nov 2025 19:32:48 GMT
VOLUME [/usr/local/xwiki]
# Mon, 10 Nov 2025 19:32:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 19:32:48 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab3da5da257e46e9d6b1be6e6312cf99ab2fd30b3369ea1e6e8133c3ec67afc`  
		Last Modified: Sat, 08 Nov 2025 18:00:24 GMT  
		Size: 17.0 MB (16972258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8908794a351cbc23988c2d21157ab97f0e7f9caf3b6ca7652c35ae100381a897`  
		Last Modified: Sat, 08 Nov 2025 18:00:40 GMT  
		Size: 53.0 MB (52978720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8db6d83f4b1e909438cff1d916e4c634deba5e4c3b141c6d0d5cce163272729`  
		Last Modified: Sat, 08 Nov 2025 18:00:23 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc3096c0eb2bbc9ac33b0cdb8552433f874659010096eb476cdd53f1aae60a3`  
		Last Modified: Sat, 08 Nov 2025 18:00:25 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3b18749b296fd1a4e2cefd7a78db16ec19391a201fbae1dfefa1cea3a84461`  
		Last Modified: Mon, 10 Nov 2025 19:12:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2bb3719c10613586cab0e6e9b92210f16e2c334bed84c18748b43eb743176f`  
		Last Modified: Mon, 10 Nov 2025 19:12:03 GMT  
		Size: 14.1 MB (14096357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ed621a82584bfab5f3b01657b033dd9791d4b1bcb0b4722cf4144fa13f9443`  
		Last Modified: Mon, 10 Nov 2025 19:12:01 GMT  
		Size: 224.8 KB (224751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeeebcf105f9cc2b0e5264d10c1c5c03c1c0b8c057440e6736983ebe73d757bf`  
		Last Modified: Mon, 10 Nov 2025 22:12:46 GMT  
		Size: 191.2 MB (191182153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1879c88a5c76f4343bb93a8aa4567ba2e4215dc956d75a347af4eb49a3b584`  
		Last Modified: Mon, 10 Nov 2025 22:12:57 GMT  
		Size: 320.6 MB (320632723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e5b5607159bd09e459d28fd5248453f3146bc76c08c65e4d95bedc2e440bb8`  
		Last Modified: Mon, 10 Nov 2025 19:33:40 GMT  
		Size: 1.0 MB (1043007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc362256a849b81b7c1f740dcb9fafc6aa4ee4530eb5b8d218ac7d06f9736fbf`  
		Last Modified: Mon, 10 Nov 2025 19:33:40 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d726c4c9d83cce64fc6c29ecca3c5ba68afc5c2fd46a3b323babd963833bf91`  
		Last Modified: Mon, 10 Nov 2025 19:33:40 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b91729393b93c2107f71f7b8b143d0f6a357dcaa28bde20dee4f343e818d63`  
		Last Modified: Mon, 10 Nov 2025 19:33:40 GMT  
		Size: 6.6 KB (6567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851db4c6cb06f1cb2dac75346f25335e2a377cc35f5ad6092b1b29ae6493b82e`  
		Last Modified: Mon, 10 Nov 2025 19:33:40 GMT  
		Size: 2.4 KB (2416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:c06d981524ca87440862967d0098e8b9d780fc20932bcea0b250fa74d469d5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9196397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7ec8bf21b971908eda63d1e43cd8dcb0cf44023781a8f45f9774001f00fb29`

```dockerfile
```

-	Layers:
	-	`sha256:9622bad64a258e7f38ad8536882002695152ff739aaf305890bed063d4212995`  
		Last Modified: Mon, 10 Nov 2025 22:08:37 GMT  
		Size: 9.2 MB (9155659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0028cd1fed5a43a8efaf26394f4a5e89e9f51c68893a58b3a6c92fc70c35ba1d`  
		Last Modified: Mon, 10 Nov 2025 22:08:38 GMT  
		Size: 40.7 KB (40738 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:postgres-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:788158970fb0b0f67fa337239c479547192b49b4f242bf48c00cf543d3ae1b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.9 MB (622865097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79125437a6cbefc14ce8a4c29911ce0ddc97b34c0f792e2ba81d3b56c5af518`
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
# Fri, 14 Nov 2025 01:40:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 14 Nov 2025 01:40:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:40:24 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Fri, 14 Nov 2025 01:40:24 GMT
WORKDIR /usr/local/tomcat
# Fri, 14 Nov 2025 01:40:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 01:40:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 14 Nov 2025 01:40:24 GMT
ENV TOMCAT_MAJOR=10
# Fri, 14 Nov 2025 01:40:24 GMT
ENV TOMCAT_VERSION=10.1.49
# Fri, 14 Nov 2025 01:40:24 GMT
ENV TOMCAT_SHA512=a46c8e37d4767b56a16dbdd8e81b80f25ad2edd5fba68b5099b9165cfffbe32bc923a601db8bb5cba50e8b1047a7906eb8c30ca176e1c0b8dfd85fbb9c54c6c2
# Fri, 14 Nov 2025 01:40:24 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Fri, 14 Nov 2025 01:40:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:40:34 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Fri, 14 Nov 2025 01:40:34 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 14 Nov 2025 01:40:34 GMT
ENTRYPOINT []
# Fri, 14 Nov 2025 01:40:34 GMT
CMD ["catalina.sh" "run"]
# Fri, 14 Nov 2025 02:24:12 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Fri, 14 Nov 2025 02:24:12 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Fri, 14 Nov 2025 02:24:12 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Fri, 14 Nov 2025 02:24:12 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Fri, 14 Nov 2025 02:24:12 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Fri, 14 Nov 2025 02:24:12 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Fri, 14 Nov 2025 02:24:12 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 02:24:12 GMT
ENV XWIKI_VERSION=17.9.0
# Fri, 14 Nov 2025 02:24:12 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.9.0
# Fri, 14 Nov 2025 02:24:12 GMT
ENV XWIKI_DOWNLOAD_SHA256=917d927f03630cb7b7811ecca76bb4a3681e55b47ee262ae27c55f4e751439ce
# Fri, 14 Nov 2025 02:24:34 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Fri, 14 Nov 2025 02:24:34 GMT
ENV POSTGRES_JDBC_VERSION=42.7.8
# Fri, 14 Nov 2025 02:24:34 GMT
ENV POSTGRES_JDBC_SHA256=2a32a9dcbc42d67a50ad3a0de5efd102c8d2be46720045f2cbd6689f160ab7c7
# Fri, 14 Nov 2025 02:24:34 GMT
ENV POSTGRES_JDBC_PREFIX=https://repo1.maven.org/maven2/org/postgresql/postgresql/42.7.8
# Fri, 14 Nov 2025 02:24:34 GMT
ENV POSTGRES_JDBC_ARTIFACT=postgresql-42.7.8.jar
# Fri, 14 Nov 2025 02:24:34 GMT
ENV POSTGRES_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/postgresql-42.7.8.jar
# Fri, 14 Nov 2025 02:24:34 GMT
RUN curl -fSL "${POSTGRES_JDBC_PREFIX}/${POSTGRES_JDBC_ARTIFACT}" -o $POSTGRES_JDBC_TARGET &&   echo "$POSTGRES_JDBC_SHA256 $POSTGRES_JDBC_TARGET" | sha256sum -c - # buildkit
# Fri, 14 Nov 2025 02:24:34 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Fri, 14 Nov 2025 02:24:34 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Fri, 14 Nov 2025 02:24:34 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Fri, 14 Nov 2025 02:24:34 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 02:24:34 GMT
VOLUME [/usr/local/xwiki]
# Fri, 14 Nov 2025 02:24:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 02:24:34 GMT
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
	-	`sha256:6cc54f22ff7be481d07fbc5563fa78622b485d16a8399546cb598cd4116d3fb6`  
		Last Modified: Fri, 14 Nov 2025 01:40:48 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796431cd390aaf24c6f9076bf17f54d840b43c2bc40b53c454e8aebb59cc538d`  
		Last Modified: Fri, 14 Nov 2025 01:40:49 GMT  
		Size: 14.1 MB (14099378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b6fa534208a2149ad3fd01edcd3758353690a78f52f6acd10f60d8572246e2`  
		Last Modified: Fri, 14 Nov 2025 01:40:48 GMT  
		Size: 225.2 KB (225203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad942bebec05b6cb1302d8a6e521725448604a844ed9449c5a689076cafb370`  
		Last Modified: Fri, 14 Nov 2025 04:10:28 GMT  
		Size: 188.8 MB (188849472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdf6cc2e3648d91fe30841f2e84a16fce50c9c01f06b9eaace97d1060e1b8f5`  
		Last Modified: Fri, 14 Nov 2025 04:10:32 GMT  
		Size: 320.6 MB (320632828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0437cdf77bf26cb6551d32d6d02a01c788cb42269b69054d09e62595d7db6705`  
		Last Modified: Fri, 14 Nov 2025 02:25:23 GMT  
		Size: 1.0 MB (1043012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d23dba122672bd7b0aae985b3cd793134fa11e2181c1a40a41ade3bc5b4663b`  
		Last Modified: Fri, 14 Nov 2025 02:25:23 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13e8c5e44a26eb82dc1f39b3613c0092955b494eed587ee5d167f125fc5b9c1`  
		Last Modified: Fri, 14 Nov 2025 02:25:23 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15abac43c5bb0f4ff6e11f3a18ea0c061435ac01f4b67c2ebbf274bdd4049106`  
		Last Modified: Fri, 14 Nov 2025 02:25:23 GMT  
		Size: 6.6 KB (6568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86c5ce58fc87b41f47173beadc0bc1eb275882b35a9d1f3d6acf08bfeaa7c06`  
		Last Modified: Fri, 14 Nov 2025 02:25:23 GMT  
		Size: 2.4 KB (2418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:postgres-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:214bb59fdbf66a8ee3da0b5b21293105666f879072918fc95ded43beb0e724a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9197340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2479bfcf04075fb3462e11ae369a04f481148ed366db9123bbfa3d8436368927`

```dockerfile
```

-	Layers:
	-	`sha256:d899e53c47f2a569444e76924e0f8e65605dbe9878cd0265c334673a1b307acb`  
		Last Modified: Fri, 14 Nov 2025 04:08:35 GMT  
		Size: 9.2 MB (9156428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e1b4694b596ff97bb5e9390c56a8894eaf7c401bb5efd64de9ca5176ab3b4e8`  
		Last Modified: Fri, 14 Nov 2025 04:08:36 GMT  
		Size: 40.9 KB (40912 bytes)  
		MIME: application/vnd.in-toto+json
