## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:04464becc31590de7b48c4acd7858f7110954ebcf0e523f92c9b1b00dd63249e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:b07f6013fd6040dda097c311df838afb4e429205f8ef88ece7b2c3b91597fa8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246902005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d3045a3f29d0271b7ef35c949a18eb7bbfc8d4878824ecc1dca2226175c03c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Mon, 30 Sep 2024 22:28:39 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 30 Sep 2024 22:28:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Sep 2024 22:28:39 GMT
ENV GOSU_VERSION=1.17
# Mon, 30 Sep 2024 22:28:39 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 30 Sep 2024 22:28:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 30 Sep 2024 22:28:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 30 Sep 2024 22:28:39 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 30 Sep 2024 22:28:39 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 30 Sep 2024 22:28:39 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 30 Sep 2024 22:28:39 GMT
ENV MONGO_MAJOR=6.0
# Mon, 30 Sep 2024 22:28:39 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 30 Sep 2024 22:28:39 GMT
ENV MONGO_VERSION=6.0.18
# Mon, 30 Sep 2024 22:28:39 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 30 Sep 2024 22:28:39 GMT
VOLUME [/data/db /data/configdb]
# Mon, 30 Sep 2024 22:28:39 GMT
ENV HOME=/data/db
# Mon, 30 Sep 2024 22:28:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Sep 2024 22:28:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Sep 2024 22:28:39 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 30 Sep 2024 22:28:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1740f148d0bffc5b5a682126b46606d2e3f94abda15f5748afcad0a581ea8789`  
		Last Modified: Tue, 01 Oct 2024 01:03:34 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835e46d6ce3f4f0eb85d092dc864227df691710b6397c7e2188fcd5226de0642`  
		Last Modified: Tue, 01 Oct 2024 01:03:34 GMT  
		Size: 1.5 MB (1512782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9f932d1b6f421c8bcfed088932bacd68c359a484324548b7afa6753f31b017`  
		Last Modified: Tue, 01 Oct 2024 01:03:34 GMT  
		Size: 1.1 MB (1094616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d295afbeb0ecc850bcc3185603291c29cbdf004c3023f2ac41070ba8ca166bc`  
		Last Modified: Tue, 01 Oct 2024 01:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4676562d01d51ad7644e92e2f419d5b819a646958291161b814816a3995b7e17`  
		Last Modified: Tue, 01 Oct 2024 01:03:34 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc376cf7e59701561908a23689e32716c752a661ce936f97ca452f1eb1e562d`  
		Last Modified: Tue, 01 Oct 2024 01:03:38 GMT  
		Size: 214.8 MB (214751760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6134f948d8fb1d344eff79c266ad6bcc0d276f2b9131e8320fe2f9477cd0e1`  
		Last Modified: Tue, 01 Oct 2024 01:03:35 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:8e3393ab4b847d8f4c51580d162fb0594fa2f0f50de478c6e01d1b73ccdbecf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3061701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c6eff9b7cf0c03dd08748a004f314cf8f1028372d97990f8589beda777094d`

```dockerfile
```

-	Layers:
	-	`sha256:023dab71e7a7e53141defc39fe714a54513abf14af6c524693f8feb1cfa08481`  
		Last Modified: Tue, 01 Oct 2024 01:03:34 GMT  
		Size: 3.0 MB (3034650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af47065f62f9a8fef820f92124bbb8ce2bdf9fa87215bb46e21b4f944ff63a72`  
		Last Modified: Tue, 01 Oct 2024 01:03:34 GMT  
		Size: 27.1 KB (27051 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:b0808616c7894aa7c1717a408155f940abc9ba92bbe222df4a171187d9f3f6dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236933934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616a68f022d061a57f5484131211f92ab32aa32e04b2ecd40fe0464a2d7f5dfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Mon, 30 Sep 2024 22:28:39 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 30 Sep 2024 22:28:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Sep 2024 22:28:39 GMT
ENV GOSU_VERSION=1.17
# Mon, 30 Sep 2024 22:28:39 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 30 Sep 2024 22:28:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 30 Sep 2024 22:28:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 30 Sep 2024 22:28:39 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 30 Sep 2024 22:28:39 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 30 Sep 2024 22:28:39 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 30 Sep 2024 22:28:39 GMT
ENV MONGO_MAJOR=6.0
# Mon, 30 Sep 2024 22:28:39 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 30 Sep 2024 22:28:39 GMT
ENV MONGO_VERSION=6.0.18
# Mon, 30 Sep 2024 22:28:39 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 30 Sep 2024 22:28:39 GMT
VOLUME [/data/db /data/configdb]
# Mon, 30 Sep 2024 22:28:39 GMT
ENV HOME=/data/db
# Mon, 30 Sep 2024 22:28:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Sep 2024 22:28:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Sep 2024 22:28:39 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 30 Sep 2024 22:28:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d432f7e11fc48086f6b23b461b4268a559c6a802b1326ca3e5c5647993d6e1`  
		Last Modified: Tue, 17 Sep 2024 02:33:38 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef31e5dc901efbe6078de6e56ff381ffa14fd1001fd17df4de4e60c30d86891`  
		Last Modified: Tue, 17 Sep 2024 02:33:39 GMT  
		Size: 1.5 MB (1465829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accf5d079e876461d067e426223084cf360a38b57f83aa6b6b974ecd24672fa3`  
		Last Modified: Tue, 01 Oct 2024 01:08:42 GMT  
		Size: 1.0 MB (1027416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6852cf5d1131a7d2aec57cf7adc33c2b1822d9f475303e80d21b55277ca872ba`  
		Last Modified: Tue, 01 Oct 2024 01:08:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bac671815c44a737f5ec58156de65dd51b50f5655855b00e78644b6f98939d`  
		Last Modified: Tue, 01 Oct 2024 01:08:42 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83bb5f3895bfc14f031fea098bca6dd32d1176e2ac1e878cf321f724d7423f3`  
		Last Modified: Tue, 01 Oct 2024 01:08:48 GMT  
		Size: 207.1 MB (207075203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbe5020e953c8549ab0c9c9a748ef8cf59a6d798f6de75303cd4fc6109536eb`  
		Last Modified: Tue, 01 Oct 2024 01:08:43 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:03d17fe937eaa7767463513ddf88cf08997b68f48f32a48950a2e0faf933d732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a3357da94e21652c26c506c77dde6a5280eca96bfcab291624cbd523f6e6cf`

```dockerfile
```

-	Layers:
	-	`sha256:40432e0a4b6f12760dae752d71aea411ff94b60824320c7534c970d3b3ede95b`  
		Last Modified: Tue, 01 Oct 2024 01:08:42 GMT  
		Size: 3.0 MB (3029078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b46156165c8c93f58b1b88f7bda4d4ff28ba96a8a7b0e0621a62ce233f442a4c`  
		Last Modified: Tue, 01 Oct 2024 01:08:42 GMT  
		Size: 27.2 KB (27248 bytes)  
		MIME: application/vnd.in-toto+json
