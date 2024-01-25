<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.30`](#neo4j4430)
-	[`neo4j:4.4.30-community`](#neo4j4430-community)
-	[`neo4j:4.4.30-enterprise`](#neo4j4430-enterprise)
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
$ docker pull neo4j@sha256:aa9ea2c2687dbc9ba13df6251f4455253d7aa0293830c65f78ceae218f616e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:4a7c6de45de1bee5cebf9294fbd3440f389b76073da39bbea735105d96240a78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297285181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf3e3c5cab8cd0d0cb5b2cabdc2529191a28744080e22056c25507671a67cc3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:10:39 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Thu, 25 Jan 2024 19:37:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 19:37:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 19:37:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 19:37:54 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 25 Jan 2024 19:38:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 19:38:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 19:38:28 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 19:38:28 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 19:38:28 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 19:38:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 19:38:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ca7d667a4ecdc7ffeb124470f85841423d14d5340d9a402d347b8dcab005f7`  
		Last Modified: Wed, 24 Jan 2024 22:37:46 GMT  
		Size: 145.3 MB (145270941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7508f2454df4064a4b8d45078d4769d0a038fb5f1b21ef08f16524eac4d21bfb`  
		Last Modified: Thu, 25 Jan 2024 19:39:46 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f825384c1d79c88f2eec033a7d4733050d4dc007d29996b2288269b687cd67c`  
		Last Modified: Thu, 25 Jan 2024 19:39:47 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d881331b6ee36669fa5d1b4d6a8c48ad588364790a416110c01a94fa7bd82a03`  
		Last Modified: Thu, 25 Jan 2024 19:39:52 GMT  
		Size: 120.6 MB (120583011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4e9108f75aca1cf363a7fd6c80598a4e318516ccfc3d30f6a84b58656bef8c22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292631705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7442cd3f557d9f2d0bd2b784711767fb48f3976a8b6382e594239f0decf1658`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:15:46 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Thu, 25 Jan 2024 19:56:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 19:56:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 19:56:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 19:56:09 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 25 Jan 2024 19:56:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 19:56:38 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 19:56:38 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 19:56:38 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 19:56:38 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 19:56:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 19:56:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526ebc7d46b758eaa180a9fe8c8d3e11a382c71f0c0f80f26cbea876285218d4`  
		Last Modified: Wed, 24 Jan 2024 22:37:42 GMT  
		Size: 142.0 MB (142006475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc07b2590aa6403488062b9e83c70c6f6ea9557a7e1d60bcad2eee20248ead27`  
		Last Modified: Thu, 25 Jan 2024 19:57:44 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f933d3e450f29d65be4e8931bed442972e4bd0da212eca00439670c90e24da`  
		Last Modified: Thu, 25 Jan 2024 19:57:44 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5d4bb3513187444d4c506290b144f8ac07d31bff746e8aa3cbe33e01cdb703`  
		Last Modified: Thu, 25 Jan 2024 19:57:48 GMT  
		Size: 120.5 MB (120547914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:aa9ea2c2687dbc9ba13df6251f4455253d7aa0293830c65f78ceae218f616e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:4a7c6de45de1bee5cebf9294fbd3440f389b76073da39bbea735105d96240a78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297285181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf3e3c5cab8cd0d0cb5b2cabdc2529191a28744080e22056c25507671a67cc3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:10:39 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Thu, 25 Jan 2024 19:37:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 19:37:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 19:37:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 19:37:54 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 25 Jan 2024 19:38:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 19:38:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 19:38:28 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 19:38:28 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 19:38:28 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 19:38:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 19:38:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ca7d667a4ecdc7ffeb124470f85841423d14d5340d9a402d347b8dcab005f7`  
		Last Modified: Wed, 24 Jan 2024 22:37:46 GMT  
		Size: 145.3 MB (145270941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7508f2454df4064a4b8d45078d4769d0a038fb5f1b21ef08f16524eac4d21bfb`  
		Last Modified: Thu, 25 Jan 2024 19:39:46 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f825384c1d79c88f2eec033a7d4733050d4dc007d29996b2288269b687cd67c`  
		Last Modified: Thu, 25 Jan 2024 19:39:47 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d881331b6ee36669fa5d1b4d6a8c48ad588364790a416110c01a94fa7bd82a03`  
		Last Modified: Thu, 25 Jan 2024 19:39:52 GMT  
		Size: 120.6 MB (120583011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4e9108f75aca1cf363a7fd6c80598a4e318516ccfc3d30f6a84b58656bef8c22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292631705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7442cd3f557d9f2d0bd2b784711767fb48f3976a8b6382e594239f0decf1658`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:15:46 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Thu, 25 Jan 2024 19:56:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 19:56:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 19:56:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 19:56:09 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 25 Jan 2024 19:56:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 19:56:38 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 19:56:38 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 19:56:38 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 19:56:38 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 19:56:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 19:56:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526ebc7d46b758eaa180a9fe8c8d3e11a382c71f0c0f80f26cbea876285218d4`  
		Last Modified: Wed, 24 Jan 2024 22:37:42 GMT  
		Size: 142.0 MB (142006475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc07b2590aa6403488062b9e83c70c6f6ea9557a7e1d60bcad2eee20248ead27`  
		Last Modified: Thu, 25 Jan 2024 19:57:44 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f933d3e450f29d65be4e8931bed442972e4bd0da212eca00439670c90e24da`  
		Last Modified: Thu, 25 Jan 2024 19:57:44 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5d4bb3513187444d4c506290b144f8ac07d31bff746e8aa3cbe33e01cdb703`  
		Last Modified: Thu, 25 Jan 2024 19:57:48 GMT  
		Size: 120.5 MB (120547914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:c2ed588af7e54c875ff9db2efbc0b18fb9270496ee3914afc7162ac372e9200b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:41226918c1effa4991f37ba2d40d43457e1090e95936d6921759bd4541018a95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.5 MB (402497697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab975444ce8e6d8427b6c3f8a92ac344e29e5778b1595532de6258d6fc8d630`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:10:39 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Thu, 25 Jan 2024 19:38:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9513dddcc0732dc3ad66b7c4c0becde8ce7c6810bf898264f01b2fe634dd4b0e NEO4J_TARBALL=neo4j-enterprise-4.4.30-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 19:38:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 19:38:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 19:38:33 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 25 Jan 2024 19:39:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 19:39:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 19:39:10 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 19:39:11 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 19:39:11 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 19:39:11 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 19:39:11 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ca7d667a4ecdc7ffeb124470f85841423d14d5340d9a402d347b8dcab005f7`  
		Last Modified: Wed, 24 Jan 2024 22:37:46 GMT  
		Size: 145.3 MB (145270941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5a496dd8ee62a75079476bf349b0224d271ad7db5ba5dac5e6b6169ab9db85`  
		Last Modified: Thu, 25 Jan 2024 19:40:06 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41009aeeae1624ec10764fe2a6ecf9a9d0046cfb2ca748ef8079fce0883d436d`  
		Last Modified: Thu, 25 Jan 2024 19:40:06 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f645ee2aab758022d5285574de4f3e9cc9d21562d1d68105997ee1e03fab65f`  
		Last Modified: Thu, 25 Jan 2024 19:40:16 GMT  
		Size: 225.8 MB (225795525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a8429ccff9a19ebf25cfd46ba186232221df2b9773373e5fd822ed6b069a8f3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.8 MB (397842345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee422cec3452143f30fc59d19514c8c332ef35c6aca67644a19d475219d6d18`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:15:46 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Thu, 25 Jan 2024 19:56:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9513dddcc0732dc3ad66b7c4c0becde8ce7c6810bf898264f01b2fe634dd4b0e NEO4J_TARBALL=neo4j-enterprise-4.4.30-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 19:56:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 19:56:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 19:56:42 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 25 Jan 2024 19:57:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 19:57:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 19:57:07 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 19:57:07 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 19:57:08 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 19:57:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 19:57:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526ebc7d46b758eaa180a9fe8c8d3e11a382c71f0c0f80f26cbea876285218d4`  
		Last Modified: Wed, 24 Jan 2024 22:37:42 GMT  
		Size: 142.0 MB (142006475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2d51ec5213c7af3492c983dcc8e275139acf1676803d7ea3934eb589aa2a63`  
		Last Modified: Thu, 25 Jan 2024 19:58:01 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969f1547247bceabf8865156a770192e50aee8fd2b97d159ce069ccce3f9d956`  
		Last Modified: Thu, 25 Jan 2024 19:58:01 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81d8cbd87b1b9243cf2a8fbd8ddcb9b2a2249e8544b71e9a6324a8c2857bf5f`  
		Last Modified: Thu, 25 Jan 2024 19:58:09 GMT  
		Size: 225.8 MB (225758557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.30`

```console
$ docker pull neo4j@sha256:aa9ea2c2687dbc9ba13df6251f4455253d7aa0293830c65f78ceae218f616e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.30` - linux; amd64

```console
$ docker pull neo4j@sha256:4a7c6de45de1bee5cebf9294fbd3440f389b76073da39bbea735105d96240a78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297285181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf3e3c5cab8cd0d0cb5b2cabdc2529191a28744080e22056c25507671a67cc3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:10:39 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Thu, 25 Jan 2024 19:37:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 19:37:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 19:37:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 19:37:54 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 25 Jan 2024 19:38:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 19:38:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 19:38:28 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 19:38:28 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 19:38:28 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 19:38:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 19:38:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ca7d667a4ecdc7ffeb124470f85841423d14d5340d9a402d347b8dcab005f7`  
		Last Modified: Wed, 24 Jan 2024 22:37:46 GMT  
		Size: 145.3 MB (145270941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7508f2454df4064a4b8d45078d4769d0a038fb5f1b21ef08f16524eac4d21bfb`  
		Last Modified: Thu, 25 Jan 2024 19:39:46 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f825384c1d79c88f2eec033a7d4733050d4dc007d29996b2288269b687cd67c`  
		Last Modified: Thu, 25 Jan 2024 19:39:47 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d881331b6ee36669fa5d1b4d6a8c48ad588364790a416110c01a94fa7bd82a03`  
		Last Modified: Thu, 25 Jan 2024 19:39:52 GMT  
		Size: 120.6 MB (120583011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.30` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4e9108f75aca1cf363a7fd6c80598a4e318516ccfc3d30f6a84b58656bef8c22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292631705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7442cd3f557d9f2d0bd2b784711767fb48f3976a8b6382e594239f0decf1658`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:15:46 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Thu, 25 Jan 2024 19:56:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 19:56:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 19:56:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 19:56:09 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 25 Jan 2024 19:56:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 19:56:38 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 19:56:38 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 19:56:38 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 19:56:38 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 19:56:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 19:56:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526ebc7d46b758eaa180a9fe8c8d3e11a382c71f0c0f80f26cbea876285218d4`  
		Last Modified: Wed, 24 Jan 2024 22:37:42 GMT  
		Size: 142.0 MB (142006475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc07b2590aa6403488062b9e83c70c6f6ea9557a7e1d60bcad2eee20248ead27`  
		Last Modified: Thu, 25 Jan 2024 19:57:44 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f933d3e450f29d65be4e8931bed442972e4bd0da212eca00439670c90e24da`  
		Last Modified: Thu, 25 Jan 2024 19:57:44 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5d4bb3513187444d4c506290b144f8ac07d31bff746e8aa3cbe33e01cdb703`  
		Last Modified: Thu, 25 Jan 2024 19:57:48 GMT  
		Size: 120.5 MB (120547914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.30-community`

```console
$ docker pull neo4j@sha256:aa9ea2c2687dbc9ba13df6251f4455253d7aa0293830c65f78ceae218f616e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.30-community` - linux; amd64

```console
$ docker pull neo4j@sha256:4a7c6de45de1bee5cebf9294fbd3440f389b76073da39bbea735105d96240a78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297285181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf3e3c5cab8cd0d0cb5b2cabdc2529191a28744080e22056c25507671a67cc3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:10:39 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Thu, 25 Jan 2024 19:37:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 19:37:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 19:37:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 19:37:54 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 25 Jan 2024 19:38:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 19:38:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 19:38:28 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 19:38:28 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 19:38:28 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 19:38:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 19:38:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ca7d667a4ecdc7ffeb124470f85841423d14d5340d9a402d347b8dcab005f7`  
		Last Modified: Wed, 24 Jan 2024 22:37:46 GMT  
		Size: 145.3 MB (145270941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7508f2454df4064a4b8d45078d4769d0a038fb5f1b21ef08f16524eac4d21bfb`  
		Last Modified: Thu, 25 Jan 2024 19:39:46 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f825384c1d79c88f2eec033a7d4733050d4dc007d29996b2288269b687cd67c`  
		Last Modified: Thu, 25 Jan 2024 19:39:47 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d881331b6ee36669fa5d1b4d6a8c48ad588364790a416110c01a94fa7bd82a03`  
		Last Modified: Thu, 25 Jan 2024 19:39:52 GMT  
		Size: 120.6 MB (120583011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.30-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4e9108f75aca1cf363a7fd6c80598a4e318516ccfc3d30f6a84b58656bef8c22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292631705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7442cd3f557d9f2d0bd2b784711767fb48f3976a8b6382e594239f0decf1658`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:15:46 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Thu, 25 Jan 2024 19:56:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=601e752be679bb057593794ccdeaf496414d859e19bf0f52ce8c259159e77566 NEO4J_TARBALL=neo4j-community-4.4.30-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 19:56:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 19:56:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 19:56:09 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 25 Jan 2024 19:56:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 19:56:38 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 19:56:38 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 19:56:38 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 19:56:38 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 19:56:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 19:56:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526ebc7d46b758eaa180a9fe8c8d3e11a382c71f0c0f80f26cbea876285218d4`  
		Last Modified: Wed, 24 Jan 2024 22:37:42 GMT  
		Size: 142.0 MB (142006475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc07b2590aa6403488062b9e83c70c6f6ea9557a7e1d60bcad2eee20248ead27`  
		Last Modified: Thu, 25 Jan 2024 19:57:44 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f933d3e450f29d65be4e8931bed442972e4bd0da212eca00439670c90e24da`  
		Last Modified: Thu, 25 Jan 2024 19:57:44 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5d4bb3513187444d4c506290b144f8ac07d31bff746e8aa3cbe33e01cdb703`  
		Last Modified: Thu, 25 Jan 2024 19:57:48 GMT  
		Size: 120.5 MB (120547914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.30-enterprise`

```console
$ docker pull neo4j@sha256:c2ed588af7e54c875ff9db2efbc0b18fb9270496ee3914afc7162ac372e9200b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.30-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:41226918c1effa4991f37ba2d40d43457e1090e95936d6921759bd4541018a95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.5 MB (402497697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab975444ce8e6d8427b6c3f8a92ac344e29e5778b1595532de6258d6fc8d630`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:10:39 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Thu, 25 Jan 2024 19:38:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9513dddcc0732dc3ad66b7c4c0becde8ce7c6810bf898264f01b2fe634dd4b0e NEO4J_TARBALL=neo4j-enterprise-4.4.30-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 19:38:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 19:38:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 19:38:33 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 25 Jan 2024 19:39:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 19:39:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 19:39:10 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 19:39:11 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 19:39:11 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 19:39:11 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 19:39:11 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ca7d667a4ecdc7ffeb124470f85841423d14d5340d9a402d347b8dcab005f7`  
		Last Modified: Wed, 24 Jan 2024 22:37:46 GMT  
		Size: 145.3 MB (145270941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5a496dd8ee62a75079476bf349b0224d271ad7db5ba5dac5e6b6169ab9db85`  
		Last Modified: Thu, 25 Jan 2024 19:40:06 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41009aeeae1624ec10764fe2a6ecf9a9d0046cfb2ca748ef8079fce0883d436d`  
		Last Modified: Thu, 25 Jan 2024 19:40:06 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f645ee2aab758022d5285574de4f3e9cc9d21562d1d68105997ee1e03fab65f`  
		Last Modified: Thu, 25 Jan 2024 19:40:16 GMT  
		Size: 225.8 MB (225795525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.30-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a8429ccff9a19ebf25cfd46ba186232221df2b9773373e5fd822ed6b069a8f3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.8 MB (397842345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee422cec3452143f30fc59d19514c8c332ef35c6aca67644a19d475219d6d18`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:15:46 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Thu, 25 Jan 2024 19:56:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9513dddcc0732dc3ad66b7c4c0becde8ce7c6810bf898264f01b2fe634dd4b0e NEO4J_TARBALL=neo4j-enterprise-4.4.30-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 19:56:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
# Thu, 25 Jan 2024 19:56:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 19:56:42 GMT
COPY multi:c12cca2f0caa27234ee009a6f13af4571110b68335ab209e0f1d1267b8204be3 in /startup/ 
# Thu, 25 Jan 2024 19:57:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.30-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 19:57:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 19:57:07 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 19:57:07 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 19:57:08 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 19:57:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 19:57:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526ebc7d46b758eaa180a9fe8c8d3e11a382c71f0c0f80f26cbea876285218d4`  
		Last Modified: Wed, 24 Jan 2024 22:37:42 GMT  
		Size: 142.0 MB (142006475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2d51ec5213c7af3492c983dcc8e275139acf1676803d7ea3934eb589aa2a63`  
		Last Modified: Thu, 25 Jan 2024 19:58:01 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969f1547247bceabf8865156a770192e50aee8fd2b97d159ce069ccce3f9d956`  
		Last Modified: Thu, 25 Jan 2024 19:58:01 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81d8cbd87b1b9243cf2a8fbd8ddcb9b2a2249e8544b71e9a6324a8c2857bf5f`  
		Last Modified: Thu, 25 Jan 2024 19:58:09 GMT  
		Size: 225.8 MB (225758557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:bcd5c1641fb6a373af1b7d5b7202854c301c04f9c9ff83eab237c998f9e99bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:1b4e537b641cacb70112e893e64f91f15df1fbd085dbb9a8b7b5aa21268eb345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb6f43b1fe2495633d36fcd70e1adb50c1f4a21286b966d48c8e575e56b6524`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:57:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:57:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:57:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:57:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:57:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:57:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:57:55 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:57:55 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:57:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:57:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60004b8ae6cd6e559abc76f4bcaf8a36e1bbbd17a6b51e62f483bb0a6e023ca`  
		Last Modified: Thu, 25 Jan 2024 01:00:28 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805cbf4626c9acf5d5dee8fcb193ab7287068f983b7959db1ecd4c1730728cff`  
		Last Modified: Thu, 25 Jan 2024 01:00:27 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa863e248b55c5b258795bf6677bd81fd3cb7c099c9c31c987c1cf3df2b59fb`  
		Last Modified: Thu, 25 Jan 2024 01:00:33 GMT  
		Size: 115.4 MB (115406727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8aecbb6ec30763424361e7e16e6fb10a8e9d34d7822e94383c0f2f8a7e08c1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771783d6469034a6ce0e040415b3c80bdb79954fdc4f4b9ea8371c635cdf4e19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:44:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:44:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:44:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:44:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:19 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:19 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:19 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2ea725d969b623cefe848599deff7717654cc1a341242805cd12b38f71f224`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b40f257a593b129d08f2d884dd256c3247d343203e39947f95d30e565d27582`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9303602f4ec278dc975499c1e851f5cac170cf094a2016ccf1e3e825ca6044`  
		Last Modified: Thu, 25 Jan 2024 01:47:19 GMT  
		Size: 115.4 MB (115369465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:bcd5c1641fb6a373af1b7d5b7202854c301c04f9c9ff83eab237c998f9e99bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1b4e537b641cacb70112e893e64f91f15df1fbd085dbb9a8b7b5aa21268eb345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb6f43b1fe2495633d36fcd70e1adb50c1f4a21286b966d48c8e575e56b6524`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:57:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:57:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:57:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:57:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:57:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:57:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:57:55 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:57:55 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:57:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:57:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60004b8ae6cd6e559abc76f4bcaf8a36e1bbbd17a6b51e62f483bb0a6e023ca`  
		Last Modified: Thu, 25 Jan 2024 01:00:28 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805cbf4626c9acf5d5dee8fcb193ab7287068f983b7959db1ecd4c1730728cff`  
		Last Modified: Thu, 25 Jan 2024 01:00:27 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa863e248b55c5b258795bf6677bd81fd3cb7c099c9c31c987c1cf3df2b59fb`  
		Last Modified: Thu, 25 Jan 2024 01:00:33 GMT  
		Size: 115.4 MB (115406727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8aecbb6ec30763424361e7e16e6fb10a8e9d34d7822e94383c0f2f8a7e08c1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771783d6469034a6ce0e040415b3c80bdb79954fdc4f4b9ea8371c635cdf4e19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:44:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:44:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:44:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:44:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:19 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:19 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:19 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2ea725d969b623cefe848599deff7717654cc1a341242805cd12b38f71f224`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b40f257a593b129d08f2d884dd256c3247d343203e39947f95d30e565d27582`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9303602f4ec278dc975499c1e851f5cac170cf094a2016ccf1e3e825ca6044`  
		Last Modified: Thu, 25 Jan 2024 01:47:19 GMT  
		Size: 115.4 MB (115369465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:bcd5c1641fb6a373af1b7d5b7202854c301c04f9c9ff83eab237c998f9e99bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:1b4e537b641cacb70112e893e64f91f15df1fbd085dbb9a8b7b5aa21268eb345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb6f43b1fe2495633d36fcd70e1adb50c1f4a21286b966d48c8e575e56b6524`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:57:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:57:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:57:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:57:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:57:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:57:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:57:55 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:57:55 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:57:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:57:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60004b8ae6cd6e559abc76f4bcaf8a36e1bbbd17a6b51e62f483bb0a6e023ca`  
		Last Modified: Thu, 25 Jan 2024 01:00:28 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805cbf4626c9acf5d5dee8fcb193ab7287068f983b7959db1ecd4c1730728cff`  
		Last Modified: Thu, 25 Jan 2024 01:00:27 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa863e248b55c5b258795bf6677bd81fd3cb7c099c9c31c987c1cf3df2b59fb`  
		Last Modified: Thu, 25 Jan 2024 01:00:33 GMT  
		Size: 115.4 MB (115406727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8aecbb6ec30763424361e7e16e6fb10a8e9d34d7822e94383c0f2f8a7e08c1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771783d6469034a6ce0e040415b3c80bdb79954fdc4f4b9ea8371c635cdf4e19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:44:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:44:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:44:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:44:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:19 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:19 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:19 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2ea725d969b623cefe848599deff7717654cc1a341242805cd12b38f71f224`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b40f257a593b129d08f2d884dd256c3247d343203e39947f95d30e565d27582`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9303602f4ec278dc975499c1e851f5cac170cf094a2016ccf1e3e825ca6044`  
		Last Modified: Thu, 25 Jan 2024 01:47:19 GMT  
		Size: 115.4 MB (115369465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:bcd5c1641fb6a373af1b7d5b7202854c301c04f9c9ff83eab237c998f9e99bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1b4e537b641cacb70112e893e64f91f15df1fbd085dbb9a8b7b5aa21268eb345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb6f43b1fe2495633d36fcd70e1adb50c1f4a21286b966d48c8e575e56b6524`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:57:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:57:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:57:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:57:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:57:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:57:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:57:55 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:57:55 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:57:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:57:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60004b8ae6cd6e559abc76f4bcaf8a36e1bbbd17a6b51e62f483bb0a6e023ca`  
		Last Modified: Thu, 25 Jan 2024 01:00:28 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805cbf4626c9acf5d5dee8fcb193ab7287068f983b7959db1ecd4c1730728cff`  
		Last Modified: Thu, 25 Jan 2024 01:00:27 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa863e248b55c5b258795bf6677bd81fd3cb7c099c9c31c987c1cf3df2b59fb`  
		Last Modified: Thu, 25 Jan 2024 01:00:33 GMT  
		Size: 115.4 MB (115406727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8aecbb6ec30763424361e7e16e6fb10a8e9d34d7822e94383c0f2f8a7e08c1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771783d6469034a6ce0e040415b3c80bdb79954fdc4f4b9ea8371c635cdf4e19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:44:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:44:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:44:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:44:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:19 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:19 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:19 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2ea725d969b623cefe848599deff7717654cc1a341242805cd12b38f71f224`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b40f257a593b129d08f2d884dd256c3247d343203e39947f95d30e565d27582`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9303602f4ec278dc975499c1e851f5cac170cf094a2016ccf1e3e825ca6044`  
		Last Modified: Thu, 25 Jan 2024 01:47:19 GMT  
		Size: 115.4 MB (115369465 bytes)  
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
$ docker pull neo4j@sha256:f17f0c65c19f787443b51b23c2de7c1ee9f8923b9941f2ebaf71db4f018fe759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:6d89af695f3771e3de8ea57d2f1e5548a9f6b633576b1623c628b4e947fa62f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547749860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cfc9f2671fcd17ceff0f129c4834597648f16db159e6f865f5c7a83074c99c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:58:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:58:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:58:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:58:03 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:58:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:58:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:58:37 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:58:37 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:58:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:58:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8bd383ee7f871467af965fb6ee8e60690e50153eac9e499338de8efa070aa0`  
		Last Modified: Thu, 25 Jan 2024 01:01:07 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76109ffe52fc0e9e6e4f06eb1cfdf97946f3c2579bb50d345821d9c23ee64a46`  
		Last Modified: Thu, 25 Jan 2024 01:01:07 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544922daf3eb961c0d0c352ad0316db1cccb5a80b8b25788b58c794cea97969a`  
		Last Modified: Thu, 25 Jan 2024 01:01:22 GMT  
		Size: 371.4 MB (371426016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bbd8bf364795ae58f106d56bc6a1aa4cecf7bb227588f798a77776cf8b09cef3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545193013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54f0705b46de6448c37b6330194747a36ab7d6e7556ce8945122b150de2701d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:45:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:45:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:45:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:45:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:52 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:52 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6936427b58f4516446f43c682b389cb5eb161e6726f54e09bcca756d10a2d8`  
		Last Modified: Thu, 25 Jan 2024 01:47:51 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3810827657c95d91034f6faa07d5f0ac00b0a3f1345e85aa5fcc4cee246eb77`  
		Last Modified: Thu, 25 Jan 2024 01:47:51 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85034c4bed730f5b7a04fba0f732444b653d49aba938fbd07fb1d0ea339965f5`  
		Last Modified: Thu, 25 Jan 2024 01:48:03 GMT  
		Size: 371.4 MB (371394755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:f17f0c65c19f787443b51b23c2de7c1ee9f8923b9941f2ebaf71db4f018fe759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:6d89af695f3771e3de8ea57d2f1e5548a9f6b633576b1623c628b4e947fa62f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547749860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cfc9f2671fcd17ceff0f129c4834597648f16db159e6f865f5c7a83074c99c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:58:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:58:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:58:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:58:03 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:58:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:58:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:58:37 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:58:37 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:58:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:58:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8bd383ee7f871467af965fb6ee8e60690e50153eac9e499338de8efa070aa0`  
		Last Modified: Thu, 25 Jan 2024 01:01:07 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76109ffe52fc0e9e6e4f06eb1cfdf97946f3c2579bb50d345821d9c23ee64a46`  
		Last Modified: Thu, 25 Jan 2024 01:01:07 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544922daf3eb961c0d0c352ad0316db1cccb5a80b8b25788b58c794cea97969a`  
		Last Modified: Thu, 25 Jan 2024 01:01:22 GMT  
		Size: 371.4 MB (371426016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bbd8bf364795ae58f106d56bc6a1aa4cecf7bb227588f798a77776cf8b09cef3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545193013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54f0705b46de6448c37b6330194747a36ab7d6e7556ce8945122b150de2701d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:45:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:45:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:45:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:45:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:52 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:52 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6936427b58f4516446f43c682b389cb5eb161e6726f54e09bcca756d10a2d8`  
		Last Modified: Thu, 25 Jan 2024 01:47:51 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3810827657c95d91034f6faa07d5f0ac00b0a3f1345e85aa5fcc4cee246eb77`  
		Last Modified: Thu, 25 Jan 2024 01:47:51 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85034c4bed730f5b7a04fba0f732444b653d49aba938fbd07fb1d0ea339965f5`  
		Last Modified: Thu, 25 Jan 2024 01:48:03 GMT  
		Size: 371.4 MB (371394755 bytes)  
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
$ docker pull neo4j@sha256:bcd5c1641fb6a373af1b7d5b7202854c301c04f9c9ff83eab237c998f9e99bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16` - linux; amd64

```console
$ docker pull neo4j@sha256:1b4e537b641cacb70112e893e64f91f15df1fbd085dbb9a8b7b5aa21268eb345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb6f43b1fe2495633d36fcd70e1adb50c1f4a21286b966d48c8e575e56b6524`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:57:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:57:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:57:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:57:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:57:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:57:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:57:55 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:57:55 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:57:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:57:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60004b8ae6cd6e559abc76f4bcaf8a36e1bbbd17a6b51e62f483bb0a6e023ca`  
		Last Modified: Thu, 25 Jan 2024 01:00:28 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805cbf4626c9acf5d5dee8fcb193ab7287068f983b7959db1ecd4c1730728cff`  
		Last Modified: Thu, 25 Jan 2024 01:00:27 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa863e248b55c5b258795bf6677bd81fd3cb7c099c9c31c987c1cf3df2b59fb`  
		Last Modified: Thu, 25 Jan 2024 01:00:33 GMT  
		Size: 115.4 MB (115406727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8aecbb6ec30763424361e7e16e6fb10a8e9d34d7822e94383c0f2f8a7e08c1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771783d6469034a6ce0e040415b3c80bdb79954fdc4f4b9ea8371c635cdf4e19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:44:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:44:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:44:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:44:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:19 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:19 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:19 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2ea725d969b623cefe848599deff7717654cc1a341242805cd12b38f71f224`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b40f257a593b129d08f2d884dd256c3247d343203e39947f95d30e565d27582`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9303602f4ec278dc975499c1e851f5cac170cf094a2016ccf1e3e825ca6044`  
		Last Modified: Thu, 25 Jan 2024 01:47:19 GMT  
		Size: 115.4 MB (115369465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16-bullseye`

```console
$ docker pull neo4j@sha256:bcd5c1641fb6a373af1b7d5b7202854c301c04f9c9ff83eab237c998f9e99bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1b4e537b641cacb70112e893e64f91f15df1fbd085dbb9a8b7b5aa21268eb345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb6f43b1fe2495633d36fcd70e1adb50c1f4a21286b966d48c8e575e56b6524`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:57:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:57:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:57:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:57:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:57:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:57:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:57:55 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:57:55 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:57:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:57:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60004b8ae6cd6e559abc76f4bcaf8a36e1bbbd17a6b51e62f483bb0a6e023ca`  
		Last Modified: Thu, 25 Jan 2024 01:00:28 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805cbf4626c9acf5d5dee8fcb193ab7287068f983b7959db1ecd4c1730728cff`  
		Last Modified: Thu, 25 Jan 2024 01:00:27 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa863e248b55c5b258795bf6677bd81fd3cb7c099c9c31c987c1cf3df2b59fb`  
		Last Modified: Thu, 25 Jan 2024 01:00:33 GMT  
		Size: 115.4 MB (115406727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8aecbb6ec30763424361e7e16e6fb10a8e9d34d7822e94383c0f2f8a7e08c1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771783d6469034a6ce0e040415b3c80bdb79954fdc4f4b9ea8371c635cdf4e19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:44:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:44:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:44:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:44:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:19 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:19 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:19 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2ea725d969b623cefe848599deff7717654cc1a341242805cd12b38f71f224`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b40f257a593b129d08f2d884dd256c3247d343203e39947f95d30e565d27582`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9303602f4ec278dc975499c1e851f5cac170cf094a2016ccf1e3e825ca6044`  
		Last Modified: Thu, 25 Jan 2024 01:47:19 GMT  
		Size: 115.4 MB (115369465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16-community`

```console
$ docker pull neo4j@sha256:bcd5c1641fb6a373af1b7d5b7202854c301c04f9c9ff83eab237c998f9e99bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16-community` - linux; amd64

```console
$ docker pull neo4j@sha256:1b4e537b641cacb70112e893e64f91f15df1fbd085dbb9a8b7b5aa21268eb345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb6f43b1fe2495633d36fcd70e1adb50c1f4a21286b966d48c8e575e56b6524`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:57:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:57:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:57:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:57:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:57:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:57:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:57:55 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:57:55 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:57:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:57:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60004b8ae6cd6e559abc76f4bcaf8a36e1bbbd17a6b51e62f483bb0a6e023ca`  
		Last Modified: Thu, 25 Jan 2024 01:00:28 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805cbf4626c9acf5d5dee8fcb193ab7287068f983b7959db1ecd4c1730728cff`  
		Last Modified: Thu, 25 Jan 2024 01:00:27 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa863e248b55c5b258795bf6677bd81fd3cb7c099c9c31c987c1cf3df2b59fb`  
		Last Modified: Thu, 25 Jan 2024 01:00:33 GMT  
		Size: 115.4 MB (115406727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8aecbb6ec30763424361e7e16e6fb10a8e9d34d7822e94383c0f2f8a7e08c1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771783d6469034a6ce0e040415b3c80bdb79954fdc4f4b9ea8371c635cdf4e19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:44:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:44:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:44:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:44:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:19 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:19 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:19 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2ea725d969b623cefe848599deff7717654cc1a341242805cd12b38f71f224`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b40f257a593b129d08f2d884dd256c3247d343203e39947f95d30e565d27582`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9303602f4ec278dc975499c1e851f5cac170cf094a2016ccf1e3e825ca6044`  
		Last Modified: Thu, 25 Jan 2024 01:47:19 GMT  
		Size: 115.4 MB (115369465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16-community-bullseye`

```console
$ docker pull neo4j@sha256:bcd5c1641fb6a373af1b7d5b7202854c301c04f9c9ff83eab237c998f9e99bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1b4e537b641cacb70112e893e64f91f15df1fbd085dbb9a8b7b5aa21268eb345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb6f43b1fe2495633d36fcd70e1adb50c1f4a21286b966d48c8e575e56b6524`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:57:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:57:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:57:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:57:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:57:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:57:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:57:55 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:57:55 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:57:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:57:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60004b8ae6cd6e559abc76f4bcaf8a36e1bbbd17a6b51e62f483bb0a6e023ca`  
		Last Modified: Thu, 25 Jan 2024 01:00:28 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805cbf4626c9acf5d5dee8fcb193ab7287068f983b7959db1ecd4c1730728cff`  
		Last Modified: Thu, 25 Jan 2024 01:00:27 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa863e248b55c5b258795bf6677bd81fd3cb7c099c9c31c987c1cf3df2b59fb`  
		Last Modified: Thu, 25 Jan 2024 01:00:33 GMT  
		Size: 115.4 MB (115406727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8aecbb6ec30763424361e7e16e6fb10a8e9d34d7822e94383c0f2f8a7e08c1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771783d6469034a6ce0e040415b3c80bdb79954fdc4f4b9ea8371c635cdf4e19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:44:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:44:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:44:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:44:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:19 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:19 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:19 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2ea725d969b623cefe848599deff7717654cc1a341242805cd12b38f71f224`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b40f257a593b129d08f2d884dd256c3247d343203e39947f95d30e565d27582`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9303602f4ec278dc975499c1e851f5cac170cf094a2016ccf1e3e825ca6044`  
		Last Modified: Thu, 25 Jan 2024 01:47:19 GMT  
		Size: 115.4 MB (115369465 bytes)  
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
$ docker pull neo4j@sha256:f17f0c65c19f787443b51b23c2de7c1ee9f8923b9941f2ebaf71db4f018fe759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:6d89af695f3771e3de8ea57d2f1e5548a9f6b633576b1623c628b4e947fa62f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547749860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cfc9f2671fcd17ceff0f129c4834597648f16db159e6f865f5c7a83074c99c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:58:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:58:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:58:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:58:03 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:58:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:58:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:58:37 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:58:37 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:58:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:58:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8bd383ee7f871467af965fb6ee8e60690e50153eac9e499338de8efa070aa0`  
		Last Modified: Thu, 25 Jan 2024 01:01:07 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76109ffe52fc0e9e6e4f06eb1cfdf97946f3c2579bb50d345821d9c23ee64a46`  
		Last Modified: Thu, 25 Jan 2024 01:01:07 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544922daf3eb961c0d0c352ad0316db1cccb5a80b8b25788b58c794cea97969a`  
		Last Modified: Thu, 25 Jan 2024 01:01:22 GMT  
		Size: 371.4 MB (371426016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bbd8bf364795ae58f106d56bc6a1aa4cecf7bb227588f798a77776cf8b09cef3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545193013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54f0705b46de6448c37b6330194747a36ab7d6e7556ce8945122b150de2701d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:45:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:45:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:45:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:45:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:52 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:52 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6936427b58f4516446f43c682b389cb5eb161e6726f54e09bcca756d10a2d8`  
		Last Modified: Thu, 25 Jan 2024 01:47:51 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3810827657c95d91034f6faa07d5f0ac00b0a3f1345e85aa5fcc4cee246eb77`  
		Last Modified: Thu, 25 Jan 2024 01:47:51 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85034c4bed730f5b7a04fba0f732444b653d49aba938fbd07fb1d0ea339965f5`  
		Last Modified: Thu, 25 Jan 2024 01:48:03 GMT  
		Size: 371.4 MB (371394755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:f17f0c65c19f787443b51b23c2de7c1ee9f8923b9941f2ebaf71db4f018fe759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:6d89af695f3771e3de8ea57d2f1e5548a9f6b633576b1623c628b4e947fa62f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547749860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cfc9f2671fcd17ceff0f129c4834597648f16db159e6f865f5c7a83074c99c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:58:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:58:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:58:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:58:03 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:58:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:58:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:58:37 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:58:37 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:58:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:58:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8bd383ee7f871467af965fb6ee8e60690e50153eac9e499338de8efa070aa0`  
		Last Modified: Thu, 25 Jan 2024 01:01:07 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76109ffe52fc0e9e6e4f06eb1cfdf97946f3c2579bb50d345821d9c23ee64a46`  
		Last Modified: Thu, 25 Jan 2024 01:01:07 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544922daf3eb961c0d0c352ad0316db1cccb5a80b8b25788b58c794cea97969a`  
		Last Modified: Thu, 25 Jan 2024 01:01:22 GMT  
		Size: 371.4 MB (371426016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bbd8bf364795ae58f106d56bc6a1aa4cecf7bb227588f798a77776cf8b09cef3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545193013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54f0705b46de6448c37b6330194747a36ab7d6e7556ce8945122b150de2701d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:45:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:45:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:45:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:45:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:52 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:52 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6936427b58f4516446f43c682b389cb5eb161e6726f54e09bcca756d10a2d8`  
		Last Modified: Thu, 25 Jan 2024 01:47:51 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3810827657c95d91034f6faa07d5f0ac00b0a3f1345e85aa5fcc4cee246eb77`  
		Last Modified: Thu, 25 Jan 2024 01:47:51 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85034c4bed730f5b7a04fba0f732444b653d49aba938fbd07fb1d0ea339965f5`  
		Last Modified: Thu, 25 Jan 2024 01:48:03 GMT  
		Size: 371.4 MB (371394755 bytes)  
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
$ docker pull neo4j@sha256:bcd5c1641fb6a373af1b7d5b7202854c301c04f9c9ff83eab237c998f9e99bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16.0` - linux; amd64

```console
$ docker pull neo4j@sha256:1b4e537b641cacb70112e893e64f91f15df1fbd085dbb9a8b7b5aa21268eb345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb6f43b1fe2495633d36fcd70e1adb50c1f4a21286b966d48c8e575e56b6524`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:57:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:57:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:57:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:57:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:57:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:57:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:57:55 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:57:55 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:57:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:57:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60004b8ae6cd6e559abc76f4bcaf8a36e1bbbd17a6b51e62f483bb0a6e023ca`  
		Last Modified: Thu, 25 Jan 2024 01:00:28 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805cbf4626c9acf5d5dee8fcb193ab7287068f983b7959db1ecd4c1730728cff`  
		Last Modified: Thu, 25 Jan 2024 01:00:27 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa863e248b55c5b258795bf6677bd81fd3cb7c099c9c31c987c1cf3df2b59fb`  
		Last Modified: Thu, 25 Jan 2024 01:00:33 GMT  
		Size: 115.4 MB (115406727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8aecbb6ec30763424361e7e16e6fb10a8e9d34d7822e94383c0f2f8a7e08c1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771783d6469034a6ce0e040415b3c80bdb79954fdc4f4b9ea8371c635cdf4e19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:44:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:44:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:44:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:44:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:19 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:19 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:19 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2ea725d969b623cefe848599deff7717654cc1a341242805cd12b38f71f224`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b40f257a593b129d08f2d884dd256c3247d343203e39947f95d30e565d27582`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9303602f4ec278dc975499c1e851f5cac170cf094a2016ccf1e3e825ca6044`  
		Last Modified: Thu, 25 Jan 2024 01:47:19 GMT  
		Size: 115.4 MB (115369465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16.0-bullseye`

```console
$ docker pull neo4j@sha256:bcd5c1641fb6a373af1b7d5b7202854c301c04f9c9ff83eab237c998f9e99bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1b4e537b641cacb70112e893e64f91f15df1fbd085dbb9a8b7b5aa21268eb345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb6f43b1fe2495633d36fcd70e1adb50c1f4a21286b966d48c8e575e56b6524`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:57:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:57:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:57:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:57:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:57:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:57:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:57:55 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:57:55 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:57:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:57:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60004b8ae6cd6e559abc76f4bcaf8a36e1bbbd17a6b51e62f483bb0a6e023ca`  
		Last Modified: Thu, 25 Jan 2024 01:00:28 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805cbf4626c9acf5d5dee8fcb193ab7287068f983b7959db1ecd4c1730728cff`  
		Last Modified: Thu, 25 Jan 2024 01:00:27 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa863e248b55c5b258795bf6677bd81fd3cb7c099c9c31c987c1cf3df2b59fb`  
		Last Modified: Thu, 25 Jan 2024 01:00:33 GMT  
		Size: 115.4 MB (115406727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8aecbb6ec30763424361e7e16e6fb10a8e9d34d7822e94383c0f2f8a7e08c1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771783d6469034a6ce0e040415b3c80bdb79954fdc4f4b9ea8371c635cdf4e19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:44:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:44:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:44:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:44:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:19 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:19 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:19 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2ea725d969b623cefe848599deff7717654cc1a341242805cd12b38f71f224`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b40f257a593b129d08f2d884dd256c3247d343203e39947f95d30e565d27582`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9303602f4ec278dc975499c1e851f5cac170cf094a2016ccf1e3e825ca6044`  
		Last Modified: Thu, 25 Jan 2024 01:47:19 GMT  
		Size: 115.4 MB (115369465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16.0-community`

```console
$ docker pull neo4j@sha256:bcd5c1641fb6a373af1b7d5b7202854c301c04f9c9ff83eab237c998f9e99bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:1b4e537b641cacb70112e893e64f91f15df1fbd085dbb9a8b7b5aa21268eb345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb6f43b1fe2495633d36fcd70e1adb50c1f4a21286b966d48c8e575e56b6524`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:57:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:57:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:57:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:57:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:57:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:57:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:57:55 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:57:55 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:57:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:57:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60004b8ae6cd6e559abc76f4bcaf8a36e1bbbd17a6b51e62f483bb0a6e023ca`  
		Last Modified: Thu, 25 Jan 2024 01:00:28 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805cbf4626c9acf5d5dee8fcb193ab7287068f983b7959db1ecd4c1730728cff`  
		Last Modified: Thu, 25 Jan 2024 01:00:27 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa863e248b55c5b258795bf6677bd81fd3cb7c099c9c31c987c1cf3df2b59fb`  
		Last Modified: Thu, 25 Jan 2024 01:00:33 GMT  
		Size: 115.4 MB (115406727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8aecbb6ec30763424361e7e16e6fb10a8e9d34d7822e94383c0f2f8a7e08c1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771783d6469034a6ce0e040415b3c80bdb79954fdc4f4b9ea8371c635cdf4e19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:44:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:44:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:44:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:44:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:19 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:19 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:19 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2ea725d969b623cefe848599deff7717654cc1a341242805cd12b38f71f224`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b40f257a593b129d08f2d884dd256c3247d343203e39947f95d30e565d27582`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9303602f4ec278dc975499c1e851f5cac170cf094a2016ccf1e3e825ca6044`  
		Last Modified: Thu, 25 Jan 2024 01:47:19 GMT  
		Size: 115.4 MB (115369465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16.0-community-bullseye`

```console
$ docker pull neo4j@sha256:bcd5c1641fb6a373af1b7d5b7202854c301c04f9c9ff83eab237c998f9e99bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1b4e537b641cacb70112e893e64f91f15df1fbd085dbb9a8b7b5aa21268eb345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb6f43b1fe2495633d36fcd70e1adb50c1f4a21286b966d48c8e575e56b6524`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:57:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:57:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:57:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:57:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:57:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:57:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:57:55 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:57:55 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:57:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:57:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60004b8ae6cd6e559abc76f4bcaf8a36e1bbbd17a6b51e62f483bb0a6e023ca`  
		Last Modified: Thu, 25 Jan 2024 01:00:28 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805cbf4626c9acf5d5dee8fcb193ab7287068f983b7959db1ecd4c1730728cff`  
		Last Modified: Thu, 25 Jan 2024 01:00:27 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa863e248b55c5b258795bf6677bd81fd3cb7c099c9c31c987c1cf3df2b59fb`  
		Last Modified: Thu, 25 Jan 2024 01:00:33 GMT  
		Size: 115.4 MB (115406727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8aecbb6ec30763424361e7e16e6fb10a8e9d34d7822e94383c0f2f8a7e08c1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771783d6469034a6ce0e040415b3c80bdb79954fdc4f4b9ea8371c635cdf4e19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:44:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:44:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:44:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:44:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:19 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:19 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:19 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2ea725d969b623cefe848599deff7717654cc1a341242805cd12b38f71f224`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b40f257a593b129d08f2d884dd256c3247d343203e39947f95d30e565d27582`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9303602f4ec278dc975499c1e851f5cac170cf094a2016ccf1e3e825ca6044`  
		Last Modified: Thu, 25 Jan 2024 01:47:19 GMT  
		Size: 115.4 MB (115369465 bytes)  
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
$ docker pull neo4j@sha256:f17f0c65c19f787443b51b23c2de7c1ee9f8923b9941f2ebaf71db4f018fe759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:6d89af695f3771e3de8ea57d2f1e5548a9f6b633576b1623c628b4e947fa62f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547749860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cfc9f2671fcd17ceff0f129c4834597648f16db159e6f865f5c7a83074c99c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:58:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:58:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:58:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:58:03 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:58:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:58:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:58:37 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:58:37 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:58:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:58:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8bd383ee7f871467af965fb6ee8e60690e50153eac9e499338de8efa070aa0`  
		Last Modified: Thu, 25 Jan 2024 01:01:07 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76109ffe52fc0e9e6e4f06eb1cfdf97946f3c2579bb50d345821d9c23ee64a46`  
		Last Modified: Thu, 25 Jan 2024 01:01:07 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544922daf3eb961c0d0c352ad0316db1cccb5a80b8b25788b58c794cea97969a`  
		Last Modified: Thu, 25 Jan 2024 01:01:22 GMT  
		Size: 371.4 MB (371426016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bbd8bf364795ae58f106d56bc6a1aa4cecf7bb227588f798a77776cf8b09cef3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545193013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54f0705b46de6448c37b6330194747a36ab7d6e7556ce8945122b150de2701d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:45:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:45:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:45:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:45:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:52 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:52 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6936427b58f4516446f43c682b389cb5eb161e6726f54e09bcca756d10a2d8`  
		Last Modified: Thu, 25 Jan 2024 01:47:51 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3810827657c95d91034f6faa07d5f0ac00b0a3f1345e85aa5fcc4cee246eb77`  
		Last Modified: Thu, 25 Jan 2024 01:47:51 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85034c4bed730f5b7a04fba0f732444b653d49aba938fbd07fb1d0ea339965f5`  
		Last Modified: Thu, 25 Jan 2024 01:48:03 GMT  
		Size: 371.4 MB (371394755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.16.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:f17f0c65c19f787443b51b23c2de7c1ee9f8923b9941f2ebaf71db4f018fe759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.16.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:6d89af695f3771e3de8ea57d2f1e5548a9f6b633576b1623c628b4e947fa62f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547749860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cfc9f2671fcd17ceff0f129c4834597648f16db159e6f865f5c7a83074c99c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:58:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:58:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:58:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:58:03 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:58:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:58:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:58:37 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:58:37 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:58:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:58:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8bd383ee7f871467af965fb6ee8e60690e50153eac9e499338de8efa070aa0`  
		Last Modified: Thu, 25 Jan 2024 01:01:07 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76109ffe52fc0e9e6e4f06eb1cfdf97946f3c2579bb50d345821d9c23ee64a46`  
		Last Modified: Thu, 25 Jan 2024 01:01:07 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544922daf3eb961c0d0c352ad0316db1cccb5a80b8b25788b58c794cea97969a`  
		Last Modified: Thu, 25 Jan 2024 01:01:22 GMT  
		Size: 371.4 MB (371426016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.16.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bbd8bf364795ae58f106d56bc6a1aa4cecf7bb227588f798a77776cf8b09cef3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545193013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54f0705b46de6448c37b6330194747a36ab7d6e7556ce8945122b150de2701d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:45:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:45:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:45:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:45:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:52 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:52 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6936427b58f4516446f43c682b389cb5eb161e6726f54e09bcca756d10a2d8`  
		Last Modified: Thu, 25 Jan 2024 01:47:51 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3810827657c95d91034f6faa07d5f0ac00b0a3f1345e85aa5fcc4cee246eb77`  
		Last Modified: Thu, 25 Jan 2024 01:47:51 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85034c4bed730f5b7a04fba0f732444b653d49aba938fbd07fb1d0ea339965f5`  
		Last Modified: Thu, 25 Jan 2024 01:48:03 GMT  
		Size: 371.4 MB (371394755 bytes)  
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
$ docker pull neo4j@sha256:bcd5c1641fb6a373af1b7d5b7202854c301c04f9c9ff83eab237c998f9e99bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1b4e537b641cacb70112e893e64f91f15df1fbd085dbb9a8b7b5aa21268eb345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb6f43b1fe2495633d36fcd70e1adb50c1f4a21286b966d48c8e575e56b6524`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:57:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:57:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:57:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:57:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:57:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:57:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:57:55 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:57:55 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:57:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:57:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60004b8ae6cd6e559abc76f4bcaf8a36e1bbbd17a6b51e62f483bb0a6e023ca`  
		Last Modified: Thu, 25 Jan 2024 01:00:28 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805cbf4626c9acf5d5dee8fcb193ab7287068f983b7959db1ecd4c1730728cff`  
		Last Modified: Thu, 25 Jan 2024 01:00:27 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa863e248b55c5b258795bf6677bd81fd3cb7c099c9c31c987c1cf3df2b59fb`  
		Last Modified: Thu, 25 Jan 2024 01:00:33 GMT  
		Size: 115.4 MB (115406727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8aecbb6ec30763424361e7e16e6fb10a8e9d34d7822e94383c0f2f8a7e08c1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771783d6469034a6ce0e040415b3c80bdb79954fdc4f4b9ea8371c635cdf4e19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:44:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:44:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:44:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:44:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:19 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:19 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:19 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2ea725d969b623cefe848599deff7717654cc1a341242805cd12b38f71f224`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b40f257a593b129d08f2d884dd256c3247d343203e39947f95d30e565d27582`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9303602f4ec278dc975499c1e851f5cac170cf094a2016ccf1e3e825ca6044`  
		Last Modified: Thu, 25 Jan 2024 01:47:19 GMT  
		Size: 115.4 MB (115369465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:bcd5c1641fb6a373af1b7d5b7202854c301c04f9c9ff83eab237c998f9e99bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:1b4e537b641cacb70112e893e64f91f15df1fbd085dbb9a8b7b5aa21268eb345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb6f43b1fe2495633d36fcd70e1adb50c1f4a21286b966d48c8e575e56b6524`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:57:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:57:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:57:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:57:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:57:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:57:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:57:55 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:57:55 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:57:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:57:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60004b8ae6cd6e559abc76f4bcaf8a36e1bbbd17a6b51e62f483bb0a6e023ca`  
		Last Modified: Thu, 25 Jan 2024 01:00:28 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805cbf4626c9acf5d5dee8fcb193ab7287068f983b7959db1ecd4c1730728cff`  
		Last Modified: Thu, 25 Jan 2024 01:00:27 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa863e248b55c5b258795bf6677bd81fd3cb7c099c9c31c987c1cf3df2b59fb`  
		Last Modified: Thu, 25 Jan 2024 01:00:33 GMT  
		Size: 115.4 MB (115406727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8aecbb6ec30763424361e7e16e6fb10a8e9d34d7822e94383c0f2f8a7e08c1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771783d6469034a6ce0e040415b3c80bdb79954fdc4f4b9ea8371c635cdf4e19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:44:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:44:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:44:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:44:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:19 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:19 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:19 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2ea725d969b623cefe848599deff7717654cc1a341242805cd12b38f71f224`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b40f257a593b129d08f2d884dd256c3247d343203e39947f95d30e565d27582`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9303602f4ec278dc975499c1e851f5cac170cf094a2016ccf1e3e825ca6044`  
		Last Modified: Thu, 25 Jan 2024 01:47:19 GMT  
		Size: 115.4 MB (115369465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:bcd5c1641fb6a373af1b7d5b7202854c301c04f9c9ff83eab237c998f9e99bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1b4e537b641cacb70112e893e64f91f15df1fbd085dbb9a8b7b5aa21268eb345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb6f43b1fe2495633d36fcd70e1adb50c1f4a21286b966d48c8e575e56b6524`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:57:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:57:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:57:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:57:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:57:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:57:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:57:55 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:57:55 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:57:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:57:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60004b8ae6cd6e559abc76f4bcaf8a36e1bbbd17a6b51e62f483bb0a6e023ca`  
		Last Modified: Thu, 25 Jan 2024 01:00:28 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805cbf4626c9acf5d5dee8fcb193ab7287068f983b7959db1ecd4c1730728cff`  
		Last Modified: Thu, 25 Jan 2024 01:00:27 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa863e248b55c5b258795bf6677bd81fd3cb7c099c9c31c987c1cf3df2b59fb`  
		Last Modified: Thu, 25 Jan 2024 01:00:33 GMT  
		Size: 115.4 MB (115406727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8aecbb6ec30763424361e7e16e6fb10a8e9d34d7822e94383c0f2f8a7e08c1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771783d6469034a6ce0e040415b3c80bdb79954fdc4f4b9ea8371c635cdf4e19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:44:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:44:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:44:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:44:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:19 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:19 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:19 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2ea725d969b623cefe848599deff7717654cc1a341242805cd12b38f71f224`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b40f257a593b129d08f2d884dd256c3247d343203e39947f95d30e565d27582`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9303602f4ec278dc975499c1e851f5cac170cf094a2016ccf1e3e825ca6044`  
		Last Modified: Thu, 25 Jan 2024 01:47:19 GMT  
		Size: 115.4 MB (115369465 bytes)  
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
$ docker pull neo4j@sha256:f17f0c65c19f787443b51b23c2de7c1ee9f8923b9941f2ebaf71db4f018fe759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:6d89af695f3771e3de8ea57d2f1e5548a9f6b633576b1623c628b4e947fa62f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547749860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cfc9f2671fcd17ceff0f129c4834597648f16db159e6f865f5c7a83074c99c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:58:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:58:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:58:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:58:03 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:58:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:58:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:58:37 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:58:37 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:58:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:58:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8bd383ee7f871467af965fb6ee8e60690e50153eac9e499338de8efa070aa0`  
		Last Modified: Thu, 25 Jan 2024 01:01:07 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76109ffe52fc0e9e6e4f06eb1cfdf97946f3c2579bb50d345821d9c23ee64a46`  
		Last Modified: Thu, 25 Jan 2024 01:01:07 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544922daf3eb961c0d0c352ad0316db1cccb5a80b8b25788b58c794cea97969a`  
		Last Modified: Thu, 25 Jan 2024 01:01:22 GMT  
		Size: 371.4 MB (371426016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bbd8bf364795ae58f106d56bc6a1aa4cecf7bb227588f798a77776cf8b09cef3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545193013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54f0705b46de6448c37b6330194747a36ab7d6e7556ce8945122b150de2701d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:45:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:45:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:45:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:45:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:52 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:52 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6936427b58f4516446f43c682b389cb5eb161e6726f54e09bcca756d10a2d8`  
		Last Modified: Thu, 25 Jan 2024 01:47:51 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3810827657c95d91034f6faa07d5f0ac00b0a3f1345e85aa5fcc4cee246eb77`  
		Last Modified: Thu, 25 Jan 2024 01:47:51 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85034c4bed730f5b7a04fba0f732444b653d49aba938fbd07fb1d0ea339965f5`  
		Last Modified: Thu, 25 Jan 2024 01:48:03 GMT  
		Size: 371.4 MB (371394755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:f17f0c65c19f787443b51b23c2de7c1ee9f8923b9941f2ebaf71db4f018fe759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:6d89af695f3771e3de8ea57d2f1e5548a9f6b633576b1623c628b4e947fa62f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547749860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cfc9f2671fcd17ceff0f129c4834597648f16db159e6f865f5c7a83074c99c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:58:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:58:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:58:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:58:03 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:58:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:58:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:58:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:58:37 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:58:37 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:58:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:58:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8bd383ee7f871467af965fb6ee8e60690e50153eac9e499338de8efa070aa0`  
		Last Modified: Thu, 25 Jan 2024 01:01:07 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76109ffe52fc0e9e6e4f06eb1cfdf97946f3c2579bb50d345821d9c23ee64a46`  
		Last Modified: Thu, 25 Jan 2024 01:01:07 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544922daf3eb961c0d0c352ad0316db1cccb5a80b8b25788b58c794cea97969a`  
		Last Modified: Thu, 25 Jan 2024 01:01:22 GMT  
		Size: 371.4 MB (371426016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bbd8bf364795ae58f106d56bc6a1aa4cecf7bb227588f798a77776cf8b09cef3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545193013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54f0705b46de6448c37b6330194747a36ab7d6e7556ce8945122b150de2701d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:45:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:45:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:45:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:45:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:52 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:52 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6936427b58f4516446f43c682b389cb5eb161e6726f54e09bcca756d10a2d8`  
		Last Modified: Thu, 25 Jan 2024 01:47:51 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3810827657c95d91034f6faa07d5f0ac00b0a3f1345e85aa5fcc4cee246eb77`  
		Last Modified: Thu, 25 Jan 2024 01:47:51 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85034c4bed730f5b7a04fba0f732444b653d49aba938fbd07fb1d0ea339965f5`  
		Last Modified: Thu, 25 Jan 2024 01:48:03 GMT  
		Size: 371.4 MB (371394755 bytes)  
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
$ docker pull neo4j@sha256:bcd5c1641fb6a373af1b7d5b7202854c301c04f9c9ff83eab237c998f9e99bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:1b4e537b641cacb70112e893e64f91f15df1fbd085dbb9a8b7b5aa21268eb345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291730569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb6f43b1fe2495633d36fcd70e1adb50c1f4a21286b966d48c8e575e56b6524`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Thu, 25 Jan 2024 00:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 00:57:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 00:57:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 00:57:22 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 00:57:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 00:57:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 00:57:55 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 00:57:55 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 00:57:55 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 00:57:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 00:57:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60004b8ae6cd6e559abc76f4bcaf8a36e1bbbd17a6b51e62f483bb0a6e023ca`  
		Last Modified: Thu, 25 Jan 2024 01:00:28 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805cbf4626c9acf5d5dee8fcb193ab7287068f983b7959db1ecd4c1730728cff`  
		Last Modified: Thu, 25 Jan 2024 01:00:27 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa863e248b55c5b258795bf6677bd81fd3cb7c099c9c31c987c1cf3df2b59fb`  
		Last Modified: Thu, 25 Jan 2024 01:00:33 GMT  
		Size: 115.4 MB (115406727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8aecbb6ec30763424361e7e16e6fb10a8e9d34d7822e94383c0f2f8a7e08c1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289167721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771783d6469034a6ce0e040415b3c80bdb79954fdc4f4b9ea8371c635cdf4e19`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 25 Jan 2024 01:44:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 25 Jan 2024 01:44:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Thu, 25 Jan 2024 01:44:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 25 Jan 2024 01:44:49 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Thu, 25 Jan 2024 01:45:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Thu, 25 Jan 2024 01:45:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jan 2024 01:45:19 GMT
WORKDIR /var/lib/neo4j
# Thu, 25 Jan 2024 01:45:19 GMT
VOLUME [/data /logs]
# Thu, 25 Jan 2024 01:45:19 GMT
EXPOSE 7473 7474 7687
# Thu, 25 Jan 2024 01:45:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 25 Jan 2024 01:45:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2ea725d969b623cefe848599deff7717654cc1a341242805cd12b38f71f224`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b40f257a593b129d08f2d884dd256c3247d343203e39947f95d30e565d27582`  
		Last Modified: Thu, 25 Jan 2024 01:47:13 GMT  
		Size: 9.5 KB (9487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9303602f4ec278dc975499c1e851f5cac170cf094a2016ccf1e3e825ca6044`  
		Last Modified: Thu, 25 Jan 2024 01:47:19 GMT  
		Size: 115.4 MB (115369465 bytes)  
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
