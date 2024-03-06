## `solr:latest`

```console
$ docker pull solr@sha256:dce8d382dbbda7bc6f2f6c421ef6fec8414f9dd911818056e068e337811b7630
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
$ docker pull solr@sha256:1c57eacc51ff0113670a93b4c88403001efc11083922cbf3fcd4d903d216040b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.4 MB (378392287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ecf3af8bbe85497500fa9ba6e9f254ece316fc792ef0e7f8dd331e9b4b4d5d1`
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
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 13 Feb 2024 16:30:16 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 16:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 16:30:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 13 Feb 2024 16:30:16 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
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
	-	`sha256:23828d760c7b04df02891af556c40ca44c2dd79d6837ea6f18fac24f4108448c`  
		Last Modified: Tue, 27 Feb 2024 20:46:06 GMT  
		Size: 30.5 MB (30451302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2670537dcebc0b445ca47e68b31667f3572b8758b8388e24d8a6770e860ecc8`  
		Last Modified: Wed, 06 Mar 2024 06:09:59 GMT  
		Size: 17.5 MB (17456336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c059ccfa41820fb3f1472c4358304407b00e3eed15933f067b1d4957a40bfc3`  
		Last Modified: Wed, 06 Mar 2024 06:10:45 GMT  
		Size: 47.2 MB (47163248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23d33d59f2ab52fa44e6fbd4e629813614bb753bb3ccac98940e981a3b13c4e`  
		Last Modified: Wed, 06 Mar 2024 06:10:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842a648f54390edf0b921f43c547b5d6d6b937e58728be46796f6aefcd4735fb`  
		Last Modified: Wed, 06 Mar 2024 06:10:39 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe11eaa0c5b9f7ec35a955d8cb4e37984cc49e7c8c6e735e6a5c23a06bb93ee`  
		Last Modified: Wed, 06 Mar 2024 06:49:46 GMT  
		Size: 281.7 MB (281714312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4319800763cf0feed029b1d332684382f8585458e90cb0a4c186bab231cbcbcc`  
		Last Modified: Wed, 06 Mar 2024 06:49:40 GMT  
		Size: 4.3 KB (4269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc75e92d4f92b799750462d665871c751ead6e389be06b3ff327d1ce27af978`  
		Last Modified: Wed, 06 Mar 2024 06:49:40 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9150c716ad10397d634ec666ea98ef78e291b08b08de0f47cff4fc0abcc638c8`  
		Last Modified: Wed, 06 Mar 2024 06:49:40 GMT  
		Size: 10.9 KB (10870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93205d57173843034cc84e1ce5d7529c82e15ce7c7d97fee334b15652092241c`  
		Last Modified: Wed, 06 Mar 2024 06:49:42 GMT  
		Size: 1.6 MB (1590815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:c517968ea25cf6b24515d229be1d22ee4628ee1279b2ce72b03ec6fcdb963398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4225924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88701b4f3333f62526de8d25203fe351ca73166dead3c10a5a7ae7adb5cc9917`

```dockerfile
```

-	Layers:
	-	`sha256:6062328509b75e88e4933196480edb907aa7357ba06868241a890acb4632d7af`  
		Last Modified: Wed, 06 Mar 2024 06:49:40 GMT  
		Size: 4.2 MB (4191120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e7cb8c83968920b29f4b6bfd9a1675d292b52d40d4ce0395837991bc8f6ce5`  
		Last Modified: Wed, 06 Mar 2024 06:49:40 GMT  
		Size: 34.8 KB (34804 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; arm variant v7

```console
$ docker pull solr@sha256:2dc5d2e36144244d5655bc7dc3bcd1bd806bfce290bea13d3712a1cf1d4aad9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.1 MB (373075520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18820bbf57e79985b4d6b8b3781d9da425bb266f00d5bbc4cca02b9158c32632`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:00 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:01 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:20 GMT
ADD file:6767efafdb51cef2acde13d723fa618ffb3cd2155983115496c43ae730e762e6 in / 
# Tue, 13 Feb 2024 10:08:21 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 16:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 16:30:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 13 Feb 2024 16:30:16 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
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
	-	`sha256:469ff1e358fe0665e6d5ee032bad43f71c0f28f2231f273ce387dcaaaabf733e`  
		Last Modified: Wed, 14 Feb 2024 02:35:21 GMT  
		Size: 27.5 MB (27532464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e772b5c9a5ba5b718084e53d8d023f0ae531de7e351cc19a4982c01a4b41a76`  
		Last Modified: Fri, 16 Feb 2024 07:43:40 GMT  
		Size: 17.6 MB (17592912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b022ee625596e3739bd37edce11492ee30b887ee03ecfda347adad2d41e3719`  
		Last Modified: Fri, 16 Feb 2024 07:44:08 GMT  
		Size: 44.8 MB (44798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d14fff6bad669ccfd42b40ec388261e0966a749c42eff32e55ec9aae647673e`  
		Last Modified: Fri, 16 Feb 2024 07:44:00 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5bd39c66ca3c30eb63a02eff2092ca19b8d79a0898c55db23b7f3b194f910e`  
		Last Modified: Fri, 16 Feb 2024 07:44:00 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce791348b66b6a7ac5866505aeeaa8e96fa10ad69fbea806643c28bf974fe599`  
		Last Modified: Sat, 17 Feb 2024 07:51:14 GMT  
		Size: 281.7 MB (281716875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d758cb405bbe1fc8d18051f4ad89a4256f129bfce465c2c7b99b62546d55eba2`  
		Last Modified: Sat, 17 Feb 2024 07:51:07 GMT  
		Size: 4.2 KB (4203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59d992fa38dfb6b51f7aea14518ffcb351091ee17b3f346033e9c4905f31f48`  
		Last Modified: Sat, 17 Feb 2024 07:51:07 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aec5ba1cd84e591b86acc0fc096102092166f0c8a6ffe90080aa7ac7d449fa9`  
		Last Modified: Sat, 17 Feb 2024 07:51:07 GMT  
		Size: 10.9 KB (10868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b431d13fe36feb50edd782f0512373015c1e4871fa95b1bc57f0f3a593b2bce`  
		Last Modified: Sat, 17 Feb 2024 07:51:09 GMT  
		Size: 1.4 MB (1418189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:85aee2de44f56858a3d0a42026c30201263ce73478fca46e77a7b4e26dfa3e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4146301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b0f72aa2d777a42bf35a0f090ca5bfbd7b877f2774547a1bd4260a81e1f39c`

```dockerfile
```

-	Layers:
	-	`sha256:bea57fe12c9c4b16fcf6496fb20894cc58e8844f0aa5b6befb8e3fa3b78ed714`  
		Last Modified: Sat, 17 Feb 2024 07:51:08 GMT  
		Size: 4.1 MB (4112192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0cc087dc43709d0e44214e620135cfa72b07473db2b1d51d8751160096e298`  
		Last Modified: Sat, 17 Feb 2024 07:51:08 GMT  
		Size: 34.1 KB (34109 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:a17ba7069fef720a62efb73bb7d24a992a577906432db4611ade36c735bca3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.1 MB (377079950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03dae3fe7efbb2d071991a075b92b934798b431fc9dbb49b8f58a38595a6561`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 16:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 16:30:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 13 Feb 2024 16:30:16 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
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
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bac6b544c281c39df6cde20776732e9b89dbfbbbb49870c60c9af5ef1df471`  
		Last Modified: Fri, 16 Feb 2024 04:55:46 GMT  
		Size: 18.9 MB (18860590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244992bb9e51f456f3e5c927182054789a275d47eba65099182705a8e1952dc2`  
		Last Modified: Fri, 16 Feb 2024 04:56:12 GMT  
		Size: 46.6 MB (46639325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e543faa97f71ea4edea5a6153e1b82e4e9143354356435ca0a085c427b9b07e`  
		Last Modified: Fri, 16 Feb 2024 04:56:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b734e973751dd4636bc278f0ef5ee31fc8e10cc65a07ebd5ef57aa728870187`  
		Last Modified: Fri, 16 Feb 2024 04:56:06 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e2a935c89037a02ca9e5a7cfa8b06d3ee6f223ddb6d87ffad1e20ff75db812`  
		Last Modified: Fri, 16 Feb 2024 14:17:43 GMT  
		Size: 281.7 MB (281714353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8534ba4bde2e67507577aa400c673bed428250b3f12b9c48692c1d1d73b1405f`  
		Last Modified: Fri, 16 Feb 2024 14:17:38 GMT  
		Size: 4.3 KB (4306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca23797ad15b54bb9725782b39e51c6ea53be159be6a03b8870c58783a1f18fa`  
		Last Modified: Fri, 16 Feb 2024 14:17:38 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02dcb09b691d01af8be072ef1f703cf12eb186d9454ca73933dea9bb48452b3d`  
		Last Modified: Fri, 16 Feb 2024 14:17:38 GMT  
		Size: 10.9 KB (10870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07839537fc37bde2402a5d2f26350c5c5556742dd971b5cd05ff9e8e0abcddbc`  
		Last Modified: Fri, 16 Feb 2024 14:17:40 GMT  
		Size: 1.4 MB (1449052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:2d5fc781f3544a0f6ed60134a4a34cc394089d1d78316b594e890239d6c70ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3830610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eefe3d5e503ce02e1b0eb8bec544b8a9c4d472389716385f11c8cb1c9bfe9f2`

```dockerfile
```

-	Layers:
	-	`sha256:cbac9145dfce70aca6ad3b1875473600abf7c575afd022dae73fbc2cdea89cdb`  
		Last Modified: Fri, 16 Feb 2024 14:17:38 GMT  
		Size: 3.8 MB (3796613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41e1e3e25381dfc88fe1d6e8f2e40feb3c8927efc8007500278f8541289c9e4f`  
		Last Modified: Fri, 16 Feb 2024 14:17:38 GMT  
		Size: 34.0 KB (33997 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; ppc64le

```console
$ docker pull solr@sha256:4e48acd923a5cceca59f76a249e7797a17ab79d54d86945a3a619a43a83f70a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.7 MB (384696356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f872f93af82140ba25e9ebf087bdbfa1800409210b12dce7620a08a23da1f776`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 16:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 16:30:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 13 Feb 2024 16:30:16 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
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
	-	`sha256:fb95b1654dd508e6f2d1e7103bcd3af75a00fa6826603132794816af5418de7c`  
		Last Modified: Fri, 16 Feb 2024 03:06:52 GMT  
		Size: 35.6 MB (35628838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc402319b10feb1c6820fa2bc7cfba7869a3473e27191ab283db519e7e6da50`  
		Last Modified: Fri, 16 Feb 2024 03:08:21 GMT  
		Size: 18.7 MB (18726189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f9bec281d586fe857a730cd40136459428c7ccefda7ad98a1e0c5194e2d295`  
		Last Modified: Fri, 16 Feb 2024 03:08:53 GMT  
		Size: 47.0 MB (47012472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64d28cb5695f590c46c7d223348d7d58bfba0e23dec221f5343b0dca7a09bcb`  
		Last Modified: Fri, 16 Feb 2024 03:08:45 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77aabc96be0541477c14b4c395f0cedb75eb6388609833afb6cb0da3a3b182c7`  
		Last Modified: Fri, 16 Feb 2024 03:08:45 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf42bb1a228450a66d96b5c7b4b54b18ea60c4605d8af5d3c3bf254d666cda6`  
		Last Modified: Fri, 16 Feb 2024 09:39:54 GMT  
		Size: 281.7 MB (281715059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874192f5d926e96cc40ab3d47899c0ce50936032136b791d0b747756229c764d`  
		Last Modified: Fri, 16 Feb 2024 09:39:47 GMT  
		Size: 4.3 KB (4271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d9c28ea996b15b31cdac14cbaf35399dc9f3ea6856997bf9af795bc6619428`  
		Last Modified: Fri, 16 Feb 2024 09:39:47 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a94057d5558f9f0cae4b9c39ec93f920088d07bee2eec0bb8a9eb51867bb3f`  
		Last Modified: Fri, 16 Feb 2024 09:39:47 GMT  
		Size: 10.9 KB (10870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd1e5544b76b120289ad8003748e3f7e8914195178a7e9f89efae78309e630f`  
		Last Modified: Fri, 16 Feb 2024 09:39:48 GMT  
		Size: 1.6 MB (1597523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:86f441a7ffd7796cca9ddb09c8c671aec9166247707a5aefd1014554a1dbfe37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3773739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9945576c90196aee6d33bd181ecde41bf6ddede8c9a722f29231a670bbf0fb1d`

```dockerfile
```

-	Layers:
	-	`sha256:3e03f479db53717796d0d6f308f82ec2445c97aeb2e0b9b149b02ef9f4dc2bf7`  
		Last Modified: Fri, 16 Feb 2024 09:39:47 GMT  
		Size: 3.7 MB (3739707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6d0a07cc92a5d3ae703b475b663fd8e31308f723e6f4d7421fca2170850f63a`  
		Last Modified: Fri, 16 Feb 2024 09:39:47 GMT  
		Size: 34.0 KB (34032 bytes)  
		MIME: application/vnd.in-toto+json

### `solr:latest` - linux; s390x

```console
$ docker pull solr@sha256:e905d8165d1932c4da9bfe382668462511b3222f69a4ac2922c00d3aa163f023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.9 MB (372934539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831e0b19eb8abb3bf8ba815986338da88e317bfd40f92a34c424facef3e84410`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 13 Feb 2024 10:05:41 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:05:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:05:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:05:43 GMT
ADD file:0903319c85e93418ab3b2652f358f9269f6605e20b1c6bd55a810d75e48d901d in / 
# Tue, 13 Feb 2024 10:05:43 GMT
CMD ["/bin/bash"]
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 16:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 16:30:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 16:30:16 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        armhf|arm)          ESUM='0378bdf6769632b182b27ba4e53b17eaefefdbafa3845c15e1bd88a5aeec8442';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 13 Feb 2024 16:30:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Tue, 13 Feb 2024 16:30:16 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
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
	-	`sha256:d1d8eb67dcb980dd20128629fc5978b1e44a91f745560a173227c42f99d34f1b`  
		Last Modified: Fri, 16 Feb 2024 06:33:37 GMT  
		Size: 28.6 MB (28638724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06439c312d07b9a9a2b1abe400a875c694ea9d34abcd938043094f9fa832631d`  
		Last Modified: Fri, 16 Feb 2024 07:38:53 GMT  
		Size: 17.3 MB (17261530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a98bc508a0ab498758127e894ef7be31f835c290ca2eb4bf51d33dcd69f3b`  
		Last Modified: Fri, 16 Feb 2024 07:39:16 GMT  
		Size: 43.8 MB (43765973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc62b1194733a4e6d63c34bbe6cb119a73c7ee7312f4f386a1257fbcacd6971`  
		Last Modified: Fri, 16 Feb 2024 07:39:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95477c395ccdd2f62b54717915da0157b15ffcd321dcfa0747ae0d633fa98db1`  
		Last Modified: Fri, 16 Feb 2024 07:39:10 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b8b1aeda9301108af215687f39f65b3d60e6b8c1e99519a0a76b5d7b374d32`  
		Last Modified: Sat, 17 Feb 2024 07:51:10 GMT  
		Size: 281.7 MB (281714498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3805ac702b07f8035d6174380c8c83d87909253c502d7293e9185cd7e3af4954`  
		Last Modified: Sat, 17 Feb 2024 07:51:06 GMT  
		Size: 4.3 KB (4307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f69a93aba0e4b12a90f5dd7b793eb4242f37a3799cdf3b0315fcf10877638e6`  
		Last Modified: Sat, 17 Feb 2024 07:51:06 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61be7bef7335a1f71801a6b25200ce3b524cff0bccbfe613b4980fe48c4854e`  
		Last Modified: Sat, 17 Feb 2024 07:51:06 GMT  
		Size: 10.9 KB (10870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695bbbb1b88b39c6921f2b69e5a74e4a6a5f6b02161121bb3992c713a5173c99`  
		Last Modified: Sat, 17 Feb 2024 07:51:07 GMT  
		Size: 1.5 MB (1537501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `solr:latest` - unknown; unknown

```console
$ docker pull solr@sha256:aba99a2a0c69d5e2ab716d334820dfab0fcbd94021ac635e8a67262f300a9a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4155040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413c0bcc03735e031656620f3b35c67b17dfadee765637ca928ae7565f549d45`

```dockerfile
```

-	Layers:
	-	`sha256:1f487a752439b287749cbad06e823529e613f6275bc0efa06aaecc47afd34799`  
		Last Modified: Sat, 17 Feb 2024 07:51:06 GMT  
		Size: 4.1 MB (4121053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79aa82e7ab6a8400226bc07c983be6563efe4b0785141825ca03c2550fe21efe`  
		Last Modified: Sat, 17 Feb 2024 07:51:06 GMT  
		Size: 34.0 KB (33987 bytes)  
		MIME: application/vnd.in-toto+json
