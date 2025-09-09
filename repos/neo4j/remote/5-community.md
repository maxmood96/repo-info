## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:6819749f84847681d8ad2a0af4f5a3d426b054cd2f93e6116fc90f4b1a7a6f67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:03f80fc0f08d28868404b7f27ce20d896f8d90a49fe8fb6d8f4ed9974680af00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.7 MB (305670857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a62aa37d5d6786cb1310c646c4824cf4f14c423a1224e5227cb41dc7447875`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 04 Sep 2025 06:40:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Thu, 04 Sep 2025 06:40:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Sep 2025 06:40:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63a686fc7cd28cbbfeb7cb5a98c6d47569914546f23a571390a9d1a1a65bd286 NEO4J_TARBALL=neo4j-community-5.26.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 04 Sep 2025 06:40:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.12-unix.tar.gz
# Thu, 04 Sep 2025 06:40:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.12-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Sep 2025 06:40:51 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 Sep 2025 06:40:51 GMT
VOLUME [/data /logs]
# Thu, 04 Sep 2025 06:40:51 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 04 Sep 2025 06:40:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 Sep 2025 06:40:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1224d36a010d2c1e1dc5ebb1efb4931d2949fa01de2dbf97908c1433a46dfd`  
		Last Modified: Mon, 08 Sep 2025 22:09:05 GMT  
		Size: 144.7 MB (144693304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75535fde32a5fd56cda023bc3c4e7670eb295a4aad04edf71ba19aa0286a71d7`  
		Last Modified: Mon, 08 Sep 2025 22:09:07 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbcd75cc03b58a01e8109e6439e876e4bb3122c4eece13db88971ff6bdf3751`  
		Last Modified: Mon, 08 Sep 2025 21:36:38 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4481f38953d354f9bf108977073c36708ed366586a24fd09222f1c4b3a3089`  
		Last Modified: Mon, 08 Sep 2025 22:08:53 GMT  
		Size: 130.7 MB (130707555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:95a7d1de41c40b80603f9a877ce033ce59691e25156ab518a294fbd5fdd8c02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5112ee438b27746bc8ac21e51847f60d5bc6e3f0ca8ca7d9af6af1890ede39`

```dockerfile
```

-	Layers:
	-	`sha256:9c257a89ceda378779ebb58eb478943712df1f3a18e9820fb03a075ad8df8620`  
		Last Modified: Mon, 08 Sep 2025 23:44:35 GMT  
		Size: 4.5 MB (4482914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fa79147332dd09f51c69bd65ab1ccebb9e00e21fc234f8a8959ff3261961b79`  
		Last Modified: Mon, 08 Sep 2025 23:44:37 GMT  
		Size: 22.8 KB (22809 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a91ffc781820dcebb158706e8354074247802bfc60a453bfc1b430c33fff4723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302258707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6173e29f3880dace94603b549ca790bd8c44b2aaa992351102e5060fafbf95`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 04 Sep 2025 06:40:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Thu, 04 Sep 2025 06:40:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Sep 2025 06:40:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=63a686fc7cd28cbbfeb7cb5a98c6d47569914546f23a571390a9d1a1a65bd286 NEO4J_TARBALL=neo4j-community-5.26.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 04 Sep 2025 06:40:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.12-unix.tar.gz
# Thu, 04 Sep 2025 06:40:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.12-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 04 Sep 2025 06:40:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Sep 2025 06:40:51 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 Sep 2025 06:40:51 GMT
VOLUME [/data /logs]
# Thu, 04 Sep 2025 06:40:51 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 04 Sep 2025 06:40:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 Sep 2025 06:40:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102cb4e7b87b3498f1d97f1a60900e115fb974feebff838e73e89288163a6f39`  
		Last Modified: Mon, 08 Sep 2025 21:43:39 GMT  
		Size: 143.5 MB (143542149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a021e132d6fe86ee0504bb6581d3aa9607b74ead51e2330125e5af185c9365b`  
		Last Modified: Mon, 08 Sep 2025 22:08:04 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650c42e61bb4f891e5e6639b19680f73960ef4ce977d51186087180230346548`  
		Last Modified: Mon, 08 Sep 2025 22:08:09 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0305e47b2dbcb275df278c01c7e0f3071cada31df8a7d752128a95b9e4fd492`  
		Last Modified: Mon, 08 Sep 2025 21:43:39 GMT  
		Size: 130.0 MB (129952143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:efb597943b7245d1eeebf9a57960e0bf5684f020a2e54d06a34bc2862717c9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4479841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:629fe50b2b4017b21f0ab4a97ccc1c8ac2c2cfb852c14bb6481f52e0205f6d07`

```dockerfile
```

-	Layers:
	-	`sha256:c0874953cf012be5ab849b4f0f164d8a8b6ec8a23ce44d1d9d4c089e96ada90a`  
		Last Modified: Mon, 08 Sep 2025 23:44:42 GMT  
		Size: 4.5 MB (4456791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6edf6bc03046edf0f71e1a66234689090adeb5b2f0d3178e897cdfb0b15280f8`  
		Last Modified: Mon, 08 Sep 2025 23:44:42 GMT  
		Size: 23.1 KB (23050 bytes)  
		MIME: application/vnd.in-toto+json
