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
$ docker pull neo4j@sha256:d9e2fb1ba398536e50d22ebc3d5d585baa086c1c0cf8e5b96bdc9e11e87e002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:69c579facb7acab1e98f28952b91144c89e469a081804a5dafebd6c3030433b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291850848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f86d3ddb8492bebea9680fc23af24f8b19f284d3105d4e76c27e9c59be160`
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
# Wed, 17 Jan 2024 09:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:50:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:50:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:50:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:51:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:51:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:51:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:51:33 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:51:33 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:51:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:51:34 GMT
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
	-	`sha256:7b6c4391345ca188f7cf7731488c29045956fb2fed39c9bad1ca720ea986e33f`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a561d23014b3b3db598c1a15412f1fd68974973dc70d26256b27b338e3b1eb`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4136c74b119e61bc90f673a2aecd4f79572e9e7b1b884b2f6fcd312951e5a192`  
		Last Modified: Wed, 17 Jan 2024 09:56:52 GMT  
		Size: 115.5 MB (115545645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15c487d57deeca6d60b1a70ccc99af6be93749a2e2f79c695f33185cee331ea4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345d13bbe837f49280d6028dd405409d0fd6f7516921bd4a0b5776cafe49512c`
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
# Wed, 17 Jan 2024 09:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:14:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:19 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:19 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:19 GMT
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
	-	`sha256:6a7923c33d74bf0af2bf76fcb09c466bb2012e428d09122b0a052f1c74923431`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d08996af1ef77445b56cc8efc4b45539461ea8cbf3f0f36714409442922e23c`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab104f0109a7eaf4b6364931310e7dc888aa49d971cfce5829bc407bee1dbe4`  
		Last Modified: Wed, 17 Jan 2024 09:17:48 GMT  
		Size: 115.5 MB (115515838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:d9e2fb1ba398536e50d22ebc3d5d585baa086c1c0cf8e5b96bdc9e11e87e002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:69c579facb7acab1e98f28952b91144c89e469a081804a5dafebd6c3030433b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291850848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f86d3ddb8492bebea9680fc23af24f8b19f284d3105d4e76c27e9c59be160`
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
# Wed, 17 Jan 2024 09:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:50:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:50:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:50:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:51:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:51:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:51:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:51:33 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:51:33 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:51:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:51:34 GMT
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
	-	`sha256:7b6c4391345ca188f7cf7731488c29045956fb2fed39c9bad1ca720ea986e33f`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a561d23014b3b3db598c1a15412f1fd68974973dc70d26256b27b338e3b1eb`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4136c74b119e61bc90f673a2aecd4f79572e9e7b1b884b2f6fcd312951e5a192`  
		Last Modified: Wed, 17 Jan 2024 09:56:52 GMT  
		Size: 115.5 MB (115545645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15c487d57deeca6d60b1a70ccc99af6be93749a2e2f79c695f33185cee331ea4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345d13bbe837f49280d6028dd405409d0fd6f7516921bd4a0b5776cafe49512c`
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
# Wed, 17 Jan 2024 09:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:14:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:19 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:19 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:19 GMT
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
	-	`sha256:6a7923c33d74bf0af2bf76fcb09c466bb2012e428d09122b0a052f1c74923431`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d08996af1ef77445b56cc8efc4b45539461ea8cbf3f0f36714409442922e23c`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab104f0109a7eaf4b6364931310e7dc888aa49d971cfce5829bc407bee1dbe4`  
		Last Modified: Wed, 17 Jan 2024 09:17:48 GMT  
		Size: 115.5 MB (115515838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:d9e2fb1ba398536e50d22ebc3d5d585baa086c1c0cf8e5b96bdc9e11e87e002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:69c579facb7acab1e98f28952b91144c89e469a081804a5dafebd6c3030433b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291850848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f86d3ddb8492bebea9680fc23af24f8b19f284d3105d4e76c27e9c59be160`
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
# Wed, 17 Jan 2024 09:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:50:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:50:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:50:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:51:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:51:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:51:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:51:33 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:51:33 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:51:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:51:34 GMT
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
	-	`sha256:7b6c4391345ca188f7cf7731488c29045956fb2fed39c9bad1ca720ea986e33f`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a561d23014b3b3db598c1a15412f1fd68974973dc70d26256b27b338e3b1eb`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4136c74b119e61bc90f673a2aecd4f79572e9e7b1b884b2f6fcd312951e5a192`  
		Last Modified: Wed, 17 Jan 2024 09:56:52 GMT  
		Size: 115.5 MB (115545645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15c487d57deeca6d60b1a70ccc99af6be93749a2e2f79c695f33185cee331ea4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345d13bbe837f49280d6028dd405409d0fd6f7516921bd4a0b5776cafe49512c`
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
# Wed, 17 Jan 2024 09:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:14:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:19 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:19 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:19 GMT
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
	-	`sha256:6a7923c33d74bf0af2bf76fcb09c466bb2012e428d09122b0a052f1c74923431`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d08996af1ef77445b56cc8efc4b45539461ea8cbf3f0f36714409442922e23c`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab104f0109a7eaf4b6364931310e7dc888aa49d971cfce5829bc407bee1dbe4`  
		Last Modified: Wed, 17 Jan 2024 09:17:48 GMT  
		Size: 115.5 MB (115515838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:d9e2fb1ba398536e50d22ebc3d5d585baa086c1c0cf8e5b96bdc9e11e87e002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:69c579facb7acab1e98f28952b91144c89e469a081804a5dafebd6c3030433b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291850848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f86d3ddb8492bebea9680fc23af24f8b19f284d3105d4e76c27e9c59be160`
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
# Wed, 17 Jan 2024 09:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:50:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:50:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:50:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:51:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:51:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:51:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:51:33 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:51:33 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:51:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:51:34 GMT
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
	-	`sha256:7b6c4391345ca188f7cf7731488c29045956fb2fed39c9bad1ca720ea986e33f`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a561d23014b3b3db598c1a15412f1fd68974973dc70d26256b27b338e3b1eb`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4136c74b119e61bc90f673a2aecd4f79572e9e7b1b884b2f6fcd312951e5a192`  
		Last Modified: Wed, 17 Jan 2024 09:56:52 GMT  
		Size: 115.5 MB (115545645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15c487d57deeca6d60b1a70ccc99af6be93749a2e2f79c695f33185cee331ea4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345d13bbe837f49280d6028dd405409d0fd6f7516921bd4a0b5776cafe49512c`
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
# Wed, 17 Jan 2024 09:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:14:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:19 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:19 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:19 GMT
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
	-	`sha256:6a7923c33d74bf0af2bf76fcb09c466bb2012e428d09122b0a052f1c74923431`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d08996af1ef77445b56cc8efc4b45539461ea8cbf3f0f36714409442922e23c`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab104f0109a7eaf4b6364931310e7dc888aa49d971cfce5829bc407bee1dbe4`  
		Last Modified: Wed, 17 Jan 2024 09:17:48 GMT  
		Size: 115.5 MB (115515838 bytes)  
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
$ docker pull neo4j@sha256:b8491b6dcf998f216079d4793dde4b7d81759d8c05792fa48787c810e9e21e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:19d5368c6892261c0930bd3e4bcdf02d20c740f66180dfa0ba3b06a57c60081f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565743813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2292c2d781a92f7b454ece7dd16d4947204976badbac9268ae389815de0d056e`
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
# Wed, 17 Jan 2024 09:51:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:51:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:51:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:51:40 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:52:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:52:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:52:14 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:52:15 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:52:15 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:52:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:52:15 GMT
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
	-	`sha256:db5087867a53785d0874723109ae2246cbbd41a0ad29bcfa4cf555d3a66d9327`  
		Last Modified: Wed, 17 Jan 2024 09:58:25 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c95943dbdbc1de3ab5f8ca7c5844f9febe8e7a4c0450aecf25a663d42f52bf9`  
		Last Modified: Wed, 17 Jan 2024 09:58:25 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446ee859c935aabd3adca96c4d49a2b55066db82db9b8c75dda8290ba33ee8ab`  
		Last Modified: Wed, 17 Jan 2024 09:58:41 GMT  
		Size: 389.4 MB (389438612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eaa709c65c0b1d607e320f029fa8a6eb75dc96d3d8d4ae5b20dfb8246d94be1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.2 MB (563162457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153e4bb747fbe60ba6ca4aa377e8b0215305bff4f2b5bfc9109fd2be5af89929`
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
# Wed, 17 Jan 2024 09:15:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:15:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:15:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:15:26 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:57 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:57 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:57 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:57 GMT
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
	-	`sha256:5a75043d0700ef59909e051972b2f2c2fe3997628e0158fac651190c7baf4897`  
		Last Modified: Wed, 17 Jan 2024 09:18:25 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0c0443d94331e0dfde24bdafdecd5f2947c3fcef0d125b4978a527dc2ebd3b`  
		Last Modified: Wed, 17 Jan 2024 09:18:25 GMT  
		Size: 9.5 KB (9485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e46b48ba3302bcd3a3e939d655ebba0b4bbbd9fb81d6a75b289a2a292878`  
		Last Modified: Wed, 17 Jan 2024 09:18:38 GMT  
		Size: 389.4 MB (389403362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:b8491b6dcf998f216079d4793dde4b7d81759d8c05792fa48787c810e9e21e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:19d5368c6892261c0930bd3e4bcdf02d20c740f66180dfa0ba3b06a57c60081f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565743813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2292c2d781a92f7b454ece7dd16d4947204976badbac9268ae389815de0d056e`
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
# Wed, 17 Jan 2024 09:51:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:51:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:51:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:51:40 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:52:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:52:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:52:14 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:52:15 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:52:15 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:52:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:52:15 GMT
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
	-	`sha256:db5087867a53785d0874723109ae2246cbbd41a0ad29bcfa4cf555d3a66d9327`  
		Last Modified: Wed, 17 Jan 2024 09:58:25 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c95943dbdbc1de3ab5f8ca7c5844f9febe8e7a4c0450aecf25a663d42f52bf9`  
		Last Modified: Wed, 17 Jan 2024 09:58:25 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446ee859c935aabd3adca96c4d49a2b55066db82db9b8c75dda8290ba33ee8ab`  
		Last Modified: Wed, 17 Jan 2024 09:58:41 GMT  
		Size: 389.4 MB (389438612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eaa709c65c0b1d607e320f029fa8a6eb75dc96d3d8d4ae5b20dfb8246d94be1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.2 MB (563162457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153e4bb747fbe60ba6ca4aa377e8b0215305bff4f2b5bfc9109fd2be5af89929`
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
# Wed, 17 Jan 2024 09:15:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:15:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:15:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:15:26 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:57 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:57 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:57 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:57 GMT
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
	-	`sha256:5a75043d0700ef59909e051972b2f2c2fe3997628e0158fac651190c7baf4897`  
		Last Modified: Wed, 17 Jan 2024 09:18:25 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0c0443d94331e0dfde24bdafdecd5f2947c3fcef0d125b4978a527dc2ebd3b`  
		Last Modified: Wed, 17 Jan 2024 09:18:25 GMT  
		Size: 9.5 KB (9485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e46b48ba3302bcd3a3e939d655ebba0b4bbbd9fb81d6a75b289a2a292878`  
		Last Modified: Wed, 17 Jan 2024 09:18:38 GMT  
		Size: 389.4 MB (389403362 bytes)  
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
$ docker pull neo4j@sha256:d9e2fb1ba398536e50d22ebc3d5d585baa086c1c0cf8e5b96bdc9e11e87e002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15` - linux; amd64

```console
$ docker pull neo4j@sha256:69c579facb7acab1e98f28952b91144c89e469a081804a5dafebd6c3030433b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291850848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f86d3ddb8492bebea9680fc23af24f8b19f284d3105d4e76c27e9c59be160`
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
# Wed, 17 Jan 2024 09:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:50:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:50:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:50:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:51:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:51:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:51:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:51:33 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:51:33 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:51:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:51:34 GMT
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
	-	`sha256:7b6c4391345ca188f7cf7731488c29045956fb2fed39c9bad1ca720ea986e33f`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a561d23014b3b3db598c1a15412f1fd68974973dc70d26256b27b338e3b1eb`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4136c74b119e61bc90f673a2aecd4f79572e9e7b1b884b2f6fcd312951e5a192`  
		Last Modified: Wed, 17 Jan 2024 09:56:52 GMT  
		Size: 115.5 MB (115545645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15c487d57deeca6d60b1a70ccc99af6be93749a2e2f79c695f33185cee331ea4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345d13bbe837f49280d6028dd405409d0fd6f7516921bd4a0b5776cafe49512c`
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
# Wed, 17 Jan 2024 09:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:14:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:19 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:19 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:19 GMT
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
	-	`sha256:6a7923c33d74bf0af2bf76fcb09c466bb2012e428d09122b0a052f1c74923431`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d08996af1ef77445b56cc8efc4b45539461ea8cbf3f0f36714409442922e23c`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab104f0109a7eaf4b6364931310e7dc888aa49d971cfce5829bc407bee1dbe4`  
		Last Modified: Wed, 17 Jan 2024 09:17:48 GMT  
		Size: 115.5 MB (115515838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15-bullseye`

```console
$ docker pull neo4j@sha256:d9e2fb1ba398536e50d22ebc3d5d585baa086c1c0cf8e5b96bdc9e11e87e002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:69c579facb7acab1e98f28952b91144c89e469a081804a5dafebd6c3030433b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291850848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f86d3ddb8492bebea9680fc23af24f8b19f284d3105d4e76c27e9c59be160`
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
# Wed, 17 Jan 2024 09:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:50:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:50:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:50:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:51:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:51:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:51:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:51:33 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:51:33 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:51:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:51:34 GMT
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
	-	`sha256:7b6c4391345ca188f7cf7731488c29045956fb2fed39c9bad1ca720ea986e33f`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a561d23014b3b3db598c1a15412f1fd68974973dc70d26256b27b338e3b1eb`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4136c74b119e61bc90f673a2aecd4f79572e9e7b1b884b2f6fcd312951e5a192`  
		Last Modified: Wed, 17 Jan 2024 09:56:52 GMT  
		Size: 115.5 MB (115545645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15c487d57deeca6d60b1a70ccc99af6be93749a2e2f79c695f33185cee331ea4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345d13bbe837f49280d6028dd405409d0fd6f7516921bd4a0b5776cafe49512c`
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
# Wed, 17 Jan 2024 09:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:14:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:19 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:19 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:19 GMT
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
	-	`sha256:6a7923c33d74bf0af2bf76fcb09c466bb2012e428d09122b0a052f1c74923431`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d08996af1ef77445b56cc8efc4b45539461ea8cbf3f0f36714409442922e23c`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab104f0109a7eaf4b6364931310e7dc888aa49d971cfce5829bc407bee1dbe4`  
		Last Modified: Wed, 17 Jan 2024 09:17:48 GMT  
		Size: 115.5 MB (115515838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15-community`

```console
$ docker pull neo4j@sha256:d9e2fb1ba398536e50d22ebc3d5d585baa086c1c0cf8e5b96bdc9e11e87e002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15-community` - linux; amd64

```console
$ docker pull neo4j@sha256:69c579facb7acab1e98f28952b91144c89e469a081804a5dafebd6c3030433b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291850848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f86d3ddb8492bebea9680fc23af24f8b19f284d3105d4e76c27e9c59be160`
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
# Wed, 17 Jan 2024 09:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:50:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:50:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:50:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:51:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:51:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:51:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:51:33 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:51:33 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:51:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:51:34 GMT
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
	-	`sha256:7b6c4391345ca188f7cf7731488c29045956fb2fed39c9bad1ca720ea986e33f`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a561d23014b3b3db598c1a15412f1fd68974973dc70d26256b27b338e3b1eb`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4136c74b119e61bc90f673a2aecd4f79572e9e7b1b884b2f6fcd312951e5a192`  
		Last Modified: Wed, 17 Jan 2024 09:56:52 GMT  
		Size: 115.5 MB (115545645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15c487d57deeca6d60b1a70ccc99af6be93749a2e2f79c695f33185cee331ea4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345d13bbe837f49280d6028dd405409d0fd6f7516921bd4a0b5776cafe49512c`
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
# Wed, 17 Jan 2024 09:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:14:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:19 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:19 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:19 GMT
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
	-	`sha256:6a7923c33d74bf0af2bf76fcb09c466bb2012e428d09122b0a052f1c74923431`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d08996af1ef77445b56cc8efc4b45539461ea8cbf3f0f36714409442922e23c`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab104f0109a7eaf4b6364931310e7dc888aa49d971cfce5829bc407bee1dbe4`  
		Last Modified: Wed, 17 Jan 2024 09:17:48 GMT  
		Size: 115.5 MB (115515838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15-community-bullseye`

```console
$ docker pull neo4j@sha256:d9e2fb1ba398536e50d22ebc3d5d585baa086c1c0cf8e5b96bdc9e11e87e002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:69c579facb7acab1e98f28952b91144c89e469a081804a5dafebd6c3030433b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291850848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f86d3ddb8492bebea9680fc23af24f8b19f284d3105d4e76c27e9c59be160`
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
# Wed, 17 Jan 2024 09:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:50:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:50:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:50:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:51:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:51:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:51:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:51:33 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:51:33 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:51:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:51:34 GMT
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
	-	`sha256:7b6c4391345ca188f7cf7731488c29045956fb2fed39c9bad1ca720ea986e33f`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a561d23014b3b3db598c1a15412f1fd68974973dc70d26256b27b338e3b1eb`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4136c74b119e61bc90f673a2aecd4f79572e9e7b1b884b2f6fcd312951e5a192`  
		Last Modified: Wed, 17 Jan 2024 09:56:52 GMT  
		Size: 115.5 MB (115545645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15c487d57deeca6d60b1a70ccc99af6be93749a2e2f79c695f33185cee331ea4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345d13bbe837f49280d6028dd405409d0fd6f7516921bd4a0b5776cafe49512c`
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
# Wed, 17 Jan 2024 09:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:14:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:19 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:19 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:19 GMT
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
	-	`sha256:6a7923c33d74bf0af2bf76fcb09c466bb2012e428d09122b0a052f1c74923431`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d08996af1ef77445b56cc8efc4b45539461ea8cbf3f0f36714409442922e23c`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab104f0109a7eaf4b6364931310e7dc888aa49d971cfce5829bc407bee1dbe4`  
		Last Modified: Wed, 17 Jan 2024 09:17:48 GMT  
		Size: 115.5 MB (115515838 bytes)  
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
$ docker pull neo4j@sha256:b8491b6dcf998f216079d4793dde4b7d81759d8c05792fa48787c810e9e21e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:19d5368c6892261c0930bd3e4bcdf02d20c740f66180dfa0ba3b06a57c60081f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565743813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2292c2d781a92f7b454ece7dd16d4947204976badbac9268ae389815de0d056e`
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
# Wed, 17 Jan 2024 09:51:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:51:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:51:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:51:40 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:52:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:52:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:52:14 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:52:15 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:52:15 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:52:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:52:15 GMT
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
	-	`sha256:db5087867a53785d0874723109ae2246cbbd41a0ad29bcfa4cf555d3a66d9327`  
		Last Modified: Wed, 17 Jan 2024 09:58:25 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c95943dbdbc1de3ab5f8ca7c5844f9febe8e7a4c0450aecf25a663d42f52bf9`  
		Last Modified: Wed, 17 Jan 2024 09:58:25 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446ee859c935aabd3adca96c4d49a2b55066db82db9b8c75dda8290ba33ee8ab`  
		Last Modified: Wed, 17 Jan 2024 09:58:41 GMT  
		Size: 389.4 MB (389438612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eaa709c65c0b1d607e320f029fa8a6eb75dc96d3d8d4ae5b20dfb8246d94be1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.2 MB (563162457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153e4bb747fbe60ba6ca4aa377e8b0215305bff4f2b5bfc9109fd2be5af89929`
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
# Wed, 17 Jan 2024 09:15:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:15:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:15:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:15:26 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:57 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:57 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:57 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:57 GMT
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
	-	`sha256:5a75043d0700ef59909e051972b2f2c2fe3997628e0158fac651190c7baf4897`  
		Last Modified: Wed, 17 Jan 2024 09:18:25 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0c0443d94331e0dfde24bdafdecd5f2947c3fcef0d125b4978a527dc2ebd3b`  
		Last Modified: Wed, 17 Jan 2024 09:18:25 GMT  
		Size: 9.5 KB (9485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e46b48ba3302bcd3a3e939d655ebba0b4bbbd9fb81d6a75b289a2a292878`  
		Last Modified: Wed, 17 Jan 2024 09:18:38 GMT  
		Size: 389.4 MB (389403362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:b8491b6dcf998f216079d4793dde4b7d81759d8c05792fa48787c810e9e21e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:19d5368c6892261c0930bd3e4bcdf02d20c740f66180dfa0ba3b06a57c60081f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565743813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2292c2d781a92f7b454ece7dd16d4947204976badbac9268ae389815de0d056e`
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
# Wed, 17 Jan 2024 09:51:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:51:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:51:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:51:40 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:52:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:52:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:52:14 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:52:15 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:52:15 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:52:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:52:15 GMT
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
	-	`sha256:db5087867a53785d0874723109ae2246cbbd41a0ad29bcfa4cf555d3a66d9327`  
		Last Modified: Wed, 17 Jan 2024 09:58:25 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c95943dbdbc1de3ab5f8ca7c5844f9febe8e7a4c0450aecf25a663d42f52bf9`  
		Last Modified: Wed, 17 Jan 2024 09:58:25 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446ee859c935aabd3adca96c4d49a2b55066db82db9b8c75dda8290ba33ee8ab`  
		Last Modified: Wed, 17 Jan 2024 09:58:41 GMT  
		Size: 389.4 MB (389438612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eaa709c65c0b1d607e320f029fa8a6eb75dc96d3d8d4ae5b20dfb8246d94be1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.2 MB (563162457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153e4bb747fbe60ba6ca4aa377e8b0215305bff4f2b5bfc9109fd2be5af89929`
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
# Wed, 17 Jan 2024 09:15:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:15:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:15:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:15:26 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:57 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:57 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:57 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:57 GMT
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
	-	`sha256:5a75043d0700ef59909e051972b2f2c2fe3997628e0158fac651190c7baf4897`  
		Last Modified: Wed, 17 Jan 2024 09:18:25 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0c0443d94331e0dfde24bdafdecd5f2947c3fcef0d125b4978a527dc2ebd3b`  
		Last Modified: Wed, 17 Jan 2024 09:18:25 GMT  
		Size: 9.5 KB (9485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e46b48ba3302bcd3a3e939d655ebba0b4bbbd9fb81d6a75b289a2a292878`  
		Last Modified: Wed, 17 Jan 2024 09:18:38 GMT  
		Size: 389.4 MB (389403362 bytes)  
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
$ docker pull neo4j@sha256:d9e2fb1ba398536e50d22ebc3d5d585baa086c1c0cf8e5b96bdc9e11e87e002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15.0` - linux; amd64

```console
$ docker pull neo4j@sha256:69c579facb7acab1e98f28952b91144c89e469a081804a5dafebd6c3030433b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291850848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f86d3ddb8492bebea9680fc23af24f8b19f284d3105d4e76c27e9c59be160`
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
# Wed, 17 Jan 2024 09:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:50:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:50:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:50:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:51:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:51:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:51:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:51:33 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:51:33 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:51:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:51:34 GMT
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
	-	`sha256:7b6c4391345ca188f7cf7731488c29045956fb2fed39c9bad1ca720ea986e33f`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a561d23014b3b3db598c1a15412f1fd68974973dc70d26256b27b338e3b1eb`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4136c74b119e61bc90f673a2aecd4f79572e9e7b1b884b2f6fcd312951e5a192`  
		Last Modified: Wed, 17 Jan 2024 09:56:52 GMT  
		Size: 115.5 MB (115545645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15c487d57deeca6d60b1a70ccc99af6be93749a2e2f79c695f33185cee331ea4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345d13bbe837f49280d6028dd405409d0fd6f7516921bd4a0b5776cafe49512c`
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
# Wed, 17 Jan 2024 09:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:14:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:19 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:19 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:19 GMT
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
	-	`sha256:6a7923c33d74bf0af2bf76fcb09c466bb2012e428d09122b0a052f1c74923431`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d08996af1ef77445b56cc8efc4b45539461ea8cbf3f0f36714409442922e23c`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab104f0109a7eaf4b6364931310e7dc888aa49d971cfce5829bc407bee1dbe4`  
		Last Modified: Wed, 17 Jan 2024 09:17:48 GMT  
		Size: 115.5 MB (115515838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15.0-bullseye`

```console
$ docker pull neo4j@sha256:d9e2fb1ba398536e50d22ebc3d5d585baa086c1c0cf8e5b96bdc9e11e87e002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:69c579facb7acab1e98f28952b91144c89e469a081804a5dafebd6c3030433b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291850848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f86d3ddb8492bebea9680fc23af24f8b19f284d3105d4e76c27e9c59be160`
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
# Wed, 17 Jan 2024 09:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:50:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:50:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:50:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:51:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:51:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:51:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:51:33 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:51:33 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:51:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:51:34 GMT
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
	-	`sha256:7b6c4391345ca188f7cf7731488c29045956fb2fed39c9bad1ca720ea986e33f`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a561d23014b3b3db598c1a15412f1fd68974973dc70d26256b27b338e3b1eb`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4136c74b119e61bc90f673a2aecd4f79572e9e7b1b884b2f6fcd312951e5a192`  
		Last Modified: Wed, 17 Jan 2024 09:56:52 GMT  
		Size: 115.5 MB (115545645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15c487d57deeca6d60b1a70ccc99af6be93749a2e2f79c695f33185cee331ea4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345d13bbe837f49280d6028dd405409d0fd6f7516921bd4a0b5776cafe49512c`
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
# Wed, 17 Jan 2024 09:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:14:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:19 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:19 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:19 GMT
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
	-	`sha256:6a7923c33d74bf0af2bf76fcb09c466bb2012e428d09122b0a052f1c74923431`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d08996af1ef77445b56cc8efc4b45539461ea8cbf3f0f36714409442922e23c`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab104f0109a7eaf4b6364931310e7dc888aa49d971cfce5829bc407bee1dbe4`  
		Last Modified: Wed, 17 Jan 2024 09:17:48 GMT  
		Size: 115.5 MB (115515838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15.0-community`

```console
$ docker pull neo4j@sha256:d9e2fb1ba398536e50d22ebc3d5d585baa086c1c0cf8e5b96bdc9e11e87e002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:69c579facb7acab1e98f28952b91144c89e469a081804a5dafebd6c3030433b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291850848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f86d3ddb8492bebea9680fc23af24f8b19f284d3105d4e76c27e9c59be160`
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
# Wed, 17 Jan 2024 09:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:50:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:50:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:50:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:51:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:51:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:51:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:51:33 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:51:33 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:51:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:51:34 GMT
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
	-	`sha256:7b6c4391345ca188f7cf7731488c29045956fb2fed39c9bad1ca720ea986e33f`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a561d23014b3b3db598c1a15412f1fd68974973dc70d26256b27b338e3b1eb`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4136c74b119e61bc90f673a2aecd4f79572e9e7b1b884b2f6fcd312951e5a192`  
		Last Modified: Wed, 17 Jan 2024 09:56:52 GMT  
		Size: 115.5 MB (115545645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15c487d57deeca6d60b1a70ccc99af6be93749a2e2f79c695f33185cee331ea4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345d13bbe837f49280d6028dd405409d0fd6f7516921bd4a0b5776cafe49512c`
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
# Wed, 17 Jan 2024 09:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:14:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:19 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:19 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:19 GMT
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
	-	`sha256:6a7923c33d74bf0af2bf76fcb09c466bb2012e428d09122b0a052f1c74923431`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d08996af1ef77445b56cc8efc4b45539461ea8cbf3f0f36714409442922e23c`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab104f0109a7eaf4b6364931310e7dc888aa49d971cfce5829bc407bee1dbe4`  
		Last Modified: Wed, 17 Jan 2024 09:17:48 GMT  
		Size: 115.5 MB (115515838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15.0-community-bullseye`

```console
$ docker pull neo4j@sha256:d9e2fb1ba398536e50d22ebc3d5d585baa086c1c0cf8e5b96bdc9e11e87e002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:69c579facb7acab1e98f28952b91144c89e469a081804a5dafebd6c3030433b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291850848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f86d3ddb8492bebea9680fc23af24f8b19f284d3105d4e76c27e9c59be160`
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
# Wed, 17 Jan 2024 09:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:50:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:50:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:50:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:51:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:51:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:51:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:51:33 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:51:33 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:51:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:51:34 GMT
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
	-	`sha256:7b6c4391345ca188f7cf7731488c29045956fb2fed39c9bad1ca720ea986e33f`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a561d23014b3b3db598c1a15412f1fd68974973dc70d26256b27b338e3b1eb`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4136c74b119e61bc90f673a2aecd4f79572e9e7b1b884b2f6fcd312951e5a192`  
		Last Modified: Wed, 17 Jan 2024 09:56:52 GMT  
		Size: 115.5 MB (115545645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15c487d57deeca6d60b1a70ccc99af6be93749a2e2f79c695f33185cee331ea4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345d13bbe837f49280d6028dd405409d0fd6f7516921bd4a0b5776cafe49512c`
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
# Wed, 17 Jan 2024 09:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:14:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:19 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:19 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:19 GMT
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
	-	`sha256:6a7923c33d74bf0af2bf76fcb09c466bb2012e428d09122b0a052f1c74923431`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d08996af1ef77445b56cc8efc4b45539461ea8cbf3f0f36714409442922e23c`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab104f0109a7eaf4b6364931310e7dc888aa49d971cfce5829bc407bee1dbe4`  
		Last Modified: Wed, 17 Jan 2024 09:17:48 GMT  
		Size: 115.5 MB (115515838 bytes)  
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
$ docker pull neo4j@sha256:b8491b6dcf998f216079d4793dde4b7d81759d8c05792fa48787c810e9e21e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:19d5368c6892261c0930bd3e4bcdf02d20c740f66180dfa0ba3b06a57c60081f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565743813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2292c2d781a92f7b454ece7dd16d4947204976badbac9268ae389815de0d056e`
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
# Wed, 17 Jan 2024 09:51:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:51:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:51:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:51:40 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:52:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:52:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:52:14 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:52:15 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:52:15 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:52:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:52:15 GMT
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
	-	`sha256:db5087867a53785d0874723109ae2246cbbd41a0ad29bcfa4cf555d3a66d9327`  
		Last Modified: Wed, 17 Jan 2024 09:58:25 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c95943dbdbc1de3ab5f8ca7c5844f9febe8e7a4c0450aecf25a663d42f52bf9`  
		Last Modified: Wed, 17 Jan 2024 09:58:25 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446ee859c935aabd3adca96c4d49a2b55066db82db9b8c75dda8290ba33ee8ab`  
		Last Modified: Wed, 17 Jan 2024 09:58:41 GMT  
		Size: 389.4 MB (389438612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eaa709c65c0b1d607e320f029fa8a6eb75dc96d3d8d4ae5b20dfb8246d94be1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.2 MB (563162457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153e4bb747fbe60ba6ca4aa377e8b0215305bff4f2b5bfc9109fd2be5af89929`
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
# Wed, 17 Jan 2024 09:15:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:15:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:15:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:15:26 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:57 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:57 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:57 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:57 GMT
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
	-	`sha256:5a75043d0700ef59909e051972b2f2c2fe3997628e0158fac651190c7baf4897`  
		Last Modified: Wed, 17 Jan 2024 09:18:25 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0c0443d94331e0dfde24bdafdecd5f2947c3fcef0d125b4978a527dc2ebd3b`  
		Last Modified: Wed, 17 Jan 2024 09:18:25 GMT  
		Size: 9.5 KB (9485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e46b48ba3302bcd3a3e939d655ebba0b4bbbd9fb81d6a75b289a2a292878`  
		Last Modified: Wed, 17 Jan 2024 09:18:38 GMT  
		Size: 389.4 MB (389403362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.15.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:b8491b6dcf998f216079d4793dde4b7d81759d8c05792fa48787c810e9e21e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.15.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:19d5368c6892261c0930bd3e4bcdf02d20c740f66180dfa0ba3b06a57c60081f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565743813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2292c2d781a92f7b454ece7dd16d4947204976badbac9268ae389815de0d056e`
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
# Wed, 17 Jan 2024 09:51:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:51:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:51:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:51:40 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:52:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:52:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:52:14 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:52:15 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:52:15 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:52:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:52:15 GMT
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
	-	`sha256:db5087867a53785d0874723109ae2246cbbd41a0ad29bcfa4cf555d3a66d9327`  
		Last Modified: Wed, 17 Jan 2024 09:58:25 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c95943dbdbc1de3ab5f8ca7c5844f9febe8e7a4c0450aecf25a663d42f52bf9`  
		Last Modified: Wed, 17 Jan 2024 09:58:25 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446ee859c935aabd3adca96c4d49a2b55066db82db9b8c75dda8290ba33ee8ab`  
		Last Modified: Wed, 17 Jan 2024 09:58:41 GMT  
		Size: 389.4 MB (389438612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.15.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eaa709c65c0b1d607e320f029fa8a6eb75dc96d3d8d4ae5b20dfb8246d94be1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.2 MB (563162457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153e4bb747fbe60ba6ca4aa377e8b0215305bff4f2b5bfc9109fd2be5af89929`
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
# Wed, 17 Jan 2024 09:15:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:15:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:15:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:15:26 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:57 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:57 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:57 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:57 GMT
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
	-	`sha256:5a75043d0700ef59909e051972b2f2c2fe3997628e0158fac651190c7baf4897`  
		Last Modified: Wed, 17 Jan 2024 09:18:25 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0c0443d94331e0dfde24bdafdecd5f2947c3fcef0d125b4978a527dc2ebd3b`  
		Last Modified: Wed, 17 Jan 2024 09:18:25 GMT  
		Size: 9.5 KB (9485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e46b48ba3302bcd3a3e939d655ebba0b4bbbd9fb81d6a75b289a2a292878`  
		Last Modified: Wed, 17 Jan 2024 09:18:38 GMT  
		Size: 389.4 MB (389403362 bytes)  
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
$ docker pull neo4j@sha256:d9e2fb1ba398536e50d22ebc3d5d585baa086c1c0cf8e5b96bdc9e11e87e002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:69c579facb7acab1e98f28952b91144c89e469a081804a5dafebd6c3030433b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291850848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f86d3ddb8492bebea9680fc23af24f8b19f284d3105d4e76c27e9c59be160`
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
# Wed, 17 Jan 2024 09:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:50:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:50:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:50:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:51:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:51:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:51:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:51:33 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:51:33 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:51:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:51:34 GMT
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
	-	`sha256:7b6c4391345ca188f7cf7731488c29045956fb2fed39c9bad1ca720ea986e33f`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a561d23014b3b3db598c1a15412f1fd68974973dc70d26256b27b338e3b1eb`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4136c74b119e61bc90f673a2aecd4f79572e9e7b1b884b2f6fcd312951e5a192`  
		Last Modified: Wed, 17 Jan 2024 09:56:52 GMT  
		Size: 115.5 MB (115545645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15c487d57deeca6d60b1a70ccc99af6be93749a2e2f79c695f33185cee331ea4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345d13bbe837f49280d6028dd405409d0fd6f7516921bd4a0b5776cafe49512c`
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
# Wed, 17 Jan 2024 09:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:14:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:19 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:19 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:19 GMT
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
	-	`sha256:6a7923c33d74bf0af2bf76fcb09c466bb2012e428d09122b0a052f1c74923431`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d08996af1ef77445b56cc8efc4b45539461ea8cbf3f0f36714409442922e23c`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab104f0109a7eaf4b6364931310e7dc888aa49d971cfce5829bc407bee1dbe4`  
		Last Modified: Wed, 17 Jan 2024 09:17:48 GMT  
		Size: 115.5 MB (115515838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:d9e2fb1ba398536e50d22ebc3d5d585baa086c1c0cf8e5b96bdc9e11e87e002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:69c579facb7acab1e98f28952b91144c89e469a081804a5dafebd6c3030433b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291850848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f86d3ddb8492bebea9680fc23af24f8b19f284d3105d4e76c27e9c59be160`
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
# Wed, 17 Jan 2024 09:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:50:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:50:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:50:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:51:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:51:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:51:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:51:33 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:51:33 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:51:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:51:34 GMT
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
	-	`sha256:7b6c4391345ca188f7cf7731488c29045956fb2fed39c9bad1ca720ea986e33f`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a561d23014b3b3db598c1a15412f1fd68974973dc70d26256b27b338e3b1eb`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4136c74b119e61bc90f673a2aecd4f79572e9e7b1b884b2f6fcd312951e5a192`  
		Last Modified: Wed, 17 Jan 2024 09:56:52 GMT  
		Size: 115.5 MB (115545645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15c487d57deeca6d60b1a70ccc99af6be93749a2e2f79c695f33185cee331ea4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345d13bbe837f49280d6028dd405409d0fd6f7516921bd4a0b5776cafe49512c`
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
# Wed, 17 Jan 2024 09:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:14:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:19 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:19 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:19 GMT
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
	-	`sha256:6a7923c33d74bf0af2bf76fcb09c466bb2012e428d09122b0a052f1c74923431`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d08996af1ef77445b56cc8efc4b45539461ea8cbf3f0f36714409442922e23c`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab104f0109a7eaf4b6364931310e7dc888aa49d971cfce5829bc407bee1dbe4`  
		Last Modified: Wed, 17 Jan 2024 09:17:48 GMT  
		Size: 115.5 MB (115515838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:d9e2fb1ba398536e50d22ebc3d5d585baa086c1c0cf8e5b96bdc9e11e87e002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:69c579facb7acab1e98f28952b91144c89e469a081804a5dafebd6c3030433b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291850848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f86d3ddb8492bebea9680fc23af24f8b19f284d3105d4e76c27e9c59be160`
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
# Wed, 17 Jan 2024 09:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:50:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:50:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:50:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:51:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:51:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:51:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:51:33 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:51:33 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:51:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:51:34 GMT
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
	-	`sha256:7b6c4391345ca188f7cf7731488c29045956fb2fed39c9bad1ca720ea986e33f`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a561d23014b3b3db598c1a15412f1fd68974973dc70d26256b27b338e3b1eb`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4136c74b119e61bc90f673a2aecd4f79572e9e7b1b884b2f6fcd312951e5a192`  
		Last Modified: Wed, 17 Jan 2024 09:56:52 GMT  
		Size: 115.5 MB (115545645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15c487d57deeca6d60b1a70ccc99af6be93749a2e2f79c695f33185cee331ea4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345d13bbe837f49280d6028dd405409d0fd6f7516921bd4a0b5776cafe49512c`
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
# Wed, 17 Jan 2024 09:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:14:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:19 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:19 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:19 GMT
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
	-	`sha256:6a7923c33d74bf0af2bf76fcb09c466bb2012e428d09122b0a052f1c74923431`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d08996af1ef77445b56cc8efc4b45539461ea8cbf3f0f36714409442922e23c`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab104f0109a7eaf4b6364931310e7dc888aa49d971cfce5829bc407bee1dbe4`  
		Last Modified: Wed, 17 Jan 2024 09:17:48 GMT  
		Size: 115.5 MB (115515838 bytes)  
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
$ docker pull neo4j@sha256:b8491b6dcf998f216079d4793dde4b7d81759d8c05792fa48787c810e9e21e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:19d5368c6892261c0930bd3e4bcdf02d20c740f66180dfa0ba3b06a57c60081f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565743813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2292c2d781a92f7b454ece7dd16d4947204976badbac9268ae389815de0d056e`
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
# Wed, 17 Jan 2024 09:51:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:51:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:51:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:51:40 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:52:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:52:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:52:14 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:52:15 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:52:15 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:52:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:52:15 GMT
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
	-	`sha256:db5087867a53785d0874723109ae2246cbbd41a0ad29bcfa4cf555d3a66d9327`  
		Last Modified: Wed, 17 Jan 2024 09:58:25 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c95943dbdbc1de3ab5f8ca7c5844f9febe8e7a4c0450aecf25a663d42f52bf9`  
		Last Modified: Wed, 17 Jan 2024 09:58:25 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446ee859c935aabd3adca96c4d49a2b55066db82db9b8c75dda8290ba33ee8ab`  
		Last Modified: Wed, 17 Jan 2024 09:58:41 GMT  
		Size: 389.4 MB (389438612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eaa709c65c0b1d607e320f029fa8a6eb75dc96d3d8d4ae5b20dfb8246d94be1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.2 MB (563162457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153e4bb747fbe60ba6ca4aa377e8b0215305bff4f2b5bfc9109fd2be5af89929`
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
# Wed, 17 Jan 2024 09:15:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:15:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:15:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:15:26 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:57 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:57 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:57 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:57 GMT
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
	-	`sha256:5a75043d0700ef59909e051972b2f2c2fe3997628e0158fac651190c7baf4897`  
		Last Modified: Wed, 17 Jan 2024 09:18:25 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0c0443d94331e0dfde24bdafdecd5f2947c3fcef0d125b4978a527dc2ebd3b`  
		Last Modified: Wed, 17 Jan 2024 09:18:25 GMT  
		Size: 9.5 KB (9485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e46b48ba3302bcd3a3e939d655ebba0b4bbbd9fb81d6a75b289a2a292878`  
		Last Modified: Wed, 17 Jan 2024 09:18:38 GMT  
		Size: 389.4 MB (389403362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:b8491b6dcf998f216079d4793dde4b7d81759d8c05792fa48787c810e9e21e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:19d5368c6892261c0930bd3e4bcdf02d20c740f66180dfa0ba3b06a57c60081f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565743813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2292c2d781a92f7b454ece7dd16d4947204976badbac9268ae389815de0d056e`
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
# Wed, 17 Jan 2024 09:51:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:51:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:51:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:51:40 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:52:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:52:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:52:14 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:52:15 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:52:15 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:52:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:52:15 GMT
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
	-	`sha256:db5087867a53785d0874723109ae2246cbbd41a0ad29bcfa4cf555d3a66d9327`  
		Last Modified: Wed, 17 Jan 2024 09:58:25 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c95943dbdbc1de3ab5f8ca7c5844f9febe8e7a4c0450aecf25a663d42f52bf9`  
		Last Modified: Wed, 17 Jan 2024 09:58:25 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446ee859c935aabd3adca96c4d49a2b55066db82db9b8c75dda8290ba33ee8ab`  
		Last Modified: Wed, 17 Jan 2024 09:58:41 GMT  
		Size: 389.4 MB (389438612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eaa709c65c0b1d607e320f029fa8a6eb75dc96d3d8d4ae5b20dfb8246d94be1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.2 MB (563162457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153e4bb747fbe60ba6ca4aa377e8b0215305bff4f2b5bfc9109fd2be5af89929`
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
# Wed, 17 Jan 2024 09:15:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7571340603eca6b15923ba213f90d6460e9622657db955488207c0437fb414fb NEO4J_TARBALL=neo4j-enterprise-5.15.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:15:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:15:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:15:26 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:57 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:57 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:57 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:57 GMT
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
	-	`sha256:5a75043d0700ef59909e051972b2f2c2fe3997628e0158fac651190c7baf4897`  
		Last Modified: Wed, 17 Jan 2024 09:18:25 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0c0443d94331e0dfde24bdafdecd5f2947c3fcef0d125b4978a527dc2ebd3b`  
		Last Modified: Wed, 17 Jan 2024 09:18:25 GMT  
		Size: 9.5 KB (9485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700e46b48ba3302bcd3a3e939d655ebba0b4bbbd9fb81d6a75b289a2a292878`  
		Last Modified: Wed, 17 Jan 2024 09:18:38 GMT  
		Size: 389.4 MB (389403362 bytes)  
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
$ docker pull neo4j@sha256:d9e2fb1ba398536e50d22ebc3d5d585baa086c1c0cf8e5b96bdc9e11e87e002a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:69c579facb7acab1e98f28952b91144c89e469a081804a5dafebd6c3030433b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291850848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f86d3ddb8492bebea9680fc23af24f8b19f284d3105d4e76c27e9c59be160`
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
# Wed, 17 Jan 2024 09:50:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:50:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:50:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:50:56 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:51:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:51:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:51:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:51:33 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:51:33 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:51:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:51:34 GMT
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
	-	`sha256:7b6c4391345ca188f7cf7731488c29045956fb2fed39c9bad1ca720ea986e33f`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a561d23014b3b3db598c1a15412f1fd68974973dc70d26256b27b338e3b1eb`  
		Last Modified: Wed, 17 Jan 2024 09:56:46 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4136c74b119e61bc90f673a2aecd4f79572e9e7b1b884b2f6fcd312951e5a192`  
		Last Modified: Wed, 17 Jan 2024 09:56:52 GMT  
		Size: 115.5 MB (115545645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15c487d57deeca6d60b1a70ccc99af6be93749a2e2f79c695f33185cee331ea4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345d13bbe837f49280d6028dd405409d0fd6f7516921bd4a0b5776cafe49512c`
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
# Wed, 17 Jan 2024 09:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Wed, 17 Jan 2024 09:14:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 17 Jan 2024 09:14:52 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Wed, 17 Jan 2024 09:15:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Wed, 17 Jan 2024 09:15:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:15:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 17 Jan 2024 09:15:19 GMT
VOLUME [/data /logs]
# Wed, 17 Jan 2024 09:15:19 GMT
EXPOSE 7473 7474 7687
# Wed, 17 Jan 2024 09:15:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 17 Jan 2024 09:15:19 GMT
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
	-	`sha256:6a7923c33d74bf0af2bf76fcb09c466bb2012e428d09122b0a052f1c74923431`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d08996af1ef77445b56cc8efc4b45539461ea8cbf3f0f36714409442922e23c`  
		Last Modified: Wed, 17 Jan 2024 09:17:43 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab104f0109a7eaf4b6364931310e7dc888aa49d971cfce5829bc407bee1dbe4`  
		Last Modified: Wed, 17 Jan 2024 09:17:48 GMT  
		Size: 115.5 MB (115515838 bytes)  
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
