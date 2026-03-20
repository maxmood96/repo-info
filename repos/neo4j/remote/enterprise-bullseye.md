## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:0ff3c4dc3b0476ddcd4085f3931380dda4b7301a4169759117e164ac73525287
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:ceaf5c02c401edc2e77a667e18e3c27227394ccb93e43793dd361cf4721ea32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.9 MB (574947305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8b6d824aa7dd0585cf2cc7a5aba89a5272df71625282859e66471794ecc083`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Fri, 20 Mar 2026 17:48:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Mar 2026 17:48:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 20 Mar 2026 17:48:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0587f264954dfea33cfec36f442c8aca5156a5db6fbca73d3a3c2523130d2408 NEO4J_TARBALL=neo4j-enterprise-2026.02.3-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 20 Mar 2026 17:48:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.02.3-unix.tar.gz
# Fri, 20 Mar 2026 17:48:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.02.3-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 20 Mar 2026 17:48:52 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 20 Mar 2026 17:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.02.3-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 20 Mar 2026 17:49:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 17:49:17 GMT
WORKDIR /var/lib/neo4j
# Fri, 20 Mar 2026 17:49:17 GMT
VOLUME [/data /logs]
# Fri, 20 Mar 2026 17:49:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 20 Mar 2026 17:49:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 20 Mar 2026 17:49:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf7edebd397e1291344bce46309969dae493a159366caccf95fccf8c1c1e8b1`  
		Last Modified: Fri, 20 Mar 2026 17:49:51 GMT  
		Size: 157.9 MB (157857092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c754e65adc88b7adb05a0f3835460d95f3baf524d80d46013680990eb0afcd`  
		Last Modified: Fri, 20 Mar 2026 17:49:45 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164f091ba5f9484c2dadbad7c0021171afbd0a32bc57cb49d908c07294291ded`  
		Last Modified: Fri, 20 Mar 2026 17:49:45 GMT  
		Size: 10.2 KB (10191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd12c5aca855239c511277039adf2c31c3d570754547370761507b071b1c4def`  
		Last Modified: Fri, 20 Mar 2026 17:49:56 GMT  
		Size: 386.8 MB (386818324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2e5f4ca9b4456bbd9e12ddd0f7c824b0c73dd8fcbe93429470c590d9a34d7d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4902693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b7a9e9bac95f84ce6d07529dab57593116a955e340936c22a598e39760bb49`

```dockerfile
```

-	Layers:
	-	`sha256:2eff533f90e878d3285c634ea70e8b5b9bb96dad200d3d7a38c379dd7c13badd`  
		Last Modified: Fri, 20 Mar 2026 17:49:45 GMT  
		Size: 4.9 MB (4882294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53cc6d511ee2c56a6f6c3273aefe8e21d30098a97c1eb1be6a288dc62bcf1712`  
		Last Modified: Fri, 20 Mar 2026 17:49:44 GMT  
		Size: 20.4 KB (20399 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ba93ee8a448f6979851507d5ccfe287ddd9fc4a22b09402e5e608ceb17c58e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.0 MB (570955965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6cc3ff41c4e4f8c3f04e17a5dd5d69e578d78b17ea78284790a4dd868433ff`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Fri, 20 Mar 2026 17:50:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Mar 2026 17:50:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 20 Mar 2026 17:50:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0587f264954dfea33cfec36f442c8aca5156a5db6fbca73d3a3c2523130d2408 NEO4J_TARBALL=neo4j-enterprise-2026.02.3-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 20 Mar 2026 17:50:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.02.3-unix.tar.gz
# Fri, 20 Mar 2026 17:51:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.02.3-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 20 Mar 2026 17:51:31 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 20 Mar 2026 17:51:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.02.3-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 20 Mar 2026 17:51:54 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 17:51:54 GMT
WORKDIR /var/lib/neo4j
# Fri, 20 Mar 2026 17:51:54 GMT
VOLUME [/data /logs]
# Fri, 20 Mar 2026 17:51:54 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 20 Mar 2026 17:51:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 20 Mar 2026 17:51:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce92e01bcf0466d97a38e2121d97a0359350c8baf3d2f0a26de9c621a73f808`  
		Last Modified: Fri, 20 Mar 2026 17:51:20 GMT  
		Size: 156.1 MB (156133028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d329411ebb17903bcd2ed4dc6a052523ee457488ac2a2d3df0409a7217009f53`  
		Last Modified: Fri, 20 Mar 2026 17:52:20 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1929d5c29c38888a5dbdbec9cdd2f19c477b204eb4d0c0543912ba49dacf76de`  
		Last Modified: Fri, 20 Mar 2026 17:52:20 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a757ef0f730fa878f950877d7b5f4d4545b6f8b9dc4de570d8b0cb9f61f7b4f`  
		Last Modified: Fri, 20 Mar 2026 17:52:28 GMT  
		Size: 386.1 MB (386064321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:6cb6736761a5a6992ecd01a33e9dae5a023df79b6b0e6b27286e06f49f47d809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4876619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d18877796f0fe86c8512e33f1287bcef0028af8e9aee2d343998ac9d1c8b74`

```dockerfile
```

-	Layers:
	-	`sha256:6c7dc01b43fe946c8fc77fe499982993c16d81b30027faf8c3ea361570d1446a`  
		Last Modified: Fri, 20 Mar 2026 17:52:20 GMT  
		Size: 4.9 MB (4856075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf31b4e18fe524382fc859d79e599d54f199085268ab8e8b0604619b37563b46`  
		Last Modified: Fri, 20 Mar 2026 17:52:20 GMT  
		Size: 20.5 KB (20544 bytes)  
		MIME: application/vnd.in-toto+json
