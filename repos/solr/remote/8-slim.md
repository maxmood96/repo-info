## `solr:8-slim`

```console
$ docker pull solr@sha256:7d55832c536a833cd1fc4c709b420a7b5c4f20429f2e3db0aaba5627c8a5bf48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `solr:8-slim` - linux; amd64

```console
$ docker pull solr@sha256:bbb3131320ba147e8b5595d43a59e811043351bbec5d40d4ae5a6924dfaecc3b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269589180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8906172354ca6ae3e2604010411b2307f8307614299ae836dcdbc1c949559c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:31:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:31:09 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 01:33:14 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Tue, 31 Mar 2020 01:33:15 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 01:33:15 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 00:28:35 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 16 Apr 2020 00:29:11 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jre_
# Thu, 16 Apr 2020 00:29:11 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 16 Apr 2020 00:29:22 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Thu, 16 Apr 2020 01:40:06 GMT
LABEL maintainer=Martijn Koster "mak-docker@greenhills.co.uk"
# Thu, 16 Apr 2020 01:40:06 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 16 Apr 2020 01:40:06 GMT
ARG SOLR_VERSION=8.5.0
# Thu, 16 Apr 2020 01:40:06 GMT
ARG SOLR_SHA512=d896057f1951260958f243988913fa51304479517cfda6ab2e690a8007e3c6c7ec3561364a47f47f3a2f2554bb34e0cb91678df5b294128c9479f036adb220a6
# Thu, 16 Apr 2020 01:40:07 GMT
ARG SOLR_KEYS=81D3EB0408B4E1EB10AF443BA4F4C886B29BC2F4
# Thu, 16 Apr 2020 01:40:07 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Apr 2020 01:40:07 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Apr 2020 01:40:16 GMT
# ARGS: SOLR_KEYS=81D3EB0408B4E1EB10AF443BA4F4C886B29BC2F4 SOLR_SHA512=d896057f1951260958f243988913fa51304479517cfda6ab2e690a8007e3c6c7ec3561364a47f47f3a2f2554bb34e0cb91678df5b294128c9479f036adb220a6 SOLR_VERSION=8.5.0
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat;   rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:40:16 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.5.0/solr-8.5.0.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.5.0/solr-8.5.0.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.5.0/solr-8.5.0.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 16 Apr 2020 01:40:16 GMT
ENV GOSU_VERSION=1.11
# Thu, 16 Apr 2020 01:40:16 GMT
ENV GOSU_KEY=B42F6819007F00F88E364FD4036A9C25BF357DD4
# Thu, 16 Apr 2020 01:40:17 GMT
ENV TINI_VERSION=v0.18.0
# Thu, 16 Apr 2020 01:40:17 GMT
ENV TINI_KEY=595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7
# Thu, 16 Apr 2020 01:40:18 GMT
# ARGS: SOLR_KEYS=81D3EB0408B4E1EB10AF443BA4F4C886B29BC2F4 SOLR_SHA512=d896057f1951260958f243988913fa51304479517cfda6ab2e690a8007e3c6c7ec3561364a47f47f3a2f2554bb34e0cb91678df5b294128c9479f036adb220a6 SOLR_VERSION=8.5.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Apr 2020 01:40:19 GMT
# ARGS: SOLR_KEYS=81D3EB0408B4E1EB10AF443BA4F4C886B29BC2F4 SOLR_SHA512=d896057f1951260958f243988913fa51304479517cfda6ab2e690a8007e3c6c7ec3561364a47f47f3a2f2554bb34e0cb91678df5b294128c9479f036adb220a6 SOLR_VERSION=8.5.0
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS $GOSU_KEY $TINI_KEY; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 16 Apr 2020 01:40:44 GMT
# ARGS: SOLR_KEYS=81D3EB0408B4E1EB10AF443BA4F4C886B29BC2F4 SOLR_SHA512=d896057f1951260958f243988913fa51304479517cfda6ab2e690a8007e3c6c7ec3561364a47f47f3a2f2554bb34e0cb91678df5b294128c9479f036adb220a6 SOLR_VERSION=8.5.0
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   pkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";   wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$pkgArch";   wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$pkgArch.asc";   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   rm /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true;   wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-$pkgArch";   wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-$pkgArch.asc";   gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;   rm /usr/local/bin/tini.asc;   chmod +x /usr/local/bin/tini;   tini --version;   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 16 Apr 2020 01:40:45 GMT
COPY --chown=0:0dir:893f144aff80480bafb27e38f7755b66644279bd92a61929697c16884927c247 in /opt/docker-solr/scripts 
# Thu, 16 Apr 2020 01:40:45 GMT
VOLUME [/var/solr]
# Thu, 16 Apr 2020 01:40:45 GMT
EXPOSE 8983
# Thu, 16 Apr 2020 01:40:45 GMT
WORKDIR /opt/solr
# Thu, 16 Apr 2020 01:40:45 GMT
USER solr
# Thu, 16 Apr 2020 01:40:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2020 01:40:46 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5e36ba391601ebce2c22f34982f56ce9236ca9cfdef13b2bc60457881d84e8`  
		Last Modified: Tue, 31 Mar 2020 01:35:26 GMT  
		Size: 3.2 MB (3249089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f5150f7beb631588d1fd1dc420e1529f2db039f6c330d8cad4d7fc17fe51e5`  
		Last Modified: Tue, 31 Mar 2020 01:36:33 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa53fc65010943502332a0ea16a9a8d6e02174893e2afe7118acc24dab46d33a`  
		Last Modified: Thu, 16 Apr 2020 00:32:53 GMT  
		Size: 42.2 MB (42214654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6517b956cf17b928fbf799a0da6755f5f4c132fac3ed52b46541d6ff8f33e1c`  
		Last Modified: Thu, 16 Apr 2020 01:50:39 GMT  
		Size: 5.5 MB (5465687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8a0b26db75fe43bb1e6df6b8ded55db1a185a001a0a39d179a140969a4d14d`  
		Last Modified: Thu, 16 Apr 2020 01:50:37 GMT  
		Size: 4.3 KB (4285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45bf759d03edd974832bc98dbe56fbf82e40aaee2c6b826649ba6e6f116ea87b`  
		Last Modified: Thu, 16 Apr 2020 01:50:38 GMT  
		Size: 24.4 KB (24390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e0a61a548e8a6a6d5f49dbad9f1d70a1124f96a7b71edebf189a899fefc6a2`  
		Last Modified: Thu, 16 Apr 2020 01:51:19 GMT  
		Size: 191.5 MB (191532730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1f0f26be9da58be631699bd7a2cb914710abb5fb134492252421d9f210b92e`  
		Last Modified: Thu, 16 Apr 2020 01:50:38 GMT  
		Size: 6.3 KB (6273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:8e0b4c106dc317192b7ef10b523eb2600f142c8a069993d9fe71cb3ce75a2cd9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267231778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63e47a020a8c0b7d5f0f855a335ee564b866515f4eb09c021d901b29d909139`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 16 Apr 2020 02:41:52 GMT
ADD file:1aab17002a9095c31dd6928277a045cb26846ac58c3d2d63316332c99a5f90bd in / 
# Thu, 16 Apr 2020 02:41:57 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 12:02:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 12:02:43 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 12:02:44 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 16 Apr 2020 12:02:44 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 12:02:46 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 12:02:47 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 16 Apr 2020 12:04:10 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jre_
# Thu, 16 Apr 2020 12:04:11 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 16 Apr 2020 12:04:33 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Fri, 17 Apr 2020 02:08:15 GMT
LABEL maintainer=Martijn Koster "mak-docker@greenhills.co.uk"
# Fri, 17 Apr 2020 02:08:16 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Fri, 17 Apr 2020 02:08:16 GMT
ARG SOLR_VERSION=8.5.0
# Fri, 17 Apr 2020 02:08:17 GMT
ARG SOLR_SHA512=d896057f1951260958f243988913fa51304479517cfda6ab2e690a8007e3c6c7ec3561364a47f47f3a2f2554bb34e0cb91678df5b294128c9479f036adb220a6
# Fri, 17 Apr 2020 02:08:17 GMT
ARG SOLR_KEYS=81D3EB0408B4E1EB10AF443BA4F4C886B29BC2F4
# Fri, 17 Apr 2020 02:08:18 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 17 Apr 2020 02:08:19 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 17 Apr 2020 02:08:34 GMT
# ARGS: SOLR_KEYS=81D3EB0408B4E1EB10AF443BA4F4C886B29BC2F4 SOLR_SHA512=d896057f1951260958f243988913fa51304479517cfda6ab2e690a8007e3c6c7ec3561364a47f47f3a2f2554bb34e0cb91678df5b294128c9479f036adb220a6 SOLR_VERSION=8.5.0
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat;   rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 02:08:35 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.5.0/solr-8.5.0.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.5.0/solr-8.5.0.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.5.0/solr-8.5.0.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Fri, 17 Apr 2020 02:08:35 GMT
ENV GOSU_VERSION=1.11
# Fri, 17 Apr 2020 02:08:36 GMT
ENV GOSU_KEY=B42F6819007F00F88E364FD4036A9C25BF357DD4
# Fri, 17 Apr 2020 02:08:37 GMT
ENV TINI_VERSION=v0.18.0
# Fri, 17 Apr 2020 02:08:37 GMT
ENV TINI_KEY=595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7
# Fri, 17 Apr 2020 02:08:39 GMT
# ARGS: SOLR_KEYS=81D3EB0408B4E1EB10AF443BA4F4C886B29BC2F4 SOLR_SHA512=d896057f1951260958f243988913fa51304479517cfda6ab2e690a8007e3c6c7ec3561364a47f47f3a2f2554bb34e0cb91678df5b294128c9479f036adb220a6 SOLR_VERSION=8.5.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 17 Apr 2020 02:08:41 GMT
# ARGS: SOLR_KEYS=81D3EB0408B4E1EB10AF443BA4F4C886B29BC2F4 SOLR_SHA512=d896057f1951260958f243988913fa51304479517cfda6ab2e690a8007e3c6c7ec3561364a47f47f3a2f2554bb34e0cb91678df5b294128c9479f036adb220a6 SOLR_VERSION=8.5.0
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS $GOSU_KEY $TINI_KEY; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Fri, 17 Apr 2020 02:18:16 GMT
# ARGS: SOLR_KEYS=81D3EB0408B4E1EB10AF443BA4F4C886B29BC2F4 SOLR_SHA512=d896057f1951260958f243988913fa51304479517cfda6ab2e690a8007e3c6c7ec3561364a47f47f3a2f2554bb34e0cb91678df5b294128c9479f036adb220a6 SOLR_VERSION=8.5.0
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   pkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";   wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$pkgArch";   wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$pkgArch.asc";   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   rm /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true;   wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-$pkgArch";   wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-$pkgArch.asc";   gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;   rm /usr/local/bin/tini.asc;   chmod +x /usr/local/bin/tini;   tini --version;   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Fri, 17 Apr 2020 02:18:18 GMT
COPY --chown=0:0dir:893f144aff80480bafb27e38f7755b66644279bd92a61929697c16884927c247 in /opt/docker-solr/scripts 
# Fri, 17 Apr 2020 02:18:19 GMT
VOLUME [/var/solr]
# Fri, 17 Apr 2020 02:18:20 GMT
EXPOSE 8983
# Fri, 17 Apr 2020 02:18:21 GMT
WORKDIR /opt/solr
# Fri, 17 Apr 2020 02:18:21 GMT
USER solr
# Fri, 17 Apr 2020 02:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2020 02:18:23 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:3d48095d71a365b5910cea98e5566c152a3f9aa11657560568259bf93ff2f4cb`  
		Last Modified: Thu, 16 Apr 2020 02:48:58 GMT  
		Size: 25.9 MB (25857715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628cdf1546c37dea88bc2254b622d28d5e44245b414d02fa659efaf2740fe14b`  
		Last Modified: Thu, 16 Apr 2020 12:05:48 GMT  
		Size: 3.1 MB (3101177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d110e1418cea572f159b8c5d0b322dea9c9eda748afaec79ab9de4b6973603b4`  
		Last Modified: Thu, 16 Apr 2020 12:05:47 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4567ad690e1966e50e8a29afa51cb3942fd5219fcd2aa94501ebf75d77aecd`  
		Last Modified: Thu, 16 Apr 2020 12:07:10 GMT  
		Size: 41.3 MB (41312518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06c8ffdb5a3a0ed5487b795373f05b2663325d95926e0dd207c08414ec3a513`  
		Last Modified: Fri, 17 Apr 2020 03:26:32 GMT  
		Size: 5.5 MB (5458100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c066ee355fcee281e1dc3c682229f1286ed00285594182a572dd7fe34b3eb5ba`  
		Last Modified: Fri, 17 Apr 2020 03:26:30 GMT  
		Size: 4.3 KB (4321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61e9aedffc86ed35e824d6535b93a244a2bf9e3f4b343bb289646e110278370`  
		Last Modified: Fri, 17 Apr 2020 03:26:31 GMT  
		Size: 24.4 KB (24450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af4e2687d82e1fb68775c43a5369d47beb4f1a8208ebf5dcaa939e31bfd3cad`  
		Last Modified: Fri, 17 Apr 2020 03:26:52 GMT  
		Size: 191.5 MB (191466985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93e712b2bb91d7d77a13b4fb21a55019d0ddc6587922430e00376658ae3fab50`  
		Last Modified: Fri, 17 Apr 2020 03:26:31 GMT  
		Size: 6.3 KB (6302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
