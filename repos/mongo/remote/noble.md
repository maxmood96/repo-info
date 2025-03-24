## `mongo:noble`

```console
$ docker pull mongo@sha256:1697f35db2404e7ca87650fee7e5aab4188d2c2f3f0adbe211d060ec9b5799e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:noble` - linux; amd64

```console
$ docker pull mongo@sha256:0fbe569f105156a412dd7383afdc9d6a784c9acea1367663c384e5e98b2ecc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288469640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d4ab2a034263b0e2306e41be1a596bd8600fb6fadef145a9088791c8d7c4b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:06:21 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Mar 2025 22:06:21 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 21 Mar 2025 22:06:21 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 21 Mar 2025 22:06:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Mar 2025 22:06:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Mar 2025 22:06:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Mar 2025 22:06:21 GMT
ENV MONGO_MAJOR=8.0
# Fri, 21 Mar 2025 22:06:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
ENV MONGO_VERSION=8.0.6
# Fri, 21 Mar 2025 22:06:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Mar 2025 22:06:21 GMT
ENV HOME=/data/db
# Fri, 21 Mar 2025 22:06:21 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Fri, 21 Mar 2025 22:06:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Mar 2025 22:06:21 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 21 Mar 2025 22:06:21 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12757b6444c4bf8265b616857e2a81e055bf662038771fc2aeb2ef7a19944d`  
		Last Modified: Mon, 24 Mar 2025 21:19:15 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cfb5e922d1078b85377cbdaa154d2b25f67fb5664a2907edd1a2b75d50f9cc`  
		Last Modified: Mon, 24 Mar 2025 21:19:15 GMT  
		Size: 3.9 MB (3911303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11968535d8a0c360571f9996ad96877a29684239f55c1918206ae5d70f49fbb`  
		Last Modified: Mon, 24 Mar 2025 21:19:15 GMT  
		Size: 1.1 MB (1130254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c711ee204b1d1383a860f114449a82e983ee41956d7c746e8791b53f066c3a82`  
		Last Modified: Mon, 24 Mar 2025 21:19:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc65ca4253fd123c695b1b74bff2d7a8cdc2771a1a5d9da1668105079e175ec`  
		Last Modified: Mon, 24 Mar 2025 21:19:16 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacd77ad2ef6c5625e09b751626186b53d4e8662f79bd9253755f474fc22ac87`  
		Last Modified: Mon, 24 Mar 2025 21:19:20 GMT  
		Size: 253.7 MB (253667204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa69bd3db1e4fcd13568432e190d90762be307687b8e8405d90181f579b5ca6`  
		Last Modified: Mon, 24 Mar 2025 21:19:16 GMT  
		Size: 5.0 KB (4993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:6b2ee100d267caee895a5a955b799f40e276bd304c913dd12521f7a4262bba72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e6dad2596c599d3c33e66d26462bbd65aacb0b1ab8de023a01d42cd29a60ca`

```dockerfile
```

-	Layers:
	-	`sha256:d0bb38821262eef175d02bdb58df3c3808f21aea6994e542e4cf6e6a7e0d5f2e`  
		Last Modified: Mon, 24 Mar 2025 21:19:15 GMT  
		Size: 2.5 MB (2524379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4b1c498653910899b1790231eef60783e70932dc161bd544b2bf1647e17b749`  
		Last Modified: Mon, 24 Mar 2025 21:19:15 GMT  
		Size: 28.8 KB (28839 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:433198e0a19aa4736f93862df15f4a75e74e6d9ffc540e9272f517e43e441f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276701240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c72c5f78fefe289d17c049f20c0e2bfbbe35607440da0175260737b1e5359b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:06:21 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
ENV GOSU_VERSION=1.17
# Fri, 21 Mar 2025 22:06:21 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 21 Mar 2025 22:06:21 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 21 Mar 2025 22:06:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Mar 2025 22:06:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Mar 2025 22:06:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Mar 2025 22:06:21 GMT
ENV MONGO_MAJOR=8.0
# Fri, 21 Mar 2025 22:06:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
ENV MONGO_VERSION=8.0.6
# Fri, 21 Mar 2025 22:06:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Mar 2025 22:06:21 GMT
ENV HOME=/data/db
# Fri, 21 Mar 2025 22:06:21 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Fri, 21 Mar 2025 22:06:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 21 Mar 2025 22:06:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Mar 2025 22:06:21 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 21 Mar 2025 22:06:21 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9286380517d7f8cc870c4ed63cf865809fb11d80de82513ae1ca35a9a0e0d744`  
		Last Modified: Mon, 24 Mar 2025 21:19:36 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbfd86d7f81de6a750a0de0b1865a6ec47f99950c02e29b090d62e56b64c4ed`  
		Last Modified: Mon, 24 Mar 2025 21:19:36 GMT  
		Size: 3.7 MB (3707246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306fcfa15fb1fcf4f3393be0773933cce9ad962d35e156ec0fd6fcc5b243ed28`  
		Last Modified: Mon, 24 Mar 2025 21:19:36 GMT  
		Size: 1.1 MB (1060641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568f73da14f2eb4f5eec89c2821555092eeb688d5acc72553f1b4981afcc2875`  
		Last Modified: Mon, 24 Mar 2025 21:19:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c5ca75dbfb7148dbb6f65679d41cb4365f652921c0f00cba8ea31ec25fdfc9`  
		Last Modified: Mon, 24 Mar 2025 21:19:37 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0f4766d11003e4c990338dfa942bd9d1228dfafb95088d4c6224daa75cb805`  
		Last Modified: Mon, 24 Mar 2025 21:19:43 GMT  
		Size: 243.0 MB (243033160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fcbf4e159abb793949f8eb8820658207317922226c0a9f07b3fd6fcebd5269`  
		Last Modified: Mon, 24 Mar 2025 21:19:37 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:d043a66b332d88d6c5b954f2c05715c8531c14cd2710a8f7d155aa7f057d6df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f79ee6278a5079672aff231f032d4b3ed1cf264dce59abd6e7753f60806104`

```dockerfile
```

-	Layers:
	-	`sha256:1fca4dee06fb75fbdf6a8b004297a4fb3356ace3664d35b0a07e854974daa083`  
		Last Modified: Mon, 24 Mar 2025 21:19:36 GMT  
		Size: 2.5 MB (2525515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9150e3fbf9463c25fd0dc740e72e308b30b36bba5b8a95ac928b2620fcaeb960`  
		Last Modified: Mon, 24 Mar 2025 21:19:36 GMT  
		Size: 29.1 KB (29067 bytes)  
		MIME: application/vnd.in-toto+json
