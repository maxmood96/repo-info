## `neo4j:2026-enterprise-trixie`

```console
$ docker pull neo4j@sha256:58360b3dad8f8359a7a00cebfd5dd405d9ad6553aea97bb73ad5616869e46c0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-enterprise-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:e8ce00452642e5574df3a40a67209aa5aaeae36a21053564a42ab1e332dc4dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.0 MB (490028484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bedac673ccbe27036c94dbcd9ac76b357678bd81213a6bbfd14b715a31477b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Wed, 04 Feb 2026 21:09:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Feb 2026 21:09:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Feb 2026 21:09:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3326a905d4accc1bdd224923a6d30c9a498bbd0fb7b43e87983aec29734c367d NEO4J_TARBALL=neo4j-enterprise-2026.01.3-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 04 Feb 2026 21:09:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
# Wed, 04 Feb 2026 21:09:41 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 04 Feb 2026 21:10:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 04 Feb 2026 21:10:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 21:10:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 04 Feb 2026 21:10:08 GMT
VOLUME [/data /logs]
# Wed, 04 Feb 2026 21:10:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 04 Feb 2026 21:10:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 21:10:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dc15291f4378ef46a41324e70583d96ed7fb41d76ae46698329b382f3b7d77`  
		Last Modified: Wed, 04 Feb 2026 21:10:37 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0677209cc89b5cfe3f2e42ff0e0c8ac6daebdda0fe545d0b7876291dca0cee`  
		Last Modified: Wed, 04 Feb 2026 21:10:33 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51097c20fd464551b9d2aced3277248a186ea5d079100a1c98efbd6ca088669a`  
		Last Modified: Wed, 04 Feb 2026 21:10:43 GMT  
		Size: 368.2 MB (368194540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:3ba55b89d0c730495455dd8b7bd1777c4c46f095ca4740725b8e021af76f19c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4632091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5350bbde36f74c6e1a1d1360b0b39f8040acf734008f7896e1b38461713223e`

```dockerfile
```

-	Layers:
	-	`sha256:cf533faae46651f5bbe0ef8db5c831e2f38f328e63b053d72fb61223f3cfebcc`  
		Last Modified: Wed, 04 Feb 2026 21:10:33 GMT  
		Size: 4.6 MB (4612128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22a8eae02b106e61c7dc4f7429aed784c25e4892a6d2ffeccbc6275e74c7594f`  
		Last Modified: Wed, 04 Feb 2026 21:10:33 GMT  
		Size: 20.0 KB (19963 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-enterprise-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:883266a7c6a46c628f88b4b6f319c3b6180fd9cde76d84dba293e9add8da007a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **488.5 MB (488473941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f52dca6ba5a2259f47152f610b7ae12f02c164e60c96dfdf85e53349172811`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Wed, 04 Feb 2026 21:05:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Feb 2026 21:05:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Feb 2026 21:05:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3326a905d4accc1bdd224923a6d30c9a498bbd0fb7b43e87983aec29734c367d NEO4J_TARBALL=neo4j-enterprise-2026.01.3-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 04 Feb 2026 21:05:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
# Wed, 04 Feb 2026 21:05:16 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 04 Feb 2026 21:06:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 04 Feb 2026 21:06:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 21:06:48 GMT
WORKDIR /var/lib/neo4j
# Wed, 04 Feb 2026 21:06:48 GMT
VOLUME [/data /logs]
# Wed, 04 Feb 2026 21:06:48 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 04 Feb 2026 21:06:48 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 21:06:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4294f798d5d8e50a6140327df68d06eeb2750404104221be398188a178e11cdc`  
		Last Modified: Wed, 04 Feb 2026 21:06:04 GMT  
		Size: 91.1 MB (91052482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077c222396ab5f80503eb028c14ff6784681979c3c552703d10a0337f76d044a`  
		Last Modified: Wed, 04 Feb 2026 21:06:00 GMT  
		Size: 10.0 KB (10022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75e2f235df2d1043feb5a51ce2f823a0b3cd2b19e5fb7d5c1d9ae14b1dd4cc3`  
		Last Modified: Wed, 04 Feb 2026 21:07:20 GMT  
		Size: 367.3 MB (367271341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:5545b03a1d497ab27ce020519a6f0dcebddf98f9b12f005dcf496bef6d1e7645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4626744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa93835010f6466919d83854d814f9bf3946574505460b1bba7971056905858c`

```dockerfile
```

-	Layers:
	-	`sha256:ea47920279efb177e1e6ba6fbd7544bfcb75e0306e0e451003c820c23708e417`  
		Last Modified: Wed, 04 Feb 2026 21:07:14 GMT  
		Size: 4.6 MB (4606603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b62fe19f493f0137cf74396576a0086e2d84b8562f4092329deeb4238fb1f625`  
		Last Modified: Wed, 04 Feb 2026 21:07:14 GMT  
		Size: 20.1 KB (20141 bytes)  
		MIME: application/vnd.in-toto+json
