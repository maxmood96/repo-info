## `neo4j:2026-enterprise-trixie`

```console
$ docker pull neo4j@sha256:3a7d41f14a50b5636d3cdf1d736c1af36657becc516fda709ff5722c62fa4d13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-enterprise-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:74d0447124faaacbda0c842bd4cf5ad5f747428d9451752f599b6f750a39f3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.4 MB (514422431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74692fcc67adcdac6d3a8367e9890f7f27b0cc5ae631956badfb4b88b876671`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 19:42:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 19:42:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=566389e8dda4f9907113193a2324f5879176a687bd3c72e033c36b88a0140ff2 NEO4J_TARBALL=neo4j-enterprise-2026.04.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 08 May 2026 19:42:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
# Fri, 08 May 2026 19:42:39 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 08 May 2026 19:43:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 08 May 2026 19:43:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:43:05 GMT
WORKDIR /var/lib/neo4j
# Fri, 08 May 2026 19:43:05 GMT
VOLUME [/data /logs]
# Fri, 08 May 2026 19:43:05 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 08 May 2026 19:43:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:43:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a63c37c8f3b378b2908819c83547ba7552e3e11f8e5bb5afafe37edd687ecc5`  
		Last Modified: Fri, 08 May 2026 19:43:35 GMT  
		Size: 92.6 MB (92574597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2115081d87b1f531895db432364281fb83e948e43228eecf00b9e979a3a26e2`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ee2f1dd98abb3f7340c747869b8001f034f0da05d8701afcea03003036d741`  
		Last Modified: Fri, 08 May 2026 19:43:40 GMT  
		Size: 392.1 MB (392057555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:26c7452d49319c2f28ca407e8ba0eec3e72e5124522581f57a2d700379b79384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4684564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e64c4a129e159910a34be74d58f03a93540170a1b32eae3dbe43966ddb7734`

```dockerfile
```

-	Layers:
	-	`sha256:2efe7d717273fce071b885559baf8b89510e30369e4d08faa60f973ebf86807e`  
		Last Modified: Fri, 08 May 2026 19:43:32 GMT  
		Size: 4.7 MB (4664447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92f787503c73a11608497dfa7ebfec9e6889e7a9854866356d5e2fc39588cdea`  
		Last Modified: Fri, 08 May 2026 19:43:31 GMT  
		Size: 20.1 KB (20117 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-enterprise-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7c7b0f6a3d944394bab118437a2ce097a35b13230919ffcadb4f4ffc9db2a87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.8 MB (512821896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec34ea1815df9ce3f3c14a153da541a2a6f285ca240b3367126a5b06156c61cb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 19:44:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 19:44:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=566389e8dda4f9907113193a2324f5879176a687bd3c72e033c36b88a0140ff2 NEO4J_TARBALL=neo4j-enterprise-2026.04.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 08 May 2026 19:44:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
# Fri, 08 May 2026 19:44:31 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 08 May 2026 19:44:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 08 May 2026 19:44:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:44:58 GMT
WORKDIR /var/lib/neo4j
# Fri, 08 May 2026 19:44:58 GMT
VOLUME [/data /logs]
# Fri, 08 May 2026 19:44:58 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 08 May 2026 19:44:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:44:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6855211a4b0c4c07a65026e4bc74ee1201161b7970d3123a4ba536543b7527`  
		Last Modified: Fri, 08 May 2026 19:45:30 GMT  
		Size: 91.5 MB (91542269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7792ec010c244b76957c0b0011f9a33df29335c2be27911bf6c52d3c7c0c42fc`  
		Last Modified: Fri, 08 May 2026 19:45:26 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe1d5aa3a92a83f39ccf47e4db6becb5c1f4ad3207e3bf1cf65638a650de0f4`  
		Last Modified: Fri, 08 May 2026 19:45:37 GMT  
		Size: 391.1 MB (391125932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:f13b064ea04870264656e8cc14a6c6751c21d882915f9f5b2542d2d7cf6e7782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4679216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1be9bd9bb54188b12f442f778632e06edc90d186277acfe82e3e636ed66940`

```dockerfile
```

-	Layers:
	-	`sha256:0fb483ecec9d77a6865b2a777260aa021f210729b80301723b90bf625e8a60cc`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 4.7 MB (4658922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b53ea9cf107538546e454685bf171f39bf88466e31017eb300ac5a452d9d27f`  
		Last Modified: Fri, 08 May 2026 19:45:26 GMT  
		Size: 20.3 KB (20294 bytes)  
		MIME: application/vnd.in-toto+json
