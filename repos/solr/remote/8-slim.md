## `solr:8-slim`

```console
$ docker pull solr@sha256:d18c2c87a969ea44af6e14454ef47d279394f9ca56fd1c5319f298ea24f45f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `solr:8-slim` - linux; amd64

```console
$ docker pull solr@sha256:7f8aae338998c0093d2b6fa20c6ab42d4f08a5011b84a4da8d7590f677aab108
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284814985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5649c1bb3b7df9d4e2fa2eebc0275b78712d247ac2bc95d1448fffc9aa471f2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:53:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 19:54:47 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Mon, 01 Feb 2021 19:54:48 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 19:54:48 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:54:48 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 19:54:49 GMT
ENV JAVA_VERSION=11.0.10
# Mon, 01 Feb 2021 19:56:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_x64_linux_11.0.10_9.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_aarch64_linux_11.0.10_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Mon, 01 Feb 2021 22:21:26 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Mon, 01 Feb 2021 22:21:26 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Mon, 01 Feb 2021 22:21:26 GMT
ARG SOLR_VERSION=8.7.0
# Mon, 01 Feb 2021 22:21:26 GMT
ARG SOLR_SHA512=15a3af83997e2cbc4bfed304f7d43efd260674d98059241605ff3cde0ae02d8bd1ccd56973c6cba1cc11895655bb76fcf1991bbb94b004e517ce15f728fa163f
# Mon, 01 Feb 2021 22:21:27 GMT
ARG SOLR_KEYS=7D8D90F8F64F23077AC87CF7CB77CB79928BB0EC
# Mon, 01 Feb 2021 22:21:27 GMT
ARG SOLR_DOWNLOAD_URL
# Mon, 01 Feb 2021 22:21:27 GMT
ARG SOLR_DOWNLOAD_SERVER
# Mon, 01 Feb 2021 22:21:36 GMT
# ARGS: SOLR_KEYS=7D8D90F8F64F23077AC87CF7CB77CB79928BB0EC SOLR_SHA512=15a3af83997e2cbc4bfed304f7d43efd260674d98059241605ff3cde0ae02d8bd1ccd56973c6cba1cc11895655bb76fcf1991bbb94b004e517ce15f728fa163f SOLR_VERSION=8.7.0
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Mon, 01 Feb 2021 22:21:36 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.7.0/solr-8.7.0.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.7.0/solr-8.7.0.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.7.0/solr-8.7.0.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Mon, 01 Feb 2021 22:21:37 GMT
# ARGS: SOLR_KEYS=7D8D90F8F64F23077AC87CF7CB77CB79928BB0EC SOLR_SHA512=15a3af83997e2cbc4bfed304f7d43efd260674d98059241605ff3cde0ae02d8bd1ccd56973c6cba1cc11895655bb76fcf1991bbb94b004e517ce15f728fa163f SOLR_VERSION=8.7.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Mon, 01 Feb 2021 22:21:38 GMT
# ARGS: SOLR_KEYS=7D8D90F8F64F23077AC87CF7CB77CB79928BB0EC SOLR_SHA512=15a3af83997e2cbc4bfed304f7d43efd260674d98059241605ff3cde0ae02d8bd1ccd56973c6cba1cc11895655bb76fcf1991bbb94b004e517ce15f728fa163f SOLR_VERSION=8.7.0
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Mon, 01 Feb 2021 22:22:05 GMT
# ARGS: SOLR_KEYS=7D8D90F8F64F23077AC87CF7CB77CB79928BB0EC SOLR_SHA512=15a3af83997e2cbc4bfed304f7d43efd260674d98059241605ff3cde0ae02d8bd1ccd56973c6cba1cc11895655bb76fcf1991bbb94b004e517ce15f728fa163f SOLR_VERSION=8.7.0
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Mon, 01 Feb 2021 22:22:05 GMT
COPY --chown=0:0dir:9bc5f3733a819401f8f06067a2f41713605d2c3bb03bbbe92d04dc2f83bd0265 in /opt/docker-solr/scripts 
# Mon, 01 Feb 2021 22:22:06 GMT
VOLUME [/var/solr]
# Mon, 01 Feb 2021 22:22:06 GMT
EXPOSE 8983
# Mon, 01 Feb 2021 22:22:06 GMT
WORKDIR /opt/solr
# Mon, 01 Feb 2021 22:22:06 GMT
USER solr
# Mon, 01 Feb 2021 22:22:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Feb 2021 22:22:07 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943d8acaac04a2b66af03bcc85abe1cd3f50e06d7e193634e04d4e55c4fc7cc8`  
		Last Modified: Tue, 12 Jan 2021 11:07:22 GMT  
		Size: 3.2 MB (3248558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0601982f39d5609688d3d24a2f70ac6655e1628df369aa95dcda6ad9aab845f0`  
		Last Modified: Mon, 01 Feb 2021 20:09:27 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0940164d1964ff9d11b1aea461a6fa253e1300e97f204bec73f228f11d3acf`  
		Last Modified: Mon, 01 Feb 2021 20:10:22 GMT  
		Size: 47.0 MB (47036369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af55280ac8a1d45c2ea1488f7e4df740c261f3978dc694699dbc5eb28261711`  
		Last Modified: Mon, 01 Feb 2021 22:46:02 GMT  
		Size: 6.5 MB (6453919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e9c7d7fa786bb4efb0fd7a4cb75d10a17c7663ab90cce7bb5eef2bf716a646`  
		Last Modified: Mon, 01 Feb 2021 22:46:01 GMT  
		Size: 4.3 KB (4292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50fecfc28e540f1fa21e59d8a95a4e1ecfbd3ab81aadcc6bd7a174f2af891bc`  
		Last Modified: Mon, 01 Feb 2021 22:46:00 GMT  
		Size: 2.4 KB (2355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b579375715b8b1fca80117218f380318cf7192dfc054f56a9cf62698ebc4688c`  
		Last Modified: Mon, 01 Feb 2021 22:46:13 GMT  
		Size: 201.0 MB (200954962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4f944375370839da73719dabec260eb0cb7cfbf4c241f3eb28f4181d84122e`  
		Last Modified: Mon, 01 Feb 2021 22:46:00 GMT  
		Size: 6.2 KB (6249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:8-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:0c5dbb7e8d7b6187626f1e106db8f9a295a41ef4a0f05ceb31238c0967e68b94
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282388041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:117797d82b0c120018de77fbbe4fe7561621e44153e2d10c26ed7d76bd19fcba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:13 GMT
ADD file:0252dccbbfb76766e0e189783d38f6a6afd13f44daa7c5370ffd094adea0f583 in / 
# Tue, 12 Jan 2021 00:41:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:00:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 01 Feb 2021 20:35:15 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Mon, 01 Feb 2021 20:35:17 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Mon, 01 Feb 2021 20:35:17 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 20:35:18 GMT
ENV LANG=C.UTF-8
# Mon, 01 Feb 2021 20:35:19 GMT
ENV JAVA_VERSION=11.0.10
# Mon, 01 Feb 2021 20:37:04 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_x64_linux_11.0.10_9.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jre_aarch64_linux_11.0.10_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Mon, 01 Feb 2021 22:34:39 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Mon, 01 Feb 2021 22:34:40 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Mon, 01 Feb 2021 22:34:41 GMT
ARG SOLR_VERSION=8.7.0
# Mon, 01 Feb 2021 22:34:41 GMT
ARG SOLR_SHA512=15a3af83997e2cbc4bfed304f7d43efd260674d98059241605ff3cde0ae02d8bd1ccd56973c6cba1cc11895655bb76fcf1991bbb94b004e517ce15f728fa163f
# Mon, 01 Feb 2021 22:34:42 GMT
ARG SOLR_KEYS=7D8D90F8F64F23077AC87CF7CB77CB79928BB0EC
# Mon, 01 Feb 2021 22:34:43 GMT
ARG SOLR_DOWNLOAD_URL
# Mon, 01 Feb 2021 22:34:43 GMT
ARG SOLR_DOWNLOAD_SERVER
# Mon, 01 Feb 2021 22:35:00 GMT
# ARGS: SOLR_KEYS=7D8D90F8F64F23077AC87CF7CB77CB79928BB0EC SOLR_SHA512=15a3af83997e2cbc4bfed304f7d43efd260674d98059241605ff3cde0ae02d8bd1ccd56973c6cba1cc11895655bb76fcf1991bbb94b004e517ce15f728fa163f SOLR_VERSION=8.7.0
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Mon, 01 Feb 2021 22:35:01 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.7.0/solr-8.7.0.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.7.0/solr-8.7.0.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.7.0/solr-8.7.0.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Mon, 01 Feb 2021 22:35:04 GMT
# ARGS: SOLR_KEYS=7D8D90F8F64F23077AC87CF7CB77CB79928BB0EC SOLR_SHA512=15a3af83997e2cbc4bfed304f7d43efd260674d98059241605ff3cde0ae02d8bd1ccd56973c6cba1cc11895655bb76fcf1991bbb94b004e517ce15f728fa163f SOLR_VERSION=8.7.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Mon, 01 Feb 2021 22:35:07 GMT
# ARGS: SOLR_KEYS=7D8D90F8F64F23077AC87CF7CB77CB79928BB0EC SOLR_SHA512=15a3af83997e2cbc4bfed304f7d43efd260674d98059241605ff3cde0ae02d8bd1ccd56973c6cba1cc11895655bb76fcf1991bbb94b004e517ce15f728fa163f SOLR_VERSION=8.7.0
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Mon, 01 Feb 2021 22:35:24 GMT
# ARGS: SOLR_KEYS=7D8D90F8F64F23077AC87CF7CB77CB79928BB0EC SOLR_SHA512=15a3af83997e2cbc4bfed304f7d43efd260674d98059241605ff3cde0ae02d8bd1ccd56973c6cba1cc11895655bb76fcf1991bbb94b004e517ce15f728fa163f SOLR_VERSION=8.7.0
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Mon, 01 Feb 2021 22:35:27 GMT
COPY --chown=0:0dir:9bc5f3733a819401f8f06067a2f41713605d2c3bb03bbbe92d04dc2f83bd0265 in /opt/docker-solr/scripts 
# Mon, 01 Feb 2021 22:35:28 GMT
VOLUME [/var/solr]
# Mon, 01 Feb 2021 22:35:29 GMT
EXPOSE 8983
# Mon, 01 Feb 2021 22:35:30 GMT
WORKDIR /opt/solr
# Mon, 01 Feb 2021 22:35:31 GMT
USER solr
# Mon, 01 Feb 2021 22:35:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Feb 2021 22:35:33 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:f8be76fcf2062bd14a3a78f858da701db8bcd907a2d0f33716d89d9329df2b1f`  
		Last Modified: Tue, 12 Jan 2021 00:51:54 GMT  
		Size: 25.9 MB (25864492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6132c56bf059fe6b3844038ac4ca6b320af5f511b4c60addc956fb470ebfcb8`  
		Last Modified: Tue, 12 Jan 2021 01:11:08 GMT  
		Size: 3.1 MB (3101516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc7648cbf49cb708b3941896176a489b3bd0a6c647d780f02dfc5b53ee4d1e7`  
		Last Modified: Mon, 01 Feb 2021 20:50:28 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4762ce56b9855a080532cf6f44e1e3ad67c234e9e95006d1f4e897007dd89600`  
		Last Modified: Mon, 01 Feb 2021 20:51:53 GMT  
		Size: 46.1 MB (46103395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ef8184fa20ffd3b2f6825c88e4c48d523aa9e7bded76394b2ee0ad02c3f26f`  
		Last Modified: Mon, 01 Feb 2021 22:56:05 GMT  
		Size: 6.4 MB (6350394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d8c60080135aa6a4f97dcb0cbfccc5cce66a81389b50febe3fe9e47d72149e`  
		Last Modified: Mon, 01 Feb 2021 22:56:04 GMT  
		Size: 4.3 KB (4325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c463afe4646188ec64267601c2a2d61557c1d392a181caa8ea271881be2c81f`  
		Last Modified: Mon, 01 Feb 2021 22:56:04 GMT  
		Size: 2.4 KB (2388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b63a6185c5cb2ddadab2892ff2a59c97cf509d1da792766b927e562c8d54e3`  
		Last Modified: Mon, 01 Feb 2021 22:56:33 GMT  
		Size: 201.0 MB (200955044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbce87070162559448ae7a514201112efa796268b26c33947e45c94a7229c4a`  
		Last Modified: Mon, 01 Feb 2021 22:56:04 GMT  
		Size: 6.3 KB (6274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
