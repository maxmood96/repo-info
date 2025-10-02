## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:36d6622d4201a62e0fa8e4903c95b9254c451f0da6c39546b1e16924424cfe46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:cfb81b675168ceceecfebb79c571cf745ff2d718e8c1a9ade2d5a45f6d86ac63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266750844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7404a43ea8192b0be554358e0d4bef2b5e558afc5c241ba50270e5b49dd95036`
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 23 Sep 2025 19:30:00 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 23 Sep 2025 19:30:00 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 23 Sep 2025 19:30:00 GMT
ENV MONGO_MAJOR=6.0
# Tue, 23 Sep 2025 19:30:00 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
ENV MONGO_VERSION=6.0.26
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
	-	`sha256:8a47d1dc7ddb820234c4edf8522982ea5acda4b94beb69ac23a55f310955ca3f`  
		Last Modified: Tue, 23 Sep 2025 23:18:53 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8fa2df2a1ab9ca08d3c820262c7376f97d4dc885fabc7cf4d80dfe80bd83f0`  
		Last Modified: Tue, 23 Sep 2025 23:18:56 GMT  
		Size: 1.5 MB (1513740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2d9c2177645b6b9c513f921a8e49d8804c436799c438a8a48b40b8e4732aee`  
		Last Modified: Tue, 23 Sep 2025 23:18:55 GMT  
		Size: 898.1 KB (898053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8375ea5eafa73a14744838f7d8d661bdeef31f940a1cfa50add714ec373195c`  
		Last Modified: Tue, 23 Sep 2025 23:18:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085259f2d883900ac80a5d5d33650a5074b3276aa74b0753db90eeb592ffed44`  
		Last Modified: Tue, 23 Sep 2025 23:18:55 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801d080ac008f521c458328c81cd35cc4682f5c17cea6c48af85ff2e497bc697`  
		Last Modified: Wed, 24 Sep 2025 01:07:58 GMT  
		Size: 234.8 MB (234794952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faca1a662cf80c0dd9a57fb40e549b5ba64f6ccac186ae95b567a252432e7992`  
		Last Modified: Tue, 23 Sep 2025 23:18:55 GMT  
		Size: 5.0 KB (5001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:f6b6ce36add9d830307d5482a7349daccd24e88284b3504b451f741b3aa25fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3251925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d889daca89a07e4617d3383ac434990df723461f5010e386d9353b2753945af`

```dockerfile
```

-	Layers:
	-	`sha256:dafc1c4e39ed1f4fd9d3529b5932caaf22bab61ab18b7a85b2f217933c1e6b9c`  
		Last Modified: Wed, 24 Sep 2025 01:07:23 GMT  
		Size: 3.2 MB (3223939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9b299278886c4fc0c22377c0d41f8eb2b64546698a2f46585fcbc94d88b432c`  
		Last Modified: Wed, 24 Sep 2025 01:07:24 GMT  
		Size: 28.0 KB (27986 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:fc5340eb5a74307968b493b4f2b1f58f8564fa90152b8332e8b6555a4f0712b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255550274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29d1e0ac4c42b531d00e586686abfe7e039fc2ac9b267949e54825d0afb65ed`
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 23 Sep 2025 19:30:00 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 23 Sep 2025 19:30:00 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 23 Sep 2025 19:30:00 GMT
ENV MONGO_MAJOR=6.0
# Tue, 23 Sep 2025 19:30:00 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 23 Sep 2025 19:30:00 GMT
ENV MONGO_VERSION=6.0.26
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
	-	`sha256:ca78afc50c9b9aff183264118db609f6752451f95fff5fd6405719b0e6f367b8`  
		Last Modified: Thu, 02 Oct 2025 01:27:57 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfacf7a0d91a048580b0a103064e9853d6a0dd0bf3c4489ae3b815de93ca0a90`  
		Last Modified: Thu, 02 Oct 2025 01:27:57 GMT  
		Size: 1.5 MB (1482380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0679a39cdc37e200713c9396b6dbe2bc5a0cd5322c3ad2e13b620172b65933fe`  
		Last Modified: Thu, 02 Oct 2025 01:27:57 GMT  
		Size: 850.5 KB (850529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff85dc5e4242c9162adfb863fc9238b621b605e7acc9dd0666096d244c9f0701`  
		Last Modified: Thu, 02 Oct 2025 01:27:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b45abd6e46f5b2f1e58875a54112be0790597dffd9d7b74b7dfc6d97e419a8`  
		Last Modified: Thu, 02 Oct 2025 01:27:56 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af08e485dd3ea4d954770a280264c57e076eaa9a9cdf9348f2db3bd64d738471`  
		Last Modified: Thu, 02 Oct 2025 02:28:48 GMT  
		Size: 225.8 MB (225827097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e98464ad5c426168e989b44210a7237fe4d968efbe20d1a2935d900359a6a62`  
		Last Modified: Thu, 02 Oct 2025 01:27:56 GMT  
		Size: 5.0 KB (5000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:a44f258581960c66bc87bdb9e367f2dfbea0c13f21fea0da5277f7e25f0a54c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f38d48fd629bcb330bcfa18adf165b5e773ea016dfa56d52bc8e6df50835065`

```dockerfile
```

-	Layers:
	-	`sha256:d22d8938bb235eb01a72f67f256e5bc3dcc84d60a8d8a4272f388952c0f985d8`  
		Last Modified: Thu, 02 Oct 2025 04:07:24 GMT  
		Size: 3.2 MB (3224258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4701c9dc416865750cc20fd7eb258794f7147a59cc1699f063deb4d3cbad16f3`  
		Last Modified: Thu, 02 Oct 2025 04:07:25 GMT  
		Size: 28.2 KB (28189 bytes)  
		MIME: application/vnd.in-toto+json
