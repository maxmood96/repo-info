## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:71a57c542d3b23aca378bfeb57b6ff0f57530c3e250468d0c3c907d276f9e701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:4950bd6777645beb6b99a38c14f60e484b83d2efb423e4dc89b057ead176c583
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291851040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e6f737ba0b7dd3f55029731f9c38bef70f0bcc69cb0cd4c945b2ab445c0bf2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 14:06:55 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Sat, 16 Dec 2023 14:06:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 16 Dec 2023 14:06:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Sat, 16 Dec 2023 14:06:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 16 Dec 2023 14:06:58 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 16 Dec 2023 14:07:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Sat, 16 Dec 2023 14:07:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 14:07:36 GMT
WORKDIR /var/lib/neo4j
# Sat, 16 Dec 2023 14:07:36 GMT
VOLUME [/data /logs]
# Sat, 16 Dec 2023 14:07:36 GMT
EXPOSE 7473 7474 7687
# Sat, 16 Dec 2023 14:07:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 14:07:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d14040669239de7bca2344d0124913a16ae7c1d2b4c9c7fd78bed42344683be`  
		Last Modified: Sat, 16 Dec 2023 14:10:12 GMT  
		Size: 144.9 MB (144873945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a5d430ce39b0b3a4d8607e4de1b606946161f0eb70fb300ea6b08224e2faa1`  
		Last Modified: Sat, 16 Dec 2023 14:10:00 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059ca9b2608dde652e2bae15a8e3947e3be3732d4db1bfdcd42a69eaf13223b4`  
		Last Modified: Sat, 16 Dec 2023 14:10:00 GMT  
		Size: 9.5 KB (9493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de341ef29672637a0bfe5a0faf6755d984f86b6cf87b6f89febbec08ba8e9345`  
		Last Modified: Sat, 16 Dec 2023 14:10:06 GMT  
		Size: 115.5 MB (115545918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:66bf192665955f5e398d5da721a575191005377ecf354f30f5ed42bc54020ee2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc9a6d9e7214384cee95606d66e28480857c28978bb0d2dccd7ed9ecc6dc29d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:00:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 03:00:20 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Tue, 19 Dec 2023 03:00:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 19 Dec 2023 03:00:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Tue, 19 Dec 2023 03:00:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 19 Dec 2023 03:00:24 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Tue, 19 Dec 2023 03:00:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Tue, 19 Dec 2023 03:00:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 03:00:52 GMT
WORKDIR /var/lib/neo4j
# Tue, 19 Dec 2023 03:00:53 GMT
VOLUME [/data /logs]
# Tue, 19 Dec 2023 03:00:53 GMT
EXPOSE 7473 7474 7687
# Tue, 19 Dec 2023 03:00:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 03:00:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80ad0f784bba75d76206ff4e1034310f072851273c25fd54ef00422a8861cef`  
		Last Modified: Tue, 19 Dec 2023 03:03:38 GMT  
		Size: 143.7 MB (143681709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222dbafa0cda84f50943c99b556276e5aa261b63b5dc78cfb5d729541579cf2d`  
		Last Modified: Tue, 19 Dec 2023 03:03:29 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7e7ec7f9ba78c43ab910762422b4f227f37d23b20e272e21f40827c8b9eb38`  
		Last Modified: Tue, 19 Dec 2023 03:03:29 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ef8ca987d90671e3effd1c997328b06e56b01f084196272853273acfee6e47`  
		Last Modified: Tue, 19 Dec 2023 03:03:34 GMT  
		Size: 115.5 MB (115515799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
