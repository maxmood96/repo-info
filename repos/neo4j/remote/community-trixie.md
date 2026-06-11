## `neo4j:community-trixie`

```console
$ docker pull neo4j@sha256:d42aba649c92f8839991a9ba0e1fb0e76892ccd80832257ff36267c7c5052db8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:b4c0c8647774735883fad3588480757f6bd3e8acbb46cfc0ec8778912652881b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.2 MB (371213852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02c51e099c2028098437bcaf2ab83d94ddd6d85a7e105a65b47cf95103fd597`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 00:44:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 00:44:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=bb753b4e9bcc331e90b968edd8da445e974090867ca825cc672defdad6066f0e NEO4J_TARBALL=neo4j-community-2026.05.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 11 Jun 2026 00:44:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.05.0-unix.tar.gz
# Thu, 11 Jun 2026 00:44:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 11 Jun 2026 00:44:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.05.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 11 Jun 2026 00:44:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:44:40 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jun 2026 00:44:40 GMT
VOLUME [/data /logs]
# Thu, 11 Jun 2026 00:44:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 11 Jun 2026 00:44:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:44:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ed80d456b1e8dd5d62daa52088a0b5afedde164daa1184a8b63c4355dd1747`  
		Last Modified: Thu, 11 Jun 2026 00:45:03 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122bf1bc5ef1669e297e45fe196d7ed0b6b77e43699f5663e20c93e1eb14e45c`  
		Last Modified: Thu, 11 Jun 2026 00:45:00 GMT  
		Size: 10.0 KB (10014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791236720cd163be51a4ee6d7686f5b1edc340f4c7178e1cc6fd5fe7c63e8807`  
		Last Modified: Thu, 11 Jun 2026 00:45:07 GMT  
		Size: 248.8 MB (248843827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:89402ec1e9d2bb8971e1e73861b328de5400efb069474cf43592da3e404a3b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4385210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7c3a87b0e46e37f0dba1eb5f40b4e6bf67ed220b7f23fa4d87d53b3d32ae87`

```dockerfile
```

-	Layers:
	-	`sha256:d7da8ac01ea1ae486e61fb2489d8ee70b5931fbf398e8f2ca6cdcd894f8802dd`  
		Last Modified: Thu, 11 Jun 2026 00:45:00 GMT  
		Size: 4.4 MB (4362701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1164172a8de120f298b97a9d4afe91ffb012ac307f97ed1b2c7827ee0e0c2cad`  
		Last Modified: Thu, 11 Jun 2026 00:44:59 GMT  
		Size: 22.5 KB (22509 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:af23f69bec651067664076ef3006d73f3614539e127020d6184c552609f10ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.6 MB (369616313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08bee7d29b4684a22ba17925a3f66456c580c0ae2ec1a2983922a7827215eb1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:45:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 00:45:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 00:45:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=bb753b4e9bcc331e90b968edd8da445e974090867ca825cc672defdad6066f0e NEO4J_TARBALL=neo4j-community-2026.05.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 11 Jun 2026 00:45:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.05.0-unix.tar.gz
# Thu, 11 Jun 2026 00:45:51 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 11 Jun 2026 00:46:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.05.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 11 Jun 2026 00:46:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:46:14 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jun 2026 00:46:14 GMT
VOLUME [/data /logs]
# Thu, 11 Jun 2026 00:46:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 11 Jun 2026 00:46:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:46:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a83dd3d65503b0e37a2a2caf0589a39ea99c29d02b53afedd6c5f10ffe34fd`  
		Last Modified: Thu, 11 Jun 2026 00:46:39 GMT  
		Size: 91.5 MB (91542261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c44ab19de230604cc03b54c06dc9b42dba1efdd10689a454f6e45421ce7d5d1`  
		Last Modified: Thu, 11 Jun 2026 00:46:36 GMT  
		Size: 10.0 KB (10018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2541a942fb3404b82b67ceb5ba7f9aecd9a59c28e043982449f97e7c2a3df4`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 247.9 MB (247915472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:116cb620041fe1dab49e9761d2b7f6c4a54ad44d24dc8f238102b6d2b4050e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98efdaab77c67d3b9aa5471ea392431c9a5850d41fd8456c5fac3c91b1388b9f`

```dockerfile
```

-	Layers:
	-	`sha256:8f50dea4e1713183c92fe85702a64d39bd3aa6fb370aab3e98ac4ef367c9f028`  
		Last Modified: Thu, 11 Jun 2026 00:46:36 GMT  
		Size: 4.4 MB (4357264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b67c3fec9e34ad364487349e0642d5ef690a3385780ca5939c91c99c9d8cf16`  
		Last Modified: Thu, 11 Jun 2026 00:46:36 GMT  
		Size: 22.8 KB (22783 bytes)  
		MIME: application/vnd.in-toto+json
