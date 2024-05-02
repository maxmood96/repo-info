## `mongo:5-focal`

```console
$ docker pull mongo@sha256:79feb790ccd1fc9976b302a062e2959f64493a068dcfef86d6bcd3dae3ddcc14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:5-focal` - linux; amd64

```console
$ docker pull mongo@sha256:cd86dfecb1f42e4cfaad2756957abe58ba3572285b72a0664c186af1bc331264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269378360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac681a3c37dafa9f2d0dc189244032e208857c15822723c856aa58c689a7cbf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 26 Mar 2024 22:01:21 GMT
ARG RELEASE
# Tue, 26 Mar 2024 22:01:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Mar 2024 22:01:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Mar 2024 22:01:21 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 26 Mar 2024 22:01:21 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Tue, 26 Mar 2024 22:01:21 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 22:01:21 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 22:01:21 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 26 Mar 2024 22:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-5.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 26 Mar 2024 22:01:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 26 Mar 2024 22:01:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 26 Mar 2024 22:01:21 GMT
ENV MONGO_MAJOR=5.0
# Tue, 26 Mar 2024 22:01:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ENV MONGO_VERSION=5.0.26
# Tue, 26 Mar 2024 22:01:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
VOLUME [/data/db /data/configdb]
# Tue, 26 Mar 2024 22:01:21 GMT
ENV HOME=/data/db
# Tue, 26 Mar 2024 22:01:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 22:01:21 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 26 Mar 2024 22:01:21 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51119b6d91b86725cc6a8a11fe0d442c374904000e644e868c61438c1aba57be`  
		Last Modified: Thu, 02 May 2024 00:53:25 GMT  
		Size: 1.8 KB (1778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3216e4814dedf5db505f5b2158388c7b3806d742cd991907ff75be740da0b1`  
		Last Modified: Thu, 02 May 2024 00:53:26 GMT  
		Size: 3.1 MB (3076354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef725b5efc9dd637e3fd48fef0ac03736af51f53e0cf1800dbfc2b42f29fa788`  
		Last Modified: Thu, 02 May 2024 00:53:26 GMT  
		Size: 1.1 MB (1091454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7890be636b0d7bf669882652b5849b4e30446e955a42e2e37e01d8f7b545a32a`  
		Last Modified: Thu, 02 May 2024 00:53:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9f5441f6e3b28336839d55d30d3796a64cd710225176f99916c518b6d20f85`  
		Last Modified: Thu, 02 May 2024 00:53:26 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df21be309c44ff35cb6df482b47027d2157b23152702d421e7ebf7879c7bade6`  
		Last Modified: Thu, 02 May 2024 00:53:32 GMT  
		Size: 237.7 MB (237691746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ad3b01c7881a2721ddd4531612d3406b1a63eab81b180ebc0d0627621aa84d`  
		Last Modified: Thu, 02 May 2024 00:53:27 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:f06ebeea4bf6bd6cf34e2732b0b9700dc3368d102aea52174eb99fa3b7986207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3026830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9d7b1c03715ad2aacc1e2ba5b44d7abb9ddff69eb0ad4aefd91ebb54c28504`

```dockerfile
```

-	Layers:
	-	`sha256:ffd9c71958186698acf4e3a7b1ea47d00f3337a79f707398581a2ca3e5d37edb`  
		Last Modified: Thu, 02 May 2024 00:53:26 GMT  
		Size: 3.0 MB (2999994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a30ecc308d374d0238c998e35ba1bf05492ed1effee40dfb188f4e93caefd0b7`  
		Last Modified: Thu, 02 May 2024 00:53:25 GMT  
		Size: 26.8 KB (26836 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:5-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:3b8efb009697356d68a30b91321b262c8faea5a5347590c4145a43f6e61cb27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.7 MB (261719202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94f3533ec439b8790f08493e2a519ecab1b35a7c8365909a64f20d094df1b8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 26 Mar 2024 22:01:21 GMT
ARG RELEASE
# Tue, 26 Mar 2024 22:01:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Mar 2024 22:01:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Mar 2024 22:01:21 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 26 Mar 2024 22:01:21 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Tue, 26 Mar 2024 22:01:21 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 22:01:21 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 22:01:21 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 26 Mar 2024 22:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-5.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 26 Mar 2024 22:01:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 26 Mar 2024 22:01:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 26 Mar 2024 22:01:21 GMT
ENV MONGO_MAJOR=5.0
# Tue, 26 Mar 2024 22:01:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ENV MONGO_VERSION=5.0.26
# Tue, 26 Mar 2024 22:01:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
VOLUME [/data/db /data/configdb]
# Tue, 26 Mar 2024 22:01:21 GMT
ENV HOME=/data/db
# Tue, 26 Mar 2024 22:01:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 22:01:21 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 26 Mar 2024 22:01:21 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d7044108e6d4d8b24ea68c7ee675f78cb56d959d0878b78c97e8ca7c6b5fa2cc`  
		Last Modified: Sat, 27 Apr 2024 14:55:02 GMT  
		Size: 26.0 MB (25975500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001b287048bd171c71db091a9a875d56c42a0df27302047ddc31d8fd21aaf6c6`  
		Last Modified: Thu, 02 May 2024 12:28:32 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dff8d23fd24b1d9bf65945df348665b3c662189fd1d17a4e13798d9e3ee6eb8`  
		Last Modified: Thu, 02 May 2024 12:28:33 GMT  
		Size: 2.9 MB (2930161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af1eaec1f0ecab67bdc0527369d3e66c23877de6cb0bd87bd46be662628a78d`  
		Last Modified: Thu, 02 May 2024 12:28:33 GMT  
		Size: 1.0 MB (1024273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2cd2b3e1adceaa08d508df73002ecd6813e77bd32a31e1b795e77cb3e54057`  
		Last Modified: Thu, 02 May 2024 12:28:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b280e1d5deee9d55aa41320d70cca887971147529c8789627bad9ce57c2f936c`  
		Last Modified: Thu, 02 May 2024 12:28:34 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585e2af471f37b1795ae4f576b5a0399b276861cf6d87aab565a9c3d7e972f82`  
		Last Modified: Thu, 02 May 2024 12:28:40 GMT  
		Size: 231.8 MB (231782116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf6efc3f127f0a77453e7ba13bace955a8eb0f8aec4cb56747b4b910a31dba2`  
		Last Modified: Thu, 02 May 2024 12:28:34 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:8e64f5f03e5054382016953f400c808dda95dfdc4d210937adb78e95b47295e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3026916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5690b5d33c1d662f01875f5cacf0bab731f9eaa698c8a38f889f203907bb2637`

```dockerfile
```

-	Layers:
	-	`sha256:6b12c044269bc1134302a082ffdee7737f39126f97078b5a5f7d6068375acad3`  
		Last Modified: Thu, 02 May 2024 12:28:33 GMT  
		Size: 3.0 MB (3000227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad1d27dd944bfc3123de9c0cef20a08b1e9ad18727e5e0904a7d56c7f772c241`  
		Last Modified: Thu, 02 May 2024 12:28:32 GMT  
		Size: 26.7 KB (26689 bytes)  
		MIME: application/vnd.in-toto+json
