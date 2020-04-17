## `solr:7-slim`

```console
$ docker pull solr@sha256:d5b5a2cd2f0601b3048ca1299949308c97e3efd45091ccd73ac018242fc29570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `solr:7-slim` - linux; amd64

```console
$ docker pull solr@sha256:27fd989de77abe79bf6dd4c0c5290491d491771913f764c4e8257d7623e21953
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250487274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c44a3c45fd42b4fd1e7ff5b2fd85f659c7e0aa4dd7fcdd6491cc211ac84fd17`
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
# Thu, 16 Apr 2020 10:19:13 GMT
ENV JAVA_HOME=/usr/local/openjdk-11
# Thu, 16 Apr 2020 10:19:13 GMT
ENV PATH=/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 10:19:14 GMT
RUN { echo '#/bin/sh'; echo 'echo "$JAVA_HOME"'; } > /usr/local/bin/docker-java-home && chmod +x /usr/local/bin/docker-java-home && [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Thu, 16 Apr 2020 10:19:14 GMT
ENV JAVA_VERSION=11.0.7
# Thu, 16 Apr 2020 10:20:16 GMT
ENV JAVA_BASE_URL=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.7%2B10/OpenJDK11U-jre_
# Thu, 16 Apr 2020 10:20:16 GMT
ENV JAVA_URL_VERSION=11.0.7_10
# Thu, 16 Apr 2020 10:20:33 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64) upstreamArch='x64' ;; 		arm64) upstreamArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture: $dpkgArch" ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O openjdk.tgz.asc "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz.sign"; 	wget -O openjdk.tgz "${JAVA_BASE_URL}${upstreamArch}_linux_${JAVA_URL_VERSION}.tar.gz" --progress=dot:giga; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'if ! [ -d "$JAVA_HOME" ]; then echo >&2 "error: missing JAVA_HOME environment variable"; exit 1; fi'; 		echo 'cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done'; 		echo 'if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$cacertsFile"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java --version
# Fri, 17 Apr 2020 09:40:13 GMT
LABEL maintainer=Martijn Koster "mak-docker@greenhills.co.uk"
# Fri, 17 Apr 2020 09:40:14 GMT
LABEL repository=https://github.com/docker-solr/docker-solr
# Fri, 17 Apr 2020 09:51:35 GMT
ARG SOLR_VERSION=7.7.2
# Fri, 17 Apr 2020 09:51:35 GMT
ARG SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85
# Fri, 17 Apr 2020 09:51:36 GMT
ARG SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E
# Fri, 17 Apr 2020 09:51:36 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 17 Apr 2020 09:51:36 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 17 Apr 2020 09:51:49 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85 SOLR_VERSION=7.7.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat;   rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 09:51:49 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/7.7.2/solr-7.7.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/7.7.2/solr-7.7.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/7.7.2/solr-7.7.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 09:51:50 GMT
ENV GOSU_VERSION=1.11
# Fri, 17 Apr 2020 09:51:50 GMT
ENV GOSU_KEY=B42F6819007F00F88E364FD4036A9C25BF357DD4
# Fri, 17 Apr 2020 09:51:50 GMT
ENV TINI_VERSION=v0.18.0
# Fri, 17 Apr 2020 09:51:51 GMT
ENV TINI_KEY=595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7
# Fri, 17 Apr 2020 09:51:52 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85 SOLR_VERSION=7.7.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 17 Apr 2020 09:51:54 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85 SOLR_VERSION=7.7.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS $GOSU_KEY $TINI_KEY; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Fri, 17 Apr 2020 09:52:11 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85 SOLR_VERSION=7.7.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   pkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";   wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$pkgArch";   wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$pkgArch.asc";   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   rm /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true;   wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-$pkgArch";   wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-$pkgArch.asc";   gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;   rm /usr/local/bin/tini.asc;   chmod +x /usr/local/bin/tini;   tini --version;   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   mv "/opt/solr-$SOLR_VERSION" /opt/solr;   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   mkdir -p /opt/solr/server/solr/mycores /opt/solr/server/logs /opt/mysolrhome;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   if [ -f "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter" ]; then chmod 0755 "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter"; fi;   chmod -R 0755 /opt/solr/server/scripts/cloud-scripts;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/solr /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/mysolrhome;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Fri, 17 Apr 2020 09:52:12 GMT
COPY --chown=solr:solrdir:ad5f25b55b5e1dd053c2ddf3b986d9715d168efb9fedcd5c63ece6818a1f856a in /opt/docker-solr/scripts 
# Fri, 17 Apr 2020 09:52:12 GMT
EXPOSE 8983
# Fri, 17 Apr 2020 09:52:12 GMT
WORKDIR /opt/solr
# Fri, 17 Apr 2020 09:52:13 GMT
USER solr
# Fri, 17 Apr 2020 09:52:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2020 09:52:14 GMT
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
	-	`sha256:98ad45fdc1358fe836a11f8750e2d244ac475142f1e4e3570954e98a2facd7bc`  
		Last Modified: Thu, 16 Apr 2020 10:26:45 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51062359ac505e3fe04d4099b00c6ffbf57552f66e928de3296199592a980f9`  
		Last Modified: Thu, 16 Apr 2020 10:27:41 GMT  
		Size: 42.2 MB (42214702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672ebf4bd35aef8957e9ea4a9b92111186cd890c72d5d4cdf9e42ee73b2c42af`  
		Last Modified: Fri, 17 Apr 2020 10:03:15 GMT  
		Size: 5.5 MB (5465769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64703b10c09fb06282cca8082f91077ddc858703d15b43c2af0f4a68bf1aec58`  
		Last Modified: Fri, 17 Apr 2020 10:03:14 GMT  
		Size: 4.3 KB (4284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb8b755bd2d09b56f39977685af2ee55c2a36e875e7c2e54848943464fc7d40`  
		Last Modified: Fri, 17 Apr 2020 10:03:13 GMT  
		Size: 26.6 KB (26584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae3c2e13facb2b6af07cade6822993326c90f0b48e27b2cc4f2d128b39cb94a`  
		Last Modified: Fri, 17 Apr 2020 10:03:27 GMT  
		Size: 172.4 MB (172422388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e970d7ad5ab5a5edbc5a5725efa4635af4a47fdf67a71acacfb3c013d9e3d6b`  
		Last Modified: Fri, 17 Apr 2020 10:03:14 GMT  
		Size: 6.0 KB (6050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:7-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:af8f05345424335a12dc6060202044ebc699c22cb6c509af6df2865c2a0a917c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248123353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c55169e2c59fc1093a20c96bbeafdc7bf4f7d7af5779a7def584f16a14a804`
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
# Fri, 17 Apr 2020 03:23:40 GMT
ARG SOLR_VERSION=7.7.2
# Fri, 17 Apr 2020 03:23:41 GMT
ARG SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85
# Fri, 17 Apr 2020 03:23:41 GMT
ARG SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E
# Fri, 17 Apr 2020 03:23:42 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 17 Apr 2020 03:23:42 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 17 Apr 2020 03:23:58 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85 SOLR_VERSION=7.7.2
RUN set -ex;   apt-get update;   apt-get -y install acl dirmngr gpg lsof procps wget netcat;   rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 03:23:59 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?filename=lucene/solr/7.7.2/solr-7.7.2.tgz&action=download SOLR_DIST_URL=https://www.apache.org/dist/lucene/solr/7.7.2/solr-7.7.2.tgz SOLR_ARCHIVE_URL=https://archive.apache.org/dist/lucene/solr/7.7.2/solr-7.7.2.tgz PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2020 03:23:59 GMT
ENV GOSU_VERSION=1.11
# Fri, 17 Apr 2020 03:24:00 GMT
ENV GOSU_KEY=B42F6819007F00F88E364FD4036A9C25BF357DD4
# Fri, 17 Apr 2020 03:24:00 GMT
ENV TINI_VERSION=v0.18.0
# Fri, 17 Apr 2020 03:24:01 GMT
ENV TINI_KEY=595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7
# Fri, 17 Apr 2020 03:24:03 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85 SOLR_VERSION=7.7.2
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 17 Apr 2020 03:24:05 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85 SOLR_VERSION=7.7.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   for key in $SOLR_KEYS $GOSU_KEY $TINI_KEY; do     found='';     for server in       ha.pool.sks-keyservers.net       hkp://keyserver.ubuntu.com:80       hkp://p80.pool.sks-keyservers.net:80       pgp.mit.edu     ; do       echo "  trying $server for $key";       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;       gpg --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$key" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch $key from several disparate servers -- network issues?" && exit 1;   done;   exit 0
# Fri, 17 Apr 2020 03:24:28 GMT
# ARGS: SOLR_KEYS=2CECBFBA181601547B654B9FFA81AC8A490F538E SOLR_SHA512=a785e3fae1f46423fe857b443760b5007e484b3f23e0137f42689515c5d0d1dadf518f03a1813e071d65831cdb161b602962b8688d987e5725006087ca507f85 SOLR_VERSION=7.7.2
RUN set -ex;   export GNUPGHOME="/tmp/gnupg_home";   pkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";   wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$pkgArch";   wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$pkgArch.asc";   gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;   rm /usr/local/bin/gosu.asc;   chmod +x /usr/local/bin/gosu;   gosu nobody true;   wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-$pkgArch";   wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-$pkgArch.asc";   gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;   rm /usr/local/bin/tini.asc;   chmod +x /usr/local/bin/tini;   tini --version;   MAX_REDIRECTS=1;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --file "/opt/solr-$SOLR_VERSION.tgz";   mv "/opt/solr-$SOLR_VERSION" /opt/solr;   rm "/opt/solr-$SOLR_VERSION.tgz"*;   rm -Rf /opt/solr/docs/ /opt/solr/dist/{solr-core-$SOLR_VERSION.jar,solr-solrj-$SOLR_VERSION.jar,solrj-lib,solr-test-framework-$SOLR_VERSION.jar,test-framework};   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d /opt/docker-solr;   mkdir -p /opt/solr/server/solr/mycores /opt/solr/server/logs /opt/mysolrhome;   sed -i -e "s/\"\$(whoami)\" == \"root\"/\$(id -u) == 0/" /opt/solr/bin/solr;   sed -i -e 's/lsof -PniTCP:/lsof -t -PniTCP:/' /opt/solr/bin/solr;   if [ -f "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter" ]; then chmod 0755 "/opt/solr/contrib/prometheus-exporter/bin/solr-exporter"; fi;   chmod -R 0755 /opt/solr/server/scripts/cloud-scripts;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/solr /docker-entrypoint-initdb.d /opt/docker-solr;   chown -R "$SOLR_USER:$SOLR_GROUP" /opt/mysolrhome;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME"
# Fri, 17 Apr 2020 03:24:29 GMT
COPY --chown=solr:solrdir:ad5f25b55b5e1dd053c2ddf3b986d9715d168efb9fedcd5c63ece6818a1f856a in /opt/docker-solr/scripts 
# Fri, 17 Apr 2020 03:24:30 GMT
EXPOSE 8983
# Fri, 17 Apr 2020 03:24:31 GMT
WORKDIR /opt/solr
# Fri, 17 Apr 2020 03:24:31 GMT
USER solr
# Fri, 17 Apr 2020 03:24:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2020 03:24:32 GMT
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
	-	`sha256:624545e52f4cc597fd27ebc180ed6015e4d8785913d350338a2b68b764df475c`  
		Last Modified: Fri, 17 Apr 2020 03:34:46 GMT  
		Size: 5.5 MB (5458088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93cf39b31bd66fc7c8bc6c50000e5c6164660b2978330947d69223fd80d44a7`  
		Last Modified: Fri, 17 Apr 2020 03:34:45 GMT  
		Size: 4.3 KB (4323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec13f06a6e2040bd2a09b95aa942b4144ee442fbd2248174fbe737693f52cd56`  
		Last Modified: Fri, 17 Apr 2020 03:34:45 GMT  
		Size: 26.6 KB (26597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1193b924121aea32ddae78c386ffa2258996e5eff5389e319af944f39c85fd37`  
		Last Modified: Fri, 17 Apr 2020 03:35:03 GMT  
		Size: 172.4 MB (172356650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4935d15428fa3c6bcb311d2d7769fa854ff393cc4fdf4193d7e6995f33a1d5d`  
		Last Modified: Fri, 17 Apr 2020 03:34:45 GMT  
		Size: 6.1 KB (6075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
