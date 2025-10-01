## `neo4j:2025-enterprise`

```console
$ docker pull neo4j@sha256:9a6ccaabd30c36766303fb6bda15cb13d2ce106d7812df893ae19ee7151204b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:fa376ec8912b5c7f8a070b8be99d6a92fa3faa47a999491d5129e2b4fb169f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.1 MB (538102112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9db3b7b32c9e8cf3f5e162c3ed05366f40886cb67d46f43898b58b9642c51a0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Tue, 30 Sep 2025 13:19:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Sep 2025 13:19:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0b81f4601987925d0a7a844b4206fc75fefb8cd989bc95b00f1ecbf38afc3e4f NEO4J_TARBALL=neo4j-enterprise-2025.09.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 30 Sep 2025 13:19:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
# Tue, 30 Sep 2025 13:19:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Sep 2025 13:19:30 GMT
WORKDIR /var/lib/neo4j
# Tue, 30 Sep 2025 13:19:30 GMT
VOLUME [/data /logs]
# Tue, 30 Sep 2025 13:19:30 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 30 Sep 2025 13:19:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 13:19:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec923cbc2421bc2d5f608020bef9b291ec63cb2db8ba1c364cc023aaf6a713e`  
		Last Modified: Wed, 01 Oct 2025 20:09:26 GMT  
		Size: 157.8 MB (157804740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d261bd2d7ecf0ab0f436448432ad971d6ff2f9a7a4421c78469a6ce292e8e5d0`  
		Last Modified: Wed, 01 Oct 2025 19:00:09 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a73d41cffc3b83050d124ed768e2e4f6f33c0171ab1b462123c81064f2d2e8`  
		Last Modified: Wed, 01 Oct 2025 19:00:09 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc39e4963476eb8c15d9cbd30024462061e6d829342c4596d6d5d87fee659bfb`  
		Last Modified: Wed, 01 Oct 2025 20:09:43 GMT  
		Size: 350.0 MB (350025115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:46f95f928415c3cda78cae4e8edc0ca9bac0212e2764c99295bab7e86974fe57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4866753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a2b85e696df5add24062fd6fcc6bbb9d3a6d9087a438d50b92c2a1e7877f54`

```dockerfile
```

-	Layers:
	-	`sha256:40b72890a00c023104e7c5e9082e45e1820ace868347afd23edf4f34d6f4ce7d`  
		Last Modified: Wed, 01 Oct 2025 20:43:46 GMT  
		Size: 4.8 MB (4845049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07eb5d3a0f8a1f799c975bd8094b9a69d501068df0c633b74750c6f8c7f102f5`  
		Last Modified: Wed, 01 Oct 2025 20:43:47 GMT  
		Size: 21.7 KB (21704 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:db8378f531e6883d6ccfc69fe075d9e2ee45176d7b438767558d0931234dd3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.1 MB (534112800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cac6b520acaecb658d753576df05350e4441e0d293d0f97afec867a2c498bf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Tue, 30 Sep 2025 13:19:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Sep 2025 13:19:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0b81f4601987925d0a7a844b4206fc75fefb8cd989bc95b00f1ecbf38afc3e4f NEO4J_TARBALL=neo4j-enterprise-2025.09.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 30 Sep 2025 13:19:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
# Tue, 30 Sep 2025 13:19:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Sep 2025 13:19:30 GMT
WORKDIR /var/lib/neo4j
# Tue, 30 Sep 2025 13:19:30 GMT
VOLUME [/data /logs]
# Tue, 30 Sep 2025 13:19:30 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 30 Sep 2025 13:19:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 13:19:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29f0c2eb2ab6409ba19d36ee7895b30a88a2bcb4c1cf580cc549ba439a24c5f`  
		Last Modified: Wed, 01 Oct 2025 20:47:07 GMT  
		Size: 156.1 MB (156081216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb938f939ef2913404d8de3f4f3e9a460d5e79355a2e79842632845f4b5b6b07`  
		Last Modified: Wed, 01 Oct 2025 16:25:00 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef116760e273753bcc0a8de0cc69128a8b610c9fae92ec58bb52b9b63f1af2c`  
		Last Modified: Wed, 01 Oct 2025 16:25:00 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f1b458b7486e11d6c903b145c91c4cfbef212e28c07dcdfac1f0cdf1f57932`  
		Last Modified: Wed, 01 Oct 2025 21:04:09 GMT  
		Size: 349.3 MB (349269239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:ec51076b2b8e60c99c8c0c3a64aa11f6a31b10046b0a9c9a9638d8669fb6e904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4840774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bafc6a7c4ddb2ec11a46d6cddab882d1e58f978787842571d5fbb3c96f5d0b4`

```dockerfile
```

-	Layers:
	-	`sha256:8a6da286fa6804578a6a4879026ddade6950b2c078b8fa5217d2c686fa177fc9`  
		Last Modified: Wed, 01 Oct 2025 20:43:52 GMT  
		Size: 4.8 MB (4818878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e91870de16675e2732982b677de8ce2c12ccf7b80b28ff411e5e75dd9cf54bc`  
		Last Modified: Wed, 01 Oct 2025 20:43:53 GMT  
		Size: 21.9 KB (21896 bytes)  
		MIME: application/vnd.in-toto+json
