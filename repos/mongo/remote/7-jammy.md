## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:c1857c629fd8c5ea094e2a076e8f123704ae8604d33df3b6ef7573f8d0c44163
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:fcde2d71bf00b592c9cabab1d7d01defde37d69b3d788c53c3bc7431b6b15de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258098249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8df2163f9aa384163ea74e076f8cf562f8d291189dbdecc79036e546e1a989c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 07 Feb 2024 00:59:03 GMT
ARG RELEASE
# Wed, 07 Feb 2024 00:59:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Feb 2024 00:59:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Feb 2024 00:59:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 07 Feb 2024 00:59:03 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Wed, 07 Feb 2024 00:59:03 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 00:59:03 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENV GOSU_VERSION=1.17
# Wed, 07 Feb 2024 00:59:03 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 07 Feb 2024 00:59:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 07 Feb 2024 00:59:03 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_MAJOR=7.0
# Wed, 07 Feb 2024 00:59:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_VERSION=7.0.5
# Wed, 07 Feb 2024 00:59:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
VOLUME [/data/db /data/configdb]
# Wed, 07 Feb 2024 00:59:03 GMT
ENV HOME=/data/db
# Wed, 07 Feb 2024 00:59:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Feb 2024 00:59:03 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 07 Feb 2024 00:59:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:01007420e9b005dc14a8c8b0f996a2ad8e0d4af6c3d01e62f123be14fe48eec7`  
		Last Modified: Tue, 13 Feb 2024 10:22:22 GMT  
		Size: 29.5 MB (29536188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3bec6a423e52cfe237a8bb42e827f3a759b013f03c93bc5f2a2cbd68eb85b0`  
		Last Modified: Fri, 16 Feb 2024 01:50:31 GMT  
		Size: 1.8 KB (1779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5db81b694a822fe777a3381ca09286e469bb38d5d4155bf576b559919062fe8`  
		Last Modified: Fri, 16 Feb 2024 01:50:31 GMT  
		Size: 1.5 MB (1500342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427a1a117df0119d24b1e60761494bd5445f366399194c0649c3cac69c90192b`  
		Last Modified: Fri, 16 Feb 2024 01:50:31 GMT  
		Size: 1.1 MB (1094199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb180c9e7b566cbbc5a149b35730ede7ba88af41fa4ea4e720fc8e94e827268`  
		Last Modified: Fri, 16 Feb 2024 01:50:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e6f08e133c083169d361c9ff6cc086d4b96df1741181d2c2e6c57187955c16`  
		Last Modified: Fri, 16 Feb 2024 01:50:31 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374f042f3159bf1ec10f6b608d853243c19b1203de03e06d61e404419f69d6d3`  
		Last Modified: Fri, 16 Feb 2024 01:50:35 GMT  
		Size: 226.0 MB (225960367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73549bb430065b1cde6a427399b09db7281ae91c46f5f717e16775fcc4bb1b70`  
		Last Modified: Fri, 16 Feb 2024 01:50:32 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:b51f2f7061b3c2e71a8feb217e4f03a7c956eb045d64a498ac6456becf24adc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2641018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bd6123deda1404c878e80f947dd52f8681dab28902d91f2f637d64bb38dc2b`

```dockerfile
```

-	Layers:
	-	`sha256:05f83f856bdcdad2c514caaf17919fe68e20c1082edc0ad74f79c0f08c536067`  
		Last Modified: Fri, 16 Feb 2024 01:50:32 GMT  
		Size: 2.6 MB (2613283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec56d9b7c6dcb49c6b8d0575fd03c8adfc9269559876debfe3117801ea8e4e59`  
		Last Modified: Fri, 16 Feb 2024 01:50:31 GMT  
		Size: 27.7 KB (27735 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:e49dddaba9c6092f223f4c4e64431b0f9756e77b30b39ec25c84b529746a9a49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.0 MB (249956704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c313d60605ed3771fab3e536d9029ef80c3835100810b4a9391fc3dfc55d0894`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 07 Feb 2024 00:59:03 GMT
ARG RELEASE
# Wed, 07 Feb 2024 00:59:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Feb 2024 00:59:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Feb 2024 00:59:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 07 Feb 2024 00:59:03 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Wed, 07 Feb 2024 00:59:03 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 00:59:03 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENV GOSU_VERSION=1.17
# Wed, 07 Feb 2024 00:59:03 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 07 Feb 2024 00:59:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 07 Feb 2024 00:59:03 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_MAJOR=7.0
# Wed, 07 Feb 2024 00:59:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_VERSION=7.0.5
# Wed, 07 Feb 2024 00:59:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
VOLUME [/data/db /data/configdb]
# Wed, 07 Feb 2024 00:59:03 GMT
ENV HOME=/data/db
# Wed, 07 Feb 2024 00:59:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Feb 2024 00:59:03 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 07 Feb 2024 00:59:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a4a2c7a57ed8b997579870d0927433b03cfd94f5dba2153bdbcd885b5d620035`  
		Last Modified: Tue, 13 Feb 2024 10:22:28 GMT  
		Size: 27.4 MB (27356877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1354176b189db5e882e8695cd36475579099a8312ad5731dd9c9365249630636`  
		Last Modified: Fri, 16 Feb 2024 19:01:34 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a94d566154f568d8d3806d6f82aeec09ecd0408a9db227eceeb6849c9ead90`  
		Last Modified: Fri, 16 Feb 2024 19:01:34 GMT  
		Size: 1.5 MB (1465222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e46f202d7a90abe40c09f31f1cf2c48277023e1dd069bf9a2687256c1c5e7b`  
		Last Modified: Fri, 16 Feb 2024 19:01:34 GMT  
		Size: 1.0 MB (1026758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d926c33a8021648a6ee91c79b9743e0c4b7824f0e4abfd2d086fa58e86b389`  
		Last Modified: Fri, 16 Feb 2024 19:01:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d249179d7272d9abc175c7f3f633122bd78ebc02e3551c0af3316984232a74`  
		Last Modified: Fri, 16 Feb 2024 19:01:35 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6ffb85f76eaccdfedf8ddf6f80fb6cf54d1f86cc0e4513f8fbe06770238102`  
		Last Modified: Fri, 16 Feb 2024 19:01:40 GMT  
		Size: 220.1 MB (220100682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ce817099037841cd13e5e1361c647a9810d96e4217de5dbd07ae4cbd4f40fd`  
		Last Modified: Fri, 16 Feb 2024 19:01:35 GMT  
		Size: 5.0 KB (5001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:ebca4c63f7dd6682add579cb9a1495bf468191e295ec1806206183083c348d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2641237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f76c010308bff455315ce10bad2387f2240232e5d9324fee301a60d7786d901`

```dockerfile
```

-	Layers:
	-	`sha256:093455ea6b5eaf71e8872c7fecf120c0f6099168bd062657f4d33c65295f16da`  
		Last Modified: Fri, 16 Feb 2024 19:01:34 GMT  
		Size: 2.6 MB (2613646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfe08756c2fff30faa8fb575a27347b6bfe3d186a61cafdc57ffc78f1d20e5ed`  
		Last Modified: Fri, 16 Feb 2024 19:01:34 GMT  
		Size: 27.6 KB (27591 bytes)  
		MIME: application/vnd.in-toto+json
