## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:52ea2c0512ea8ac1ee6bf558711efbeb0332e0a2504caac24ad743cc9509738b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:ee78b6708347055b87d034043a81dd16aefc2f7282aa1d7caffa60955fbcd988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258796598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:199c7e9888b41ed904a8fe08ff037b59ef6eae3b57dd43e07c9c647e19279a75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 23:06:36 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
ENV GOSU_VERSION=1.17
# Fri, 20 Dec 2024 23:06:36 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 20 Dec 2024 23:06:36 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 20 Dec 2024 23:06:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 20 Dec 2024 23:06:36 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 20 Dec 2024 23:06:36 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 20 Dec 2024 23:06:36 GMT
ENV MONGO_MAJOR=7.0
# Fri, 20 Dec 2024 23:06:36 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
ENV MONGO_VERSION=7.0.16
# Fri, 20 Dec 2024 23:06:36 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
VOLUME [/data/db /data/configdb]
# Fri, 20 Dec 2024 23:06:36 GMT
ENV HOME=/data/db
# Fri, 20 Dec 2024 23:06:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Dec 2024 23:06:36 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 20 Dec 2024 23:06:36 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02c29789a2d5655303f0a2f8ac8f22cdc0a259f26caea2ac0bdf504b502675e`  
		Last Modified: Mon, 23 Dec 2024 17:28:48 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd75870704cc15e18ba0758bbcfcd80d2ce662bae1e576372e16402af381e1f`  
		Last Modified: Mon, 23 Dec 2024 17:28:48 GMT  
		Size: 1.5 MB (1512820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8cb3291b9a374e4c70ac3203ff9046d7e10f28850efb198489f8653fb2352f`  
		Last Modified: Mon, 23 Dec 2024 17:28:48 GMT  
		Size: 1.1 MB (1094682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b05b3ed020a9851dd0f55ebdce59ce37b6a6239f07183c2ce2fe2d3dcfca5f5`  
		Last Modified: Mon, 23 Dec 2024 17:28:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62958acdaa697a934f5bfdc1b739bee40319f8a02b806d9f41973056dafbeee`  
		Last Modified: Mon, 23 Dec 2024 17:28:49 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e975de0b5efef85eef8db9cbe38d809d1ba7e9b1504de8dd8f0ad4b0675d87`  
		Last Modified: Mon, 23 Dec 2024 17:28:55 GMT  
		Size: 226.6 MB (226646245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eebf83eff81734bf0750c1ceb707e0db175a1ac1406e1c6dbb893f5b4b663b`  
		Last Modified: Mon, 23 Dec 2024 17:28:49 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:bcc93b5640999e1a9cd6cbd15003fce019567fae3092922e911e0a5a8ddcdb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d80686ba627cd01c906b98fede86a6422ceeaaafd269380ba85dc3f24aa9b04`

```dockerfile
```

-	Layers:
	-	`sha256:65afcd1a95be74704c37dc8bbb49f4ab410fc2397613243053263e6ada8facf9`  
		Last Modified: Mon, 23 Dec 2024 17:28:48 GMT  
		Size: 3.0 MB (3049271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5871a21d62a69db69f96bd3f893027a64919c56132211a6f331afb51ba7c5e15`  
		Last Modified: Mon, 23 Dec 2024 17:28:48 GMT  
		Size: 28.0 KB (27991 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:3906d768163309d7282f80769b43a2b43d271ca98cdef484908df15b74b71f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247338378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082b79b5037cec2fa8ae4e2c4a09b749c47efdc01e274f7bed661a37d2ce787f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 23:06:36 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
ENV GOSU_VERSION=1.17
# Fri, 20 Dec 2024 23:06:36 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 20 Dec 2024 23:06:36 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 20 Dec 2024 23:06:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 20 Dec 2024 23:06:36 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 20 Dec 2024 23:06:36 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 20 Dec 2024 23:06:36 GMT
ENV MONGO_MAJOR=7.0
# Fri, 20 Dec 2024 23:06:36 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
ENV MONGO_VERSION=7.0.16
# Fri, 20 Dec 2024 23:06:36 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
VOLUME [/data/db /data/configdb]
# Fri, 20 Dec 2024 23:06:36 GMT
ENV HOME=/data/db
# Fri, 20 Dec 2024 23:06:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Dec 2024 23:06:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Dec 2024 23:06:36 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 20 Dec 2024 23:06:36 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe71bf4de30ded530999b7bd82283cde3eb0ae8df19cef680273f3c6a553ff5`  
		Last Modified: Wed, 11 Dec 2024 21:36:18 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4a3559a03510d1db0f081c6c5cf8381a2dd6d06b4cfbd6ea87b98e552113a8`  
		Last Modified: Wed, 11 Dec 2024 21:36:18 GMT  
		Size: 1.5 MB (1481430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90ee5f3f39c5784babc660d7b481cf1e0f9175f09dd816bf1efada803828486`  
		Last Modified: Mon, 23 Dec 2024 17:28:44 GMT  
		Size: 1.0 MB (1027429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe1a0c20f49a59cb96ed1fb8cf12b66fa2a3dd4aeef0de977041276fce31dc`  
		Last Modified: Mon, 23 Dec 2024 17:28:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739c521ffbbdc2ad589fafceec435247fef38e035d6562a24ce41b3269992816`  
		Last Modified: Mon, 23 Dec 2024 17:28:44 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd63593da07889a8fd0e054c37e74feeff4502a76e63ea543e34a083eb28ab5`  
		Last Modified: Mon, 23 Dec 2024 17:28:50 GMT  
		Size: 217.5 MB (217464021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68355a08d73353217626fe4f6722b8d51b0c2ac483f6efa43af9548cb5a992b`  
		Last Modified: Mon, 23 Dec 2024 17:28:45 GMT  
		Size: 5.0 KB (4999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:33ebcfa424d3c5c06af601138b5db13bcbf4737e7c4936690b4286606390fbe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3077784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da79e330a8abeb12906e235206ac052f9cd7cd9728d08028707664b7e93400e9`

```dockerfile
```

-	Layers:
	-	`sha256:aea94392cde32eb50e822709889bf48143202f706403ddd7408aa06ee231d7ef`  
		Last Modified: Mon, 23 Dec 2024 17:28:45 GMT  
		Size: 3.0 MB (3049590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af120660e43334504d95a774121b03fcc5dd882cf2666c31ea33286f659f1731`  
		Last Modified: Mon, 23 Dec 2024 17:28:44 GMT  
		Size: 28.2 KB (28194 bytes)  
		MIME: application/vnd.in-toto+json
