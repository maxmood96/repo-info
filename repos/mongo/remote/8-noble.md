## `mongo:8-noble`

```console
$ docker pull mongo@sha256:6fe103ae60b5929989ec6d6e2f5eb159e8b3c53685b26b9fb41cf2ca8bf279cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:8-noble` - linux; amd64

```console
$ docker pull mongo@sha256:6b0f3b8898c09d1d15753978cd8a733834f692d70aa3d424f680bccd2896f6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.9 MB (285924417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe2220a3a52775d0ddfc59d6ca8140c80e5169c5c374f048b8a76f2f11820e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 06 Dec 2024 23:01:34 GMT
ARG RELEASE
# Fri, 06 Dec 2024 23:01:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 06 Dec 2024 23:01:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 06 Dec 2024 23:01:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 06 Dec 2024 23:01:34 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Fri, 06 Dec 2024 23:01:34 GMT
CMD ["/bin/bash"]
# Fri, 06 Dec 2024 23:01:34 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 23:01:34 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 06 Dec 2024 23:01:34 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 06 Dec 2024 23:01:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 06 Dec 2024 23:01:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 06 Dec 2024 23:01:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 06 Dec 2024 23:01:34 GMT
ENV MONGO_MAJOR=8.0
# Fri, 06 Dec 2024 23:01:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
ENV MONGO_VERSION=8.0.4
# Fri, 06 Dec 2024 23:01:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
VOLUME [/data/db /data/configdb]
# Fri, 06 Dec 2024 23:01:34 GMT
ENV HOME=/data/db
# Fri, 06 Dec 2024 23:01:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 23:01:34 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 06 Dec 2024 23:01:34 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b085c891536905a630108e9c2cae84e5df58a2e4c9522292e5f10f3ea59609`  
		Last Modified: Tue, 04 Feb 2025 04:25:49 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8170e4b2100044db8144d8c602ce88f3bf9c54d362bebd6d264ae8f484a4a356`  
		Last Modified: Tue, 04 Feb 2025 04:25:50 GMT  
		Size: 1.5 MB (1507712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa9099a841aa455ba8890471169d2b9eca5ce33602ce9099645e6fcca74379a`  
		Last Modified: Tue, 04 Feb 2025 04:25:50 GMT  
		Size: 1.1 MB (1130168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce7aaa046eeae8acaa1058fa7d32c5511f2295cb531b288f9804f95e0131616`  
		Last Modified: Tue, 04 Feb 2025 04:25:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53a70bd8c23d8f8cfa4a1048f3e5fe87a0241af20831c5dce50f05d3309fa86`  
		Last Modified: Tue, 04 Feb 2025 04:25:50 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c76b9a0da2596161beb8f2d67ff8d34faf57865807f6877e54e34428776ef20`  
		Last Modified: Tue, 04 Feb 2025 04:25:59 GMT  
		Size: 253.5 MB (253525653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990f24c1b0762fed7b60e0aff8160df42b43330ad4ea6e9fe14a5a4189d8320a`  
		Last Modified: Tue, 04 Feb 2025 04:25:51 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:71e7a6568cd2cbd7960f73316f3d0313236b1397137767b9f2e97280a894609d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2552947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ea7d9d26fec05960afc4092afb4035ca97d2c40ec59a4a4fe8ec63e0956aca`

```dockerfile
```

-	Layers:
	-	`sha256:d4e1cdaf7002d3e43cbfa30a8a4a6c4712992715ed129964bed3e49a33063107`  
		Last Modified: Tue, 04 Feb 2025 04:25:50 GMT  
		Size: 2.5 MB (2524375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25624e5fe1a2f076e1ba11596e9eb4b6782081249133a040c7a722fd06f3edbe`  
		Last Modified: Tue, 04 Feb 2025 04:25:49 GMT  
		Size: 28.6 KB (28572 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:8-noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:a76cbb4d4f8410d918acd7864851d989dc098a302f08130272431f687d71ff07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.4 MB (274373779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f16add76dfe97756170429fa25b5102cb4384a7eea7bb94303c1ac7efc6847`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 06 Dec 2024 23:01:34 GMT
ARG RELEASE
# Fri, 06 Dec 2024 23:01:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 06 Dec 2024 23:01:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 06 Dec 2024 23:01:34 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 06 Dec 2024 23:01:34 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Fri, 06 Dec 2024 23:01:34 GMT
CMD ["/bin/bash"]
# Fri, 06 Dec 2024 23:01:34 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Dec 2024 23:01:34 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 06 Dec 2024 23:01:34 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 06 Dec 2024 23:01:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 06 Dec 2024 23:01:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 06 Dec 2024 23:01:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 06 Dec 2024 23:01:34 GMT
ENV MONGO_MAJOR=8.0
# Fri, 06 Dec 2024 23:01:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
ENV MONGO_VERSION=8.0.4
# Fri, 06 Dec 2024 23:01:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
VOLUME [/data/db /data/configdb]
# Fri, 06 Dec 2024 23:01:34 GMT
ENV HOME=/data/db
# Fri, 06 Dec 2024 23:01:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 06 Dec 2024 23:01:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Dec 2024 23:01:34 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 06 Dec 2024 23:01:34 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57206b2c2f49bae2b4b2a62c43e6b6fcef27c05df7db7879d3e203aef2db906e`  
		Last Modified: Tue, 04 Feb 2025 10:09:16 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31671604d6bf0cbab08e486892cc9f69f5ce6a45a1e63c148ed38a07c2bff6a2`  
		Last Modified: Tue, 04 Feb 2025 10:09:17 GMT  
		Size: 1.5 MB (1492017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8626d1b8e2adc910df7f95398d359f408e7315740cc887966be1d9265b0a3408`  
		Last Modified: Tue, 04 Feb 2025 10:09:17 GMT  
		Size: 1.1 MB (1060531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1aa7dfe923a34dcd012c2cd795df9690c48f9bdc033b284188861fb38794ffb`  
		Last Modified: Tue, 04 Feb 2025 10:09:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2eb3e2f1b19dce025b5df2d73f2eb88653de2be8873b73bfc7a909fe4f2771`  
		Last Modified: Tue, 04 Feb 2025 10:09:17 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d170f9caa3009819cf5ad1b341d6cb6b1d56fa72d925e2ac6678ec0fb27e9c59`  
		Last Modified: Tue, 04 Feb 2025 10:09:23 GMT  
		Size: 242.9 MB (242921037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f4e92e71e1d78a98e115e7243e433d0f4961429c3797d05a3da72105f23d6c`  
		Last Modified: Tue, 04 Feb 2025 10:09:18 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:e0751d071b89a9d624e5ca4dba79cea1130782d2108fbd5f17bf5bd398ff1596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56c87d3b4670b58b88cd28ee4d5a976f30283ba4886903c3bba0d8516daabfd`

```dockerfile
```

-	Layers:
	-	`sha256:71fefb86aeb0f30843f2da28f9f4483f1ee420bee132bb82f408b14f6c34c6a4`  
		Last Modified: Tue, 04 Feb 2025 10:09:17 GMT  
		Size: 2.5 MB (2525511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdcc56ad6586ca102f4d69041347e75d9b903ecde92d301f1cd9aaca8efa370a`  
		Last Modified: Tue, 04 Feb 2025 10:09:16 GMT  
		Size: 28.8 KB (28799 bytes)  
		MIME: application/vnd.in-toto+json
