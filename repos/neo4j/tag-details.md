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
-	[`neo4j:5.16`](#neo4j516)
-	[`neo4j:5.16-bullseye`](#neo4j516-bullseye)
-	[`neo4j:5.16-community`](#neo4j516-community)
-	[`neo4j:5.16-community-bullseye`](#neo4j516-community-bullseye)
-	[`neo4j:5.16-community-ubi8`](#neo4j516-community-ubi8)
-	[`neo4j:5.16-enterprise`](#neo4j516-enterprise)
-	[`neo4j:5.16-enterprise-bullseye`](#neo4j516-enterprise-bullseye)
-	[`neo4j:5.16-enterprise-ubi8`](#neo4j516-enterprise-ubi8)
-	[`neo4j:5.16-ubi8`](#neo4j516-ubi8)
-	[`neo4j:5.16.0`](#neo4j5160)
-	[`neo4j:5.16.0-bullseye`](#neo4j5160-bullseye)
-	[`neo4j:5.16.0-community`](#neo4j5160-community)
-	[`neo4j:5.16.0-community-bullseye`](#neo4j5160-community-bullseye)
-	[`neo4j:5.16.0-community-ubi8`](#neo4j5160-community-ubi8)
-	[`neo4j:5.16.0-enterprise`](#neo4j5160-enterprise)
-	[`neo4j:5.16.0-enterprise-bullseye`](#neo4j5160-enterprise-bullseye)
-	[`neo4j:5.16.0-enterprise-ubi8`](#neo4j5160-enterprise-ubi8)
-	[`neo4j:5.16.0-ubi8`](#neo4j5160-ubi8)
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
$ docker pull neo4j@sha256:42da788d8ce3a27e8ce244414ec4fea3df56095ab1b25e8572201ae4304c5c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:64e92cbdf4d9e6e6bb3a8ec969eb6f04db784ec14f91255129db31a59b9a2c6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297255836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6713a926c95fc0fce5f04290e5c5620c161143be4668d64a088490eba40e831`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:52:28 GMT
COPY dir:c80966d54ee599fa5b16f964e9342a0dab00f0ed4f5d18b7bebc8a71278b8b40 in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:52:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9aa9af96f80388581f626d9e4b8b4c0f467aefbcac3ea7d9c8cd68025067d076 NEO4J_TARBALL=neo4j-community-4.4.29-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:52:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
# Wed, 17 Jan 2024 09:52:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:52:31 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Wed, 17 Jan 2024 09:52:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:52:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:52:58 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:52:58 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:52:58 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:52:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:52:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9d6ac0f872fa5de31ed0dbba601da225123345990c63c2932d30823ee9dbb6`  
		Last Modified: Wed, 17 Jan 2024 10:00:36 GMT  
		Size: 145.3 MB (145266432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b5b8d14436e160f8897b2a453bada4f3982d6c1de7f5e570b576d54a95b1f7`  
		Last Modified: Wed, 17 Jan 2024 10:00:25 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60104f06cfc737986f3e69a81902703c78efeb49dbf762ca35953f68794fa247`  
		Last Modified: Wed, 17 Jan 2024 10:00:25 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a985b2d45a61039d337122e7bd0b1cd72ae5d35a520f5ef3f529856fc6aa48`  
		Last Modified: Wed, 17 Jan 2024 10:00:31 GMT  
		Size: 120.6 MB (120558171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8c25d6121a78103cbe50916e199ba2891077be5090f82d61b17bba4db63a9874
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292604987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1a1a73bb8f8f493353df84e78b5c34ef76a47fdad49472646289168f3d9a3f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:16:05 GMT
COPY dir:de5568efb2f4de409b0bbafecabebfd7b12106c4b1a8ded40ebb723247056709 in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:16:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9aa9af96f80388581f626d9e4b8b4c0f467aefbcac3ea7d9c8cd68025067d076 NEO4J_TARBALL=neo4j-community-4.4.29-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:16:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
# Wed, 17 Jan 2024 09:16:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:16:09 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Wed, 17 Jan 2024 09:16:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:16:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:16:34 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:16:34 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:16:34 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:16:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:16:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0061069c38442e79937393f0fa9c1f974fd52693e9510fcedd14c9e82de00a`  
		Last Modified: Wed, 17 Jan 2024 09:19:08 GMT  
		Size: 142.0 MB (142002056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f2e68d9966fe5af97c50753a2f8c8a5ef9992de24d862d8e7f5c7c0812f5b7`  
		Last Modified: Wed, 17 Jan 2024 09:18:59 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f0a71cb83f8bd3f6c6a9727032130d7f82c3667950e1d40b6bfeb62f95da05`  
		Last Modified: Wed, 17 Jan 2024 09:18:59 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eff8d9dc9c64eee5a4e82cd3e88e61785ae011e8c8d720dae88f1d4a01ad8c4`  
		Last Modified: Wed, 17 Jan 2024 09:19:05 GMT  
		Size: 120.5 MB (120525612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:42da788d8ce3a27e8ce244414ec4fea3df56095ab1b25e8572201ae4304c5c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:64e92cbdf4d9e6e6bb3a8ec969eb6f04db784ec14f91255129db31a59b9a2c6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297255836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6713a926c95fc0fce5f04290e5c5620c161143be4668d64a088490eba40e831`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:52:28 GMT
COPY dir:c80966d54ee599fa5b16f964e9342a0dab00f0ed4f5d18b7bebc8a71278b8b40 in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:52:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9aa9af96f80388581f626d9e4b8b4c0f467aefbcac3ea7d9c8cd68025067d076 NEO4J_TARBALL=neo4j-community-4.4.29-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:52:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
# Wed, 17 Jan 2024 09:52:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:52:31 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Wed, 17 Jan 2024 09:52:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:52:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:52:58 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:52:58 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:52:58 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:52:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:52:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9d6ac0f872fa5de31ed0dbba601da225123345990c63c2932d30823ee9dbb6`  
		Last Modified: Wed, 17 Jan 2024 10:00:36 GMT  
		Size: 145.3 MB (145266432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b5b8d14436e160f8897b2a453bada4f3982d6c1de7f5e570b576d54a95b1f7`  
		Last Modified: Wed, 17 Jan 2024 10:00:25 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60104f06cfc737986f3e69a81902703c78efeb49dbf762ca35953f68794fa247`  
		Last Modified: Wed, 17 Jan 2024 10:00:25 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a985b2d45a61039d337122e7bd0b1cd72ae5d35a520f5ef3f529856fc6aa48`  
		Last Modified: Wed, 17 Jan 2024 10:00:31 GMT  
		Size: 120.6 MB (120558171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8c25d6121a78103cbe50916e199ba2891077be5090f82d61b17bba4db63a9874
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292604987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1a1a73bb8f8f493353df84e78b5c34ef76a47fdad49472646289168f3d9a3f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:16:05 GMT
COPY dir:de5568efb2f4de409b0bbafecabebfd7b12106c4b1a8ded40ebb723247056709 in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:16:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9aa9af96f80388581f626d9e4b8b4c0f467aefbcac3ea7d9c8cd68025067d076 NEO4J_TARBALL=neo4j-community-4.4.29-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:16:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
# Wed, 17 Jan 2024 09:16:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:16:09 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Wed, 17 Jan 2024 09:16:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:16:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:16:34 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:16:34 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:16:34 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:16:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:16:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0061069c38442e79937393f0fa9c1f974fd52693e9510fcedd14c9e82de00a`  
		Last Modified: Wed, 17 Jan 2024 09:19:08 GMT  
		Size: 142.0 MB (142002056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f2e68d9966fe5af97c50753a2f8c8a5ef9992de24d862d8e7f5c7c0812f5b7`  
		Last Modified: Wed, 17 Jan 2024 09:18:59 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f0a71cb83f8bd3f6c6a9727032130d7f82c3667950e1d40b6bfeb62f95da05`  
		Last Modified: Wed, 17 Jan 2024 09:18:59 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eff8d9dc9c64eee5a4e82cd3e88e61785ae011e8c8d720dae88f1d4a01ad8c4`  
		Last Modified: Wed, 17 Jan 2024 09:19:05 GMT  
		Size: 120.5 MB (120525612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:7a5b32ea84a503cf035d5e305dd849b92cbd37db5dae17dc50fa9f5802a941df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:0cf90935a7889d57c2078771e017b8b77bcc132dc09576523be4e0c8f8875174
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.3 MB (402296267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70786bef7a7bea6cf71922b893acb91ad7b424268ff5427d5a9f222a25b51e24`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:52:28 GMT
COPY dir:c80966d54ee599fa5b16f964e9342a0dab00f0ed4f5d18b7bebc8a71278b8b40 in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:53:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ec65a14a4e43c03a7fc1c6b1bf573cc91ec0d6bd527b183ffbf3f6f5386b120b NEO4J_TARBALL=neo4j-enterprise-4.4.29-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:53:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
# Wed, 17 Jan 2024 09:53:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:53:07 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Wed, 17 Jan 2024 09:53:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:53:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:53:37 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:53:37 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:53:37 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:53:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:53:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9d6ac0f872fa5de31ed0dbba601da225123345990c63c2932d30823ee9dbb6`  
		Last Modified: Wed, 17 Jan 2024 10:00:36 GMT  
		Size: 145.3 MB (145266432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdfc4b6dbf68c589c961217481d4a521aa6c86eeb29e6b06cf8ddc5efc80d436`  
		Last Modified: Wed, 17 Jan 2024 10:01:04 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b00030608aa9db5197b27b8893704085946dfa4e6b233edc32166f948a7cb3`  
		Last Modified: Wed, 17 Jan 2024 10:01:04 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f79ceb7655a05d18c49c4fa06d2279018eaae7fab11f3170730a33cd77c5da`  
		Last Modified: Wed, 17 Jan 2024 10:01:15 GMT  
		Size: 225.6 MB (225598602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7b0336430aa4e487df29c5adc59eeba90fb200a08c476f6277f36eaa04289c6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.6 MB (397638712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028ee792b03d0a5064ef9ca092716c1b760ba194e13f5742da892f71974b244d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:16:05 GMT
COPY dir:de5568efb2f4de409b0bbafecabebfd7b12106c4b1a8ded40ebb723247056709 in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:16:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ec65a14a4e43c03a7fc1c6b1bf573cc91ec0d6bd527b183ffbf3f6f5386b120b NEO4J_TARBALL=neo4j-enterprise-4.4.29-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:16:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
# Wed, 17 Jan 2024 09:16:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:16:43 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Wed, 17 Jan 2024 09:17:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:17:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:17:16 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:17:16 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:17:16 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:17:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:17:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0061069c38442e79937393f0fa9c1f974fd52693e9510fcedd14c9e82de00a`  
		Last Modified: Wed, 17 Jan 2024 09:19:08 GMT  
		Size: 142.0 MB (142002056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9959ab3b6b2e9951ee5da48c6925a8a83a9fee7c4e1ee28934be1ccb5d616846`  
		Last Modified: Wed, 17 Jan 2024 09:19:21 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffd2f5281ba038a0d5ea652181e0e71cc38da41d91f8bf0b3ab0920eb378238`  
		Last Modified: Wed, 17 Jan 2024 09:19:21 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bc7a59b5e450197fd4e8fe7b5ba48afec9ef4e9289de1f9c44e2341513415e`  
		Last Modified: Wed, 17 Jan 2024 09:19:30 GMT  
		Size: 225.6 MB (225559340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.29`

```console
$ docker pull neo4j@sha256:42da788d8ce3a27e8ce244414ec4fea3df56095ab1b25e8572201ae4304c5c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.29` - linux; amd64

```console
$ docker pull neo4j@sha256:64e92cbdf4d9e6e6bb3a8ec969eb6f04db784ec14f91255129db31a59b9a2c6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297255836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6713a926c95fc0fce5f04290e5c5620c161143be4668d64a088490eba40e831`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:52:28 GMT
COPY dir:c80966d54ee599fa5b16f964e9342a0dab00f0ed4f5d18b7bebc8a71278b8b40 in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:52:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9aa9af96f80388581f626d9e4b8b4c0f467aefbcac3ea7d9c8cd68025067d076 NEO4J_TARBALL=neo4j-community-4.4.29-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:52:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
# Wed, 17 Jan 2024 09:52:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:52:31 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Wed, 17 Jan 2024 09:52:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:52:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:52:58 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:52:58 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:52:58 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:52:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:52:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9d6ac0f872fa5de31ed0dbba601da225123345990c63c2932d30823ee9dbb6`  
		Last Modified: Wed, 17 Jan 2024 10:00:36 GMT  
		Size: 145.3 MB (145266432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b5b8d14436e160f8897b2a453bada4f3982d6c1de7f5e570b576d54a95b1f7`  
		Last Modified: Wed, 17 Jan 2024 10:00:25 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60104f06cfc737986f3e69a81902703c78efeb49dbf762ca35953f68794fa247`  
		Last Modified: Wed, 17 Jan 2024 10:00:25 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a985b2d45a61039d337122e7bd0b1cd72ae5d35a520f5ef3f529856fc6aa48`  
		Last Modified: Wed, 17 Jan 2024 10:00:31 GMT  
		Size: 120.6 MB (120558171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.29` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8c25d6121a78103cbe50916e199ba2891077be5090f82d61b17bba4db63a9874
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292604987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1a1a73bb8f8f493353df84e78b5c34ef76a47fdad49472646289168f3d9a3f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:16:05 GMT
COPY dir:de5568efb2f4de409b0bbafecabebfd7b12106c4b1a8ded40ebb723247056709 in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:16:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9aa9af96f80388581f626d9e4b8b4c0f467aefbcac3ea7d9c8cd68025067d076 NEO4J_TARBALL=neo4j-community-4.4.29-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:16:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
# Wed, 17 Jan 2024 09:16:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:16:09 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Wed, 17 Jan 2024 09:16:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:16:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:16:34 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:16:34 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:16:34 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:16:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:16:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0061069c38442e79937393f0fa9c1f974fd52693e9510fcedd14c9e82de00a`  
		Last Modified: Wed, 17 Jan 2024 09:19:08 GMT  
		Size: 142.0 MB (142002056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f2e68d9966fe5af97c50753a2f8c8a5ef9992de24d862d8e7f5c7c0812f5b7`  
		Last Modified: Wed, 17 Jan 2024 09:18:59 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f0a71cb83f8bd3f6c6a9727032130d7f82c3667950e1d40b6bfeb62f95da05`  
		Last Modified: Wed, 17 Jan 2024 09:18:59 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eff8d9dc9c64eee5a4e82cd3e88e61785ae011e8c8d720dae88f1d4a01ad8c4`  
		Last Modified: Wed, 17 Jan 2024 09:19:05 GMT  
		Size: 120.5 MB (120525612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.29-community`

```console
$ docker pull neo4j@sha256:42da788d8ce3a27e8ce244414ec4fea3df56095ab1b25e8572201ae4304c5c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.29-community` - linux; amd64

```console
$ docker pull neo4j@sha256:64e92cbdf4d9e6e6bb3a8ec969eb6f04db784ec14f91255129db31a59b9a2c6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297255836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6713a926c95fc0fce5f04290e5c5620c161143be4668d64a088490eba40e831`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:52:28 GMT
COPY dir:c80966d54ee599fa5b16f964e9342a0dab00f0ed4f5d18b7bebc8a71278b8b40 in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:52:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9aa9af96f80388581f626d9e4b8b4c0f467aefbcac3ea7d9c8cd68025067d076 NEO4J_TARBALL=neo4j-community-4.4.29-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:52:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
# Wed, 17 Jan 2024 09:52:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:52:31 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Wed, 17 Jan 2024 09:52:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:52:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:52:58 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:52:58 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:52:58 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:52:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:52:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9d6ac0f872fa5de31ed0dbba601da225123345990c63c2932d30823ee9dbb6`  
		Last Modified: Wed, 17 Jan 2024 10:00:36 GMT  
		Size: 145.3 MB (145266432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b5b8d14436e160f8897b2a453bada4f3982d6c1de7f5e570b576d54a95b1f7`  
		Last Modified: Wed, 17 Jan 2024 10:00:25 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60104f06cfc737986f3e69a81902703c78efeb49dbf762ca35953f68794fa247`  
		Last Modified: Wed, 17 Jan 2024 10:00:25 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a985b2d45a61039d337122e7bd0b1cd72ae5d35a520f5ef3f529856fc6aa48`  
		Last Modified: Wed, 17 Jan 2024 10:00:31 GMT  
		Size: 120.6 MB (120558171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.29-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8c25d6121a78103cbe50916e199ba2891077be5090f82d61b17bba4db63a9874
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292604987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1a1a73bb8f8f493353df84e78b5c34ef76a47fdad49472646289168f3d9a3f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:16:05 GMT
COPY dir:de5568efb2f4de409b0bbafecabebfd7b12106c4b1a8ded40ebb723247056709 in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:16:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9aa9af96f80388581f626d9e4b8b4c0f467aefbcac3ea7d9c8cd68025067d076 NEO4J_TARBALL=neo4j-community-4.4.29-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:16:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
# Wed, 17 Jan 2024 09:16:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:16:09 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Wed, 17 Jan 2024 09:16:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:16:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:16:34 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:16:34 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:16:34 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:16:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:16:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0061069c38442e79937393f0fa9c1f974fd52693e9510fcedd14c9e82de00a`  
		Last Modified: Wed, 17 Jan 2024 09:19:08 GMT  
		Size: 142.0 MB (142002056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f2e68d9966fe5af97c50753a2f8c8a5ef9992de24d862d8e7f5c7c0812f5b7`  
		Last Modified: Wed, 17 Jan 2024 09:18:59 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f0a71cb83f8bd3f6c6a9727032130d7f82c3667950e1d40b6bfeb62f95da05`  
		Last Modified: Wed, 17 Jan 2024 09:18:59 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eff8d9dc9c64eee5a4e82cd3e88e61785ae011e8c8d720dae88f1d4a01ad8c4`  
		Last Modified: Wed, 17 Jan 2024 09:19:05 GMT  
		Size: 120.5 MB (120525612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.29-enterprise`

```console
$ docker pull neo4j@sha256:7a5b32ea84a503cf035d5e305dd849b92cbd37db5dae17dc50fa9f5802a941df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.29-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:0cf90935a7889d57c2078771e017b8b77bcc132dc09576523be4e0c8f8875174
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.3 MB (402296267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70786bef7a7bea6cf71922b893acb91ad7b424268ff5427d5a9f222a25b51e24`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:52:28 GMT
COPY dir:c80966d54ee599fa5b16f964e9342a0dab00f0ed4f5d18b7bebc8a71278b8b40 in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:53:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ec65a14a4e43c03a7fc1c6b1bf573cc91ec0d6bd527b183ffbf3f6f5386b120b NEO4J_TARBALL=neo4j-enterprise-4.4.29-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:53:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
# Wed, 17 Jan 2024 09:53:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:53:07 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Wed, 17 Jan 2024 09:53:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:53:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:53:37 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:53:37 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:53:37 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:53:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:53:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9d6ac0f872fa5de31ed0dbba601da225123345990c63c2932d30823ee9dbb6`  
		Last Modified: Wed, 17 Jan 2024 10:00:36 GMT  
		Size: 145.3 MB (145266432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdfc4b6dbf68c589c961217481d4a521aa6c86eeb29e6b06cf8ddc5efc80d436`  
		Last Modified: Wed, 17 Jan 2024 10:01:04 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b00030608aa9db5197b27b8893704085946dfa4e6b233edc32166f948a7cb3`  
		Last Modified: Wed, 17 Jan 2024 10:01:04 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f79ceb7655a05d18c49c4fa06d2279018eaae7fab11f3170730a33cd77c5da`  
		Last Modified: Wed, 17 Jan 2024 10:01:15 GMT  
		Size: 225.6 MB (225598602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.29-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7b0336430aa4e487df29c5adc59eeba90fb200a08c476f6277f36eaa04289c6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.6 MB (397638712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028ee792b03d0a5064ef9ca092716c1b760ba194e13f5742da892f71974b244d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:16:05 GMT
COPY dir:de5568efb2f4de409b0bbafecabebfd7b12106c4b1a8ded40ebb723247056709 in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:16:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ec65a14a4e43c03a7fc1c6b1bf573cc91ec0d6bd527b183ffbf3f6f5386b120b NEO4J_TARBALL=neo4j-enterprise-4.4.29-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:16:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
# Wed, 17 Jan 2024 09:16:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:16:43 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Wed, 17 Jan 2024 09:17:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.29-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:17:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:17:16 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:17:16 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:17:16 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:17:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:17:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0061069c38442e79937393f0fa9c1f974fd52693e9510fcedd14c9e82de00a`  
		Last Modified: Wed, 17 Jan 2024 09:19:08 GMT  
		Size: 142.0 MB (142002056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9959ab3b6b2e9951ee5da48c6925a8a83a9fee7c4e1ee28934be1ccb5d616846`  
		Last Modified: Wed, 17 Jan 2024 09:19:21 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffd2f5281ba038a0d5ea652181e0e71cc38da41d91f8bf0b3ab0920eb378238`  
		Last Modified: Wed, 17 Jan 2024 09:19:21 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bc7a59b5e450197fd4e8fe7b5ba48afec9ef4e9289de1f9c44e2341513415e`  
		Last Modified: Wed, 17 Jan 2024 09:19:30 GMT  
		Size: 225.6 MB (225559340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:bed18a4185cd5cf48fb5a3d824e0b186d68c03aa6d742e984f7b057df11e7079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:d89db4d15e32dc6f55d55f9d90c2ee953cd0bef20b30338e8679e391fdae056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291711797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2aa72c09cea9e884de8b27becd2181bd6145213112df161870613dfed3f504`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:18 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:47:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:47:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:47:53 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:47:53 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:47:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:47:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:47:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc3dbe4bb8a8cf8e09e918d254f3aed4b07eefac670122b2b59ae28b9b3b8b`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd92a499088faebaebde741ac37801df615c730d808f6f813c2fb58e0d16bcd0`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525a37b23ba6491d60512c25b46d68c4f02853d322f45ef6baf9c0c2b5aeef79`  
		Last Modified: Mon, 22 Jan 2024 19:49:53 GMT  
		Size: 115.4 MB (115406589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:82911582124ea6c08f4ea4e98c4d0b2787aa4bc70d9bba240b3a74e29f4a2dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289128515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de3e315a5b3cc5cfa640775a133b8da83a690d3e2b2a7b9d41ab6838b55a79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:48:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:18 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:18 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:18 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc3bece22f184494fde29a2c4342f688108f00536363d27f7cb4b15a4406b09`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6163ed4009633c27651dab5010b3dc1a3b8ee4613183a1f51d2f9eb426169f67`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473b967008ef8e7c3d8189a7fbb26b472becf20c4ae78169d1d185d1488b8a1c`  
		Last Modified: Mon, 22 Jan 2024 19:50:45 GMT  
		Size: 115.4 MB (115369417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:bed18a4185cd5cf48fb5a3d824e0b186d68c03aa6d742e984f7b057df11e7079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d89db4d15e32dc6f55d55f9d90c2ee953cd0bef20b30338e8679e391fdae056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291711797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2aa72c09cea9e884de8b27becd2181bd6145213112df161870613dfed3f504`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:18 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:47:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:47:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:47:53 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:47:53 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:47:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:47:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:47:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc3dbe4bb8a8cf8e09e918d254f3aed4b07eefac670122b2b59ae28b9b3b8b`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd92a499088faebaebde741ac37801df615c730d808f6f813c2fb58e0d16bcd0`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525a37b23ba6491d60512c25b46d68c4f02853d322f45ef6baf9c0c2b5aeef79`  
		Last Modified: Mon, 22 Jan 2024 19:49:53 GMT  
		Size: 115.4 MB (115406589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:82911582124ea6c08f4ea4e98c4d0b2787aa4bc70d9bba240b3a74e29f4a2dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289128515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de3e315a5b3cc5cfa640775a133b8da83a690d3e2b2a7b9d41ab6838b55a79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:48:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:18 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:18 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:18 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc3bece22f184494fde29a2c4342f688108f00536363d27f7cb4b15a4406b09`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6163ed4009633c27651dab5010b3dc1a3b8ee4613183a1f51d2f9eb426169f67`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473b967008ef8e7c3d8189a7fbb26b472becf20c4ae78169d1d185d1488b8a1c`  
		Last Modified: Mon, 22 Jan 2024 19:50:45 GMT  
		Size: 115.4 MB (115369417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:bed18a4185cd5cf48fb5a3d824e0b186d68c03aa6d742e984f7b057df11e7079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:d89db4d15e32dc6f55d55f9d90c2ee953cd0bef20b30338e8679e391fdae056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291711797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2aa72c09cea9e884de8b27becd2181bd6145213112df161870613dfed3f504`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:18 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:47:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:47:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:47:53 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:47:53 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:47:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:47:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:47:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc3dbe4bb8a8cf8e09e918d254f3aed4b07eefac670122b2b59ae28b9b3b8b`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd92a499088faebaebde741ac37801df615c730d808f6f813c2fb58e0d16bcd0`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525a37b23ba6491d60512c25b46d68c4f02853d322f45ef6baf9c0c2b5aeef79`  
		Last Modified: Mon, 22 Jan 2024 19:49:53 GMT  
		Size: 115.4 MB (115406589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:82911582124ea6c08f4ea4e98c4d0b2787aa4bc70d9bba240b3a74e29f4a2dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289128515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de3e315a5b3cc5cfa640775a133b8da83a690d3e2b2a7b9d41ab6838b55a79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:48:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:18 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:18 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:18 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc3bece22f184494fde29a2c4342f688108f00536363d27f7cb4b15a4406b09`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6163ed4009633c27651dab5010b3dc1a3b8ee4613183a1f51d2f9eb426169f67`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473b967008ef8e7c3d8189a7fbb26b472becf20c4ae78169d1d185d1488b8a1c`  
		Last Modified: Mon, 22 Jan 2024 19:50:45 GMT  
		Size: 115.4 MB (115369417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:bed18a4185cd5cf48fb5a3d824e0b186d68c03aa6d742e984f7b057df11e7079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d89db4d15e32dc6f55d55f9d90c2ee953cd0bef20b30338e8679e391fdae056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291711797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2aa72c09cea9e884de8b27becd2181bd6145213112df161870613dfed3f504`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:18 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:47:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:47:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:47:53 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:47:53 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:47:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:47:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:47:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc3dbe4bb8a8cf8e09e918d254f3aed4b07eefac670122b2b59ae28b9b3b8b`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd92a499088faebaebde741ac37801df615c730d808f6f813c2fb58e0d16bcd0`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525a37b23ba6491d60512c25b46d68c4f02853d322f45ef6baf9c0c2b5aeef79`  
		Last Modified: Mon, 22 Jan 2024 19:49:53 GMT  
		Size: 115.4 MB (115406589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:82911582124ea6c08f4ea4e98c4d0b2787aa4bc70d9bba240b3a74e29f4a2dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289128515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de3e315a5b3cc5cfa640775a133b8da83a690d3e2b2a7b9d41ab6838b55a79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:48:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:18 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:18 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:18 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc3bece22f184494fde29a2c4342f688108f00536363d27f7cb4b15a4406b09`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6163ed4009633c27651dab5010b3dc1a3b8ee4613183a1f51d2f9eb426169f67`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473b967008ef8e7c3d8189a7fbb26b472becf20c4ae78169d1d185d1488b8a1c`  
		Last Modified: Mon, 22 Jan 2024 19:50:45 GMT  
		Size: 115.4 MB (115369417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:d32aeff2b18878258eaa305da1588e0476a7f7df392519fc983e6de6608d3f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:20c5ca5b4f1ea1482e59dc06348a558b680fa9e0ec6a1f95c88e3c40bef55732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303997821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2997e2fd0b59f0d3851a3905d3a77b89777a21296f402a9135377f0d2f1515f8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:18:20 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:19:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:48:57 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:57 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:01 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b288f2fdef4d0a03dcb62d1fc0cbc844eb2cd220de6a3a99e9d7a725ad3a839`  
		Last Modified: Fri, 19 Jan 2024 01:20:39 GMT  
		Size: 152.2 MB (152169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe2f4fbd6df0ece7afe995953a09fcb7d2d5fe14950f59c766f71f342010168`  
		Last Modified: Mon, 22 Jan 2024 19:51:04 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646b1996cc82c317f0f36b6908ecc9344390135e70b9826145e65519fd9476ee`  
		Last Modified: Mon, 22 Jan 2024 19:51:09 GMT  
		Size: 112.5 MB (112472544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:da93d1e99342156e148fa8242b294f60931971f5fe8e808d32e0916363c79803
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300872225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e9587083dbb641f1b7d1ee0c350c1723d6cdc37fa25341e62d32e4745f3229`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:49:06 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:49:53 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:49:55 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:59 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:59 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:59 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:59 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:50:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:50:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393943727a332ace094e701aa8cd3d1e740a2265b6ad85882a2d6284690d4880`  
		Last Modified: Fri, 19 Jan 2024 01:51:13 GMT  
		Size: 150.7 MB (150737265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5337c3b8f4ecf77b5ee865e36e6c42c8542a3ec620c6105b9a6cb8a7f6cafb`  
		Last Modified: Mon, 22 Jan 2024 19:51:55 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65848330b066709b421d118f0b5d5a3fe033e281e9a2d5ba86f5f37a886432e7`  
		Last Modified: Mon, 22 Jan 2024 19:51:59 GMT  
		Size: 112.5 MB (112472594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:07e21db007ea859b1a809780e298cc7dc3959e5829ee777ae6b3d3b137ab4b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:77a9374c0ca8e878cd26b5d5273c71132473aae2b61da6ff0a6549be297d51fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547731335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1a5abe453f2856e5f2dbed753ffc1356fe54ba921cf7151ce5675db1819d4b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:59 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:48:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:48:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:48:44 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:48:44 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:48:44 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:48:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:48:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a275040e0f8b7fa8958e5f2a55d70e18d1b371e9e9cacb43422445abe21b7d8`  
		Last Modified: Mon, 22 Jan 2024 19:50:28 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38410ce9acd115784289e56f716e16ed6ed418e7937d50f801a500dd1067750`  
		Last Modified: Mon, 22 Jan 2024 19:50:28 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bb32b856508b5fd4974a48407005fdb63abe39b1fe5780f7e72c0f7c2ac7cb`  
		Last Modified: Mon, 22 Jan 2024 19:50:43 GMT  
		Size: 371.4 MB (371426127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ee47ca1b630d41456ed4c1bde04625f2081a9c6e96b27cf061d7852b54f89c8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545154012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf8efd0b2617e45908a7fa3232fbe178d312e6a936d31f7836f2408e6784724`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:49:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:49:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:51 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:52 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:52 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596c61f2a7289c0db2b2f4798b205db39a8245f0487f5f358cc932bb6bc0f68b`  
		Last Modified: Mon, 22 Jan 2024 19:51:21 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0d4d7aea8cb96020ede5c28edefdef6123ca902a0348c723d68402865e7b1a`  
		Last Modified: Mon, 22 Jan 2024 19:51:21 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cd593bb3eaef178cb7a963b0c70c4d07b79e4247a71460f90a26315b53585c`  
		Last Modified: Mon, 22 Jan 2024 19:51:33 GMT  
		Size: 371.4 MB (371394916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:07e21db007ea859b1a809780e298cc7dc3959e5829ee777ae6b3d3b137ab4b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:77a9374c0ca8e878cd26b5d5273c71132473aae2b61da6ff0a6549be297d51fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547731335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1a5abe453f2856e5f2dbed753ffc1356fe54ba921cf7151ce5675db1819d4b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:59 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:48:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:48:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:48:44 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:48:44 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:48:44 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:48:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:48:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a275040e0f8b7fa8958e5f2a55d70e18d1b371e9e9cacb43422445abe21b7d8`  
		Last Modified: Mon, 22 Jan 2024 19:50:28 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38410ce9acd115784289e56f716e16ed6ed418e7937d50f801a500dd1067750`  
		Last Modified: Mon, 22 Jan 2024 19:50:28 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bb32b856508b5fd4974a48407005fdb63abe39b1fe5780f7e72c0f7c2ac7cb`  
		Last Modified: Mon, 22 Jan 2024 19:50:43 GMT  
		Size: 371.4 MB (371426127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ee47ca1b630d41456ed4c1bde04625f2081a9c6e96b27cf061d7852b54f89c8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545154012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf8efd0b2617e45908a7fa3232fbe178d312e6a936d31f7836f2408e6784724`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:49:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:49:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:51 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:52 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:52 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596c61f2a7289c0db2b2f4798b205db39a8245f0487f5f358cc932bb6bc0f68b`  
		Last Modified: Mon, 22 Jan 2024 19:51:21 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0d4d7aea8cb96020ede5c28edefdef6123ca902a0348c723d68402865e7b1a`  
		Last Modified: Mon, 22 Jan 2024 19:51:21 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cd593bb3eaef178cb7a963b0c70c4d07b79e4247a71460f90a26315b53585c`  
		Last Modified: Mon, 22 Jan 2024 19:51:33 GMT  
		Size: 371.4 MB (371394916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:208c3ed5da6cbf2edbe40b2862b7d29eddbd0302342344972c8a33584dd96dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:59fded3746220789b2fdadd2631843ed20b9bc8484612c828c895de0ead03c05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (560021769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1820a8a7e17954c9b2c658e3895657e19ff1247c60ac734cd89d36afca69c6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:18:20 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:19:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:49:04 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:05 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:16 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:16 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:16 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:16 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b288f2fdef4d0a03dcb62d1fc0cbc844eb2cd220de6a3a99e9d7a725ad3a839`  
		Last Modified: Fri, 19 Jan 2024 01:20:39 GMT  
		Size: 152.2 MB (152169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5435e73e2a0cd9b7940e79edf658fb2d75ebffa747232a4fe91a0d125820ab`  
		Last Modified: Mon, 22 Jan 2024 19:51:31 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693c39c2b4ae5ca8cf86a701272004e04d8f68fa55585be237152b2b6b02ef20`  
		Last Modified: Mon, 22 Jan 2024 19:51:46 GMT  
		Size: 368.5 MB (368496491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e5c0b51f3107a46c11c7b6685bc64ccc9e2c350bd74257e316716966c959c155
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556896197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c1d23e0e8fc1d167d73d42f33484d49d4f8304c68612f89efbe6485bc4dde2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:49:06 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:49:53 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:50:02 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:50:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:50:02 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:50:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:50:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:50:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:50:14 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:50:14 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:50:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:50:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393943727a332ace094e701aa8cd3d1e740a2265b6ad85882a2d6284690d4880`  
		Last Modified: Fri, 19 Jan 2024 01:51:13 GMT  
		Size: 150.7 MB (150737265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d832087479e0dd60463c20faa5ab722705448985bac6c6ec1b5b6530a64b8e`  
		Last Modified: Mon, 22 Jan 2024 19:52:20 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf706e61d45631559eb7da7b20786928036d40388cf8f7d05b9e0dd9bcbc74`  
		Last Modified: Mon, 22 Jan 2024 19:52:32 GMT  
		Size: 368.5 MB (368496571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:d32aeff2b18878258eaa305da1588e0476a7f7df392519fc983e6de6608d3f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:20c5ca5b4f1ea1482e59dc06348a558b680fa9e0ec6a1f95c88e3c40bef55732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303997821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2997e2fd0b59f0d3851a3905d3a77b89777a21296f402a9135377f0d2f1515f8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:18:20 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:19:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:48:57 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:57 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:01 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b288f2fdef4d0a03dcb62d1fc0cbc844eb2cd220de6a3a99e9d7a725ad3a839`  
		Last Modified: Fri, 19 Jan 2024 01:20:39 GMT  
		Size: 152.2 MB (152169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe2f4fbd6df0ece7afe995953a09fcb7d2d5fe14950f59c766f71f342010168`  
		Last Modified: Mon, 22 Jan 2024 19:51:04 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646b1996cc82c317f0f36b6908ecc9344390135e70b9826145e65519fd9476ee`  
		Last Modified: Mon, 22 Jan 2024 19:51:09 GMT  
		Size: 112.5 MB (112472544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:da93d1e99342156e148fa8242b294f60931971f5fe8e808d32e0916363c79803
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300872225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e9587083dbb641f1b7d1ee0c350c1723d6cdc37fa25341e62d32e4745f3229`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:49:06 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:49:53 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:49:55 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:59 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:59 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:59 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:59 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:50:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:50:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393943727a332ace094e701aa8cd3d1e740a2265b6ad85882a2d6284690d4880`  
		Last Modified: Fri, 19 Jan 2024 01:51:13 GMT  
		Size: 150.7 MB (150737265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5337c3b8f4ecf77b5ee865e36e6c42c8542a3ec620c6105b9a6cb8a7f6cafb`  
		Last Modified: Mon, 22 Jan 2024 19:51:55 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65848330b066709b421d118f0b5d5a3fe033e281e9a2d5ba86f5f37a886432e7`  
		Last Modified: Mon, 22 Jan 2024 19:51:59 GMT  
		Size: 112.5 MB (112472594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16`

```console
$ docker pull neo4j@sha256:bed18a4185cd5cf48fb5a3d824e0b186d68c03aa6d742e984f7b057df11e7079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16` - linux; amd64

```console
$ docker pull neo4j@sha256:d89db4d15e32dc6f55d55f9d90c2ee953cd0bef20b30338e8679e391fdae056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291711797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2aa72c09cea9e884de8b27becd2181bd6145213112df161870613dfed3f504`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:18 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:47:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:47:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:47:53 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:47:53 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:47:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:47:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:47:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc3dbe4bb8a8cf8e09e918d254f3aed4b07eefac670122b2b59ae28b9b3b8b`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd92a499088faebaebde741ac37801df615c730d808f6f813c2fb58e0d16bcd0`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525a37b23ba6491d60512c25b46d68c4f02853d322f45ef6baf9c0c2b5aeef79`  
		Last Modified: Mon, 22 Jan 2024 19:49:53 GMT  
		Size: 115.4 MB (115406589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:82911582124ea6c08f4ea4e98c4d0b2787aa4bc70d9bba240b3a74e29f4a2dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289128515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de3e315a5b3cc5cfa640775a133b8da83a690d3e2b2a7b9d41ab6838b55a79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:48:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:18 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:18 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:18 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc3bece22f184494fde29a2c4342f688108f00536363d27f7cb4b15a4406b09`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6163ed4009633c27651dab5010b3dc1a3b8ee4613183a1f51d2f9eb426169f67`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473b967008ef8e7c3d8189a7fbb26b472becf20c4ae78169d1d185d1488b8a1c`  
		Last Modified: Mon, 22 Jan 2024 19:50:45 GMT  
		Size: 115.4 MB (115369417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16-bullseye`

```console
$ docker pull neo4j@sha256:bed18a4185cd5cf48fb5a3d824e0b186d68c03aa6d742e984f7b057df11e7079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d89db4d15e32dc6f55d55f9d90c2ee953cd0bef20b30338e8679e391fdae056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291711797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2aa72c09cea9e884de8b27becd2181bd6145213112df161870613dfed3f504`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:18 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:47:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:47:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:47:53 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:47:53 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:47:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:47:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:47:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc3dbe4bb8a8cf8e09e918d254f3aed4b07eefac670122b2b59ae28b9b3b8b`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd92a499088faebaebde741ac37801df615c730d808f6f813c2fb58e0d16bcd0`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525a37b23ba6491d60512c25b46d68c4f02853d322f45ef6baf9c0c2b5aeef79`  
		Last Modified: Mon, 22 Jan 2024 19:49:53 GMT  
		Size: 115.4 MB (115406589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:82911582124ea6c08f4ea4e98c4d0b2787aa4bc70d9bba240b3a74e29f4a2dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289128515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de3e315a5b3cc5cfa640775a133b8da83a690d3e2b2a7b9d41ab6838b55a79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:48:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:18 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:18 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:18 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc3bece22f184494fde29a2c4342f688108f00536363d27f7cb4b15a4406b09`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6163ed4009633c27651dab5010b3dc1a3b8ee4613183a1f51d2f9eb426169f67`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473b967008ef8e7c3d8189a7fbb26b472becf20c4ae78169d1d185d1488b8a1c`  
		Last Modified: Mon, 22 Jan 2024 19:50:45 GMT  
		Size: 115.4 MB (115369417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16-community`

```console
$ docker pull neo4j@sha256:bed18a4185cd5cf48fb5a3d824e0b186d68c03aa6d742e984f7b057df11e7079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16-community` - linux; amd64

```console
$ docker pull neo4j@sha256:d89db4d15e32dc6f55d55f9d90c2ee953cd0bef20b30338e8679e391fdae056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291711797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2aa72c09cea9e884de8b27becd2181bd6145213112df161870613dfed3f504`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:18 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:47:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:47:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:47:53 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:47:53 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:47:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:47:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:47:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc3dbe4bb8a8cf8e09e918d254f3aed4b07eefac670122b2b59ae28b9b3b8b`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd92a499088faebaebde741ac37801df615c730d808f6f813c2fb58e0d16bcd0`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525a37b23ba6491d60512c25b46d68c4f02853d322f45ef6baf9c0c2b5aeef79`  
		Last Modified: Mon, 22 Jan 2024 19:49:53 GMT  
		Size: 115.4 MB (115406589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:82911582124ea6c08f4ea4e98c4d0b2787aa4bc70d9bba240b3a74e29f4a2dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289128515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de3e315a5b3cc5cfa640775a133b8da83a690d3e2b2a7b9d41ab6838b55a79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:48:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:18 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:18 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:18 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc3bece22f184494fde29a2c4342f688108f00536363d27f7cb4b15a4406b09`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6163ed4009633c27651dab5010b3dc1a3b8ee4613183a1f51d2f9eb426169f67`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473b967008ef8e7c3d8189a7fbb26b472becf20c4ae78169d1d185d1488b8a1c`  
		Last Modified: Mon, 22 Jan 2024 19:50:45 GMT  
		Size: 115.4 MB (115369417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16-community-bullseye`

```console
$ docker pull neo4j@sha256:bed18a4185cd5cf48fb5a3d824e0b186d68c03aa6d742e984f7b057df11e7079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d89db4d15e32dc6f55d55f9d90c2ee953cd0bef20b30338e8679e391fdae056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291711797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2aa72c09cea9e884de8b27becd2181bd6145213112df161870613dfed3f504`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:18 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:47:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:47:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:47:53 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:47:53 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:47:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:47:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:47:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc3dbe4bb8a8cf8e09e918d254f3aed4b07eefac670122b2b59ae28b9b3b8b`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd92a499088faebaebde741ac37801df615c730d808f6f813c2fb58e0d16bcd0`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525a37b23ba6491d60512c25b46d68c4f02853d322f45ef6baf9c0c2b5aeef79`  
		Last Modified: Mon, 22 Jan 2024 19:49:53 GMT  
		Size: 115.4 MB (115406589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:82911582124ea6c08f4ea4e98c4d0b2787aa4bc70d9bba240b3a74e29f4a2dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289128515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de3e315a5b3cc5cfa640775a133b8da83a690d3e2b2a7b9d41ab6838b55a79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:48:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:18 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:18 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:18 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc3bece22f184494fde29a2c4342f688108f00536363d27f7cb4b15a4406b09`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6163ed4009633c27651dab5010b3dc1a3b8ee4613183a1f51d2f9eb426169f67`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473b967008ef8e7c3d8189a7fbb26b472becf20c4ae78169d1d185d1488b8a1c`  
		Last Modified: Mon, 22 Jan 2024 19:50:45 GMT  
		Size: 115.4 MB (115369417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16-community-ubi8`

```console
$ docker pull neo4j@sha256:d32aeff2b18878258eaa305da1588e0476a7f7df392519fc983e6de6608d3f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:20c5ca5b4f1ea1482e59dc06348a558b680fa9e0ec6a1f95c88e3c40bef55732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303997821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2997e2fd0b59f0d3851a3905d3a77b89777a21296f402a9135377f0d2f1515f8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:18:20 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:19:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:48:57 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:57 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:01 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b288f2fdef4d0a03dcb62d1fc0cbc844eb2cd220de6a3a99e9d7a725ad3a839`  
		Last Modified: Fri, 19 Jan 2024 01:20:39 GMT  
		Size: 152.2 MB (152169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe2f4fbd6df0ece7afe995953a09fcb7d2d5fe14950f59c766f71f342010168`  
		Last Modified: Mon, 22 Jan 2024 19:51:04 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646b1996cc82c317f0f36b6908ecc9344390135e70b9826145e65519fd9476ee`  
		Last Modified: Mon, 22 Jan 2024 19:51:09 GMT  
		Size: 112.5 MB (112472544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:da93d1e99342156e148fa8242b294f60931971f5fe8e808d32e0916363c79803
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300872225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e9587083dbb641f1b7d1ee0c350c1723d6cdc37fa25341e62d32e4745f3229`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:49:06 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:49:53 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:49:55 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:59 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:59 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:59 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:59 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:50:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:50:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393943727a332ace094e701aa8cd3d1e740a2265b6ad85882a2d6284690d4880`  
		Last Modified: Fri, 19 Jan 2024 01:51:13 GMT  
		Size: 150.7 MB (150737265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5337c3b8f4ecf77b5ee865e36e6c42c8542a3ec620c6105b9a6cb8a7f6cafb`  
		Last Modified: Mon, 22 Jan 2024 19:51:55 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65848330b066709b421d118f0b5d5a3fe033e281e9a2d5ba86f5f37a886432e7`  
		Last Modified: Mon, 22 Jan 2024 19:51:59 GMT  
		Size: 112.5 MB (112472594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16-enterprise`

```console
$ docker pull neo4j@sha256:07e21db007ea859b1a809780e298cc7dc3959e5829ee777ae6b3d3b137ab4b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:77a9374c0ca8e878cd26b5d5273c71132473aae2b61da6ff0a6549be297d51fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547731335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1a5abe453f2856e5f2dbed753ffc1356fe54ba921cf7151ce5675db1819d4b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:59 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:48:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:48:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:48:44 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:48:44 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:48:44 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:48:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:48:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a275040e0f8b7fa8958e5f2a55d70e18d1b371e9e9cacb43422445abe21b7d8`  
		Last Modified: Mon, 22 Jan 2024 19:50:28 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38410ce9acd115784289e56f716e16ed6ed418e7937d50f801a500dd1067750`  
		Last Modified: Mon, 22 Jan 2024 19:50:28 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bb32b856508b5fd4974a48407005fdb63abe39b1fe5780f7e72c0f7c2ac7cb`  
		Last Modified: Mon, 22 Jan 2024 19:50:43 GMT  
		Size: 371.4 MB (371426127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ee47ca1b630d41456ed4c1bde04625f2081a9c6e96b27cf061d7852b54f89c8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545154012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf8efd0b2617e45908a7fa3232fbe178d312e6a936d31f7836f2408e6784724`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:49:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:49:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:51 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:52 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:52 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596c61f2a7289c0db2b2f4798b205db39a8245f0487f5f358cc932bb6bc0f68b`  
		Last Modified: Mon, 22 Jan 2024 19:51:21 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0d4d7aea8cb96020ede5c28edefdef6123ca902a0348c723d68402865e7b1a`  
		Last Modified: Mon, 22 Jan 2024 19:51:21 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cd593bb3eaef178cb7a963b0c70c4d07b79e4247a71460f90a26315b53585c`  
		Last Modified: Mon, 22 Jan 2024 19:51:33 GMT  
		Size: 371.4 MB (371394916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:07e21db007ea859b1a809780e298cc7dc3959e5829ee777ae6b3d3b137ab4b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:77a9374c0ca8e878cd26b5d5273c71132473aae2b61da6ff0a6549be297d51fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547731335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1a5abe453f2856e5f2dbed753ffc1356fe54ba921cf7151ce5675db1819d4b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:59 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:48:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:48:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:48:44 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:48:44 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:48:44 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:48:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:48:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a275040e0f8b7fa8958e5f2a55d70e18d1b371e9e9cacb43422445abe21b7d8`  
		Last Modified: Mon, 22 Jan 2024 19:50:28 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38410ce9acd115784289e56f716e16ed6ed418e7937d50f801a500dd1067750`  
		Last Modified: Mon, 22 Jan 2024 19:50:28 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bb32b856508b5fd4974a48407005fdb63abe39b1fe5780f7e72c0f7c2ac7cb`  
		Last Modified: Mon, 22 Jan 2024 19:50:43 GMT  
		Size: 371.4 MB (371426127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ee47ca1b630d41456ed4c1bde04625f2081a9c6e96b27cf061d7852b54f89c8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545154012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf8efd0b2617e45908a7fa3232fbe178d312e6a936d31f7836f2408e6784724`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:49:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:49:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:51 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:52 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:52 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596c61f2a7289c0db2b2f4798b205db39a8245f0487f5f358cc932bb6bc0f68b`  
		Last Modified: Mon, 22 Jan 2024 19:51:21 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0d4d7aea8cb96020ede5c28edefdef6123ca902a0348c723d68402865e7b1a`  
		Last Modified: Mon, 22 Jan 2024 19:51:21 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cd593bb3eaef178cb7a963b0c70c4d07b79e4247a71460f90a26315b53585c`  
		Last Modified: Mon, 22 Jan 2024 19:51:33 GMT  
		Size: 371.4 MB (371394916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:208c3ed5da6cbf2edbe40b2862b7d29eddbd0302342344972c8a33584dd96dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:59fded3746220789b2fdadd2631843ed20b9bc8484612c828c895de0ead03c05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (560021769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1820a8a7e17954c9b2c658e3895657e19ff1247c60ac734cd89d36afca69c6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:18:20 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:19:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:49:04 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:05 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:16 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:16 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:16 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:16 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b288f2fdef4d0a03dcb62d1fc0cbc844eb2cd220de6a3a99e9d7a725ad3a839`  
		Last Modified: Fri, 19 Jan 2024 01:20:39 GMT  
		Size: 152.2 MB (152169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5435e73e2a0cd9b7940e79edf658fb2d75ebffa747232a4fe91a0d125820ab`  
		Last Modified: Mon, 22 Jan 2024 19:51:31 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693c39c2b4ae5ca8cf86a701272004e04d8f68fa55585be237152b2b6b02ef20`  
		Last Modified: Mon, 22 Jan 2024 19:51:46 GMT  
		Size: 368.5 MB (368496491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e5c0b51f3107a46c11c7b6685bc64ccc9e2c350bd74257e316716966c959c155
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556896197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c1d23e0e8fc1d167d73d42f33484d49d4f8304c68612f89efbe6485bc4dde2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:49:06 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:49:53 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:50:02 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:50:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:50:02 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:50:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:50:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:50:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:50:14 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:50:14 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:50:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:50:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393943727a332ace094e701aa8cd3d1e740a2265b6ad85882a2d6284690d4880`  
		Last Modified: Fri, 19 Jan 2024 01:51:13 GMT  
		Size: 150.7 MB (150737265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d832087479e0dd60463c20faa5ab722705448985bac6c6ec1b5b6530a64b8e`  
		Last Modified: Mon, 22 Jan 2024 19:52:20 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf706e61d45631559eb7da7b20786928036d40388cf8f7d05b9e0dd9bcbc74`  
		Last Modified: Mon, 22 Jan 2024 19:52:32 GMT  
		Size: 368.5 MB (368496571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16-ubi8`

```console
$ docker pull neo4j@sha256:d32aeff2b18878258eaa305da1588e0476a7f7df392519fc983e6de6608d3f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:20c5ca5b4f1ea1482e59dc06348a558b680fa9e0ec6a1f95c88e3c40bef55732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303997821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2997e2fd0b59f0d3851a3905d3a77b89777a21296f402a9135377f0d2f1515f8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:18:20 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:19:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:48:57 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:57 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:01 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b288f2fdef4d0a03dcb62d1fc0cbc844eb2cd220de6a3a99e9d7a725ad3a839`  
		Last Modified: Fri, 19 Jan 2024 01:20:39 GMT  
		Size: 152.2 MB (152169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe2f4fbd6df0ece7afe995953a09fcb7d2d5fe14950f59c766f71f342010168`  
		Last Modified: Mon, 22 Jan 2024 19:51:04 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646b1996cc82c317f0f36b6908ecc9344390135e70b9826145e65519fd9476ee`  
		Last Modified: Mon, 22 Jan 2024 19:51:09 GMT  
		Size: 112.5 MB (112472544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:da93d1e99342156e148fa8242b294f60931971f5fe8e808d32e0916363c79803
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300872225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e9587083dbb641f1b7d1ee0c350c1723d6cdc37fa25341e62d32e4745f3229`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:49:06 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:49:53 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:49:55 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:59 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:59 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:59 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:59 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:50:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:50:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393943727a332ace094e701aa8cd3d1e740a2265b6ad85882a2d6284690d4880`  
		Last Modified: Fri, 19 Jan 2024 01:51:13 GMT  
		Size: 150.7 MB (150737265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5337c3b8f4ecf77b5ee865e36e6c42c8542a3ec620c6105b9a6cb8a7f6cafb`  
		Last Modified: Mon, 22 Jan 2024 19:51:55 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65848330b066709b421d118f0b5d5a3fe033e281e9a2d5ba86f5f37a886432e7`  
		Last Modified: Mon, 22 Jan 2024 19:51:59 GMT  
		Size: 112.5 MB (112472594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16.0`

```console
$ docker pull neo4j@sha256:bed18a4185cd5cf48fb5a3d824e0b186d68c03aa6d742e984f7b057df11e7079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16.0` - linux; amd64

```console
$ docker pull neo4j@sha256:d89db4d15e32dc6f55d55f9d90c2ee953cd0bef20b30338e8679e391fdae056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291711797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2aa72c09cea9e884de8b27becd2181bd6145213112df161870613dfed3f504`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:18 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:47:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:47:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:47:53 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:47:53 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:47:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:47:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:47:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc3dbe4bb8a8cf8e09e918d254f3aed4b07eefac670122b2b59ae28b9b3b8b`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd92a499088faebaebde741ac37801df615c730d808f6f813c2fb58e0d16bcd0`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525a37b23ba6491d60512c25b46d68c4f02853d322f45ef6baf9c0c2b5aeef79`  
		Last Modified: Mon, 22 Jan 2024 19:49:53 GMT  
		Size: 115.4 MB (115406589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:82911582124ea6c08f4ea4e98c4d0b2787aa4bc70d9bba240b3a74e29f4a2dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289128515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de3e315a5b3cc5cfa640775a133b8da83a690d3e2b2a7b9d41ab6838b55a79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:48:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:18 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:18 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:18 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc3bece22f184494fde29a2c4342f688108f00536363d27f7cb4b15a4406b09`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6163ed4009633c27651dab5010b3dc1a3b8ee4613183a1f51d2f9eb426169f67`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473b967008ef8e7c3d8189a7fbb26b472becf20c4ae78169d1d185d1488b8a1c`  
		Last Modified: Mon, 22 Jan 2024 19:50:45 GMT  
		Size: 115.4 MB (115369417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16.0-bullseye`

```console
$ docker pull neo4j@sha256:bed18a4185cd5cf48fb5a3d824e0b186d68c03aa6d742e984f7b057df11e7079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d89db4d15e32dc6f55d55f9d90c2ee953cd0bef20b30338e8679e391fdae056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291711797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2aa72c09cea9e884de8b27becd2181bd6145213112df161870613dfed3f504`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:18 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:47:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:47:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:47:53 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:47:53 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:47:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:47:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:47:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc3dbe4bb8a8cf8e09e918d254f3aed4b07eefac670122b2b59ae28b9b3b8b`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd92a499088faebaebde741ac37801df615c730d808f6f813c2fb58e0d16bcd0`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525a37b23ba6491d60512c25b46d68c4f02853d322f45ef6baf9c0c2b5aeef79`  
		Last Modified: Mon, 22 Jan 2024 19:49:53 GMT  
		Size: 115.4 MB (115406589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:82911582124ea6c08f4ea4e98c4d0b2787aa4bc70d9bba240b3a74e29f4a2dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289128515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de3e315a5b3cc5cfa640775a133b8da83a690d3e2b2a7b9d41ab6838b55a79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:48:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:18 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:18 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:18 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc3bece22f184494fde29a2c4342f688108f00536363d27f7cb4b15a4406b09`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6163ed4009633c27651dab5010b3dc1a3b8ee4613183a1f51d2f9eb426169f67`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473b967008ef8e7c3d8189a7fbb26b472becf20c4ae78169d1d185d1488b8a1c`  
		Last Modified: Mon, 22 Jan 2024 19:50:45 GMT  
		Size: 115.4 MB (115369417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16.0-community`

```console
$ docker pull neo4j@sha256:bed18a4185cd5cf48fb5a3d824e0b186d68c03aa6d742e984f7b057df11e7079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:d89db4d15e32dc6f55d55f9d90c2ee953cd0bef20b30338e8679e391fdae056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291711797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2aa72c09cea9e884de8b27becd2181bd6145213112df161870613dfed3f504`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:18 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:47:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:47:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:47:53 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:47:53 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:47:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:47:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:47:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc3dbe4bb8a8cf8e09e918d254f3aed4b07eefac670122b2b59ae28b9b3b8b`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd92a499088faebaebde741ac37801df615c730d808f6f813c2fb58e0d16bcd0`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525a37b23ba6491d60512c25b46d68c4f02853d322f45ef6baf9c0c2b5aeef79`  
		Last Modified: Mon, 22 Jan 2024 19:49:53 GMT  
		Size: 115.4 MB (115406589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:82911582124ea6c08f4ea4e98c4d0b2787aa4bc70d9bba240b3a74e29f4a2dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289128515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de3e315a5b3cc5cfa640775a133b8da83a690d3e2b2a7b9d41ab6838b55a79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:48:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:18 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:18 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:18 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc3bece22f184494fde29a2c4342f688108f00536363d27f7cb4b15a4406b09`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6163ed4009633c27651dab5010b3dc1a3b8ee4613183a1f51d2f9eb426169f67`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473b967008ef8e7c3d8189a7fbb26b472becf20c4ae78169d1d185d1488b8a1c`  
		Last Modified: Mon, 22 Jan 2024 19:50:45 GMT  
		Size: 115.4 MB (115369417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16.0-community-bullseye`

```console
$ docker pull neo4j@sha256:bed18a4185cd5cf48fb5a3d824e0b186d68c03aa6d742e984f7b057df11e7079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d89db4d15e32dc6f55d55f9d90c2ee953cd0bef20b30338e8679e391fdae056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291711797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2aa72c09cea9e884de8b27becd2181bd6145213112df161870613dfed3f504`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:18 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:47:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:47:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:47:53 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:47:53 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:47:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:47:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:47:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc3dbe4bb8a8cf8e09e918d254f3aed4b07eefac670122b2b59ae28b9b3b8b`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd92a499088faebaebde741ac37801df615c730d808f6f813c2fb58e0d16bcd0`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525a37b23ba6491d60512c25b46d68c4f02853d322f45ef6baf9c0c2b5aeef79`  
		Last Modified: Mon, 22 Jan 2024 19:49:53 GMT  
		Size: 115.4 MB (115406589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:82911582124ea6c08f4ea4e98c4d0b2787aa4bc70d9bba240b3a74e29f4a2dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289128515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de3e315a5b3cc5cfa640775a133b8da83a690d3e2b2a7b9d41ab6838b55a79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:48:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:18 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:18 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:18 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc3bece22f184494fde29a2c4342f688108f00536363d27f7cb4b15a4406b09`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6163ed4009633c27651dab5010b3dc1a3b8ee4613183a1f51d2f9eb426169f67`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473b967008ef8e7c3d8189a7fbb26b472becf20c4ae78169d1d185d1488b8a1c`  
		Last Modified: Mon, 22 Jan 2024 19:50:45 GMT  
		Size: 115.4 MB (115369417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16.0-community-ubi8`

```console
$ docker pull neo4j@sha256:d32aeff2b18878258eaa305da1588e0476a7f7df392519fc983e6de6608d3f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16.0-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:20c5ca5b4f1ea1482e59dc06348a558b680fa9e0ec6a1f95c88e3c40bef55732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303997821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2997e2fd0b59f0d3851a3905d3a77b89777a21296f402a9135377f0d2f1515f8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:18:20 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:19:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:48:57 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:57 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:01 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b288f2fdef4d0a03dcb62d1fc0cbc844eb2cd220de6a3a99e9d7a725ad3a839`  
		Last Modified: Fri, 19 Jan 2024 01:20:39 GMT  
		Size: 152.2 MB (152169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe2f4fbd6df0ece7afe995953a09fcb7d2d5fe14950f59c766f71f342010168`  
		Last Modified: Mon, 22 Jan 2024 19:51:04 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646b1996cc82c317f0f36b6908ecc9344390135e70b9826145e65519fd9476ee`  
		Last Modified: Mon, 22 Jan 2024 19:51:09 GMT  
		Size: 112.5 MB (112472544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16.0-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:da93d1e99342156e148fa8242b294f60931971f5fe8e808d32e0916363c79803
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300872225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e9587083dbb641f1b7d1ee0c350c1723d6cdc37fa25341e62d32e4745f3229`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:49:06 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:49:53 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:49:55 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:59 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:59 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:59 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:59 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:50:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:50:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393943727a332ace094e701aa8cd3d1e740a2265b6ad85882a2d6284690d4880`  
		Last Modified: Fri, 19 Jan 2024 01:51:13 GMT  
		Size: 150.7 MB (150737265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5337c3b8f4ecf77b5ee865e36e6c42c8542a3ec620c6105b9a6cb8a7f6cafb`  
		Last Modified: Mon, 22 Jan 2024 19:51:55 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65848330b066709b421d118f0b5d5a3fe033e281e9a2d5ba86f5f37a886432e7`  
		Last Modified: Mon, 22 Jan 2024 19:51:59 GMT  
		Size: 112.5 MB (112472594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16.0-enterprise`

```console
$ docker pull neo4j@sha256:07e21db007ea859b1a809780e298cc7dc3959e5829ee777ae6b3d3b137ab4b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:77a9374c0ca8e878cd26b5d5273c71132473aae2b61da6ff0a6549be297d51fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547731335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1a5abe453f2856e5f2dbed753ffc1356fe54ba921cf7151ce5675db1819d4b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:59 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:48:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:48:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:48:44 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:48:44 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:48:44 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:48:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:48:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a275040e0f8b7fa8958e5f2a55d70e18d1b371e9e9cacb43422445abe21b7d8`  
		Last Modified: Mon, 22 Jan 2024 19:50:28 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38410ce9acd115784289e56f716e16ed6ed418e7937d50f801a500dd1067750`  
		Last Modified: Mon, 22 Jan 2024 19:50:28 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bb32b856508b5fd4974a48407005fdb63abe39b1fe5780f7e72c0f7c2ac7cb`  
		Last Modified: Mon, 22 Jan 2024 19:50:43 GMT  
		Size: 371.4 MB (371426127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ee47ca1b630d41456ed4c1bde04625f2081a9c6e96b27cf061d7852b54f89c8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545154012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf8efd0b2617e45908a7fa3232fbe178d312e6a936d31f7836f2408e6784724`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:49:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:49:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:51 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:52 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:52 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596c61f2a7289c0db2b2f4798b205db39a8245f0487f5f358cc932bb6bc0f68b`  
		Last Modified: Mon, 22 Jan 2024 19:51:21 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0d4d7aea8cb96020ede5c28edefdef6123ca902a0348c723d68402865e7b1a`  
		Last Modified: Mon, 22 Jan 2024 19:51:21 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cd593bb3eaef178cb7a963b0c70c4d07b79e4247a71460f90a26315b53585c`  
		Last Modified: Mon, 22 Jan 2024 19:51:33 GMT  
		Size: 371.4 MB (371394916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:07e21db007ea859b1a809780e298cc7dc3959e5829ee777ae6b3d3b137ab4b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:77a9374c0ca8e878cd26b5d5273c71132473aae2b61da6ff0a6549be297d51fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547731335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1a5abe453f2856e5f2dbed753ffc1356fe54ba921cf7151ce5675db1819d4b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:59 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:48:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:48:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:48:44 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:48:44 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:48:44 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:48:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:48:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a275040e0f8b7fa8958e5f2a55d70e18d1b371e9e9cacb43422445abe21b7d8`  
		Last Modified: Mon, 22 Jan 2024 19:50:28 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38410ce9acd115784289e56f716e16ed6ed418e7937d50f801a500dd1067750`  
		Last Modified: Mon, 22 Jan 2024 19:50:28 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bb32b856508b5fd4974a48407005fdb63abe39b1fe5780f7e72c0f7c2ac7cb`  
		Last Modified: Mon, 22 Jan 2024 19:50:43 GMT  
		Size: 371.4 MB (371426127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ee47ca1b630d41456ed4c1bde04625f2081a9c6e96b27cf061d7852b54f89c8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545154012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf8efd0b2617e45908a7fa3232fbe178d312e6a936d31f7836f2408e6784724`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:49:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:49:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:51 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:52 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:52 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596c61f2a7289c0db2b2f4798b205db39a8245f0487f5f358cc932bb6bc0f68b`  
		Last Modified: Mon, 22 Jan 2024 19:51:21 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0d4d7aea8cb96020ede5c28edefdef6123ca902a0348c723d68402865e7b1a`  
		Last Modified: Mon, 22 Jan 2024 19:51:21 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cd593bb3eaef178cb7a963b0c70c4d07b79e4247a71460f90a26315b53585c`  
		Last Modified: Mon, 22 Jan 2024 19:51:33 GMT  
		Size: 371.4 MB (371394916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16.0-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:208c3ed5da6cbf2edbe40b2862b7d29eddbd0302342344972c8a33584dd96dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16.0-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:59fded3746220789b2fdadd2631843ed20b9bc8484612c828c895de0ead03c05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (560021769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1820a8a7e17954c9b2c658e3895657e19ff1247c60ac734cd89d36afca69c6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:18:20 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:19:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:49:04 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:05 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:16 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:16 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:16 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:16 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b288f2fdef4d0a03dcb62d1fc0cbc844eb2cd220de6a3a99e9d7a725ad3a839`  
		Last Modified: Fri, 19 Jan 2024 01:20:39 GMT  
		Size: 152.2 MB (152169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5435e73e2a0cd9b7940e79edf658fb2d75ebffa747232a4fe91a0d125820ab`  
		Last Modified: Mon, 22 Jan 2024 19:51:31 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693c39c2b4ae5ca8cf86a701272004e04d8f68fa55585be237152b2b6b02ef20`  
		Last Modified: Mon, 22 Jan 2024 19:51:46 GMT  
		Size: 368.5 MB (368496491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16.0-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e5c0b51f3107a46c11c7b6685bc64ccc9e2c350bd74257e316716966c959c155
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556896197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c1d23e0e8fc1d167d73d42f33484d49d4f8304c68612f89efbe6485bc4dde2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:49:06 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:49:53 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:50:02 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:50:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:50:02 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:50:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:50:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:50:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:50:14 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:50:14 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:50:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:50:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393943727a332ace094e701aa8cd3d1e740a2265b6ad85882a2d6284690d4880`  
		Last Modified: Fri, 19 Jan 2024 01:51:13 GMT  
		Size: 150.7 MB (150737265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d832087479e0dd60463c20faa5ab722705448985bac6c6ec1b5b6530a64b8e`  
		Last Modified: Mon, 22 Jan 2024 19:52:20 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf706e61d45631559eb7da7b20786928036d40388cf8f7d05b9e0dd9bcbc74`  
		Last Modified: Mon, 22 Jan 2024 19:52:32 GMT  
		Size: 368.5 MB (368496571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16.0-ubi8`

```console
$ docker pull neo4j@sha256:d32aeff2b18878258eaa305da1588e0476a7f7df392519fc983e6de6608d3f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16.0-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:20c5ca5b4f1ea1482e59dc06348a558b680fa9e0ec6a1f95c88e3c40bef55732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303997821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2997e2fd0b59f0d3851a3905d3a77b89777a21296f402a9135377f0d2f1515f8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:18:20 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:19:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:48:57 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:57 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:01 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b288f2fdef4d0a03dcb62d1fc0cbc844eb2cd220de6a3a99e9d7a725ad3a839`  
		Last Modified: Fri, 19 Jan 2024 01:20:39 GMT  
		Size: 152.2 MB (152169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe2f4fbd6df0ece7afe995953a09fcb7d2d5fe14950f59c766f71f342010168`  
		Last Modified: Mon, 22 Jan 2024 19:51:04 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646b1996cc82c317f0f36b6908ecc9344390135e70b9826145e65519fd9476ee`  
		Last Modified: Mon, 22 Jan 2024 19:51:09 GMT  
		Size: 112.5 MB (112472544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16.0-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:da93d1e99342156e148fa8242b294f60931971f5fe8e808d32e0916363c79803
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300872225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e9587083dbb641f1b7d1ee0c350c1723d6cdc37fa25341e62d32e4745f3229`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:49:06 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:49:53 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:49:55 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:59 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:59 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:59 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:59 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:50:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:50:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393943727a332ace094e701aa8cd3d1e740a2265b6ad85882a2d6284690d4880`  
		Last Modified: Fri, 19 Jan 2024 01:51:13 GMT  
		Size: 150.7 MB (150737265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5337c3b8f4ecf77b5ee865e36e6c42c8542a3ec620c6105b9a6cb8a7f6cafb`  
		Last Modified: Mon, 22 Jan 2024 19:51:55 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65848330b066709b421d118f0b5d5a3fe033e281e9a2d5ba86f5f37a886432e7`  
		Last Modified: Mon, 22 Jan 2024 19:51:59 GMT  
		Size: 112.5 MB (112472594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:bed18a4185cd5cf48fb5a3d824e0b186d68c03aa6d742e984f7b057df11e7079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d89db4d15e32dc6f55d55f9d90c2ee953cd0bef20b30338e8679e391fdae056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291711797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2aa72c09cea9e884de8b27becd2181bd6145213112df161870613dfed3f504`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:18 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:47:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:47:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:47:53 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:47:53 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:47:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:47:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:47:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc3dbe4bb8a8cf8e09e918d254f3aed4b07eefac670122b2b59ae28b9b3b8b`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd92a499088faebaebde741ac37801df615c730d808f6f813c2fb58e0d16bcd0`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525a37b23ba6491d60512c25b46d68c4f02853d322f45ef6baf9c0c2b5aeef79`  
		Last Modified: Mon, 22 Jan 2024 19:49:53 GMT  
		Size: 115.4 MB (115406589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:82911582124ea6c08f4ea4e98c4d0b2787aa4bc70d9bba240b3a74e29f4a2dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289128515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de3e315a5b3cc5cfa640775a133b8da83a690d3e2b2a7b9d41ab6838b55a79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:48:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:18 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:18 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:18 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc3bece22f184494fde29a2c4342f688108f00536363d27f7cb4b15a4406b09`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6163ed4009633c27651dab5010b3dc1a3b8ee4613183a1f51d2f9eb426169f67`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473b967008ef8e7c3d8189a7fbb26b472becf20c4ae78169d1d185d1488b8a1c`  
		Last Modified: Mon, 22 Jan 2024 19:50:45 GMT  
		Size: 115.4 MB (115369417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:bed18a4185cd5cf48fb5a3d824e0b186d68c03aa6d742e984f7b057df11e7079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:d89db4d15e32dc6f55d55f9d90c2ee953cd0bef20b30338e8679e391fdae056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291711797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2aa72c09cea9e884de8b27becd2181bd6145213112df161870613dfed3f504`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:18 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:47:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:47:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:47:53 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:47:53 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:47:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:47:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:47:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc3dbe4bb8a8cf8e09e918d254f3aed4b07eefac670122b2b59ae28b9b3b8b`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd92a499088faebaebde741ac37801df615c730d808f6f813c2fb58e0d16bcd0`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525a37b23ba6491d60512c25b46d68c4f02853d322f45ef6baf9c0c2b5aeef79`  
		Last Modified: Mon, 22 Jan 2024 19:49:53 GMT  
		Size: 115.4 MB (115406589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:82911582124ea6c08f4ea4e98c4d0b2787aa4bc70d9bba240b3a74e29f4a2dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289128515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de3e315a5b3cc5cfa640775a133b8da83a690d3e2b2a7b9d41ab6838b55a79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:48:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:18 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:18 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:18 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc3bece22f184494fde29a2c4342f688108f00536363d27f7cb4b15a4406b09`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6163ed4009633c27651dab5010b3dc1a3b8ee4613183a1f51d2f9eb426169f67`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473b967008ef8e7c3d8189a7fbb26b472becf20c4ae78169d1d185d1488b8a1c`  
		Last Modified: Mon, 22 Jan 2024 19:50:45 GMT  
		Size: 115.4 MB (115369417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:bed18a4185cd5cf48fb5a3d824e0b186d68c03aa6d742e984f7b057df11e7079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d89db4d15e32dc6f55d55f9d90c2ee953cd0bef20b30338e8679e391fdae056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291711797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2aa72c09cea9e884de8b27becd2181bd6145213112df161870613dfed3f504`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:18 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:47:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:47:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:47:53 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:47:53 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:47:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:47:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:47:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc3dbe4bb8a8cf8e09e918d254f3aed4b07eefac670122b2b59ae28b9b3b8b`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd92a499088faebaebde741ac37801df615c730d808f6f813c2fb58e0d16bcd0`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525a37b23ba6491d60512c25b46d68c4f02853d322f45ef6baf9c0c2b5aeef79`  
		Last Modified: Mon, 22 Jan 2024 19:49:53 GMT  
		Size: 115.4 MB (115406589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:82911582124ea6c08f4ea4e98c4d0b2787aa4bc70d9bba240b3a74e29f4a2dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289128515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de3e315a5b3cc5cfa640775a133b8da83a690d3e2b2a7b9d41ab6838b55a79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:48:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:18 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:18 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:18 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc3bece22f184494fde29a2c4342f688108f00536363d27f7cb4b15a4406b09`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6163ed4009633c27651dab5010b3dc1a3b8ee4613183a1f51d2f9eb426169f67`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473b967008ef8e7c3d8189a7fbb26b472becf20c4ae78169d1d185d1488b8a1c`  
		Last Modified: Mon, 22 Jan 2024 19:50:45 GMT  
		Size: 115.4 MB (115369417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:d32aeff2b18878258eaa305da1588e0476a7f7df392519fc983e6de6608d3f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:20c5ca5b4f1ea1482e59dc06348a558b680fa9e0ec6a1f95c88e3c40bef55732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303997821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2997e2fd0b59f0d3851a3905d3a77b89777a21296f402a9135377f0d2f1515f8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:18:20 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:19:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:48:57 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:57 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:01 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b288f2fdef4d0a03dcb62d1fc0cbc844eb2cd220de6a3a99e9d7a725ad3a839`  
		Last Modified: Fri, 19 Jan 2024 01:20:39 GMT  
		Size: 152.2 MB (152169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe2f4fbd6df0ece7afe995953a09fcb7d2d5fe14950f59c766f71f342010168`  
		Last Modified: Mon, 22 Jan 2024 19:51:04 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646b1996cc82c317f0f36b6908ecc9344390135e70b9826145e65519fd9476ee`  
		Last Modified: Mon, 22 Jan 2024 19:51:09 GMT  
		Size: 112.5 MB (112472544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:da93d1e99342156e148fa8242b294f60931971f5fe8e808d32e0916363c79803
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300872225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e9587083dbb641f1b7d1ee0c350c1723d6cdc37fa25341e62d32e4745f3229`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:49:06 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:49:53 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:49:55 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:59 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:59 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:59 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:59 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:50:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:50:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393943727a332ace094e701aa8cd3d1e740a2265b6ad85882a2d6284690d4880`  
		Last Modified: Fri, 19 Jan 2024 01:51:13 GMT  
		Size: 150.7 MB (150737265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5337c3b8f4ecf77b5ee865e36e6c42c8542a3ec620c6105b9a6cb8a7f6cafb`  
		Last Modified: Mon, 22 Jan 2024 19:51:55 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65848330b066709b421d118f0b5d5a3fe033e281e9a2d5ba86f5f37a886432e7`  
		Last Modified: Mon, 22 Jan 2024 19:51:59 GMT  
		Size: 112.5 MB (112472594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:07e21db007ea859b1a809780e298cc7dc3959e5829ee777ae6b3d3b137ab4b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:77a9374c0ca8e878cd26b5d5273c71132473aae2b61da6ff0a6549be297d51fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547731335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1a5abe453f2856e5f2dbed753ffc1356fe54ba921cf7151ce5675db1819d4b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:59 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:48:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:48:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:48:44 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:48:44 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:48:44 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:48:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:48:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a275040e0f8b7fa8958e5f2a55d70e18d1b371e9e9cacb43422445abe21b7d8`  
		Last Modified: Mon, 22 Jan 2024 19:50:28 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38410ce9acd115784289e56f716e16ed6ed418e7937d50f801a500dd1067750`  
		Last Modified: Mon, 22 Jan 2024 19:50:28 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bb32b856508b5fd4974a48407005fdb63abe39b1fe5780f7e72c0f7c2ac7cb`  
		Last Modified: Mon, 22 Jan 2024 19:50:43 GMT  
		Size: 371.4 MB (371426127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ee47ca1b630d41456ed4c1bde04625f2081a9c6e96b27cf061d7852b54f89c8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545154012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf8efd0b2617e45908a7fa3232fbe178d312e6a936d31f7836f2408e6784724`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:49:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:49:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:51 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:52 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:52 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596c61f2a7289c0db2b2f4798b205db39a8245f0487f5f358cc932bb6bc0f68b`  
		Last Modified: Mon, 22 Jan 2024 19:51:21 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0d4d7aea8cb96020ede5c28edefdef6123ca902a0348c723d68402865e7b1a`  
		Last Modified: Mon, 22 Jan 2024 19:51:21 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cd593bb3eaef178cb7a963b0c70c4d07b79e4247a71460f90a26315b53585c`  
		Last Modified: Mon, 22 Jan 2024 19:51:33 GMT  
		Size: 371.4 MB (371394916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:07e21db007ea859b1a809780e298cc7dc3959e5829ee777ae6b3d3b137ab4b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:77a9374c0ca8e878cd26b5d5273c71132473aae2b61da6ff0a6549be297d51fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547731335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1a5abe453f2856e5f2dbed753ffc1356fe54ba921cf7151ce5675db1819d4b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:59 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:48:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:48:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:48:44 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:48:44 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:48:44 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:48:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:48:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a275040e0f8b7fa8958e5f2a55d70e18d1b371e9e9cacb43422445abe21b7d8`  
		Last Modified: Mon, 22 Jan 2024 19:50:28 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38410ce9acd115784289e56f716e16ed6ed418e7937d50f801a500dd1067750`  
		Last Modified: Mon, 22 Jan 2024 19:50:28 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bb32b856508b5fd4974a48407005fdb63abe39b1fe5780f7e72c0f7c2ac7cb`  
		Last Modified: Mon, 22 Jan 2024 19:50:43 GMT  
		Size: 371.4 MB (371426127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ee47ca1b630d41456ed4c1bde04625f2081a9c6e96b27cf061d7852b54f89c8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545154012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf8efd0b2617e45908a7fa3232fbe178d312e6a936d31f7836f2408e6784724`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:49:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:49:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:51 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:52 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:52 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596c61f2a7289c0db2b2f4798b205db39a8245f0487f5f358cc932bb6bc0f68b`  
		Last Modified: Mon, 22 Jan 2024 19:51:21 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0d4d7aea8cb96020ede5c28edefdef6123ca902a0348c723d68402865e7b1a`  
		Last Modified: Mon, 22 Jan 2024 19:51:21 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cd593bb3eaef178cb7a963b0c70c4d07b79e4247a71460f90a26315b53585c`  
		Last Modified: Mon, 22 Jan 2024 19:51:33 GMT  
		Size: 371.4 MB (371394916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:208c3ed5da6cbf2edbe40b2862b7d29eddbd0302342344972c8a33584dd96dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:59fded3746220789b2fdadd2631843ed20b9bc8484612c828c895de0ead03c05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.0 MB (560021769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1820a8a7e17954c9b2c658e3895657e19ff1247c60ac734cd89d36afca69c6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:18:20 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:19:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:49:04 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:05 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:16 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:16 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:16 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:16 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b288f2fdef4d0a03dcb62d1fc0cbc844eb2cd220de6a3a99e9d7a725ad3a839`  
		Last Modified: Fri, 19 Jan 2024 01:20:39 GMT  
		Size: 152.2 MB (152169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5435e73e2a0cd9b7940e79edf658fb2d75ebffa747232a4fe91a0d125820ab`  
		Last Modified: Mon, 22 Jan 2024 19:51:31 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693c39c2b4ae5ca8cf86a701272004e04d8f68fa55585be237152b2b6b02ef20`  
		Last Modified: Mon, 22 Jan 2024 19:51:46 GMT  
		Size: 368.5 MB (368496491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e5c0b51f3107a46c11c7b6685bc64ccc9e2c350bd74257e316716966c959c155
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.9 MB (556896197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c1d23e0e8fc1d167d73d42f33484d49d4f8304c68612f89efbe6485bc4dde2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:49:06 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:49:53 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:50:02 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:50:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:50:02 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:50:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:50:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:50:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:50:14 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:50:14 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:50:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:50:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393943727a332ace094e701aa8cd3d1e740a2265b6ad85882a2d6284690d4880`  
		Last Modified: Fri, 19 Jan 2024 01:51:13 GMT  
		Size: 150.7 MB (150737265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d832087479e0dd60463c20faa5ab722705448985bac6c6ec1b5b6530a64b8e`  
		Last Modified: Mon, 22 Jan 2024 19:52:20 GMT  
		Size: 9.5 KB (9486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edaf706e61d45631559eb7da7b20786928036d40388cf8f7d05b9e0dd9bcbc74`  
		Last Modified: Mon, 22 Jan 2024 19:52:32 GMT  
		Size: 368.5 MB (368496571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:bed18a4185cd5cf48fb5a3d824e0b186d68c03aa6d742e984f7b057df11e7079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:d89db4d15e32dc6f55d55f9d90c2ee953cd0bef20b30338e8679e391fdae056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291711797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2aa72c09cea9e884de8b27becd2181bd6145213112df161870613dfed3f504`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:50:53 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:47:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:47:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:47:18 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:47:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:47:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:47:53 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:47:53 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:47:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:47:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:47:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46717352c8c1b1a14dae51cf68d48d9972e9ef011a053e3f0a066fc3e03e87e7`  
		Last Modified: Wed, 17 Jan 2024 09:56:58 GMT  
		Size: 144.9 MB (144873898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fc3dbe4bb8a8cf8e09e918d254f3aed4b07eefac670122b2b59ae28b9b3b8b`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd92a499088faebaebde741ac37801df615c730d808f6f813c2fb58e0d16bcd0`  
		Last Modified: Mon, 22 Jan 2024 19:49:47 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525a37b23ba6491d60512c25b46d68c4f02853d322f45ef6baf9c0c2b5aeef79`  
		Last Modified: Mon, 22 Jan 2024 19:49:53 GMT  
		Size: 115.4 MB (115406589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:82911582124ea6c08f4ea4e98c4d0b2787aa4bc70d9bba240b3a74e29f4a2dbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289128515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41de3e315a5b3cc5cfa640775a133b8da83a690d3e2b2a7b9d41ab6838b55a79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:14:48 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Mon, 22 Jan 2024 19:48:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 Jan 2024 19:48:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Mon, 22 Jan 2024 19:49:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:18 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:18 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:18 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4930239c772442472776a3f39445182c29063526754a34d3ff7b45d8a8e38`  
		Last Modified: Wed, 17 Jan 2024 09:17:52 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc3bece22f184494fde29a2c4342f688108f00536363d27f7cb4b15a4406b09`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6163ed4009633c27651dab5010b3dc1a3b8ee4613183a1f51d2f9eb426169f67`  
		Last Modified: Mon, 22 Jan 2024 19:50:40 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473b967008ef8e7c3d8189a7fbb26b472becf20c4ae78169d1d185d1488b8a1c`  
		Last Modified: Mon, 22 Jan 2024 19:50:45 GMT  
		Size: 115.4 MB (115369417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:d32aeff2b18878258eaa305da1588e0476a7f7df392519fc983e6de6608d3f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:20c5ca5b4f1ea1482e59dc06348a558b680fa9e0ec6a1f95c88e3c40bef55732
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (303997821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2997e2fd0b59f0d3851a3905d3a77b89777a21296f402a9135377f0d2f1515f8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:56:15 GMT
ADD file:9418b073acabd63a66eeaa4f888516960d900cb6d4513a829e5f7ecc8abc3c7e in / 
# Tue, 16 Jan 2024 18:57:16 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:57:17 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:57:21 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:57:21 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:57:21 GMT
ENV container oci
# Tue, 16 Jan 2024 18:57:21 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:57:21 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:57:23 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:57:25 GMT
ADD file:9017ab3a596b80515dcdb86e0805a2028a5e0bef9c4b919e241f0c3251f2e54c in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:57:27 GMT
ADD file:1ab2088551a8e8b02a7ffebace3454d68a6706696d4b81e3bc6c8b590d700b85 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:57:27 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:57:30 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:57:34 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:57:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:18:20 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:19:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:48:57 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:48:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:48:57 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:01 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:01 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:49:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:49:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8ff9fa40d38b692a51dbb584c7cbba030ab66f5e54941b744e5580500495139a`  
		Last Modified: Thu, 18 Jan 2024 07:23:53 GMT  
		Size: 39.3 MB (39346564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b288f2fdef4d0a03dcb62d1fc0cbc844eb2cd220de6a3a99e9d7a725ad3a839`  
		Last Modified: Fri, 19 Jan 2024 01:20:39 GMT  
		Size: 152.2 MB (152169226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe2f4fbd6df0ece7afe995953a09fcb7d2d5fe14950f59c766f71f342010168`  
		Last Modified: Mon, 22 Jan 2024 19:51:04 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646b1996cc82c317f0f36b6908ecc9344390135e70b9826145e65519fd9476ee`  
		Last Modified: Mon, 22 Jan 2024 19:51:09 GMT  
		Size: 112.5 MB (112472544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:da93d1e99342156e148fa8242b294f60931971f5fe8e808d32e0916363c79803
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300872225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e9587083dbb641f1b7d1ee0c350c1723d6cdc37fa25341e62d32e4745f3229`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 16 Jan 2024 18:55:55 GMT
ADD file:930a15f0a767b7eb3592de6af04ff19b00fb9c6a458e07ef8fb74d97a7bc4337 in / 
# Tue, 16 Jan 2024 18:55:57 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 16 Jan 2024 18:55:57 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Tue, 16 Jan 2024 18:55:57 GMT
ADD multi:87568757c88b156bce2f2afc6b7ff03019c581565d09b4c07ecf9186c6cb5e9f in /etc/yum.repos.d/ 
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Jan 2024 18:55:57 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 16 Jan 2024 18:55:57 GMT
ENV container oci
# Tue, 16 Jan 2024 18:55:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jan 2024 18:55:57 GMT
CMD ["/bin/bash"]
# Tue, 16 Jan 2024 18:55:58 GMT
RUN rm -rf /var/log/*
# Tue, 16 Jan 2024 18:55:58 GMT
ADD file:ea330585183deec5bb4f4ba26a19491bd2cd7fd9bc089c574fabd9161fcdf997 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1705420507.json 
# Tue, 16 Jan 2024 18:55:59 GMT
ADD file:933beaa935eea03e45e72c9390bc128169863ab081881c35673ec1dbb32c2d3d in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1705420507 
# Tue, 16 Jan 2024 18:55:59 GMT
LABEL "release"="1108.1705420507" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-16T18:44:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1705420507"
# Tue, 16 Jan 2024 18:56:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2675671-1ddde.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Tue, 16 Jan 2024 18:56:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 16 Jan 2024 18:56:03 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 19 Jan 2024 01:49:06 GMT
ENV JAVA_HOME=/usr
# Fri, 19 Jan 2024 01:49:53 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all
# Mon, 22 Jan 2024 19:49:55 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 19:49:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 19:49:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Mon, 22 Jan 2024 19:49:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Mon, 22 Jan 2024 19:49:59 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 19:49:59 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 19:49:59 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 19:49:59 GMT
EXPOSE 7473 7474 7687
# Mon, 22 Jan 2024 19:50:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 19:50:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9f7ce5bd6ef90529eff494df493058700bf255507761bcbd0aee765430df418`  
		Last Modified: Thu, 18 Jan 2024 08:02:46 GMT  
		Size: 37.7 MB (37652875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393943727a332ace094e701aa8cd3d1e740a2265b6ad85882a2d6284690d4880`  
		Last Modified: Fri, 19 Jan 2024 01:51:13 GMT  
		Size: 150.7 MB (150737265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5337c3b8f4ecf77b5ee865e36e6c42c8542a3ec620c6105b9a6cb8a7f6cafb`  
		Last Modified: Mon, 22 Jan 2024 19:51:55 GMT  
		Size: 9.5 KB (9491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65848330b066709b421d118f0b5d5a3fe033e281e9a2d5ba86f5f37a886432e7`  
		Last Modified: Mon, 22 Jan 2024 19:51:59 GMT  
		Size: 112.5 MB (112472594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
