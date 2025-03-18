## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:8eed65a7d588cadc1d59ccc0101707f060ee03006fb6aeed0f8fb6ef7c03625b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:9aafba5985b7ac9be16b11332e2529123f9e1cea7931c7ee0462068a9e3c0371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258100886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da299f6229b0806644154c41ddbbbb80ed7a9039b4d3398a8e5d912d231db655`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Mon, 17 Mar 2025 22:01:11 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 17 Mar 2025 22:01:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Mar 2025 22:01:11 GMT
ENV GOSU_VERSION=1.17
# Mon, 17 Mar 2025 22:01:11 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 17 Mar 2025 22:01:11 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Mon, 17 Mar 2025 22:01:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 17 Mar 2025 22:01:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 17 Mar 2025 22:01:11 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 17 Mar 2025 22:01:11 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 17 Mar 2025 22:01:11 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 17 Mar 2025 22:01:11 GMT
ENV MONGO_MAJOR=6.0
# Mon, 17 Mar 2025 22:01:11 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 17 Mar 2025 22:01:11 GMT
ENV MONGO_VERSION=6.0.21
# Mon, 17 Mar 2025 22:01:11 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 17 Mar 2025 22:01:11 GMT
VOLUME [/data/db /data/configdb]
# Mon, 17 Mar 2025 22:01:11 GMT
ENV HOME=/data/db
# Mon, 17 Mar 2025 22:01:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Mar 2025 22:01:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Mar 2025 22:01:11 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 17 Mar 2025 22:01:11 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147a757512f6b666c08b0d10c0fd8cfb6a1a97e7a5c35fb9805582d6da47959a`  
		Last Modified: Tue, 18 Mar 2025 17:19:16 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876012a5f4b7606345992d081dc9a9d1949aa5ace1b4ba1bfb9983c8f6385c8f`  
		Last Modified: Tue, 18 Mar 2025 17:19:16 GMT  
		Size: 1.5 MB (1513282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b91eb705c7e75a3a154ab69d8253852792600d35341baf14aeef399702bbf2`  
		Last Modified: Tue, 18 Mar 2025 17:19:16 GMT  
		Size: 1.1 MB (1095110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa49e3e29adea3ada96a62299829728b643813cee2e6e23dddce3c14269096d`  
		Last Modified: Tue, 18 Mar 2025 17:19:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152a4f6c3783c91f00566af253a6b869ada7bcb97cacbc3f775543e998476e8f`  
		Last Modified: Tue, 18 Mar 2025 17:19:17 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61401eeca3a3fb372bdfc4ad430e934753832c999543b61473bf07058d24a02b`  
		Last Modified: Tue, 18 Mar 2025 17:19:23 GMT  
		Size: 225.9 MB (225949395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1c81570b11f0bc63688577bd4abf6b7195d1a5360a5fae08be3a9c8fe84dc9`  
		Last Modified: Tue, 18 Mar 2025 17:19:17 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:76a3bd2683ab7eeaa88f56326233051b0ef170800c0c4bf1a826f9c008f41667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3102094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec74a38f67e3fb094120a95fd76cb0fc29e5798386ef172a1d686b4d19f3d7c`

```dockerfile
```

-	Layers:
	-	`sha256:0378a625a0cb25f3fbe38c6689450b5158b9299a34833da321b405582ce9672d`  
		Last Modified: Tue, 18 Mar 2025 17:19:16 GMT  
		Size: 3.1 MB (3074103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66440fc488c2af5ee7e189869b3922197156adf310a90e6576d18d5fff686720`  
		Last Modified: Tue, 18 Mar 2025 17:19:16 GMT  
		Size: 28.0 KB (27991 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:0a9067cdba7ac3f412119c1e5e653308b7c1fab50f69b4d0fb4edfd8e5a3f3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.5 MB (247510272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc9678f5cc7574df402714ade2ebd706e651eddee3cb0799fc3a805d2f845f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 15 Jan 2025 17:06:20 GMT
ARG RELEASE
# Wed, 15 Jan 2025 17:06:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 15 Jan 2025 17:06:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 15 Jan 2025 17:06:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 15 Jan 2025 17:06:20 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Wed, 15 Jan 2025 17:06:20 GMT
CMD ["/bin/bash"]
# Wed, 15 Jan 2025 17:06:20 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 15 Jan 2025 17:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Jan 2025 17:06:20 GMT
ENV GOSU_VERSION=1.17
# Wed, 15 Jan 2025 17:06:20 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 15 Jan 2025 17:06:20 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Wed, 15 Jan 2025 17:06:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Jan 2025 17:06:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Jan 2025 17:06:20 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 15 Jan 2025 17:06:20 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 15 Jan 2025 17:06:20 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 15 Jan 2025 17:06:20 GMT
ENV MONGO_MAJOR=6.0
# Wed, 15 Jan 2025 17:06:20 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 15 Jan 2025 17:06:20 GMT
ENV MONGO_VERSION=6.0.20
# Wed, 15 Jan 2025 17:06:20 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 15 Jan 2025 17:06:20 GMT
VOLUME [/data/db /data/configdb]
# Wed, 15 Jan 2025 17:06:20 GMT
ENV HOME=/data/db
# Wed, 15 Jan 2025 17:06:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Jan 2025 17:06:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Jan 2025 17:06:20 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 15 Jan 2025 17:06:20 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9d6e156c6c6367fa8873008371d39cc2d74566625ef867d6ec1010e1c80749`  
		Last Modified: Tue, 04 Feb 2025 10:10:47 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8722339df2579e4dfe90fc326438631097e0de731b957fcfab2dc56471c6ff1d`  
		Last Modified: Tue, 04 Feb 2025 10:10:47 GMT  
		Size: 1.5 MB (1481639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d410be1990efd450d8d689a1b5f69a7adaefca89de08875413368238a242ccd5`  
		Last Modified: Tue, 04 Feb 2025 10:12:13 GMT  
		Size: 1.0 MB (1027621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6667c4abbe40efeda6e5519dc908839132bd22d376e26c1036a8118f2b1b1a92`  
		Last Modified: Tue, 04 Feb 2025 10:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf83c4197e73a40235166d4395461d3210107ec8e7c6b75d3b9a279309f9ac`  
		Last Modified: Tue, 04 Feb 2025 10:12:13 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1376710818ab45acd7dca0a4ee89f7d6d50eec5999be1ef6f3fe5357352aa0`  
		Last Modified: Tue, 04 Feb 2025 10:12:18 GMT  
		Size: 217.6 MB (217635666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c6bf54697f2fc13b7c6939ffe94fd086190b4a241289a3b2fa3a927067a5f7`  
		Last Modified: Tue, 04 Feb 2025 10:12:14 GMT  
		Size: 5.0 KB (4998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:e5b9bf308ca96c0bb46733872952cda3eaa2f532dfd2d67e17e156ff33379788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3100709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcc8d36e8abb94f2f06c980980d34df8d36e8cb18bf7c7cbcd5b0334b081ae8`

```dockerfile
```

-	Layers:
	-	`sha256:116475715b97d90fda10fd9a3cc8361f98bbf1d37fefbd344e72c35960acba24`  
		Last Modified: Tue, 04 Feb 2025 10:12:13 GMT  
		Size: 3.1 MB (3072515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a4265aaa99b64c5dbe6541a278e84a2d9b3bb2679f6d24e20ecef8f4df600e`  
		Last Modified: Tue, 04 Feb 2025 10:12:13 GMT  
		Size: 28.2 KB (28194 bytes)  
		MIME: application/vnd.in-toto+json
