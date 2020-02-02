## `couchdb:latest`

```console
$ docker pull couchdb@sha256:37124bd9171d735d7b6fc14eea8214d700a23af8b268a90e1da6c2f1163c6c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:088fb3bc9c193ab4783e47d34f30f009eebabe305ea32280fb3ef0e44f8af8ab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82442939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c00781d955d35c8e39859dab22bd71b4180d267591ebb51cd2f955c4f425aaa`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Sat, 01 Feb 2020 17:23:57 GMT
ADD file:003d2bac85e72555ed93f77a2b1d595a7fe51c4a9a2401496a82fc673a863fd6 in / 
# Sat, 01 Feb 2020 17:23:58 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 00:45:46 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Sun, 02 Feb 2020 00:45:47 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Sun, 02 Feb 2020 00:45:57 GMT
RUN set -ex;         apt-get update;         apt-get install -y --no-install-recommends                 apt-transport-https                 ca-certificates                 dirmngr                 gnupg         ;         rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 00:45:57 GMT
ENV GOSU_VERSION=1.11
# Sun, 02 Feb 2020 00:45:57 GMT
ENV TINI_VERSION=0.18.0
# Sun, 02 Feb 2020 00:46:07 GMT
RUN set -ex; 		apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 		wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)";         echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;         for server in $(shuf -e pgpkeys.mit.edu             ha.pool.sks-keyservers.net             hkp://p80.pool.sks-keyservers.net:80             pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;         done; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true;     	wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch"; 	wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)";         echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;         for server in $(shuf -e pgpkeys.mit.edu             ha.pool.sks-keyservers.net             hkp://p80.pool.sks-keyservers.net:80             pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;         done; 	gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini; 	rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc; 	chmod +x /usr/local/bin/tini;         apt-get purge -y --auto-remove wget; 	tini --version
# Sun, 02 Feb 2020 00:46:07 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Sun, 02 Feb 2020 00:46:10 GMT
RUN set -xe;         export GNUPGHOME="$(mktemp -d)";         echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;         for server in $(shuf -e pgpkeys.mit.edu             ha.pool.sks-keyservers.net             hkp://p80.pool.sks-keyservers.net:80             pgp.mit.edu) ; do                 gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;         done;         gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;         command -v gpgconf && gpgconf --kill all || :;         rm -rf "$GNUPGHOME";         apt-key list
# Sun, 02 Feb 2020 00:46:10 GMT
ENV COUCHDB_VERSION=2.3.1
# Sun, 02 Feb 2020 00:46:11 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb stretch main" > /etc/apt/sources.list.d/couchdb.list
# Sun, 02 Feb 2020 00:46:32 GMT
RUN set -xe;         apt-get update;                 echo "couchdb couchdb/mode select none" | debconf-set-selections;         DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages                 couchdb="$COUCHDB_VERSION"~stretch         ;         rmdir /var/lib/couchdb /var/log/couchdb;         rm /opt/couchdb/data /opt/couchdb/var/log;         mkdir -p /opt/couchdb/data /opt/couchdb/var/log;         chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;         chmod 777 /opt/couchdb/data /opt/couchdb/var/log;         rm /opt/couchdb/etc/default.d/10-filelog.ini;         rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 00:46:32 GMT
COPY file:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Sun, 02 Feb 2020 00:46:32 GMT
COPY file:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Sun, 02 Feb 2020 00:46:32 GMT
COPY file:fc62f0c3f2a39a070ec3c03ac9e1f9ae02b94364cb5492a733584c34458af969 in /usr/local/bin 
# Sun, 02 Feb 2020 00:46:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Sun, 02 Feb 2020 00:46:33 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Sun, 02 Feb 2020 00:46:34 GMT
RUN chown -R couchdb:couchdb /opt/couchdb/etc/default.d/ /opt/couchdb/etc/vm.args
# Sun, 02 Feb 2020 00:46:34 GMT
VOLUME [/opt/couchdb/data]
# Sun, 02 Feb 2020 00:46:35 GMT
EXPOSE 4369 5984 9100
# Sun, 02 Feb 2020 00:46:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:619014d83c026bca3d21f5eb42a629ac2dbe15bdb37b77f25fc1ac5fbada68e5`  
		Last Modified: Sat, 01 Feb 2020 17:29:01 GMT  
		Size: 22.5 MB (22524713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bcd27e5cfd6a719d3656b17c8730a60228d8e265f59a88efa02ea3dac6847d0`  
		Last Modified: Sun, 02 Feb 2020 00:47:33 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a920e9c1f1732bb4c535ae4d40630a1ff22376192e06c8342274b1912e420aeb`  
		Last Modified: Sun, 02 Feb 2020 00:47:35 GMT  
		Size: 8.5 MB (8514950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681c7f7bafee2d8a176e2d0b1a1d21d6d6c10bf309fb7093d2b6587b7568d1d0`  
		Last Modified: Sun, 02 Feb 2020 00:47:32 GMT  
		Size: 1.2 MB (1190688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4cadf8a73953f6232ca987ea391fefef2e31ca3b47d08cd1b49ff2c20dedaa`  
		Last Modified: Sun, 02 Feb 2020 00:47:32 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32160199e71aa5a0fa80cb1d2d4f16dde9d78a0f7c3df928cdd8409d697a3057`  
		Last Modified: Sun, 02 Feb 2020 00:47:32 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d361bf917c36f0ec2b637ef39d017af96e9fb02b6ae17a362166c67a51b2f109`  
		Last Modified: Sun, 02 Feb 2020 00:47:45 GMT  
		Size: 50.2 MB (50202146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19587d369ef7f08f01d5c3f39f1c6f04804363314e6069b6cf186602955d968d`  
		Last Modified: Sun, 02 Feb 2020 00:47:30 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab71925ba4e2eeef75c850bc00a46923f8f5e0e8898bfed1c21a85f3a4876694`  
		Last Modified: Sun, 02 Feb 2020 00:47:31 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eb45a1caa30eb03de1b991b6bf62f7e8a22d57bb4d21b7fddd379c9f96391d5`  
		Last Modified: Sun, 02 Feb 2020 00:47:31 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7e40ef8caaf751be0719f707d6ca7babbc7976a298c16582fa5c073631cef8`  
		Last Modified: Sun, 02 Feb 2020 00:47:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8232fb4dc1500bdc0828a36ba4e915e7c9f82067a09eec063fe6033c0cae8a5c`  
		Last Modified: Sun, 02 Feb 2020 00:47:31 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
