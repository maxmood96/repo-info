## `solr:latest`

```console
$ docker pull solr@sha256:83f5d2606eb0f0a8550ba8984e9368318179f6fecd91aff2916d57dde86b487f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `solr:latest` - linux; amd64

```console
$ docker pull solr@sha256:8d54a40b766e6ba0599664dad755ef5d55511571509d2e5667935b07cb0169c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.8 MB (373825562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e6314cf93f63d68163f20902b6c12ec2ae8b884568f6eec6d5426b7d77dda6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 16:30:16 GMT
ARG RELEASE
# Tue, 13 Feb 2024 16:30:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 16:30:16 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 16:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 16:30:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DIST=
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dddff65ed2408fb8512cf4a5e475bc56396102dc76b9968c1f68a06414767b`  
		Last Modified: Tue, 16 Apr 2024 04:03:41 GMT  
		Size: 12.9 MB (12905145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1799e72eec6b835f4f493ec08eef7c0de31e3d1e4b3265db1d346a5282630e16`  
		Last Modified: Tue, 16 Apr 2024 04:06:54 GMT  
		Size: 47.2 MB (47163386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e489940d10c0f286533ea7999e045f2ff1188baa6aad2d676349e3e72c5e8b`  
		Last Modified: Tue, 16 Apr 2024 04:06:48 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34382f6b019ca012a4b3f974b3039a24f169585e6ae8fa737cf539791d51ea1f`  
		Last Modified: Tue, 16 Apr 2024 04:06:48 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7cb398fe2eec5e4e84b236b5a98f30b2d3ddcc64801e8bf03f37cdf365158f`  
		Last Modified: Tue, 16 Apr 2024 05:57:35 GMT  
		Size: 281.7 MB (281712514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54db9ec64c66cf2647ea4da4202270406b294ae8165fbbeca4251f7dde616e84`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 4.3 KB (4267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825d2b46f92f5404d40d626dbf6f5b5c3285018385086e44b16c54da1516555d`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cba7f51fdf5e8343fb65e64e5ef20b6209be7a1963025fa143a00a3a4f770f`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 10.9 KB (10873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fb0c799aad68401843ddb57af5c5ab170470ff16c11dfc85fa5296009df545`  
		Last Modified: Tue, 16 Apr 2024 05:57:32 GMT  
		Size: 1.6 MB (1588465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:3d169e49b3655aa8a4e9bc6fd242f7973f1e8cb9669175456c81db560fd58d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4070386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134b5ae3441e68b43749749aa749e6e01b8ca526c6a63e109e9f34c6ae051494`

```dockerfile
```

-	Layers:
	-	`sha256:27031bf704742c8b250b1deae988f5a0b0aa634146c19a869b778d6e9bbe8252`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 4.0 MB (4035582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee7de752730eb9d4d81da7bb2db865df320cfffe12cbd3f001fc1e78e8b33ebb`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 34.8 KB (34804 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; arm variant v7

```console
$ docker pull solr@sha256:792a81a0a50f129d83fcc796589decb939067cee55ce5aa076539dbdacbba745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.0 MB (367967270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d27fdbf58b6a464b78092bfd631cc18c2f11c6543c920d5ae001c5eb3b8a75b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 16:30:16 GMT
ARG RELEASE
# Tue, 13 Feb 2024 16:30:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 16:30:16 GMT
ADD file:6f389bd2321c4403916e241916136a723f3b4369eff026717faa53640b11a045 in / 
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 16:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 16:30:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DIST=
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:e6fd83845bcc21353d922e9f1f86f9a9a54a91d9d0e8ce05b528e0da1d3d93fe`  
		Last Modified: Thu, 29 Feb 2024 14:13:02 GMT  
		Size: 27.5 MB (27533934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d2c224798ac0ce7a6f36b8c9070679367fd5f1f25797715e763bfddd543276`  
		Last Modified: Thu, 28 Mar 2024 01:05:05 GMT  
		Size: 12.5 MB (12492356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f947e4507bdafae7864aa88cd5863f27cbed07089ca3c783b977a577717fca`  
		Last Modified: Thu, 28 Mar 2024 01:08:54 GMT  
		Size: 44.8 MB (44798863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166d2a4b4c88bf35c82b992e558a38b4591379b4123c3d86e167ed8d093efcd1`  
		Last Modified: Thu, 28 Mar 2024 01:08:45 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea621d9212ebe92f269047be5f4612aaa6b9e665cbf5b730234d0197f55511e8`  
		Last Modified: Thu, 28 Mar 2024 01:08:45 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379e4ae9a7d7f7d7fd390d63dafa92951dbf986f13da5f0dcc486c45bde468d4`  
		Last Modified: Thu, 28 Mar 2024 19:55:28 GMT  
		Size: 281.7 MB (281712459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca2b6cae7e6ef3822998ca713c0c731de70972f3531bce17f29a3a24ad4e60`  
		Last Modified: Thu, 28 Mar 2024 19:55:23 GMT  
		Size: 4.2 KB (4205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8866afc6405dd5c1f23b61ae843b7caed59da61997d33397fefbbb7a4e07faed`  
		Last Modified: Thu, 28 Mar 2024 19:55:22 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf5e7470a7e309892e47eed27c43420fae7fc297170ffe6a4b444baca20b2c9`  
		Last Modified: Thu, 28 Mar 2024 19:55:22 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd3f7d36c2bf3e1cdcb7975c13ee1c5849403aade4143361aa8a98d08d3fa64`  
		Last Modified: Thu, 28 Mar 2024 19:55:23 GMT  
		Size: 1.4 MB (1413449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:39f6cc415063133f8b1a1b038bce8f750402a8100c75b127c7b1777b623204c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4071990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d953161c5b0b491e455a4103ee12ecf7b1d932e88ff9661080100b6451c5e63`

```dockerfile
```

-	Layers:
	-	`sha256:6d47b0b39cec2dd57f65730f6cc28e33d1c543bee622675bc9fd68e2ca9d4fcf`  
		Last Modified: Thu, 28 Mar 2024 19:55:22 GMT  
		Size: 4.0 MB (4037881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eb00a8fbfdf3e1c03d80a1e2ea93fc62063c9d9585762bb8efb33188da9352b`  
		Last Modified: Thu, 28 Mar 2024 19:55:22 GMT  
		Size: 34.1 KB (34109 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:1ce44f07f755f1e26ee4dbe53a259078fc4fc58751f878155add3c3b9b4a0919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.1 MB (371061735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7880c9d5400416446b142f1509fd5802439fac7753ea88aae7598677d795bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 16:30:16 GMT
ARG RELEASE
# Tue, 13 Feb 2024 16:30:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 16:30:16 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 16:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 16:30:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DIST=
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:71dca2167f9f5ee82e602460098ce45ba714cb60cd683d677d994dad97c74bb2`  
		Last Modified: Wed, 28 Feb 2024 01:55:47 GMT  
		Size: 28.4 MB (28400638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2168560270786452bc1288278f5b8a7831c90a490efa55dc798deec8e871311a`  
		Last Modified: Thu, 28 Mar 2024 00:48:42 GMT  
		Size: 12.8 MB (12846303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6274ee4a91612c77ed0ab2ea4b1df4f10d29a3c2881d2d8b564571694cd9f69`  
		Last Modified: Thu, 28 Mar 2024 00:54:00 GMT  
		Size: 46.6 MB (46639100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f6d824ccd2521a065aa5ce5d027e0f7b027066e53446b20eaa7793a0bce51b`  
		Last Modified: Thu, 28 Mar 2024 00:53:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754a82fa6b427b86617d873030d69cf741994674dcdcb02c137f9489c28e29c5`  
		Last Modified: Thu, 28 Mar 2024 00:53:55 GMT  
		Size: 731.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a2a80c261752abdd1fc0cfe8d542192c31f6881b157d2330b9a809b168f867`  
		Last Modified: Thu, 28 Mar 2024 19:51:38 GMT  
		Size: 281.7 MB (281712387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9e0ae2b856091891d5661b936cb1f196826862e69b0409fabcbe965d7e8cae`  
		Last Modified: Thu, 28 Mar 2024 19:51:31 GMT  
		Size: 4.3 KB (4308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f2a37dce946fe559883a7709c8ed5fbbc078b7ff4f3150efd5054d39f5db5b`  
		Last Modified: Thu, 28 Mar 2024 19:51:32 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bc5f7adeb2353801b474405eea8bb99831123a6765d977fdc4f5705c3ac494`  
		Last Modified: Thu, 28 Mar 2024 19:51:32 GMT  
		Size: 10.9 KB (10870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4013a3e87a20a0f0c57b8cee85593093e40eeca69270f843bd7a84838fc0cbc`  
		Last Modified: Thu, 28 Mar 2024 19:51:33 GMT  
		Size: 1.4 MB (1446998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:201c1a95706a30082645c917dcc66b006aeab1e8e283222661b23cb1925b96ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4069795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e534660ab8b4d448f31197910a7e9f53178e4b6223dc88f66cb95f840631fd`

```dockerfile
```

-	Layers:
	-	`sha256:dc87a3821993c265c3974630d6ab5a031a0734f2a16585f9f6108c6d08e555e6`  
		Last Modified: Thu, 28 Mar 2024 19:51:32 GMT  
		Size: 4.0 MB (4035798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0945ef176d973d4fb14ada300c0aefaa54fe48ff403b759e698b4930b80f01c1`  
		Last Modified: Thu, 28 Mar 2024 19:51:31 GMT  
		Size: 34.0 KB (33997 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; ppc64le

```console
$ docker pull solr@sha256:55bf9848da602c6903898e177164e648ac4d0222c2cd05936c4426d4dfc0c48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 MB (379726173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880634e2138dbc5718eb69e63fb64844db047403739414d9d5ec07ee51804781`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 16:30:16 GMT
ARG RELEASE
# Tue, 13 Feb 2024 16:30:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 16:30:16 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 16:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 16:30:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DIST=
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:feb7982de9d21be48470dea87ea05ea815bb86577e041bfce6dd451f3993b96a`  
		Last Modified: Wed, 06 Mar 2024 01:44:45 GMT  
		Size: 35.6 MB (35622739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d32fecda2e29794161435064531bf3c8f696877ba3caedeb09d1812422c074b`  
		Last Modified: Thu, 28 Mar 2024 01:40:29 GMT  
		Size: 13.8 MB (13766644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2541a09db5a97fe5627863854001c1c5860315cea952865fc3a91729ff0f29e3`  
		Last Modified: Thu, 28 Mar 2024 01:47:30 GMT  
		Size: 47.0 MB (47012404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46aed06cb4e587f8dd478454aa925f426863ebf4b417523c89fb80dc14f2704`  
		Last Modified: Thu, 28 Mar 2024 01:47:22 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c256d251ce18314167b553387318b3e684c06d1f30473a085e082ea471c824c9`  
		Last Modified: Thu, 28 Mar 2024 01:47:22 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794838145479cc81ad0360fc54d302b54a89f842ef972e9b06363e8a44193867`  
		Last Modified: Thu, 28 Mar 2024 19:23:36 GMT  
		Size: 281.7 MB (281712906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9d04bdfe98819344787a2ddc1efc611c913f35bc2faeb7bfcdb19caa77fc82`  
		Last Modified: Thu, 28 Mar 2024 19:23:29 GMT  
		Size: 4.3 KB (4273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4ba8345521420d0d29c6e03451239aeabc3f81ea5350a9e8b62c5017d38446`  
		Last Modified: Thu, 28 Mar 2024 19:23:29 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7031264ccc9b600ccda47cc6d4f220f34927dee1310b459c0c9c1b3e2dc0091`  
		Last Modified: Thu, 28 Mar 2024 19:23:29 GMT  
		Size: 10.9 KB (10876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e315758e240819e4a85c9c6b3bc66ee3acebbf72c735b50e4e4bca37b9f1cc`  
		Last Modified: Thu, 28 Mar 2024 19:23:30 GMT  
		Size: 1.6 MB (1595195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:5339718499eac4efae7d7fabaa72dde2c93bf7bc3f1527795abae0797a95803c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4074109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac168f7dc379f7f06136db770a736ba9c8784d7850faef77d841e3648993b69`

```dockerfile
```

-	Layers:
	-	`sha256:abc45c688c78290d23276e4446d5e21c3385d6601c69f16bb32913afdd3ad4e2`  
		Last Modified: Thu, 28 Mar 2024 19:23:29 GMT  
		Size: 4.0 MB (4040076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd1d4b96f2f1a091c1a26b75116a59655f29ba6f98ea015fe2252737f167be96`  
		Last Modified: Thu, 28 Mar 2024 19:23:28 GMT  
		Size: 34.0 KB (34033 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; s390x

```console
$ docker pull solr@sha256:b76b4db4050d0bd143cf8c3475e82533c8702038f0d42521473f7483d90fc631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.7 MB (368653740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6caf011ca0286f5c0f0ebb587405b60b18423277d9cd74f6e8edb9a0297e753f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 16:30:16 GMT
ARG RELEASE
# Tue, 13 Feb 2024 16:30:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 16:30:16 GMT
ADD file:7691b95908cace61ceeec91c44a1a37e7dc2fc3ab5a5fd89f493cefdff9e840e in / 
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 16:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 16:30:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_VERSION=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DIST=
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455
# Tue, 13 Feb 2024 16:30:16 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.version=9.5.0
# Tue, 13 Feb 2024 16:30:16 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Tue, 13 Feb 2024 16:30:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER" # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
# ARGS: SOLR_VERSION=9.5.0 SOLR_DIST= SOLR_SHA512=e34b2421db8586691ff41b86beca77bcb61243ce8edfade74eda8da4b0fabde0078884db301350a0d0dfc4a6fee46320ddf059469300444da4e3693220df5e40 SOLR_KEYS=E05FDF113D89E7FB4A2DF4B2684D544160392455 SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 13 Feb 2024 16:30:16 GMT
VOLUME [/var/solr]
# Tue, 13 Feb 2024 16:30:16 GMT
EXPOSE map[8983/tcp:{}]
# Tue, 13 Feb 2024 16:30:16 GMT
WORKDIR /opt/solr
# Tue, 13 Feb 2024 16:30:16 GMT
USER 8983
# Tue, 13 Feb 2024 16:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:800aa7ed945a05dec0024b71aaef6a3ed35eb8fc8eef0982ff134513d2295713`  
		Last Modified: Tue, 16 Apr 2024 01:37:03 GMT  
		Size: 28.6 MB (28637157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8b881b4864a2e46e88ac5ec37c0b320ca30be290b791f04917dcc056809f3b`  
		Last Modified: Tue, 16 Apr 2024 01:50:44 GMT  
		Size: 13.0 MB (12986387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfebbced680b7390af0f88a97ca932f8f27bff80826bc87eb9bf49c145e698d`  
		Last Modified: Tue, 16 Apr 2024 01:52:25 GMT  
		Size: 43.8 MB (43765845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d3da2d88573089bc4ee694af587d7d08402f351e99599db6d1da2b3604eae0`  
		Last Modified: Tue, 16 Apr 2024 01:52:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5c2b092b12993a47168eec02810c84eeb0fd925b4dd1e08fedb626dd3fb089`  
		Last Modified: Tue, 16 Apr 2024 01:52:19 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96e7a50a88756ff6413748df2c0c1b93b5953edb5bed556e697fffb446a44a9`  
		Last Modified: Tue, 16 Apr 2024 18:14:47 GMT  
		Size: 281.7 MB (281712806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357a145f2114494464814c4e37cb93c3907b8823e726a26603f63c9b08889d93`  
		Last Modified: Tue, 16 Apr 2024 18:14:41 GMT  
		Size: 4.3 KB (4300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5222149e560c7b185a7f0672914e5598b5a0d7508822a1499cda1249c11791d8`  
		Last Modified: Tue, 16 Apr 2024 18:14:41 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d7420c1067910584234833c6bc2eb3dbe5d3735c2a82fe1c173b3f75ee08fe`  
		Last Modified: Tue, 16 Apr 2024 18:14:41 GMT  
		Size: 10.9 KB (10871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973618365dd4da83829a7f373745583c32f234455957469a784c8697cb4ba507`  
		Last Modified: Tue, 16 Apr 2024 18:14:42 GMT  
		Size: 1.5 MB (1535241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:4765f9226406cd3ca7ca7e7583043afe52a5e26a52e512ace9ef418a70026fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4071787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9da33c95c2b41f0ea74cbd207d9387ce2a28d40da3f33c479ae1061f36b0ff`

```dockerfile
```

-	Layers:
	-	`sha256:e3305505d24943eaf2378eb8e8fde6e5583caee925b006f29c97cce177db41c7`  
		Last Modified: Tue, 16 Apr 2024 18:14:41 GMT  
		Size: 4.0 MB (4037800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08abe693ecf38eb3b2b0c1d78f83d3a380fc107cd1d6adc1f803c90d7f2b96ab`  
		Last Modified: Tue, 16 Apr 2024 18:14:41 GMT  
		Size: 34.0 KB (33987 bytes)  
		MIME: application/vnd.in-toto+json
