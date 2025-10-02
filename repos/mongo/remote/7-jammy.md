## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:83d2871ffff38b5a2e0599045b94fe0c42240a1142c17569cf093578b2be0d1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:f52818ecf4e41d1efa08b8da2c129ca91c55089b56c5d58fb9871c91757bf240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279792446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf268408fc594dda9854f84c2baa2ed9059c3ffe3644ec07169a970f408fe55d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:00 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:00 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 23 Sep 2025 19:30:00 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 23 Sep 2025 19:30:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 23 Sep 2025 19:30:00 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 23 Sep 2025 19:30:00 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 23 Sep 2025 19:30:00 GMT
ENV MONGO_MAJOR=7.0
# Tue, 23 Sep 2025 19:30:00 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
ENV MONGO_VERSION=7.0.24
# Tue, 23 Sep 2025 19:30:00 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
VOLUME [/data/db /data/configdb]
# Tue, 23 Sep 2025 19:30:00 GMT
ENV HOME=/data/db
# Tue, 23 Sep 2025 19:30:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:00 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 23 Sep 2025 19:30:00 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec080621ab5b2f87a7f00e7f9e1927788701eda5a321843d9106a5514a1355c1`  
		Last Modified: Tue, 23 Sep 2025 23:18:20 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d931995d7c3b2d7dce6412b0b7ff9aca64321ba09b08c1156151ad55436595ac`  
		Last Modified: Tue, 23 Sep 2025 23:18:21 GMT  
		Size: 1.5 MB (1513793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708b21e918f1b53e607f86a3f1eddb32b0293603e1d3c670e71c90abc22b04bd`  
		Last Modified: Tue, 23 Sep 2025 23:18:21 GMT  
		Size: 898.1 KB (898093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b400a31ec3bf70fa6a6b65e85b53a7aa69476b4b24abda82c646024499f28330`  
		Last Modified: Tue, 23 Sep 2025 23:18:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67e38654598989b63be74f8be042a88973f5620915389a9a91fde65afff6223`  
		Last Modified: Tue, 23 Sep 2025 23:18:21 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8100c7c13643ff0dc932f358c0e91b68500c08c81b91bc19273c573c58cdb220`  
		Last Modified: Tue, 23 Sep 2025 23:28:12 GMT  
		Size: 247.8 MB (247836464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6cb34e0f7327a9788da97962aa371f4c1c725a1a3e33298dba0123c4a082c5`  
		Last Modified: Tue, 23 Sep 2025 23:18:21 GMT  
		Size: 5.0 KB (4998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:e438c19ac92f96f1fdede9b3105d622355b11a598244a05c93448add8fda81f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3251925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af7a747f0d0eed11b58f9246bba90822dbf98b7b1351c48ad980afc499c5daf`

```dockerfile
```

-	Layers:
	-	`sha256:5dee0d0210064de7d2c35b2b5612d459640bb969715f11edc59c8b382a3ce6af`  
		Last Modified: Wed, 24 Sep 2025 01:07:46 GMT  
		Size: 3.2 MB (3223939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c03e118757a34a6111f2dcb4a111956a53109928709d7285728334108b920bee`  
		Last Modified: Wed, 24 Sep 2025 01:07:47 GMT  
		Size: 28.0 KB (27986 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:c632000bacffc7f0f476effa91ea261fcc4502a924246db2e43d980b19b1dafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.1 MB (267054433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe091090d27a6da3cb4826a116fd38eb47ae50ed1acd04074528246a497bf621`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 23 Sep 2025 19:30:00 GMT
ARG RELEASE
# Tue, 23 Sep 2025 19:30:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 19:30:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 19:30:00 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 23 Sep 2025 19:30:00 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Tue, 23 Sep 2025 19:30:00 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 19:30:00 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:30:00 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 23 Sep 2025 19:30:00 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 23 Sep 2025 19:30:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 23 Sep 2025 19:30:00 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 23 Sep 2025 19:30:00 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 23 Sep 2025 19:30:00 GMT
ENV MONGO_MAJOR=7.0
# Tue, 23 Sep 2025 19:30:00 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
ENV MONGO_VERSION=7.0.24
# Tue, 23 Sep 2025 19:30:00 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
VOLUME [/data/db /data/configdb]
# Tue, 23 Sep 2025 19:30:00 GMT
ENV HOME=/data/db
# Tue, 23 Sep 2025 19:30:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:30:00 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 23 Sep 2025 19:30:00 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4395bb377dd9c9057d9290a33d82827ab8c0a429c1ed1b0a142342c852c9a2e9`  
		Last Modified: Thu, 02 Oct 2025 01:27:57 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc46d0f1b6577b7a2792ab5a8f7aaad5201ebeeb6b7638ca64d68a5b9a113fcc`  
		Last Modified: Thu, 02 Oct 2025 01:27:57 GMT  
		Size: 1.5 MB (1482390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfb40faa05540d4e0272334a197e30c812d09b4af9da0140480a3536af4c1f4`  
		Last Modified: Thu, 02 Oct 2025 01:27:58 GMT  
		Size: 850.5 KB (850549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c39403d0cf68c90d3142bd8a2bc3b648526c0ff698d8723bbdd40c2e24f6744`  
		Last Modified: Thu, 02 Oct 2025 01:27:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de6770684e5bd006fa2f13f336f93ea5d5e0c8284dac5edc3a25692b7d58b76`  
		Last Modified: Thu, 02 Oct 2025 01:27:57 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8ff0433f6f72a892d40226df4830e28adc1218a6dee176ca41ef3dfc49aba1`  
		Last Modified: Thu, 02 Oct 2025 02:32:10 GMT  
		Size: 237.3 MB (237331223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1231dfed087ed221465e8e169ac55c5e8243d0d5394f106a3363ebdad2385c`  
		Last Modified: Thu, 02 Oct 2025 01:27:57 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:111165a7ccf3add72f6463c08eb7f4540b1d3fd250788e0182436a83edef2f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becf0a2e963b147a7c3bdffc8f813ff278c93d6c29ebf101fa6924f1df8a8977`

```dockerfile
```

-	Layers:
	-	`sha256:b859c3ea31942ef87df06deedc97faf02dff634db3c3fdb4f6b59461130c5481`  
		Last Modified: Thu, 02 Oct 2025 04:07:46 GMT  
		Size: 3.2 MB (3224258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9ef9a33581c291acfef46eb0be5cc5e6420946744b249d5a489e763a2fa6c58`  
		Last Modified: Thu, 02 Oct 2025 04:07:47 GMT  
		Size: 28.2 KB (28189 bytes)  
		MIME: application/vnd.in-toto+json
