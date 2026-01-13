## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:cbca9e5ca0808c4629882f684e7abe452e0cec23d53a5e2778db90138870ec9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:092e3ddd7d66bf7c3d1495f750fc18304d9833cdd5c65bc6c737a0eeaf14da3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.4 MB (403370451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e17a4509b31b350bb5720b882da97f49d23cace7307790419cfaeeebb52a93`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:27:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 02:27:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 02:27:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0b9b8155d366ae64ed7c21e208b42be15da231c2f8040f9f745885aab43ee76a NEO4J_TARBALL=neo4j-community-2025.11.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 13 Jan 2026 02:27:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.11.2-unix.tar.gz
# Tue, 13 Jan 2026 02:27:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.11.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 13 Jan 2026 02:27:24 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 13 Jan 2026 02:27:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.11.2-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 13 Jan 2026 02:27:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:27:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Jan 2026 02:27:50 GMT
VOLUME [/data /logs]
# Tue, 13 Jan 2026 02:27:50 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 13 Jan 2026 02:27:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:27:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f2da96b7de746ba174dab2a39ed6389e7e90314f090ff0cd1b0e2022fd62b0`  
		Last Modified: Tue, 13 Jan 2026 02:28:37 GMT  
		Size: 157.8 MB (157826031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c922f4af6a454abbe16a9eb28f7677bf248608d82045cf5b200b165aaea7cd`  
		Last Modified: Tue, 13 Jan 2026 02:28:27 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae279c22cf96f29d3c299f9a022312538cb0c72f3d8ea013c21ff4ba309315e`  
		Last Modified: Tue, 13 Jan 2026 02:28:26 GMT  
		Size: 10.0 KB (10022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72c5de8bdc42aa6eab750bc1f868732cfdfad50bfc98532f1588e4e822012b7`  
		Last Modified: Tue, 13 Jan 2026 02:28:37 GMT  
		Size: 215.3 MB (215272032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:73d80e539f0d8e051c92a837f5586553f5186311c1129744c93cbdadabe3d313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4634353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80918efac5a485f5b61f76e88f90a87fa04d91874efbf37db0c2fd843a772958`

```dockerfile
```

-	Layers:
	-	`sha256:f0c7240da9197703aa2b14020516c1c45bb0f642acbecb9750b4dcb547e1c1c6`  
		Last Modified: Tue, 13 Jan 2026 03:44:15 GMT  
		Size: 4.6 MB (4610287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bef3e94120c886d7fb9e353004558bcb815d85cb3b5ebf6d79dc96815704780`  
		Last Modified: Tue, 13 Jan 2026 03:44:17 GMT  
		Size: 24.1 KB (24066 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc0c15f49c80f6c661cb918c625fbef2cfaf485fd5a2610d772eefb9f155d0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.4 MB (399386118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09725f867feeb3c17e9f278fc55b21053b193405a53434ee4ec21069c08449c6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:31:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 02:31:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 02:31:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0b9b8155d366ae64ed7c21e208b42be15da231c2f8040f9f745885aab43ee76a NEO4J_TARBALL=neo4j-community-2025.11.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 13 Jan 2026 02:31:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.11.2-unix.tar.gz
# Tue, 13 Jan 2026 02:31:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.11.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 13 Jan 2026 02:31:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 13 Jan 2026 02:31:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.11.2-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 13 Jan 2026 02:31:56 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:31:56 GMT
WORKDIR /var/lib/neo4j
# Tue, 13 Jan 2026 02:31:56 GMT
VOLUME [/data /logs]
# Tue, 13 Jan 2026 02:31:56 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 13 Jan 2026 02:31:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:31:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8743a5370cc44b3339f70515bd8cc86f8b26c8ac2b8049da722adcd5d8bf6325`  
		Last Modified: Tue, 13 Jan 2026 02:32:50 GMT  
		Size: 156.1 MB (156107580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61507fe8d4877dd129011c3e42551ba3bc942e1200c3208f4e34612c23bb9f86`  
		Last Modified: Tue, 13 Jan 2026 02:32:31 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e8df99df86e804c7eb6b44fc58c2b4812b41976dc7ac121ab904ffa1afdae4`  
		Last Modified: Tue, 13 Jan 2026 02:32:31 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a5599ce4f25db746876ce50223dd9cccd7b43408ba079172b5dff3fd2391a0`  
		Last Modified: Tue, 13 Jan 2026 02:33:01 GMT  
		Size: 214.5 MB (214516101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4328aa522da5f95d1b8a5c810962cb0f3d2b1a23b6580a3237954fa2621861e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4608566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7575993eb1a1ab5e3a7a5e734dd29df29d3a282c79f2ab59fd1f8f73a8a580`

```dockerfile
```

-	Layers:
	-	`sha256:edf8d128f8a62b08942b48ff11b23020e73797c1abd06d7db9443e650d6f402c`  
		Last Modified: Tue, 13 Jan 2026 03:44:23 GMT  
		Size: 4.6 MB (4584212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:315d1af45d153768c328d1c473fff69bd2faa131db9fe0d252324af3e8f50d55`  
		Last Modified: Tue, 13 Jan 2026 03:44:24 GMT  
		Size: 24.4 KB (24354 bytes)  
		MIME: application/vnd.in-toto+json
