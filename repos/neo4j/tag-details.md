<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.29`](#neo4j4429)
-	[`neo4j:4.4.29-community`](#neo4j4429-community)
-	[`neo4j:4.4.29-enterprise`](#neo4j4429-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-bullseye`](#neo4j5-bullseye)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-community-bullseye`](#neo4j5-community-bullseye)
-	[`neo4j:5-community-ubi8`](#neo4j5-community-ubi8)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5-enterprise-bullseye`](#neo4j5-enterprise-bullseye)
-	[`neo4j:5-enterprise-ubi8`](#neo4j5-enterprise-ubi8)
-	[`neo4j:5-ubi8`](#neo4j5-ubi8)
-	[`neo4j:5.15`](#neo4j515)
-	[`neo4j:5.15-bullseye`](#neo4j515-bullseye)
-	[`neo4j:5.15-community`](#neo4j515-community)
-	[`neo4j:5.15-community-bullseye`](#neo4j515-community-bullseye)
-	[`neo4j:5.15-community-ubi8`](#neo4j515-community-ubi8)
-	[`neo4j:5.15-enterprise`](#neo4j515-enterprise)
-	[`neo4j:5.15-enterprise-bullseye`](#neo4j515-enterprise-bullseye)
-	[`neo4j:5.15-enterprise-ubi8`](#neo4j515-enterprise-ubi8)
-	[`neo4j:5.15-ubi8`](#neo4j515-ubi8)
-	[`neo4j:5.15.0`](#neo4j5150)
-	[`neo4j:5.15.0-bullseye`](#neo4j5150-bullseye)
-	[`neo4j:5.15.0-community`](#neo4j5150-community)
-	[`neo4j:5.15.0-community-bullseye`](#neo4j5150-community-bullseye)
-	[`neo4j:5.15.0-community-ubi8`](#neo4j5150-community-ubi8)
-	[`neo4j:5.15.0-enterprise`](#neo4j5150-enterprise)
-	[`neo4j:5.15.0-enterprise-bullseye`](#neo4j5150-enterprise-bullseye)
-	[`neo4j:5.15.0-enterprise-ubi8`](#neo4j5150-enterprise-ubi8)
-	[`neo4j:5.15.0-ubi8`](#neo4j5150-ubi8)
-	[`neo4j:bullseye`](#neo4jbullseye)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:community-bullseye`](#neo4jcommunity-bullseye)
-	[`neo4j:community-ubi8`](#neo4jcommunity-ubi8)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:enterprise-bullseye`](#neo4jenterprise-bullseye)
-	[`neo4j:enterprise-ubi8`](#neo4jenterprise-ubi8)
-	[`neo4j:latest`](#neo4jlatest)
-	[`neo4j:ubi8`](#neo4jubi8)

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:786a008e8e2b64ea39302d33c8afe78f11f52ca1e6b201dc99fec8a8adf94a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:19a51cae3302bf22f4a7e459db107419e24e5d4cfdf906aa715a190ebbf73a5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297255819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8588ea95b2a8a09459acd6522e84ff438aa012ae39512a6b5d5d8ff60f0b3517`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:59:46 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:09:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9aa9af96f80388581f626d9e4b8b4c0f467aefbcac3ea7d9c8cd68025067d076 NEO4J_TARBALL=neo4j-community-4.4.29-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:09:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
# Thu, 11 Jan 2024 06:09:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:09:13 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 11 Jan 2024 06:09:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:09:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:09:44 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:09:44 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:09:45 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:09:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:09:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b73066ba82716b83b2f778c5be1f8d952d9952a3fe0c473dea2bf497f35bbb`  
		Last Modified: Thu, 11 Jan 2024 05:18:40 GMT  
		Size: 145.3 MB (145266337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9cf38d5eb9240e1ee64237ab85eded9252a6f5dcbf82d7240131c6df07e1fc1`  
		Last Modified: Thu, 11 Jan 2024 06:12:11 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ba10e7ad99fc6d8c530ec9493faac7d1ca5dadabf63fd3d8409e8b52952fcf`  
		Last Modified: Thu, 11 Jan 2024 06:12:11 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece77c018cf36cfaf351d09a4d126918042b1d9c024b4379a770b8b4390eb912`  
		Last Modified: Thu, 11 Jan 2024 06:12:17 GMT  
		Size: 120.6 MB (120558255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:980efc0767035583bb06c45c0f88fe53bf654c5889caf0f9432fc88f8e646ee1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292604827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce6637254521c80387a325c161b21774bdc843d81aa0140588d44ec068dcabf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:23:14 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:23:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9aa9af96f80388581f626d9e4b8b4c0f467aefbcac3ea7d9c8cd68025067d076 NEO4J_TARBALL=neo4j-community-4.4.29-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:23:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
# Thu, 11 Jan 2024 06:23:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:23:18 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 11 Jan 2024 06:23:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:23:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:23:40 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:23:40 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:23:40 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:23:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:23:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2512ad494dc6647b15f05fa5d740eddc1f4e45014c47ec0d2067bc790ed15fc9`  
		Last Modified: Thu, 11 Jan 2024 06:26:12 GMT  
		Size: 142.0 MB (142001836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3cd86e81d517dd2a5e08dff680460e9cdecae51b8a71b3b7da51aab0ad5d77`  
		Last Modified: Thu, 11 Jan 2024 06:26:03 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51c74a9b928afe705953d431530cabdde8bcd0d8c803234f482e11dfc972403`  
		Last Modified: Thu, 11 Jan 2024 06:26:03 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b520507ca27260333d1f73f6e8162a477987c85ca515091de7d8b8ddc4a66b`  
		Last Modified: Thu, 11 Jan 2024 06:26:08 GMT  
		Size: 120.5 MB (120525677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:786a008e8e2b64ea39302d33c8afe78f11f52ca1e6b201dc99fec8a8adf94a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:19a51cae3302bf22f4a7e459db107419e24e5d4cfdf906aa715a190ebbf73a5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297255819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8588ea95b2a8a09459acd6522e84ff438aa012ae39512a6b5d5d8ff60f0b3517`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:59:46 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:09:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9aa9af96f80388581f626d9e4b8b4c0f467aefbcac3ea7d9c8cd68025067d076 NEO4J_TARBALL=neo4j-community-4.4.29-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:09:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
# Thu, 11 Jan 2024 06:09:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:09:13 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 11 Jan 2024 06:09:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:09:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:09:44 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:09:44 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:09:45 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:09:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:09:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b73066ba82716b83b2f778c5be1f8d952d9952a3fe0c473dea2bf497f35bbb`  
		Last Modified: Thu, 11 Jan 2024 05:18:40 GMT  
		Size: 145.3 MB (145266337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9cf38d5eb9240e1ee64237ab85eded9252a6f5dcbf82d7240131c6df07e1fc1`  
		Last Modified: Thu, 11 Jan 2024 06:12:11 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ba10e7ad99fc6d8c530ec9493faac7d1ca5dadabf63fd3d8409e8b52952fcf`  
		Last Modified: Thu, 11 Jan 2024 06:12:11 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece77c018cf36cfaf351d09a4d126918042b1d9c024b4379a770b8b4390eb912`  
		Last Modified: Thu, 11 Jan 2024 06:12:17 GMT  
		Size: 120.6 MB (120558255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:980efc0767035583bb06c45c0f88fe53bf654c5889caf0f9432fc88f8e646ee1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292604827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce6637254521c80387a325c161b21774bdc843d81aa0140588d44ec068dcabf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:23:14 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:23:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9aa9af96f80388581f626d9e4b8b4c0f467aefbcac3ea7d9c8cd68025067d076 NEO4J_TARBALL=neo4j-community-4.4.29-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:23:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
# Thu, 11 Jan 2024 06:23:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:23:18 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 11 Jan 2024 06:23:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:23:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:23:40 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:23:40 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:23:40 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:23:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:23:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2512ad494dc6647b15f05fa5d740eddc1f4e45014c47ec0d2067bc790ed15fc9`  
		Last Modified: Thu, 11 Jan 2024 06:26:12 GMT  
		Size: 142.0 MB (142001836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3cd86e81d517dd2a5e08dff680460e9cdecae51b8a71b3b7da51aab0ad5d77`  
		Last Modified: Thu, 11 Jan 2024 06:26:03 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51c74a9b928afe705953d431530cabdde8bcd0d8c803234f482e11dfc972403`  
		Last Modified: Thu, 11 Jan 2024 06:26:03 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b520507ca27260333d1f73f6e8162a477987c85ca515091de7d8b8ddc4a66b`  
		Last Modified: Thu, 11 Jan 2024 06:26:08 GMT  
		Size: 120.5 MB (120525677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:69d17855bcbe138a013da8a5d0d43e4efb803502150c1860d7f001f0002dc1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:6a8ba18585fa4706d734591f81434743519b5c9bfb9e0bd784884fcee3fcb891
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.3 MB (402296124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bed7811db97a328444f4286b48e1ebcb36d160516c98529d49a2c3994d5a58c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:59:46 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:09:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ec65a14a4e43c03a7fc1c6b1bf573cc91ec0d6bd527b183ffbf3f6f5386b120b NEO4J_TARBALL=neo4j-enterprise-4.4.29-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:09:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
# Thu, 11 Jan 2024 06:09:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:09:54 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 11 Jan 2024 06:10:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:10:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:10:31 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:10:31 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:10:31 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:10:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:10:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b73066ba82716b83b2f778c5be1f8d952d9952a3fe0c473dea2bf497f35bbb`  
		Last Modified: Thu, 11 Jan 2024 05:18:40 GMT  
		Size: 145.3 MB (145266337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541dc0039302c1e41e851031e6f4bea6175d8a1207078d20f60e125341b48235`  
		Last Modified: Thu, 11 Jan 2024 06:12:28 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9d4fa87d4ec8e15dd9ff67924bfa73f8e2099880741a708e790fbe138f2a49`  
		Last Modified: Thu, 11 Jan 2024 06:12:28 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5e6c1d6752dbe07817074cd66d692e206ab5eca535cb58a328ee4f6135234c`  
		Last Modified: Thu, 11 Jan 2024 06:12:38 GMT  
		Size: 225.6 MB (225598556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9a94dcb474875a1a75e5327f0869c58b5b7acf1e4dbaacdea5556541a6385705
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.6 MB (397638421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db8c75bec0c64999efb8daa6519c7e2ad7a8b13e1b154e413fadbd0c9325cf8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:23:14 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:23:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ec65a14a4e43c03a7fc1c6b1bf573cc91ec0d6bd527b183ffbf3f6f5386b120b NEO4J_TARBALL=neo4j-enterprise-4.4.29-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:23:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
# Thu, 11 Jan 2024 06:23:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:23:46 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 11 Jan 2024 06:24:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:24:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:24:12 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:24:12 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:24:12 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:24:12 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:24:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2512ad494dc6647b15f05fa5d740eddc1f4e45014c47ec0d2067bc790ed15fc9`  
		Last Modified: Thu, 11 Jan 2024 06:26:12 GMT  
		Size: 142.0 MB (142001836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b359094a22a05a5ad942b6017b3fd511420a7af1d16253befa60dc22f8a64d87`  
		Last Modified: Thu, 11 Jan 2024 06:26:28 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50189c29015646fcc23583e0c8867fcc67bcba963c34d3ec1323494656b86f1`  
		Last Modified: Thu, 11 Jan 2024 06:26:28 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35a0465442b3441963d808a92ce9def2d20aa9f9ccc7327bb5974d7e20128ec`  
		Last Modified: Thu, 11 Jan 2024 06:26:37 GMT  
		Size: 225.6 MB (225559269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.29`

```console
$ docker pull neo4j@sha256:786a008e8e2b64ea39302d33c8afe78f11f52ca1e6b201dc99fec8a8adf94a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.29` - linux; amd64

```console
$ docker pull neo4j@sha256:19a51cae3302bf22f4a7e459db107419e24e5d4cfdf906aa715a190ebbf73a5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297255819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8588ea95b2a8a09459acd6522e84ff438aa012ae39512a6b5d5d8ff60f0b3517`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:59:46 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:09:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9aa9af96f80388581f626d9e4b8b4c0f467aefbcac3ea7d9c8cd68025067d076 NEO4J_TARBALL=neo4j-community-4.4.29-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:09:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
# Thu, 11 Jan 2024 06:09:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:09:13 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 11 Jan 2024 06:09:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:09:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:09:44 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:09:44 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:09:45 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:09:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:09:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b73066ba82716b83b2f778c5be1f8d952d9952a3fe0c473dea2bf497f35bbb`  
		Last Modified: Thu, 11 Jan 2024 05:18:40 GMT  
		Size: 145.3 MB (145266337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9cf38d5eb9240e1ee64237ab85eded9252a6f5dcbf82d7240131c6df07e1fc1`  
		Last Modified: Thu, 11 Jan 2024 06:12:11 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ba10e7ad99fc6d8c530ec9493faac7d1ca5dadabf63fd3d8409e8b52952fcf`  
		Last Modified: Thu, 11 Jan 2024 06:12:11 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece77c018cf36cfaf351d09a4d126918042b1d9c024b4379a770b8b4390eb912`  
		Last Modified: Thu, 11 Jan 2024 06:12:17 GMT  
		Size: 120.6 MB (120558255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.29` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:980efc0767035583bb06c45c0f88fe53bf654c5889caf0f9432fc88f8e646ee1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292604827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce6637254521c80387a325c161b21774bdc843d81aa0140588d44ec068dcabf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:23:14 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:23:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9aa9af96f80388581f626d9e4b8b4c0f467aefbcac3ea7d9c8cd68025067d076 NEO4J_TARBALL=neo4j-community-4.4.29-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:23:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
# Thu, 11 Jan 2024 06:23:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:23:18 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 11 Jan 2024 06:23:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:23:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:23:40 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:23:40 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:23:40 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:23:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:23:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2512ad494dc6647b15f05fa5d740eddc1f4e45014c47ec0d2067bc790ed15fc9`  
		Last Modified: Thu, 11 Jan 2024 06:26:12 GMT  
		Size: 142.0 MB (142001836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3cd86e81d517dd2a5e08dff680460e9cdecae51b8a71b3b7da51aab0ad5d77`  
		Last Modified: Thu, 11 Jan 2024 06:26:03 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51c74a9b928afe705953d431530cabdde8bcd0d8c803234f482e11dfc972403`  
		Last Modified: Thu, 11 Jan 2024 06:26:03 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b520507ca27260333d1f73f6e8162a477987c85ca515091de7d8b8ddc4a66b`  
		Last Modified: Thu, 11 Jan 2024 06:26:08 GMT  
		Size: 120.5 MB (120525677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.29-community`

```console
$ docker pull neo4j@sha256:786a008e8e2b64ea39302d33c8afe78f11f52ca1e6b201dc99fec8a8adf94a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.29-community` - linux; amd64

```console
$ docker pull neo4j@sha256:19a51cae3302bf22f4a7e459db107419e24e5d4cfdf906aa715a190ebbf73a5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297255819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8588ea95b2a8a09459acd6522e84ff438aa012ae39512a6b5d5d8ff60f0b3517`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:59:46 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:09:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9aa9af96f80388581f626d9e4b8b4c0f467aefbcac3ea7d9c8cd68025067d076 NEO4J_TARBALL=neo4j-community-4.4.29-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:09:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
# Thu, 11 Jan 2024 06:09:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:09:13 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 11 Jan 2024 06:09:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:09:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:09:44 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:09:44 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:09:45 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:09:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:09:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b73066ba82716b83b2f778c5be1f8d952d9952a3fe0c473dea2bf497f35bbb`  
		Last Modified: Thu, 11 Jan 2024 05:18:40 GMT  
		Size: 145.3 MB (145266337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9cf38d5eb9240e1ee64237ab85eded9252a6f5dcbf82d7240131c6df07e1fc1`  
		Last Modified: Thu, 11 Jan 2024 06:12:11 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ba10e7ad99fc6d8c530ec9493faac7d1ca5dadabf63fd3d8409e8b52952fcf`  
		Last Modified: Thu, 11 Jan 2024 06:12:11 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece77c018cf36cfaf351d09a4d126918042b1d9c024b4379a770b8b4390eb912`  
		Last Modified: Thu, 11 Jan 2024 06:12:17 GMT  
		Size: 120.6 MB (120558255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.29-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:980efc0767035583bb06c45c0f88fe53bf654c5889caf0f9432fc88f8e646ee1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292604827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce6637254521c80387a325c161b21774bdc843d81aa0140588d44ec068dcabf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:23:14 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:23:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9aa9af96f80388581f626d9e4b8b4c0f467aefbcac3ea7d9c8cd68025067d076 NEO4J_TARBALL=neo4j-community-4.4.29-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:23:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
# Thu, 11 Jan 2024 06:23:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:23:18 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 11 Jan 2024 06:23:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:23:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:23:40 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:23:40 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:23:40 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:23:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:23:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2512ad494dc6647b15f05fa5d740eddc1f4e45014c47ec0d2067bc790ed15fc9`  
		Last Modified: Thu, 11 Jan 2024 06:26:12 GMT  
		Size: 142.0 MB (142001836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3cd86e81d517dd2a5e08dff680460e9cdecae51b8a71b3b7da51aab0ad5d77`  
		Last Modified: Thu, 11 Jan 2024 06:26:03 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51c74a9b928afe705953d431530cabdde8bcd0d8c803234f482e11dfc972403`  
		Last Modified: Thu, 11 Jan 2024 06:26:03 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b520507ca27260333d1f73f6e8162a477987c85ca515091de7d8b8ddc4a66b`  
		Last Modified: Thu, 11 Jan 2024 06:26:08 GMT  
		Size: 120.5 MB (120525677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.29-enterprise`

```console
$ docker pull neo4j@sha256:69d17855bcbe138a013da8a5d0d43e4efb803502150c1860d7f001f0002dc1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.29-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:6a8ba18585fa4706d734591f81434743519b5c9bfb9e0bd784884fcee3fcb891
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.3 MB (402296124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bed7811db97a328444f4286b48e1ebcb36d160516c98529d49a2c3994d5a58c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:59:46 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:09:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ec65a14a4e43c03a7fc1c6b1bf573cc91ec0d6bd527b183ffbf3f6f5386b120b NEO4J_TARBALL=neo4j-enterprise-4.4.29-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:09:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
# Thu, 11 Jan 2024 06:09:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:09:54 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 11 Jan 2024 06:10:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:10:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:10:31 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:10:31 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:10:31 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:10:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:10:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b73066ba82716b83b2f778c5be1f8d952d9952a3fe0c473dea2bf497f35bbb`  
		Last Modified: Thu, 11 Jan 2024 05:18:40 GMT  
		Size: 145.3 MB (145266337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541dc0039302c1e41e851031e6f4bea6175d8a1207078d20f60e125341b48235`  
		Last Modified: Thu, 11 Jan 2024 06:12:28 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9d4fa87d4ec8e15dd9ff67924bfa73f8e2099880741a708e790fbe138f2a49`  
		Last Modified: Thu, 11 Jan 2024 06:12:28 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5e6c1d6752dbe07817074cd66d692e206ab5eca535cb58a328ee4f6135234c`  
		Last Modified: Thu, 11 Jan 2024 06:12:38 GMT  
		Size: 225.6 MB (225598556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.29-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9a94dcb474875a1a75e5327f0869c58b5b7acf1e4dbaacdea5556541a6385705
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.6 MB (397638421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db8c75bec0c64999efb8daa6519c7e2ad7a8b13e1b154e413fadbd0c9325cf8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:23:14 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:23:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ec65a14a4e43c03a7fc1c6b1bf573cc91ec0d6bd527b183ffbf3f6f5386b120b NEO4J_TARBALL=neo4j-enterprise-4.4.29-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:23:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
# Thu, 11 Jan 2024 06:23:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:23:46 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 11 Jan 2024 06:24:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:24:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:24:12 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:24:12 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:24:12 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:24:12 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:24:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2512ad494dc6647b15f05fa5d740eddc1f4e45014c47ec0d2067bc790ed15fc9`  
		Last Modified: Thu, 11 Jan 2024 06:26:12 GMT  
		Size: 142.0 MB (142001836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b359094a22a05a5ad942b6017b3fd511420a7af1d16253befa60dc22f8a64d87`  
		Last Modified: Thu, 11 Jan 2024 06:26:28 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50189c29015646fcc23583e0c8867fcc67bcba963c34d3ec1323494656b86f1`  
		Last Modified: Thu, 11 Jan 2024 06:26:28 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35a0465442b3441963d808a92ce9def2d20aa9f9ccc7327bb5974d7e20128ec`  
		Last Modified: Thu, 11 Jan 2024 06:26:37 GMT  
		Size: 225.6 MB (225559269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:0a3c9c4eb4cb09bd30ddae5ded33edba2bdaa1d1f263709e3b834fc9040c9d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:2377f4203c56c5b139694c96e7324c78d22befb7a0d5c479baa3539494c1b65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291851185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc8fa1b57980bdf08750d60d432b37508e82d5f9f6a63ac9373e2c5598353f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:07:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:07:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:05 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:06 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05509e4b1c34bdb466397876153ead4ecbdc03389deadbb9b72f758e9841a51`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a316564fdae6d2d92ab40ff74bbd79b03c9837463e521a576eeb1d51ffe14bd7`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffffa9c686d1675f116635f73719a4267f8149f487c624f3dd3fc0d64add3706`  
		Last Modified: Thu, 11 Jan 2024 06:11:02 GMT  
		Size: 115.5 MB (115545976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1fe91b7489538e32154a8cc6388b6bed98806360bd57ea143cf50e6465e6bb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4e6f4de772f3b4c752d7df0f5dc81f54e45dbc474daa0cbe740d01f7f6bdb4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:21:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:21:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:21:55 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:22:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:22:21 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:22:21 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:22:21 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:22:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:22:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af1789ab5680e3789b3db8df3c09f623907aacbc747237e0bfa42437b4e5ed4`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ff6b54382050e5e495f1807b96e890e32936115d55df0892d42b47fb5ad9dc`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acf82b1dfc10fb2132b6abedd93a9b5beed9845fdeddf980134e2b1e69a820e`  
		Last Modified: Thu, 11 Jan 2024 06:24:46 GMT  
		Size: 115.5 MB (115515864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:0a3c9c4eb4cb09bd30ddae5ded33edba2bdaa1d1f263709e3b834fc9040c9d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2377f4203c56c5b139694c96e7324c78d22befb7a0d5c479baa3539494c1b65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291851185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc8fa1b57980bdf08750d60d432b37508e82d5f9f6a63ac9373e2c5598353f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:07:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:07:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:05 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:06 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05509e4b1c34bdb466397876153ead4ecbdc03389deadbb9b72f758e9841a51`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a316564fdae6d2d92ab40ff74bbd79b03c9837463e521a576eeb1d51ffe14bd7`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffffa9c686d1675f116635f73719a4267f8149f487c624f3dd3fc0d64add3706`  
		Last Modified: Thu, 11 Jan 2024 06:11:02 GMT  
		Size: 115.5 MB (115545976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1fe91b7489538e32154a8cc6388b6bed98806360bd57ea143cf50e6465e6bb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4e6f4de772f3b4c752d7df0f5dc81f54e45dbc474daa0cbe740d01f7f6bdb4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:21:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:21:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:21:55 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:22:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:22:21 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:22:21 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:22:21 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:22:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:22:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af1789ab5680e3789b3db8df3c09f623907aacbc747237e0bfa42437b4e5ed4`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ff6b54382050e5e495f1807b96e890e32936115d55df0892d42b47fb5ad9dc`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acf82b1dfc10fb2132b6abedd93a9b5beed9845fdeddf980134e2b1e69a820e`  
		Last Modified: Thu, 11 Jan 2024 06:24:46 GMT  
		Size: 115.5 MB (115515864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:0a3c9c4eb4cb09bd30ddae5ded33edba2bdaa1d1f263709e3b834fc9040c9d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:2377f4203c56c5b139694c96e7324c78d22befb7a0d5c479baa3539494c1b65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291851185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc8fa1b57980bdf08750d60d432b37508e82d5f9f6a63ac9373e2c5598353f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:07:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:07:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:05 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:06 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05509e4b1c34bdb466397876153ead4ecbdc03389deadbb9b72f758e9841a51`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a316564fdae6d2d92ab40ff74bbd79b03c9837463e521a576eeb1d51ffe14bd7`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffffa9c686d1675f116635f73719a4267f8149f487c624f3dd3fc0d64add3706`  
		Last Modified: Thu, 11 Jan 2024 06:11:02 GMT  
		Size: 115.5 MB (115545976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1fe91b7489538e32154a8cc6388b6bed98806360bd57ea143cf50e6465e6bb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4e6f4de772f3b4c752d7df0f5dc81f54e45dbc474daa0cbe740d01f7f6bdb4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:21:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:21:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:21:55 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:22:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:22:21 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:22:21 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:22:21 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:22:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:22:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af1789ab5680e3789b3db8df3c09f623907aacbc747237e0bfa42437b4e5ed4`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ff6b54382050e5e495f1807b96e890e32936115d55df0892d42b47fb5ad9dc`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acf82b1dfc10fb2132b6abedd93a9b5beed9845fdeddf980134e2b1e69a820e`  
		Last Modified: Thu, 11 Jan 2024 06:24:46 GMT  
		Size: 115.5 MB (115515864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:0a3c9c4eb4cb09bd30ddae5ded33edba2bdaa1d1f263709e3b834fc9040c9d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2377f4203c56c5b139694c96e7324c78d22befb7a0d5c479baa3539494c1b65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291851185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc8fa1b57980bdf08750d60d432b37508e82d5f9f6a63ac9373e2c5598353f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:07:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:07:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:05 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:06 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05509e4b1c34bdb466397876153ead4ecbdc03389deadbb9b72f758e9841a51`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a316564fdae6d2d92ab40ff74bbd79b03c9837463e521a576eeb1d51ffe14bd7`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffffa9c686d1675f116635f73719a4267f8149f487c624f3dd3fc0d64add3706`  
		Last Modified: Thu, 11 Jan 2024 06:11:02 GMT  
		Size: 115.5 MB (115545976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1fe91b7489538e32154a8cc6388b6bed98806360bd57ea143cf50e6465e6bb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4e6f4de772f3b4c752d7df0f5dc81f54e45dbc474daa0cbe740d01f7f6bdb4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:21:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:21:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:21:55 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:22:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:22:21 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:22:21 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:22:21 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:22:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:22:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af1789ab5680e3789b3db8df3c09f623907aacbc747237e0bfa42437b4e5ed4`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ff6b54382050e5e495f1807b96e890e32936115d55df0892d42b47fb5ad9dc`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acf82b1dfc10fb2132b6abedd93a9b5beed9845fdeddf980134e2b1e69a820e`  
		Last Modified: Thu, 11 Jan 2024 06:24:46 GMT  
		Size: 115.5 MB (115515864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:edf7ddeb1c0676261b41fe0f6b131e63e0c1ff828bb537aeb6bcdf1794dde41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:b466350737ba1171ce7f377e8fbf78ef0b2a7c5c661dca0478122b4bd3b78cb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304130411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25d10559bd3b0b69abd5f5df711610d7494cf7ef6b4f17b1a1d124e6a862619`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:7f7df342ffd2955c9678013b3f777c87b323653d27236a9e1db2138fb7d52c3a in / 
# Wed, 03 Jan 2024 02:28:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:05 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:05 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:2404cd050b85acd3a327d3a58d0ec7bfda5f799f72f681d7f9cd48d64d0fb171 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:aec12625f757d84dbf50e30bbdd719c35331419fcfef0309bcc46e532c8f8c75 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:06 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:08 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 01:40:58 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 01:43:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 01:43:02 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 01:43:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 01:43:03 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 01:43:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 01:43:07 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 01:43:07 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 01:43:07 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 01:43:07 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 01:43:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 01:43:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b08c51af1a038ce2a6ca7097b2fbc332c78d5e0e85f2049859341da594558f63`  
		Last Modified: Wed, 10 Jan 2024 18:45:10 GMT  
		Size: 39.3 MB (39337272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e783b5d61e3cc6aa5413af0e608a66e1b7714ff3c3c9d7dabf5a0cd4b63e53e`  
		Last Modified: Sat, 13 Jan 2024 01:44:27 GMT  
		Size: 152.2 MB (152164797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe40d93c58c2e41c08a2f0840996e983e2e40c906a51710a1af4a7e21c07ff2c`  
		Last Modified: Sat, 13 Jan 2024 01:44:08 GMT  
		Size: 9.5 KB (9493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e125dbbe0ae6f46ef283205e2e73d2b9f23bae4ed3162c18a55ad3bf9c47c8`  
		Last Modified: Sat, 13 Jan 2024 01:44:14 GMT  
		Size: 112.6 MB (112618849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d6d0486b92e2504cd59f19696baa62760d8b3e5e5057255f96241d696e035908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300999716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06a77249e68c2e72a2bdff6a80e59c7d8b5c5400b02c0babd09335ba9b58d17`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:02 GMT
ADD file:44d847d928ee6a2f89f63e8a4d8911ad5f06ca8d03614b92f771437b7af97a93 in / 
# Wed, 03 Jan 2024 02:28:03 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:04 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:04 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:04 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:732275022803e0afa209662684138de795a06022f8b219d6fc37652986ecd682 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:bd521bacd38743c2200dc36ae2ef5224c3aec5086b9fab8e40ae3295fcd4398f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:06 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:08 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:09 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 02:01:05 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 02:03:02 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 02:03:05 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 02:03:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 02:03:05 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 02:03:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 02:03:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 02:03:09 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 02:03:09 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 02:03:09 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 02:03:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 02:03:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:da34b6d716bae3dbcb7925078ba70c246964d3569631d06767906fc030e3282b`  
		Last Modified: Wed, 10 Jan 2024 18:53:17 GMT  
		Size: 37.6 MB (37648974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae574271df94eab1939b41b3e3e5e5dc6b9aeef55608e3a9aeca6d9cfa53fff`  
		Last Modified: Sat, 13 Jan 2024 02:04:10 GMT  
		Size: 150.7 MB (150722468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609c3489b4ed27bfdbb91801da65a8cef9acb74935558997a096fd8caa8738c3`  
		Last Modified: Sat, 13 Jan 2024 02:03:55 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e5cbbedc29000984b29c7e1799687e4fe68fe09f4527d13ac808b9050eb47b`  
		Last Modified: Sat, 13 Jan 2024 02:03:59 GMT  
		Size: 112.6 MB (112618784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:127497f652e5686c4d64fe2be75b28d32c9d13286efd55e5515bc985e8e40690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1e3d6345fc8fb0eb6d82490041cd7ec2e08b8528f2bbc3109c854b0f98318bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565743747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9437581c6b72c901dd9545a1b9b20a18f966a00b860564aaa51e70c441e7b8e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:08:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:08:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:08:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:08:10 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:55 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:56 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29012b384b25080b769b29d87f60ab473b8d98b32012af3173368ef1ad4371ff`  
		Last Modified: Thu, 11 Jan 2024 06:11:34 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8c818ffc318228bb2a0b6beb3cb15f26dc0f9c238f33ae36a4112a2473e64a`  
		Last Modified: Thu, 11 Jan 2024 06:11:34 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8324b0159e9b83e62618362ce15ae215b63dc7ff3dff8ab7470fbf148a54e36`  
		Last Modified: Thu, 11 Jan 2024 06:11:49 GMT  
		Size: 389.4 MB (389438540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1f408c92b56a47ad4beda82085777562fc33368d2d9f8bb1c39556a6e06c891
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.2 MB (563162394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d90cc33b79544292ea903466ff4ee66e4037f282a2b069383fdbbd6857e2f8a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:22:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:22:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:22:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:22:30 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:23:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:23:00 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:23:01 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:23:01 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:23:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:23:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af3b5c7d496bb91413fd4067043bec0f3df4c6de6fa33ec87a8bb2cb57f317f`  
		Last Modified: Thu, 11 Jan 2024 06:25:25 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230a8cb6522c827881b04d2a1b535850d0614c5b93f6fa0ccdd3a1bfc967eb59`  
		Last Modified: Thu, 11 Jan 2024 06:25:26 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ef547d1254408c8a5346cdf3e916f9a2d29a346839165f58681a0750f738fa`  
		Last Modified: Thu, 11 Jan 2024 06:25:38 GMT  
		Size: 389.4 MB (389403266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:127497f652e5686c4d64fe2be75b28d32c9d13286efd55e5515bc985e8e40690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1e3d6345fc8fb0eb6d82490041cd7ec2e08b8528f2bbc3109c854b0f98318bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565743747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9437581c6b72c901dd9545a1b9b20a18f966a00b860564aaa51e70c441e7b8e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:08:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:08:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:08:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:08:10 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:55 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:56 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29012b384b25080b769b29d87f60ab473b8d98b32012af3173368ef1ad4371ff`  
		Last Modified: Thu, 11 Jan 2024 06:11:34 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8c818ffc318228bb2a0b6beb3cb15f26dc0f9c238f33ae36a4112a2473e64a`  
		Last Modified: Thu, 11 Jan 2024 06:11:34 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8324b0159e9b83e62618362ce15ae215b63dc7ff3dff8ab7470fbf148a54e36`  
		Last Modified: Thu, 11 Jan 2024 06:11:49 GMT  
		Size: 389.4 MB (389438540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1f408c92b56a47ad4beda82085777562fc33368d2d9f8bb1c39556a6e06c891
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.2 MB (563162394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d90cc33b79544292ea903466ff4ee66e4037f282a2b069383fdbbd6857e2f8a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:22:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:22:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:22:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:22:30 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:23:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:23:00 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:23:01 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:23:01 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:23:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:23:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af3b5c7d496bb91413fd4067043bec0f3df4c6de6fa33ec87a8bb2cb57f317f`  
		Last Modified: Thu, 11 Jan 2024 06:25:25 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230a8cb6522c827881b04d2a1b535850d0614c5b93f6fa0ccdd3a1bfc967eb59`  
		Last Modified: Thu, 11 Jan 2024 06:25:26 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ef547d1254408c8a5346cdf3e916f9a2d29a346839165f58681a0750f738fa`  
		Last Modified: Thu, 11 Jan 2024 06:25:38 GMT  
		Size: 389.4 MB (389403266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:a0cae6f4624183fa45cb85bc2b31748016148bd01311f65c33e5ec186bee8dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:243df31dc47f3f16850e55572e857edf9f6c6c8e4801b430be9bd4acf80f3094
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.0 MB (578017303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c400c424063b58e226df5c615cc3f4c55be5863972121be57dca869808d40435`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:7f7df342ffd2955c9678013b3f777c87b323653d27236a9e1db2138fb7d52c3a in / 
# Wed, 03 Jan 2024 02:28:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:05 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:05 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:2404cd050b85acd3a327d3a58d0ec7bfda5f799f72f681d7f9cd48d64d0fb171 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:aec12625f757d84dbf50e30bbdd719c35331419fcfef0309bcc46e532c8f8c75 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:06 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:08 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 01:40:58 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 01:43:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 01:43:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 01:43:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 01:43:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 01:43:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 01:43:34 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 01:43:34 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 01:43:34 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 01:43:34 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 01:43:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 01:43:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b08c51af1a038ce2a6ca7097b2fbc332c78d5e0e85f2049859341da594558f63`  
		Last Modified: Wed, 10 Jan 2024 18:45:10 GMT  
		Size: 39.3 MB (39337272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e783b5d61e3cc6aa5413af0e608a66e1b7714ff3c3c9d7dabf5a0cd4b63e53e`  
		Last Modified: Sat, 13 Jan 2024 01:44:27 GMT  
		Size: 152.2 MB (152164797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68fd23edb2d9b49aec29b82d959df19e70f963346e257ec44eca21b2b4f8d3b1`  
		Last Modified: Sat, 13 Jan 2024 01:44:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf0491e1bd7f1a00786edb4049d0156ee59800c03e6e827b10bb68656c19601`  
		Last Modified: Sat, 13 Jan 2024 01:45:01 GMT  
		Size: 386.5 MB (386505744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:712debf8f7763ddef037ad684929d2e7222b83a6a7be3733691b897148480d73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.9 MB (574886737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f864c73a20b6934ada25a7991897d1e7676c75016ef0ebf29f05b350ec72a2f0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:02 GMT
ADD file:44d847d928ee6a2f89f63e8a4d8911ad5f06ca8d03614b92f771437b7af97a93 in / 
# Wed, 03 Jan 2024 02:28:03 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:04 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:04 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:04 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:732275022803e0afa209662684138de795a06022f8b219d6fc37652986ecd682 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:bd521bacd38743c2200dc36ae2ef5224c3aec5086b9fab8e40ae3295fcd4398f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:06 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:08 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:09 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 02:01:05 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 02:03:02 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 02:03:13 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 02:03:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 02:03:13 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 02:03:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 02:03:24 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 02:03:24 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 02:03:24 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 02:03:25 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 02:03:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 02:03:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:da34b6d716bae3dbcb7925078ba70c246964d3569631d06767906fc030e3282b`  
		Last Modified: Wed, 10 Jan 2024 18:53:17 GMT  
		Size: 37.6 MB (37648974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae574271df94eab1939b41b3e3e5e5dc6b9aeef55608e3a9aeca6d9cfa53fff`  
		Last Modified: Sat, 13 Jan 2024 02:04:10 GMT  
		Size: 150.7 MB (150722468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6250a684ece16d1e9a0387114dc0c7f5d11f9abde1bcc7dc70f18355fc9dd00f`  
		Last Modified: Sat, 13 Jan 2024 02:04:29 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a8cbe41783ac22a0eb802fdefc9a8d1c814c290996330bb6cd7ac6749c9330`  
		Last Modified: Sat, 13 Jan 2024 02:04:41 GMT  
		Size: 386.5 MB (386505811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:edf7ddeb1c0676261b41fe0f6b131e63e0c1ff828bb537aeb6bcdf1794dde41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:b466350737ba1171ce7f377e8fbf78ef0b2a7c5c661dca0478122b4bd3b78cb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304130411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25d10559bd3b0b69abd5f5df711610d7494cf7ef6b4f17b1a1d124e6a862619`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:7f7df342ffd2955c9678013b3f777c87b323653d27236a9e1db2138fb7d52c3a in / 
# Wed, 03 Jan 2024 02:28:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:05 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:05 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:2404cd050b85acd3a327d3a58d0ec7bfda5f799f72f681d7f9cd48d64d0fb171 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:aec12625f757d84dbf50e30bbdd719c35331419fcfef0309bcc46e532c8f8c75 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:06 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:08 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 01:40:58 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 01:43:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 01:43:02 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 01:43:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 01:43:03 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 01:43:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 01:43:07 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 01:43:07 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 01:43:07 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 01:43:07 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 01:43:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 01:43:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b08c51af1a038ce2a6ca7097b2fbc332c78d5e0e85f2049859341da594558f63`  
		Last Modified: Wed, 10 Jan 2024 18:45:10 GMT  
		Size: 39.3 MB (39337272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e783b5d61e3cc6aa5413af0e608a66e1b7714ff3c3c9d7dabf5a0cd4b63e53e`  
		Last Modified: Sat, 13 Jan 2024 01:44:27 GMT  
		Size: 152.2 MB (152164797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe40d93c58c2e41c08a2f0840996e983e2e40c906a51710a1af4a7e21c07ff2c`  
		Last Modified: Sat, 13 Jan 2024 01:44:08 GMT  
		Size: 9.5 KB (9493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e125dbbe0ae6f46ef283205e2e73d2b9f23bae4ed3162c18a55ad3bf9c47c8`  
		Last Modified: Sat, 13 Jan 2024 01:44:14 GMT  
		Size: 112.6 MB (112618849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d6d0486b92e2504cd59f19696baa62760d8b3e5e5057255f96241d696e035908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300999716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06a77249e68c2e72a2bdff6a80e59c7d8b5c5400b02c0babd09335ba9b58d17`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:02 GMT
ADD file:44d847d928ee6a2f89f63e8a4d8911ad5f06ca8d03614b92f771437b7af97a93 in / 
# Wed, 03 Jan 2024 02:28:03 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:04 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:04 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:04 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:732275022803e0afa209662684138de795a06022f8b219d6fc37652986ecd682 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:bd521bacd38743c2200dc36ae2ef5224c3aec5086b9fab8e40ae3295fcd4398f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:06 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:08 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:09 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 02:01:05 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 02:03:02 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 02:03:05 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 02:03:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 02:03:05 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 02:03:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 02:03:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 02:03:09 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 02:03:09 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 02:03:09 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 02:03:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 02:03:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:da34b6d716bae3dbcb7925078ba70c246964d3569631d06767906fc030e3282b`  
		Last Modified: Wed, 10 Jan 2024 18:53:17 GMT  
		Size: 37.6 MB (37648974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae574271df94eab1939b41b3e3e5e5dc6b9aeef55608e3a9aeca6d9cfa53fff`  
		Last Modified: Sat, 13 Jan 2024 02:04:10 GMT  
		Size: 150.7 MB (150722468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609c3489b4ed27bfdbb91801da65a8cef9acb74935558997a096fd8caa8738c3`  
		Last Modified: Sat, 13 Jan 2024 02:03:55 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e5cbbedc29000984b29c7e1799687e4fe68fe09f4527d13ac808b9050eb47b`  
		Last Modified: Sat, 13 Jan 2024 02:03:59 GMT  
		Size: 112.6 MB (112618784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15`

```console
$ docker pull neo4j@sha256:0a3c9c4eb4cb09bd30ddae5ded33edba2bdaa1d1f263709e3b834fc9040c9d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15` - linux; amd64

```console
$ docker pull neo4j@sha256:2377f4203c56c5b139694c96e7324c78d22befb7a0d5c479baa3539494c1b65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291851185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc8fa1b57980bdf08750d60d432b37508e82d5f9f6a63ac9373e2c5598353f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:07:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:07:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:05 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:06 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05509e4b1c34bdb466397876153ead4ecbdc03389deadbb9b72f758e9841a51`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a316564fdae6d2d92ab40ff74bbd79b03c9837463e521a576eeb1d51ffe14bd7`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffffa9c686d1675f116635f73719a4267f8149f487c624f3dd3fc0d64add3706`  
		Last Modified: Thu, 11 Jan 2024 06:11:02 GMT  
		Size: 115.5 MB (115545976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1fe91b7489538e32154a8cc6388b6bed98806360bd57ea143cf50e6465e6bb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4e6f4de772f3b4c752d7df0f5dc81f54e45dbc474daa0cbe740d01f7f6bdb4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:21:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:21:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:21:55 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:22:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:22:21 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:22:21 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:22:21 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:22:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:22:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af1789ab5680e3789b3db8df3c09f623907aacbc747237e0bfa42437b4e5ed4`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ff6b54382050e5e495f1807b96e890e32936115d55df0892d42b47fb5ad9dc`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acf82b1dfc10fb2132b6abedd93a9b5beed9845fdeddf980134e2b1e69a820e`  
		Last Modified: Thu, 11 Jan 2024 06:24:46 GMT  
		Size: 115.5 MB (115515864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15-bullseye`

```console
$ docker pull neo4j@sha256:0a3c9c4eb4cb09bd30ddae5ded33edba2bdaa1d1f263709e3b834fc9040c9d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2377f4203c56c5b139694c96e7324c78d22befb7a0d5c479baa3539494c1b65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291851185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc8fa1b57980bdf08750d60d432b37508e82d5f9f6a63ac9373e2c5598353f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:07:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:07:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:05 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:06 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05509e4b1c34bdb466397876153ead4ecbdc03389deadbb9b72f758e9841a51`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a316564fdae6d2d92ab40ff74bbd79b03c9837463e521a576eeb1d51ffe14bd7`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffffa9c686d1675f116635f73719a4267f8149f487c624f3dd3fc0d64add3706`  
		Last Modified: Thu, 11 Jan 2024 06:11:02 GMT  
		Size: 115.5 MB (115545976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1fe91b7489538e32154a8cc6388b6bed98806360bd57ea143cf50e6465e6bb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4e6f4de772f3b4c752d7df0f5dc81f54e45dbc474daa0cbe740d01f7f6bdb4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:21:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:21:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:21:55 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:22:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:22:21 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:22:21 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:22:21 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:22:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:22:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af1789ab5680e3789b3db8df3c09f623907aacbc747237e0bfa42437b4e5ed4`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ff6b54382050e5e495f1807b96e890e32936115d55df0892d42b47fb5ad9dc`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acf82b1dfc10fb2132b6abedd93a9b5beed9845fdeddf980134e2b1e69a820e`  
		Last Modified: Thu, 11 Jan 2024 06:24:46 GMT  
		Size: 115.5 MB (115515864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15-community`

```console
$ docker pull neo4j@sha256:0a3c9c4eb4cb09bd30ddae5ded33edba2bdaa1d1f263709e3b834fc9040c9d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15-community` - linux; amd64

```console
$ docker pull neo4j@sha256:2377f4203c56c5b139694c96e7324c78d22befb7a0d5c479baa3539494c1b65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291851185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc8fa1b57980bdf08750d60d432b37508e82d5f9f6a63ac9373e2c5598353f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:07:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:07:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:05 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:06 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05509e4b1c34bdb466397876153ead4ecbdc03389deadbb9b72f758e9841a51`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a316564fdae6d2d92ab40ff74bbd79b03c9837463e521a576eeb1d51ffe14bd7`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffffa9c686d1675f116635f73719a4267f8149f487c624f3dd3fc0d64add3706`  
		Last Modified: Thu, 11 Jan 2024 06:11:02 GMT  
		Size: 115.5 MB (115545976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1fe91b7489538e32154a8cc6388b6bed98806360bd57ea143cf50e6465e6bb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4e6f4de772f3b4c752d7df0f5dc81f54e45dbc474daa0cbe740d01f7f6bdb4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:21:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:21:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:21:55 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:22:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:22:21 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:22:21 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:22:21 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:22:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:22:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af1789ab5680e3789b3db8df3c09f623907aacbc747237e0bfa42437b4e5ed4`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ff6b54382050e5e495f1807b96e890e32936115d55df0892d42b47fb5ad9dc`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acf82b1dfc10fb2132b6abedd93a9b5beed9845fdeddf980134e2b1e69a820e`  
		Last Modified: Thu, 11 Jan 2024 06:24:46 GMT  
		Size: 115.5 MB (115515864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15-community-bullseye`

```console
$ docker pull neo4j@sha256:0a3c9c4eb4cb09bd30ddae5ded33edba2bdaa1d1f263709e3b834fc9040c9d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2377f4203c56c5b139694c96e7324c78d22befb7a0d5c479baa3539494c1b65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291851185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc8fa1b57980bdf08750d60d432b37508e82d5f9f6a63ac9373e2c5598353f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:07:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:07:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:05 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:06 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05509e4b1c34bdb466397876153ead4ecbdc03389deadbb9b72f758e9841a51`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a316564fdae6d2d92ab40ff74bbd79b03c9837463e521a576eeb1d51ffe14bd7`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffffa9c686d1675f116635f73719a4267f8149f487c624f3dd3fc0d64add3706`  
		Last Modified: Thu, 11 Jan 2024 06:11:02 GMT  
		Size: 115.5 MB (115545976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1fe91b7489538e32154a8cc6388b6bed98806360bd57ea143cf50e6465e6bb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4e6f4de772f3b4c752d7df0f5dc81f54e45dbc474daa0cbe740d01f7f6bdb4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:21:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:21:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:21:55 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:22:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:22:21 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:22:21 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:22:21 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:22:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:22:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af1789ab5680e3789b3db8df3c09f623907aacbc747237e0bfa42437b4e5ed4`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ff6b54382050e5e495f1807b96e890e32936115d55df0892d42b47fb5ad9dc`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acf82b1dfc10fb2132b6abedd93a9b5beed9845fdeddf980134e2b1e69a820e`  
		Last Modified: Thu, 11 Jan 2024 06:24:46 GMT  
		Size: 115.5 MB (115515864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15-community-ubi8`

```console
$ docker pull neo4j@sha256:edf7ddeb1c0676261b41fe0f6b131e63e0c1ff828bb537aeb6bcdf1794dde41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:b466350737ba1171ce7f377e8fbf78ef0b2a7c5c661dca0478122b4bd3b78cb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304130411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25d10559bd3b0b69abd5f5df711610d7494cf7ef6b4f17b1a1d124e6a862619`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:7f7df342ffd2955c9678013b3f777c87b323653d27236a9e1db2138fb7d52c3a in / 
# Wed, 03 Jan 2024 02:28:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:05 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:05 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:2404cd050b85acd3a327d3a58d0ec7bfda5f799f72f681d7f9cd48d64d0fb171 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:aec12625f757d84dbf50e30bbdd719c35331419fcfef0309bcc46e532c8f8c75 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:06 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:08 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 01:40:58 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 01:43:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 01:43:02 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 01:43:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 01:43:03 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 01:43:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 01:43:07 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 01:43:07 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 01:43:07 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 01:43:07 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 01:43:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 01:43:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b08c51af1a038ce2a6ca7097b2fbc332c78d5e0e85f2049859341da594558f63`  
		Last Modified: Wed, 10 Jan 2024 18:45:10 GMT  
		Size: 39.3 MB (39337272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e783b5d61e3cc6aa5413af0e608a66e1b7714ff3c3c9d7dabf5a0cd4b63e53e`  
		Last Modified: Sat, 13 Jan 2024 01:44:27 GMT  
		Size: 152.2 MB (152164797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe40d93c58c2e41c08a2f0840996e983e2e40c906a51710a1af4a7e21c07ff2c`  
		Last Modified: Sat, 13 Jan 2024 01:44:08 GMT  
		Size: 9.5 KB (9493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e125dbbe0ae6f46ef283205e2e73d2b9f23bae4ed3162c18a55ad3bf9c47c8`  
		Last Modified: Sat, 13 Jan 2024 01:44:14 GMT  
		Size: 112.6 MB (112618849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d6d0486b92e2504cd59f19696baa62760d8b3e5e5057255f96241d696e035908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300999716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06a77249e68c2e72a2bdff6a80e59c7d8b5c5400b02c0babd09335ba9b58d17`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:02 GMT
ADD file:44d847d928ee6a2f89f63e8a4d8911ad5f06ca8d03614b92f771437b7af97a93 in / 
# Wed, 03 Jan 2024 02:28:03 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:04 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:04 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:04 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:732275022803e0afa209662684138de795a06022f8b219d6fc37652986ecd682 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:bd521bacd38743c2200dc36ae2ef5224c3aec5086b9fab8e40ae3295fcd4398f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:06 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:08 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:09 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 02:01:05 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 02:03:02 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 02:03:05 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 02:03:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 02:03:05 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 02:03:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 02:03:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 02:03:09 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 02:03:09 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 02:03:09 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 02:03:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 02:03:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:da34b6d716bae3dbcb7925078ba70c246964d3569631d06767906fc030e3282b`  
		Last Modified: Wed, 10 Jan 2024 18:53:17 GMT  
		Size: 37.6 MB (37648974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae574271df94eab1939b41b3e3e5e5dc6b9aeef55608e3a9aeca6d9cfa53fff`  
		Last Modified: Sat, 13 Jan 2024 02:04:10 GMT  
		Size: 150.7 MB (150722468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609c3489b4ed27bfdbb91801da65a8cef9acb74935558997a096fd8caa8738c3`  
		Last Modified: Sat, 13 Jan 2024 02:03:55 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e5cbbedc29000984b29c7e1799687e4fe68fe09f4527d13ac808b9050eb47b`  
		Last Modified: Sat, 13 Jan 2024 02:03:59 GMT  
		Size: 112.6 MB (112618784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15-enterprise`

```console
$ docker pull neo4j@sha256:127497f652e5686c4d64fe2be75b28d32c9d13286efd55e5515bc985e8e40690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1e3d6345fc8fb0eb6d82490041cd7ec2e08b8528f2bbc3109c854b0f98318bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565743747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9437581c6b72c901dd9545a1b9b20a18f966a00b860564aaa51e70c441e7b8e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:08:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:08:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:08:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:08:10 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:55 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:56 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29012b384b25080b769b29d87f60ab473b8d98b32012af3173368ef1ad4371ff`  
		Last Modified: Thu, 11 Jan 2024 06:11:34 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8c818ffc318228bb2a0b6beb3cb15f26dc0f9c238f33ae36a4112a2473e64a`  
		Last Modified: Thu, 11 Jan 2024 06:11:34 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8324b0159e9b83e62618362ce15ae215b63dc7ff3dff8ab7470fbf148a54e36`  
		Last Modified: Thu, 11 Jan 2024 06:11:49 GMT  
		Size: 389.4 MB (389438540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1f408c92b56a47ad4beda82085777562fc33368d2d9f8bb1c39556a6e06c891
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.2 MB (563162394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d90cc33b79544292ea903466ff4ee66e4037f282a2b069383fdbbd6857e2f8a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:22:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:22:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:22:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:22:30 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:23:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:23:00 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:23:01 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:23:01 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:23:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:23:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af3b5c7d496bb91413fd4067043bec0f3df4c6de6fa33ec87a8bb2cb57f317f`  
		Last Modified: Thu, 11 Jan 2024 06:25:25 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230a8cb6522c827881b04d2a1b535850d0614c5b93f6fa0ccdd3a1bfc967eb59`  
		Last Modified: Thu, 11 Jan 2024 06:25:26 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ef547d1254408c8a5346cdf3e916f9a2d29a346839165f58681a0750f738fa`  
		Last Modified: Thu, 11 Jan 2024 06:25:38 GMT  
		Size: 389.4 MB (389403266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:127497f652e5686c4d64fe2be75b28d32c9d13286efd55e5515bc985e8e40690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1e3d6345fc8fb0eb6d82490041cd7ec2e08b8528f2bbc3109c854b0f98318bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565743747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9437581c6b72c901dd9545a1b9b20a18f966a00b860564aaa51e70c441e7b8e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:08:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:08:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:08:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:08:10 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:55 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:56 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29012b384b25080b769b29d87f60ab473b8d98b32012af3173368ef1ad4371ff`  
		Last Modified: Thu, 11 Jan 2024 06:11:34 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8c818ffc318228bb2a0b6beb3cb15f26dc0f9c238f33ae36a4112a2473e64a`  
		Last Modified: Thu, 11 Jan 2024 06:11:34 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8324b0159e9b83e62618362ce15ae215b63dc7ff3dff8ab7470fbf148a54e36`  
		Last Modified: Thu, 11 Jan 2024 06:11:49 GMT  
		Size: 389.4 MB (389438540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1f408c92b56a47ad4beda82085777562fc33368d2d9f8bb1c39556a6e06c891
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.2 MB (563162394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d90cc33b79544292ea903466ff4ee66e4037f282a2b069383fdbbd6857e2f8a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:22:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:22:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:22:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:22:30 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:23:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:23:00 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:23:01 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:23:01 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:23:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:23:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af3b5c7d496bb91413fd4067043bec0f3df4c6de6fa33ec87a8bb2cb57f317f`  
		Last Modified: Thu, 11 Jan 2024 06:25:25 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230a8cb6522c827881b04d2a1b535850d0614c5b93f6fa0ccdd3a1bfc967eb59`  
		Last Modified: Thu, 11 Jan 2024 06:25:26 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ef547d1254408c8a5346cdf3e916f9a2d29a346839165f58681a0750f738fa`  
		Last Modified: Thu, 11 Jan 2024 06:25:38 GMT  
		Size: 389.4 MB (389403266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:a0cae6f4624183fa45cb85bc2b31748016148bd01311f65c33e5ec186bee8dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:243df31dc47f3f16850e55572e857edf9f6c6c8e4801b430be9bd4acf80f3094
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.0 MB (578017303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c400c424063b58e226df5c615cc3f4c55be5863972121be57dca869808d40435`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:7f7df342ffd2955c9678013b3f777c87b323653d27236a9e1db2138fb7d52c3a in / 
# Wed, 03 Jan 2024 02:28:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:05 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:05 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:2404cd050b85acd3a327d3a58d0ec7bfda5f799f72f681d7f9cd48d64d0fb171 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:aec12625f757d84dbf50e30bbdd719c35331419fcfef0309bcc46e532c8f8c75 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:06 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:08 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 01:40:58 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 01:43:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 01:43:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 01:43:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 01:43:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 01:43:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 01:43:34 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 01:43:34 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 01:43:34 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 01:43:34 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 01:43:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 01:43:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b08c51af1a038ce2a6ca7097b2fbc332c78d5e0e85f2049859341da594558f63`  
		Last Modified: Wed, 10 Jan 2024 18:45:10 GMT  
		Size: 39.3 MB (39337272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e783b5d61e3cc6aa5413af0e608a66e1b7714ff3c3c9d7dabf5a0cd4b63e53e`  
		Last Modified: Sat, 13 Jan 2024 01:44:27 GMT  
		Size: 152.2 MB (152164797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68fd23edb2d9b49aec29b82d959df19e70f963346e257ec44eca21b2b4f8d3b1`  
		Last Modified: Sat, 13 Jan 2024 01:44:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf0491e1bd7f1a00786edb4049d0156ee59800c03e6e827b10bb68656c19601`  
		Last Modified: Sat, 13 Jan 2024 01:45:01 GMT  
		Size: 386.5 MB (386505744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:712debf8f7763ddef037ad684929d2e7222b83a6a7be3733691b897148480d73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.9 MB (574886737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f864c73a20b6934ada25a7991897d1e7676c75016ef0ebf29f05b350ec72a2f0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:02 GMT
ADD file:44d847d928ee6a2f89f63e8a4d8911ad5f06ca8d03614b92f771437b7af97a93 in / 
# Wed, 03 Jan 2024 02:28:03 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:04 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:04 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:04 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:732275022803e0afa209662684138de795a06022f8b219d6fc37652986ecd682 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:bd521bacd38743c2200dc36ae2ef5224c3aec5086b9fab8e40ae3295fcd4398f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:06 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:08 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:09 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 02:01:05 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 02:03:02 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 02:03:13 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 02:03:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 02:03:13 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 02:03:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 02:03:24 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 02:03:24 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 02:03:24 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 02:03:25 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 02:03:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 02:03:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:da34b6d716bae3dbcb7925078ba70c246964d3569631d06767906fc030e3282b`  
		Last Modified: Wed, 10 Jan 2024 18:53:17 GMT  
		Size: 37.6 MB (37648974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae574271df94eab1939b41b3e3e5e5dc6b9aeef55608e3a9aeca6d9cfa53fff`  
		Last Modified: Sat, 13 Jan 2024 02:04:10 GMT  
		Size: 150.7 MB (150722468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6250a684ece16d1e9a0387114dc0c7f5d11f9abde1bcc7dc70f18355fc9dd00f`  
		Last Modified: Sat, 13 Jan 2024 02:04:29 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a8cbe41783ac22a0eb802fdefc9a8d1c814c290996330bb6cd7ac6749c9330`  
		Last Modified: Sat, 13 Jan 2024 02:04:41 GMT  
		Size: 386.5 MB (386505811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15-ubi8`

```console
$ docker pull neo4j@sha256:edf7ddeb1c0676261b41fe0f6b131e63e0c1ff828bb537aeb6bcdf1794dde41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:b466350737ba1171ce7f377e8fbf78ef0b2a7c5c661dca0478122b4bd3b78cb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304130411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25d10559bd3b0b69abd5f5df711610d7494cf7ef6b4f17b1a1d124e6a862619`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:7f7df342ffd2955c9678013b3f777c87b323653d27236a9e1db2138fb7d52c3a in / 
# Wed, 03 Jan 2024 02:28:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:05 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:05 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:2404cd050b85acd3a327d3a58d0ec7bfda5f799f72f681d7f9cd48d64d0fb171 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:aec12625f757d84dbf50e30bbdd719c35331419fcfef0309bcc46e532c8f8c75 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:06 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:08 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 01:40:58 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 01:43:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 01:43:02 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 01:43:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 01:43:03 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 01:43:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 01:43:07 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 01:43:07 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 01:43:07 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 01:43:07 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 01:43:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 01:43:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b08c51af1a038ce2a6ca7097b2fbc332c78d5e0e85f2049859341da594558f63`  
		Last Modified: Wed, 10 Jan 2024 18:45:10 GMT  
		Size: 39.3 MB (39337272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e783b5d61e3cc6aa5413af0e608a66e1b7714ff3c3c9d7dabf5a0cd4b63e53e`  
		Last Modified: Sat, 13 Jan 2024 01:44:27 GMT  
		Size: 152.2 MB (152164797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe40d93c58c2e41c08a2f0840996e983e2e40c906a51710a1af4a7e21c07ff2c`  
		Last Modified: Sat, 13 Jan 2024 01:44:08 GMT  
		Size: 9.5 KB (9493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e125dbbe0ae6f46ef283205e2e73d2b9f23bae4ed3162c18a55ad3bf9c47c8`  
		Last Modified: Sat, 13 Jan 2024 01:44:14 GMT  
		Size: 112.6 MB (112618849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d6d0486b92e2504cd59f19696baa62760d8b3e5e5057255f96241d696e035908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300999716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06a77249e68c2e72a2bdff6a80e59c7d8b5c5400b02c0babd09335ba9b58d17`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:02 GMT
ADD file:44d847d928ee6a2f89f63e8a4d8911ad5f06ca8d03614b92f771437b7af97a93 in / 
# Wed, 03 Jan 2024 02:28:03 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:04 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:04 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:04 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:732275022803e0afa209662684138de795a06022f8b219d6fc37652986ecd682 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:bd521bacd38743c2200dc36ae2ef5224c3aec5086b9fab8e40ae3295fcd4398f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:06 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:08 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:09 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 02:01:05 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 02:03:02 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 02:03:05 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 02:03:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 02:03:05 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 02:03:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 02:03:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 02:03:09 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 02:03:09 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 02:03:09 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 02:03:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 02:03:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:da34b6d716bae3dbcb7925078ba70c246964d3569631d06767906fc030e3282b`  
		Last Modified: Wed, 10 Jan 2024 18:53:17 GMT  
		Size: 37.6 MB (37648974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae574271df94eab1939b41b3e3e5e5dc6b9aeef55608e3a9aeca6d9cfa53fff`  
		Last Modified: Sat, 13 Jan 2024 02:04:10 GMT  
		Size: 150.7 MB (150722468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609c3489b4ed27bfdbb91801da65a8cef9acb74935558997a096fd8caa8738c3`  
		Last Modified: Sat, 13 Jan 2024 02:03:55 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e5cbbedc29000984b29c7e1799687e4fe68fe09f4527d13ac808b9050eb47b`  
		Last Modified: Sat, 13 Jan 2024 02:03:59 GMT  
		Size: 112.6 MB (112618784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15.0`

```console
$ docker pull neo4j@sha256:0a3c9c4eb4cb09bd30ddae5ded33edba2bdaa1d1f263709e3b834fc9040c9d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15.0` - linux; amd64

```console
$ docker pull neo4j@sha256:2377f4203c56c5b139694c96e7324c78d22befb7a0d5c479baa3539494c1b65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291851185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc8fa1b57980bdf08750d60d432b37508e82d5f9f6a63ac9373e2c5598353f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:07:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:07:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:05 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:06 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05509e4b1c34bdb466397876153ead4ecbdc03389deadbb9b72f758e9841a51`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a316564fdae6d2d92ab40ff74bbd79b03c9837463e521a576eeb1d51ffe14bd7`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffffa9c686d1675f116635f73719a4267f8149f487c624f3dd3fc0d64add3706`  
		Last Modified: Thu, 11 Jan 2024 06:11:02 GMT  
		Size: 115.5 MB (115545976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1fe91b7489538e32154a8cc6388b6bed98806360bd57ea143cf50e6465e6bb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4e6f4de772f3b4c752d7df0f5dc81f54e45dbc474daa0cbe740d01f7f6bdb4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:21:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:21:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:21:55 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:22:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:22:21 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:22:21 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:22:21 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:22:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:22:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af1789ab5680e3789b3db8df3c09f623907aacbc747237e0bfa42437b4e5ed4`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ff6b54382050e5e495f1807b96e890e32936115d55df0892d42b47fb5ad9dc`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acf82b1dfc10fb2132b6abedd93a9b5beed9845fdeddf980134e2b1e69a820e`  
		Last Modified: Thu, 11 Jan 2024 06:24:46 GMT  
		Size: 115.5 MB (115515864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15.0-bullseye`

```console
$ docker pull neo4j@sha256:0a3c9c4eb4cb09bd30ddae5ded33edba2bdaa1d1f263709e3b834fc9040c9d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2377f4203c56c5b139694c96e7324c78d22befb7a0d5c479baa3539494c1b65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291851185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc8fa1b57980bdf08750d60d432b37508e82d5f9f6a63ac9373e2c5598353f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:07:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:07:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:05 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:06 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05509e4b1c34bdb466397876153ead4ecbdc03389deadbb9b72f758e9841a51`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a316564fdae6d2d92ab40ff74bbd79b03c9837463e521a576eeb1d51ffe14bd7`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffffa9c686d1675f116635f73719a4267f8149f487c624f3dd3fc0d64add3706`  
		Last Modified: Thu, 11 Jan 2024 06:11:02 GMT  
		Size: 115.5 MB (115545976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1fe91b7489538e32154a8cc6388b6bed98806360bd57ea143cf50e6465e6bb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4e6f4de772f3b4c752d7df0f5dc81f54e45dbc474daa0cbe740d01f7f6bdb4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:21:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:21:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:21:55 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:22:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:22:21 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:22:21 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:22:21 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:22:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:22:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af1789ab5680e3789b3db8df3c09f623907aacbc747237e0bfa42437b4e5ed4`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ff6b54382050e5e495f1807b96e890e32936115d55df0892d42b47fb5ad9dc`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acf82b1dfc10fb2132b6abedd93a9b5beed9845fdeddf980134e2b1e69a820e`  
		Last Modified: Thu, 11 Jan 2024 06:24:46 GMT  
		Size: 115.5 MB (115515864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15.0-community`

```console
$ docker pull neo4j@sha256:0a3c9c4eb4cb09bd30ddae5ded33edba2bdaa1d1f263709e3b834fc9040c9d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:2377f4203c56c5b139694c96e7324c78d22befb7a0d5c479baa3539494c1b65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291851185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc8fa1b57980bdf08750d60d432b37508e82d5f9f6a63ac9373e2c5598353f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:07:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:07:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:05 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:06 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05509e4b1c34bdb466397876153ead4ecbdc03389deadbb9b72f758e9841a51`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a316564fdae6d2d92ab40ff74bbd79b03c9837463e521a576eeb1d51ffe14bd7`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffffa9c686d1675f116635f73719a4267f8149f487c624f3dd3fc0d64add3706`  
		Last Modified: Thu, 11 Jan 2024 06:11:02 GMT  
		Size: 115.5 MB (115545976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1fe91b7489538e32154a8cc6388b6bed98806360bd57ea143cf50e6465e6bb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4e6f4de772f3b4c752d7df0f5dc81f54e45dbc474daa0cbe740d01f7f6bdb4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:21:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:21:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:21:55 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:22:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:22:21 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:22:21 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:22:21 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:22:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:22:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af1789ab5680e3789b3db8df3c09f623907aacbc747237e0bfa42437b4e5ed4`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ff6b54382050e5e495f1807b96e890e32936115d55df0892d42b47fb5ad9dc`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acf82b1dfc10fb2132b6abedd93a9b5beed9845fdeddf980134e2b1e69a820e`  
		Last Modified: Thu, 11 Jan 2024 06:24:46 GMT  
		Size: 115.5 MB (115515864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15.0-community-bullseye`

```console
$ docker pull neo4j@sha256:0a3c9c4eb4cb09bd30ddae5ded33edba2bdaa1d1f263709e3b834fc9040c9d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2377f4203c56c5b139694c96e7324c78d22befb7a0d5c479baa3539494c1b65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291851185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc8fa1b57980bdf08750d60d432b37508e82d5f9f6a63ac9373e2c5598353f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:07:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:07:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:05 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:06 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05509e4b1c34bdb466397876153ead4ecbdc03389deadbb9b72f758e9841a51`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a316564fdae6d2d92ab40ff74bbd79b03c9837463e521a576eeb1d51ffe14bd7`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffffa9c686d1675f116635f73719a4267f8149f487c624f3dd3fc0d64add3706`  
		Last Modified: Thu, 11 Jan 2024 06:11:02 GMT  
		Size: 115.5 MB (115545976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1fe91b7489538e32154a8cc6388b6bed98806360bd57ea143cf50e6465e6bb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4e6f4de772f3b4c752d7df0f5dc81f54e45dbc474daa0cbe740d01f7f6bdb4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:21:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:21:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:21:55 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:22:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:22:21 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:22:21 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:22:21 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:22:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:22:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af1789ab5680e3789b3db8df3c09f623907aacbc747237e0bfa42437b4e5ed4`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ff6b54382050e5e495f1807b96e890e32936115d55df0892d42b47fb5ad9dc`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acf82b1dfc10fb2132b6abedd93a9b5beed9845fdeddf980134e2b1e69a820e`  
		Last Modified: Thu, 11 Jan 2024 06:24:46 GMT  
		Size: 115.5 MB (115515864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15.0-community-ubi8`

```console
$ docker pull neo4j@sha256:edf7ddeb1c0676261b41fe0f6b131e63e0c1ff828bb537aeb6bcdf1794dde41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15.0-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:b466350737ba1171ce7f377e8fbf78ef0b2a7c5c661dca0478122b4bd3b78cb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304130411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25d10559bd3b0b69abd5f5df711610d7494cf7ef6b4f17b1a1d124e6a862619`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:7f7df342ffd2955c9678013b3f777c87b323653d27236a9e1db2138fb7d52c3a in / 
# Wed, 03 Jan 2024 02:28:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:05 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:05 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:2404cd050b85acd3a327d3a58d0ec7bfda5f799f72f681d7f9cd48d64d0fb171 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:aec12625f757d84dbf50e30bbdd719c35331419fcfef0309bcc46e532c8f8c75 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:06 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:08 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 01:40:58 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 01:43:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 01:43:02 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 01:43:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 01:43:03 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 01:43:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 01:43:07 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 01:43:07 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 01:43:07 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 01:43:07 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 01:43:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 01:43:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b08c51af1a038ce2a6ca7097b2fbc332c78d5e0e85f2049859341da594558f63`  
		Last Modified: Wed, 10 Jan 2024 18:45:10 GMT  
		Size: 39.3 MB (39337272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e783b5d61e3cc6aa5413af0e608a66e1b7714ff3c3c9d7dabf5a0cd4b63e53e`  
		Last Modified: Sat, 13 Jan 2024 01:44:27 GMT  
		Size: 152.2 MB (152164797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe40d93c58c2e41c08a2f0840996e983e2e40c906a51710a1af4a7e21c07ff2c`  
		Last Modified: Sat, 13 Jan 2024 01:44:08 GMT  
		Size: 9.5 KB (9493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e125dbbe0ae6f46ef283205e2e73d2b9f23bae4ed3162c18a55ad3bf9c47c8`  
		Last Modified: Sat, 13 Jan 2024 01:44:14 GMT  
		Size: 112.6 MB (112618849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15.0-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d6d0486b92e2504cd59f19696baa62760d8b3e5e5057255f96241d696e035908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300999716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06a77249e68c2e72a2bdff6a80e59c7d8b5c5400b02c0babd09335ba9b58d17`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:02 GMT
ADD file:44d847d928ee6a2f89f63e8a4d8911ad5f06ca8d03614b92f771437b7af97a93 in / 
# Wed, 03 Jan 2024 02:28:03 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:04 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:04 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:04 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:732275022803e0afa209662684138de795a06022f8b219d6fc37652986ecd682 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:bd521bacd38743c2200dc36ae2ef5224c3aec5086b9fab8e40ae3295fcd4398f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:06 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:08 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:09 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 02:01:05 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 02:03:02 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 02:03:05 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 02:03:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 02:03:05 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 02:03:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 02:03:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 02:03:09 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 02:03:09 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 02:03:09 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 02:03:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 02:03:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:da34b6d716bae3dbcb7925078ba70c246964d3569631d06767906fc030e3282b`  
		Last Modified: Wed, 10 Jan 2024 18:53:17 GMT  
		Size: 37.6 MB (37648974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae574271df94eab1939b41b3e3e5e5dc6b9aeef55608e3a9aeca6d9cfa53fff`  
		Last Modified: Sat, 13 Jan 2024 02:04:10 GMT  
		Size: 150.7 MB (150722468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609c3489b4ed27bfdbb91801da65a8cef9acb74935558997a096fd8caa8738c3`  
		Last Modified: Sat, 13 Jan 2024 02:03:55 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e5cbbedc29000984b29c7e1799687e4fe68fe09f4527d13ac808b9050eb47b`  
		Last Modified: Sat, 13 Jan 2024 02:03:59 GMT  
		Size: 112.6 MB (112618784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15.0-enterprise`

```console
$ docker pull neo4j@sha256:127497f652e5686c4d64fe2be75b28d32c9d13286efd55e5515bc985e8e40690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1e3d6345fc8fb0eb6d82490041cd7ec2e08b8528f2bbc3109c854b0f98318bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565743747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9437581c6b72c901dd9545a1b9b20a18f966a00b860564aaa51e70c441e7b8e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:08:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:08:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:08:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:08:10 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:55 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:56 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29012b384b25080b769b29d87f60ab473b8d98b32012af3173368ef1ad4371ff`  
		Last Modified: Thu, 11 Jan 2024 06:11:34 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8c818ffc318228bb2a0b6beb3cb15f26dc0f9c238f33ae36a4112a2473e64a`  
		Last Modified: Thu, 11 Jan 2024 06:11:34 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8324b0159e9b83e62618362ce15ae215b63dc7ff3dff8ab7470fbf148a54e36`  
		Last Modified: Thu, 11 Jan 2024 06:11:49 GMT  
		Size: 389.4 MB (389438540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1f408c92b56a47ad4beda82085777562fc33368d2d9f8bb1c39556a6e06c891
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.2 MB (563162394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d90cc33b79544292ea903466ff4ee66e4037f282a2b069383fdbbd6857e2f8a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:22:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:22:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:22:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:22:30 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:23:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:23:00 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:23:01 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:23:01 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:23:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:23:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af3b5c7d496bb91413fd4067043bec0f3df4c6de6fa33ec87a8bb2cb57f317f`  
		Last Modified: Thu, 11 Jan 2024 06:25:25 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230a8cb6522c827881b04d2a1b535850d0614c5b93f6fa0ccdd3a1bfc967eb59`  
		Last Modified: Thu, 11 Jan 2024 06:25:26 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ef547d1254408c8a5346cdf3e916f9a2d29a346839165f58681a0750f738fa`  
		Last Modified: Thu, 11 Jan 2024 06:25:38 GMT  
		Size: 389.4 MB (389403266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:127497f652e5686c4d64fe2be75b28d32c9d13286efd55e5515bc985e8e40690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1e3d6345fc8fb0eb6d82490041cd7ec2e08b8528f2bbc3109c854b0f98318bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565743747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9437581c6b72c901dd9545a1b9b20a18f966a00b860564aaa51e70c441e7b8e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:08:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:08:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:08:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:08:10 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:55 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:56 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29012b384b25080b769b29d87f60ab473b8d98b32012af3173368ef1ad4371ff`  
		Last Modified: Thu, 11 Jan 2024 06:11:34 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8c818ffc318228bb2a0b6beb3cb15f26dc0f9c238f33ae36a4112a2473e64a`  
		Last Modified: Thu, 11 Jan 2024 06:11:34 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8324b0159e9b83e62618362ce15ae215b63dc7ff3dff8ab7470fbf148a54e36`  
		Last Modified: Thu, 11 Jan 2024 06:11:49 GMT  
		Size: 389.4 MB (389438540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1f408c92b56a47ad4beda82085777562fc33368d2d9f8bb1c39556a6e06c891
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.2 MB (563162394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d90cc33b79544292ea903466ff4ee66e4037f282a2b069383fdbbd6857e2f8a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:22:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:22:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:22:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:22:30 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:23:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:23:00 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:23:01 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:23:01 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:23:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:23:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af3b5c7d496bb91413fd4067043bec0f3df4c6de6fa33ec87a8bb2cb57f317f`  
		Last Modified: Thu, 11 Jan 2024 06:25:25 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230a8cb6522c827881b04d2a1b535850d0614c5b93f6fa0ccdd3a1bfc967eb59`  
		Last Modified: Thu, 11 Jan 2024 06:25:26 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ef547d1254408c8a5346cdf3e916f9a2d29a346839165f58681a0750f738fa`  
		Last Modified: Thu, 11 Jan 2024 06:25:38 GMT  
		Size: 389.4 MB (389403266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15.0-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:a0cae6f4624183fa45cb85bc2b31748016148bd01311f65c33e5ec186bee8dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15.0-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:243df31dc47f3f16850e55572e857edf9f6c6c8e4801b430be9bd4acf80f3094
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.0 MB (578017303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c400c424063b58e226df5c615cc3f4c55be5863972121be57dca869808d40435`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:7f7df342ffd2955c9678013b3f777c87b323653d27236a9e1db2138fb7d52c3a in / 
# Wed, 03 Jan 2024 02:28:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:05 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:05 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:2404cd050b85acd3a327d3a58d0ec7bfda5f799f72f681d7f9cd48d64d0fb171 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:aec12625f757d84dbf50e30bbdd719c35331419fcfef0309bcc46e532c8f8c75 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:06 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:08 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 01:40:58 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 01:43:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 01:43:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 01:43:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 01:43:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 01:43:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 01:43:34 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 01:43:34 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 01:43:34 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 01:43:34 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 01:43:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 01:43:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b08c51af1a038ce2a6ca7097b2fbc332c78d5e0e85f2049859341da594558f63`  
		Last Modified: Wed, 10 Jan 2024 18:45:10 GMT  
		Size: 39.3 MB (39337272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e783b5d61e3cc6aa5413af0e608a66e1b7714ff3c3c9d7dabf5a0cd4b63e53e`  
		Last Modified: Sat, 13 Jan 2024 01:44:27 GMT  
		Size: 152.2 MB (152164797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68fd23edb2d9b49aec29b82d959df19e70f963346e257ec44eca21b2b4f8d3b1`  
		Last Modified: Sat, 13 Jan 2024 01:44:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf0491e1bd7f1a00786edb4049d0156ee59800c03e6e827b10bb68656c19601`  
		Last Modified: Sat, 13 Jan 2024 01:45:01 GMT  
		Size: 386.5 MB (386505744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15.0-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:712debf8f7763ddef037ad684929d2e7222b83a6a7be3733691b897148480d73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.9 MB (574886737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f864c73a20b6934ada25a7991897d1e7676c75016ef0ebf29f05b350ec72a2f0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:02 GMT
ADD file:44d847d928ee6a2f89f63e8a4d8911ad5f06ca8d03614b92f771437b7af97a93 in / 
# Wed, 03 Jan 2024 02:28:03 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:04 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:04 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:04 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:732275022803e0afa209662684138de795a06022f8b219d6fc37652986ecd682 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:bd521bacd38743c2200dc36ae2ef5224c3aec5086b9fab8e40ae3295fcd4398f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:06 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:08 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:09 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 02:01:05 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 02:03:02 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 02:03:13 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 02:03:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 02:03:13 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 02:03:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 02:03:24 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 02:03:24 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 02:03:24 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 02:03:25 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 02:03:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 02:03:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:da34b6d716bae3dbcb7925078ba70c246964d3569631d06767906fc030e3282b`  
		Last Modified: Wed, 10 Jan 2024 18:53:17 GMT  
		Size: 37.6 MB (37648974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae574271df94eab1939b41b3e3e5e5dc6b9aeef55608e3a9aeca6d9cfa53fff`  
		Last Modified: Sat, 13 Jan 2024 02:04:10 GMT  
		Size: 150.7 MB (150722468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6250a684ece16d1e9a0387114dc0c7f5d11f9abde1bcc7dc70f18355fc9dd00f`  
		Last Modified: Sat, 13 Jan 2024 02:04:29 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a8cbe41783ac22a0eb802fdefc9a8d1c814c290996330bb6cd7ac6749c9330`  
		Last Modified: Sat, 13 Jan 2024 02:04:41 GMT  
		Size: 386.5 MB (386505811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15.0-ubi8`

```console
$ docker pull neo4j@sha256:edf7ddeb1c0676261b41fe0f6b131e63e0c1ff828bb537aeb6bcdf1794dde41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15.0-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:b466350737ba1171ce7f377e8fbf78ef0b2a7c5c661dca0478122b4bd3b78cb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304130411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25d10559bd3b0b69abd5f5df711610d7494cf7ef6b4f17b1a1d124e6a862619`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:7f7df342ffd2955c9678013b3f777c87b323653d27236a9e1db2138fb7d52c3a in / 
# Wed, 03 Jan 2024 02:28:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:05 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:05 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:2404cd050b85acd3a327d3a58d0ec7bfda5f799f72f681d7f9cd48d64d0fb171 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:aec12625f757d84dbf50e30bbdd719c35331419fcfef0309bcc46e532c8f8c75 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:06 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:08 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 01:40:58 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 01:43:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 01:43:02 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 01:43:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 01:43:03 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 01:43:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 01:43:07 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 01:43:07 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 01:43:07 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 01:43:07 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 01:43:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 01:43:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b08c51af1a038ce2a6ca7097b2fbc332c78d5e0e85f2049859341da594558f63`  
		Last Modified: Wed, 10 Jan 2024 18:45:10 GMT  
		Size: 39.3 MB (39337272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e783b5d61e3cc6aa5413af0e608a66e1b7714ff3c3c9d7dabf5a0cd4b63e53e`  
		Last Modified: Sat, 13 Jan 2024 01:44:27 GMT  
		Size: 152.2 MB (152164797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe40d93c58c2e41c08a2f0840996e983e2e40c906a51710a1af4a7e21c07ff2c`  
		Last Modified: Sat, 13 Jan 2024 01:44:08 GMT  
		Size: 9.5 KB (9493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e125dbbe0ae6f46ef283205e2e73d2b9f23bae4ed3162c18a55ad3bf9c47c8`  
		Last Modified: Sat, 13 Jan 2024 01:44:14 GMT  
		Size: 112.6 MB (112618849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15.0-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d6d0486b92e2504cd59f19696baa62760d8b3e5e5057255f96241d696e035908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300999716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06a77249e68c2e72a2bdff6a80e59c7d8b5c5400b02c0babd09335ba9b58d17`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:02 GMT
ADD file:44d847d928ee6a2f89f63e8a4d8911ad5f06ca8d03614b92f771437b7af97a93 in / 
# Wed, 03 Jan 2024 02:28:03 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:04 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:04 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:04 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:732275022803e0afa209662684138de795a06022f8b219d6fc37652986ecd682 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:bd521bacd38743c2200dc36ae2ef5224c3aec5086b9fab8e40ae3295fcd4398f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:06 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:08 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:09 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 02:01:05 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 02:03:02 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 02:03:05 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 02:03:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 02:03:05 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 02:03:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 02:03:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 02:03:09 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 02:03:09 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 02:03:09 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 02:03:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 02:03:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:da34b6d716bae3dbcb7925078ba70c246964d3569631d06767906fc030e3282b`  
		Last Modified: Wed, 10 Jan 2024 18:53:17 GMT  
		Size: 37.6 MB (37648974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae574271df94eab1939b41b3e3e5e5dc6b9aeef55608e3a9aeca6d9cfa53fff`  
		Last Modified: Sat, 13 Jan 2024 02:04:10 GMT  
		Size: 150.7 MB (150722468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609c3489b4ed27bfdbb91801da65a8cef9acb74935558997a096fd8caa8738c3`  
		Last Modified: Sat, 13 Jan 2024 02:03:55 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e5cbbedc29000984b29c7e1799687e4fe68fe09f4527d13ac808b9050eb47b`  
		Last Modified: Sat, 13 Jan 2024 02:03:59 GMT  
		Size: 112.6 MB (112618784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:0a3c9c4eb4cb09bd30ddae5ded33edba2bdaa1d1f263709e3b834fc9040c9d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2377f4203c56c5b139694c96e7324c78d22befb7a0d5c479baa3539494c1b65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291851185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc8fa1b57980bdf08750d60d432b37508e82d5f9f6a63ac9373e2c5598353f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:07:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:07:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:05 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:06 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05509e4b1c34bdb466397876153ead4ecbdc03389deadbb9b72f758e9841a51`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a316564fdae6d2d92ab40ff74bbd79b03c9837463e521a576eeb1d51ffe14bd7`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffffa9c686d1675f116635f73719a4267f8149f487c624f3dd3fc0d64add3706`  
		Last Modified: Thu, 11 Jan 2024 06:11:02 GMT  
		Size: 115.5 MB (115545976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1fe91b7489538e32154a8cc6388b6bed98806360bd57ea143cf50e6465e6bb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4e6f4de772f3b4c752d7df0f5dc81f54e45dbc474daa0cbe740d01f7f6bdb4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:21:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:21:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:21:55 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:22:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:22:21 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:22:21 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:22:21 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:22:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:22:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af1789ab5680e3789b3db8df3c09f623907aacbc747237e0bfa42437b4e5ed4`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ff6b54382050e5e495f1807b96e890e32936115d55df0892d42b47fb5ad9dc`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acf82b1dfc10fb2132b6abedd93a9b5beed9845fdeddf980134e2b1e69a820e`  
		Last Modified: Thu, 11 Jan 2024 06:24:46 GMT  
		Size: 115.5 MB (115515864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:0a3c9c4eb4cb09bd30ddae5ded33edba2bdaa1d1f263709e3b834fc9040c9d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:2377f4203c56c5b139694c96e7324c78d22befb7a0d5c479baa3539494c1b65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291851185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc8fa1b57980bdf08750d60d432b37508e82d5f9f6a63ac9373e2c5598353f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:07:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:07:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:05 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:06 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05509e4b1c34bdb466397876153ead4ecbdc03389deadbb9b72f758e9841a51`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a316564fdae6d2d92ab40ff74bbd79b03c9837463e521a576eeb1d51ffe14bd7`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffffa9c686d1675f116635f73719a4267f8149f487c624f3dd3fc0d64add3706`  
		Last Modified: Thu, 11 Jan 2024 06:11:02 GMT  
		Size: 115.5 MB (115545976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1fe91b7489538e32154a8cc6388b6bed98806360bd57ea143cf50e6465e6bb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4e6f4de772f3b4c752d7df0f5dc81f54e45dbc474daa0cbe740d01f7f6bdb4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:21:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:21:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:21:55 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:22:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:22:21 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:22:21 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:22:21 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:22:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:22:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af1789ab5680e3789b3db8df3c09f623907aacbc747237e0bfa42437b4e5ed4`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ff6b54382050e5e495f1807b96e890e32936115d55df0892d42b47fb5ad9dc`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acf82b1dfc10fb2132b6abedd93a9b5beed9845fdeddf980134e2b1e69a820e`  
		Last Modified: Thu, 11 Jan 2024 06:24:46 GMT  
		Size: 115.5 MB (115515864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:0a3c9c4eb4cb09bd30ddae5ded33edba2bdaa1d1f263709e3b834fc9040c9d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2377f4203c56c5b139694c96e7324c78d22befb7a0d5c479baa3539494c1b65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291851185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc8fa1b57980bdf08750d60d432b37508e82d5f9f6a63ac9373e2c5598353f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:07:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:07:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:05 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:06 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05509e4b1c34bdb466397876153ead4ecbdc03389deadbb9b72f758e9841a51`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a316564fdae6d2d92ab40ff74bbd79b03c9837463e521a576eeb1d51ffe14bd7`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffffa9c686d1675f116635f73719a4267f8149f487c624f3dd3fc0d64add3706`  
		Last Modified: Thu, 11 Jan 2024 06:11:02 GMT  
		Size: 115.5 MB (115545976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1fe91b7489538e32154a8cc6388b6bed98806360bd57ea143cf50e6465e6bb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4e6f4de772f3b4c752d7df0f5dc81f54e45dbc474daa0cbe740d01f7f6bdb4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:21:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:21:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:21:55 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:22:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:22:21 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:22:21 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:22:21 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:22:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:22:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af1789ab5680e3789b3db8df3c09f623907aacbc747237e0bfa42437b4e5ed4`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ff6b54382050e5e495f1807b96e890e32936115d55df0892d42b47fb5ad9dc`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acf82b1dfc10fb2132b6abedd93a9b5beed9845fdeddf980134e2b1e69a820e`  
		Last Modified: Thu, 11 Jan 2024 06:24:46 GMT  
		Size: 115.5 MB (115515864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:edf7ddeb1c0676261b41fe0f6b131e63e0c1ff828bb537aeb6bcdf1794dde41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:b466350737ba1171ce7f377e8fbf78ef0b2a7c5c661dca0478122b4bd3b78cb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304130411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25d10559bd3b0b69abd5f5df711610d7494cf7ef6b4f17b1a1d124e6a862619`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:7f7df342ffd2955c9678013b3f777c87b323653d27236a9e1db2138fb7d52c3a in / 
# Wed, 03 Jan 2024 02:28:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:05 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:05 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:2404cd050b85acd3a327d3a58d0ec7bfda5f799f72f681d7f9cd48d64d0fb171 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:aec12625f757d84dbf50e30bbdd719c35331419fcfef0309bcc46e532c8f8c75 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:06 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:08 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 01:40:58 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 01:43:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 01:43:02 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 01:43:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 01:43:03 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 01:43:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 01:43:07 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 01:43:07 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 01:43:07 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 01:43:07 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 01:43:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 01:43:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b08c51af1a038ce2a6ca7097b2fbc332c78d5e0e85f2049859341da594558f63`  
		Last Modified: Wed, 10 Jan 2024 18:45:10 GMT  
		Size: 39.3 MB (39337272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e783b5d61e3cc6aa5413af0e608a66e1b7714ff3c3c9d7dabf5a0cd4b63e53e`  
		Last Modified: Sat, 13 Jan 2024 01:44:27 GMT  
		Size: 152.2 MB (152164797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe40d93c58c2e41c08a2f0840996e983e2e40c906a51710a1af4a7e21c07ff2c`  
		Last Modified: Sat, 13 Jan 2024 01:44:08 GMT  
		Size: 9.5 KB (9493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e125dbbe0ae6f46ef283205e2e73d2b9f23bae4ed3162c18a55ad3bf9c47c8`  
		Last Modified: Sat, 13 Jan 2024 01:44:14 GMT  
		Size: 112.6 MB (112618849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d6d0486b92e2504cd59f19696baa62760d8b3e5e5057255f96241d696e035908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300999716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06a77249e68c2e72a2bdff6a80e59c7d8b5c5400b02c0babd09335ba9b58d17`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:02 GMT
ADD file:44d847d928ee6a2f89f63e8a4d8911ad5f06ca8d03614b92f771437b7af97a93 in / 
# Wed, 03 Jan 2024 02:28:03 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:04 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:04 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:04 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:732275022803e0afa209662684138de795a06022f8b219d6fc37652986ecd682 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:bd521bacd38743c2200dc36ae2ef5224c3aec5086b9fab8e40ae3295fcd4398f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:06 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:08 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:09 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 02:01:05 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 02:03:02 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 02:03:05 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 02:03:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 02:03:05 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 02:03:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 02:03:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 02:03:09 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 02:03:09 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 02:03:09 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 02:03:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 02:03:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:da34b6d716bae3dbcb7925078ba70c246964d3569631d06767906fc030e3282b`  
		Last Modified: Wed, 10 Jan 2024 18:53:17 GMT  
		Size: 37.6 MB (37648974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae574271df94eab1939b41b3e3e5e5dc6b9aeef55608e3a9aeca6d9cfa53fff`  
		Last Modified: Sat, 13 Jan 2024 02:04:10 GMT  
		Size: 150.7 MB (150722468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609c3489b4ed27bfdbb91801da65a8cef9acb74935558997a096fd8caa8738c3`  
		Last Modified: Sat, 13 Jan 2024 02:03:55 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e5cbbedc29000984b29c7e1799687e4fe68fe09f4527d13ac808b9050eb47b`  
		Last Modified: Sat, 13 Jan 2024 02:03:59 GMT  
		Size: 112.6 MB (112618784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:127497f652e5686c4d64fe2be75b28d32c9d13286efd55e5515bc985e8e40690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1e3d6345fc8fb0eb6d82490041cd7ec2e08b8528f2bbc3109c854b0f98318bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565743747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9437581c6b72c901dd9545a1b9b20a18f966a00b860564aaa51e70c441e7b8e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:08:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:08:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:08:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:08:10 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:55 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:56 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29012b384b25080b769b29d87f60ab473b8d98b32012af3173368ef1ad4371ff`  
		Last Modified: Thu, 11 Jan 2024 06:11:34 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8c818ffc318228bb2a0b6beb3cb15f26dc0f9c238f33ae36a4112a2473e64a`  
		Last Modified: Thu, 11 Jan 2024 06:11:34 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8324b0159e9b83e62618362ce15ae215b63dc7ff3dff8ab7470fbf148a54e36`  
		Last Modified: Thu, 11 Jan 2024 06:11:49 GMT  
		Size: 389.4 MB (389438540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1f408c92b56a47ad4beda82085777562fc33368d2d9f8bb1c39556a6e06c891
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.2 MB (563162394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d90cc33b79544292ea903466ff4ee66e4037f282a2b069383fdbbd6857e2f8a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:22:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:22:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:22:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:22:30 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:23:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:23:00 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:23:01 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:23:01 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:23:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:23:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af3b5c7d496bb91413fd4067043bec0f3df4c6de6fa33ec87a8bb2cb57f317f`  
		Last Modified: Thu, 11 Jan 2024 06:25:25 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230a8cb6522c827881b04d2a1b535850d0614c5b93f6fa0ccdd3a1bfc967eb59`  
		Last Modified: Thu, 11 Jan 2024 06:25:26 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ef547d1254408c8a5346cdf3e916f9a2d29a346839165f58681a0750f738fa`  
		Last Modified: Thu, 11 Jan 2024 06:25:38 GMT  
		Size: 389.4 MB (389403266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:127497f652e5686c4d64fe2be75b28d32c9d13286efd55e5515bc985e8e40690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1e3d6345fc8fb0eb6d82490041cd7ec2e08b8528f2bbc3109c854b0f98318bb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565743747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9437581c6b72c901dd9545a1b9b20a18f966a00b860564aaa51e70c441e7b8e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:08:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:08:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:08:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:08:10 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:55 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:56 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29012b384b25080b769b29d87f60ab473b8d98b32012af3173368ef1ad4371ff`  
		Last Modified: Thu, 11 Jan 2024 06:11:34 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8c818ffc318228bb2a0b6beb3cb15f26dc0f9c238f33ae36a4112a2473e64a`  
		Last Modified: Thu, 11 Jan 2024 06:11:34 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8324b0159e9b83e62618362ce15ae215b63dc7ff3dff8ab7470fbf148a54e36`  
		Last Modified: Thu, 11 Jan 2024 06:11:49 GMT  
		Size: 389.4 MB (389438540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1f408c92b56a47ad4beda82085777562fc33368d2d9f8bb1c39556a6e06c891
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.2 MB (563162394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d90cc33b79544292ea903466ff4ee66e4037f282a2b069383fdbbd6857e2f8a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:22:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:22:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:22:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:22:30 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:23:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:23:00 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:23:01 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:23:01 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:23:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:23:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af3b5c7d496bb91413fd4067043bec0f3df4c6de6fa33ec87a8bb2cb57f317f`  
		Last Modified: Thu, 11 Jan 2024 06:25:25 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230a8cb6522c827881b04d2a1b535850d0614c5b93f6fa0ccdd3a1bfc967eb59`  
		Last Modified: Thu, 11 Jan 2024 06:25:26 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ef547d1254408c8a5346cdf3e916f9a2d29a346839165f58681a0750f738fa`  
		Last Modified: Thu, 11 Jan 2024 06:25:38 GMT  
		Size: 389.4 MB (389403266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:a0cae6f4624183fa45cb85bc2b31748016148bd01311f65c33e5ec186bee8dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:243df31dc47f3f16850e55572e857edf9f6c6c8e4801b430be9bd4acf80f3094
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.0 MB (578017303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c400c424063b58e226df5c615cc3f4c55be5863972121be57dca869808d40435`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:7f7df342ffd2955c9678013b3f777c87b323653d27236a9e1db2138fb7d52c3a in / 
# Wed, 03 Jan 2024 02:28:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:05 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:05 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:2404cd050b85acd3a327d3a58d0ec7bfda5f799f72f681d7f9cd48d64d0fb171 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:aec12625f757d84dbf50e30bbdd719c35331419fcfef0309bcc46e532c8f8c75 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:06 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:08 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 01:40:58 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 01:43:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 01:43:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 01:43:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 01:43:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 01:43:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 01:43:34 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 01:43:34 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 01:43:34 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 01:43:34 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 01:43:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 01:43:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b08c51af1a038ce2a6ca7097b2fbc332c78d5e0e85f2049859341da594558f63`  
		Last Modified: Wed, 10 Jan 2024 18:45:10 GMT  
		Size: 39.3 MB (39337272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e783b5d61e3cc6aa5413af0e608a66e1b7714ff3c3c9d7dabf5a0cd4b63e53e`  
		Last Modified: Sat, 13 Jan 2024 01:44:27 GMT  
		Size: 152.2 MB (152164797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68fd23edb2d9b49aec29b82d959df19e70f963346e257ec44eca21b2b4f8d3b1`  
		Last Modified: Sat, 13 Jan 2024 01:44:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf0491e1bd7f1a00786edb4049d0156ee59800c03e6e827b10bb68656c19601`  
		Last Modified: Sat, 13 Jan 2024 01:45:01 GMT  
		Size: 386.5 MB (386505744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:712debf8f7763ddef037ad684929d2e7222b83a6a7be3733691b897148480d73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.9 MB (574886737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f864c73a20b6934ada25a7991897d1e7676c75016ef0ebf29f05b350ec72a2f0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:02 GMT
ADD file:44d847d928ee6a2f89f63e8a4d8911ad5f06ca8d03614b92f771437b7af97a93 in / 
# Wed, 03 Jan 2024 02:28:03 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:04 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:04 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:04 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:732275022803e0afa209662684138de795a06022f8b219d6fc37652986ecd682 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:bd521bacd38743c2200dc36ae2ef5224c3aec5086b9fab8e40ae3295fcd4398f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:06 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:08 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:09 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 02:01:05 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 02:03:02 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 02:03:13 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 02:03:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 02:03:13 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 02:03:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 02:03:24 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 02:03:24 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 02:03:24 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 02:03:25 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 02:03:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 02:03:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:da34b6d716bae3dbcb7925078ba70c246964d3569631d06767906fc030e3282b`  
		Last Modified: Wed, 10 Jan 2024 18:53:17 GMT  
		Size: 37.6 MB (37648974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae574271df94eab1939b41b3e3e5e5dc6b9aeef55608e3a9aeca6d9cfa53fff`  
		Last Modified: Sat, 13 Jan 2024 02:04:10 GMT  
		Size: 150.7 MB (150722468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6250a684ece16d1e9a0387114dc0c7f5d11f9abde1bcc7dc70f18355fc9dd00f`  
		Last Modified: Sat, 13 Jan 2024 02:04:29 GMT  
		Size: 9.5 KB (9484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a8cbe41783ac22a0eb802fdefc9a8d1c814c290996330bb6cd7ac6749c9330`  
		Last Modified: Sat, 13 Jan 2024 02:04:41 GMT  
		Size: 386.5 MB (386505811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:0a3c9c4eb4cb09bd30ddae5ded33edba2bdaa1d1f263709e3b834fc9040c9d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:2377f4203c56c5b139694c96e7324c78d22befb7a0d5c479baa3539494c1b65e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291851185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebc8fa1b57980bdf08750d60d432b37508e82d5f9f6a63ac9373e2c5598353f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:07:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:07:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:07:35 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:08:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:08:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:08:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:08:05 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:08:06 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:08:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:08:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05509e4b1c34bdb466397876153ead4ecbdc03389deadbb9b72f758e9841a51`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a316564fdae6d2d92ab40ff74bbd79b03c9837463e521a576eeb1d51ffe14bd7`  
		Last Modified: Thu, 11 Jan 2024 06:10:56 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffffa9c686d1675f116635f73719a4267f8149f487c624f3dd3fc0d64add3706`  
		Last Modified: Thu, 11 Jan 2024 06:11:02 GMT  
		Size: 115.5 MB (115545976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e1fe91b7489538e32154a8cc6388b6bed98806360bd57ea143cf50e6465e6bb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4e6f4de772f3b4c752d7df0f5dc81f54e45dbc474daa0cbe740d01f7f6bdb4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 06:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 11 Jan 2024 06:21:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Thu, 11 Jan 2024 06:21:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 11 Jan 2024 06:21:55 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 11 Jan 2024 06:22:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 11 Jan 2024 06:22:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 06:22:21 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jan 2024 06:22:21 GMT
VOLUME [/data /logs]
# Thu, 11 Jan 2024 06:22:21 GMT
EXPOSE 7473 7474 7687
# Thu, 11 Jan 2024 06:22:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:22:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af1789ab5680e3789b3db8df3c09f623907aacbc747237e0bfa42437b4e5ed4`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ff6b54382050e5e495f1807b96e890e32936115d55df0892d42b47fb5ad9dc`  
		Last Modified: Thu, 11 Jan 2024 06:24:41 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acf82b1dfc10fb2132b6abedd93a9b5beed9845fdeddf980134e2b1e69a820e`  
		Last Modified: Thu, 11 Jan 2024 06:24:46 GMT  
		Size: 115.5 MB (115515864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:edf7ddeb1c0676261b41fe0f6b131e63e0c1ff828bb537aeb6bcdf1794dde41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:b466350737ba1171ce7f377e8fbf78ef0b2a7c5c661dca0478122b4bd3b78cb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304130411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25d10559bd3b0b69abd5f5df711610d7494cf7ef6b4f17b1a1d124e6a862619`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:7f7df342ffd2955c9678013b3f777c87b323653d27236a9e1db2138fb7d52c3a in / 
# Wed, 03 Jan 2024 02:28:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:05 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:05 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:2404cd050b85acd3a327d3a58d0ec7bfda5f799f72f681d7f9cd48d64d0fb171 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:06 GMT
ADD file:aec12625f757d84dbf50e30bbdd719c35331419fcfef0309bcc46e532c8f8c75 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:06 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:07 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:08 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 01:40:58 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 01:43:01 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 01:43:02 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 01:43:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 01:43:03 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 01:43:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 01:43:07 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 01:43:07 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 01:43:07 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 01:43:07 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 01:43:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 01:43:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b08c51af1a038ce2a6ca7097b2fbc332c78d5e0e85f2049859341da594558f63`  
		Last Modified: Wed, 10 Jan 2024 18:45:10 GMT  
		Size: 39.3 MB (39337272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e783b5d61e3cc6aa5413af0e608a66e1b7714ff3c3c9d7dabf5a0cd4b63e53e`  
		Last Modified: Sat, 13 Jan 2024 01:44:27 GMT  
		Size: 152.2 MB (152164797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe40d93c58c2e41c08a2f0840996e983e2e40c906a51710a1af4a7e21c07ff2c`  
		Last Modified: Sat, 13 Jan 2024 01:44:08 GMT  
		Size: 9.5 KB (9493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e125dbbe0ae6f46ef283205e2e73d2b9f23bae4ed3162c18a55ad3bf9c47c8`  
		Last Modified: Sat, 13 Jan 2024 01:44:14 GMT  
		Size: 112.6 MB (112618849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d6d0486b92e2504cd59f19696baa62760d8b3e5e5057255f96241d696e035908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300999716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06a77249e68c2e72a2bdff6a80e59c7d8b5c5400b02c0babd09335ba9b58d17`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 Jan 2024 02:28:02 GMT
ADD file:44d847d928ee6a2f89f63e8a4d8911ad5f06ca8d03614b92f771437b7af97a93 in / 
# Wed, 03 Jan 2024 02:28:03 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 03 Jan 2024 02:28:04 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 03 Jan 2024 02:28:04 GMT
ADD multi:d5b484313b227467de5b0ffa3d38c602093c421f02ba060b0fc9353e374f6517 in /etc/yum.repos.d/ 
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Jan 2024 02:28:04 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 03 Jan 2024 02:28:04 GMT
ENV container oci
# Wed, 03 Jan 2024 02:28:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Jan 2024 02:28:04 GMT
CMD ["/bin/bash"]
# Wed, 03 Jan 2024 02:28:05 GMT
RUN rm -rf /var/log/*
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL release=1108
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:732275022803e0afa209662684138de795a06022f8b219d6fc37652986ecd682 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.json 
# Wed, 03 Jan 2024 02:28:05 GMT
ADD file:bd521bacd38743c2200dc36ae2ef5224c3aec5086b9fab8e40ae3295fcd4398f in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108 
# Wed, 03 Jan 2024 02:28:05 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-03T02:09:22" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108"
# Wed, 03 Jan 2024 02:28:06 GMT
RUN rm -f '/etc/yum.repos.d/repo-9816f.repo' '/etc/yum.repos.d/repo-7a3a9.repo'
# Wed, 03 Jan 2024 02:28:08 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 03 Jan 2024 02:28:09 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 13 Jan 2024 02:01:05 GMT
ENV JAVA_HOME=/usr
# Sat, 13 Jan 2024 02:03:02 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Sat, 13 Jan 2024 02:03:05 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 13 Jan 2024 02:03:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Sat, 13 Jan 2024 02:03:05 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 13 Jan 2024 02:03:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 13 Jan 2024 02:03:09 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jan 2024 02:03:09 GMT
WORKDIR /var/lib/neo4j
# Sat, 13 Jan 2024 02:03:09 GMT
VOLUME [/data /logs]
# Sat, 13 Jan 2024 02:03:09 GMT
EXPOSE 7473 7474 7687
# Sat, 13 Jan 2024 02:03:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 13 Jan 2024 02:03:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:da34b6d716bae3dbcb7925078ba70c246964d3569631d06767906fc030e3282b`  
		Last Modified: Wed, 10 Jan 2024 18:53:17 GMT  
		Size: 37.6 MB (37648974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae574271df94eab1939b41b3e3e5e5dc6b9aeef55608e3a9aeca6d9cfa53fff`  
		Last Modified: Sat, 13 Jan 2024 02:04:10 GMT  
		Size: 150.7 MB (150722468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609c3489b4ed27bfdbb91801da65a8cef9acb74935558997a096fd8caa8738c3`  
		Last Modified: Sat, 13 Jan 2024 02:03:55 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e5cbbedc29000984b29c7e1799687e4fe68fe09f4527d13ac808b9050eb47b`  
		Last Modified: Sat, 13 Jan 2024 02:03:59 GMT  
		Size: 112.6 MB (112618784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
