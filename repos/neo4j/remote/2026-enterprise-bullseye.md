## `neo4j:2026-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:f773f539f0cca7e029282ef2b075976c4d127742d83636df589937c180b38f33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d956297fd27703cb7ee192a5644996effe3295992f46376fb80e4980ca1a40f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.4 MB (577427245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b49e43449e3c99cc55e3d568ff4f7c80e7e40fe6436652bafd79082b2c61b95`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Thu, 23 Apr 2026 17:15:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 Apr 2026 17:15:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 Apr 2026 17:15:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=566389e8dda4f9907113193a2324f5879176a687bd3c72e033c36b88a0140ff2 NEO4J_TARBALL=neo4j-enterprise-2026.04.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 23 Apr 2026 17:15:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
# Thu, 23 Apr 2026 17:15:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 Apr 2026 17:15:47 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 Apr 2026 17:16:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 Apr 2026 17:16:11 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:16:11 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 Apr 2026 17:16:11 GMT
VOLUME [/data /logs]
# Thu, 23 Apr 2026 17:16:11 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 Apr 2026 17:16:11 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 Apr 2026 17:16:11 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782b8a5b693159210c1f69a67cbdf8a4f2c6baad9c8937dda8f667b8f74602a`  
		Last Modified: Thu, 23 Apr 2026 17:16:45 GMT  
		Size: 157.9 MB (157857073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d3b1a03b50b403147ebe444718f85f03d0540a3880d67bd8e2c5a9d81ff6bd`  
		Last Modified: Thu, 23 Apr 2026 17:16:38 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f373759abff833d75748c7b7b2d585f8b09be134d4192c2398a1bc00b05a1cc`  
		Last Modified: Thu, 23 Apr 2026 17:16:38 GMT  
		Size: 10.2 KB (10205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f286c76dd1e11800305444f2cce85fe24ed45e71395a484e91e2da8cf99169`  
		Last Modified: Thu, 23 Apr 2026 17:16:49 GMT  
		Size: 389.3 MB (389298163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:7be8c0c438c850c31be5bfd9b09d1d5f596e79ab610e0f65fce8527071ca186e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4918016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4aaabae1ec03fe0ef32634a4448f0dc5df4f755f2f9309fc27468a5bcb3a04`

```dockerfile
```

-	Layers:
	-	`sha256:4f9145c05ec69172f713a25c7469a07ae6316e6807f1f9a13cbe6932354fc7e6`  
		Last Modified: Thu, 23 Apr 2026 17:16:39 GMT  
		Size: 4.9 MB (4897617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d3d8ea3b25605176988fd530679e9d898ceb62f1f6b9300f5a63ca062bd8fec`  
		Last Modified: Thu, 23 Apr 2026 17:16:38 GMT  
		Size: 20.4 KB (20399 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:192f87085332e549d4ff407f5a598148ea6f5bf16a57ab697f11237e26c50f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.8 MB (573761736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe34bd62c994109eb4adef4536de64ec1b9bed703cbfbb69dfe38a7fb74899c0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:18:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:18:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=566389e8dda4f9907113193a2324f5879176a687bd3c72e033c36b88a0140ff2 NEO4J_TARBALL=neo4j-enterprise-2026.04.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 08 May 2026 00:18:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
# Fri, 08 May 2026 00:18:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 08 May 2026 00:18:37 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 08 May 2026 00:19:00 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 08 May 2026 00:19:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:19:00 GMT
WORKDIR /var/lib/neo4j
# Fri, 08 May 2026 00:19:00 GMT
VOLUME [/data /logs]
# Fri, 08 May 2026 00:19:00 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 08 May 2026 00:19:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 08 May 2026 00:19:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56eee578c1d8d972144dd116c7149c97b18b1a6ee07cb9aa664c0bc2edcb14cb`  
		Last Modified: Fri, 08 May 2026 00:19:33 GMT  
		Size: 156.5 MB (156461225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc185eb628903ca4475b34ddde3539cac295d64ee01bbbfa4274a7909523d44`  
		Last Modified: Fri, 08 May 2026 00:19:27 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48175de0fb54c1fec4280377a18c9f104b14bd72b2d3a3dee66764ec72b869c8`  
		Last Modified: Fri, 08 May 2026 00:19:27 GMT  
		Size: 10.2 KB (10201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d86ff6c46745247592a53f358d02e3283fa6d81677323dc5a639a820bd69eb`  
		Last Modified: Fri, 08 May 2026 00:19:40 GMT  
		Size: 388.5 MB (388543898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d4ec4a1238d7905fc49fc2360ecab8d8f07c61f644ea6e544cb2a142e3402287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4892723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca3429082e5c342a814b6f93447c03a3344837a316ef9b2f1721d81a49fdabd`

```dockerfile
```

-	Layers:
	-	`sha256:ca983dbfc332047dff68a6459ecbb7d31079b3a0da1dd9775983d2b66c9189b7`  
		Last Modified: Fri, 08 May 2026 00:19:27 GMT  
		Size: 4.9 MB (4872025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb6d25278a535aced6e4a12739298962e5f97864de3a0c6173ad90cb43f12753`  
		Last Modified: Fri, 08 May 2026 00:19:27 GMT  
		Size: 20.7 KB (20698 bytes)  
		MIME: application/vnd.in-toto+json
