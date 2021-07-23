## `solr:slim`

```console
$ docker pull solr@sha256:77a3467f639b696e97a76b6611bff7ee8a31625c7e9b6b5b70c35571ddaeef75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `solr:slim` - linux; amd64

```console
$ docker pull solr@sha256:c93672b8d37ae881a07d27f3458a92b8f9e51d3aa22eb16472dbf5f8a570ac18
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287108533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d59563004903985b96d7a285ea327a51013a13f481877869b134f3aef331a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 13:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 13:36:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 22 Jul 2021 13:36:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 22 Jul 2021 13:36:14 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 13:36:14 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 13:36:14 GMT
ENV JAVA_VERSION=11.0.12
# Thu, 22 Jul 2021 13:37:11 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Fri, 23 Jul 2021 08:58:32 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Fri, 23 Jul 2021 08:58:32 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Fri, 23 Jul 2021 08:58:32 GMT
ARG SOLR_VERSION=8.9.0
# Fri, 23 Jul 2021 08:58:33 GMT
ARG SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242
# Fri, 23 Jul 2021 08:58:33 GMT
ARG SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969
# Fri, 23 Jul 2021 08:58:33 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 23 Jul 2021 08:58:33 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 23 Jul 2021 08:58:40 GMT
# ARGS: SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969 SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242 SOLR_VERSION=8.9.0
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Fri, 23 Jul 2021 08:58:40 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.9.0/solr-8.9.0.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.9.0/solr-8.9.0.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.9.0/solr-8.9.0.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Fri, 23 Jul 2021 08:58:41 GMT
# ARGS: SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969 SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242 SOLR_VERSION=8.9.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 23 Jul 2021 08:58:42 GMT
# ARGS: SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969 SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242 SOLR_VERSION=8.9.0
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Fri, 23 Jul 2021 08:59:01 GMT
# ARGS: SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969 SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242 SOLR_VERSION=8.9.0
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Fri, 23 Jul 2021 08:59:01 GMT
COPY --chown=0:0dir:9bc5f3733a819401f8f06067a2f41713605d2c3bb03bbbe92d04dc2f83bd0265 in /opt/docker-solr/scripts 
# Fri, 23 Jul 2021 08:59:01 GMT
VOLUME [/var/solr]
# Fri, 23 Jul 2021 08:59:02 GMT
EXPOSE 8983
# Fri, 23 Jul 2021 08:59:02 GMT
WORKDIR /opt/solr
# Fri, 23 Jul 2021 08:59:02 GMT
USER solr
# Fri, 23 Jul 2021 08:59:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 08:59:03 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d5ef013a6164e3b6c391252d0a26dbd18a3c564f734d771b4033a83f6d84a9`  
		Last Modified: Thu, 22 Jul 2021 13:43:45 GMT  
		Size: 3.3 MB (3268756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6aa028937a70f85a710a428a58ddccddd63e2905c6b765e9bfb7f50bd51959`  
		Last Modified: Thu, 22 Jul 2021 13:48:54 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabac214cb3b9a892e4c2d0e5d1a5ee9293220c1362ef892a3cd10d52481cefc`  
		Last Modified: Thu, 22 Jul 2021 13:50:23 GMT  
		Size: 47.1 MB (47136368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fbb91175ada6c138daa34f48ac45d2bc8e3acce8c62bdac22d061bcf4d19bb`  
		Last Modified: Fri, 23 Jul 2021 09:18:44 GMT  
		Size: 6.5 MB (6455442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0b16885e4c7b312eb035a551c56b48ad5b7cdc7f1dd1ace898bec254907f40`  
		Last Modified: Fri, 23 Jul 2021 09:18:43 GMT  
		Size: 4.3 KB (4288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fc92cefe75eae4b2cb9b43b94fa2f995e09830231acad09b1ca5e9beb9e324`  
		Last Modified: Fri, 23 Jul 2021 09:18:43 GMT  
		Size: 2.9 KB (2914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f50c54d776c991b182dce4c470a0a955276b9706c2d4fd568870a975089c71`  
		Last Modified: Fri, 23 Jul 2021 09:18:53 GMT  
		Size: 203.1 MB (203088484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd6ba8cf4f0647cbd3d2a793ba49c81fcbf331b5eaa03e707d90c800105c45f`  
		Last Modified: Fri, 23 Jul 2021 09:18:43 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:b5e6f9f573b88fc0709b21017720798299df61684cda571a39a1605d630158f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.7 MB (284691775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b93a77ccf081a7110fb78183c4be21059b46b7522b8d7ea395ebabf4a793cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:14 GMT
ADD file:074ffc2065bab83c9a5c596576656b04d271dd78406aadad160b68e38f38269f in / 
# Thu, 22 Jul 2021 00:40:14 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 05:15:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 05:19:20 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 22 Jul 2021 05:19:21 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ] # backwards compatibility
# Thu, 22 Jul 2021 05:19:21 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 05:19:21 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 05:19:22 GMT
ENV JAVA_VERSION=11.0.12
# Thu, 22 Jul 2021 05:20:28 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_linux_11.0.12_7.tar.gz'; 			;; 		'arm64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_aarch64_linux_11.0.12_7.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	wget --progress=dot:giga -O openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		java --version
# Thu, 22 Jul 2021 20:50:05 GMT
LABEL maintainer=The Apache Lucene/Solr Project
# Thu, 22 Jul 2021 20:50:05 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Thu, 22 Jul 2021 20:50:05 GMT
ARG SOLR_VERSION=8.9.0
# Thu, 22 Jul 2021 20:50:05 GMT
ARG SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242
# Thu, 22 Jul 2021 20:50:05 GMT
ARG SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969
# Thu, 22 Jul 2021 20:50:06 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 22 Jul 2021 20:50:06 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 22 Jul 2021 20:50:17 GMT
# ARGS: SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969 SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242 SOLR_VERSION=8.9.0
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat gosu tini;   rm -rf /var/lib/apt/lists/*;   cd /usr/local/bin; wget -nv https://github.com/apangin/jattach/releases/download/v1.5/jattach; chmod 755 jattach;   echo >jattach.sha512 "d8eedbb3e192a8596c08efedff99b9acf1075331e1747107c07cdb1718db2abe259ef168109e46bd4cf80d47d43028ff469f95e6ddcbdda4d7ffa73a20e852f9  jattach";   sha512sum -c jattach.sha512; rm jattach.sha512
# Thu, 22 Jul 2021 20:50:17 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/8.9.0/solr-8.9.0.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/8.9.0/solr-8.9.0.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/8.9.0/solr-8.9.0.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml
# Thu, 22 Jul 2021 20:50:18 GMT
# ARGS: SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969 SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242 SOLR_VERSION=8.9.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 22 Jul 2021 20:50:19 GMT
# ARGS: SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969 SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242 SOLR_VERSION=8.9.0
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Thu, 22 Jul 2021 20:50:36 GMT
# ARGS: SOLR_KEYS=9722F25F650057E26C803B60A6D064D833B3A969 SOLR_SHA512=15150b7f191fd9e8d2c1bd8bb619dd4b3f27af2e0e94b7609031f7e745a2e263391c30f68865c208afb97ccaa9bde6d16050200e9bfccef65f762c2ed743c242 SOLR_VERSION=8.9.0
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   (cd /opt; ln -s "solr-$SOLR_VERSION" solr);   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R 0:0 "/opt/solr-$SOLR_VERSION";   find "/opt/solr-$SOLR_VERSION" -type d -print0 | xargs -0 chmod 0755;   find "/opt/solr-$SOLR_VERSION" -type f -print0 | xargs -0 chmod 0644;   chmod -R 0755 "/opt/solr-$SOLR_VERSION/bin" "/opt/solr-$SOLR_VERSION/contrib/prometheus-exporter/bin/solr-exporter" /opt/solr-$SOLR_VERSION/server/scripts/cloud-scripts;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chown root:0 /etc/default/solr.in.sh;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p /var/solr/data /var/solr/logs;   (cd /opt/solr/server/solr; cp solr.xml zoo.cfg /var/solr/data/);   cp /opt/solr/server/resources/log4j2.xml /var/solr/log4j2.xml;   find /var/solr -type d -print0 | xargs -0 chmod 0770;   find /var/solr -type f -print0 | xargs -0 chmod 0660;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   chown -R "0:0" /opt/solr-$SOLR_VERSION /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:0" /var/solr;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Thu, 22 Jul 2021 20:50:36 GMT
COPY --chown=0:0dir:9bc5f3733a819401f8f06067a2f41713605d2c3bb03bbbe92d04dc2f83bd0265 in /opt/docker-solr/scripts 
# Thu, 22 Jul 2021 20:50:36 GMT
VOLUME [/var/solr]
# Thu, 22 Jul 2021 20:50:37 GMT
EXPOSE 8983
# Thu, 22 Jul 2021 20:50:37 GMT
WORKDIR /opt/solr
# Thu, 22 Jul 2021 20:50:37 GMT
USER solr
# Thu, 22 Jul 2021 20:50:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jul 2021 20:50:37 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:513c6babab2b9079da61a69300c0e26d1037ca98910376098e9ae87baeb112c0`  
		Last Modified: Thu, 22 Jul 2021 00:45:53 GMT  
		Size: 25.9 MB (25914794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e464611cad28e3191fb5458b5b6b9bbcfd879d9863a4aa29debea8bf188cc100`  
		Last Modified: Thu, 22 Jul 2021 05:30:12 GMT  
		Size: 3.1 MB (3118880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1072d9f3862c6a624e0bfd318de35256b27e48842c71dc09bc7c198851a6e719`  
		Last Modified: Thu, 22 Jul 2021 05:36:37 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e02df45a8f59804b8364ef9d623c77c88f9b9cb152bc07da97ae8e2f49488f`  
		Last Modified: Thu, 22 Jul 2021 05:38:14 GMT  
		Size: 46.2 MB (46205548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0f931cdecbce8540b48a6543da1355c2c8710c15cc37c7b6036d332e5857df`  
		Last Modified: Thu, 22 Jul 2021 21:08:26 GMT  
		Size: 6.4 MB (6350374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026192759d604dba2658aecf86993d46ad9a74285b98b14263b27658feb57b3e`  
		Last Modified: Thu, 22 Jul 2021 21:08:25 GMT  
		Size: 4.3 KB (4324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e9da0564ec7efa1087f95a27480861c195ee41fa37c8e4502dbb5a7fae6c6f`  
		Last Modified: Thu, 22 Jul 2021 21:08:25 GMT  
		Size: 2.9 KB (2912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e684cdfdf2152e74fc770d6be31f47008024d3055042b254f4a4909dbc6d0f`  
		Last Modified: Thu, 22 Jul 2021 21:08:38 GMT  
		Size: 203.1 MB (203088457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5780a6aabcbbe914c2cba82fde6dc4a2c44bd55be491b3fd4fc8c2c5b524096`  
		Last Modified: Thu, 22 Jul 2021 21:08:25 GMT  
		Size: 6.3 KB (6276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
