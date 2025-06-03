## `solr:latest`

```console
$ docker pull solr@sha256:48cdf12cbaf971e308cf771d712c585fd4bb1a8289a1c58601e3c66ad17b22a4
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

### `solr:latest` - linux; amd64

```console
$ docker pull solr@sha256:637432c105a36fd8ebd5a85917db308c432c49d3fd52b8c7ec84981407f0d942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.6 MB (480647220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e0c0bf228b94ad0076be6a242fc5022753c7da51f9a334839e6d53c3dfe83c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 11 Mar 2025 21:10:22 GMT
ARG RELEASE
# Tue, 11 Mar 2025 21:10:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 11 Mar 2025 21:10:22 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Tue, 11 Mar 2025 21:10:22 GMT
CMD ["/bin/bash"]
# Tue, 11 Mar 2025 21:10:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 11 Mar 2025 21:10:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 21:10:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_VERSION=9.8.1
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DIST=
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.version=9.8.1
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 Mar 2025 21:10:22 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
VOLUME [/var/solr]
# Tue, 11 Mar 2025 21:10:22 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 11 Mar 2025 21:10:22 GMT
WORKDIR /opt/solr
# Tue, 11 Mar 2025 21:10:22 GMT
USER 8983
# Tue, 11 Mar 2025 21:10:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 21:10:22 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Fri, 30 May 2025 23:34:45 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31436012ac5bcbfec41a08366dfca6b77481c32087f9bd45d95448fe0a7f9be5`  
		Last Modified: Tue, 03 Jun 2025 04:16:07 GMT  
		Size: 16.1 MB (16146482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d16eb76e762f57fa51a1791f6debba460cba6ff9f06b379eaf3cdff3c47e941`  
		Last Modified: Tue, 03 Jun 2025 04:16:07 GMT  
		Size: 47.0 MB (46958345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac81863d97cb5054d3aa0f11069ea169a935f25e9faeb4f28a878a00f457e8bd`  
		Last Modified: Tue, 03 Jun 2025 04:16:07 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f6dfeccc1004ac0a37834f29e63e280bf5877d3e658a037ac6e80b51c91894`  
		Last Modified: Tue, 03 Jun 2025 04:16:07 GMT  
		Size: 2.3 KB (2284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd4248e081d7f26501fb92f8cb09ad9a6f5595431cd6c0db2908dd466c010c3`  
		Last Modified: Tue, 03 Jun 2025 05:15:28 GMT  
		Size: 386.4 MB (386373747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da15ad5148e2269769805b4a4e5a21ab86bae7e82c3d9a616d141f82f1fb327`  
		Last Modified: Tue, 03 Jun 2025 05:15:18 GMT  
		Size: 4.3 KB (4271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54d764c960608facbb1506fa85b6a22ec3462f7d8eba7b725cbd555fd25f959`  
		Last Modified: Tue, 03 Jun 2025 05:15:18 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887b62b5bd1add2f714f1646a965d5568cd22f8c915449d91f198349059b7848`  
		Last Modified: Tue, 03 Jun 2025 05:15:18 GMT  
		Size: 10.9 KB (10889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5d0761a4e4f69ed88281651839e47f864dccb12e96e5076e7090c3c770b1a1`  
		Last Modified: Tue, 03 Jun 2025 05:15:20 GMT  
		Size: 1.6 MB (1617800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:eda05f0aba4c1f5198d6f4a81cd6934dd6267cfd0bbca78e971d2d24982f6313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4443216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916f0069a9a8ebe495abf11c7010f3ed2604eac689d91d0acba1ac4af56c90c8`

```dockerfile
```

-	Layers:
	-	`sha256:00ccf2a4498d569da77d42b662904fdfb097154f1b6452c22eb6623d504410fb`  
		Last Modified: Tue, 03 Jun 2025 05:15:19 GMT  
		Size: 4.4 MB (4408881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b11391fe8042f2fd7eec63d465f4c3fcd6897f72b637624bc9bb9f756f43e9`  
		Last Modified: Tue, 03 Jun 2025 05:15:18 GMT  
		Size: 34.3 KB (34335 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:d25d32d21416786c690541303eac8bc102f24009dc22872676f19a945f8f0ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.8 MB (477754386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2ae7052b751c87eb3e9facea7406da257e187e6c3c079a4c0aa2898671e9c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 11 Mar 2025 21:10:22 GMT
ARG RELEASE
# Tue, 11 Mar 2025 21:10:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 11 Mar 2025 21:10:22 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Tue, 11 Mar 2025 21:10:22 GMT
CMD ["/bin/bash"]
# Tue, 11 Mar 2025 21:10:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 11 Mar 2025 21:10:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 21:10:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_VERSION=9.8.1
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DIST=
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.version=9.8.1
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 Mar 2025 21:10:22 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
VOLUME [/var/solr]
# Tue, 11 Mar 2025 21:10:22 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 11 Mar 2025 21:10:22 GMT
WORKDIR /opt/solr
# Tue, 11 Mar 2025 21:10:22 GMT
USER 8983
# Tue, 11 Mar 2025 21:10:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 21:10:22 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2a012351716029262feccd21d93c2eefbe543395255454bd5fbe2c647d7688`  
		Last Modified: Mon, 05 May 2025 16:49:48 GMT  
		Size: 16.1 MB (16059611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752104f1900141a559b0e68417061aa6cedecc9e70caa4685aed66e24a12ec44`  
		Last Modified: Mon, 05 May 2025 16:55:41 GMT  
		Size: 46.5 MB (46474272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17a6154fa8e1be02bff54c2febdfe1086692615737560db25d42cfe1b5a374e`  
		Last Modified: Mon, 05 May 2025 16:55:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0be8ecb107f9f1045913701b14a8cfb603bcccd47377e8d359a9e368e9417f9`  
		Last Modified: Mon, 05 May 2025 16:55:40 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39865b16d2432c1ac6cb60d794edd7b70842211dd9b415f53d07a6b95f93c446`  
		Last Modified: Mon, 05 May 2025 23:01:26 GMT  
		Size: 386.4 MB (386373671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71664e75e1f07350dcaf3d254a535994007614e6532d9e86500f7a7446d2feea`  
		Last Modified: Mon, 05 May 2025 23:01:16 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce469bc932f288c130580394416e8fc6b68400a0368c67f3a5ccd23eb5386d3`  
		Last Modified: Mon, 05 May 2025 23:01:16 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2469d8b44cf0810292786d160b81c28fd664263747f8bc32f5dad5a156bb96`  
		Last Modified: Mon, 05 May 2025 23:01:16 GMT  
		Size: 10.9 KB (10890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6592c0509dabd2fcc9dfccd5e58cbb555dde1ad352d6b79da06d4cec3b687f16`  
		Last Modified: Mon, 05 May 2025 23:01:17 GMT  
		Size: 1.5 MB (1474742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:0e5bf181e429ee3b12757fee5f288dccddc68a6edd705f757a864a2225655625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907f96c05473674df3c0e59e19be8069d7c7b1e11e56abaa2ead43010606d8a5`

```dockerfile
```

-	Layers:
	-	`sha256:d177e6c55f38b3abf8ff804ed16dfeb52318d7cb1bb8e099cc91c94a89c81ddd`  
		Last Modified: Mon, 05 May 2025 23:01:16 GMT  
		Size: 4.3 MB (4348225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55117abaadb3e69816fd8088193818408ff5904c78733b8cffb240c58b97cab3`  
		Last Modified: Mon, 05 May 2025 23:01:15 GMT  
		Size: 34.5 KB (34499 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; ppc64le

```console
$ docker pull solr@sha256:cea33588e506cd0562537588421fe037456a6ad01ebcf54e31eab7d973f6bc38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.9 MB (486853695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33fef10d3b6c3dc899e282ebe298c811e5651323103436c94a40a050a51f0ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 11 Mar 2025 21:10:22 GMT
ARG RELEASE
# Tue, 11 Mar 2025 21:10:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 11 Mar 2025 21:10:22 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Tue, 11 Mar 2025 21:10:22 GMT
CMD ["/bin/bash"]
# Tue, 11 Mar 2025 21:10:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 11 Mar 2025 21:10:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 21:10:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_VERSION=9.8.1
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DIST=
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.version=9.8.1
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 Mar 2025 21:10:22 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
VOLUME [/var/solr]
# Tue, 11 Mar 2025 21:10:22 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 11 Mar 2025 21:10:22 GMT
WORKDIR /opt/solr
# Tue, 11 Mar 2025 21:10:22 GMT
USER 8983
# Tue, 11 Mar 2025 21:10:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 21:10:22 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Mon, 28 Apr 2025 10:44:03 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec33a1aac040bccef1eea8d18ca590aec33573ce5507988fad5185d8737eaf2`  
		Last Modified: Mon, 05 May 2025 16:36:58 GMT  
		Size: 17.6 MB (17617818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25834f6d324d384142c5971685387b19e67dd389327576cfb3b257b255fc7df2`  
		Last Modified: Mon, 05 May 2025 16:46:54 GMT  
		Size: 46.8 MB (46769841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba96371a080094ed65cd163b9c7d953fad55d03cf77727fef406c96801bf5b75`  
		Last Modified: Mon, 05 May 2025 16:46:52 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9541f7f9fbd3768210ed938e497493b4a1a0dcb71989d9d49796d3fdde9c6395`  
		Last Modified: Mon, 05 May 2025 16:46:52 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac23c3a93451d1f029685cc146fc280b2a9838793b57d2fa608fa8bbf04ffd26`  
		Last Modified: Mon, 05 May 2025 20:35:43 GMT  
		Size: 386.4 MB (386374140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f4756a0b4f6b04266a24e263fa729f969fa9a94bfe13913aadc28a0b887c2b`  
		Last Modified: Mon, 05 May 2025 20:35:30 GMT  
		Size: 4.3 KB (4274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57840906c7e114b0cd756c339f8ae2ef80e71783948e11c33a69015c7b104415`  
		Last Modified: Mon, 05 May 2025 20:35:30 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d015d5a2abf465437a250e668abe5f050bcb52ac6ddc0a92519fbc9d628ff79b`  
		Last Modified: Mon, 05 May 2025 20:35:31 GMT  
		Size: 10.9 KB (10898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf3afee566f6b0a1480a8702ab9c289c37aa6827d0a307a7bfd7b78ce5aeb33`  
		Last Modified: Mon, 05 May 2025 20:35:32 GMT  
		Size: 1.6 MB (1630825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:e95e561fca4bcb1c5a330fe026cdf4740972e9dd2b688043f9ecb0e89af42a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4386845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd751404ec5887e3c0c0d5e50e7b7fd30bdba4b012c3f7a241a3b739bafb886b`

```dockerfile
```

-	Layers:
	-	`sha256:c93ba7dc9bc902bdbba9e745143f4ae91c95d64f0e540c3ccd7fb9f27cc19914`  
		Last Modified: Mon, 05 May 2025 20:35:31 GMT  
		Size: 4.4 MB (4352458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2710d56512e82ddcf55b7efce3c51024a3e4a4eeffacf203b8f6a927ecfc3368`  
		Last Modified: Mon, 05 May 2025 20:35:30 GMT  
		Size: 34.4 KB (34387 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; s390x

```console
$ docker pull solr@sha256:dd210b4dc0df2beb5561d11e14eb39671495df4de509be953959d1ef5c4f95fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.1 MB (476056110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0fb1ed5b12adbb3fcb73517d583501853dbd4301406b934c63374c0a2343d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 11 Mar 2025 21:10:22 GMT
ARG RELEASE
# Tue, 11 Mar 2025 21:10:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 11 Mar 2025 21:10:22 GMT
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Tue, 11 Mar 2025 21:10:22 GMT
CMD ["/bin/bash"]
# Tue, 11 Mar 2025 21:10:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 11 Mar 2025 21:10:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 21:10:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='aaed740c38ff1e87a4b920f9deb165d419d9fdf23f423740d2ecb280eeab9647';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_x64_linux_hotspot_17.0.15_6.tar.gz';          ;;        arm64)          ESUM='c89467f543bd434b71f3b748adeeeb1b2692f90242824b78205be1ae72ba385f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.15_6.tar.gz';          ;;        armhf)          ESUM='c5ba30280b49f5654440c897265819ed749259afd2d46d3136720ab182933679';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_arm_linux_hotspot_17.0.15_6.tar.gz';          ;;        ppc64el)          ESUM='f35795f3f62885460e96ebcc2ee4e34bb59ab0d1668f0dc0642070ed89e3dda9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.15_6.tar.gz';          ;;        s390x)          ESUM='68275080c9010d1ef0cab7002c8489777c85952dc9c422d2aad4b20cd5123d69';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.15%2B6/OpenJDK17U-jre_s390x_linux_hotspot_17.0.15_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_VERSION=9.8.1
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DIST=
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Tue, 11 Mar 2025 21:10:22 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.description=Solr is the blazing-fast, open source, multi-modal search platform built on Apache Lucene. It powers full-text, vector, and geospatial search at many of the world's largest organizations.
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.version=9.8.1
# Tue, 11 Mar 2025 21:10:22 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 11 Mar 2025 21:10:22 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/solr/cross-dc-manager/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
# ARGS: SOLR_VERSION=9.8.1 SOLR_DIST= SOLR_SHA512=08888ea626b9fa617438b97f9f8d552acfbd087fc9fd248e7495627716decca5e2e8d55bedf0e1f2484c838295c2abd68debb002d1ae36965eb99753320459f4 SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 11 Mar 2025 21:10:22 GMT
VOLUME [/var/solr]
# Tue, 11 Mar 2025 21:10:22 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 11 Mar 2025 21:10:22 GMT
WORKDIR /opt/solr
# Tue, 11 Mar 2025 21:10:22 GMT
USER 8983
# Tue, 11 Mar 2025 21:10:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 21:10:22 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Fri, 30 May 2025 23:35:16 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b083bb928961c2c7996d495007331b50b7da602cad00b66781c07e7118c9394`  
		Last Modified: Tue, 03 Jun 2025 04:19:49 GMT  
		Size: 16.1 MB (16144355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e488d5d8106ce381c68977236ddb865aed01ba664d86a2a199770719a82afafa`  
		Last Modified: Tue, 03 Jun 2025 04:24:37 GMT  
		Size: 44.0 MB (43960915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b0ccdf4a2e452831fcde3f5339b6b340300388219842b1405f35f287219e06`  
		Last Modified: Tue, 03 Jun 2025 04:24:36 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa91a862670de4da5926a34a72dd28e49dd2e804f1a4c5aac92b21b4a3a4b113`  
		Last Modified: Tue, 03 Jun 2025 04:24:36 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a77f5e6fb2ec930a409a61cd05686249e585f5141eaed44d4c3698c7fce75d`  
		Last Modified: Tue, 03 Jun 2025 05:35:10 GMT  
		Size: 386.4 MB (386373432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4344731e90dee2e60dfb12b0119a2f624a4853cad54aa9be0ad8976547ee45`  
		Last Modified: Tue, 03 Jun 2025 05:35:04 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3384f3fbbfb48411314dde0bc31bf6689a3c5b6858e44f49bfef042ad48614f3`  
		Last Modified: Tue, 03 Jun 2025 05:35:04 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68899f5bb792560e8545cf4e91c12f4a848e8315a06aac1594927e3d419cc28b`  
		Last Modified: Tue, 03 Jun 2025 05:35:04 GMT  
		Size: 10.9 KB (10892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3176ed7e697e9c12cbb5b70a65664c7a0ee2526500dbfe917ee13234d9cf3f8`  
		Last Modified: Tue, 03 Jun 2025 05:35:04 GMT  
		Size: 1.6 MB (1558923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:bcf484dab0018252079daa88869a8f00a1f365fd0df821269ae3982fbcacde5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4444812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4256f7d08ce4483f926689abc316740d0f073f9e6707e497e7bcf4edbd536fa3`

```dockerfile
```

-	Layers:
	-	`sha256:bf190973f9ab8cfd16e3be9b1b89abf3b250fd2afde32fb0080d61d56ff96359`  
		Last Modified: Tue, 03 Jun 2025 05:35:04 GMT  
		Size: 4.4 MB (4410477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:701af2d99f973afab095911e263136fa6878341a6a370c6afca32cc47ea05fdb`  
		Last Modified: Tue, 03 Jun 2025 05:35:04 GMT  
		Size: 34.3 KB (34335 bytes)  
		MIME: application/vnd.in-toto+json
