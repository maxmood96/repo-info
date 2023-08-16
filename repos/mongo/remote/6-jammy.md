## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:4f8925a292842796e2fcb7696b17363687ebabba02c8880e8d9d2844128b3a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:cb49c21879557f7805df8a50a4a315412461649eab2a2ad28ad2e240eb68c761
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237543054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9e08095631faef5dc9e898411067cb73002046e5f882151619ac7519a82ec2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 18:35:44 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 04 Jul 2023 18:35:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 18:35:58 GMT
ENV GOSU_VERSION=1.16
# Tue, 04 Jul 2023 18:35:58 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 04 Jul 2023 18:36:05 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Jul 2023 18:36:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Jul 2023 18:37:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 04 Jul 2023 18:37:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 04 Jul 2023 18:37:12 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 04 Jul 2023 18:37:12 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 04 Jul 2023 18:37:12 GMT
ENV MONGO_MAJOR=6.0
# Tue, 04 Jul 2023 18:37:13 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 15 Aug 2023 23:35:09 GMT
ENV MONGO_VERSION=6.0.9
# Tue, 15 Aug 2023 23:35:31 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 15 Aug 2023 23:35:31 GMT
VOLUME [/data/db /data/configdb]
# Tue, 15 Aug 2023 23:35:31 GMT
ENV HOME=/data/db
# Tue, 15 Aug 2023 23:35:31 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Tue, 15 Aug 2023 23:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Aug 2023 23:35:32 GMT
EXPOSE 27017
# Tue, 15 Aug 2023 23:35:32 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c1327991fa5c5486760d982d77d664b70b2e706b8f8869990798786fb4c9f1`  
		Last Modified: Tue, 04 Jul 2023 18:40:25 GMT  
		Size: 1.8 KB (1830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1feec59ecd14b079156c7fd92342b9106a9f5648ab04d8dfa0aea0751266fc0c`  
		Last Modified: Tue, 04 Jul 2023 18:40:26 GMT  
		Size: 5.1 MB (5050536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af7480eaf553461e3f6a793fc4fe4777f8616f6a84bbaeaa9ff2d1c3f71f76a`  
		Last Modified: Tue, 04 Jul 2023 18:40:26 GMT  
		Size: 1.3 MB (1253028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7524ee16ced6fa4a128f589dd138410a33c974f34e036ae8c1723f3a8532fba`  
		Last Modified: Tue, 04 Jul 2023 18:40:25 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4742175eefcaeaaa59e55371c0a663e862c656a98b2c066b03cb553fa41f676`  
		Last Modified: Tue, 04 Jul 2023 18:41:29 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d688a8d9c18df4dcf5f10af235bc26cd7ff1a9eea9fa7dd8ec784893ba649ad`  
		Last Modified: Tue, 04 Jul 2023 18:41:29 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8600b649c8a77619483e3ccf84f5a944d5e07df89b2f223af5244689378fbe1a`  
		Last Modified: Tue, 15 Aug 2023 23:37:07 GMT  
		Size: 200.8 MB (200799597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a536bb8a5ad74b3acfa305bb2011c31763af2e4ef7837966ac0635522890b3`  
		Last Modified: Tue, 15 Aug 2023 23:36:40 GMT  
		Size: 5.0 KB (5000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:edaa57a92bff882392d8b49ab02d30644e30080082572ea44a1207d3ab1a4670
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231090179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072d346b207a3ebc6d84ae2f513eea5592d71107b0560031a7eccd3a3a0d3a50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 14:49:29 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 16 Aug 2023 14:49:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 14:49:38 GMT
ENV GOSU_VERSION=1.16
# Wed, 16 Aug 2023 14:49:38 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 16 Aug 2023 14:49:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 16 Aug 2023 14:49:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 16 Aug 2023 14:49:46 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '39BD841E4BE5FB195A65400E6A26B1AE64C3C388'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 16 Aug 2023 14:49:46 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 16 Aug 2023 14:49:46 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 16 Aug 2023 14:49:46 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 16 Aug 2023 14:49:46 GMT
ENV MONGO_MAJOR=6.0
# Wed, 16 Aug 2023 14:49:47 GMT
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 16 Aug 2023 14:49:47 GMT
ENV MONGO_VERSION=6.0.9
# Wed, 16 Aug 2023 14:50:04 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 16 Aug 2023 14:50:08 GMT
VOLUME [/data/db /data/configdb]
# Wed, 16 Aug 2023 14:50:08 GMT
ENV HOME=/data/db
# Wed, 16 Aug 2023 14:50:08 GMT
COPY file:8fc8efb4e3db886ece2de8764459b4ab3e639e636ed08b2e828441229b4f8571 in /usr/local/bin/ 
# Wed, 16 Aug 2023 14:50:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Aug 2023 14:50:08 GMT
EXPOSE 27017
# Wed, 16 Aug 2023 14:50:08 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303f1ca3efb97b175995e3f2e70c6a646e0e27d9b6ad5b6bb83385a069aad6d9`  
		Last Modified: Wed, 16 Aug 2023 14:50:39 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b0a2b71cfcf9fba9591e46268b319c8cf749fd1bbb23ca5a71b4c23a5c3ccf`  
		Last Modified: Wed, 16 Aug 2023 14:50:40 GMT  
		Size: 5.0 MB (4993945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07c969b361c9e4836e4f5bf5402920e857a21a92435e238f48043b870b3f107`  
		Last Modified: Wed, 16 Aug 2023 14:50:40 GMT  
		Size: 1.2 MB (1186400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333b867e6b438067ef26466f5e86818da58b7350dd63f755cd24f805194878df`  
		Last Modified: Wed, 16 Aug 2023 14:50:37 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cc89b5f3ad374b1fbdd3e74db2b73ba233605e600460277591439cff6271ea`  
		Last Modified: Wed, 16 Aug 2023 14:50:37 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c316c86750379453dd785f4ab81ec93c059e069491557b8b89aa3a4ddfbe2eeb`  
		Last Modified: Wed, 16 Aug 2023 14:50:37 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b172a0dcff2beae3ddbb0899bf47b42dde234f5f4c82b6667fbc6b1d368e611`  
		Last Modified: Wed, 16 Aug 2023 14:50:55 GMT  
		Size: 196.5 MB (196509253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd757bc2c08ae6c22ecb3ea1c3f12259e9123725cf26995bde832d174681290`  
		Last Modified: Wed, 16 Aug 2023 14:50:37 GMT  
		Size: 5.0 KB (4994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
