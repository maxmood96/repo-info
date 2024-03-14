## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:36bc7fadb9afec73a2eb4bcfa19844a90bbb6a5957c07db8d1de3caec5b84771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:291c8f54bb68b73893d6b8033284f53a4d7eb6f8735209241a37f275d13b9ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557171902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb73604ad9fd708f013276b18597e207831d18e14661fb70e54d7905191a5165`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e68e5c089844daf9f08460efccfc0561874936190e10b4af31b74c5cdad648`  
		Last Modified: Wed, 13 Mar 2024 19:50:55 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9f037a727b88b4f735ce95c33762cb3d044beef4b26093e50d932d18ab8b55`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b19e47a9c78334ceb36d56a8e9df45c497c368a990bb5c64dea11ba27fffff`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8266ce07a566a25dddc5b82565c41f15d92f3b3867fe3583ad7b310c146645`  
		Last Modified: Wed, 13 Mar 2024 19:51:00 GMT  
		Size: 380.8 MB (380843001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:50848cdacb6a5cb9e435d2c80e59afa04b2021b7c1c5195fcc0078494554320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7782abd9c2e9e89f1b2218ebea2d37e7bdd15c19629e9f08c682535a38965a`

```dockerfile
```

-	Layers:
	-	`sha256:7e79e748d787e14fc48dab9645096462fe1949dcdea86193ec5dd1eac7a16144`  
		Last Modified: Wed, 13 Mar 2024 19:50:52 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03b9ab1e275fe75e23c702bea31050b5e48c4865cd9212144dfa5d3d4475bce`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3a54ac46e2711df9a42b4dd1d2d60528b14b2b34844dad2864718610cfa4a756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554612849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fb262c0611b2c5928d02e895ec57225bb2834bebb944918448cedc9d5c203c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e38e4dfe0d7e2b4c883bb9dbdfb9b92f0fcdb107d3f003c2a17ac9b9ab90267`  
		Last Modified: Tue, 12 Mar 2024 22:17:28 GMT  
		Size: 143.7 MB (143720407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8069ee70137f9dcf7f4ef1b952b2bec6a4c23760dfcb967593e91b0abf124f`  
		Last Modified: Wed, 13 Mar 2024 19:52:55 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75506c7aa22e57c2f47b01a544705e63ffa1483382d8a63b150fd69fa857dceb`  
		Last Modified: Wed, 13 Mar 2024 19:52:55 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0fa1249dabf9993c26d71ddf3ab7a48dad02cc7e2da8714ac96e1bfbded688`  
		Last Modified: Wed, 13 Mar 2024 19:53:03 GMT  
		Size: 380.8 MB (380807891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0a1f04ab05dd7afbfa7b9790d8e582fba472a1a7039045b01ead28ef552473f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9bf8f432824b4e848d416af42e855fe3e235d5ff35f24928866ef02199be87`

```dockerfile
```

-	Layers:
	-	`sha256:11879ddd0521286ac33efd2fd80d27f144d507038a48ef5d03888060717b89ce`  
		Last Modified: Wed, 13 Mar 2024 19:52:56 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eae2cc5909bfc60e5ccee8b43d7ca16e365bd934e1d637e18a263d56e23238c`  
		Last Modified: Wed, 13 Mar 2024 19:52:56 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json
