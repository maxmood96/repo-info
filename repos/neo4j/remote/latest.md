## `neo4j:latest`

```console
$ docker pull neo4j@sha256:a2c781d94f92ba0438b9111bdb240120a00b4ad6fe520f27f69d76ffc1ee43f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:922361295d9ea617de79e52f8aed1b26d6e8b883ed16589e50cd560b52d263af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.2 MB (371208652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac22cf25c88ca4a5222435fa3428b7647c74b26ddb270d13ade2c230fc599496`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Mon, 01 Jun 2026 22:37:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 01 Jun 2026 22:37:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 01 Jun 2026 22:37:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=bb753b4e9bcc331e90b968edd8da445e974090867ca825cc672defdad6066f0e NEO4J_TARBALL=neo4j-community-2026.05.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 01 Jun 2026 22:37:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.05.0-unix.tar.gz
# Mon, 01 Jun 2026 22:37:51 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 01 Jun 2026 22:38:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.05.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 01 Jun 2026 22:38:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Jun 2026 22:38:19 GMT
WORKDIR /var/lib/neo4j
# Mon, 01 Jun 2026 22:38:19 GMT
VOLUME [/data /logs]
# Mon, 01 Jun 2026 22:38:19 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 01 Jun 2026 22:38:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:38:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1aceb5545d6df93b967e2b19ba0f79acb72c8a06470e4766268ff4194fcb6bf`  
		Last Modified: Mon, 01 Jun 2026 22:38:40 GMT  
		Size: 92.6 MB (92574589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e64b4556d4f8832a140a8eb9224c9a2317c14556d9098a25c5b6a76c54bc545`  
		Last Modified: Mon, 01 Jun 2026 22:38:37 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f0fda5942c18a04d8bb25ec0f45a8ae69c8d4a74e4a7f9996a4133af493d52`  
		Last Modified: Mon, 01 Jun 2026 22:38:43 GMT  
		Size: 248.8 MB (248844084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:1d58cf745b1caabdc4fdba29f084e9e73c05c34ebcb8d9b1dbe10f0477ce5916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4385210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8394b3b3aac20129a14d4c4382f644dd5a008fe5745027df965074c4c0af2c`

```dockerfile
```

-	Layers:
	-	`sha256:ccb135570bfd6100e6722d14c197a3d355df16e09c3be17874ea6941115f6cf8`  
		Last Modified: Mon, 01 Jun 2026 22:38:37 GMT  
		Size: 4.4 MB (4362701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ff434f1234443380087c611c977c42452a3f2a7f595bedfade86dd9511cfc5`  
		Last Modified: Mon, 01 Jun 2026 22:38:37 GMT  
		Size: 22.5 KB (22509 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1d37619e6add978134c1cb18186efe00e5c09e577b5f38d61509666cc9152abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.0 MB (367009563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b23edcb479ac603c0d56f4fdf55bbbd28a7a0a0ec1ac8871dfae6037712c21`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:28:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:28:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=fd750466b1247c0d1ef09a84c614f7e045793b30dfa277148e8da71646598820 NEO4J_TARBALL=neo4j-community-2026.04.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 19 May 2026 23:28:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
# Tue, 19 May 2026 23:28:37 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 19 May 2026 23:29:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 19 May 2026 23:29:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:29:01 GMT
WORKDIR /var/lib/neo4j
# Tue, 19 May 2026 23:29:01 GMT
VOLUME [/data /logs]
# Tue, 19 May 2026 23:29:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 19 May 2026 23:29:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:29:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d02a0b02b0a2fee546440b8b26e911492900960a48ada515d3f3d1f5ad32022`  
		Last Modified: Tue, 19 May 2026 23:29:25 GMT  
		Size: 91.5 MB (91542270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1264213c21d3318afd6d2fdfc255bb5b04d9aa28cf85f3bc1131fe42be7d50`  
		Last Modified: Tue, 19 May 2026 23:29:22 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f56d027ab0f13b25ddb17805f752e3c3562d8b862dbba29d78f2410b6b38774`  
		Last Modified: Tue, 19 May 2026 23:29:28 GMT  
		Size: 245.3 MB (245315321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:3f80ffd4b3f1d81ee2630bbbc11644f167b8a4e674e4a9eba5c255c76b3d9048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4377347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8fcd2605aa59fe987221136196db5f046180e80415ae1c9c515b02c4300da9`

```dockerfile
```

-	Layers:
	-	`sha256:48c4c9e6f103fce8e682972f4d3ac5dd467ae7ed5237d325d4e6fbdee402c25b`  
		Last Modified: Tue, 19 May 2026 23:29:22 GMT  
		Size: 4.4 MB (4354564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77157fe7dfe5a5f24a6f99f08dc8df619a98a84f586c28307557fb20f7603c64`  
		Last Modified: Tue, 19 May 2026 23:29:22 GMT  
		Size: 22.8 KB (22783 bytes)  
		MIME: application/vnd.in-toto+json
