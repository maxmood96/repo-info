## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:fc487f6ea51387291231431f6ffc21bf6b7e607d5621c0afc4f34a114ee54890
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:139e9929d6828943d9cf67b8942969b800556e84102a653926bbf49d543c590f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (258966315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d7f1b1df90d956db6a421ea351666ae2912df10c149bb0b0ae7c896bcba1f5`
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
# Fri, 25 Oct 2024 04:11:28 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 25 Oct 2024 04:11:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Oct 2024 04:11:28 GMT
ENV GOSU_VERSION=1.17
# Fri, 25 Oct 2024 04:11:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 25 Oct 2024 04:11:28 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 25 Oct 2024 04:11:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 25 Oct 2024 04:11:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 25 Oct 2024 04:11:28 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 25 Oct 2024 04:11:28 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 25 Oct 2024 04:11:28 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 25 Oct 2024 04:11:28 GMT
ENV MONGO_MAJOR=7.0
# Fri, 25 Oct 2024 04:11:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 25 Oct 2024 04:11:28 GMT
ENV MONGO_VERSION=7.0.15
# Fri, 25 Oct 2024 04:11:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 25 Oct 2024 04:11:28 GMT
VOLUME [/data/db /data/configdb]
# Fri, 25 Oct 2024 04:11:28 GMT
ENV HOME=/data/db
# Fri, 25 Oct 2024 04:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Oct 2024 04:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Oct 2024 04:11:28 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 25 Oct 2024 04:11:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1461f3348e1dce5fcaabc8ea597e41186cbf3d9f1e0eab674cd69015010b87`  
		Last Modified: Fri, 25 Oct 2024 23:58:01 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e95ad87db41be6cf667de256948ded2ac6e24f76ea0d802045d75c6570879f`  
		Last Modified: Fri, 25 Oct 2024 23:58:01 GMT  
		Size: 1.5 MB (1512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25c183860c42cf4a76cbe5153c27a68a4ed739c12fac85ee93956335aee548b`  
		Last Modified: Fri, 25 Oct 2024 23:58:01 GMT  
		Size: 1.1 MB (1094650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f01f4e8b589a43c4ae61a6548262c45ce754a731f40edade45e488c578778cd`  
		Last Modified: Fri, 25 Oct 2024 23:58:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fe70253afce3237bf536b147788a7b4984e34938aca69ca7e5ab9b95111edf`  
		Last Modified: Fri, 25 Oct 2024 23:58:01 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c42b20f83df7c6cb19d2f5d72996ed6b5a33e3fb7ce41a7f9f3308d3ece35bd`  
		Last Modified: Fri, 25 Oct 2024 23:58:05 GMT  
		Size: 226.8 MB (226816000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef052cfe243ae4cad8ecb1cdc616aeaa5908b8501e831ca80c0c87f817cc26f`  
		Last Modified: Fri, 25 Oct 2024 23:58:02 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:03a3ab6bae998b48e0ff910ccad3175921ed2396d0855de0646c9c49dae24e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3080117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63d9f62969c1a832fb37695997b837df1011cb3ceea01421cf4d4d0385d68c0`

```dockerfile
```

-	Layers:
	-	`sha256:24109848a2459286beae7b0d527258496b7662c90c4417413a9e342dddf68ff3`  
		Last Modified: Fri, 25 Oct 2024 23:58:01 GMT  
		Size: 3.1 MB (3052127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78732683a91caaf65e905370972c95c6b0eece577cd72a1aaa09ebdb25bab15a`  
		Last Modified: Fri, 25 Oct 2024 23:58:01 GMT  
		Size: 28.0 KB (27990 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:8279ea0675cff259aec142159050dee0222a8bc163c17e4406c945a9db374380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.5 MB (247513887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ea8941fb0c15d7c37bc48a141b35be0584446c0d5ec81658aca1254dae3ddf`
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
# Fri, 25 Oct 2024 04:11:28 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 25 Oct 2024 04:11:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Oct 2024 04:11:28 GMT
ENV GOSU_VERSION=1.17
# Fri, 25 Oct 2024 04:11:28 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 25 Oct 2024 04:11:28 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 25 Oct 2024 04:11:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 25 Oct 2024 04:11:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 25 Oct 2024 04:11:28 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 25 Oct 2024 04:11:28 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 25 Oct 2024 04:11:28 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 25 Oct 2024 04:11:28 GMT
ENV MONGO_MAJOR=7.0
# Fri, 25 Oct 2024 04:11:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 25 Oct 2024 04:11:28 GMT
ENV MONGO_VERSION=7.0.15
# Fri, 25 Oct 2024 04:11:28 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 25 Oct 2024 04:11:28 GMT
VOLUME [/data/db /data/configdb]
# Fri, 25 Oct 2024 04:11:28 GMT
ENV HOME=/data/db
# Fri, 25 Oct 2024 04:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Oct 2024 04:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Oct 2024 04:11:28 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 25 Oct 2024 04:11:28 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734d6dbbc27c12b95f1ab477f3062c1b5b55e860e5608433a076e3f6303cd617`  
		Last Modified: Sat, 26 Oct 2024 00:00:19 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144e60e5b4809387eabf960f84f77793ce5b61f037fae95ec677f534bbb5f93f`  
		Last Modified: Sat, 26 Oct 2024 00:00:20 GMT  
		Size: 1.5 MB (1481417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefec46e343f09a7d424ad69e0991adc5dabbf92a5649503d9ba2a61302dd288`  
		Last Modified: Sat, 26 Oct 2024 00:00:20 GMT  
		Size: 1.0 MB (1027402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f17a100ebf45ac5dd9e917f13ac8b6078270063ad01f9d140deefa2701d884`  
		Last Modified: Sat, 26 Oct 2024 00:00:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abe9870bb1a2ff3198f9320e6ac27f42b645d109e05d955b62cf9829be6eb3f`  
		Last Modified: Sat, 26 Oct 2024 00:00:20 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2a20cdc0dc4a267669df52238e165d825a2a2787612447997253b44152ddb7`  
		Last Modified: Sat, 26 Oct 2024 00:00:26 GMT  
		Size: 217.6 MB (217639573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810b9e368bc32744a89edc8ef67b3a5befac5a33ac24d5ef50a90dddee9e59de`  
		Last Modified: Sat, 26 Oct 2024 00:00:21 GMT  
		Size: 5.0 KB (4999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:819696d4fe2cf25eed954075cd887fac7181a9f21e0bb845db35e2f2e637924f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3080639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5a468627d63a301dbd9b785c4b56f397e73d78dcebe90106ff8a039557ab6b`

```dockerfile
```

-	Layers:
	-	`sha256:5eee679cd5d3c115684290fb2e962352c2acecc8e4a49df6a509940a9a095474`  
		Last Modified: Sat, 26 Oct 2024 00:00:20 GMT  
		Size: 3.1 MB (3052445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d7d0aeaf83583b069eb541aa7be4f7d709deb8aa062fdc0e4cab0efb4d8e3c2`  
		Last Modified: Sat, 26 Oct 2024 00:00:20 GMT  
		Size: 28.2 KB (28194 bytes)  
		MIME: application/vnd.in-toto+json
