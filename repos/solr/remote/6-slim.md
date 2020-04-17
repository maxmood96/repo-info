## `solr:6-slim`

```console
$ docker pull solr@sha256:66eec9fcdc9c4a119ea601d0f2184a025dd7c6ba5e99c01f778ec88df19e9f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `solr:6-slim` - linux; amd64

```console
$ docker pull solr@sha256:9b7b76faaf85e3e2980079b382359e882c96b0d4eecd71c239d4ffc8730553fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224812121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a36f7a6363038f663ab170bf8f8d4c7964962fdeba384d106a0d060bce04c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 10:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 10:16:26 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV JAVA_HOME=/usr/local/openjdk-8
# Thu, 16 Apr 2020 10:21:01 GMT
ENV PATH=/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:21:02 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:21:03 GMT
ENV JAVA_VERSION=8u252
# Thu, 16 Apr 2020 10:21:34 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u252-b09/OpenJDK8U-jre_
# Thu, 16 Apr 2020 10:21:35 GMT
ENV JAVA_URL_VERSION=8u252b09
# Thu, 16 Apr 2020 10:21:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -version
# Fri, 17 Apr 2020 09:53:09 GMT
LABEL maintainer=Martijn Koster "mak-docker@greenhills.co.uk"
# Fri, 17 Apr 2020 09:53:10 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Fri, 17 Apr 2020 09:53:10 GMT
ARG SOLR_VERSION=6.6.6
# Fri, 17 Apr 2020 09:53:10 GMT
ARG SOLR_SHA512=3f58b5975108ccfe95347e291a2435f8f35b69a5eeadd182fac5c19b78e6998cefcc3f217831ff9847834952f9e18753532c4982b85ed09d33bd90998753f78c
# Fri, 17 Apr 2020 09:53:10 GMT
ARG SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C
# Fri, 17 Apr 2020 09:53:11 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 17 Apr 2020 09:53:11 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 17 Apr 2020 09:53:23 GMT
# ARGS: SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=3f58b5975108ccfe95347e291a2435f8f35b69a5eeadd182fac5c19b78e6998cefcc3f217831ff9847834952f9e18753532c4982b85ed09d33bd90998753f78c SOLR_VERSION=6.6.6
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat;   rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 09:53:23 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/6.6.6/solr-6.6.6.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/6.6.6/solr-6.6.6.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/6.6.6/solr-6.6.6.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 09:53:23 GMT
ENV GOSU_VERSION=1.11
# Fri, 17 Apr 2020 09:53:24 GMT
ENV GOSU_KEY=B42F6819007F00F88E364FD4036A9C25BF357DD4
# Fri, 17 Apr 2020 09:53:24 GMT
ENV TINI_VERSION=v0.18.0
# Fri, 17 Apr 2020 09:53:24 GMT
ENV TINI_KEY=595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7
# Fri, 17 Apr 2020 09:53:26 GMT
# ARGS: SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=3f58b5975108ccfe95347e291a2435f8f35b69a5eeadd182fac5c19b78e6998cefcc3f217831ff9847834952f9e18753532c4982b85ed09d33bd90998753f78c SOLR_VERSION=6.6.6
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 17 Apr 2020 09:53:27 GMT
# ARGS: SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=3f58b5975108ccfe95347e291a2435f8f35b69a5eeadd182fac5c19b78e6998cefcc3f217831ff9847834952f9e18753532c4982b85ed09d33bd90998753f78c SOLR_VERSION=6.6.6
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS $GOSU_KEY $TINI_KEY; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Fri, 17 Apr 2020 09:53:45 GMT
# ARGS: SOLR_KEYS=2085660D9C1FCCACC4A479A3BF160FF14992A24C SOLR_SHA512=3f58b5975108ccfe95347e291a2435f8f35b69a5eeadd182fac5c19b78e6998cefcc3f217831ff9847834952f9e18753532c4982b85ed09d33bd90998753f78c SOLR_VERSION=6.6.6
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   pkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";   wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$pkgArch";   wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$pkgArch.asc";   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   rm /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true;   wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-$pkgArch";   wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-$pkgArch.asc";   gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;   rm /usr/local/bin/tini.asc;   chmod +x /usr/local/bin/tini;   tini --version;   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   mv "/opt/solr-$SOLR_VERSION" /opt/solr;   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   mkdir -p /opt/solr/server/solr/mycores /opt/solr/server/logs /opt/mysolrhome;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   if [ -f "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter" ]; then chmod 0755 "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter"; fi;   chmod -R 0755 /opt/solr/server/scripts/cloud-scripts;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/solr /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/mysolrhome;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Fri, 17 Apr 2020 09:53:46 GMT
COPY --chown=solr:solrdir:ad5f25b55b5e1dd053c2ddf3b986d9715d168efb9fedcd5c63ece6818a1f856a in /opt/docker-solr/scripts 
# Fri, 17 Apr 2020 09:53:46 GMT
EXPOSE 8983
# Fri, 17 Apr 2020 09:53:46 GMT
WORKDIR /opt/solr
# Fri, 17 Apr 2020 09:53:47 GMT
USER solr
# Fri, 17 Apr 2020 09:53:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2020 09:53:47 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2750eaebe665cac8881d45b8ac3ca818589f2e864b46191ed16b27b4839a087e`  
		Last Modified: Thu, 16 Apr 2020 10:23:39 GMT  
		Size: 3.2 MB (3249138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6194962cc7e75a338d9334e5dc2147357476bd4c67a58283763d56122df125c7`  
		Last Modified: Thu, 16 Apr 2020 10:28:20 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd6278a5cc716fe7dbd13add11ff357ca24f4c9b20d7fbc68d62c32be9c310c`  
		Last Modified: Thu, 16 Apr 2020 10:29:05 GMT  
		Size: 40.6 MB (40592816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3e4920563937a9d6ac6bfbd245ee86d5cd4701334f0e9ba0a365a47d44494f`  
		Last Modified: Fri, 17 Apr 2020 10:03:55 GMT  
		Size: 5.5 MB (5465739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6ec5e90ee44aedf5a5fc8798e4f2fda011cdaa1f3cf011f880cdf0f6dfda87`  
		Last Modified: Fri, 17 Apr 2020 10:03:52 GMT  
		Size: 4.3 KB (4287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65874673cf3d6001331afd2466778b74d8cf7c82b9387838ac56485e8c5327fa`  
		Last Modified: Fri, 17 Apr 2020 10:03:52 GMT  
		Size: 24.4 KB (24369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700bf505b0d85871e68f3e38fad2042bb7d49887014372198861e62258496072`  
		Last Modified: Fri, 17 Apr 2020 10:04:15 GMT  
		Size: 148.4 MB (148371368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2d27f8fd68e932e52156aba6c50b16c9628b60a446b153ca18df6cc782efcc`  
		Last Modified: Fri, 17 Apr 2020 10:03:52 GMT  
		Size: 6.0 KB (6046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
