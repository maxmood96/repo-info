## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:393556b45a745f9ffd0e6542503ae8ff229984c7b7c9e01a150bdd67f3c4d332
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:6789519c0026d84b41591f26b810b745b1d7dfd19991be712a710a8139ae40ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280075992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626bb65b2a783570c80fc1604037b319219e10a0ee89261edb4397b94410cd26`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42869c9f398f4acb68bc4873982e8ec73c56f5aa6c158683a33309a93928e19d`  
		Last Modified: Tue, 02 Sep 2025 00:24:48 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7f42db5a9c374f32537f0ff8bdbab082d419e7b505f5f8f082eface26d8d93`  
		Last Modified: Tue, 02 Sep 2025 00:24:49 GMT  
		Size: 1.5 MB (1513818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42686e6bd012040a618b622a84e97498325b3a037ee72a2410771b7fdee26706`  
		Last Modified: Tue, 02 Sep 2025 00:24:49 GMT  
		Size: 1.1 MB (1095134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70dec88ea665815c4f5e58885e889b7c144730c038d99533449177118afd843`  
		Last Modified: Tue, 02 Sep 2025 00:24:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0215223c89d650bfad876935b9af5f4954543ece3a8c08552a4cefbb70f295`  
		Last Modified: Tue, 02 Sep 2025 00:24:49 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836cc8275d7863d915fd1279542108ee6b8133a5414754fdfe7fadc7d029267c`  
		Last Modified: Tue, 02 Sep 2025 00:29:25 GMT  
		Size: 247.9 MB (247922942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d148e43fcf23d2c68bed5c82263e416e2bc02504528fbfc8a51c2391f67a544a`  
		Last Modified: Tue, 02 Sep 2025 00:24:49 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:18f601abe2b90ffb03639fe6fbc946abf124fdb757ccd02b7a76abfbb6dbcd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3251932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7d56fb53ed73aafb05d789cea161759fb23add154fd670edf9f5b0d5823057`

```dockerfile
```

-	Layers:
	-	`sha256:cee23b9da14f8498e86568a5a2d03423f521666f21617a3082aa1cfec5d9542c`  
		Last Modified: Tue, 02 Sep 2025 01:07:36 GMT  
		Size: 3.2 MB (3223943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e957cf66e29d65f9421659d2d7a275ac5d46dd09e0feaddb1ad4a7212b5d3179`  
		Last Modified: Tue, 02 Sep 2025 01:07:37 GMT  
		Size: 28.0 KB (27989 bytes)  
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
