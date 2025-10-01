## `neo4j:community`

```console
$ docker pull neo4j@sha256:bd9fd536561bf09d5fbb144cd6b6f59d199e338da1303520116abdc687056e23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:c7bc36fc726c21ce5d762c965bde62612eb4b5c71a5cf673dde5413db56d9891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.3 MB (399317645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15ac5d176d8d6a1e80a91a02010c80540259408b1882a1f4e23cf0cba64f163`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Sep 2025 16:30:37 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Wed, 24 Sep 2025 16:30:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Sep 2025 16:30:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=38e6828ba11a700c94e4a532a10e3481e94cfabc45f9b4819cafc4bdc105cba5 NEO4J_TARBALL=neo4j-community-2025.09.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 24 Sep 2025 16:30:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
# Wed, 24 Sep 2025 16:30:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Sep 2025 16:30:37 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Sep 2025 16:30:37 GMT
VOLUME [/data /logs]
# Wed, 24 Sep 2025 16:30:37 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Sep 2025 16:30:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 16:30:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8095144b38ad21ac51e022149966abda1f520aa64d76e023e8c1725728c4638c`  
		Last Modified: Tue, 30 Sep 2025 22:47:47 GMT  
		Size: 157.8 MB (157804776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8547a4c5289e8eee944861898ae786c5cef59f5c8f831824b2db4eef596822`  
		Last Modified: Tue, 30 Sep 2025 01:04:52 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103f5671ff5f2adf7208a6d725a8ab544e371e912278c3df973dbb9dabbf1068`  
		Last Modified: Tue, 30 Sep 2025 01:04:52 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0260942c9dd2ae3587a728a0469afce6c280468d625775f7c1524d1b0bcca21a`  
		Last Modified: Tue, 30 Sep 2025 22:49:14 GMT  
		Size: 211.2 MB (211240617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:79c53fe505cde2e12c9c4c32dd579c04e8808a50d63f0b0dcc8b409785ba3633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4627779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a89ffadfa565e0501c2a28399ebbfd66ada95890a1071b8feafed9b9db1933f`

```dockerfile
```

-	Layers:
	-	`sha256:e9d803b8999cbf3cfa6dbf9cda6c67a11707928f37a65d383f546884651d9d1c`  
		Last Modified: Tue, 30 Sep 2025 20:43:27 GMT  
		Size: 4.6 MB (4603670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e72e907878170675c862df2d975b62a958e5eb7f46060eb18d8a42d9180a81`  
		Last Modified: Tue, 30 Sep 2025 20:43:28 GMT  
		Size: 24.1 KB (24109 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:637fb607c1e94b390dc056f032810f78ed6bdd169fa9d2b279644445e3935955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.3 MB (395328629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:203b498907ab4a30474a618be99bd49e4236fe22d3de68cde2fff0f472ce2d5b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 24 Sep 2025 16:30:37 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Wed, 24 Sep 2025 16:30:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Sep 2025 16:30:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=38e6828ba11a700c94e4a532a10e3481e94cfabc45f9b4819cafc4bdc105cba5 NEO4J_TARBALL=neo4j-community-2025.09.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 24 Sep 2025 16:30:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
# Wed, 24 Sep 2025 16:30:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Sep 2025 16:30:37 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Sep 2025 16:30:37 GMT
VOLUME [/data /logs]
# Wed, 24 Sep 2025 16:30:37 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Sep 2025 16:30:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 16:30:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4704d89a177a8bf24216b30202c330f13365c567ddf52ee488d4850410155a`  
		Last Modified: Wed, 01 Oct 2025 11:02:10 GMT  
		Size: 156.1 MB (156081218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8af8d8cd32de3bf0175d5423576ac0441b65d20ca635f26a3bdab7a5f15e23f`  
		Last Modified: Tue, 30 Sep 2025 00:18:08 GMT  
		Size: 3.9 KB (3863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710d092fdb444a060d2267fc6b1efae8ae6f764e7921ac4c72b76bf2cf58a49d`  
		Last Modified: Tue, 30 Sep 2025 00:18:08 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2519e10e623a2eed2cb15f8aabaa4f823a1224f2397a6af387821e10371f1a`  
		Last Modified: Wed, 01 Oct 2025 11:02:12 GMT  
		Size: 210.5 MB (210485068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:2c83a7fe4ab184641648f3351f75022bee519a7652cf3f3644747d1edcb05872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4601993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18fda15f04d535347cf0382c0ca371c5b44746d7f197cbd8ed4d64d8831d5a53`

```dockerfile
```

-	Layers:
	-	`sha256:4c9ff542894978b78a8b26d4105b84572239eed419105f56c7d503883b762150`  
		Last Modified: Wed, 01 Oct 2025 11:43:20 GMT  
		Size: 4.6 MB (4577595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:510a9fd6c43783a8bc8d17575c402bfa4f5be3f25c7944ba50e4637f6a6f3ddf`  
		Last Modified: Wed, 01 Oct 2025 11:43:21 GMT  
		Size: 24.4 KB (24398 bytes)  
		MIME: application/vnd.in-toto+json
