## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:62e406591dfdf7f71d0e5fcee5ab79c121e2cf8c941aa8e2ed9ca5968ccf9983
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:af4dda07b9c26a06c31612fa6061fabc18d976416c142d40cf83fa9e8890805a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **550.8 MB (550757497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413e7f3ab03ce674fbbe76e0c2755d6c16c4681abfe955e72998d240adb020ab`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 21:47:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 21:47:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 21:47:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=aa53a477a26c7392cdaa8f057a87c353eed9ebc4883b9991b23fada6344626dc NEO4J_TARBALL=neo4j-enterprise-2025.12.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 16 Jan 2026 21:47:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.12.1-unix.tar.gz
# Fri, 16 Jan 2026 21:47:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.12.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 16 Jan 2026 21:47:23 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 16 Jan 2026 21:47:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.12.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 16 Jan 2026 21:47:56 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:47:56 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jan 2026 21:47:56 GMT
VOLUME [/data /logs]
# Fri, 16 Jan 2026 21:47:56 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 16 Jan 2026 21:47:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:47:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56bb913fa66be3b4a2750f83f5f8caf28868019ab01676d975285f4fb0e725f`  
		Last Modified: Fri, 16 Jan 2026 21:48:28 GMT  
		Size: 157.8 MB (157826054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a643009bfad6c725dd037e70a5274ffe0aba97f33338292c9dfb70118fa19cd7`  
		Last Modified: Fri, 16 Jan 2026 21:48:22 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc70053a80e85f24f26319e247664a21e579775116a52f0ba5fe906e3fc55408`  
		Last Modified: Fri, 16 Jan 2026 21:48:22 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1383e2ef459004dd0e7e154d3fe460dd6bcf15721ac676979dcb5e92b6beb92`  
		Last Modified: Fri, 16 Jan 2026 21:48:31 GMT  
		Size: 362.7 MB (362659054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:6c2909d0a3293f450d5c9798d3cfc60f69245ffe56fbdc19975fc38b0da0657b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4871534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a84a27181fae4f0123e732be3a3321e9e1770dbf397704f73134630cf26ce6`

```dockerfile
```

-	Layers:
	-	`sha256:e81452e48c79bf463f82904830bcfb9af9c45ad278eef535efda3209cc818a30`  
		Last Modified: Fri, 16 Jan 2026 21:48:23 GMT  
		Size: 4.8 MB (4849873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cb4cd47c1fdbc4e62e9a57ac98a7e5dd8ac5eee32c87f83086ac748902f4e46`  
		Last Modified: Fri, 16 Jan 2026 21:48:22 GMT  
		Size: 21.7 KB (21661 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0bd0a871b4d2c971f4fed236d0cb44d907a84bbfac76632a44a82677d7c932a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.8 MB (546772930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da99b1b826d670597f826ca7a9a2c829e697325deeb0637e5afab27c84842a2b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 21:47:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 21:47:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 21:47:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=aa53a477a26c7392cdaa8f057a87c353eed9ebc4883b9991b23fada6344626dc NEO4J_TARBALL=neo4j-enterprise-2025.12.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 16 Jan 2026 21:47:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.12.1-unix.tar.gz
# Fri, 16 Jan 2026 21:47:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.12.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 16 Jan 2026 21:47:24 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 16 Jan 2026 21:47:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.12.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 16 Jan 2026 21:47:56 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:47:56 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jan 2026 21:47:56 GMT
VOLUME [/data /logs]
# Fri, 16 Jan 2026 21:47:56 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 16 Jan 2026 21:47:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:47:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ab4d9b81445de870027b2a0f3c2632f32ba27583109b8b95a796ca05e65ada`  
		Last Modified: Fri, 16 Jan 2026 21:48:29 GMT  
		Size: 156.1 MB (156107648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680607a82e63002ac206eb5fb5aee4b8b4c333c44ac28f26e39347477f3ab96a`  
		Last Modified: Fri, 16 Jan 2026 21:48:23 GMT  
		Size: 3.9 KB (3876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3199d423f1d902d558f53bb693ab3f4320a00e7763f0814b924eba30208959`  
		Last Modified: Fri, 16 Jan 2026 21:48:23 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b894ad4942a598f5f4ef728dbb6432ca79ac77bd9b075587f49290fb81e0aba`  
		Last Modified: Fri, 16 Jan 2026 21:48:33 GMT  
		Size: 361.9 MB (361902835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5b7b6f097e55a81dac34ece96619a0ef03e561e23870a2082fb4c8d0813b2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4845556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf09e2d7c5a4d02f59bf567a6770eb4635c9aeb8420bc98a7517c31b0132df56`

```dockerfile
```

-	Layers:
	-	`sha256:9247850ffe9b826989d477deac38782a2ede07889d432015578c755767e19cde`  
		Last Modified: Fri, 16 Jan 2026 21:48:23 GMT  
		Size: 4.8 MB (4823702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc38796a66ff5e100def07fb336c409cba9ad1d4fdf4d101923023241f180d36`  
		Last Modified: Fri, 16 Jan 2026 21:48:23 GMT  
		Size: 21.9 KB (21854 bytes)  
		MIME: application/vnd.in-toto+json
