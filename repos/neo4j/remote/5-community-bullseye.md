## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:3252f22777b26aa223fbc1ebac95b8f58552af62ff7cbdad5362a180da6943bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:e1dbba6c6bd0c18a27ccdd6ccfd2fbc83ab410777ec15a96722b6e3527de1b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351107464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1180167a77116973f120c76a369bdcf9c98a1a6c15731abdacdf7615e997e0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Thu, 10 Jul 2025 14:24:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 10 Jul 2025 14:24:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 10 Jul 2025 14:24:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2beb60e00e52562099a82693b8af2e48cdc8c96518d36b13a5816db0370a49ae NEO4J_TARBALL=neo4j-community-5.26.9-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 10 Jul 2025 14:24:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.9-unix.tar.gz
# Thu, 10 Jul 2025 14:24:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.9-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 10 Jul 2025 14:24:05 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 10 Jul 2025 14:24:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.9-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 10 Jul 2025 14:24:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jul 2025 14:24:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 10 Jul 2025 14:24:05 GMT
VOLUME [/data /logs]
# Thu, 10 Jul 2025 14:24:05 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 10 Jul 2025 14:24:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 10 Jul 2025 14:24:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e15b1a88ca69f48f2eb1a34c655d8771886578f09037c131a15caa1b189c07`  
		Last Modified: Sat, 12 Jul 2025 02:48:39 GMT  
		Size: 144.6 MB (144634998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821d9e3de3611c316ec6f4d5650522622b69cab7111a9b0959b75b9b40706e70`  
		Last Modified: Fri, 11 Jul 2025 23:41:40 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56dcf0cbbc390501dbc73df3aad56dc484059b2997fdff113bfe0ef5f97545f`  
		Last Modified: Fri, 11 Jul 2025 23:41:40 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9846d5457edbbd79a0a297ac7af2cf6a17ea74155cda29f2452276409838d31e`  
		Last Modified: Sat, 12 Jul 2025 02:48:36 GMT  
		Size: 176.2 MB (176202517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0a8cedeee7937132d05e61fef6132ca96288b7db2257c04cf190fe880adccca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4540413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ada8d2e0c14050f0a896e1cb1bc64be16af79bf38779002b1954ae8b8cbcc0f`

```dockerfile
```

-	Layers:
	-	`sha256:18f142d2129cd891a35d060ebf86c5d595ac3c28d7c41aa16992a82d3b87f167`  
		Last Modified: Sat, 12 Jul 2025 02:44:17 GMT  
		Size: 4.5 MB (4517623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ab388e51f4027567b18cc39181b8ec8a29e2e83414fdab6ccd3d5ad0f674d3c`  
		Last Modified: Sat, 12 Jul 2025 02:44:17 GMT  
		Size: 22.8 KB (22790 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:32de2dcaf8c723cb064e1dff1b97ee4e6ebc3cf9dda52614081d19b984710cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.7 MB (347717204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebc90cd4fd3a42a88ed292e4229842a0bc5e7e54ea69cda28db42f1666ea526`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Thu, 10 Jul 2025 14:24:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 10 Jul 2025 14:24:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 10 Jul 2025 14:24:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2beb60e00e52562099a82693b8af2e48cdc8c96518d36b13a5816db0370a49ae NEO4J_TARBALL=neo4j-community-5.26.9-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 10 Jul 2025 14:24:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.9-unix.tar.gz
# Thu, 10 Jul 2025 14:24:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.9-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 10 Jul 2025 14:24:05 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 10 Jul 2025 14:24:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.9-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 10 Jul 2025 14:24:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jul 2025 14:24:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 10 Jul 2025 14:24:05 GMT
VOLUME [/data /logs]
# Thu, 10 Jul 2025 14:24:05 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 10 Jul 2025 14:24:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 10 Jul 2025 14:24:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fef6ee0b9946051d8d3bfa169999cf4c735d5970589010a1411377faea8c31a`  
		Last Modified: Wed, 02 Jul 2025 11:51:22 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731e0e7e794808bb1bd570fec8fe873fcb706db23d6ce39ff77b81c0d58d4421`  
		Last Modified: Sat, 12 Jul 2025 00:38:31 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73fe0b9cb369b1cf447f989dcbd5cbccf0fd3fe81bafc99024c2ad92d5041dc`  
		Last Modified: Sat, 12 Jul 2025 00:38:31 GMT  
		Size: 10.0 KB (10030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4034178005bb979c4ab6091dfdaf50c2acba619005a4c01299f9deed863468eb`  
		Last Modified: Sat, 12 Jul 2025 03:33:33 GMT  
		Size: 175.4 MB (175446500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c37e73a0f499b1e6f5e1cbbbd55c171f0dcf7b570e615175e1165bcd96a851ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4514531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8481b7cf06c9b17c64d05fa3d2ae7aad88af9e0e2e33f367525c87fed7dbbbbf`

```dockerfile
```

-	Layers:
	-	`sha256:5a0c2992945e76f1b1fc21cdf958758a47f6fc01f18a3e4df5dbf27e004b2a84`  
		Last Modified: Sat, 12 Jul 2025 02:44:22 GMT  
		Size: 4.5 MB (4491500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3a182399dfc042b52f2e711571715daffd3d92bf4d13f3e8d35e29914ee03b7`  
		Last Modified: Sat, 12 Jul 2025 02:44:23 GMT  
		Size: 23.0 KB (23031 bytes)  
		MIME: application/vnd.in-toto+json
