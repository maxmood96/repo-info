## `neo4j:community`

```console
$ docker pull neo4j@sha256:0f5c756e6cc18cd53fed04db25505a9f097842f847f872c6ff73ffc71ae7c0a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:0b65cd45e30ca9a2e7cd6799ce2b1bda55306b91dd8ea8112cfccfe442666140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.4 MB (341392179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59093d74e3227dfd7a405098cc3c8aab649f49beb9d6bbce293905dd7cf28dc`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 22:50:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:50:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 22:50:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=fd9376186034a84eeca384971b2e9e3e80f8e41166529843f49c48e390a48694 NEO4J_TARBALL=neo4j-community-2026.01.3-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 05 Feb 2026 22:50:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.3-unix.tar.gz
# Thu, 05 Feb 2026 22:50:16 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 05 Feb 2026 22:50:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.3-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 05 Feb 2026 22:50:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:50:40 GMT
WORKDIR /var/lib/neo4j
# Thu, 05 Feb 2026 22:50:40 GMT
VOLUME [/data /logs]
# Thu, 05 Feb 2026 22:50:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 05 Feb 2026 22:50:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:50:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17d38c6c4189ca1b9a92e6872afec90c68cd5cd08d2b24d6857890448e72b94`  
		Last Modified: Thu, 05 Feb 2026 22:51:03 GMT  
		Size: 92.3 MB (92256263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7976f083da46ef5869a8ca189b3d9422127ee3e7fff106971dc56d2ea0e06317`  
		Last Modified: Thu, 05 Feb 2026 22:50:59 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b39230b73cc6ce003b8f45cbb4ca40b56bc9d1931356d229cc8c9607689b8d`  
		Last Modified: Thu, 05 Feb 2026 22:51:05 GMT  
		Size: 219.3 MB (219347267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:203a6552e5baa2207ede06537fd84fef45a047696ecdaf1f48d4dcc60a6d3ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4409765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a0306a358f6108085923c917ae9e31017624a111f94d228c1271be2c110194`

```dockerfile
```

-	Layers:
	-	`sha256:4d1b77399e53fda9294329e2e3a022b96670869a73d9785e2550019fc2488bae`  
		Last Modified: Thu, 05 Feb 2026 22:50:59 GMT  
		Size: 4.4 MB (4387410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc51b4e7b0136cf4af9fd1d114ac39f5b88ee6243e5bcf471c2394394e402e4`  
		Last Modified: Thu, 05 Feb 2026 22:50:59 GMT  
		Size: 22.4 KB (22355 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ab695cf1d1ad99bf4aaa1400a44daf1f4e10a5ccf6ebb0338af5bbc56e21155a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.9 MB (339855647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e520593ce47b108a74d3afdb243eb6dc0c008a9ddf3cbbbeb9f905ae9f136102`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 22:50:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:50:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 22:50:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=fd9376186034a84eeca384971b2e9e3e80f8e41166529843f49c48e390a48694 NEO4J_TARBALL=neo4j-community-2026.01.3-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 05 Feb 2026 22:50:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.3-unix.tar.gz
# Thu, 05 Feb 2026 22:50:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 05 Feb 2026 22:50:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.3-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 05 Feb 2026 22:50:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:50:40 GMT
WORKDIR /var/lib/neo4j
# Thu, 05 Feb 2026 22:50:40 GMT
VOLUME [/data /logs]
# Thu, 05 Feb 2026 22:50:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 05 Feb 2026 22:50:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:50:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37afe58b16a225f4cc090239679dd513408d9949320ac5988e322d94cde2a9f5`  
		Last Modified: Thu, 05 Feb 2026 22:51:04 GMT  
		Size: 91.3 MB (91288272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ed4593a9be9500618983407cdf963274a0de927856287d57538d1b4c637db8`  
		Last Modified: Thu, 05 Feb 2026 22:51:01 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54187a54e80538adb190498c326fa0ddc9c774320913246aecb5b4954159e404`  
		Last Modified: Thu, 05 Feb 2026 22:51:07 GMT  
		Size: 218.4 MB (218417258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:6992fd0f84cc31726c63bad6377c4c5cdcbd6d717edaa4ba396bfe128a81e677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4404610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8256093ca66625c4deb62182e9c8660d391671620b49714806e0ec5072cbe879`

```dockerfile
```

-	Layers:
	-	`sha256:36e0f645b28c941cf972ad88dbe52d988f32c9767bbe367d9295c2b75618b395`  
		Last Modified: Thu, 05 Feb 2026 22:51:01 GMT  
		Size: 4.4 MB (4381981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5276bfe5d90789f573a823f9a9d2794fc61ea67257ad01c2f770b78c7ffeabf9`  
		Last Modified: Thu, 05 Feb 2026 22:51:01 GMT  
		Size: 22.6 KB (22629 bytes)  
		MIME: application/vnd.in-toto+json
