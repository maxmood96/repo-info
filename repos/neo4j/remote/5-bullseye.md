## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:e75829e8b9bd0c1797f089e7eb1ceb726232fda887554b74f80ce3b330653879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:afd6aebdc76a22b10400a35406982c7bc660d6689caf09f5c51146f2f694c8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ffce706897811457fd55247d62a6d91ca8d8d763d5ee68d06720e9a84851e5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2c1f3afaa66524093f6695771afc0863ba72985cb088d777934710c94e1f30`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d48018aa379af23d9797d940fe5d72d08525f1a01af7a02aee06afc2c73cd`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.8 KB (3849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de32ac1a96365c985435a9c6cbe5360a65af62a0d4e5128acd154bef564af8df`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae20a3ffeb4750cb4433b65595da02066ed8f697572ff3df9606ab403ed945`  
		Last Modified: Tue, 17 Sep 2024 01:57:39 GMT  
		Size: 127.3 MB (127275138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:226ef14b9399803837d15808e0f541daef59367a060fe2c69f49a7c40f3b4e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23db1de1bfae2e3dff7595567eb0f0f47c8b1076488a8df8d40b3a166b7ad1f8`

```dockerfile
```

-	Layers:
	-	`sha256:b98cf195f5283104dcd323832d12347ec389301292ed6cbec80af7d44d9328cc`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 3.0 MB (3030102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57708fc1180c3867e4278239f82f70532dd67c90227964777ab8b9e10d4f9d38`  
		Last Modified: Tue, 17 Sep 2024 01:57:37 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:71049124fb5d73e9e29f61404538f0cdd6d3928509423f9b637c5b122f6ede9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301289893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4305974b38bfefe9344ecfc9ca1346177c2ccd8da505a83b7adfb78d18266f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f55449bae4ec290f9641402fbc69309319cc209bbe79d2772ae3d8b275f393a`  
		Last Modified: Thu, 05 Sep 2024 08:04:53 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38706148773c618625864cde73d4b483752c530be384f633d245566a6dc28e88`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2506904d281219bdf090d25dfec2b1999be9cdbdfe3430ffd23d7b96f4f3f05`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151d4b36da25a669b88e70f3b264a3e88c2cbdcbfec745fe29237f1489f21ff`  
		Last Modified: Thu, 05 Sep 2024 12:30:53 GMT  
		Size: 127.2 MB (127242536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5ab4892a64e6b6af772f05ee53d6df5c72cdfc943ef1b929e3b0104b793f386e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3054590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e745120e75bc7923e193b10c4e8c0265f99e9fa3ef78395938673dce9d77985d`

```dockerfile
```

-	Layers:
	-	`sha256:114aca455ec35178c8f14d0e994802740eae3ed394d18526ca89f707e8e65baf`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 3.0 MB (3030509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d7bd56c571b3beb8b86165ddbae02593a922675c8f337d970770cf4d59c30d`  
		Last Modified: Thu, 05 Sep 2024 12:30:50 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json
