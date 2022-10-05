## `mongo:5-focal`

```console
$ docker pull mongo@sha256:9e0b6c3cbd55f4bb347b63d495d4aa6b49fe0972acdc9df5cd8250ca675e9a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:5-focal` - linux; amd64

```console
$ docker pull mongo@sha256:4b639ee355b4f0f6202705f0755375b763ccf987d4b796dfa07c1b320e852be3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.0 MB (246969997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82781b19f1b6ba19b7d31efd91890160fa69c6ca3b2f24000a75e32c40bf3f72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:52:11 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 02 Sep 2022 03:52:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:52:19 GMT
ENV GOSU_VERSION=1.12
# Fri, 02 Sep 2022 03:52:20 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 02 Sep 2022 03:52:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 02 Sep 2022 03:52:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 02 Sep 2022 03:53:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Fri, 02 Sep 2022 03:53:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 02 Sep 2022 03:53:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 02 Sep 2022 03:53:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 02 Sep 2022 03:53:10 GMT
ENV MONGO_MAJOR=5.0
# Fri, 02 Sep 2022 03:53:11 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 29 Sep 2022 21:20:10 GMT
ENV MONGO_VERSION=5.0.13
# Thu, 29 Sep 2022 21:20:33 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 29 Sep 2022 21:20:34 GMT
VOLUME [/data/db /data/configdb]
# Thu, 29 Sep 2022 21:20:34 GMT
ENV HOME=/data/db
# Thu, 29 Sep 2022 21:20:34 GMT
COPY file:a062061dd38363517a589afdd763f61500b162faee89d415017c58fd70abe392 in /usr/local/bin/ 
# Thu, 29 Sep 2022 21:20:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Sep 2022 21:20:35 GMT
EXPOSE 27017
# Thu, 29 Sep 2022 21:20:35 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9c8c301e0f21d7d0b229b7ce3bf5f73a8032a77f1fd0ead5a40ae2904e7386`  
		Last Modified: Fri, 02 Sep 2022 03:57:03 GMT  
		Size: 1.8 KB (1830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73738965c4ce390367a607807b960c2c4cd8aa410fc4b1bea6ce71263c6725a8`  
		Last Modified: Fri, 02 Sep 2022 03:57:04 GMT  
		Size: 3.1 MB (3059566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd6635b9ddf662b5aad927979bc18877d5e93da5b68d0257bf589086be3fc24`  
		Last Modified: Fri, 02 Sep 2022 03:57:04 GMT  
		Size: 6.5 MB (6506072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a471eaa4ad67f863744ea2570d2995126f69ac4a5156455603a9308c2c915e`  
		Last Modified: Fri, 02 Sep 2022 03:57:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abd0e4db1c77c9d2823cf5d0d4d725e622cd03991e67bcb2ae6aa5f1a94d572`  
		Last Modified: Fri, 02 Sep 2022 03:57:43 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90013e6cca25832e6d27f62bf64f3a667d10b7a3a65221381f1bf9ab81c34ad7`  
		Last Modified: Fri, 02 Sep 2022 03:57:44 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88b6355fefbbd084b1c1b7e3bd7a8b2a11c8f26789b372a07399d4a2387bb27`  
		Last Modified: Thu, 29 Sep 2022 21:22:49 GMT  
		Size: 208.8 MB (208822921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f0e33dbefc7999a24cd81b01d91bb4e8d321ba3d7b6ad2d2b414819a3c8857`  
		Last Modified: Thu, 29 Sep 2022 21:22:18 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:0926d8aa42ccca3a55068197cc9906b5c1254ade91dd2dd049a2f59b33e0d40c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239248236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d81fb74d08d05851b9fe3823c069f004221f34df7f12aa8b4ccbb21c5d2f3df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 16:54:34 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 05 Oct 2022 16:54:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 16:54:45 GMT
ENV GOSU_VERSION=1.12
# Wed, 05 Oct 2022 16:54:46 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 05 Oct 2022 16:55:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 05 Oct 2022 16:55:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 05 Oct 2022 16:55:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"
# Wed, 05 Oct 2022 16:55:49 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 05 Oct 2022 16:55:50 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 05 Oct 2022 16:55:51 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 05 Oct 2022 16:55:52 GMT
ENV MONGO_MAJOR=5.0
# Wed, 05 Oct 2022 16:55:53 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 05 Oct 2022 16:55:54 GMT
ENV MONGO_VERSION=5.0.13
# Wed, 05 Oct 2022 16:56:17 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 05 Oct 2022 16:56:18 GMT
VOLUME [/data/db /data/configdb]
# Wed, 05 Oct 2022 16:56:18 GMT
ENV HOME=/data/db
# Wed, 05 Oct 2022 16:56:20 GMT
COPY file:a062061dd38363517a589afdd763f61500b162faee89d415017c58fd70abe392 in /usr/local/bin/ 
# Wed, 05 Oct 2022 16:56:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 16:56:21 GMT
EXPOSE 27017
# Wed, 05 Oct 2022 16:56:22 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808a7df5fbbc12c4cd8f740fabdbbe301d6a4efe1b81b3f196474a28d0322c92`  
		Last Modified: Wed, 05 Oct 2022 16:59:14 GMT  
		Size: 1.8 KB (1778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5a5e151a7f04dcea23cd214c84a62e5c02bfd8bf21e50b6384cb32a7dac4ed`  
		Last Modified: Wed, 05 Oct 2022 16:59:14 GMT  
		Size: 2.9 MB (2905895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbed2c86a740691aafa2028087ed2a11f64352f3ab06a520efa22bc7c5246f03`  
		Last Modified: Wed, 05 Oct 2022 16:59:14 GMT  
		Size: 6.2 MB (6248099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c6dc442fc2aca80b585c0c229cf8addb668c43cb2b7b15193532981186e6d`  
		Last Modified: Wed, 05 Oct 2022 16:59:11 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298734b330d3680fbe87b3fa8fbd3448f058d41dd3106b1c54a824df12ccb8a8`  
		Last Modified: Wed, 05 Oct 2022 16:59:55 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0daafae2ada882b2a73be7721feccd5873ef8cc6f1d787bc2d0fd84e270ed5f`  
		Last Modified: Wed, 05 Oct 2022 16:59:55 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d15ac784e427008b57b135adad6c4cf6dd2e056c54e25a3b9ec3bc17417648`  
		Last Modified: Wed, 05 Oct 2022 17:00:22 GMT  
		Size: 202.9 MB (202893999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839f0121c344c0c546d396b2b399cc3ff424ca6c406b47f9b96ff36713e77ae0`  
		Last Modified: Wed, 05 Oct 2022 16:59:55 GMT  
		Size: 5.1 KB (5072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
