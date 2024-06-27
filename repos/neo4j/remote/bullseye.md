## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:2357ee27d0b8cedc10fb2e2eb214980643878088cc5c786fa15b3f8e44f41a15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:4f00469bcc43b1c583438ebcba656b158cf6422e0137be3a117088d64e7d644c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306444322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e920913346bf3c90e5ba4467f3b6db212364040123e72ab1bef3b36fbfa883`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:18 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 13 Jun 2024 01:21:18 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072ed23e77c4a338ecf4ff503470ff538c5f9f9cb628a5bdf91903ee8ce84dfa`  
		Last Modified: Thu, 27 Jun 2024 18:55:41 GMT  
		Size: 145.1 MB (145095091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d40d65342fac4cd656d7561c66413b974f8a1ad2f8ba144e20658f459eee1b`  
		Last Modified: Thu, 27 Jun 2024 18:55:39 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4f01c7c15c91a335d54d8f7f9e190cf7ac7c0459f09158e24d666fa90b1cfc`  
		Last Modified: Thu, 27 Jun 2024 18:55:39 GMT  
		Size: 9.6 KB (9631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2727f2e28eb4b3de161bdc825f2e28ad8da43daf783c520a896ea7e66a6ae8ae`  
		Last Modified: Thu, 27 Jun 2024 18:55:41 GMT  
		Size: 129.9 MB (129901689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:485acf792324e6cbb6cc35f20264a1c46a5792c608d75a6e204cc67fc76e949f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd3de0ec8461b88ff3d6613f5cdfdc6e8cb10d9a5c9164efc8a225b23f001a1`

```dockerfile
```

-	Layers:
	-	`sha256:f5823ed8c1d066e537942f82757a32eee2c9e03348a0a1f57528450e3cc71bbb`  
		Last Modified: Thu, 27 Jun 2024 18:55:39 GMT  
		Size: 3.0 MB (2967888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f4aa3b27345b7d669a6eaad831eb67f9e080bc199af577f3cab2c956c46aa80`  
		Last Modified: Thu, 27 Jun 2024 18:55:39 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45ef0824f41a2bab0e196558cd1e7164beea9fbe0df92d615af786a38cb71ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303863095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee200c8e1e14b4820c7f7581fe671e284f29ac9d3ac6d87c49cc5dff1120763`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850f5fd6366e203f151cb710c3418988466ec7f9b017c10a7045867888f139a`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddc5ce8cbef080759ac3c765ae521faf252b845604fa7e5a3a51570ab227760`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1aeea181ee9c08b81c8ade6a2985db100e1836fb04b069713a5816940a1e43`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 129.9 MB (129869805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:93a8a2d0e5392e4f7d8cb946f26f73bcc957c092d6cce446034c3c2666c5fc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e858c0c551e72940b6e7f679bac9b624e92374330419c5696caa2f35e7d398`

```dockerfile
```

-	Layers:
	-	`sha256:2c83f7504793d2e59e4a6ef33303ac8dbec01f0278bded96378d6f677162ef80`  
		Last Modified: Thu, 27 Jun 2024 18:55:55 GMT  
		Size: 3.0 MB (2968295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09edd92520917eb4cec7bc6a55f9cd219ed82095a4659056a5fec7e227ed1c8`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json
