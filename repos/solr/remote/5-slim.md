## `solr:5-slim`

```console
$ docker pull solr@sha256:8e5ff753539b8fb7716ef32e663926444fd55fd845aa0e752f6b0c6aa06c3f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `solr:5-slim` - linux; amd64

```console
$ docker pull solr@sha256:7ce61daaaa8cd9fce826b6ca8a838e168c47a2e25b92f99bd4721d5befe9f3eb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210403428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34c4e3bf4fc1b134104fdb6f71528ef599ab064666f18528a3c4d51e77cdaa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 06:48:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 06:52:23 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 12 May 2021 06:52:24 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 12 May 2021 06:52:24 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 06:52:25 GMT
ENV LANG=C.UTF-8
# Wed, 12 May 2021 06:52:25 GMT
ENV JAVA_VERSION=8u292
# Wed, 12 May 2021 06:53:07 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_x64_linux_8u292b10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_aarch64_linux_8u292b10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 13 May 2021 05:10:04 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 13 May 2021 05:10:04 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 13 May 2021 05:11:29 GMT
ARG SOLR_VERSION=5.5.5
# Thu, 13 May 2021 05:11:29 GMT
ARG SOLR_SHA512=9aa02a362b75fc2af8c01d7b7d37d04450787902397644ca2d950836aa9efc8447922255d23de1d228c96f442ec82b08be64c590438dbf5f71da04616ab022f2
# Thu, 13 May 2021 05:11:29 GMT
ARG SOLR_KEYS=5F55943E13D49059D3F342777186B06E1ED139E7
# Thu, 13 May 2021 05:11:29 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 13 May 2021 05:11:30 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 13 May 2021 05:11:36 GMT
# ARGS: SOLR_KEYS=5F55943E13D49059D3F342777186B06E1ED139E7 SOLR_SHA512=9aa02a362b75fc2af8c01d7b7d37d04450787902397644ca2d950836aa9efc8447922255d23de1d228c96f442ec82b08be64c590438dbf5f71da04616ab022f2 SOLR_VERSION=5.5.5
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 13 May 2021 05:11:37 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/5.5.5/solr-5.5.5.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/5.5.5/solr-5.5.5.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/5.5.5/solr-5.5.5.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 May 2021 05:11:38 GMT
# ARGS: SOLR_KEYS=5F55943E13D49059D3F342777186B06E1ED139E7 SOLR_SHA512=9aa02a362b75fc2af8c01d7b7d37d04450787902397644ca2d950836aa9efc8447922255d23de1d228c96f442ec82b08be64c590438dbf5f71da04616ab022f2 SOLR_VERSION=5.5.5
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 13 May 2021 05:11:39 GMT
# ARGS: SOLR_KEYS=5F55943E13D49059D3F342777186B06E1ED139E7 SOLR_SHA512=9aa02a362b75fc2af8c01d7b7d37d04450787902397644ca2d950836aa9efc8447922255d23de1d228c96f442ec82b08be64c590438dbf5f71da04616ab022f2 SOLR_VERSION=5.5.5
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 13 May 2021 05:12:05 GMT
# ARGS: SOLR_KEYS=5F55943E13D49059D3F342777186B06E1ED139E7 SOLR_SHA512=9aa02a362b75fc2af8c01d7b7d37d04450787902397644ca2d950836aa9efc8447922255d23de1d228c96f442ec82b08be64c590438dbf5f71da04616ab022f2 SOLR_VERSION=5.5.5
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   mv "/opt/solr-$SOLR_VERSION" /opt/solr;   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   mkdir -p /opt/solr/server/solr/mycores /opt/solr/server/logs /opt/mysolrhome;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   if [ -f "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter" ]; then chmod 0755 "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter"; fi;   chmod -R 0755 /opt/solr/server/scripts/cloud-scripts;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/solr /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/mysolrhome;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 13 May 2021 05:12:05 GMT
COPY --chown=solr:solrdir:24d14aedda51f56007d2c3091bd65f0167210afaf1c88aa50fac48af9e1d6037 in /opt/docker-solr/scripts 
# Thu, 13 May 2021 05:12:05 GMT
EXPOSE 8983
# Thu, 13 May 2021 05:12:06 GMT
WORKDIR /opt/solr
# Thu, 13 May 2021 05:12:06 GMT
USER solr
# Thu, 13 May 2021 05:12:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 May 2021 05:12:06 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2b89b6081832b112f9483322d4710c661f12135e79279dc3fb1672883ada8d`  
		Last Modified: Wed, 12 May 2021 06:58:18 GMT  
		Size: 3.3 MB (3268772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c211c6bdc908f680650c61f8d6df3358fc801fe67079a47251a837b62cad8d`  
		Last Modified: Wed, 12 May 2021 07:05:25 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c25606a3064020e8fd7271f6943576b6c0045873169f8ebf48205ff11a728de`  
		Last Modified: Wed, 12 May 2021 07:06:32 GMT  
		Size: 41.6 MB (41598808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6887daffed446b4fd7ddc0bb1d33e794e934f2ac8bfbc97208597f5d046ffaf9`  
		Last Modified: Thu, 13 May 2021 05:22:20 GMT  
		Size: 6.5 MB (6455362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7414623c6c81b70ab8a194f99da53735c6313ce0eab8a52c295f6480d3beb0c5`  
		Last Modified: Thu, 13 May 2021 05:22:18 GMT  
		Size: 4.3 KB (4287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7828e248c5fa27d61408e0451778465d9d6b024d1509d60bfcf7dbdabeecaa8d`  
		Last Modified: Thu, 13 May 2021 05:22:18 GMT  
		Size: 4.0 KB (3986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e99c1b6ddccc20b8fe6228bbfdfa8206c5ed8326fbea93d90302e9884bd5e6`  
		Last Modified: Thu, 13 May 2021 05:22:26 GMT  
		Size: 131.9 MB (131920004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4f382250bc674aabcfef35a3dec9e0b72a7d3624bd23c273549b0400c0b9a8`  
		Last Modified: Thu, 13 May 2021 05:22:18 GMT  
		Size: 6.1 KB (6085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
