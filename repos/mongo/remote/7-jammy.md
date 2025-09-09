## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:0f6d97b870d0757692bfbf8ed40252339b715e0d1da5874ab9fe776784de1951
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:924ff55fd3c77ac9a05da158cff133251b6baf700ce4fe2114f719b6a279a7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279878152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42b1a5b51f4779f8f39abd5dfad9169eb1a059096f53b859986242c563a92ff`
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
# Mon, 08 Sep 2025 20:03:49 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 08 Sep 2025 20:03:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 20:03:49 GMT
ENV GOSU_VERSION=1.18
# Mon, 08 Sep 2025 20:03:49 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 08 Sep 2025 20:03:49 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Mon, 08 Sep 2025 20:03:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Sep 2025 20:03:49 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Sep 2025 20:03:49 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 08 Sep 2025 20:03:49 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 08 Sep 2025 20:03:49 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 08 Sep 2025 20:03:49 GMT
ENV MONGO_MAJOR=7.0
# Mon, 08 Sep 2025 20:03:49 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 08 Sep 2025 20:03:49 GMT
ENV MONGO_VERSION=7.0.23
# Mon, 08 Sep 2025 20:03:49 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 08 Sep 2025 20:03:49 GMT
VOLUME [/data/db /data/configdb]
# Mon, 08 Sep 2025 20:03:49 GMT
ENV HOME=/data/db
# Mon, 08 Sep 2025 20:03:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 20:03:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 20:03:49 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 08 Sep 2025 20:03:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8069ef369dba12281edf117d37fdb76c7c52b2e4799668dd6722f9ae6f622f`  
		Last Modified: Mon, 08 Sep 2025 22:39:27 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0640117a40e4938d95b1d888a70a7e9f09ece551076db341f18c177e9783dd`  
		Last Modified: Mon, 08 Sep 2025 22:39:31 GMT  
		Size: 1.5 MB (1513806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04cd11dfa0008919534d23748a203d510a72db0c70fd30f1e35d1a643257ac2`  
		Last Modified: Mon, 08 Sep 2025 22:39:39 GMT  
		Size: 897.3 KB (897317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e3940a139ba188b4f0e2e83616438599ad769eb977ef27999331c1817715dd`  
		Last Modified: Mon, 08 Sep 2025 22:39:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507abacc6816954d3ee7a51425f3730bf77582c0a640576144749833bb54c5ca`  
		Last Modified: Mon, 08 Sep 2025 22:39:46 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa0e366c9995f33630c873426e76668b7653e85995080c39111d2d31cd50bc3`  
		Last Modified: Mon, 08 Sep 2025 22:44:49 GMT  
		Size: 247.9 MB (247922934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab0b2a4a64b471ab4666bbe07456fd853e01457d9a3877854cf08069ee840fc`  
		Last Modified: Mon, 08 Sep 2025 22:39:49 GMT  
		Size: 5.0 KB (5000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:c2819853aacf180dab101624d340a0dd7b57b136a1f2f4f92249de3f6155a8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3251925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030c7946aef79815e75621f00d92737fd9506cb3cfed025cca0786c808df62ad`

```dockerfile
```

-	Layers:
	-	`sha256:44482d9a119e50dc994833e8a33a61e607a5096134463d4080fb3238de013719`  
		Last Modified: Tue, 09 Sep 2025 01:07:41 GMT  
		Size: 3.2 MB (3223939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8b7a0a2dda617eb6a3ce7ba7a4afd1cb3406d1d0bbcdcf009d2d243427ba9be`  
		Last Modified: Tue, 09 Sep 2025 01:07:42 GMT  
		Size: 28.0 KB (27986 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:c913fed9cd2f22198efa44049550416b8b18de4bb9009aa151f537d99b415384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267383425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e7c3ab5ec62e703fd6b651754a35f84a49f70c1cea0dd8be735e8133cb687`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 13 Aug 2025 22:01:21 GMT
ARG RELEASE
# Wed, 13 Aug 2025 22:01:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Aug 2025 22:01:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Aug 2025 22:01:21 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 13 Aug 2025 22:01:21 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Wed, 13 Aug 2025 22:01:21 GMT
CMD ["/bin/bash"]
# Wed, 13 Aug 2025 22:01:21 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 13 Aug 2025 22:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Aug 2025 22:01:21 GMT
ENV GOSU_VERSION=1.17
# Wed, 13 Aug 2025 22:01:21 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 13 Aug 2025 22:01:21 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Wed, 13 Aug 2025 22:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 Aug 2025 22:01:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 13 Aug 2025 22:01:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 13 Aug 2025 22:01:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 13 Aug 2025 22:01:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 13 Aug 2025 22:01:21 GMT
ENV MONGO_MAJOR=7.0
# Wed, 13 Aug 2025 22:01:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 13 Aug 2025 22:01:21 GMT
ENV MONGO_VERSION=7.0.23
# Wed, 13 Aug 2025 22:01:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 13 Aug 2025 22:01:21 GMT
VOLUME [/data/db /data/configdb]
# Wed, 13 Aug 2025 22:01:21 GMT
ENV HOME=/data/db
# Wed, 13 Aug 2025 22:01:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 22:01:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 22:01:21 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 13 Aug 2025 22:01:21 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b843a43cd4e6b19e24683fd320160c91ff88d01428a2702f2b76e569f89e2b65`  
		Last Modified: Tue, 02 Sep 2025 02:28:52 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f044f8713b789a5ddb654658beeeff4cf8b772640b95d95495013aa3e16915b`  
		Last Modified: Tue, 02 Sep 2025 02:28:52 GMT  
		Size: 1.5 MB (1482407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e8947d1b9f2bb692bcac9b2c188b318e732a2ae75f2db67532c77715dbaffb`  
		Last Modified: Tue, 02 Sep 2025 02:29:55 GMT  
		Size: 1.0 MB (1027798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6308449df9f06d4498158009b36371ea70c0da6eb6117df99af8572e6d969bb`  
		Last Modified: Tue, 02 Sep 2025 02:29:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9b1aa7618186391705392b2d3c899c58140353283d27c1d4e06ce3e0e32e65`  
		Last Modified: Tue, 02 Sep 2025 02:29:55 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d049fb6c750dc2816b5af3b40f84b47fb28bcdc00d5f0fd168a4769d9050e3b`  
		Last Modified: Tue, 02 Sep 2025 03:26:41 GMT  
		Size: 237.5 MB (237504585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73e22ac645dffe3840c5dec7ba548957bcfb26162a4bc3096cee2893c43881c`  
		Last Modified: Tue, 02 Sep 2025 02:29:55 GMT  
		Size: 5.0 KB (5001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:64a7e06d8b58613ab5390b23ac4231845d3424e39854c6a8d880e394c48fb582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8690bde0adccc58ffd5eee00135fd2fdb86171bcf8ce55b0ce686aa70edc55`

```dockerfile
```

-	Layers:
	-	`sha256:42d9e43eb1125b009ac4312f0d33ff84e4615ad38de640c4c2da376f15904bfe`  
		Last Modified: Tue, 02 Sep 2025 04:07:39 GMT  
		Size: 3.2 MB (3224262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a700f595bd152325e60650c71d510d8723972e2732cea96368c450149625f5bf`  
		Last Modified: Tue, 02 Sep 2025 04:07:40 GMT  
		Size: 28.2 KB (28194 bytes)  
		MIME: application/vnd.in-toto+json
