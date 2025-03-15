## `mongo:8-noble`

```console
$ docker pull mongo@sha256:506d5c2b36a4bfa6997450fc387c2fa04b36c5aede480c7b24a056f4e2035547
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:8-noble` - linux; amd64

```console
$ docker pull mongo@sha256:8f3d23076b6992ddf4a42e53cf829859c28e921516094e3d9ddaf9e6522f45b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288450964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81a621037ef33c357805810a4995dd1bf81b8bc81f7640857d10f1dd7434f26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Fri, 14 Mar 2025 17:39:01 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 14 Mar 2025 17:39:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Mar 2025 17:39:01 GMT
ENV GOSU_VERSION=1.17
# Fri, 14 Mar 2025 17:39:01 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 14 Mar 2025 17:39:01 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 14 Mar 2025 17:39:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Mar 2025 17:39:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Mar 2025 17:39:01 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 14 Mar 2025 17:39:01 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 14 Mar 2025 17:39:01 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 14 Mar 2025 17:39:01 GMT
ENV MONGO_MAJOR=8.0
# Fri, 14 Mar 2025 17:39:01 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 14 Mar 2025 17:39:01 GMT
ENV MONGO_VERSION=8.0.5
# Fri, 14 Mar 2025 17:39:01 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 14 Mar 2025 17:39:01 GMT
VOLUME [/data/db /data/configdb]
# Fri, 14 Mar 2025 17:39:01 GMT
ENV HOME=/data/db
# Fri, 14 Mar 2025 17:39:01 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Fri, 14 Mar 2025 17:39:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Mar 2025 17:39:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Mar 2025 17:39:01 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 14 Mar 2025 17:39:01 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67c4ebf9460766c3ff634ee2987a8c2feeddf5868af800bdc58f25662b30544`  
		Last Modified: Fri, 14 Mar 2025 23:24:55 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afa02f8c09ee5fa9257ba0027a63be18d82e5ecf1dea795f9a9156246a04beb`  
		Last Modified: Fri, 14 Mar 2025 23:24:55 GMT  
		Size: 3.9 MB (3911366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7ca17a42bd92cc0beb1e66201c847bd8644ebdf4ec5c007dbbea2e8de3c86c`  
		Last Modified: Fri, 14 Mar 2025 23:24:55 GMT  
		Size: 1.1 MB (1130312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342a4f4728ffe530da8c68fe6791b6c846de81b20f740b7d43db9b54fb1d8e5f`  
		Last Modified: Fri, 14 Mar 2025 23:24:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bafd14fbe88f784f216133a1d53f267157ce210163bc353445b4a8dc97eb95`  
		Last Modified: Fri, 14 Mar 2025 23:24:56 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c492c8e8cfdcbbd6a76a6548e0ba7af70e7078e5f70c574aaff4ae016a882fb`  
		Last Modified: Fri, 14 Mar 2025 23:25:03 GMT  
		Size: 253.6 MB (253648404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734719e891c0965080626624fd5c750f37e62388950fc2b1e317d72c5cdb6839`  
		Last Modified: Fri, 14 Mar 2025 23:24:56 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:c2c8136cbd88bed7cf91b335015fe2faa1f0a1241f671a53ab7e7d8064eb7ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3873bd404d9c7044a8b2cce93b3be7aabf9eace9dac480220925744c1dd069fe`

```dockerfile
```

-	Layers:
	-	`sha256:b481d1b42ff9a69c72d6696b190878c6b6a6f37b643c3585ae680cdb883a3179`  
		Last Modified: Fri, 14 Mar 2025 23:24:55 GMT  
		Size: 2.5 MB (2524379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e851abdfbbb1c1dadf63c38629575451eb40dd8d534f64fd68c4fe07034112da`  
		Last Modified: Fri, 14 Mar 2025 23:24:55 GMT  
		Size: 28.8 KB (28840 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:8-noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:0a5974c4885b11f60d9411dd4f5296465dcfeca2f1338187b7f3ff56a2af1969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276689730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39c40dda68153a4c35b5dd411c23d34b3c37a02ea15569a233600110e14a753`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Fri, 14 Mar 2025 17:39:01 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 14 Mar 2025 17:39:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Mar 2025 17:39:01 GMT
ENV GOSU_VERSION=1.17
# Fri, 14 Mar 2025 17:39:01 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 14 Mar 2025 17:39:01 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 14 Mar 2025 17:39:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Mar 2025 17:39:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Mar 2025 17:39:01 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 14 Mar 2025 17:39:01 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 14 Mar 2025 17:39:01 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 14 Mar 2025 17:39:01 GMT
ENV MONGO_MAJOR=8.0
# Fri, 14 Mar 2025 17:39:01 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Fri, 14 Mar 2025 17:39:01 GMT
ENV MONGO_VERSION=8.0.5
# Fri, 14 Mar 2025 17:39:01 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 14 Mar 2025 17:39:01 GMT
VOLUME [/data/db /data/configdb]
# Fri, 14 Mar 2025 17:39:01 GMT
ENV HOME=/data/db
# Fri, 14 Mar 2025 17:39:01 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Fri, 14 Mar 2025 17:39:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Mar 2025 17:39:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Mar 2025 17:39:01 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 14 Mar 2025 17:39:01 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db36a6fa5a5c926f8a74b3f11768760522ee98c768dc655b42a1c44dc7c82251`  
		Last Modified: Wed, 12 Mar 2025 17:59:57 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760f9fca27722d1074ad9b7375fe4ebe6d6af4a584ef6a3bb012828153d3590a`  
		Last Modified: Wed, 12 Mar 2025 17:59:57 GMT  
		Size: 3.7 MB (3707274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf53cef41591a792ebe9720fa15bf0f0eb1d975f51f9280192edc93a88cf325e`  
		Last Modified: Fri, 14 Mar 2025 23:45:19 GMT  
		Size: 1.1 MB (1060685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db051dd9feae4bde9c1b8f7eb878b4539ffb3742597ae839657a50c7d5011bb`  
		Last Modified: Fri, 14 Mar 2025 23:45:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4279f66f03d3c47130ce0e28217ac1ff0acf76cb3e82f772ccb6b8b8d4646e8`  
		Last Modified: Fri, 14 Mar 2025 23:45:18 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b6129e229560a8bccb737e12d188ae44204a4f81174dae27007835b027b23a`  
		Last Modified: Fri, 14 Mar 2025 23:45:25 GMT  
		Size: 243.0 MB (243021582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b75310b0dbde0d21fcb6c4115c71f5e4425ed4da4e97756b998527cf24ba4a`  
		Last Modified: Fri, 14 Mar 2025 23:45:19 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:a8089cad72a995958f45a153006ff1f84473defcaa3f6cb3ad1ab85bd59d3e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83a2d14855a046faf1166079e59a76bd3ff1e036e6b66dfa69a5d3e16590b80`

```dockerfile
```

-	Layers:
	-	`sha256:fec8dd3237dbbda1f306ccef73c4b98b1b32e2f471611491b4b00cf6310af40f`  
		Last Modified: Fri, 14 Mar 2025 23:45:19 GMT  
		Size: 2.5 MB (2525515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb2631d1babe8ea76a1f913cd20812d85d4af9eb8a79657c4f802e669bfdd08`  
		Last Modified: Fri, 14 Mar 2025 23:45:18 GMT  
		Size: 29.1 KB (29066 bytes)  
		MIME: application/vnd.in-toto+json
