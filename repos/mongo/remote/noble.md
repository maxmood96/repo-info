## `mongo:noble`

```console
$ docker pull mongo@sha256:41061c0c52f9506bdc70bfa10a50955c080aa69382d4cde96be48918a8562473
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:noble` - linux; amd64

```console
$ docker pull mongo@sha256:3f04076470ff9110ce77473afe54c549feaca994a29bc5ff01a549bf340acf8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274452261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08e39122805c55578b51555cf58418692d9842b74aa153441681e7e4cdd7729`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Fri, 06 Dec 2024 23:01:34 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 23:01:34 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 06 Dec 2024 23:01:34 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 06 Dec 2024 23:01:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 06 Dec 2024 23:01:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 06 Dec 2024 23:01:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 06 Dec 2024 23:01:34 GMT
ENV MONGO_MAJOR=8.0
# Fri, 06 Dec 2024 23:01:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
ENV MONGO_VERSION=8.0.4
# Fri, 06 Dec 2024 23:01:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
VOLUME [/data/db /data/configdb]
# Fri, 06 Dec 2024 23:01:34 GMT
ENV HOME=/data/db
# Fri, 06 Dec 2024 23:01:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 23:01:34 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 06 Dec 2024 23:01:34 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add2cfa32b4d238ee12f15bfd6aa93ccfe9642fd196c8547875c8283b2368d7a`  
		Last Modified: Mon, 09 Dec 2024 20:37:59 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3422d31c845e81955669c12fae32ec2f8975c34bf71c15f513ebb0c3f28f99`  
		Last Modified: Mon, 09 Dec 2024 20:37:59 GMT  
		Size: 1.5 MB (1507485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9869afb5187e201a30dee6e4e2d6f47e75178ba69949fdd9cb7d449edde587b`  
		Last Modified: Mon, 09 Dec 2024 20:37:59 GMT  
		Size: 1.1 MB (1129950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9284108c06f819c4f7000852a1c2cb637f197eb63414136ebe4c1c43a93ae87f`  
		Last Modified: Mon, 09 Dec 2024 20:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17351a831ef124fbf4e5cd477230ea72d93c351b1fb43d403a52500ecf9d71bc`  
		Last Modified: Mon, 09 Dec 2024 20:38:00 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2613644e011d299f77e47da4ce236167e82074b1bc89eabc8c9776c5ac03fc18`  
		Last Modified: Mon, 09 Dec 2024 20:38:04 GMT  
		Size: 242.1 MB (242056265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cc0f1cded4ad17b51117ffcb3f5c0b5197cc52495d9a922416183d3105fd6e`  
		Last Modified: Mon, 09 Dec 2024 20:38:00 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:4f3a9cedeb0af30f16f652bea4759139d3a907ac30b98d9cab8dd518da7f1352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2526408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1957543002df091f216135119c7e94e6508c2e8b9cf08d37c626b4f867b666d2`

```dockerfile
```

-	Layers:
	-	`sha256:cfdf5e6c458675464fd22510767fbb6adfa80e4340aefdd45a6e37970ce17a5b`  
		Last Modified: Mon, 09 Dec 2024 20:37:59 GMT  
		Size: 2.5 MB (2497837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed65411667e6cc826e7168c932e9397f93ce453dc8427c3091326403f4990ea5`  
		Last Modified: Mon, 09 Dec 2024 20:37:59 GMT  
		Size: 28.6 KB (28571 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:112ff68b2168d2f94d09050b9681ef876ee2869d865e9daa4df62f7234cffae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.6 MB (263576623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb86096614c22834c0f416892d263001d04d8892d681ad3e504b5ea4f6190d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Fri, 06 Dec 2024 23:01:34 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 23:01:34 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 06 Dec 2024 23:01:34 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 06 Dec 2024 23:01:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 06 Dec 2024 23:01:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 06 Dec 2024 23:01:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 06 Dec 2024 23:01:34 GMT
ENV MONGO_MAJOR=8.0
# Fri, 06 Dec 2024 23:01:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
ENV MONGO_VERSION=8.0.4
# Fri, 06 Dec 2024 23:01:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
VOLUME [/data/db /data/configdb]
# Fri, 06 Dec 2024 23:01:34 GMT
ENV HOME=/data/db
# Fri, 06 Dec 2024 23:01:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 23:01:34 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 06 Dec 2024 23:01:34 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50af98a999ca9179bc6f9f96cff2b6b06de18db2640d1c22668f22607b3fb6aa`  
		Last Modified: Tue, 03 Dec 2024 06:14:00 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2b33d58e9a8050338a63963e7a4d3f199e76f3a82083b53b3eddf6bdcebf38`  
		Size: 1.5 MB (1491716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c5b23bf5cf2e4b85b5aa1d3cd7ea65fd9991be6d569a37036ccf5faca7b4b9`  
		Last Modified: Tue, 03 Dec 2024 06:15:17 GMT  
		Size: 1.1 MB (1060184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216f2761441aa3521e82846a06397d71b1d3412600a7ac411231adc34ee87524`  
		Last Modified: Tue, 03 Dec 2024 06:15:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075a696718bbbc686430ac5b0d2a17ebf9159f95a3d5a741df57d52658b338c8`  
		Last Modified: Tue, 03 Dec 2024 06:15:17 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da089b883a540a65e962647aaeab9b7f5727eb1cb69ca1a3a8f6b03098eeff5b`  
		Last Modified: Tue, 10 Dec 2024 00:21:38 GMT  
		Size: 232.1 MB (232125459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019eaf26198ff9c843350c1ff26791c6ea1b9e1754fa224f5375bdf2c4f4e642`  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:4bfd15a96855b49e333edcd1581b1486ddf5d76205b35888b2c4b298fd1a2be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2527772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9486690867ee35d689e2ee40bfdbb6df4ee7b299027dc498bbb3db82947c96`

```dockerfile
```

-	Layers:
	-	`sha256:efb99bf710d3bf4d4b4813df3c76ba5ea96f8959f87da205b84fc893c3a75d56`  
		Last Modified: Tue, 10 Dec 2024 00:21:33 GMT  
		Size: 2.5 MB (2498973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79863932882a73481a4470049b2502617fd98aee2a4955e75486724090f01eb0`  
		Last Modified: Tue, 10 Dec 2024 00:21:32 GMT  
		Size: 28.8 KB (28799 bytes)  
		MIME: application/vnd.in-toto+json
