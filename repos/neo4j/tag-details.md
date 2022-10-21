<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.3`](#neo4j43)
-	[`neo4j:4.3-community`](#neo4j43-community)
-	[`neo4j:4.3-enterprise`](#neo4j43-enterprise)
-	[`neo4j:4.3.19`](#neo4j4319)
-	[`neo4j:4.3.19-community`](#neo4j4319-community)
-	[`neo4j:4.3.19-enterprise`](#neo4j4319-enterprise)
-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.12`](#neo4j4412)
-	[`neo4j:4.4.12-community`](#neo4j4412-community)
-	[`neo4j:4.4.12-enterprise`](#neo4j4412-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5.1.0`](#neo4j510)
-	[`neo4j:5.1.0-community`](#neo4j510-community)
-	[`neo4j:5.1.0-enterprise`](#neo4j510-enterprise)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:latest`](#neo4jlatest)

## `neo4j:4.3`

```console
$ docker pull neo4j@sha256:1f812cbf84ac974b8ec1e02bcbc63184af26f710ddfbfc3b83bf3f8ad94bb0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3` - linux; amd64

```console
$ docker pull neo4j@sha256:82632cff37ccb99e2c863b67b925419fcd7dd3e6a08c0f7c4f3f4cfca45e07c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359830984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc0051dc925c16c9527b6e07a9bf00b3013d7eed8a783ba6d129b5d4ffadf5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:51:16 GMT
COPY dir:e3c63d67b32fccda756dd62000a0cf47da966d18fe6f1f25cd1f37b60881f0ec in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:21:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=55e4dec03a4424933d753387913a38ac2a6100dbfbb1cd976b3958fb8489e3a7 NEO4J_TARBALL=neo4j-community-4.3.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:21:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
# Fri, 14 Oct 2022 21:21:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:21:01 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Fri, 14 Oct 2022 21:21:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:21:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:21:13 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:21:13 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:21:13 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:21:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:21:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411b6cb0e944ff13c8e89f4a886c731ea8293c8f3dbc5d78ed1df2e6fbef5b9`  
		Last Modified: Thu, 06 Oct 2022 04:08:54 GMT  
		Size: 198.1 MB (198124981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32100031fa0df58d1a737feb53dabce362781ab9807ba26efc72ad1676b37d70`  
		Last Modified: Fri, 14 Oct 2022 21:23:21 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c70486fd88fe318f6be32cf1d6693a505f3845534cf403c8b4d2e15415a698b`  
		Last Modified: Fri, 14 Oct 2022 21:23:21 GMT  
		Size: 7.6 KB (7626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890bc0bbd243a87948c29dda33e73ca84faf4bc1b876b1249fefef543878e331`  
		Last Modified: Fri, 14 Oct 2022 21:23:28 GMT  
		Size: 130.3 MB (130274418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3-community`

```console
$ docker pull neo4j@sha256:1f812cbf84ac974b8ec1e02bcbc63184af26f710ddfbfc3b83bf3f8ad94bb0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3-community` - linux; amd64

```console
$ docker pull neo4j@sha256:82632cff37ccb99e2c863b67b925419fcd7dd3e6a08c0f7c4f3f4cfca45e07c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359830984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc0051dc925c16c9527b6e07a9bf00b3013d7eed8a783ba6d129b5d4ffadf5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:51:16 GMT
COPY dir:e3c63d67b32fccda756dd62000a0cf47da966d18fe6f1f25cd1f37b60881f0ec in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:21:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=55e4dec03a4424933d753387913a38ac2a6100dbfbb1cd976b3958fb8489e3a7 NEO4J_TARBALL=neo4j-community-4.3.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:21:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
# Fri, 14 Oct 2022 21:21:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:21:01 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Fri, 14 Oct 2022 21:21:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:21:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:21:13 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:21:13 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:21:13 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:21:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:21:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411b6cb0e944ff13c8e89f4a886c731ea8293c8f3dbc5d78ed1df2e6fbef5b9`  
		Last Modified: Thu, 06 Oct 2022 04:08:54 GMT  
		Size: 198.1 MB (198124981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32100031fa0df58d1a737feb53dabce362781ab9807ba26efc72ad1676b37d70`  
		Last Modified: Fri, 14 Oct 2022 21:23:21 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c70486fd88fe318f6be32cf1d6693a505f3845534cf403c8b4d2e15415a698b`  
		Last Modified: Fri, 14 Oct 2022 21:23:21 GMT  
		Size: 7.6 KB (7626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890bc0bbd243a87948c29dda33e73ca84faf4bc1b876b1249fefef543878e331`  
		Last Modified: Fri, 14 Oct 2022 21:23:28 GMT  
		Size: 130.3 MB (130274418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3-enterprise`

```console
$ docker pull neo4j@sha256:dec06ef3c403919d5bbd7e86600de1cd98f25450cf037e3213fede22966446a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:c85143be43fdc23301aa4ad8eebbf0927e59b792145d898486c89a3a198c94b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 MB (390318762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ff698173ca779964f887ad85f7b97793669a7039ac77ebd3131301ce891982`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:51:16 GMT
COPY dir:e3c63d67b32fccda756dd62000a0cf47da966d18fe6f1f25cd1f37b60881f0ec in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:21:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4f574dc264853263b865d9c696b389c6dd3e4c9bf7adb84d2f6ac87f907a561c NEO4J_TARBALL=neo4j-enterprise-4.3.19-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:21:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.19-unix.tar.gz
# Fri, 14 Oct 2022 21:21:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:21:18 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Fri, 14 Oct 2022 21:21:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:21:30 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:21:31 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:21:31 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:21:31 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:21:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:21:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411b6cb0e944ff13c8e89f4a886c731ea8293c8f3dbc5d78ed1df2e6fbef5b9`  
		Last Modified: Thu, 06 Oct 2022 04:08:54 GMT  
		Size: 198.1 MB (198124981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4dd0e61dd46338de13f630cc953595e853729840536a28360b8a0ac7fa75867`  
		Last Modified: Fri, 14 Oct 2022 21:23:42 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665d31b0693235e1a81837b27c6e13c78be0910017b2c7da808415421544b8a0`  
		Last Modified: Fri, 14 Oct 2022 21:23:42 GMT  
		Size: 7.6 KB (7626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77769066af457107db71c3b1c07570f95e5c2c9c21e799d2953b109c4d64e0aa`  
		Last Modified: Fri, 14 Oct 2022 21:23:50 GMT  
		Size: 160.8 MB (160762193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.19`

```console
$ docker pull neo4j@sha256:1f812cbf84ac974b8ec1e02bcbc63184af26f710ddfbfc3b83bf3f8ad94bb0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.19` - linux; amd64

```console
$ docker pull neo4j@sha256:82632cff37ccb99e2c863b67b925419fcd7dd3e6a08c0f7c4f3f4cfca45e07c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359830984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc0051dc925c16c9527b6e07a9bf00b3013d7eed8a783ba6d129b5d4ffadf5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:51:16 GMT
COPY dir:e3c63d67b32fccda756dd62000a0cf47da966d18fe6f1f25cd1f37b60881f0ec in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:21:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=55e4dec03a4424933d753387913a38ac2a6100dbfbb1cd976b3958fb8489e3a7 NEO4J_TARBALL=neo4j-community-4.3.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:21:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
# Fri, 14 Oct 2022 21:21:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:21:01 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Fri, 14 Oct 2022 21:21:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:21:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:21:13 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:21:13 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:21:13 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:21:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:21:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411b6cb0e944ff13c8e89f4a886c731ea8293c8f3dbc5d78ed1df2e6fbef5b9`  
		Last Modified: Thu, 06 Oct 2022 04:08:54 GMT  
		Size: 198.1 MB (198124981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32100031fa0df58d1a737feb53dabce362781ab9807ba26efc72ad1676b37d70`  
		Last Modified: Fri, 14 Oct 2022 21:23:21 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c70486fd88fe318f6be32cf1d6693a505f3845534cf403c8b4d2e15415a698b`  
		Last Modified: Fri, 14 Oct 2022 21:23:21 GMT  
		Size: 7.6 KB (7626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890bc0bbd243a87948c29dda33e73ca84faf4bc1b876b1249fefef543878e331`  
		Last Modified: Fri, 14 Oct 2022 21:23:28 GMT  
		Size: 130.3 MB (130274418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.19-community`

```console
$ docker pull neo4j@sha256:1f812cbf84ac974b8ec1e02bcbc63184af26f710ddfbfc3b83bf3f8ad94bb0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.19-community` - linux; amd64

```console
$ docker pull neo4j@sha256:82632cff37ccb99e2c863b67b925419fcd7dd3e6a08c0f7c4f3f4cfca45e07c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359830984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc0051dc925c16c9527b6e07a9bf00b3013d7eed8a783ba6d129b5d4ffadf5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:51:16 GMT
COPY dir:e3c63d67b32fccda756dd62000a0cf47da966d18fe6f1f25cd1f37b60881f0ec in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:21:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=55e4dec03a4424933d753387913a38ac2a6100dbfbb1cd976b3958fb8489e3a7 NEO4J_TARBALL=neo4j-community-4.3.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:21:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
# Fri, 14 Oct 2022 21:21:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:21:01 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Fri, 14 Oct 2022 21:21:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:21:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:21:13 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:21:13 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:21:13 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:21:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:21:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411b6cb0e944ff13c8e89f4a886c731ea8293c8f3dbc5d78ed1df2e6fbef5b9`  
		Last Modified: Thu, 06 Oct 2022 04:08:54 GMT  
		Size: 198.1 MB (198124981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32100031fa0df58d1a737feb53dabce362781ab9807ba26efc72ad1676b37d70`  
		Last Modified: Fri, 14 Oct 2022 21:23:21 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c70486fd88fe318f6be32cf1d6693a505f3845534cf403c8b4d2e15415a698b`  
		Last Modified: Fri, 14 Oct 2022 21:23:21 GMT  
		Size: 7.6 KB (7626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890bc0bbd243a87948c29dda33e73ca84faf4bc1b876b1249fefef543878e331`  
		Last Modified: Fri, 14 Oct 2022 21:23:28 GMT  
		Size: 130.3 MB (130274418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.19-enterprise`

```console
$ docker pull neo4j@sha256:dec06ef3c403919d5bbd7e86600de1cd98f25450cf037e3213fede22966446a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.19-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:c85143be43fdc23301aa4ad8eebbf0927e59b792145d898486c89a3a198c94b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 MB (390318762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ff698173ca779964f887ad85f7b97793669a7039ac77ebd3131301ce891982`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:51:16 GMT
COPY dir:e3c63d67b32fccda756dd62000a0cf47da966d18fe6f1f25cd1f37b60881f0ec in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:21:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4f574dc264853263b865d9c696b389c6dd3e4c9bf7adb84d2f6ac87f907a561c NEO4J_TARBALL=neo4j-enterprise-4.3.19-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:21:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.19-unix.tar.gz
# Fri, 14 Oct 2022 21:21:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:21:18 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Fri, 14 Oct 2022 21:21:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:21:30 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:21:31 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:21:31 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:21:31 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:21:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:21:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411b6cb0e944ff13c8e89f4a886c731ea8293c8f3dbc5d78ed1df2e6fbef5b9`  
		Last Modified: Thu, 06 Oct 2022 04:08:54 GMT  
		Size: 198.1 MB (198124981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4dd0e61dd46338de13f630cc953595e853729840536a28360b8a0ac7fa75867`  
		Last Modified: Fri, 14 Oct 2022 21:23:42 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665d31b0693235e1a81837b27c6e13c78be0910017b2c7da808415421544b8a0`  
		Last Modified: Fri, 14 Oct 2022 21:23:42 GMT  
		Size: 7.6 KB (7626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77769066af457107db71c3b1c07570f95e5c2c9c21e799d2953b109c4d64e0aa`  
		Last Modified: Fri, 14 Oct 2022 21:23:50 GMT  
		Size: 160.8 MB (160762193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:b8bd93e9a9256c24e89d57299cf37a2f890b463a981eec8d4e8b5e621a874e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:17334cbc668d852ca8a3d8590f66c4fda64d9c7de7d93cc62803f534ae7dbce6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364700569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ae5bfb75495d129630107d1dc2ff2fac5a5988315c7c0383ba4a448632e78b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:51:16 GMT
COPY dir:e3c63d67b32fccda756dd62000a0cf47da966d18fe6f1f25cd1f37b60881f0ec in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:19:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=58f2ab847b1898c3f33731dc247784459223185307a4c89757f43ea94eb2a491 NEO4J_TARBALL=neo4j-community-4.4.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:19:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
# Fri, 14 Oct 2022 21:19:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:19:59 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Fri, 14 Oct 2022 21:20:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:20:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:20:12 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:20:12 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:20:13 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:20:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:20:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411b6cb0e944ff13c8e89f4a886c731ea8293c8f3dbc5d78ed1df2e6fbef5b9`  
		Last Modified: Thu, 06 Oct 2022 04:08:54 GMT  
		Size: 198.1 MB (198124981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aaaaf8954c2ff61e744735d2032871d4080c8bed1b8c878313d64c2dac07254`  
		Last Modified: Fri, 14 Oct 2022 21:22:29 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7c1680a7fe090ca41b7fffbd63d3a951f0e80c76f43334f336ba552d885eb0`  
		Last Modified: Fri, 14 Oct 2022 21:22:28 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a0126ab25e546fa6b2fb0f68c2737627f4dee15f96c92b4bea749a07d0f91e`  
		Last Modified: Fri, 14 Oct 2022 21:22:35 GMT  
		Size: 135.1 MB (135144015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15aabe0a070a165e52ae3bf8781bcbdc6588ee4935f0a5c0c544f3da3301d743
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359736471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530ec3c2144ed1ade06f96a81979f7ecbb3c8383fcce46c162cd38e94284faa5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:32:30 GMT
COPY dir:0dc06d70d42a32ae203bdf41d3806f1204b90ca101c4efe4662ba862f2c76b8a in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:40:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=58f2ab847b1898c3f33731dc247784459223185307a4c89757f43ea94eb2a491 NEO4J_TARBALL=neo4j-community-4.4.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:40:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
# Fri, 14 Oct 2022 21:40:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:40:46 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Fri, 14 Oct 2022 21:40:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:40:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:40:58 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:40:59 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:41:00 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:41:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:41:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bfdcb0b9c92e9c3da0e6ca913cb8d3cf77c13d55a20c234730a5896afdec4a`  
		Last Modified: Thu, 06 Oct 2022 02:57:34 GMT  
		Size: 194.9 MB (194866592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9484df044d656b445873a7daa65c765f30d6896c583418086772c0d902a5b94`  
		Last Modified: Fri, 14 Oct 2022 21:42:43 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885002c3309b298661a5b4a76d61e67ff3c385070fedb22692774343f3c93e2c`  
		Last Modified: Fri, 14 Oct 2022 21:42:43 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eca9d5d225cef9f0d9f1bec2a18e72eebd5e333f79e022b3f31a4f6bf8e2f50`  
		Last Modified: Fri, 14 Oct 2022 21:42:52 GMT  
		Size: 134.8 MB (134794066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:b8bd93e9a9256c24e89d57299cf37a2f890b463a981eec8d4e8b5e621a874e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:17334cbc668d852ca8a3d8590f66c4fda64d9c7de7d93cc62803f534ae7dbce6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364700569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ae5bfb75495d129630107d1dc2ff2fac5a5988315c7c0383ba4a448632e78b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:51:16 GMT
COPY dir:e3c63d67b32fccda756dd62000a0cf47da966d18fe6f1f25cd1f37b60881f0ec in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:19:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=58f2ab847b1898c3f33731dc247784459223185307a4c89757f43ea94eb2a491 NEO4J_TARBALL=neo4j-community-4.4.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:19:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
# Fri, 14 Oct 2022 21:19:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:19:59 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Fri, 14 Oct 2022 21:20:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:20:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:20:12 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:20:12 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:20:13 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:20:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:20:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411b6cb0e944ff13c8e89f4a886c731ea8293c8f3dbc5d78ed1df2e6fbef5b9`  
		Last Modified: Thu, 06 Oct 2022 04:08:54 GMT  
		Size: 198.1 MB (198124981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aaaaf8954c2ff61e744735d2032871d4080c8bed1b8c878313d64c2dac07254`  
		Last Modified: Fri, 14 Oct 2022 21:22:29 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7c1680a7fe090ca41b7fffbd63d3a951f0e80c76f43334f336ba552d885eb0`  
		Last Modified: Fri, 14 Oct 2022 21:22:28 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a0126ab25e546fa6b2fb0f68c2737627f4dee15f96c92b4bea749a07d0f91e`  
		Last Modified: Fri, 14 Oct 2022 21:22:35 GMT  
		Size: 135.1 MB (135144015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15aabe0a070a165e52ae3bf8781bcbdc6588ee4935f0a5c0c544f3da3301d743
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359736471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530ec3c2144ed1ade06f96a81979f7ecbb3c8383fcce46c162cd38e94284faa5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:32:30 GMT
COPY dir:0dc06d70d42a32ae203bdf41d3806f1204b90ca101c4efe4662ba862f2c76b8a in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:40:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=58f2ab847b1898c3f33731dc247784459223185307a4c89757f43ea94eb2a491 NEO4J_TARBALL=neo4j-community-4.4.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:40:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
# Fri, 14 Oct 2022 21:40:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:40:46 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Fri, 14 Oct 2022 21:40:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:40:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:40:58 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:40:59 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:41:00 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:41:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:41:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bfdcb0b9c92e9c3da0e6ca913cb8d3cf77c13d55a20c234730a5896afdec4a`  
		Last Modified: Thu, 06 Oct 2022 02:57:34 GMT  
		Size: 194.9 MB (194866592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9484df044d656b445873a7daa65c765f30d6896c583418086772c0d902a5b94`  
		Last Modified: Fri, 14 Oct 2022 21:42:43 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885002c3309b298661a5b4a76d61e67ff3c385070fedb22692774343f3c93e2c`  
		Last Modified: Fri, 14 Oct 2022 21:42:43 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eca9d5d225cef9f0d9f1bec2a18e72eebd5e333f79e022b3f31a4f6bf8e2f50`  
		Last Modified: Fri, 14 Oct 2022 21:42:52 GMT  
		Size: 134.8 MB (134794066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:af21862908e801ee3e4783d996efe873409492acbd152d3d8b0766b73890c7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8e42a92720d1eaeeb21bde7fa086252df23aea5b900b28a61cd49298efe0b84d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.5 MB (459549712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64df2f843720a7fa616ddc08d1f7f2b12408991615bb5cba8c4dcd156da3c406`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:51:16 GMT
COPY dir:e3c63d67b32fccda756dd62000a0cf47da966d18fe6f1f25cd1f37b60881f0ec in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:20:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f0eff8c70ec5666169803d3d29363b770cd767f5737c8495e2daa3808c87836f NEO4J_TARBALL=neo4j-enterprise-4.4.12-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:20:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
# Fri, 14 Oct 2022 21:20:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:20:19 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Fri, 14 Oct 2022 21:20:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:20:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:20:41 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:20:41 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:20:42 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:20:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:20:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411b6cb0e944ff13c8e89f4a886c731ea8293c8f3dbc5d78ed1df2e6fbef5b9`  
		Last Modified: Thu, 06 Oct 2022 04:08:54 GMT  
		Size: 198.1 MB (198124981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba558a79e0d400395a055d250ff767069bf9dd44bb6888298ada302a90e54`  
		Last Modified: Fri, 14 Oct 2022 21:22:54 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3b79c9113a9b467ce260487eeef01e8cbdf07589d7097cc702567b975398a0`  
		Last Modified: Fri, 14 Oct 2022 21:22:54 GMT  
		Size: 7.6 KB (7614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4142eb9018d23d23ca0266ccc7c7ca3dc13080f7883a0a70afaeda87b6313058`  
		Last Modified: Fri, 14 Oct 2022 21:23:06 GMT  
		Size: 230.0 MB (229993160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b06e0ccf7e63b4657ff2a923f11022f4beafeb743e8fbdd5961e583d07005cb4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.6 MB (454585249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a289397c97545617681b8c9968ec5b28c5ef288d3c2887f12062cbf342ab9a5e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:32:30 GMT
COPY dir:0dc06d70d42a32ae203bdf41d3806f1204b90ca101c4efe4662ba862f2c76b8a in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:41:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f0eff8c70ec5666169803d3d29363b770cd767f5737c8495e2daa3808c87836f NEO4J_TARBALL=neo4j-enterprise-4.4.12-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:41:11 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
# Fri, 14 Oct 2022 21:41:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:41:14 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Fri, 14 Oct 2022 21:41:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:41:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:41:29 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:41:30 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:41:31 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:41:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:41:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bfdcb0b9c92e9c3da0e6ca913cb8d3cf77c13d55a20c234730a5896afdec4a`  
		Last Modified: Thu, 06 Oct 2022 02:57:34 GMT  
		Size: 194.9 MB (194866592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfdbc40515d5ea11f90fdc78603767ed197ef8fa4d888f4c4026262ccc3be3f`  
		Last Modified: Fri, 14 Oct 2022 21:43:15 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf1f26f166c527f7e1d229ef3f0763ddc6ab845a1059da71d8b4e08a001c082`  
		Last Modified: Fri, 14 Oct 2022 21:43:15 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72a648573de11717d92f64374bdd6ff1337e319707fdd3e22d2628c2203c449`  
		Last Modified: Fri, 14 Oct 2022 21:43:30 GMT  
		Size: 229.6 MB (229642844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.12`

```console
$ docker pull neo4j@sha256:b8bd93e9a9256c24e89d57299cf37a2f890b463a981eec8d4e8b5e621a874e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.12` - linux; amd64

```console
$ docker pull neo4j@sha256:17334cbc668d852ca8a3d8590f66c4fda64d9c7de7d93cc62803f534ae7dbce6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364700569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ae5bfb75495d129630107d1dc2ff2fac5a5988315c7c0383ba4a448632e78b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:51:16 GMT
COPY dir:e3c63d67b32fccda756dd62000a0cf47da966d18fe6f1f25cd1f37b60881f0ec in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:19:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=58f2ab847b1898c3f33731dc247784459223185307a4c89757f43ea94eb2a491 NEO4J_TARBALL=neo4j-community-4.4.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:19:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
# Fri, 14 Oct 2022 21:19:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:19:59 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Fri, 14 Oct 2022 21:20:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:20:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:20:12 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:20:12 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:20:13 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:20:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:20:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411b6cb0e944ff13c8e89f4a886c731ea8293c8f3dbc5d78ed1df2e6fbef5b9`  
		Last Modified: Thu, 06 Oct 2022 04:08:54 GMT  
		Size: 198.1 MB (198124981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aaaaf8954c2ff61e744735d2032871d4080c8bed1b8c878313d64c2dac07254`  
		Last Modified: Fri, 14 Oct 2022 21:22:29 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7c1680a7fe090ca41b7fffbd63d3a951f0e80c76f43334f336ba552d885eb0`  
		Last Modified: Fri, 14 Oct 2022 21:22:28 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a0126ab25e546fa6b2fb0f68c2737627f4dee15f96c92b4bea749a07d0f91e`  
		Last Modified: Fri, 14 Oct 2022 21:22:35 GMT  
		Size: 135.1 MB (135144015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.12` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15aabe0a070a165e52ae3bf8781bcbdc6588ee4935f0a5c0c544f3da3301d743
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359736471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530ec3c2144ed1ade06f96a81979f7ecbb3c8383fcce46c162cd38e94284faa5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:32:30 GMT
COPY dir:0dc06d70d42a32ae203bdf41d3806f1204b90ca101c4efe4662ba862f2c76b8a in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:40:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=58f2ab847b1898c3f33731dc247784459223185307a4c89757f43ea94eb2a491 NEO4J_TARBALL=neo4j-community-4.4.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:40:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
# Fri, 14 Oct 2022 21:40:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:40:46 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Fri, 14 Oct 2022 21:40:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:40:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:40:58 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:40:59 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:41:00 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:41:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:41:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bfdcb0b9c92e9c3da0e6ca913cb8d3cf77c13d55a20c234730a5896afdec4a`  
		Last Modified: Thu, 06 Oct 2022 02:57:34 GMT  
		Size: 194.9 MB (194866592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9484df044d656b445873a7daa65c765f30d6896c583418086772c0d902a5b94`  
		Last Modified: Fri, 14 Oct 2022 21:42:43 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885002c3309b298661a5b4a76d61e67ff3c385070fedb22692774343f3c93e2c`  
		Last Modified: Fri, 14 Oct 2022 21:42:43 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eca9d5d225cef9f0d9f1bec2a18e72eebd5e333f79e022b3f31a4f6bf8e2f50`  
		Last Modified: Fri, 14 Oct 2022 21:42:52 GMT  
		Size: 134.8 MB (134794066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.12-community`

```console
$ docker pull neo4j@sha256:b8bd93e9a9256c24e89d57299cf37a2f890b463a981eec8d4e8b5e621a874e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.12-community` - linux; amd64

```console
$ docker pull neo4j@sha256:17334cbc668d852ca8a3d8590f66c4fda64d9c7de7d93cc62803f534ae7dbce6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364700569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ae5bfb75495d129630107d1dc2ff2fac5a5988315c7c0383ba4a448632e78b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:51:16 GMT
COPY dir:e3c63d67b32fccda756dd62000a0cf47da966d18fe6f1f25cd1f37b60881f0ec in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:19:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=58f2ab847b1898c3f33731dc247784459223185307a4c89757f43ea94eb2a491 NEO4J_TARBALL=neo4j-community-4.4.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:19:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
# Fri, 14 Oct 2022 21:19:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:19:59 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Fri, 14 Oct 2022 21:20:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:20:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:20:12 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:20:12 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:20:13 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:20:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:20:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411b6cb0e944ff13c8e89f4a886c731ea8293c8f3dbc5d78ed1df2e6fbef5b9`  
		Last Modified: Thu, 06 Oct 2022 04:08:54 GMT  
		Size: 198.1 MB (198124981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aaaaf8954c2ff61e744735d2032871d4080c8bed1b8c878313d64c2dac07254`  
		Last Modified: Fri, 14 Oct 2022 21:22:29 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7c1680a7fe090ca41b7fffbd63d3a951f0e80c76f43334f336ba552d885eb0`  
		Last Modified: Fri, 14 Oct 2022 21:22:28 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a0126ab25e546fa6b2fb0f68c2737627f4dee15f96c92b4bea749a07d0f91e`  
		Last Modified: Fri, 14 Oct 2022 21:22:35 GMT  
		Size: 135.1 MB (135144015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.12-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15aabe0a070a165e52ae3bf8781bcbdc6588ee4935f0a5c0c544f3da3301d743
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359736471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530ec3c2144ed1ade06f96a81979f7ecbb3c8383fcce46c162cd38e94284faa5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:32:30 GMT
COPY dir:0dc06d70d42a32ae203bdf41d3806f1204b90ca101c4efe4662ba862f2c76b8a in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:40:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=58f2ab847b1898c3f33731dc247784459223185307a4c89757f43ea94eb2a491 NEO4J_TARBALL=neo4j-community-4.4.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:40:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
# Fri, 14 Oct 2022 21:40:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:40:46 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Fri, 14 Oct 2022 21:40:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:40:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:40:58 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:40:59 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:41:00 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:41:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:41:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bfdcb0b9c92e9c3da0e6ca913cb8d3cf77c13d55a20c234730a5896afdec4a`  
		Last Modified: Thu, 06 Oct 2022 02:57:34 GMT  
		Size: 194.9 MB (194866592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9484df044d656b445873a7daa65c765f30d6896c583418086772c0d902a5b94`  
		Last Modified: Fri, 14 Oct 2022 21:42:43 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885002c3309b298661a5b4a76d61e67ff3c385070fedb22692774343f3c93e2c`  
		Last Modified: Fri, 14 Oct 2022 21:42:43 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eca9d5d225cef9f0d9f1bec2a18e72eebd5e333f79e022b3f31a4f6bf8e2f50`  
		Last Modified: Fri, 14 Oct 2022 21:42:52 GMT  
		Size: 134.8 MB (134794066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.12-enterprise`

```console
$ docker pull neo4j@sha256:af21862908e801ee3e4783d996efe873409492acbd152d3d8b0766b73890c7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.12-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8e42a92720d1eaeeb21bde7fa086252df23aea5b900b28a61cd49298efe0b84d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.5 MB (459549712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64df2f843720a7fa616ddc08d1f7f2b12408991615bb5cba8c4dcd156da3c406`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:51:16 GMT
COPY dir:e3c63d67b32fccda756dd62000a0cf47da966d18fe6f1f25cd1f37b60881f0ec in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:20:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f0eff8c70ec5666169803d3d29363b770cd767f5737c8495e2daa3808c87836f NEO4J_TARBALL=neo4j-enterprise-4.4.12-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:20:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
# Fri, 14 Oct 2022 21:20:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:20:19 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Fri, 14 Oct 2022 21:20:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:20:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:20:41 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:20:41 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:20:42 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:20:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:20:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411b6cb0e944ff13c8e89f4a886c731ea8293c8f3dbc5d78ed1df2e6fbef5b9`  
		Last Modified: Thu, 06 Oct 2022 04:08:54 GMT  
		Size: 198.1 MB (198124981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ba558a79e0d400395a055d250ff767069bf9dd44bb6888298ada302a90e54`  
		Last Modified: Fri, 14 Oct 2022 21:22:54 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3b79c9113a9b467ce260487eeef01e8cbdf07589d7097cc702567b975398a0`  
		Last Modified: Fri, 14 Oct 2022 21:22:54 GMT  
		Size: 7.6 KB (7614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4142eb9018d23d23ca0266ccc7c7ca3dc13080f7883a0a70afaeda87b6313058`  
		Last Modified: Fri, 14 Oct 2022 21:23:06 GMT  
		Size: 230.0 MB (229993160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.12-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b06e0ccf7e63b4657ff2a923f11022f4beafeb743e8fbdd5961e583d07005cb4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.6 MB (454585249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a289397c97545617681b8c9968ec5b28c5ef288d3c2887f12062cbf342ab9a5e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:32:30 GMT
COPY dir:0dc06d70d42a32ae203bdf41d3806f1204b90ca101c4efe4662ba862f2c76b8a in /opt/java/openjdk 
# Fri, 14 Oct 2022 21:41:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f0eff8c70ec5666169803d3d29363b770cd767f5737c8495e2daa3808c87836f NEO4J_TARBALL=neo4j-enterprise-4.4.12-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 14 Oct 2022 21:41:11 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
# Fri, 14 Oct 2022 21:41:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 14 Oct 2022 21:41:14 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Fri, 14 Oct 2022 21:41:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Oct 2022 21:41:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Oct 2022 21:41:29 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Oct 2022 21:41:30 GMT
VOLUME [/data /logs]
# Fri, 14 Oct 2022 21:41:31 GMT
EXPOSE 7473 7474 7687
# Fri, 14 Oct 2022 21:41:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Oct 2022 21:41:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bfdcb0b9c92e9c3da0e6ca913cb8d3cf77c13d55a20c234730a5896afdec4a`  
		Last Modified: Thu, 06 Oct 2022 02:57:34 GMT  
		Size: 194.9 MB (194866592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfdbc40515d5ea11f90fdc78603767ed197ef8fa4d888f4c4026262ccc3be3f`  
		Last Modified: Fri, 14 Oct 2022 21:43:15 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf1f26f166c527f7e1d229ef3f0763ddc6ab845a1059da71d8b4e08a001c082`  
		Last Modified: Fri, 14 Oct 2022 21:43:15 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72a648573de11717d92f64374bdd6ff1337e319707fdd3e22d2628c2203c449`  
		Last Modified: Fri, 14 Oct 2022 21:43:30 GMT  
		Size: 229.6 MB (229642844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:7c481932f1ecd2bfa1c668a20e9a95d11faeb2e1efb41429ede705016101ccdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:5d5ced7f0e8689e7b811be472c1bf19e69cd589e945da70c0b967188a82a48f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334276637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40309d82fee848dc4169ac740f3ba37b9f82ebcace8796f2e7893efc2ec590c5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:56:40 GMT
COPY dir:09afbf947759009c57336c17f70cd71239c5d8b0170793151aec66483cdd0976 in /opt/java/openjdk 
# Fri, 21 Oct 2022 17:20:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 21 Oct 2022 17:20:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Fri, 21 Oct 2022 17:20:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 21 Oct 2022 17:20:22 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Fri, 21 Oct 2022 17:20:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Oct 2022 17:20:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 17:20:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 21 Oct 2022 17:20:36 GMT
VOLUME [/data /logs]
# Fri, 21 Oct 2022 17:20:37 GMT
EXPOSE 7473 7474 7687
# Fri, 21 Oct 2022 17:20:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 21 Oct 2022 17:20:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef3d95ee3a8969f154e4e82981119ffbe3fb6d2183d260566ed8ba03b8fc6f8`  
		Last Modified: Thu, 06 Oct 2022 04:12:33 GMT  
		Size: 192.1 MB (192137622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3babaea8053234a9b9f347886f7ca5e677120aac4830f9d9e4a27d4bfaef150`  
		Last Modified: Fri, 21 Oct 2022 17:21:40 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67363ff205d3facaf0ac86b4e0b51607850084d76a402fe5fd09bcb888e218d6`  
		Last Modified: Fri, 21 Oct 2022 17:21:40 GMT  
		Size: 7.6 KB (7631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab09fcd8a19d9615075947c863963e12b91a9e73f5b0cff814a1bccdca6161bc`  
		Last Modified: Fri, 21 Oct 2022 17:21:46 GMT  
		Size: 110.7 MB (110707422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:46070621652c1732552ce3e930c59d00c5f20a72388ceb001cbce61d47c9f848
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.3 MB (331339423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe863a6c8f78a5f998b60f7f7302c9842299f82672aebf2eb5d910b02e22b32`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:39:47 GMT
COPY dir:dc2bc1e50ab42c5231433386b6bc2a9cff04b310112464fb4909efc66be10627 in /opt/java/openjdk 
# Fri, 21 Oct 2022 17:44:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 21 Oct 2022 17:44:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Fri, 21 Oct 2022 17:44:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 21 Oct 2022 17:44:53 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Fri, 21 Oct 2022 17:45:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Oct 2022 17:45:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 17:45:10 GMT
WORKDIR /var/lib/neo4j
# Fri, 21 Oct 2022 17:45:11 GMT
VOLUME [/data /logs]
# Fri, 21 Oct 2022 17:45:12 GMT
EXPOSE 7473 7474 7687
# Fri, 21 Oct 2022 17:45:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 21 Oct 2022 17:45:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd853b0df38079bcf0a5945a7e8ed2935d92b2270210148614164b9ddd8b48b`  
		Last Modified: Thu, 06 Oct 2022 03:01:36 GMT  
		Size: 190.9 MB (190904238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73db62081413dcbb9d78d6ec1d4c0f05cc47732db74073a5f728b9454c916d2`  
		Last Modified: Fri, 21 Oct 2022 17:46:29 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0f686a061688747ffda1418dc7dfd0c598b3fa1e8961314498d95dad00589`  
		Last Modified: Fri, 21 Oct 2022 17:46:29 GMT  
		Size: 7.6 KB (7604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1ef5ade98f8a5b0e388c7ca3d630c6ad016c8375995967239534cf2349ba1b`  
		Last Modified: Fri, 21 Oct 2022 17:46:37 GMT  
		Size: 110.4 MB (110359348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:7c481932f1ecd2bfa1c668a20e9a95d11faeb2e1efb41429ede705016101ccdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:5d5ced7f0e8689e7b811be472c1bf19e69cd589e945da70c0b967188a82a48f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334276637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40309d82fee848dc4169ac740f3ba37b9f82ebcace8796f2e7893efc2ec590c5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:56:40 GMT
COPY dir:09afbf947759009c57336c17f70cd71239c5d8b0170793151aec66483cdd0976 in /opt/java/openjdk 
# Fri, 21 Oct 2022 17:20:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 21 Oct 2022 17:20:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Fri, 21 Oct 2022 17:20:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 21 Oct 2022 17:20:22 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Fri, 21 Oct 2022 17:20:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Oct 2022 17:20:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 17:20:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 21 Oct 2022 17:20:36 GMT
VOLUME [/data /logs]
# Fri, 21 Oct 2022 17:20:37 GMT
EXPOSE 7473 7474 7687
# Fri, 21 Oct 2022 17:20:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 21 Oct 2022 17:20:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef3d95ee3a8969f154e4e82981119ffbe3fb6d2183d260566ed8ba03b8fc6f8`  
		Last Modified: Thu, 06 Oct 2022 04:12:33 GMT  
		Size: 192.1 MB (192137622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3babaea8053234a9b9f347886f7ca5e677120aac4830f9d9e4a27d4bfaef150`  
		Last Modified: Fri, 21 Oct 2022 17:21:40 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67363ff205d3facaf0ac86b4e0b51607850084d76a402fe5fd09bcb888e218d6`  
		Last Modified: Fri, 21 Oct 2022 17:21:40 GMT  
		Size: 7.6 KB (7631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab09fcd8a19d9615075947c863963e12b91a9e73f5b0cff814a1bccdca6161bc`  
		Last Modified: Fri, 21 Oct 2022 17:21:46 GMT  
		Size: 110.7 MB (110707422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:46070621652c1732552ce3e930c59d00c5f20a72388ceb001cbce61d47c9f848
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.3 MB (331339423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe863a6c8f78a5f998b60f7f7302c9842299f82672aebf2eb5d910b02e22b32`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:39:47 GMT
COPY dir:dc2bc1e50ab42c5231433386b6bc2a9cff04b310112464fb4909efc66be10627 in /opt/java/openjdk 
# Fri, 21 Oct 2022 17:44:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 21 Oct 2022 17:44:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Fri, 21 Oct 2022 17:44:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 21 Oct 2022 17:44:53 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Fri, 21 Oct 2022 17:45:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Oct 2022 17:45:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 17:45:10 GMT
WORKDIR /var/lib/neo4j
# Fri, 21 Oct 2022 17:45:11 GMT
VOLUME [/data /logs]
# Fri, 21 Oct 2022 17:45:12 GMT
EXPOSE 7473 7474 7687
# Fri, 21 Oct 2022 17:45:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 21 Oct 2022 17:45:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd853b0df38079bcf0a5945a7e8ed2935d92b2270210148614164b9ddd8b48b`  
		Last Modified: Thu, 06 Oct 2022 03:01:36 GMT  
		Size: 190.9 MB (190904238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73db62081413dcbb9d78d6ec1d4c0f05cc47732db74073a5f728b9454c916d2`  
		Last Modified: Fri, 21 Oct 2022 17:46:29 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0f686a061688747ffda1418dc7dfd0c598b3fa1e8961314498d95dad00589`  
		Last Modified: Fri, 21 Oct 2022 17:46:29 GMT  
		Size: 7.6 KB (7604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1ef5ade98f8a5b0e388c7ca3d630c6ad016c8375995967239534cf2349ba1b`  
		Last Modified: Fri, 21 Oct 2022 17:46:37 GMT  
		Size: 110.4 MB (110359348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:cf537157f71df4c42870b5f0bb3ac4eca34874504488fa976bf2bfa7b8602057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8a3da6b9b6ad1f67a28525b26eb8fcaf91d7d2b799dade407d1f837a0c31edb8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.9 MB (429863450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98330a56fbcba9e3988991ab090d570f19144c6ad9264b9dfb13b15b524c760`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:56:40 GMT
COPY dir:09afbf947759009c57336c17f70cd71239c5d8b0170793151aec66483cdd0976 in /opt/java/openjdk 
# Fri, 21 Oct 2022 17:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 21 Oct 2022 17:20:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Fri, 21 Oct 2022 17:20:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 21 Oct 2022 17:20:42 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Fri, 21 Oct 2022 17:21:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Oct 2022 17:21:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 17:21:05 GMT
WORKDIR /var/lib/neo4j
# Fri, 21 Oct 2022 17:21:05 GMT
VOLUME [/data /logs]
# Fri, 21 Oct 2022 17:21:05 GMT
EXPOSE 7473 7474 7687
# Fri, 21 Oct 2022 17:21:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 21 Oct 2022 17:21:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef3d95ee3a8969f154e4e82981119ffbe3fb6d2183d260566ed8ba03b8fc6f8`  
		Last Modified: Thu, 06 Oct 2022 04:12:33 GMT  
		Size: 192.1 MB (192137622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2292f5e8da65674ddbb822a38c3af87ec6e3f41825fc5a3b9709610abf74996b`  
		Last Modified: Fri, 21 Oct 2022 17:22:05 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689624bf02af9c38a0df4e4f5661fc8a6dec39394e5f23c2cdf9b36187d7ba8b`  
		Last Modified: Fri, 21 Oct 2022 17:22:06 GMT  
		Size: 7.6 KB (7631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2b253976aad4e6521f0231a9b6c86e59b7d26535c2cee96d7767be1512cd26`  
		Last Modified: Fri, 21 Oct 2022 17:22:16 GMT  
		Size: 206.3 MB (206294235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:be4f79db3420332606dcd1115f34f6b546a712be7ab1d610adefc23afb042eab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.9 MB (426924214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffd857c506e44aa81b48bddac18e88273e8dc69fb52ad55f93002a9d162e103`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:39:47 GMT
COPY dir:dc2bc1e50ab42c5231433386b6bc2a9cff04b310112464fb4909efc66be10627 in /opt/java/openjdk 
# Fri, 21 Oct 2022 17:45:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 21 Oct 2022 17:45:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Fri, 21 Oct 2022 17:45:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 21 Oct 2022 17:45:26 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Fri, 21 Oct 2022 17:45:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Oct 2022 17:45:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 17:45:40 GMT
WORKDIR /var/lib/neo4j
# Fri, 21 Oct 2022 17:45:41 GMT
VOLUME [/data /logs]
# Fri, 21 Oct 2022 17:45:42 GMT
EXPOSE 7473 7474 7687
# Fri, 21 Oct 2022 17:45:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 21 Oct 2022 17:45:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd853b0df38079bcf0a5945a7e8ed2935d92b2270210148614164b9ddd8b48b`  
		Last Modified: Thu, 06 Oct 2022 03:01:36 GMT  
		Size: 190.9 MB (190904238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b7b1db26005ebd580580c7e752caa00a2ef7dfb3f4876fb3ac49834270b8aa`  
		Last Modified: Fri, 21 Oct 2022 17:47:01 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98b504bb32f867520353837710ae6d57bcb5b831f10794e188d1c57cd6fd835`  
		Last Modified: Fri, 21 Oct 2022 17:47:00 GMT  
		Size: 7.6 KB (7604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f0a19e1aed201a0aa40acd78f112a87b5dc0378b21c18da269c4e85e05d0ee`  
		Last Modified: Fri, 21 Oct 2022 17:47:14 GMT  
		Size: 205.9 MB (205944139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.1.0`

```console
$ docker pull neo4j@sha256:7c481932f1ecd2bfa1c668a20e9a95d11faeb2e1efb41429ede705016101ccdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.1.0` - linux; amd64

```console
$ docker pull neo4j@sha256:5d5ced7f0e8689e7b811be472c1bf19e69cd589e945da70c0b967188a82a48f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334276637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40309d82fee848dc4169ac740f3ba37b9f82ebcace8796f2e7893efc2ec590c5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:56:40 GMT
COPY dir:09afbf947759009c57336c17f70cd71239c5d8b0170793151aec66483cdd0976 in /opt/java/openjdk 
# Fri, 21 Oct 2022 17:20:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 21 Oct 2022 17:20:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Fri, 21 Oct 2022 17:20:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 21 Oct 2022 17:20:22 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Fri, 21 Oct 2022 17:20:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Oct 2022 17:20:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 17:20:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 21 Oct 2022 17:20:36 GMT
VOLUME [/data /logs]
# Fri, 21 Oct 2022 17:20:37 GMT
EXPOSE 7473 7474 7687
# Fri, 21 Oct 2022 17:20:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 21 Oct 2022 17:20:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef3d95ee3a8969f154e4e82981119ffbe3fb6d2183d260566ed8ba03b8fc6f8`  
		Last Modified: Thu, 06 Oct 2022 04:12:33 GMT  
		Size: 192.1 MB (192137622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3babaea8053234a9b9f347886f7ca5e677120aac4830f9d9e4a27d4bfaef150`  
		Last Modified: Fri, 21 Oct 2022 17:21:40 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67363ff205d3facaf0ac86b4e0b51607850084d76a402fe5fd09bcb888e218d6`  
		Last Modified: Fri, 21 Oct 2022 17:21:40 GMT  
		Size: 7.6 KB (7631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab09fcd8a19d9615075947c863963e12b91a9e73f5b0cff814a1bccdca6161bc`  
		Last Modified: Fri, 21 Oct 2022 17:21:46 GMT  
		Size: 110.7 MB (110707422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.1.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:46070621652c1732552ce3e930c59d00c5f20a72388ceb001cbce61d47c9f848
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.3 MB (331339423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe863a6c8f78a5f998b60f7f7302c9842299f82672aebf2eb5d910b02e22b32`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:39:47 GMT
COPY dir:dc2bc1e50ab42c5231433386b6bc2a9cff04b310112464fb4909efc66be10627 in /opt/java/openjdk 
# Fri, 21 Oct 2022 17:44:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 21 Oct 2022 17:44:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Fri, 21 Oct 2022 17:44:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 21 Oct 2022 17:44:53 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Fri, 21 Oct 2022 17:45:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Oct 2022 17:45:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 17:45:10 GMT
WORKDIR /var/lib/neo4j
# Fri, 21 Oct 2022 17:45:11 GMT
VOLUME [/data /logs]
# Fri, 21 Oct 2022 17:45:12 GMT
EXPOSE 7473 7474 7687
# Fri, 21 Oct 2022 17:45:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 21 Oct 2022 17:45:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd853b0df38079bcf0a5945a7e8ed2935d92b2270210148614164b9ddd8b48b`  
		Last Modified: Thu, 06 Oct 2022 03:01:36 GMT  
		Size: 190.9 MB (190904238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73db62081413dcbb9d78d6ec1d4c0f05cc47732db74073a5f728b9454c916d2`  
		Last Modified: Fri, 21 Oct 2022 17:46:29 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0f686a061688747ffda1418dc7dfd0c598b3fa1e8961314498d95dad00589`  
		Last Modified: Fri, 21 Oct 2022 17:46:29 GMT  
		Size: 7.6 KB (7604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1ef5ade98f8a5b0e388c7ca3d630c6ad016c8375995967239534cf2349ba1b`  
		Last Modified: Fri, 21 Oct 2022 17:46:37 GMT  
		Size: 110.4 MB (110359348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.1.0-community`

```console
$ docker pull neo4j@sha256:7c481932f1ecd2bfa1c668a20e9a95d11faeb2e1efb41429ede705016101ccdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.1.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:5d5ced7f0e8689e7b811be472c1bf19e69cd589e945da70c0b967188a82a48f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334276637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40309d82fee848dc4169ac740f3ba37b9f82ebcace8796f2e7893efc2ec590c5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:56:40 GMT
COPY dir:09afbf947759009c57336c17f70cd71239c5d8b0170793151aec66483cdd0976 in /opt/java/openjdk 
# Fri, 21 Oct 2022 17:20:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 21 Oct 2022 17:20:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Fri, 21 Oct 2022 17:20:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 21 Oct 2022 17:20:22 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Fri, 21 Oct 2022 17:20:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Oct 2022 17:20:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 17:20:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 21 Oct 2022 17:20:36 GMT
VOLUME [/data /logs]
# Fri, 21 Oct 2022 17:20:37 GMT
EXPOSE 7473 7474 7687
# Fri, 21 Oct 2022 17:20:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 21 Oct 2022 17:20:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef3d95ee3a8969f154e4e82981119ffbe3fb6d2183d260566ed8ba03b8fc6f8`  
		Last Modified: Thu, 06 Oct 2022 04:12:33 GMT  
		Size: 192.1 MB (192137622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3babaea8053234a9b9f347886f7ca5e677120aac4830f9d9e4a27d4bfaef150`  
		Last Modified: Fri, 21 Oct 2022 17:21:40 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67363ff205d3facaf0ac86b4e0b51607850084d76a402fe5fd09bcb888e218d6`  
		Last Modified: Fri, 21 Oct 2022 17:21:40 GMT  
		Size: 7.6 KB (7631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab09fcd8a19d9615075947c863963e12b91a9e73f5b0cff814a1bccdca6161bc`  
		Last Modified: Fri, 21 Oct 2022 17:21:46 GMT  
		Size: 110.7 MB (110707422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.1.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:46070621652c1732552ce3e930c59d00c5f20a72388ceb001cbce61d47c9f848
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.3 MB (331339423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe863a6c8f78a5f998b60f7f7302c9842299f82672aebf2eb5d910b02e22b32`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:39:47 GMT
COPY dir:dc2bc1e50ab42c5231433386b6bc2a9cff04b310112464fb4909efc66be10627 in /opt/java/openjdk 
# Fri, 21 Oct 2022 17:44:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 21 Oct 2022 17:44:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Fri, 21 Oct 2022 17:44:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 21 Oct 2022 17:44:53 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Fri, 21 Oct 2022 17:45:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Oct 2022 17:45:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 17:45:10 GMT
WORKDIR /var/lib/neo4j
# Fri, 21 Oct 2022 17:45:11 GMT
VOLUME [/data /logs]
# Fri, 21 Oct 2022 17:45:12 GMT
EXPOSE 7473 7474 7687
# Fri, 21 Oct 2022 17:45:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 21 Oct 2022 17:45:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd853b0df38079bcf0a5945a7e8ed2935d92b2270210148614164b9ddd8b48b`  
		Last Modified: Thu, 06 Oct 2022 03:01:36 GMT  
		Size: 190.9 MB (190904238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73db62081413dcbb9d78d6ec1d4c0f05cc47732db74073a5f728b9454c916d2`  
		Last Modified: Fri, 21 Oct 2022 17:46:29 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0f686a061688747ffda1418dc7dfd0c598b3fa1e8961314498d95dad00589`  
		Last Modified: Fri, 21 Oct 2022 17:46:29 GMT  
		Size: 7.6 KB (7604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1ef5ade98f8a5b0e388c7ca3d630c6ad016c8375995967239534cf2349ba1b`  
		Last Modified: Fri, 21 Oct 2022 17:46:37 GMT  
		Size: 110.4 MB (110359348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.1.0-enterprise`

```console
$ docker pull neo4j@sha256:cf537157f71df4c42870b5f0bb3ac4eca34874504488fa976bf2bfa7b8602057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.1.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8a3da6b9b6ad1f67a28525b26eb8fcaf91d7d2b799dade407d1f837a0c31edb8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.9 MB (429863450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98330a56fbcba9e3988991ab090d570f19144c6ad9264b9dfb13b15b524c760`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:56:40 GMT
COPY dir:09afbf947759009c57336c17f70cd71239c5d8b0170793151aec66483cdd0976 in /opt/java/openjdk 
# Fri, 21 Oct 2022 17:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 21 Oct 2022 17:20:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Fri, 21 Oct 2022 17:20:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 21 Oct 2022 17:20:42 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Fri, 21 Oct 2022 17:21:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Oct 2022 17:21:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 17:21:05 GMT
WORKDIR /var/lib/neo4j
# Fri, 21 Oct 2022 17:21:05 GMT
VOLUME [/data /logs]
# Fri, 21 Oct 2022 17:21:05 GMT
EXPOSE 7473 7474 7687
# Fri, 21 Oct 2022 17:21:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 21 Oct 2022 17:21:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef3d95ee3a8969f154e4e82981119ffbe3fb6d2183d260566ed8ba03b8fc6f8`  
		Last Modified: Thu, 06 Oct 2022 04:12:33 GMT  
		Size: 192.1 MB (192137622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2292f5e8da65674ddbb822a38c3af87ec6e3f41825fc5a3b9709610abf74996b`  
		Last Modified: Fri, 21 Oct 2022 17:22:05 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689624bf02af9c38a0df4e4f5661fc8a6dec39394e5f23c2cdf9b36187d7ba8b`  
		Last Modified: Fri, 21 Oct 2022 17:22:06 GMT  
		Size: 7.6 KB (7631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2b253976aad4e6521f0231a9b6c86e59b7d26535c2cee96d7767be1512cd26`  
		Last Modified: Fri, 21 Oct 2022 17:22:16 GMT  
		Size: 206.3 MB (206294235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.1.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:be4f79db3420332606dcd1115f34f6b546a712be7ab1d610adefc23afb042eab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.9 MB (426924214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffd857c506e44aa81b48bddac18e88273e8dc69fb52ad55f93002a9d162e103`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:39:47 GMT
COPY dir:dc2bc1e50ab42c5231433386b6bc2a9cff04b310112464fb4909efc66be10627 in /opt/java/openjdk 
# Fri, 21 Oct 2022 17:45:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 21 Oct 2022 17:45:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Fri, 21 Oct 2022 17:45:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 21 Oct 2022 17:45:26 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Fri, 21 Oct 2022 17:45:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Oct 2022 17:45:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 17:45:40 GMT
WORKDIR /var/lib/neo4j
# Fri, 21 Oct 2022 17:45:41 GMT
VOLUME [/data /logs]
# Fri, 21 Oct 2022 17:45:42 GMT
EXPOSE 7473 7474 7687
# Fri, 21 Oct 2022 17:45:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 21 Oct 2022 17:45:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd853b0df38079bcf0a5945a7e8ed2935d92b2270210148614164b9ddd8b48b`  
		Last Modified: Thu, 06 Oct 2022 03:01:36 GMT  
		Size: 190.9 MB (190904238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b7b1db26005ebd580580c7e752caa00a2ef7dfb3f4876fb3ac49834270b8aa`  
		Last Modified: Fri, 21 Oct 2022 17:47:01 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98b504bb32f867520353837710ae6d57bcb5b831f10794e188d1c57cd6fd835`  
		Last Modified: Fri, 21 Oct 2022 17:47:00 GMT  
		Size: 7.6 KB (7604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f0a19e1aed201a0aa40acd78f112a87b5dc0378b21c18da269c4e85e05d0ee`  
		Last Modified: Fri, 21 Oct 2022 17:47:14 GMT  
		Size: 205.9 MB (205944139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:7c481932f1ecd2bfa1c668a20e9a95d11faeb2e1efb41429ede705016101ccdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:5d5ced7f0e8689e7b811be472c1bf19e69cd589e945da70c0b967188a82a48f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334276637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40309d82fee848dc4169ac740f3ba37b9f82ebcace8796f2e7893efc2ec590c5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:56:40 GMT
COPY dir:09afbf947759009c57336c17f70cd71239c5d8b0170793151aec66483cdd0976 in /opt/java/openjdk 
# Fri, 21 Oct 2022 17:20:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 21 Oct 2022 17:20:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Fri, 21 Oct 2022 17:20:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 21 Oct 2022 17:20:22 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Fri, 21 Oct 2022 17:20:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Oct 2022 17:20:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 17:20:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 21 Oct 2022 17:20:36 GMT
VOLUME [/data /logs]
# Fri, 21 Oct 2022 17:20:37 GMT
EXPOSE 7473 7474 7687
# Fri, 21 Oct 2022 17:20:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 21 Oct 2022 17:20:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef3d95ee3a8969f154e4e82981119ffbe3fb6d2183d260566ed8ba03b8fc6f8`  
		Last Modified: Thu, 06 Oct 2022 04:12:33 GMT  
		Size: 192.1 MB (192137622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3babaea8053234a9b9f347886f7ca5e677120aac4830f9d9e4a27d4bfaef150`  
		Last Modified: Fri, 21 Oct 2022 17:21:40 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67363ff205d3facaf0ac86b4e0b51607850084d76a402fe5fd09bcb888e218d6`  
		Last Modified: Fri, 21 Oct 2022 17:21:40 GMT  
		Size: 7.6 KB (7631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab09fcd8a19d9615075947c863963e12b91a9e73f5b0cff814a1bccdca6161bc`  
		Last Modified: Fri, 21 Oct 2022 17:21:46 GMT  
		Size: 110.7 MB (110707422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:46070621652c1732552ce3e930c59d00c5f20a72388ceb001cbce61d47c9f848
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.3 MB (331339423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe863a6c8f78a5f998b60f7f7302c9842299f82672aebf2eb5d910b02e22b32`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:39:47 GMT
COPY dir:dc2bc1e50ab42c5231433386b6bc2a9cff04b310112464fb4909efc66be10627 in /opt/java/openjdk 
# Fri, 21 Oct 2022 17:44:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 21 Oct 2022 17:44:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Fri, 21 Oct 2022 17:44:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 21 Oct 2022 17:44:53 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Fri, 21 Oct 2022 17:45:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Oct 2022 17:45:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 17:45:10 GMT
WORKDIR /var/lib/neo4j
# Fri, 21 Oct 2022 17:45:11 GMT
VOLUME [/data /logs]
# Fri, 21 Oct 2022 17:45:12 GMT
EXPOSE 7473 7474 7687
# Fri, 21 Oct 2022 17:45:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 21 Oct 2022 17:45:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd853b0df38079bcf0a5945a7e8ed2935d92b2270210148614164b9ddd8b48b`  
		Last Modified: Thu, 06 Oct 2022 03:01:36 GMT  
		Size: 190.9 MB (190904238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73db62081413dcbb9d78d6ec1d4c0f05cc47732db74073a5f728b9454c916d2`  
		Last Modified: Fri, 21 Oct 2022 17:46:29 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0f686a061688747ffda1418dc7dfd0c598b3fa1e8961314498d95dad00589`  
		Last Modified: Fri, 21 Oct 2022 17:46:29 GMT  
		Size: 7.6 KB (7604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1ef5ade98f8a5b0e388c7ca3d630c6ad016c8375995967239534cf2349ba1b`  
		Last Modified: Fri, 21 Oct 2022 17:46:37 GMT  
		Size: 110.4 MB (110359348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:cf537157f71df4c42870b5f0bb3ac4eca34874504488fa976bf2bfa7b8602057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8a3da6b9b6ad1f67a28525b26eb8fcaf91d7d2b799dade407d1f837a0c31edb8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.9 MB (429863450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98330a56fbcba9e3988991ab090d570f19144c6ad9264b9dfb13b15b524c760`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:56:40 GMT
COPY dir:09afbf947759009c57336c17f70cd71239c5d8b0170793151aec66483cdd0976 in /opt/java/openjdk 
# Fri, 21 Oct 2022 17:20:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 21 Oct 2022 17:20:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Fri, 21 Oct 2022 17:20:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 21 Oct 2022 17:20:42 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Fri, 21 Oct 2022 17:21:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Oct 2022 17:21:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 17:21:05 GMT
WORKDIR /var/lib/neo4j
# Fri, 21 Oct 2022 17:21:05 GMT
VOLUME [/data /logs]
# Fri, 21 Oct 2022 17:21:05 GMT
EXPOSE 7473 7474 7687
# Fri, 21 Oct 2022 17:21:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 21 Oct 2022 17:21:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef3d95ee3a8969f154e4e82981119ffbe3fb6d2183d260566ed8ba03b8fc6f8`  
		Last Modified: Thu, 06 Oct 2022 04:12:33 GMT  
		Size: 192.1 MB (192137622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2292f5e8da65674ddbb822a38c3af87ec6e3f41825fc5a3b9709610abf74996b`  
		Last Modified: Fri, 21 Oct 2022 17:22:05 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689624bf02af9c38a0df4e4f5661fc8a6dec39394e5f23c2cdf9b36187d7ba8b`  
		Last Modified: Fri, 21 Oct 2022 17:22:06 GMT  
		Size: 7.6 KB (7631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2b253976aad4e6521f0231a9b6c86e59b7d26535c2cee96d7767be1512cd26`  
		Last Modified: Fri, 21 Oct 2022 17:22:16 GMT  
		Size: 206.3 MB (206294235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:be4f79db3420332606dcd1115f34f6b546a712be7ab1d610adefc23afb042eab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.9 MB (426924214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffd857c506e44aa81b48bddac18e88273e8dc69fb52ad55f93002a9d162e103`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:39:47 GMT
COPY dir:dc2bc1e50ab42c5231433386b6bc2a9cff04b310112464fb4909efc66be10627 in /opt/java/openjdk 
# Fri, 21 Oct 2022 17:45:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 21 Oct 2022 17:45:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Fri, 21 Oct 2022 17:45:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 21 Oct 2022 17:45:26 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Fri, 21 Oct 2022 17:45:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Oct 2022 17:45:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 17:45:40 GMT
WORKDIR /var/lib/neo4j
# Fri, 21 Oct 2022 17:45:41 GMT
VOLUME [/data /logs]
# Fri, 21 Oct 2022 17:45:42 GMT
EXPOSE 7473 7474 7687
# Fri, 21 Oct 2022 17:45:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 21 Oct 2022 17:45:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd853b0df38079bcf0a5945a7e8ed2935d92b2270210148614164b9ddd8b48b`  
		Last Modified: Thu, 06 Oct 2022 03:01:36 GMT  
		Size: 190.9 MB (190904238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b7b1db26005ebd580580c7e752caa00a2ef7dfb3f4876fb3ac49834270b8aa`  
		Last Modified: Fri, 21 Oct 2022 17:47:01 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98b504bb32f867520353837710ae6d57bcb5b831f10794e188d1c57cd6fd835`  
		Last Modified: Fri, 21 Oct 2022 17:47:00 GMT  
		Size: 7.6 KB (7604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f0a19e1aed201a0aa40acd78f112a87b5dc0378b21c18da269c4e85e05d0ee`  
		Last Modified: Fri, 21 Oct 2022 17:47:14 GMT  
		Size: 205.9 MB (205944139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:7c481932f1ecd2bfa1c668a20e9a95d11faeb2e1efb41429ede705016101ccdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:5d5ced7f0e8689e7b811be472c1bf19e69cd589e945da70c0b967188a82a48f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334276637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40309d82fee848dc4169ac740f3ba37b9f82ebcace8796f2e7893efc2ec590c5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:56:40 GMT
COPY dir:09afbf947759009c57336c17f70cd71239c5d8b0170793151aec66483cdd0976 in /opt/java/openjdk 
# Fri, 21 Oct 2022 17:20:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 21 Oct 2022 17:20:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Fri, 21 Oct 2022 17:20:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 21 Oct 2022 17:20:22 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Fri, 21 Oct 2022 17:20:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Oct 2022 17:20:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 17:20:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 21 Oct 2022 17:20:36 GMT
VOLUME [/data /logs]
# Fri, 21 Oct 2022 17:20:37 GMT
EXPOSE 7473 7474 7687
# Fri, 21 Oct 2022 17:20:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 21 Oct 2022 17:20:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef3d95ee3a8969f154e4e82981119ffbe3fb6d2183d260566ed8ba03b8fc6f8`  
		Last Modified: Thu, 06 Oct 2022 04:12:33 GMT  
		Size: 192.1 MB (192137622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3babaea8053234a9b9f347886f7ca5e677120aac4830f9d9e4a27d4bfaef150`  
		Last Modified: Fri, 21 Oct 2022 17:21:40 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67363ff205d3facaf0ac86b4e0b51607850084d76a402fe5fd09bcb888e218d6`  
		Last Modified: Fri, 21 Oct 2022 17:21:40 GMT  
		Size: 7.6 KB (7631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab09fcd8a19d9615075947c863963e12b91a9e73f5b0cff814a1bccdca6161bc`  
		Last Modified: Fri, 21 Oct 2022 17:21:46 GMT  
		Size: 110.7 MB (110707422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:46070621652c1732552ce3e930c59d00c5f20a72388ceb001cbce61d47c9f848
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.3 MB (331339423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe863a6c8f78a5f998b60f7f7302c9842299f82672aebf2eb5d910b02e22b32`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:39:47 GMT
COPY dir:dc2bc1e50ab42c5231433386b6bc2a9cff04b310112464fb4909efc66be10627 in /opt/java/openjdk 
# Fri, 21 Oct 2022 17:44:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 21 Oct 2022 17:44:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Fri, 21 Oct 2022 17:44:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 21 Oct 2022 17:44:53 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Fri, 21 Oct 2022 17:45:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 21 Oct 2022 17:45:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Oct 2022 17:45:10 GMT
WORKDIR /var/lib/neo4j
# Fri, 21 Oct 2022 17:45:11 GMT
VOLUME [/data /logs]
# Fri, 21 Oct 2022 17:45:12 GMT
EXPOSE 7473 7474 7687
# Fri, 21 Oct 2022 17:45:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 21 Oct 2022 17:45:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd853b0df38079bcf0a5945a7e8ed2935d92b2270210148614164b9ddd8b48b`  
		Last Modified: Thu, 06 Oct 2022 03:01:36 GMT  
		Size: 190.9 MB (190904238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73db62081413dcbb9d78d6ec1d4c0f05cc47732db74073a5f728b9454c916d2`  
		Last Modified: Fri, 21 Oct 2022 17:46:29 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0f686a061688747ffda1418dc7dfd0c598b3fa1e8961314498d95dad00589`  
		Last Modified: Fri, 21 Oct 2022 17:46:29 GMT  
		Size: 7.6 KB (7604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1ef5ade98f8a5b0e388c7ca3d630c6ad016c8375995967239534cf2349ba1b`  
		Last Modified: Fri, 21 Oct 2022 17:46:37 GMT  
		Size: 110.4 MB (110359348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
