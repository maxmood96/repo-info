## `mongo:noble`

```console
$ docker pull mongo@sha256:086f90faa9c3c65c6f06d0f7b757460ece878754b35fc7d53d15abab4328815d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:noble` - linux; amd64

```console
$ docker pull mongo@sha256:25c45597712d8f37915a52a172ce927ab197bcb764e81364df4c492083a20154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.4 MB (274360930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3f01eba940177a289878d5d4931e9fc67c63a4774c7e96e0096bb6c8fe3717`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
CMD ["/bin/bash"]
# Fri, 25 Oct 2024 04:15:38 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
ENV GOSU_VERSION=1.17
# Fri, 25 Oct 2024 04:15:38 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 25 Oct 2024 04:15:38 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 25 Oct 2024 04:15:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 25 Oct 2024 04:15:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 25 Oct 2024 04:15:38 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 25 Oct 2024 04:15:38 GMT
ENV MONGO_MAJOR=8.0
# Fri, 25 Oct 2024 04:15:38 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
ENV MONGO_VERSION=8.0.3
# Fri, 25 Oct 2024 04:15:38 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
VOLUME [/data/db /data/configdb]
# Fri, 25 Oct 2024 04:15:38 GMT
ENV HOME=/data/db
# Fri, 25 Oct 2024 04:15:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Oct 2024 04:15:38 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 25 Oct 2024 04:15:38 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab913c649fa1abe49187fd324d1e01ac31c34fe6b091687b49c9b10a8dbb847`  
		Last Modified: Sat, 16 Nov 2024 02:57:27 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142bff30356fe103c719b4870aba78b32cac6f290fa0352accae4eb8656c9749`  
		Last Modified: Sat, 16 Nov 2024 02:57:28 GMT  
		Size: 1.5 MB (1507380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6a78a8bfa5bc592320d2600fd10f6d4e1b13e1023a67d362db5fcb4c14fb41`  
		Last Modified: Sat, 16 Nov 2024 02:57:28 GMT  
		Size: 1.1 MB (1129796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87de320d14acc0fcf483ef571d08deecd480af08e6fd5a66b04d8d7544d06db`  
		Last Modified: Sat, 16 Nov 2024 02:57:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fb995504bd758c5e984546fc4e41ce5cf373252e61c154ad9afcce70ff4f7b`  
		Last Modified: Sat, 16 Nov 2024 02:57:28 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbe36f78898ca9da9ceba79b5d8ecf70c8bdde17afadc3e94a1c2021e789859`  
		Last Modified: Sat, 16 Nov 2024 02:57:32 GMT  
		Size: 242.0 MB (241965380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f774f57f04f52c7a406825ce474d3ff82d8580dc0f15c5b66fe6c7492027776`  
		Last Modified: Sat, 16 Nov 2024 02:57:28 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:4e0c92fe7ce70abfcd2914bf0b5f666cc503414c8d0f02650ea0a1c20faefaf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2526389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c0ce27a89310c259fb1c63e3e4912782234725896829d631ce2013608305da`

```dockerfile
```

-	Layers:
	-	`sha256:ba5904b7138738dd9c1ca4066f4694ac62139f6e82228760f60aae368ed1ccbb`  
		Last Modified: Sat, 16 Nov 2024 02:57:27 GMT  
		Size: 2.5 MB (2497817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab6e464220673bfbab8eb49eb725248c0d4258c6a0b3878aa3e7bab008b9ac8`  
		Last Modified: Sat, 16 Nov 2024 02:57:27 GMT  
		Size: 28.6 KB (28572 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:61465063ea9cd9cd2b3de970ebd77dcce82d7998aadfef43863264da58c42c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263472048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c53a547a74ef5eb3b3e637c5a2a016710b2a21a8ae1ad0b4bf4d8ae585e323`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Fri, 25 Oct 2024 04:15:38 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
ENV GOSU_VERSION=1.17
# Fri, 25 Oct 2024 04:15:38 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 25 Oct 2024 04:15:38 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 25 Oct 2024 04:15:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 25 Oct 2024 04:15:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 25 Oct 2024 04:15:38 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 25 Oct 2024 04:15:38 GMT
ENV MONGO_MAJOR=8.0
# Fri, 25 Oct 2024 04:15:38 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
ENV MONGO_VERSION=8.0.3
# Fri, 25 Oct 2024 04:15:38 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
VOLUME [/data/db /data/configdb]
# Fri, 25 Oct 2024 04:15:38 GMT
ENV HOME=/data/db
# Fri, 25 Oct 2024 04:15:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Oct 2024 04:15:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Oct 2024 04:15:38 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 25 Oct 2024 04:15:38 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6af9b7b3e8647aeef7d147457ff9cef1d2b078c486a79f5236f88a75d94d6c2`  
		Last Modified: Sat, 16 Nov 2024 03:18:28 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99a34a965cbc55e3242f0e53458eab7213bac95c19156de915c7c81640c3018`  
		Last Modified: Sat, 16 Nov 2024 03:18:29 GMT  
		Size: 1.5 MB (1491511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf83cf22909f3406c792e834d64d783be9bd780004dec141885b8e03f515688`  
		Last Modified: Sat, 16 Nov 2024 03:18:29 GMT  
		Size: 1.1 MB (1059951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf24ef7e4830915a00010b92679449280edb73ed60c186dd1c7ccbf76ed39b07`  
		Last Modified: Sat, 16 Nov 2024 03:18:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbeb3fddb7cc99898ba9dfe9a6a521fe15ec642d5afd194a85e85fbd8188ae0`  
		Last Modified: Sat, 16 Nov 2024 03:18:29 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eebf45717497300c9f46c2054816b40b2927dae0b77541263e9bf2645173055`  
		Last Modified: Sat, 16 Nov 2024 03:18:35 GMT  
		Size: 232.0 MB (232021570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44034023f7c5e18518a15a7e3d7fa85bb39db62f0b930307364c91c4825e5d26`  
		Last Modified: Sat, 16 Nov 2024 03:18:30 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:5a26842d6e1fa888826446435432ea8cde9219d235c071052052641324ae5dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2527752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb0984a63e2c3db787a0b6f0f09b80efcf16d3897ff2953b9bc8d8f4a29eb8f`

```dockerfile
```

-	Layers:
	-	`sha256:50d3325072dada299e285f62e5fb6065b367c66baa1cdfec6d85f30f67ebaf95`  
		Last Modified: Sat, 16 Nov 2024 03:18:29 GMT  
		Size: 2.5 MB (2498953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc62954e3218e0782a4ae0c671ad47829156eeb0c3c7f082c6b8dd071e8afdf`  
		Last Modified: Sat, 16 Nov 2024 03:18:28 GMT  
		Size: 28.8 KB (28799 bytes)  
		MIME: application/vnd.in-toto+json
