## `mongo:jammy`

```console
$ docker pull mongo@sha256:bed1f0e3d69c8b8137b9a28ac185743c6c3552e1025b946d700e332ffe69afea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:jammy` - linux; amd64

```console
$ docker pull mongo@sha256:b4e6a91ba7665456eef62213aa4bb51d3c9cc1209072910e87a48b72c28d02de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262510616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3902e4c1fa5c51eb16684a09feb755432151c03003bd804ce0caf27f2e4cb50c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 03 Apr 2024 16:02:10 GMT
ARG RELEASE
# Wed, 03 Apr 2024 16:02:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 03 Apr 2024 16:02:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 03 Apr 2024 16:02:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 03 Apr 2024 16:02:10 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 03 Apr 2024 16:02:10 GMT
CMD ["/bin/bash"]
# Wed, 03 Apr 2024 16:02:10 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Apr 2024 16:02:10 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 03 Apr 2024 16:02:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 03 Apr 2024 16:02:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 03 Apr 2024 16:02:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 03 Apr 2024 16:02:10 GMT
ENV MONGO_MAJOR=7.0
# Wed, 03 Apr 2024 16:02:10 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ENV MONGO_VERSION=7.0.8
# Wed, 03 Apr 2024 16:02:10 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
VOLUME [/data/db /data/configdb]
# Wed, 03 Apr 2024 16:02:10 GMT
ENV HOME=/data/db
# Wed, 03 Apr 2024 16:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Apr 2024 16:02:10 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 03 Apr 2024 16:02:10 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3c645031de2917ade93ec54b118d5d3e45de72ef580b8f419a8cdc41e01d042c`  
		Last Modified: Wed, 10 Apr 2024 19:20:48 GMT  
		Size: 29.5 MB (29533419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa196f67a922d387266e3fc925d24cf929d514e6eb7cf9a5f76817691b4ab5a`  
		Last Modified: Tue, 16 Apr 2024 04:26:26 GMT  
		Size: 1.8 KB (1778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb794c1d8eba6b1dada168d8d18da6701c9b668a90e55ca6c21856e7012388a`  
		Last Modified: Tue, 16 Apr 2024 04:26:26 GMT  
		Size: 1.5 MB (1500751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a415fad0b1a4cc355f24e9776045892c92509eeb431f18ac2eae51c758d8c5d`  
		Last Modified: Tue, 16 Apr 2024 04:26:26 GMT  
		Size: 1.1 MB (1094567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0ca0d8db42f00e61f1e845478d55b759b78b4b418c844adf0b43144499d1b2`  
		Last Modified: Tue, 16 Apr 2024 04:26:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7341c0351e263c04e370b346faa2accb08e377de04cdfeea9d4dd47829f17899`  
		Last Modified: Tue, 16 Apr 2024 04:26:27 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11062490c406b34474a8daacf31af15a897a321856c2db5916de5b96179a09e5`  
		Last Modified: Tue, 16 Apr 2024 04:26:31 GMT  
		Size: 230.4 MB (230374727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e953fad04d180faa2a238fecef4a5ddcc0470a11a6a66b3aeecfeddec69faab4`  
		Last Modified: Tue, 16 Apr 2024 04:26:27 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:c29dfe83a0e8db72fdac156bfdbfd368f0dbd8b96d137102895b607e663d0d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3028779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddafdb281f03d426ef31f454a6c9d3dd7300f5aa767da2633b9ebde9c82fecb4`

```dockerfile
```

-	Layers:
	-	`sha256:4cd927dff7b576c1cdf3409828eb9b78b7c23fdb2d127abaf95973e5d03b9d97`  
		Last Modified: Tue, 16 Apr 2024 04:26:26 GMT  
		Size: 3.0 MB (3001045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cecc9c6d7acb8a7dc13b3c24820141a7e0fbfda059990c0789eb7e3b449fa773`  
		Last Modified: Tue, 16 Apr 2024 04:26:26 GMT  
		Size: 27.7 KB (27734 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:d21bcd02f2c5f50b862436ebb55c8c07f1782b4e6cb909ba87b0dbee72293217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (254038304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372eb238b2a053d7bd28d06b67544050d4bd99a8a5f29553e8bc4547472c1039`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Wed, 03 Apr 2024 16:02:10 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Apr 2024 16:02:10 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 03 Apr 2024 16:02:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 03 Apr 2024 16:02:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 03 Apr 2024 16:02:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 03 Apr 2024 16:02:10 GMT
ENV MONGO_MAJOR=7.0
# Wed, 03 Apr 2024 16:02:10 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ENV MONGO_VERSION=7.0.8
# Wed, 03 Apr 2024 16:02:10 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
VOLUME [/data/db /data/configdb]
# Wed, 03 Apr 2024 16:02:10 GMT
ENV HOME=/data/db
# Wed, 03 Apr 2024 16:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Apr 2024 16:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Apr 2024 16:02:10 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 03 Apr 2024 16:02:10 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f4bb4e8dca02be491b4f72d2ef2127a64ce49c48d0d9c0a0fcaffa625067679d`  
		Last Modified: Tue, 27 Feb 2024 19:00:12 GMT  
		Size: 27.4 MB (27358724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52b73deb9edc3115af86e72d5e6b01b7580448fe8f2bad37252f1c6d6e47fab`  
		Last Modified: Tue, 19 Mar 2024 23:51:02 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d310f328ae06be202e6c074df5e8ccf467ef34a7167b47f0d408d0ea70b6a44`  
		Last Modified: Tue, 19 Mar 2024 23:51:03 GMT  
		Size: 1.5 MB (1465416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6688fa40c23ff36e90f3fc306fbd3b7a6c9ab594bef76fd7b2a7b95b73202df`  
		Last Modified: Tue, 19 Mar 2024 23:51:03 GMT  
		Size: 1.0 MB (1026959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed5465e8998f674efa29cb64907336cd6669dc7c8468953e3d2b59cabf59a7e`  
		Last Modified: Tue, 19 Mar 2024 23:51:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaefe376ac3e126cd19d0b24976dcceb6f13ce301e1ed1029a293f44152c5983`  
		Last Modified: Tue, 19 Mar 2024 23:51:04 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd67cbaf0950c8a8192b42f1d3bad362b58d0fac767e58bae988f0cf0a62368`  
		Last Modified: Wed, 03 Apr 2024 20:59:46 GMT  
		Size: 224.2 MB (224180046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dbc7944e9af83852ad093fce6890e0574eca59af4f7ad7ddab55f723fa361a`  
		Last Modified: Wed, 03 Apr 2024 20:59:40 GMT  
		Size: 5.0 KB (4992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:1c1a761dbab4cbeb7c7dbae9752fc02ddb9e557648a08bbe692a35717300927b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3028862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1235223d2819f4775b0f2f285bc77019fb91557fe0917e1d77e0db0b08e7d7`

```dockerfile
```

-	Layers:
	-	`sha256:9e71c61c72eacebc24f2bb170cb9c0081afa1c4f6c75c5d2329ca9df5683030c`  
		Last Modified: Wed, 03 Apr 2024 20:59:41 GMT  
		Size: 3.0 MB (3001270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18dd4f1f79ae2953f56a4c5469da97744f4feddcba8693fc39d4fd9bd08f7205`  
		Last Modified: Wed, 03 Apr 2024 20:59:40 GMT  
		Size: 27.6 KB (27592 bytes)  
		MIME: application/vnd.in-toto+json
