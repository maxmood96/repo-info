## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:a505dec1d64a2797f76d03fac983c48f39f4bec2c1fb520515ef3c13987e80a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

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

### `neo4j:5-enterprise` - unknown; unknown

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

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d89b124682604c4ea5a2e6afe90259ba97ea4ddaa721fd2b66d5efe6c6458a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.8 MB (648848698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4523442a00d039f88db9a127f5807348f24dafa04438c1f8f156391386161ba`
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
	-	`sha256:5fef6ee0b9946051d8d3bfa169999cf4c735d5970589010a1411377faea8c31a`  
		Last Modified: Wed, 02 Jul 2025 11:51:22 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d45eddab9cabc8077864d1a8393930324e320f140da3956fe81acb5ccaffe4`  
		Last Modified: Wed, 02 Jul 2025 08:47:46 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66a1673f6fc0ceb28217cb4b2b0941c4325d10440c72bf34596f5b4f190e36b`  
		Last Modified: Wed, 02 Jul 2025 08:47:46 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821239c145a1912bd8aba43fa9a851251395de252cda766b3bd242400c4380b7`  
		Last Modified: Wed, 02 Jul 2025 13:28:23 GMT  
		Size: 476.6 MB (476578000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:734bb2d62fc3be7d9099ef9a179bfc0824a0d2ce2a7a9bf871dba59a92a12253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4854876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238df415ca76d4b11aee9270eff70860908a71f79afa327b3cc2f3d9525583e3`

```dockerfile
```

-	Layers:
	-	`sha256:bfbbd50be687186cf5846e572d716022bb2fc8faad4ee0b9c0422e549a806434`  
		Last Modified: Wed, 02 Jul 2025 11:44:11 GMT  
		Size: 4.8 MB (4833694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98bd59b98747301b5171da6e71c91bf729651ff294bf9a05ce01ae894eacc907`  
		Last Modified: Wed, 02 Jul 2025 11:44:11 GMT  
		Size: 21.2 KB (21182 bytes)  
		MIME: application/vnd.in-toto+json
