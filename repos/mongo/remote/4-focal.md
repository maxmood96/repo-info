## `mongo:4-focal`

```console
$ docker pull mongo@sha256:b9bc8cd3cfb6e5cc6aa5fc94e1ac7135cba9dd2cbdaf30b761ef021b4338d729
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:4-focal` - linux; amd64

```console
$ docker pull mongo@sha256:06d63ac6a9bea27017da01bf024a19c19fd6e44a4b2a42188bd8e4730ae9aa9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.1 MB (173059878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc8406a7c95f23d7be778b6c524428fb47cb82948d4c8b2220904af3d9bf10f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 23:25:19 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 29 Feb 2024 23:25:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 23:25:19 GMT
ENV GOSU_VERSION=1.17
# Thu, 29 Feb 2024 23:25:19 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 29 Feb 2024 23:25:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-4.4.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '20691EEC35216C63CAF66CE1656408E390CFB1F5' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Feb 2024 23:25:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Feb 2024 23:25:19 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 29 Feb 2024 23:25:19 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:25:19 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:25:19 GMT
ENV MONGO_MAJOR=4.4
# Thu, 29 Feb 2024 23:25:19 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 29 Feb 2024 23:25:19 GMT
ENV MONGO_VERSION=4.4.29
# Thu, 29 Feb 2024 23:25:19 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 29 Feb 2024 23:25:19 GMT
VOLUME [/data/db /data/configdb]
# Thu, 29 Feb 2024 23:25:19 GMT
ENV HOME=/data/db
# Thu, 29 Feb 2024 23:25:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 23:25:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 23:25:19 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 29 Feb 2024 23:25:19 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487ea3c5fbdc3dd2f8f7d5256cd6331a493dfd9470650fbdfbec01edc319fa4`  
		Last Modified: Fri, 01 Mar 2024 00:50:20 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431ed8625b59f5260ff8ae60b24ad834fe17fef95fdcc7fdcf5eaa20c86b318f`  
		Last Modified: Fri, 01 Mar 2024 00:50:20 GMT  
		Size: 3.1 MB (3076329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e25f51968e8b08f1f049bff3cdf9551d7d99f83d33aaebc5187e8b33499b748`  
		Last Modified: Fri, 01 Mar 2024 00:50:20 GMT  
		Size: 1.1 MB (1091386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb446c04ffd50b51d2b40e516fb021a603d392cb9ceeb55dbcbb670c216f64fe`  
		Last Modified: Fri, 01 Mar 2024 00:50:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4df67ea53c6f7d36bf463746012aa9c71ecfe2c661afd54d56fd1b7b15302c`  
		Last Modified: Fri, 01 Mar 2024 00:50:21 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7827965ef64d4dbcc7fe975e12afba2cdc1bcc02ac447654effa6de48ab638`  
		Last Modified: Fri, 01 Mar 2024 00:50:23 GMT  
		Size: 141.4 MB (141370082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd90548d5131beda18bc752547f7e669dd209149d8ab9c1e579fd325940a30d3`  
		Last Modified: Fri, 01 Mar 2024 00:50:21 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:4-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:cb2fe0b00c405e988f7bb5b67ba07e2cc04a5dec37cf187f55c29e5bb6988d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3017605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd027e5bc7ee194d1c320720266652e3918a2f3937caa68cbd3531d9b658d8f6`

```dockerfile
```

-	Layers:
	-	`sha256:f39cff0d90548b26cea8f496214ca8ae27db025dca863a844e78108b43f855cb`  
		Last Modified: Fri, 01 Mar 2024 00:50:20 GMT  
		Size: 3.0 MB (2990773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b05d9ec0e908cf527c085bd93f9dcaab3659981ed7353e31d71aa01af1a774d6`  
		Last Modified: Fri, 01 Mar 2024 00:50:20 GMT  
		Size: 26.8 KB (26832 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:4-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:93d3321d559d04e7991bde2529d5fb0dc3ba833247dc95b0fd3b6a68420b19ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.3 MB (168312137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436fdd6e693e7a1672d4c8cd142f7b4afc3d51366c9c3915a666730086268c4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 23:25:19 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 29 Feb 2024 23:25:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 23:25:19 GMT
ENV GOSU_VERSION=1.17
# Thu, 29 Feb 2024 23:25:19 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 29 Feb 2024 23:25:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-4.4.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '20691EEC35216C63CAF66CE1656408E390CFB1F5' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Feb 2024 23:25:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Feb 2024 23:25:19 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 29 Feb 2024 23:25:19 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:25:19 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:25:19 GMT
ENV MONGO_MAJOR=4.4
# Thu, 29 Feb 2024 23:25:19 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 29 Feb 2024 23:25:19 GMT
ENV MONGO_VERSION=4.4.29
# Thu, 29 Feb 2024 23:25:19 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 29 Feb 2024 23:25:19 GMT
VOLUME [/data/db /data/configdb]
# Thu, 29 Feb 2024 23:25:19 GMT
ENV HOME=/data/db
# Thu, 29 Feb 2024 23:25:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 23:25:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 23:25:19 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 29 Feb 2024 23:25:19 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234fb188b2907c9715c7137a90acbfd86a567df40cb64cba4347f0e70b62bf32`  
		Last Modified: Sat, 03 Feb 2024 08:43:47 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3e56574048716548ffedbd95cd3f241e84077f8afa6862852f8eebe3c60a9f`  
		Last Modified: Wed, 07 Feb 2024 02:31:59 GMT  
		Size: 2.9 MB (2927602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adda3404e07ff98ab203ee0e2081cc749594009b960611c735ecb1189f6fb9f2`  
		Last Modified: Wed, 07 Feb 2024 02:33:24 GMT  
		Size: 1.0 MB (1023724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2a8b8a8e02ee59dc295f023a3bbccb9e76025c101bcfc5c0a86fa00ba0560c`  
		Last Modified: Wed, 07 Feb 2024 02:33:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4c3428fb423dffd3be491a8912830972e23e616ae7c9a358a8c776be3f97d4`  
		Last Modified: Wed, 07 Feb 2024 02:33:24 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fd3e4c72e9ffb5f5847c50998220f4fac3f10f9ea700616a4131504845e4b7`  
		Last Modified: Fri, 01 Mar 2024 06:58:57 GMT  
		Size: 138.4 MB (138378054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d4df08e238852b3b63aef16b4ef85cba6c94a05c6dbc629ba058dc051f5be`  
		Last Modified: Fri, 01 Mar 2024 06:58:53 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:4-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:1d02f131d33d78e3cdc7e3f199282080c311a9f18299315873766af013d0bc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3017690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d9bffc4ab6679c4c94ba98dc85d8f7f1117b3b3fd8d20efda6bcd69e5b07e2`

```dockerfile
```

-	Layers:
	-	`sha256:d146f59e3ed011ac2620891174133439c88ea05b075debef944903167e8ec147`  
		Last Modified: Fri, 01 Mar 2024 06:58:53 GMT  
		Size: 3.0 MB (2991006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4ab2aff88631dc07bac6ae3152943472d3e3e1056f926f189a4738af86f90c6`  
		Last Modified: Fri, 01 Mar 2024 06:58:53 GMT  
		Size: 26.7 KB (26684 bytes)  
		MIME: application/vnd.in-toto+json
