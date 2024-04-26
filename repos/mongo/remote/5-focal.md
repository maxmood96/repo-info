## `mongo:5-focal`

```console
$ docker pull mongo@sha256:26e0a01e9a0342932edf24794847d4b2e6ae33e6b8277afec6ac1f68110475a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:5-focal` - linux; amd64

```console
$ docker pull mongo@sha256:3f9311a738817f4fe67bb8f47590774b5fa0fd78061f9d091d47de5e16b93b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269378143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787e6dffe515a24f0566322a421a3314b6fc0370f2707c87e33c063a28216f06`
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
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
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
	-	`sha256:4477f8fe99ebfd23fa06d28a2fa42eaa05d726926afc0a055e1ff2b612b7a293`  
		Last Modified: Wed, 17 Apr 2024 18:54:17 GMT  
		Size: 27.5 MB (27511740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff81671fc34d83fb47a232aa09df2ade21ff0d894ef8d0333c7a9050ff4905c`  
		Last Modified: Thu, 25 Apr 2024 21:52:43 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3653ddce29d93a5d03aeeccc718ad2e6fb7b60166c5f8a2229a6f3fcc3abaa32`  
		Last Modified: Thu, 25 Apr 2024 21:52:43 GMT  
		Size: 3.1 MB (3076309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20f9b1db83f3ebe5058bcac76b74218e7857705cbc2b6c6de44555e21de84a5`  
		Last Modified: Thu, 25 Apr 2024 21:52:43 GMT  
		Size: 1.1 MB (1091412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e52b595401a2db955b98283650f78c9499fbc4822f365e234201813fd27af0`  
		Last Modified: Thu, 25 Apr 2024 21:52:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc74972d903bd6ae8bd1992f732ee501d955af3536cd17a1c39b298307ad83a`  
		Last Modified: Thu, 25 Apr 2024 21:52:43 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d11f3af85523795b1943a4472498a993ba9fa5af088dce8197f53bbb469d55`  
		Last Modified: Thu, 25 Apr 2024 21:52:47 GMT  
		Size: 237.7 MB (237691523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cd6b369e7b42aad3cde223ca302309a8531f8ffd16edc6be5e0308efd98741`  
		Last Modified: Thu, 25 Apr 2024 21:52:44 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:577490dd8bf0cacfa4302a9e27ed80a1f77f3ddd203db7c3cfd264b1e2d7c232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3026830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c53930ab975fb92f9ffcef8512b7e48fbf06ef3366ad4ad3f875661bb97c52f`

```dockerfile
```

-	Layers:
	-	`sha256:95db9968ee95b6f93e7cd185e593af25f9973c49ca934ec4cc5a2069efcb9e04`  
		Last Modified: Thu, 25 Apr 2024 21:52:42 GMT  
		Size: 3.0 MB (2999994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:100e93ae6bade57cbd72bcf6aa7525a32f28479e593d74eb736bf5399cb4ed3b`  
		Last Modified: Thu, 25 Apr 2024 21:52:42 GMT  
		Size: 26.8 KB (26836 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:5-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:53062884b587e1452af8a0a19041ade9574fc429fb3b6b382ded41dd15a01aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.7 MB (261721711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd1bc7e0fbaae0574a095c7ab21a741f7ca513f6d34c6a9b6d9e6325421bdc3`
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
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
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
	-	`sha256:935803725f5775642918295f3557fecf93003fde6403df6fcbb2379ce4795a1d`  
		Last Modified: Wed, 17 Apr 2024 18:54:25 GMT  
		Size: 26.0 MB (25976141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3fd5c65590d20091046442753552e41f6bb2d131a49113f00ef98d908f451b`  
		Last Modified: Fri, 26 Apr 2024 08:14:06 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc85b435ebfc0132408d206c2ef59169f5e1fec11958a3c18d0eff51748e6016`  
		Last Modified: Fri, 26 Apr 2024 08:14:07 GMT  
		Size: 2.9 MB (2930816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af431028c5eb041642f2dfe9f009c478ef8435c66718f1c8b06ca6b3a2d9c155`  
		Last Modified: Fri, 26 Apr 2024 08:14:07 GMT  
		Size: 1.0 MB (1024906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac470ae60838610d20e4d17789cec5e61476c47e71c0aea867b88c2026971aee`  
		Last Modified: Fri, 26 Apr 2024 08:14:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141929eda1eede08261ee2271e68cef612e46a80be66e237736d8086c442cded`  
		Last Modified: Fri, 26 Apr 2024 08:14:07 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1302a0bf29cba836cd73300102c0501ef1ce0e35a0a62eb90a3260674f89ea97`  
		Last Modified: Fri, 26 Apr 2024 08:14:12 GMT  
		Size: 231.8 MB (231782692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ac38a496b7904df727bc4ac413d97ec2d8ca86ed225226c85fa352d59b457b`  
		Last Modified: Fri, 26 Apr 2024 08:14:08 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:f35fc5baf1f72c1f49587b12233f6a1e9659d0e9071ff138f8cfaad177a3b7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3026916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bf263e5f48285aad266c0a65b91c245bd5377702d808dbe86744d2e1e0bd9d`

```dockerfile
```

-	Layers:
	-	`sha256:0a9b716f1399c7b6b75be572ed5a0543c13060758a9733363341e47a5c0329f6`  
		Last Modified: Fri, 26 Apr 2024 08:14:07 GMT  
		Size: 3.0 MB (3000227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dba6eb2ba2503dda8ec7311f51cea746c620915923eca1d42825bd64cbc8626`  
		Last Modified: Fri, 26 Apr 2024 08:14:06 GMT  
		Size: 26.7 KB (26689 bytes)  
		MIME: application/vnd.in-toto+json
