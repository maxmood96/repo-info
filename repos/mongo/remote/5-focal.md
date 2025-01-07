## `mongo:5-focal`

```console
$ docker pull mongo@sha256:5cd2a3f5594e4b12b2e995a96ad681ff4cfdc57b3b985f1d567c91af909af90d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:5-focal` - linux; amd64

```console
$ docker pull mongo@sha256:02425a4d2150ff04e01a515388f4190d4dcc73b1912a5be5c993eda18bb07412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263869770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1e02a705a3c51d7cd3f499ca2bcd2d1bbfed657b46911ddf1e33dd898d11fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Fri, 25 Oct 2024 04:01:11 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 25 Oct 2024 04:01:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Oct 2024 04:01:11 GMT
ENV GOSU_VERSION=1.17
# Fri, 25 Oct 2024 04:01:11 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 25 Oct 2024 04:01:11 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 25 Oct 2024 04:01:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-5.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 25 Oct 2024 04:01:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 25 Oct 2024 04:01:11 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 25 Oct 2024 04:01:11 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 25 Oct 2024 04:01:11 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 25 Oct 2024 04:01:11 GMT
ENV MONGO_MAJOR=5.0
# Fri, 25 Oct 2024 04:01:11 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 25 Oct 2024 04:01:11 GMT
ENV MONGO_VERSION=5.0.30
# Fri, 25 Oct 2024 04:01:11 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 25 Oct 2024 04:01:11 GMT
VOLUME [/data/db /data/configdb]
# Fri, 25 Oct 2024 04:01:11 GMT
ENV HOME=/data/db
# Fri, 25 Oct 2024 04:01:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Oct 2024 04:01:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Oct 2024 04:01:11 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 25 Oct 2024 04:01:11 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c639256977f2ab6985f966a7789809636ded5584acc97db22542b740ea1a51a7`  
		Last Modified: Fri, 25 Oct 2024 23:58:11 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc495391c999703ddec0e04202263013bfabc38451d7c3392c53deeb838dbee2`  
		Last Modified: Fri, 25 Oct 2024 23:58:11 GMT  
		Size: 3.1 MB (3094287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108af7d9389b8e86e8e22cddb5cb51546128ec4a9f4691fc0374034b452d0c80`  
		Size: 1.1 MB (1091645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17345914fafb4908b7f8dd7003021539580b2e303cc9224e0e5ccfd1fedf71e1`  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda15e596a1e8d891cf59f751ef17e27b7748d7b7292b40db64ad910397696b9`  
		Last Modified: Fri, 25 Oct 2024 23:58:12 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694f3c40f621034016d9ad5867d3bbac69ca91d1e9b4a151bba1f5f1a3a52cb3`  
		Last Modified: Fri, 25 Oct 2024 23:58:15 GMT  
		Size: 232.2 MB (232165627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72839d4ce31b51ff6984704947b3737d8656deb0077ba073ba8924e06fccfb96`  
		Last Modified: Fri, 25 Oct 2024 23:58:12 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:aca619abbce716240ab29772132ce2d28ebc01698d4765a8892d3b62c49befa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3080877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe7899b87b778e4a6b3f0f82354412e9c6a583344dc0d814617b9f9b19c495b`

```dockerfile
```

-	Layers:
	-	`sha256:fddacfafe16d7ccaac251a8481932a64627371a04506c6981227b752f8ce0979`  
		Last Modified: Fri, 25 Oct 2024 23:58:11 GMT  
		Size: 3.1 MB (3053208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceed8d5b97fc42c97d5b7f39886690d877e5d275229a80c6fb2516cc91a51f7e`  
		Last Modified: Fri, 25 Oct 2024 23:58:11 GMT  
		Size: 27.7 KB (27669 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:5-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:44f22afd5594be7988d5ae52350b33d00e9f9c3555a97193c98f44784d473929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253550060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689e1e70fd703b383c78b102b17a18ba45923e84a7176f563279778f1c75de7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Fri, 25 Oct 2024 04:01:11 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 25 Oct 2024 04:01:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Oct 2024 04:01:11 GMT
ENV GOSU_VERSION=1.17
# Fri, 25 Oct 2024 04:01:11 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 25 Oct 2024 04:01:11 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 25 Oct 2024 04:01:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-5.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 25 Oct 2024 04:01:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 25 Oct 2024 04:01:11 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 25 Oct 2024 04:01:11 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 25 Oct 2024 04:01:11 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 25 Oct 2024 04:01:11 GMT
ENV MONGO_MAJOR=5.0
# Fri, 25 Oct 2024 04:01:11 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 25 Oct 2024 04:01:11 GMT
ENV MONGO_VERSION=5.0.30
# Fri, 25 Oct 2024 04:01:11 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 25 Oct 2024 04:01:11 GMT
VOLUME [/data/db /data/configdb]
# Fri, 25 Oct 2024 04:01:11 GMT
ENV HOME=/data/db
# Fri, 25 Oct 2024 04:01:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Oct 2024 04:01:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Oct 2024 04:01:11 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 25 Oct 2024 04:01:11 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d7fd7ec32066589a5ec2eba9f948ec532fe1e032339df12dfb6f7e4ae9f13`  
		Last Modified: Sat, 26 Oct 2024 00:03:27 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98dbb51de1139770906897ef0e5a71c2c35f94ab4dc53cfabd46ec9ff08a69c5`  
		Last Modified: Sat, 26 Oct 2024 00:03:28 GMT  
		Size: 2.9 MB (2943219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38a47385442a8d8acbb07b707e484a1d33af7fee5dd9132906cf0005804a655`  
		Last Modified: Sat, 26 Oct 2024 00:03:28 GMT  
		Size: 1.0 MB (1023832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ef69d9191fa40bc36559ea14f14c38f4ef14c1562a5838baec0ab6a74b563c`  
		Last Modified: Sat, 26 Oct 2024 00:03:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d454a4e444447d15d0fd76c64062cdb40a386e8cc48f96919edb8e9eaeb80a`  
		Last Modified: Sat, 26 Oct 2024 00:03:28 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a983b3d9bc2d2de55aaef93c1e383cd494e082ede44409e194935b879210da9`  
		Last Modified: Sat, 26 Oct 2024 00:03:33 GMT  
		Size: 223.6 MB (223602030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6464c66f671bbf7b95472b6660a9e84ee28d94d03ff09d39e638be0981f92a30`  
		Last Modified: Sat, 26 Oct 2024 00:03:29 GMT  
		Size: 5.0 KB (4991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:6e311de6d41cee35ac6a90ccd9bc81b4a1b3997478b173e6d98cae4a7b8cf89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3081378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c731d31bc3ab147025756e8d34ca87ace4ac92f478d73de37e085ef73cb0cb7f`

```dockerfile
```

-	Layers:
	-	`sha256:cfbb45d706edc0ecfc0480a7a5fe018c9dbb23dbb61a4312adaaee02c32aa256`  
		Last Modified: Sat, 26 Oct 2024 00:03:28 GMT  
		Size: 3.1 MB (3053506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e67dda861ef25dcb8d67e49be6fe8bfd5283fbda267c29a43214f53ede326f9d`  
		Last Modified: Sat, 26 Oct 2024 00:03:27 GMT  
		Size: 27.9 KB (27872 bytes)  
		MIME: application/vnd.in-toto+json
