## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:4c278b820250d78f6a0494abd063a564aed68bd2d37a67938202970fd7ded473
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:e730ead72d1aceb1020e2422b7a5e929c261f36186e0ccc5314be310b18a1f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305884166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8afb562a3b3db7d92bade70ff123aa9fffd632a8f9890dd6adbd57d9a0f4cd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Wed, 04 Feb 2026 21:10:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Feb 2026 21:10:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Feb 2026 21:10:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e7479438004924167ceb707f9620ee39db7d06870e9ce00d52573350f3518dc4 NEO4J_TARBALL=neo4j-community-5.26.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 04 Feb 2026 21:10:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.21-unix.tar.gz
# Wed, 04 Feb 2026 21:10:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 04 Feb 2026 21:10:19 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 04 Feb 2026 21:10:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.21-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 04 Feb 2026 21:10:38 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 21:10:38 GMT
WORKDIR /var/lib/neo4j
# Wed, 04 Feb 2026 21:10:38 GMT
VOLUME [/data /logs]
# Wed, 04 Feb 2026 21:10:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 04 Feb 2026 21:10:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 21:10:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577146e5c16ba053ac368587fcdad03d65509f320296fd6e9f6e15af74c42893`  
		Last Modified: Wed, 04 Feb 2026 21:11:01 GMT  
		Size: 144.8 MB (144847906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77df731a98e3d3ff15d48968cb7a0ae32db282a206274900b443a7bdbc4121c8`  
		Last Modified: Wed, 04 Feb 2026 21:10:56 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6137ede97fdab27039cae5d2a7017c0eec0ccd32ea00cd85b944f0b4045f1f27`  
		Last Modified: Wed, 04 Feb 2026 21:10:56 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5a0934915585ee02a9ae9d7b53b5218ffaa10c0bb6fbe363df08a74ade45a7`  
		Last Modified: Wed, 04 Feb 2026 21:11:01 GMT  
		Size: 130.8 MB (130763865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:a7f005d923d14980296c5b1ca877a96272f9df24d525efa4e6c1cf65cc8e7309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4500875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beda7196de29ebd643d597298babfb24a879d1215df426ef098d61139e6ad14b`

```dockerfile
```

-	Layers:
	-	`sha256:5988e92e33e3f1579b7d4dec8f0080dfa256f94e9167d6a04c3248d2477dc561`  
		Last Modified: Wed, 04 Feb 2026 21:10:56 GMT  
		Size: 4.5 MB (4479921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd81d84d17a7703756b3d512bc642dd92d6c556c79b2c56568d721b873a64d88`  
		Last Modified: Wed, 04 Feb 2026 21:10:56 GMT  
		Size: 21.0 KB (20954 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3567737ae96e91abc9bb62f4a9dcdc9df2dcfabaaa07753f9f83564509e79030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302446756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d99397d1b22ba5f8dddddc31a0a0238d40c028a7747df70f80b4362dab03b82`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Wed, 04 Feb 2026 21:08:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Feb 2026 21:08:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Feb 2026 21:08:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e7479438004924167ceb707f9620ee39db7d06870e9ce00d52573350f3518dc4 NEO4J_TARBALL=neo4j-community-5.26.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 04 Feb 2026 21:08:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.21-unix.tar.gz
# Wed, 04 Feb 2026 21:08:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 04 Feb 2026 21:08:24 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 04 Feb 2026 21:08:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.21-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 04 Feb 2026 21:08:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 21:08:42 GMT
WORKDIR /var/lib/neo4j
# Wed, 04 Feb 2026 21:08:42 GMT
VOLUME [/data /logs]
# Wed, 04 Feb 2026 21:08:42 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 04 Feb 2026 21:08:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 21:08:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef01185f2140b9206b5c98b3501e59db78fd767c7e06fbe8afccfbe9611a5cc`  
		Last Modified: Wed, 04 Feb 2026 21:09:07 GMT  
		Size: 143.7 MB (143679941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950074ddcd82ba21b234f6e44dba3441e5904b7dc593066b4e686d991eab270e`  
		Last Modified: Wed, 04 Feb 2026 21:09:00 GMT  
		Size: 3.9 KB (3878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4c8f38b2bef5077d6aa9fa781d42cec99b5aa330885e1ac410b6f7b24e084a`  
		Last Modified: Wed, 04 Feb 2026 21:09:00 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91184e8561a3ede14c8f5d637794cd6a0b3fa3bab3be2561facea8c90604a29`  
		Last Modified: Wed, 04 Feb 2026 21:09:06 GMT  
		Size: 130.0 MB (130008225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:918a60fc96ef9468d3d7e0e6ee06c8eb6d2b0c412ca772c23610bd7824b32194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4474849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef09e6b79d7b62acc4d1d94c64f2693dcef570d07cc5a8c00691586beee4f196`

```dockerfile
```

-	Layers:
	-	`sha256:927125e32054d9007094d8e1619a67ccc9aa74f505e400c7dd984bbb81e5dbe0`  
		Last Modified: Wed, 04 Feb 2026 21:09:00 GMT  
		Size: 4.5 MB (4453726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7174dd2174dcf11a95b97d37b40c9f7bf6ff6f18492b68246930a09096a19ad`  
		Last Modified: Wed, 04 Feb 2026 21:09:00 GMT  
		Size: 21.1 KB (21123 bytes)  
		MIME: application/vnd.in-toto+json
