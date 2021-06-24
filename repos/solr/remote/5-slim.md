## `solr:5-slim`

```console
$ docker pull solr@sha256:7ebb57e7775d7f8ac89d3077b7ccae44676c8cac34e455de3566c21390a92b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `solr:5-slim` - linux; amd64

```console
$ docker pull solr@sha256:4e75bcaa0809713233ff27d2bfcc4c24554258162cecda7f2a489cb14f9fa728
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210403577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bfba892cc60cb3b34980a3ff091b8e5dc53a2d45f0148c0fd3af4dd75bc765f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 08:00:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 08:05:30 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Wed, 23 Jun 2021 08:05:31 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Wed, 23 Jun 2021 08:05:31 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Jun 2021 08:05:32 GMT
ENV LANG=C.UTF-8
# Wed, 23 Jun 2021 08:05:32 GMT
ENV JAVA_VERSION=8u292
# Wed, 23 Jun 2021 08:06:23 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_x64_linux_8u292b10.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_aarch64_linux_8u292b10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Thu, 24 Jun 2021 04:52:34 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 24 Jun 2021 04:52:35 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 24 Jun 2021 04:53:53 GMT
ARG SOLR_VERSION=5.5.5
# Thu, 24 Jun 2021 04:53:53 GMT
ARG SOLR_SHA512=9aa02a362b75fc2af8c01d7b7d37d04450787902397644ca2d950836aa9efc8447922255d23de1d228c96f442ec82b08be64c590438dbf5f71da04616ab022f2
# Thu, 24 Jun 2021 04:53:53 GMT
ARG SOLR_KEYS=5F55943E13D49059D3F342777186B06E1ED139E7
# Thu, 24 Jun 2021 04:53:53 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 24 Jun 2021 04:53:54 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 24 Jun 2021 04:54:01 GMT
# ARGS: SOLR_KEYS=5F55943E13D49059D3F342777186B06E1ED139E7 SOLR_SHA512=9aa02a362b75fc2af8c01d7b7d37d04450787902397644ca2d950836aa9efc8447922255d23de1d228c96f442ec82b08be64c590438dbf5f71da04616ab022f2 SOLR_VERSION=5.5.5
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 24 Jun 2021 04:54:01 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/5.5.5/solr-5.5.5.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/5.5.5/solr-5.5.5.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/5.5.5/solr-5.5.5.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jun 2021 04:54:02 GMT
# ARGS: SOLR_KEYS=5F55943E13D49059D3F342777186B06E1ED139E7 SOLR_SHA512=9aa02a362b75fc2af8c01d7b7d37d04450787902397644ca2d950836aa9efc8447922255d23de1d228c96f442ec82b08be64c590438dbf5f71da04616ab022f2 SOLR_VERSION=5.5.5
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 24 Jun 2021 04:54:04 GMT
# ARGS: SOLR_KEYS=5F55943E13D49059D3F342777186B06E1ED139E7 SOLR_SHA512=9aa02a362b75fc2af8c01d7b7d37d04450787902397644ca2d950836aa9efc8447922255d23de1d228c96f442ec82b08be64c590438dbf5f71da04616ab022f2 SOLR_VERSION=5.5.5
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 24 Jun 2021 04:54:25 GMT
# ARGS: SOLR_KEYS=5F55943E13D49059D3F342777186B06E1ED139E7 SOLR_SHA512=9aa02a362b75fc2af8c01d7b7d37d04450787902397644ca2d950836aa9efc8447922255d23de1d228c96f442ec82b08be64c590438dbf5f71da04616ab022f2 SOLR_VERSION=5.5.5
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   mv "/opt/solr-$SOLR_VERSION" /opt/solr;   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   mkdir -p /opt/solr/server/solr/mycores /opt/solr/server/logs /opt/mysolrhome;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   if [ -f "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter" ]; then chmod 0755 "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter"; fi;   chmod -R 0755 /opt/solr/server/scripts/cloud-scripts;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/solr /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/mysolrhome;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 24 Jun 2021 04:54:25 GMT
COPY --chown=solr:solrdir:24d14aedda51f56007d2c3091bd65f0167210afaf1c88aa50fac48af9e1d6037 in /opt/docker-solr/scripts 
# Thu, 24 Jun 2021 04:54:26 GMT
EXPOSE 8983
# Thu, 24 Jun 2021 04:54:26 GMT
WORKDIR /opt/solr
# Thu, 24 Jun 2021 04:54:26 GMT
USER solr
# Thu, 24 Jun 2021 04:54:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 04:54:27 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee45ae9730633057cf9bd12924f9a1bf2b590631d3d085b14c96f4466557794`  
		Last Modified: Wed, 23 Jun 2021 08:12:04 GMT  
		Size: 3.3 MB (3268886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3346229aaa8035c095bb0a01147fa25b7ee72d62fb757cbd2dcf092c2822075a`  
		Last Modified: Wed, 23 Jun 2021 08:20:57 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6ce9b3b72220698f274bfe3d2bb2657f171f632c75c66efc8f8b055cc0aefc`  
		Last Modified: Wed, 23 Jun 2021 08:22:01 GMT  
		Size: 41.6 MB (41598850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e679aa16ea9680f25f2868e46ab3f0d10ab0f5e37d96a4c1fbdf6dac2bdb79`  
		Last Modified: Thu, 24 Jun 2021 05:04:22 GMT  
		Size: 6.5 MB (6455410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb75f3880adfc0d6670c32866cb66d14e6a20ddf40fc36d82ec17e2901a0902`  
		Last Modified: Thu, 24 Jun 2021 05:04:21 GMT  
		Size: 4.3 KB (4287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5abfeabe9d2cb75460d938ce8c4127e575e50df5e431871dea343d7c0c9161`  
		Last Modified: Thu, 24 Jun 2021 05:04:21 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355215940bb4eba65700a63aa2415c0ec2b6a14abed3fc97519d97e9fcba8a7a`  
		Last Modified: Thu, 24 Jun 2021 05:04:29 GMT  
		Size: 131.9 MB (131920010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718d8cb32e1fec605c4b1bb33f6e2118c1269aa28ecfe75c5269341ab8ad1c70`  
		Last Modified: Thu, 24 Jun 2021 05:04:21 GMT  
		Size: 6.1 KB (6082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
