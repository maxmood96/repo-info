## `neo4j:community`

```console
$ docker pull neo4j@sha256:6ef6db341d90d516fbd582670192dced94067ce3e6ed6faa88f34546805f5bf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:a4a184f5cad249936a170ac75e84ecc91d71cde781a1e356340b0bd426707e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.4 MB (341393460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591d35aae922778e92e1f9f6eb505d9c3f03bf3f245aac12f82a9c0ddcb30eef`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:24:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:24:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:24:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f026977b1559a9a5e796faf6b0d3da3ecf8fae4d2bfb3a3c01ce9980f8010de2 NEO4J_TARBALL=neo4j-community-2026.01.4-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 17 Feb 2026 21:24:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.4-unix.tar.gz
# Tue, 17 Feb 2026 21:24:29 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 17 Feb 2026 21:24:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.4-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 17 Feb 2026 21:24:56 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:24:56 GMT
WORKDIR /var/lib/neo4j
# Tue, 17 Feb 2026 21:24:56 GMT
VOLUME [/data /logs]
# Tue, 17 Feb 2026 21:24:56 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 17 Feb 2026 21:24:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:24:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d0b63a1d6ed834ba72f9d6877308634c61815630ec57289bffc64c8dad38cb`  
		Last Modified: Tue, 17 Feb 2026 21:25:20 GMT  
		Size: 92.3 MB (92256289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7622c325bfc9d8122b37e06dba27d206ad49a84b6b8ef25e0a8022b4c71824c9`  
		Last Modified: Tue, 17 Feb 2026 21:25:17 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46b68b7962d6c1fa008c43a7e4e5ab34faa4e1b68369f94b2ce47325f0cabeb`  
		Last Modified: Tue, 17 Feb 2026 21:25:23 GMT  
		Size: 219.3 MB (219348522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:e5ab97416e9124174bba353ba1d45e03dd2b5423a62937ca201be34071025008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4409765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245b7c2b47260f1211f2b4f8d095e20bfd02bc4ddc46877861b5d832b15c8cf2`

```dockerfile
```

-	Layers:
	-	`sha256:822f25e480a9f785227be35f164c929257d6316964a03f39664c9093e04dca03`  
		Last Modified: Tue, 17 Feb 2026 21:25:17 GMT  
		Size: 4.4 MB (4387410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94acc9d6e152653be30ba3d709322feb76dc3a8291d29ac4d7e870a8f69f73df`  
		Last Modified: Tue, 17 Feb 2026 21:25:17 GMT  
		Size: 22.4 KB (22355 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2c07cfe563460cc542b6c2063cc0771d22bfc7e11e3264134ac15fa30ec5a56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.9 MB (339856650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7190902ed6f41d8a4a69d9fd9b22e6bcc3e84b485036b648a71102893865985`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:24:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:24:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:24:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f026977b1559a9a5e796faf6b0d3da3ecf8fae4d2bfb3a3c01ce9980f8010de2 NEO4J_TARBALL=neo4j-community-2026.01.4-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 17 Feb 2026 21:24:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.4-unix.tar.gz
# Tue, 17 Feb 2026 21:24:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 17 Feb 2026 21:25:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.4-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 17 Feb 2026 21:25:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:25:01 GMT
WORKDIR /var/lib/neo4j
# Tue, 17 Feb 2026 21:25:01 GMT
VOLUME [/data /logs]
# Tue, 17 Feb 2026 21:25:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 17 Feb 2026 21:25:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:25:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12566f8e35ae8d2780280fa4c358ba81665454b532f1ec3ec96b9a09fe6feacf`  
		Last Modified: Tue, 17 Feb 2026 21:25:25 GMT  
		Size: 91.3 MB (91288272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f480adc40e46193a391805fa95f9a763bf62418d7ebd5661394756bd17bea6`  
		Last Modified: Tue, 17 Feb 2026 21:25:22 GMT  
		Size: 10.0 KB (10016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b8d5d1296cebdd13dfdea9d81a444be9966a210c1e9188ea120f48adf53aa9`  
		Last Modified: Tue, 17 Feb 2026 21:25:28 GMT  
		Size: 218.4 MB (218418266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:e192a98a419d74f5bc2c7a10ebadbfcdceb5b4f11ee0a6e7aa2d5498325abe0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4404610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf7c6e59f24e6c044a2c56a42aeb551cd49b020cd6990f8caa222993eefd26a`

```dockerfile
```

-	Layers:
	-	`sha256:6a9ba2b05bd32f7c474545546d6cd6f25db014f85e83762b28a689ae37d8e4b1`  
		Last Modified: Tue, 17 Feb 2026 21:25:22 GMT  
		Size: 4.4 MB (4381981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82f13b6d90905936ec7632b7668dade8d22ec752500c9b08c45a6691a52f3abc`  
		Last Modified: Tue, 17 Feb 2026 21:25:22 GMT  
		Size: 22.6 KB (22629 bytes)  
		MIME: application/vnd.in-toto+json
