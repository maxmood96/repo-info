## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:fc5e43e419b0923eae836e9b218378fb86deb125320507ae99a9750964b347d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:920a9ea759b9b6ca3179cd00022c379164edf5e1aab2a0a84bdaced54c296e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.5 MB (594464110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8196ea37e56f8dc24ef31967f0688b512313677ae73903a418236d6fd6c1ae2f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Oct 2024 14:23:38 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Tue, 15 Oct 2024 14:23:38 GMT
CMD ["bash"]
# Tue, 15 Oct 2024 14:23:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Oct 2024 14:23:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7ce97bd9a4348af14df442f00b3dc5085b5983d6f03da643744838c7a1bc8ba7 NEO4J_TARBALL=neo4j-enterprise-5.24.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 15 Oct 2024 14:23:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.2-unix.tar.gz
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 14:23:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 15 Oct 2024 14:23:38 GMT
VOLUME [/data /logs]
# Tue, 15 Oct 2024 14:23:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 15 Oct 2024 14:23:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 15 Oct 2024 14:23:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d78db0f3a73b75daf645b4e1f733ca53f9530ce4e3585b8952efb416a72b5a2`  
		Last Modified: Thu, 17 Oct 2024 01:14:45 GMT  
		Size: 145.2 MB (145166496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da73729729fdbf7dad5946c5b66b0148b0e1601ad657b90fa156bd9bd4fa3a29`  
		Last Modified: Thu, 17 Oct 2024 01:14:43 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3c9035285f33e922d7689be5562474c5fec32274e2e2f2205b9789e022a4f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:43 GMT  
		Size: 10.0 KB (10008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc062885c744cb5d7821143c9088f9639a3a97c19f5c859931dcc69283cc6cd`  
		Last Modified: Thu, 17 Oct 2024 01:14:49 GMT  
		Size: 417.9 MB (417854939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:7584e44cda6b606e1e7798196effcaa663e694d7b874f64177090dfcc6137ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3490333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29fe7882f9ab9ce2e08357411359678bd30696632c842da806aadc687d69cd2e`

```dockerfile
```

-	Layers:
	-	`sha256:8a3272a8de20bee75a0f8373ee11382e5d5b4520758b98cfb63a5779c77e0278`  
		Last Modified: Thu, 17 Oct 2024 01:14:44 GMT  
		Size: 3.5 MB (3469277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fae0572ee30222395d0952b6f71c1c0d962b7147592d994ff4adc1f59754eb0`  
		Last Modified: Thu, 17 Oct 2024 01:14:43 GMT  
		Size: 21.1 KB (21056 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:36ed9f2252ccb26641b59a54e874d1d284d69b5ead967f4828c53ea72c335132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.9 MB (591864788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a0915516dcccd8033370da4a482c2a7833ff183f13ec0880dd2ffd99069199`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Oct 2024 14:23:38 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Tue, 15 Oct 2024 14:23:38 GMT
CMD ["bash"]
# Tue, 15 Oct 2024 14:23:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Oct 2024 14:23:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7ce97bd9a4348af14df442f00b3dc5085b5983d6f03da643744838c7a1bc8ba7 NEO4J_TARBALL=neo4j-enterprise-5.24.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 15 Oct 2024 14:23:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.2-unix.tar.gz
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.24.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 15 Oct 2024 14:23:38 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Oct 2024 14:23:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 15 Oct 2024 14:23:38 GMT
VOLUME [/data /logs]
# Tue, 15 Oct 2024 14:23:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 15 Oct 2024 14:23:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 15 Oct 2024 14:23:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414bb17c66e1a956e8e8cfbcd993934c289b1940da79f19f4baaede4b6a72b09`  
		Last Modified: Thu, 17 Oct 2024 08:15:01 GMT  
		Size: 144.0 MB (143959469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e441c891a0a607ffd7c487f22e228c83d14584d86040f698b1f909aac041d6fe`  
		Last Modified: Thu, 17 Oct 2024 13:24:54 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cbba9cf9e5dc46fbac084f316957c7b370029bf9730744a81e13018bf4e979`  
		Last Modified: Thu, 17 Oct 2024 13:24:53 GMT  
		Size: 10.0 KB (10003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc7e1ffdd6293addc6f0d1800e6b689733386646ac9bb7c8e1f279803096677`  
		Last Modified: Thu, 17 Oct 2024 13:25:06 GMT  
		Size: 417.8 MB (417815663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:0dd7a7dad669d3b6cfcef3cf5bb8f821606a7f8540d640193c9ba37d4f56f06e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3490205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0109b1a869edc24764cd39d1f7894f51fb5ae3bf94b190420b2a68f6458fea`

```dockerfile
```

-	Layers:
	-	`sha256:4b0c2bf597bf505ef8161f44faeaa959e910ac74192d735dbe6ff22dc936f975`  
		Last Modified: Thu, 17 Oct 2024 13:24:54 GMT  
		Size: 3.5 MB (3468969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6add5287530066a265ed2291a17a0b4236bba17de8c8fb175417754f352033f9`  
		Last Modified: Thu, 17 Oct 2024 13:24:54 GMT  
		Size: 21.2 KB (21236 bytes)  
		MIME: application/vnd.in-toto+json
