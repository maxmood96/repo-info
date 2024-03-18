## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:838de73d2f310b5e949526f21dbfebbb3cd96c90c3a2e26647e663b88ff66481
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:58493c48026e0a2f692b1ccb9e492e6d65f008da5b25b1d4dd918235f7e953ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557172447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f330eb7278051975e4417a4cd75fe83ee2283b214f85fb4da6e92390924231`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780d02b22b4bc2ee99138f6f8c073c75ed4c005ddd1ab50d1d1c417d1c47c493`  
		Last Modified: Mon, 18 Mar 2024 18:37:16 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30416cac1a73765fc4fa530339682deca30f6e64fcc0c7b1821d3099285c7c1`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 3.8 KB (3844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1527d59162ce7411b72ef36fab2a67fc12f3a94ddb40c697fdbb62895074cf`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc11d282d34d871d300f927eecd6a1b57bb0661a773b370cf9c721b8a36ae51`  
		Last Modified: Mon, 18 Mar 2024 18:37:19 GMT  
		Size: 380.8 MB (380843542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2a2ee8765dba8ce8bb9b63e172f7f95343d3f3fdfebf34cc8abc21e6d8ad1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0d8b56d5b550944a60c3bad68a8fcf7e2045d4ebb8d796028a127196800da1`

```dockerfile
```

-	Layers:
	-	`sha256:945595dfdfb5eceea1676cf83030e69f8d4baef597a4ea9a3cf166842c89ab87`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6316ff8ca6c6b92a0b7e029e2ac5fe0ac5d1ea45f41c6cd56104726599ede16b`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
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
