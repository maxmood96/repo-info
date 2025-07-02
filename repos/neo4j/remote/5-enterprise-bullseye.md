## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:bee5f7c937296ba05544abe8cfefec34b2e5911c77054cf40a4619786b020527
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:431168397107d7a1ad0d7da395cc946d359104e654c3be74fc2be7ca61f6dd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **652.2 MB (652238631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f8236c9098c8f2f94e612708b2e6420f2a171f5bb7438c60f9508ca149a105`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Jun 2025 10:01:35 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Mon, 09 Jun 2025 10:01:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Jun 2025 10:01:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=906d67491fa2f1352f06fa327d3b850b5f8163ad1fe7bdd8d193326c2855e65b NEO4J_TARBALL=neo4j-enterprise-5.26.8-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Jun 2025 10:01:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.8-unix.tar.gz
# Mon, 09 Jun 2025 10:01:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.8-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.8-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 10:01:35 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Jun 2025 10:01:35 GMT
VOLUME [/data /logs]
# Mon, 09 Jun 2025 10:01:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Jun 2025 10:01:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Jun 2025 10:01:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e941dd1750a1d1502aefa0f3ae94c46e8b38fda65631a02e35e86e4ffa12ec31`  
		Last Modified: Wed, 02 Jul 2025 08:44:24 GMT  
		Size: 144.6 MB (144635030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c479b84994623fde58c36bd3916eb71474232d6d4d98cec1a2d65b8cfb71b62`  
		Last Modified: Wed, 02 Jul 2025 08:44:14 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074507f3351b29f6b47085c34e24c9d0917d091d54a08d76226d47cc2935e4a6`  
		Last Modified: Wed, 02 Jul 2025 08:44:15 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a438488ec807c737fb3e7bf5520a1a782ba385e2247575c2d7aecba6ef9d06`  
		Last Modified: Wed, 02 Jul 2025 08:44:54 GMT  
		Size: 477.3 MB (477333653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3ff60b8eb965716f2f200e7381760519cc2e7b1c547a0953c4645447a9f2a6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e134735d695afecf9ad24884de3d83febd51f905c9e1d033082ca70a6e4e7147`

```dockerfile
```

-	Layers:
	-	`sha256:6191cbc3d53dbf078e3da4dd3e7518dd8253fcb102ebc789230f706260dff771`  
		Last Modified: Wed, 02 Jul 2025 08:43:52 GMT  
		Size: 4.9 MB (4859889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a216c002b4f13685aa6d813ab9a34d51a274d000c7d48a5ed14454054184cdb`  
		Last Modified: Wed, 02 Jul 2025 08:43:53 GMT  
		Size: 21.0 KB (21013 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cfd14cf00b563ad7d8d8f2209c345f33ad8f72034c53b39eff644dd68ebd3b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.8 MB (648848689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d219c8429a7d1640b5e16e9d0fb604d788ff555defa864e371098fd530e213`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Jun 2025 10:01:35 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Mon, 09 Jun 2025 10:01:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Jun 2025 10:01:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=906d67491fa2f1352f06fa327d3b850b5f8163ad1fe7bdd8d193326c2855e65b NEO4J_TARBALL=neo4j-enterprise-5.26.8-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Jun 2025 10:01:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.8-unix.tar.gz
# Mon, 09 Jun 2025 10:01:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.8-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.8-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Jun 2025 10:01:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jun 2025 10:01:35 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Jun 2025 10:01:35 GMT
VOLUME [/data /logs]
# Mon, 09 Jun 2025 10:01:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Jun 2025 10:01:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Jun 2025 10:01:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62bd73b5d8c3ab8e527ba51e9b40ba5e6501a7c7901b0c2ec811446b945e8ac`  
		Last Modified: Tue, 01 Jul 2025 08:50:41 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720fda21f87dad8f94ca2770bc1b38f009ef570aa6ed4398c4b5e757c8d67264`  
		Last Modified: Tue, 01 Jul 2025 07:21:36 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1a7406060b047b877afde901cee5eb38fa9029bc6beca42d50574fb4afcae1`  
		Last Modified: Tue, 01 Jul 2025 07:21:36 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d8636e23d58e91619638afadf9eb6ad498e774f67539bb5337a04d81ee49f0`  
		Last Modified: Tue, 01 Jul 2025 09:10:45 GMT  
		Size: 476.6 MB (476577988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:7eb7a1f5881ebbcb6f56f7db15ce68811f0d3f23abc2344d7856794ed4dead80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4854876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bb724d7b6d62576e3ecdfec25f7244effaa91d2573d2d2ee172e6df9bd0ce1`

```dockerfile
```

-	Layers:
	-	`sha256:61c70c887d4efd49aa5cf76e249daf2c04afee9a987e81c89a3cf1d4ddb8fa92`  
		Last Modified: Tue, 01 Jul 2025 08:44:17 GMT  
		Size: 4.8 MB (4833694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1df0c50d8ca4f604991a737ae730409fed1988fa1ed2edafa0ae93719098d58e`  
		Last Modified: Tue, 01 Jul 2025 08:44:17 GMT  
		Size: 21.2 KB (21182 bytes)  
		MIME: application/vnd.in-toto+json
