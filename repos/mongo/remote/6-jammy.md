## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:3d5b0d61968d7637427368648bc2410b17983622d604bcdea9ce73714905ef4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:a25e4ed58c36590c8c1f2ee42f976132f7c6bf4403ae7ab0ab5ba1577c0144d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262315688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bcab5453b4498e3de17f873a290d04828ac1a0a5ceaf7bdc12509342fd24c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 17 Mar 2025 22:01:11 GMT
ARG RELEASE
# Mon, 17 Mar 2025 22:01:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 17 Mar 2025 22:01:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 17 Mar 2025 22:01:11 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 17 Mar 2025 22:01:11 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 17 Mar 2025 22:01:11 GMT
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bd9e9ce4dca5ece369a2a4a59e15e188b21ab09a7a0a9bbf01f926a1df3f0b`  
		Last Modified: Wed, 09 Apr 2025 01:20:17 GMT  
		Size: 1.8 KB (1777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a28d8e10e668292bb81a4850236a9dad0255b85b6daca2074f0fb3db948656d`  
		Last Modified: Wed, 09 Apr 2025 01:20:18 GMT  
		Size: 1.5 MB (1513314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1e910af53a6da6768ca49ec54f62b8dca525212c2a0ba17b750646cf5d1ec0`  
		Last Modified: Wed, 09 Apr 2025 01:20:18 GMT  
		Size: 1.1 MB (1095159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b08c165256e7f9b6ac5a4502f64f6fc50b4e9d3b7ef69e560bc204936fee981`  
		Last Modified: Wed, 09 Apr 2025 01:20:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564edad542d74710919ac7f63e73fd401bc887094605d6e80096a8ac5463df4`  
		Last Modified: Wed, 09 Apr 2025 01:20:18 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3183389c3113d1188cf4040f6294b6562ce8c1a72ad5b950818a32844b817841`  
		Last Modified: Wed, 09 Apr 2025 01:20:25 GMT  
		Size: 230.2 MB (230167699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901c3e814024c2e99ec46c6994c5bfcdbe430c080b4077f6ccd1c75b98c6630e`  
		Last Modified: Wed, 09 Apr 2025 01:20:19 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:5f8c46312033877f76ff96e5443097711cf6a1a8a3b5b4643968cb8d700a32a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3104539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3bcde2d7e7c0ea853bd338d05de2ac5c76f2ef37d1f4284c24cc8beee954851`

```dockerfile
```

-	Layers:
	-	`sha256:e3627c602ad7c3cd0c08a89d1ff69e0faa04c8f90adb385a7819155c0aaafeb7`  
		Last Modified: Wed, 09 Apr 2025 01:20:18 GMT  
		Size: 3.1 MB (3076548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f4129c447760576487e6774448927d9f8c716f7904f47a48f1c60c49fe357bf`  
		Last Modified: Wed, 09 Apr 2025 01:20:17 GMT  
		Size: 28.0 KB (27991 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:be5528d6f380309e950d9e1f7fe08801e7bfc89c30011abf2aa9652062657b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251254907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3290eadf0cc92b82baf66eb3d0d87a5ce9900833bb0ff22a75ede23fe08e6047`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 17 Mar 2025 22:01:11 GMT
ARG RELEASE
# Mon, 17 Mar 2025 22:01:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 17 Mar 2025 22:01:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 17 Mar 2025 22:01:11 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 17 Mar 2025 22:01:11 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 17 Mar 2025 22:01:11 GMT
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a9680ebf8757cf00f3f44c8e11741d6a6695b4d4fb9f8c47ba2f4efe41bb38`  
		Last Modified: Wed, 09 Apr 2025 08:36:13 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49f871ed9c366a03abbed08130f14a06a417b31c488a293fb737c96eb1ecc46`  
		Last Modified: Wed, 09 Apr 2025 08:36:13 GMT  
		Size: 1.5 MB (1481698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19cf80be8e2651edf60c815ec64b3f8ee55e18d0663547bb448224178088783`  
		Last Modified: Wed, 09 Apr 2025 08:37:25 GMT  
		Size: 1.0 MB (1027736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d688391fd1b059a159119d95f59e60b13a79e6b9cb9d7ea9ccce50a0a260733`  
		Last Modified: Wed, 09 Apr 2025 08:37:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fd445302aed743efa2e0bcc46ba37fe36d011858f05be1908ff192d0da3fe9`  
		Last Modified: Wed, 09 Apr 2025 08:37:25 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecc338ccb33a05f369c92b2885c02e50020f07304ec840709331b137299727a`  
		Last Modified: Wed, 09 Apr 2025 08:37:30 GMT  
		Size: 221.4 MB (221384084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca01894c65cca52cbe3785a3810b7c2623449449a5a006544584baa88a5d10c`  
		Last Modified: Wed, 09 Apr 2025 08:37:25 GMT  
		Size: 5.0 KB (4992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:ac69ee150f172fe83c44ff13f3dc1ac23478ff149951a0dad4d6cb13c7b0e721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3105061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac11ce8bf0dda3178605a1921b28a76940991f69b572babfe1b67cc0f98a162a`

```dockerfile
```

-	Layers:
	-	`sha256:49eca334754f64255b65dbea7c00d6a9b11985e25619d4c164542eb256b1678c`  
		Last Modified: Wed, 09 Apr 2025 08:37:25 GMT  
		Size: 3.1 MB (3076867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d91ed91cc5de67e898937647176690bf9b7e71e15ea5ca8c419b99f1a6a6268`  
		Last Modified: Wed, 09 Apr 2025 08:37:25 GMT  
		Size: 28.2 KB (28194 bytes)  
		MIME: application/vnd.in-toto+json
