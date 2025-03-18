## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:f136835f6ccf96bb90eca84942cfc629780958c12f7211892e71066f74cb5618
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:34e707f0beb1dfbc63033dded37182a8ff297e99920fbb8c66ca575300e76025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.9 MB (625872266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a1347f0f43681561bb30a3df117cf4d27a799a32a5724b3dbdcfda880ffeb3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 11 Mar 2025 12:43:49 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Tue, 11 Mar 2025 12:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 11 Mar 2025 12:43:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 11 Mar 2025 12:43:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=417eaac39dca242bbf9973bc1a7a0abe38ecb821398c78e910e422e75e89fe07 NEO4J_TARBALL=neo4j-enterprise-5.26.4-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 11 Mar 2025 12:43:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.4-unix.tar.gz
# Tue, 11 Mar 2025 12:43:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.4-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 11 Mar 2025 12:43:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 11 Mar 2025 12:43:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.4-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 11 Mar 2025 12:43:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 12:43:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 11 Mar 2025 12:43:49 GMT
VOLUME [/data /logs]
# Tue, 11 Mar 2025 12:43:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 11 Mar 2025 12:43:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 12:43:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d52269bb5fb66e3627f57c157ada592f7c146aa076f943f68597feecd9be5f`  
		Last Modified: Mon, 17 Mar 2025 23:19:44 GMT  
		Size: 144.6 MB (144566551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45f0afed4315b51225a47813b229c52f4f6f4be7bfa839c3c2cd76b63e34827`  
		Last Modified: Mon, 17 Mar 2025 23:19:42 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b03ca57b3ae90a1e3717424e0abf7ffdb71b9d32aeca374417918d77c3ca4d9`  
		Last Modified: Mon, 17 Mar 2025 23:19:42 GMT  
		Size: 10.0 KB (10030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd859815790511cf8a38adbc4ccc0bd32fadcbe32369bf5e92d980697e1c160`  
		Last Modified: Mon, 17 Mar 2025 23:19:49 GMT  
		Size: 451.0 MB (451037980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:6c8f0659fb062de2ffa3aa036ada8320bbf1f778116b019567886fb820cec3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be20d9c24091edea8a07249212e9d92861d8577438ff3fe8cd836da89edeb59b`

```dockerfile
```

-	Layers:
	-	`sha256:4ccbe68609274ae02b046c99f8b7b8cb5a6671a422a0efe773a6d18e45fd80b7`  
		Last Modified: Mon, 17 Mar 2025 23:19:42 GMT  
		Size: 3.5 MB (3549223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9d46816f89f669fd471f47e9de60e127e64ad49c50d70bf02789a392b534e8d`  
		Last Modified: Mon, 17 Mar 2025 23:19:42 GMT  
		Size: 20.8 KB (20758 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1796521353ac3729e89ab6d0f58f5c5e66d6cc548de9928a55ef9a7642b1a0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.2 MB (623215642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78ea33f6877e5e1b298a6551c6d7b0d07cf900ceeb20776fc3dc19ccc9e8650`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 11 Mar 2025 12:43:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Tue, 11 Mar 2025 12:43:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 11 Mar 2025 12:43:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 11 Mar 2025 12:43:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=417eaac39dca242bbf9973bc1a7a0abe38ecb821398c78e910e422e75e89fe07 NEO4J_TARBALL=neo4j-enterprise-5.26.4-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 11 Mar 2025 12:43:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.4-unix.tar.gz
# Tue, 11 Mar 2025 12:43:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.4-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 11 Mar 2025 12:43:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 11 Mar 2025 12:43:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.4-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 11 Mar 2025 12:43:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 12:43:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 11 Mar 2025 12:43:49 GMT
VOLUME [/data /logs]
# Tue, 11 Mar 2025 12:43:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 11 Mar 2025 12:43:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 11 Mar 2025 12:43:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4714185560a3e233c84e342c5acf31dfcaa7f6f2b630be407160545cce8ab643`  
		Last Modified: Mon, 17 Mar 2025 23:58:19 GMT  
		Size: 143.5 MB (143454543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d360ee792446f6f01f33f3b0d751f3be5e97f88ebcec20a10f9c999f5381cc2`  
		Last Modified: Tue, 18 Mar 2025 03:50:29 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4ee851d5eee6f24b399bea431b6569d37db3d38481a5d24c4d236bdf826aa8`  
		Last Modified: Tue, 18 Mar 2025 03:50:29 GMT  
		Size: 10.0 KB (10030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3c81cb6bc247e7eec7ab5f104cbfdf808261c47dc2795169e8d024df9ba243`  
		Last Modified: Tue, 18 Mar 2025 03:50:38 GMT  
		Size: 451.0 MB (451001250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:c46134c062235d60039b25baf3a72e467a1857dc562a3f8265bec89d47770fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ba0b255a6a783fd5a6dd37d77e81440cc19a0cf99332c090125bdabb2d97db`

```dockerfile
```

-	Layers:
	-	`sha256:87c8c4b0700ef369f970531f7af5eae50b6d60f3139691ef6ffd2c09454d9fff`  
		Last Modified: Tue, 18 Mar 2025 03:50:29 GMT  
		Size: 3.5 MB (3548893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d0075676b0a59cd638f728a2102f508035d5df02617ebd51e564bb6c91d89ec`  
		Last Modified: Tue, 18 Mar 2025 03:50:29 GMT  
		Size: 20.9 KB (20927 bytes)  
		MIME: application/vnd.in-toto+json
