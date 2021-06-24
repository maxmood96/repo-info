## `solr:6-slim`

```console
$ docker pull solr@sha256:a2cd4fef07b31643a13bbd8c5b90caf4c30b9652e6f9d6612525c53ccc4de30c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `solr:6-slim` - linux; amd64

```console
$ docker pull solr@sha256:6b715a71179e6f0d9eebe2b66d24a6de4a7be47939a52e4183dd4ac594c5d094
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225943468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7f0f58b39af179f0055ceb01bd0e2859628815dd247825411556f0943088`
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
# Thu, 24 Jun 2021 04:52:35 GMT
ARG SOLR_VERSION=6.6.6
# Thu, 24 Jun 2021 04:52:35 GMT
ARG SOLR_SHA512=3f58b5975108ccfe95347e291a2435f8f35b69a5eeadd182fac5c19b78e6998cefcc3f217831ff9847834952f9e18753532c4982b85ed09d33bd90998753f78c
# Thu, 24 Jun 2021 04:52:35 GMT
ARG SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C
# Thu, 24 Jun 2021 04:52:35 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 24 Jun 2021 04:52:35 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 24 Jun 2021 04:52:43 GMT
# ARGS: SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=3f58b5975108ccfe95347e291a2435f8f35b69a5eeadd182fac5c19b78e6998cefcc3f217831ff9847834952f9e18753532c4982b85ed09d33bd90998753f78c SOLR_VERSION=6.6.6
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 24 Jun 2021 04:52:43 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/6.6.6/solr-6.6.6.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/6.6.6/solr-6.6.6.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/6.6.6/solr-6.6.6.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Jun 2021 04:52:44 GMT
# ARGS: SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=3f58b5975108ccfe95347e291a2435f8f35b69a5eeadd182fac5c19b78e6998cefcc3f217831ff9847834952f9e18753532c4982b85ed09d33bd90998753f78c SOLR_VERSION=6.6.6
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 24 Jun 2021 04:52:47 GMT
# ARGS: SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=3f58b5975108ccfe95347e291a2435f8f35b69a5eeadd182fac5c19b78e6998cefcc3f217831ff9847834952f9e18753532c4982b85ed09d33bd90998753f78c SOLR_VERSION=6.6.6
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 24 Jun 2021 04:53:09 GMT
# ARGS: SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=3f58b5975108ccfe95347e291a2435f8f35b69a5eeadd182fac5c19b78e6998cefcc3f217831ff9847834952f9e18753532c4982b85ed09d33bd90998753f78c SOLR_VERSION=6.6.6
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   mv "/opt/solr-$SOLR_VERSION" /opt/solr;   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   mkdir -p /opt/solr/server/solr/mycores /opt/solr/server/logs /opt/mysolrhome;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   if [ -f "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter" ]; then chmod 0755 "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter"; fi;   chmod -R 0755 /opt/solr/server/scripts/cloud-scripts;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/solr /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/mysolrhome;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 24 Jun 2021 04:53:10 GMT
COPY --chown=solr:solrdir:24d14aedda51f56007d2c3091bd65f0167210afaf1c88aa50fac48af9e1d6037 in /opt/docker-solr/scripts 
# Thu, 24 Jun 2021 04:53:10 GMT
EXPOSE 8983
# Thu, 24 Jun 2021 04:53:10 GMT
WORKDIR /opt/solr
# Thu, 24 Jun 2021 04:53:10 GMT
USER solr
# Thu, 24 Jun 2021 04:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 04:53:10 GMT
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
	-	`sha256:c672058afeee49862e61a43d6f0b0adc2d58dbf6319dbb00102252350a61e53a`  
		Last Modified: Thu, 24 Jun 2021 05:03:36 GMT  
		Size: 6.5 MB (6455406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5f627e8bfa260f4cbd88e6483a7d782368bcda75c83193d39700a8087aa33c`  
		Last Modified: Thu, 24 Jun 2021 05:03:35 GMT  
		Size: 4.3 KB (4284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4385e86abfac0696a710cc0073a83261fdb530be2bfba77e09f5ee433fa88f62`  
		Last Modified: Thu, 24 Jun 2021 05:03:35 GMT  
		Size: 2.9 KB (2900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca83d243e77857e89cafa092e069f6dd7661f07179ef8baa9be915813f312de`  
		Last Modified: Thu, 24 Jun 2021 05:03:43 GMT  
		Size: 147.5 MB (147460995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d6f72fee0fc1c44788395015f30d575b76a7886328158dc182fb266fa71081`  
		Last Modified: Thu, 24 Jun 2021 05:03:35 GMT  
		Size: 6.1 KB (6084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
