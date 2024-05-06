## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:443140356299c50205ba58d8dba73b22b29d582db4bdfb6c76cc97a68d194ef1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:28b702db9a9a8938cba7f9b646cd3b7843791a21a6c3ced0899b719d12f5c783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 MB (251684002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ffd9d39bd0f80aa63f58d2f4521e2e966d09b36258c00f99f3aa6fd3fd519f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 18 Apr 2024 10:01:32 GMT
ARG RELEASE
# Thu, 18 Apr 2024 10:01:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Apr 2024 10:01:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Apr 2024 10:01:32 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Apr 2024 10:01:32 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Thu, 18 Apr 2024 10:01:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Apr 2024 10:01:32 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 18 Apr 2024 10:01:32 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 18 Apr 2024 10:01:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 18 Apr 2024 10:01:32 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 18 Apr 2024 10:01:32 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 18 Apr 2024 10:01:32 GMT
ENV MONGO_MAJOR=6.0
# Thu, 18 Apr 2024 10:01:32 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
ENV MONGO_VERSION=6.0.15
# Thu, 18 Apr 2024 10:01:32 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
VOLUME [/data/db /data/configdb]
# Thu, 18 Apr 2024 10:01:32 GMT
ENV HOME=/data/db
# Thu, 18 Apr 2024 10:01:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Apr 2024 10:01:32 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 18 Apr 2024 10:01:32 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed08b1245dafbeff7a0c72a515ea02cc11c332d21d5801f99a1ab9c9c2fcfd7`  
		Last Modified: Thu, 02 May 2024 00:53:01 GMT  
		Size: 1.8 KB (1777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424e77ee1a6ddfe343bb356c9077cee0b41a29fb43f19fab07544117f6f1493e`  
		Last Modified: Thu, 02 May 2024 00:53:01 GMT  
		Size: 1.5 MB (1500680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5b3225781c22b4bf4149f6239793e040ee0d45b564ffc215588b63f46be9e0`  
		Last Modified: Thu, 02 May 2024 00:53:01 GMT  
		Size: 1.1 MB (1094552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df517147e11136e83dadce73e43b9288512a946487d4dbff49793a8e9e03352`  
		Last Modified: Thu, 02 May 2024 00:53:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d7ed74cba039af3a4d90d9ade7b0b0c20e1a62cb150f3062546450b524c54c`  
		Last Modified: Thu, 02 May 2024 00:53:02 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae88a75ed24ed90da80a361ac9d504d90d10c48f3b6d1e8cb32189d16354d44`  
		Last Modified: Thu, 02 May 2024 00:53:06 GMT  
		Size: 219.5 MB (219547670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4138c7eb3b7136898bd53240fef7e2c908abbda8e2034405bae73f64deaa3d88`  
		Last Modified: Thu, 02 May 2024 00:53:02 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:bf603bd998c4931ff2079152bf2a9ef7f1df9b4aa0b2720e543299de233ce8f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3027670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20341f2ca8248ec67e34934cd1bdcfc059fc9b3e564c20f404dddecd5320587f`

```dockerfile
```

-	Layers:
	-	`sha256:eebf51f97069203092415172758b0e181ebae18013e17393a1f067d50bc1fb05`  
		Last Modified: Thu, 02 May 2024 00:53:01 GMT  
		Size: 3.0 MB (3000513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c8325df876165c0e19addbe21dece2661c1b035f89f5cf284a20cb54755f3cf`  
		Last Modified: Thu, 02 May 2024 00:53:01 GMT  
		Size: 27.2 KB (27157 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:8383d20caa3f03a149030e3c751603e9365a255f027bdbd15a28c8c0fde7cb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244557239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346b42537c76d1a61a3b2ca418c8416d4e7a17dd02eaf38d4e9a00f6c3a78678`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 18 Apr 2024 10:01:32 GMT
ARG RELEASE
# Thu, 18 Apr 2024 10:01:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Apr 2024 10:01:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Apr 2024 10:01:32 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Apr 2024 10:01:32 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Thu, 18 Apr 2024 10:01:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Apr 2024 10:01:32 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 18 Apr 2024 10:01:32 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 18 Apr 2024 10:01:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 18 Apr 2024 10:01:32 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 18 Apr 2024 10:01:32 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 18 Apr 2024 10:01:32 GMT
ENV MONGO_MAJOR=6.0
# Thu, 18 Apr 2024 10:01:32 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
ENV MONGO_VERSION=6.0.15
# Thu, 18 Apr 2024 10:01:32 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
VOLUME [/data/db /data/configdb]
# Thu, 18 Apr 2024 10:01:32 GMT
ENV HOME=/data/db
# Thu, 18 Apr 2024 10:01:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Apr 2024 10:01:32 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 18 Apr 2024 10:01:32 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d5a2ad729c09fbfdb259ae764f92188efc67a615ffde9bb34a46298d1edf3cd6`  
		Last Modified: Sat, 27 Apr 2024 14:45:36 GMT  
		Size: 27.4 MB (27360530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8997f1f9f9006d728589447abdb1409fa9e5a099131cd4e1e64cd6a6aebc75a4`  
		Last Modified: Mon, 06 May 2024 16:53:50 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df3da78ba55adacc12f99125c8d02a8619ea246b5d158139419be8088a877bb`  
		Last Modified: Mon, 06 May 2024 16:53:50 GMT  
		Size: 1.5 MB (1466053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca276a62f6c588822e149eb4ba8338f8c1c0c627a382636aeb40ea9e215aac1`  
		Last Modified: Mon, 06 May 2024 16:54:14 GMT  
		Size: 1.0 MB (1027628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000c0c930b296f7a3fc0dac7b76eb5db6878df6973564218843d56d94577683e`  
		Last Modified: Mon, 06 May 2024 16:54:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542e58fb223fe9cb255877933c7df13f72c93e39db53c2c0d2187cb3bdb8e7ee`  
		Last Modified: Mon, 06 May 2024 16:54:14 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d231b487772ac3d11edf1da00221a4cafb521f290f255c7df1399cd64d8844c7`  
		Last Modified: Mon, 06 May 2024 16:54:19 GMT  
		Size: 214.7 MB (214695879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17530a96fbddeab4bc45996d4810418892ba9f13fcf9d9c8bf500c59be52df65`  
		Last Modified: Mon, 06 May 2024 16:54:15 GMT  
		Size: 5.0 KB (4989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:b69b0986343d34bb9f72fe7f2e34fa9fcec2ce613ce9c031703367680bac87f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3027777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2aa786171748db4ab2cc604e47088124b2fde757a279fbb18d7c7ab7d90cfe1`

```dockerfile
```

-	Layers:
	-	`sha256:90270b481a197059489a7736a9b2bad605f4d3e5d0857308d51bb82eb0bc4fae`  
		Last Modified: Mon, 06 May 2024 16:54:13 GMT  
		Size: 3.0 MB (3000766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0acf1f022473b3447f5176803712afb592ed30d522c3eeb189ed284102f99547`  
		Last Modified: Mon, 06 May 2024 16:54:13 GMT  
		Size: 27.0 KB (27011 bytes)  
		MIME: application/vnd.in-toto+json
