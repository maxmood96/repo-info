## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:e4a9a8e125578970a1f327a943053284a8d417fc30bc6d4cafe24ed2daad1821
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:c53da4bbbdfa5db09e94e90b55ebe752f2655c74ca765969378da5f13d1800aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249870422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba573339425152eaca413ff1a519446adc01426e1983e8dceefac2203f65d92f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 29 Feb 2024 23:30:03 GMT
ARG RELEASE
# Thu, 29 Feb 2024 23:30:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 23:30:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 23:30:03 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 23:30:03 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Thu, 29 Feb 2024 23:30:03 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 23:30:03 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
ENV GOSU_VERSION=1.17
# Thu, 29 Feb 2024 23:30:03 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 29 Feb 2024 23:30:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 29 Feb 2024 23:30:03 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:30:03 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:30:03 GMT
ENV MONGO_MAJOR=6.0
# Thu, 29 Feb 2024 23:30:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
ENV MONGO_VERSION=6.0.14
# Thu, 29 Feb 2024 23:30:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
VOLUME [/data/db /data/configdb]
# Thu, 29 Feb 2024 23:30:03 GMT
ENV HOME=/data/db
# Thu, 29 Feb 2024 23:30:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 23:30:03 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 29 Feb 2024 23:30:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3c645031de2917ade93ec54b118d5d3e45de72ef580b8f419a8cdc41e01d042c`  
		Last Modified: Wed, 10 Apr 2024 19:20:48 GMT  
		Size: 29.5 MB (29533419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be08a6ad8f73e40f7f7e86b5320c94f7d742d277591dc101d76be3de036a3e62`  
		Last Modified: Tue, 16 Apr 2024 04:26:33 GMT  
		Size: 1.8 KB (1779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028ec7404ae1c45f73f1c0f1dede5e86402c4476ceef7f5c8b26253d41c88883`  
		Last Modified: Tue, 16 Apr 2024 04:26:33 GMT  
		Size: 1.5 MB (1500733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de6a3840a1414fbe92dd1649ee9f96b4024278a7c1e6d3a49b626a881c2cdfc`  
		Last Modified: Tue, 16 Apr 2024 04:26:33 GMT  
		Size: 1.1 MB (1094559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfec3ae22f1edcfb838e051252f9fff4f0d7b09e9cc4a7b60023d8308eb3786`  
		Last Modified: Tue, 16 Apr 2024 04:26:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058091b083e50de7de7f38d71af49b492fba00ffe74f99448e5a35bf3df4e65e`  
		Last Modified: Tue, 16 Apr 2024 04:26:34 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35aa6c04412442663a2780572474e0e6c4f27b8b2390c1febed7b306b3d7f84`  
		Last Modified: Tue, 16 Apr 2024 04:26:38 GMT  
		Size: 217.7 MB (217734556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93830f5cc4d3a9ca78c6a7d173b2aae7788a56fc975cdff28320b42ce9548ba7`  
		Last Modified: Tue, 16 Apr 2024 04:26:34 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:b2ddc00c12e2b509bc6faca95e95c37fabd06d8b8f9a1609922054803fbefa67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3027627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f4ae2a70c1aee8e2a183f6533f4b2f1defea87d2d3a923eee5f9deb82a9e23`

```dockerfile
```

-	Layers:
	-	`sha256:a608465c2659a5c33512fbda286e47208321af3b840d7a42e51bd63186fe91b9`  
		Last Modified: Tue, 16 Apr 2024 04:26:33 GMT  
		Size: 3.0 MB (3000473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b28e2df836f1874530a05f89a77c9db8d64797298c8f7736467dea2c109472a5`  
		Last Modified: Tue, 16 Apr 2024 04:26:33 GMT  
		Size: 27.2 KB (27154 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:efcddf529c6903b11cef0b00d12e9feabd140f0b7805fd0369a2aec4a41956af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.7 MB (242693342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c455e298c235e9413dbc348eaec622cf956b27c8addad8c7ac739e8640df783d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 29 Feb 2024 23:30:03 GMT
ARG RELEASE
# Thu, 29 Feb 2024 23:30:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 Feb 2024 23:30:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 Feb 2024 23:30:03 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 29 Feb 2024 23:30:03 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Thu, 29 Feb 2024 23:30:03 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 23:30:03 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
ENV GOSU_VERSION=1.17
# Thu, 29 Feb 2024 23:30:03 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 29 Feb 2024 23:30:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 29 Feb 2024 23:30:03 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:30:03 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:30:03 GMT
ENV MONGO_MAJOR=6.0
# Thu, 29 Feb 2024 23:30:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
ENV MONGO_VERSION=6.0.14
# Thu, 29 Feb 2024 23:30:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
VOLUME [/data/db /data/configdb]
# Thu, 29 Feb 2024 23:30:03 GMT
ENV HOME=/data/db
# Thu, 29 Feb 2024 23:30:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 23:30:03 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 29 Feb 2024 23:30:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:70104cd59e2a443b9d9a13a6bce3bbf1ae78261c4198a40bf69d6e0515abe06a`  
		Last Modified: Wed, 10 Apr 2024 19:20:55 GMT  
		Size: 27.4 MB (27359551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7829398e6cec615872199f7d302253b64f2f90c209329783d7db2d99013a9c`  
		Last Modified: Tue, 16 Apr 2024 12:10:40 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645b7b6e30ae2933272d4495229ca7bb56b79fbc1005aa636c8957eb79a38e43`  
		Last Modified: Tue, 16 Apr 2024 12:10:40 GMT  
		Size: 1.5 MB (1466198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f48c0cb459b2794ae1aa8ef68dcea52e699cf446f13d3315833924bd0b2339b`  
		Last Modified: Tue, 16 Apr 2024 12:14:41 GMT  
		Size: 1.0 MB (1027756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3b5ebbf1f9b57a8970ddd81742a71019c1614f5fcec5fc1597fed2b4759371`  
		Last Modified: Tue, 16 Apr 2024 12:14:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ee9006ab51b3c479be5eabea00663a776a6b3728dfbaa4d593c6e8167dd300`  
		Last Modified: Tue, 16 Apr 2024 12:14:40 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d90cf2f43c0ae2a21e416ccfdc6ff136fabc3ed1e0aa88473c32d3a0493987`  
		Last Modified: Tue, 16 Apr 2024 12:14:45 GMT  
		Size: 212.8 MB (212832678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4726a6df8a6387c709530ac4d9a7074a45547033da6eaef03b32e2126a0cadd3`  
		Last Modified: Tue, 16 Apr 2024 12:14:42 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:44769d17550cdd5e5b438c3ea29adadaf947baab5e0063cbde79af71f4a2f68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3027733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadfc55a601c2f84cb1affda48db805cbfc0ed5ae26ec5f1fae2c7b2796a5966`

```dockerfile
```

-	Layers:
	-	`sha256:f2f028506425297aec8beee714afffb341956b53a3b996dbe504798775d1747f`  
		Last Modified: Tue, 16 Apr 2024 12:14:41 GMT  
		Size: 3.0 MB (3000726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f83eb07ce313083f4753ea67272afb2289770939b2a9a3d12a2583d69e1330a0`  
		Last Modified: Tue, 16 Apr 2024 12:14:40 GMT  
		Size: 27.0 KB (27007 bytes)  
		MIME: application/vnd.in-toto+json
