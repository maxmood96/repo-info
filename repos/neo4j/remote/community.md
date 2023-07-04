## `neo4j:community`

```console
$ docker pull neo4j@sha256:95de8dc67e16abc946a16d385bba05080f06f7590170d58f788d179ce5d8621e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:fa8f71d6091bc76419f571acd04d30fd654642c7f834e5d671f637303611425d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339764660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246f3b226b168f5342e28e71b7502c2fe6bf1d2afe536b7694ce2cb9cd99c25`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:19:27 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:30 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:19:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:19:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:19:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:19:50 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:19:50 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:19:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:19:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16587156d6d664ce45c78f53fd4abf3903d66718d37c56e9d942121e5a5c2298`  
		Last Modified: Fri, 16 Jun 2023 05:21:41 GMT  
		Size: 192.6 MB (192580339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf092e6a4075a792e6cfdfa941697da3110c57b3eed1a6514ac06fb653fcd446`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 3.9 KB (3853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e8789f08f62ffed6acd775d54345f8ffdcc301329b64e9c9b676d8782c8ae`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b62bb6d5e4ab5cd0b4e67117c58f65929c22d74141894345bac35d9df4bf77`  
		Last Modified: Fri, 16 Jun 2023 05:21:34 GMT  
		Size: 115.8 MB (115753684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ab9c060c7ff61a54b35a7b38fc09f4cb143f210c2c7711c04d19802b0b97f10f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337110137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2aa94390a4d91363d5896f5f9c83921b57d038fa1fefc849bf32f4c662ab5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:34:28 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:34:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:34:32 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Tue, 04 Jul 2023 06:34:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:34:33 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Tue, 04 Jul 2023 06:34:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:34:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:34:48 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:34:49 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:34:49 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:34:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:34:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275827ff61a5cc842494b7c486dc8fd020f878ff693af5f57969cf5f7481a0d0`  
		Last Modified: Tue, 04 Jul 2023 06:36:29 GMT  
		Size: 191.4 MB (191387687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31bbf0eb561b1650f22e928cbeccb17872671effa64cad96c568923c773c5e1`  
		Last Modified: Tue, 04 Jul 2023 06:36:18 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7602e07641dac1311b8a2427efdb849b9749894a1a9ed64979931ed3d6f03bdc`  
		Last Modified: Tue, 04 Jul 2023 06:36:18 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925b08e9954cc34ec2861c0b6ea5ade09ae1a9361db08e6c22d2c5eba5010b65`  
		Last Modified: Tue, 04 Jul 2023 06:36:23 GMT  
		Size: 115.6 MB (115646236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
