## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:93feaa788d19c0a7e5783f3e81d45189ce4707a91b38f9ffb72072b9a9a11f42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:672df4c65dc451d147a6be9784289ee7fa9ba1e7d540a62eb6a3323ee292f9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.1 MB (514104185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e5e06c79afe06e3276aec160c30b9c53a846824ee84013dddabc85ec6aa731`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Thu, 23 Apr 2026 17:15:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 Apr 2026 17:15:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 Apr 2026 17:15:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=566389e8dda4f9907113193a2324f5879176a687bd3c72e033c36b88a0140ff2 NEO4J_TARBALL=neo4j-enterprise-2026.04.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 23 Apr 2026 17:15:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
# Thu, 23 Apr 2026 17:15:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 Apr 2026 17:15:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 Apr 2026 17:15:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:15:51 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 Apr 2026 17:15:51 GMT
VOLUME [/data /logs]
# Thu, 23 Apr 2026 17:15:51 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 Apr 2026 17:15:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 Apr 2026 17:15:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7cc05ca1cf7b2254225fad0f69acca413c819aa274157974692c33789135d0`  
		Last Modified: Thu, 23 Apr 2026 17:16:19 GMT  
		Size: 92.3 MB (92256332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5224655913f20b619591783a32e788a9a85c349b813d028e078ecdc63e8c391b`  
		Last Modified: Thu, 23 Apr 2026 17:16:16 GMT  
		Size: 10.0 KB (10017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4783390011d606480997c71c3186306bf200eaf19d9bfc7ccaba61482137422a`  
		Last Modified: Thu, 23 Apr 2026 17:16:25 GMT  
		Size: 392.1 MB (392057630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b76ad888bb6738081e570b0f936f3bdc9dbd1904bfb22b39b8348273c91d6c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4683787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7626007b992ed3c4751abfc92bb54ed17c7dde82d3a59aae8fccb9b741babcfd`

```dockerfile
```

-	Layers:
	-	`sha256:931eb795fc2348cb493d0b40b8e66ad7f8475766c403a4674a8669955b624204`  
		Last Modified: Thu, 23 Apr 2026 17:16:16 GMT  
		Size: 4.7 MB (4663824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f9fe4b88aaa10f205eff885670ee761a78dfbfd8a4b7ade1ee428d6b9f10b67`  
		Last Modified: Thu, 23 Apr 2026 17:16:16 GMT  
		Size: 20.0 KB (19963 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5654bf8da0ac8242e5c2c71c7232cd1aa43b802980d8933b6e918585dab7af00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.6 MB (512567067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fe2b27c7ead174ddfbe26c6fd6aa520d5256b98bd616e21ed0023683221b29`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Thu, 23 Apr 2026 17:15:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 Apr 2026 17:15:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 Apr 2026 17:15:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=566389e8dda4f9907113193a2324f5879176a687bd3c72e033c36b88a0140ff2 NEO4J_TARBALL=neo4j-enterprise-2026.04.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 23 Apr 2026 17:15:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
# Thu, 23 Apr 2026 17:15:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 Apr 2026 17:15:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.04.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 Apr 2026 17:15:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2026 17:15:50 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 Apr 2026 17:15:50 GMT
VOLUME [/data /logs]
# Thu, 23 Apr 2026 17:15:50 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 Apr 2026 17:15:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 Apr 2026 17:15:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928fa5dfb34144ee625eff1f309f8f97613568e0641313553247d44d5bb419ad`  
		Last Modified: Thu, 23 Apr 2026 17:16:22 GMT  
		Size: 91.3 MB (91288287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c794a800de5bf76647f383c541cc0caa5ec31edbf35ae32a5523f605661fed`  
		Last Modified: Thu, 23 Apr 2026 17:16:18 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac71afbbade0387cec462718c92c52627b5555b031e14e3b74d8af6df8240c0`  
		Last Modified: Thu, 23 Apr 2026 17:16:27 GMT  
		Size: 391.1 MB (391125121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:05595599a96d5dae76c9f2cdc0d35535b78fe55e66198f58d8780081880298b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4678440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7e9a6f485ebf765ed4a8ef4a7337d1928ded32d9812668d3e489a55a357cad`

```dockerfile
```

-	Layers:
	-	`sha256:1db0dd3c3d92d79cd6c955ad1cb31775d51870a78472df6da7c866abae6eccfd`  
		Last Modified: Thu, 23 Apr 2026 17:16:18 GMT  
		Size: 4.7 MB (4658299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c69deb7a2de59b9c4145526e8cee43186c89eaddc9c6c2c42c52ed967bf7578`  
		Last Modified: Thu, 23 Apr 2026 17:16:17 GMT  
		Size: 20.1 KB (20141 bytes)  
		MIME: application/vnd.in-toto+json
