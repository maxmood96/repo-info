## `solr:9-slim`

```console
$ docker pull solr@sha256:c31309064085bd43b3f368d5fddea34ba5236865647e6427f128b9f3e300da61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `solr:9-slim` - linux; amd64

```console
$ docker pull solr@sha256:4daa6d1e786eb32ec8b5415cdcd4c5876002913bf6083dcac0c39404f2fb1e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161214755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175396fa3960e97942c6a95f1a7fd44e10f9e47de1f9fd8aea2bc2ead9b2ad7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Thu, 07 May 2026 23:59:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:59:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:59:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:59:40 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 23:59:40 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Thu, 07 May 2026 23:59:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 07 May 2026 23:59:43 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:16:37 GMT
ARG SOLR_VERSION=9.10.1
# Fri, 08 May 2026 00:16:37 GMT
ARG SOLR_DIST=-slim
# Fri, 08 May 2026 00:16:37 GMT
ARG SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1
# Fri, 08 May 2026 00:16:37 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Fri, 08 May 2026 00:16:37 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 08 May 2026 00:16:37 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 08 May 2026 00:16:37 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 08 May 2026 00:16:37 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 08 May 2026 00:16:37 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 08 May 2026 00:16:37 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 08 May 2026 00:16:37 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 08 May 2026 00:16:37 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 08 May 2026 00:16:37 GMT
LABEL org.opencontainers.image.version=9.10.1
# Fri, 08 May 2026 00:16:37 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 May 2026 00:16:37 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 08 May 2026 00:16:37 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 08 May 2026 00:16:38 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 08 May 2026 00:16:38 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 08 May 2026 00:16:43 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 00:16:43 GMT
VOLUME [/var/solr]
# Fri, 08 May 2026 00:16:43 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 08 May 2026 00:16:43 GMT
WORKDIR /opt/solr
# Fri, 08 May 2026 00:16:43 GMT
USER 8983
# Fri, 08 May 2026 00:16:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 00:16:43 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e233fa9a2426d781eb3a663f5209668a0f543876fe801ffb333d28a7b018f2`  
		Last Modified: Thu, 07 May 2026 23:59:55 GMT  
		Size: 16.2 MB (16152698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90beff01515b4843e02a005e5aed6983c3b40af0454e41e00a84de716f4fd77`  
		Last Modified: Thu, 07 May 2026 23:59:56 GMT  
		Size: 47.6 MB (47564754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fabe90376bfc1c9d02eb490592776f0251a977e98a5fc8e9525ccde67dc7b0`  
		Last Modified: Thu, 07 May 2026 23:59:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0690947699dd57d8e357ab0e8cb9995edfd49ff2450152d2b8788515b5b7096b`  
		Last Modified: Thu, 07 May 2026 23:59:54 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b246182faf18a2c30c05bf9a7fc4a038d1e4d10ddf056d2178e4661aebeb3154`  
		Last Modified: Fri, 08 May 2026 00:16:55 GMT  
		Size: 66.1 MB (66125104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d653227840cc902af62bb755ca95c4297e540ba5441a49ecf312b8692b44cc`  
		Last Modified: Fri, 08 May 2026 00:16:53 GMT  
		Size: 4.3 KB (4275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8806318d3ef8662a19de9abfa8151089c7e99bd19ec4627baeabdb45cb5ae5bd`  
		Last Modified: Fri, 08 May 2026 00:16:53 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f385cfc36a3a684de54eba51bd32d9c11a81a105ec7dff1ec237069b652dfa86`  
		Last Modified: Fri, 08 May 2026 00:16:53 GMT  
		Size: 10.8 KB (10807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3666cb9a2d673100544a7070b251224223649aca0ba001c6422c777dee4ce2`  
		Last Modified: Fri, 08 May 2026 00:16:54 GMT  
		Size: 1.6 MB (1617931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:48f2bb9c30a509c9a74b4ddbbc3e5e9903b982608942f13bf497486dfcc99415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f87fad9835f011893e3c7005279d60b6efbbba7bbea0081edddbeab828cef8`

```dockerfile
```

-	Layers:
	-	`sha256:ad065d6e2186544593c294eb0e0880903c73449dc02a88476a1854c77a340e8c`  
		Last Modified: Fri, 08 May 2026 00:16:53 GMT  
		Size: 4.0 MB (3966170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d31966f2a283cb33cc654a9cb49e4739e2452dbd40d4f49dda9a5d4be3eef60`  
		Last Modified: Fri, 08 May 2026 00:16:53 GMT  
		Size: 34.1 KB (34080 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:ab00c8e858bea315bc6d479361058c94aa13e3dc0921955114732e8bfe149840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158350793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3a9fae2d5b9e142e18500394800426d22dd747493be76224aca9579b04ace7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Thu, 07 May 2026 23:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 May 2026 23:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 23:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 07 May 2026 23:59:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 07 May 2026 23:59:06 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Thu, 07 May 2026 23:59:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 07 May 2026 23:59:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 07 May 2026 23:59:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 07 May 2026 23:59:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:05:34 GMT
ARG SOLR_VERSION=9.10.1
# Fri, 08 May 2026 00:05:34 GMT
ARG SOLR_DIST=-slim
# Fri, 08 May 2026 00:05:34 GMT
ARG SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1
# Fri, 08 May 2026 00:05:34 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Fri, 08 May 2026 00:05:34 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 08 May 2026 00:05:34 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 08 May 2026 00:05:34 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 08 May 2026 00:05:34 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 08 May 2026 00:05:34 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 08 May 2026 00:05:34 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 08 May 2026 00:05:34 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 08 May 2026 00:05:34 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 08 May 2026 00:05:34 GMT
LABEL org.opencontainers.image.version=9.10.1
# Fri, 08 May 2026 00:05:34 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 May 2026 00:05:34 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 08 May 2026 00:05:34 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 08 May 2026 00:05:34 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 08 May 2026 00:05:34 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 08 May 2026 00:05:43 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 00:05:43 GMT
VOLUME [/var/solr]
# Fri, 08 May 2026 00:05:43 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 08 May 2026 00:05:43 GMT
WORKDIR /opt/solr
# Fri, 08 May 2026 00:05:43 GMT
USER 8983
# Fri, 08 May 2026 00:05:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 00:05:43 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959dacbeeb3d16a92354f9d67deddec1e89003269f4432cfbf8e46286a97fe1`  
		Last Modified: Thu, 07 May 2026 23:59:23 GMT  
		Size: 16.1 MB (16076177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c594e1edc9977ad3a65e0f725187bd270bfacdf75ebfa13000e465215bac98d3`  
		Last Modified: Thu, 07 May 2026 23:59:27 GMT  
		Size: 47.1 MB (47050262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430d5d773bfbc3dc1169cc436b31f0e1debb520687663e282d3fefde0c64ff92`  
		Last Modified: Thu, 07 May 2026 23:59:22 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771827679748aff6fee75de328131e1e2609e9c1ea12c71728800755bd7437f8`  
		Last Modified: Thu, 07 May 2026 23:59:23 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c849387a3424ea41cb18e57fcfe77ac1a76a31021df4e03c4204f23e16e3b27`  
		Last Modified: Fri, 08 May 2026 00:05:55 GMT  
		Size: 66.1 MB (66125215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304068bbd491a67d95a2a7c0e23a551776d5c50fc9f583f6e492472fdac36e3e`  
		Last Modified: Fri, 08 May 2026 00:05:53 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eff79dd0b1e806a77b155e0d8a431078de44d234489556bcf799559925e42f8`  
		Last Modified: Fri, 08 May 2026 00:05:53 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e1fccb5586397e71dc604b7cc16a0059749e7f11871d75505807fdd7bef7b7`  
		Last Modified: Fri, 08 May 2026 00:05:53 GMT  
		Size: 10.8 KB (10802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da9a21cafd77f79609c573b864f1477d9f4b13935e672c07be883357751b96b`  
		Last Modified: Fri, 08 May 2026 00:05:54 GMT  
		Size: 1.5 MB (1474800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:f4718aad5459857391b0823ea7d44f2230cf1db5338baacc3784a8707a2502f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d9780c86fe167bf2ab2032ece26eef9995de080a653827aef7a901ada9de62`

```dockerfile
```

-	Layers:
	-	`sha256:f0ee59b2bdecf6be457f0cb78b14d716bb776c1d3ca54c99a01cfb3c7ce43403`  
		Last Modified: Fri, 08 May 2026 00:05:53 GMT  
		Size: 4.0 MB (3965834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ad6b74ccbc8c54a6b444dbe8b1dee1c8bc520075cf41bf8bd7552dd8a45e0c`  
		Last Modified: Fri, 08 May 2026 00:05:53 GMT  
		Size: 34.2 KB (34233 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:53e44856fe106fc01a72a5bbcd9ff65bd703c685dbd5175a3722dba87c4e78fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167533481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2648f05f0addf484bde29641f489c04a291c9a6dbe2b5b9da445cdefb02e1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:14:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:14:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:14:32 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:14:32 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 08 May 2026 00:08:46 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:08:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:08:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:08:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 01:24:43 GMT
ARG SOLR_VERSION=9.10.1
# Fri, 08 May 2026 01:24:43 GMT
ARG SOLR_DIST=-slim
# Fri, 08 May 2026 01:24:43 GMT
ARG SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1
# Fri, 08 May 2026 01:24:43 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Fri, 08 May 2026 01:24:43 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 08 May 2026 01:24:43 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 08 May 2026 01:24:43 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 08 May 2026 01:24:43 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 08 May 2026 01:24:43 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 08 May 2026 01:24:43 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 08 May 2026 01:24:43 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 08 May 2026 01:24:43 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 08 May 2026 01:24:43 GMT
LABEL org.opencontainers.image.version=9.10.1
# Fri, 08 May 2026 01:24:43 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 May 2026 01:24:43 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 08 May 2026 01:24:43 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 08 May 2026 01:24:44 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 08 May 2026 01:24:44 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 08 May 2026 01:24:54 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 01:24:54 GMT
VOLUME [/var/solr]
# Fri, 08 May 2026 01:24:54 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 08 May 2026 01:24:54 GMT
WORKDIR /opt/solr
# Fri, 08 May 2026 01:24:54 GMT
USER 8983
# Fri, 08 May 2026 01:24:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 01:24:54 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fb6b0270a1e57e97f5a37840672246e903f6d765edf38fbdc976c403a8074e`  
		Last Modified: Wed, 15 Apr 2026 21:15:05 GMT  
		Size: 17.6 MB (17623543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63547f1d1a11cf1ca686dfb040571560bc2bb1758e416deef521d6e7ba04e95`  
		Last Modified: Fri, 08 May 2026 00:09:13 GMT  
		Size: 47.5 MB (47487447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45d6f9c4ba053fa7791ab933b4e8f064feab6632b55d9bf0277a1ade6cd7819`  
		Last Modified: Fri, 08 May 2026 00:09:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7880754df2ca5b7d2b60a4ba8e796203260e6c4cb24a0cc583d470917d2341`  
		Last Modified: Fri, 08 May 2026 00:09:12 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d3bc7dd0b7cc26b747bbb262e9db7598a139894322e19d13a7a1b2ddcfd3d2`  
		Last Modified: Fri, 08 May 2026 01:25:17 GMT  
		Size: 66.1 MB (66125503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287423e6ae620d2378da83d152a5463c15231bb3eade32156f6cc7713bddc11a`  
		Last Modified: Fri, 08 May 2026 01:25:15 GMT  
		Size: 4.3 KB (4276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40288d5a6b93f71e622938086e5de12d83bc2939c769f66eaa8a7dc8efaf4074`  
		Last Modified: Fri, 08 May 2026 01:25:15 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669b1d497a3f6ace2f532f43dc272b7b1d3fae509783584b04829292d76c6433`  
		Last Modified: Fri, 08 May 2026 01:25:15 GMT  
		Size: 10.8 KB (10803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275ee95a5951e649c25443f7f0a1dbd7ef2105870433f5b56aeddd1b8884b635`  
		Last Modified: Fri, 08 May 2026 01:25:16 GMT  
		Size: 1.6 MB (1630823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:e205ae31156a6b336b9ba8bb5f94113ca3390f99a0fa048777863039ad5df65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f3bc2b4641d21a284a2abeaa3a6c57f6ad55b4fe9307167010df0fb719d63b`

```dockerfile
```

-	Layers:
	-	`sha256:465eb22a9326093b39b5f98f3fb232f5af5fe51872dc124cb2f139f3d1f8974c`  
		Last Modified: Fri, 08 May 2026 01:25:15 GMT  
		Size: 4.0 MB (3970217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e60d9d9a90eefe0036d04a640a3d30cf7d05394bfc1066f7c93925a31bbfe84`  
		Last Modified: Fri, 08 May 2026 01:25:15 GMT  
		Size: 34.1 KB (34127 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:9-slim` - linux; s390x

```console
$ docker pull solr@sha256:e217c05a4e2fa1d8552f37457002e18cbc71824c9df7d8ce5385df50413aae93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156597326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5ee0a7ccbc1ced6a77f7d97e276b8f0655346e4aca9ee289ad8fa7af50233f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 10 Apr 2026 09:43:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:43:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:43:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:43:55 GMT
ADD file:2c9e0af50ab31bc11b1e04ab400db61aea5daeabc681e3e3b339bd029ab64362 in / 
# Fri, 10 Apr 2026 09:43:55 GMT
CMD ["/bin/bash"]
# Fri, 08 May 2026 00:03:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:03:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:03:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 00:03:18 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:03:18 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 08 May 2026 00:03:20 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        arm64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        armhf)          ESUM='018d1f5c11b2f1a2175c282a0fe8a17d9166da84b70ec1c60c1fa628a261d1eb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64el)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Fri, 08 May 2026 00:03:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 00:03:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 00:03:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 00:19:09 GMT
ARG SOLR_VERSION=9.10.1
# Fri, 08 May 2026 00:19:09 GMT
ARG SOLR_DIST=-slim
# Fri, 08 May 2026 00:19:09 GMT
ARG SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1
# Fri, 08 May 2026 00:19:09 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Fri, 08 May 2026 00:19:09 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Fri, 08 May 2026 00:19:09 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Fri, 08 May 2026 00:19:09 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 08 May 2026 00:19:09 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Fri, 08 May 2026 00:19:09 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 08 May 2026 00:19:09 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 08 May 2026 00:19:09 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 08 May 2026 00:19:09 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 08 May 2026 00:19:09 GMT
LABEL org.opencontainers.image.version=9.10.1
# Fri, 08 May 2026 00:19:09 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 08 May 2026 00:19:09 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Fri, 08 May 2026 00:19:09 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Fri, 08 May 2026 00:19:09 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Fri, 08 May 2026 00:19:09 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Fri, 08 May 2026 00:19:15 GMT
# ARGS: SOLR_VERSION=9.10.1 SOLR_DIST=-slim SOLR_SHA512=8720f813f1679360f11c753ad516d4680db31afc28065626d2558fb078bd163b79107326733bee3ba6702ca2fa7ef86bd608d594a740b7dcc5475e7c8650cae1 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 08 May 2026 00:19:15 GMT
VOLUME [/var/solr]
# Fri, 08 May 2026 00:19:15 GMT
EXPOSE map[8983/tcp:{}]
# Fri, 08 May 2026 00:19:15 GMT
WORKDIR /opt/solr
# Fri, 08 May 2026 00:19:15 GMT
USER 8983
# Fri, 08 May 2026 00:19:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 00:19:15 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f071508ee04bf825822830b555145d34544929d147718c75aef809024f1294d5`  
		Last Modified: Fri, 10 Apr 2026 11:01:30 GMT  
		Size: 28.2 MB (28202299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cc10c2e936d4cf190e275072a588bfa448d6b908fb8a997baff0f82c2f933c`  
		Last Modified: Fri, 08 May 2026 00:03:39 GMT  
		Size: 16.2 MB (16151040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd6cd162496e7cca760a14cca69a6088d2ddfa698d3f70a82d9ee1cd3674463`  
		Last Modified: Fri, 08 May 2026 00:03:39 GMT  
		Size: 44.5 MB (44542116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91941fdc45e2b271b1c116be1afb15588b7290faaea1aa70f2430e4a6064c90`  
		Last Modified: Fri, 08 May 2026 00:03:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a749db7a869bb24126a49476a8694bc1aeed908b099c8a66fb84eb01941fc27`  
		Last Modified: Fri, 08 May 2026 00:03:38 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772724d4bed91815851b387b1eba453e66ec0a1853f6dd45252f2853dbe1445b`  
		Last Modified: Fri, 08 May 2026 00:19:33 GMT  
		Size: 66.1 MB (66125016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea32c492b06893ef55d3bd9ba9d87e9384fa86c56da6b04735a5698bc312f08f`  
		Last Modified: Fri, 08 May 2026 00:19:32 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07dbcd2656ab14c334eb983900b672740635bb0d7d82656831582cc91809d5ad`  
		Last Modified: Fri, 08 May 2026 00:19:32 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda023ec3c41847f330aaff4f65c635e35f75affb3f60026e393e0eca5510f6b`  
		Last Modified: Fri, 08 May 2026 00:19:31 GMT  
		Size: 10.8 KB (10802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334ac7cf133bfc4875fa880e6f4f8e8baf7ad4121885ed0af90957b03451652b`  
		Last Modified: Fri, 08 May 2026 00:19:33 GMT  
		Size: 1.6 MB (1559062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:9-slim` - unknown; unknown

```console
$ docker pull solr@sha256:774a524ffdde65df9319bc7120e0a004f163d08fcffdee4376cdd1042eb7f0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb680a783280e78d4583feb98f8d5c38a1fbdecf847e4760be46e313a43afe4`

```dockerfile
```

-	Layers:
	-	`sha256:95b22c89ecdf37e15e9b486281fb9f74c88d61802686c855ad60f1d16b4699ad`  
		Last Modified: Fri, 08 May 2026 00:19:31 GMT  
		Size: 4.0 MB (3967766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d03ff14e15816f74095423dfeed5a84660b3565594236cd09e99cd1550f38111`  
		Last Modified: Fri, 08 May 2026 00:19:31 GMT  
		Size: 34.1 KB (34080 bytes)  
		MIME: application/vnd.in-toto+json
