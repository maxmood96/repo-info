## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:885ee3effa8cbb0cafbc77326374fb8ee7679957afe35d7b3592ffa5b3f99ab7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:c09bc65b6cce19657d494de81c53d279e5f720cf7486ccf188c742d27896b7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **509.3 MB (509304095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d53facffecbdda4ca252f617b9d6bc240af5ed62136d5e3da8b9d23208eac4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Mar 2025 13:20:50 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Thu, 27 Mar 2025 13:20:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Mar 2025 13:20:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=39d74d8f0e1f6d31a3ab459a2548f8c66eff86678bb141572513c6f68f893d45 NEO4J_TARBALL=neo4j-enterprise-2025.03.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 27 Mar 2025 13:20:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.03.0-unix.tar.gz
# Thu, 27 Mar 2025 13:20:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.03.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.03.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:20:50 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Mar 2025 13:20:50 GMT
VOLUME [/data /logs]
# Thu, 27 Mar 2025 13:20:50 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Mar 2025 13:20:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Mar 2025 13:20:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc89e2090f4f99653a1b91ddda7d11fd7fa7378d75be24fc18671add7a0e221`  
		Last Modified: Mon, 28 Apr 2025 22:08:58 GMT  
		Size: 157.6 MB (157634512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838d9aaf68c05e18ed0a7a5e4265eb49bea414161c9c473de6e2d99f2831a7ed`  
		Last Modified: Mon, 28 Apr 2025 22:08:55 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9c120e4072f47199a4b89d9baf487c196c24b662fbba98fdb99ac1bf2e08e1`  
		Last Modified: Mon, 28 Apr 2025 22:08:56 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ced5772fcd43a8c10413be5f562eea3eac3c2aa5387a1190d12263a1b63614`  
		Last Modified: Mon, 28 Apr 2025 22:09:02 GMT  
		Size: 321.4 MB (321401080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:776c52832f5445a78f780e5435ab2c80ed3ad80bd6a23538007df315c5836114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3561246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7214c2096010db9e1e1161b81a989ae97c0f82e5c9e747f09da17b7b3bb51cc5`

```dockerfile
```

-	Layers:
	-	`sha256:e339713c5f01257ee8a8a91e4d8a9202f34091fd13e52d9208269450e2244522`  
		Last Modified: Mon, 28 Apr 2025 22:08:56 GMT  
		Size: 3.5 MB (3539797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c5e745d5b5c2d022b1f4df72f6fc7e692d9cd8a51eb877478fbd7f7d18e241`  
		Last Modified: Mon, 28 Apr 2025 22:08:55 GMT  
		Size: 21.4 KB (21449 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f917e5124900dea3fa4646d728222657041914c76d7959f4df5332405f5cdb2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.1 MB (506060396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b340a1ccefb7df5169dd52e8c22ef7bb281cbb2636c8a7828d8415c1d6f44877`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Mar 2025 13:20:50 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Thu, 27 Mar 2025 13:20:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Mar 2025 13:20:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=39d74d8f0e1f6d31a3ab459a2548f8c66eff86678bb141572513c6f68f893d45 NEO4J_TARBALL=neo4j-enterprise-2025.03.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 27 Mar 2025 13:20:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.03.0-unix.tar.gz
# Thu, 27 Mar 2025 13:20:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.03.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.03.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Mar 2025 13:20:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Mar 2025 13:20:50 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Mar 2025 13:20:50 GMT
VOLUME [/data /logs]
# Thu, 27 Mar 2025 13:20:50 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Mar 2025 13:20:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Mar 2025 13:20:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6ea0ce4481c6c59b9cdc12bd913c4b5bafca5da592cdedda4048ea90395fca`  
		Last Modified: Wed, 23 Apr 2025 18:09:18 GMT  
		Size: 155.9 MB (155928792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d759ae3f58108c9f4351916509909b22721918b49a05f6d6270842184f1b0f`  
		Last Modified: Wed, 23 Apr 2025 18:10:26 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17e6a480f6fa6f1b522258ce64ce062cc6d530e17bc7999b82130186b9f49c6`  
		Last Modified: Wed, 23 Apr 2025 18:10:26 GMT  
		Size: 10.0 KB (10022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bc43097314be860e5e86e0cba22a03e5b04f9f91cb6b44af44636c6e3a6876`  
		Last Modified: Wed, 23 Apr 2025 18:10:34 GMT  
		Size: 321.4 MB (321368186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:72f5b7b550db500dbe3785a3be04f8e65ec20e437b797472d4fd7004c8204b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3561079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ab739a101718c25daeaf0ecf1eb5377b518c0a892fe597c4dffae29b7f8c3c`

```dockerfile
```

-	Layers:
	-	`sha256:8481a32aa27c0d3797cfe849775a759ecbeb7c858c5994a8c01b5fe1bad16e86`  
		Last Modified: Wed, 23 Apr 2025 18:10:27 GMT  
		Size: 3.5 MB (3539437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd269fd95b8ec408ff68b88c0f571dc207e7acdd7dc9544d2b48b351ecdba0ab`  
		Last Modified: Wed, 23 Apr 2025 18:10:26 GMT  
		Size: 21.6 KB (21642 bytes)  
		MIME: application/vnd.in-toto+json
