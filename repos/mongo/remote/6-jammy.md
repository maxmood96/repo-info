## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:7ea7478a6aff3eb7c651df7fac1b1450680d6ad03747dfc63ebc1136682057d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:01ac386c1c55e0f26ae1a516383baac2f29937eefe4b6276f8def33d4016e6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.7 MB (245681785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2af2fc1fab9821704350a989d6c1a6ed12400b3dd72acc3d9362c7b6aa4011`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 07 Feb 2024 00:59:03 GMT
ARG RELEASE
# Wed, 07 Feb 2024 00:59:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Feb 2024 00:59:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Feb 2024 00:59:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 07 Feb 2024 00:59:03 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Wed, 07 Feb 2024 00:59:03 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 00:59:03 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENV GOSU_VERSION=1.17
# Wed, 07 Feb 2024 00:59:03 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 07 Feb 2024 00:59:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 07 Feb 2024 00:59:03 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_MAJOR=6.0
# Wed, 07 Feb 2024 00:59:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_VERSION=6.0.13
# Wed, 07 Feb 2024 00:59:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
VOLUME [/data/db /data/configdb]
# Wed, 07 Feb 2024 00:59:03 GMT
ENV HOME=/data/db
# Wed, 07 Feb 2024 00:59:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Feb 2024 00:59:03 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 07 Feb 2024 00:59:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:01007420e9b005dc14a8c8b0f996a2ad8e0d4af6c3d01e62f123be14fe48eec7`  
		Last Modified: Tue, 13 Feb 2024 10:22:22 GMT  
		Size: 29.5 MB (29536188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ca97e2c46744df517d23a76ede0e93207293fd2a9c3c6b52143793e6c91a62`  
		Last Modified: Fri, 16 Feb 2024 01:50:30 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd242b4fa75fbca86a20176548fe13200198bc0ad8b671aaf12a16063afc0982`  
		Last Modified: Fri, 16 Feb 2024 01:50:30 GMT  
		Size: 1.5 MB (1500368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9608f6bb829c7442172994785e577f1873b87bc88cb38a1007048cb4ced71f9`  
		Last Modified: Fri, 16 Feb 2024 01:50:30 GMT  
		Size: 1.1 MB (1094198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb180c9e7b566cbbc5a149b35730ede7ba88af41fa4ea4e720fc8e94e827268`  
		Last Modified: Fri, 16 Feb 2024 01:50:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fe9b1d0ed3c92100c6d0d098167fedc53f7b2252312c45150699119b4ce0a2`  
		Last Modified: Fri, 16 Feb 2024 01:50:31 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d50a4b3eea6135b9a13609719e24a5cc3f2b6bf83fa00fbc733478f66b13eee`  
		Last Modified: Fri, 16 Feb 2024 01:50:34 GMT  
		Size: 213.5 MB (213543873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f2ecffbdb8bc0221c09a625af36ee86809d91663e933c886a491f1150e5877`  
		Last Modified: Fri, 16 Feb 2024 01:50:31 GMT  
		Size: 5.0 KB (4998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:a4dc68f98d7904829545ec4d853a953682a6adc51a35163eb25be96f160a5195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2639865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be74d46a203f82528ee28ed45bcd0cf25238e1d6ed1cd352bf41de610df9a597`

```dockerfile
```

-	Layers:
	-	`sha256:680aef0e221ba176cabf73c4fbd00d660ce77913ef4b427fe77102725fa863fc`  
		Last Modified: Fri, 16 Feb 2024 01:50:30 GMT  
		Size: 2.6 MB (2612711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae46a89e7116e9169a5274db009b2f86cc46ff1f44410cbc758555f752aea15c`  
		Last Modified: Fri, 16 Feb 2024 01:50:30 GMT  
		Size: 27.2 KB (27154 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:ba69f4aba491d2a4e423a18617e5287752a2b10e1c69d7d5d73a9633b5a533d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.6 MB (238569771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0129276f779a3ebd089b2c0f4dce56ee33fd0af07bc8d529ce2b215599bfe986`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 07 Feb 2024 00:59:03 GMT
ARG RELEASE
# Wed, 07 Feb 2024 00:59:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Feb 2024 00:59:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Feb 2024 00:59:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 07 Feb 2024 00:59:03 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Wed, 07 Feb 2024 00:59:03 GMT
CMD ["/bin/bash"]
# Wed, 07 Feb 2024 00:59:03 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENV GOSU_VERSION=1.17
# Wed, 07 Feb 2024 00:59:03 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 07 Feb 2024 00:59:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 07 Feb 2024 00:59:03 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_MAJOR=6.0
# Wed, 07 Feb 2024 00:59:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENV MONGO_VERSION=6.0.13
# Wed, 07 Feb 2024 00:59:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
VOLUME [/data/db /data/configdb]
# Wed, 07 Feb 2024 00:59:03 GMT
ENV HOME=/data/db
# Wed, 07 Feb 2024 00:59:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 Feb 2024 00:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Feb 2024 00:59:03 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 07 Feb 2024 00:59:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a4a2c7a57ed8b997579870d0927433b03cfd94f5dba2153bdbcd885b5d620035`  
		Last Modified: Tue, 13 Feb 2024 10:22:28 GMT  
		Size: 27.4 MB (27356877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1354176b189db5e882e8695cd36475579099a8312ad5731dd9c9365249630636`  
		Last Modified: Fri, 16 Feb 2024 19:01:34 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a94d566154f568d8d3806d6f82aeec09ecd0408a9db227eceeb6849c9ead90`  
		Last Modified: Fri, 16 Feb 2024 19:01:34 GMT  
		Size: 1.5 MB (1465222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832ca3cde8a70d1e9094ba7a1fa270ccf4f19f988a7433817acdc276c47569f7`  
		Last Modified: Fri, 16 Feb 2024 19:01:58 GMT  
		Size: 1.0 MB (1026761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6c95269521ca0fca0ec1780673cb30b25e908bffe4a21d5572c47a0e51eac5`  
		Last Modified: Fri, 16 Feb 2024 19:01:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d1506690d249600ade5083575fdc073240f694c5fc5833bec25481aa546953`  
		Last Modified: Fri, 16 Feb 2024 19:01:58 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af841cb5ea6c8a3dc217f938e8ed6d40d8a08694ae28b403c7eb58ff3d655d9b`  
		Last Modified: Fri, 16 Feb 2024 19:02:03 GMT  
		Size: 208.7 MB (208713747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09031fe34eae12cf13c250ff22a91f081a459d95e5a817da1535f7edb7bcc21a`  
		Last Modified: Fri, 16 Feb 2024 19:01:59 GMT  
		Size: 5.0 KB (4999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:a9f57d34793acb24588842a7652a87b621d3664c9f79875be7cc4868e507e494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2640077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd7daa029631ac23946e36d72429ed84774577a17b842b5f1a6363d654cb71ae`

```dockerfile
```

-	Layers:
	-	`sha256:5b5c292e20bb32113dfcacea3c4ad16b9d4483bcd1cf38765dfd1f486d635657`  
		Last Modified: Fri, 16 Feb 2024 19:01:58 GMT  
		Size: 2.6 MB (2613070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2998b5dffb6ca85a5077ce688b657b60096a624a191f27b164dfec299e82e0d`  
		Last Modified: Fri, 16 Feb 2024 19:01:58 GMT  
		Size: 27.0 KB (27007 bytes)  
		MIME: application/vnd.in-toto+json
