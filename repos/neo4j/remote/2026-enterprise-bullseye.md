## `neo4j:2026-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:571976b56c352d56ca564f0dde1756d8618d809ebfcc576c1ce6ffc664a50114
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:79586f053c95602b2654ddf40c4a8a56ac57f9d83743b84d2cd39cd432f17772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.5 MB (553523304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa72d88ef35eaee3c2237857a07dd1ba4efddfc2b5f739abbf7c68f51805bd80`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Wed, 04 Feb 2026 21:10:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Feb 2026 21:10:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Feb 2026 21:10:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3326a905d4accc1bdd224923a6d30c9a498bbd0fb7b43e87983aec29734c367d NEO4J_TARBALL=neo4j-enterprise-2026.01.3-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 04 Feb 2026 21:10:11 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
# Wed, 04 Feb 2026 21:10:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 04 Feb 2026 21:10:12 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 04 Feb 2026 21:10:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 04 Feb 2026 21:10:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 21:10:37 GMT
WORKDIR /var/lib/neo4j
# Wed, 04 Feb 2026 21:10:37 GMT
VOLUME [/data /logs]
# Wed, 04 Feb 2026 21:10:37 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 04 Feb 2026 21:10:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 21:10:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d158efa041c19f95682fe5983a07a0f0a2e30d41ea6c5ca5bb6fd1b6980ca6f3`  
		Last Modified: Wed, 04 Feb 2026 21:11:08 GMT  
		Size: 157.8 MB (157826002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1cc3fd8b7d748bde0f4e6a3068bde77edd2a3763ab299ff8802455d71a1f0c`  
		Last Modified: Wed, 04 Feb 2026 21:11:02 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d64fa110d70b29d29eec4adcc116307129587fca62eb9cf14675aa4f20e388`  
		Last Modified: Wed, 04 Feb 2026 21:11:02 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b337cf90985ba15a4a67d715434c4c6448a01765a25ea1d7b63f48e6c7e5cce6`  
		Last Modified: Wed, 04 Feb 2026 21:11:12 GMT  
		Size: 365.4 MB (365424954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ee3a176cfde0483e2b05868677a44591c768c02549f1d0c67602d18347fcf007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4875922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a41c96fccd9f46116a8908866bd71ca757f00a06bbcf3bd7a9fedbceb16ccd95`

```dockerfile
```

-	Layers:
	-	`sha256:7721dd0cc7620c5e7815dbe7db6ec655b39a78930091510111cd4b614718c7ee`  
		Last Modified: Wed, 04 Feb 2026 21:11:03 GMT  
		Size: 4.9 MB (4855523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7a600107e776a7481a7c4568f4770047eef427ad1c4a5185b0926fefda2e6c6`  
		Last Modified: Wed, 04 Feb 2026 21:11:02 GMT  
		Size: 20.4 KB (20399 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f9733291e9265561e7b0c016535a2979e6358a118c85510ba17c5b211102c412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.5 MB (549536544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baba93e89c9bf73958c31ef0718716b1517d5e567820d585d58b779a76d83d45`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Wed, 04 Feb 2026 21:08:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Feb 2026 21:08:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Feb 2026 21:08:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3326a905d4accc1bdd224923a6d30c9a498bbd0fb7b43e87983aec29734c367d NEO4J_TARBALL=neo4j-enterprise-2026.01.3-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 04 Feb 2026 21:08:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
# Wed, 04 Feb 2026 21:08:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 04 Feb 2026 21:08:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 04 Feb 2026 21:08:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 04 Feb 2026 21:08:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 21:08:41 GMT
WORKDIR /var/lib/neo4j
# Wed, 04 Feb 2026 21:08:41 GMT
VOLUME [/data /logs]
# Wed, 04 Feb 2026 21:08:41 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 04 Feb 2026 21:08:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 21:08:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67702c678c31d3c3f8dbc675850d5a7abef6f4dfff1589573d59703216dcd449`  
		Last Modified: Wed, 04 Feb 2026 21:09:06 GMT  
		Size: 156.1 MB (156107672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a98c5971654a1f625cd6fdf72a9a14978308b9670262da7d034c3b6c60d959`  
		Last Modified: Wed, 04 Feb 2026 21:09:08 GMT  
		Size: 3.9 KB (3875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07395edf3672222b1cb98580ddfac3623b826e90fcf2fd27b4f3fd52d700e372`  
		Last Modified: Wed, 04 Feb 2026 21:09:08 GMT  
		Size: 10.2 KB (10190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6cc6f577232304f4bfd7a7b021106470e3efee547255002841301a2916afe3`  
		Last Modified: Wed, 04 Feb 2026 21:09:21 GMT  
		Size: 364.7 MB (364670336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e4c3e6274aa2de8bcfbeb9008be4b2f1c3572e91a32ac01057578ab670bb9672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4849847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d124ea156e77c573d796ff7c0db842f414f02f4c59f84ea875be5ddce6e70014`

```dockerfile
```

-	Layers:
	-	`sha256:36776c5a8b2b5fbd7bc57581368987963ee8c83af43a6edb00437a3c8f560e17`  
		Last Modified: Wed, 04 Feb 2026 21:09:08 GMT  
		Size: 4.8 MB (4829304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b19bfb5e0cf517f86e92e464b1033141dc22f2d66b34c2456afc571df95d26c0`  
		Last Modified: Wed, 04 Feb 2026 21:09:07 GMT  
		Size: 20.5 KB (20543 bytes)  
		MIME: application/vnd.in-toto+json
