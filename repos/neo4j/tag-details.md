<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.3`](#neo4j43)
-	[`neo4j:4.3-community`](#neo4j43-community)
-	[`neo4j:4.3-enterprise`](#neo4j43-enterprise)
-	[`neo4j:4.3.20`](#neo4j4320)
-	[`neo4j:4.3.20-community`](#neo4j4320-community)
-	[`neo4j:4.3.20-enterprise`](#neo4j4320-enterprise)
-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.13`](#neo4j4413)
-	[`neo4j:4.4.13-community`](#neo4j4413-community)
-	[`neo4j:4.4.13-enterprise`](#neo4j4413-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5.1`](#neo4j51)
-	[`neo4j:5.1-enterprise`](#neo4j51-enterprise)
-	[`neo4j:5.1.0`](#neo4j510)
-	[`neo4j:5.1.0-community`](#neo4j510-community)
-	[`neo4j:5.1.0-enterprise`](#neo4j510-enterprise)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:latest`](#neo4jlatest)

## `neo4j:4.3`

```console
$ docker pull neo4j@sha256:fee8b9b0f3ab31de53750a3d6dcaae551b6807d58ac60b0b3cb798873119c337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3` - linux; amd64

```console
$ docker pull neo4j@sha256:9baf075aaaeeafe1ded9bdbab40148610a0e53cec81aca1923e3e2cf214433a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.2 MB (360217041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8cc320674c8a4571f22723fbb5a8cee8085db6fcc4a3c49390fb15c8bb15da`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Mon, 07 Nov 2022 19:25:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1a006ae166e1fc3f51b0a846728979f01c5269334f78ea6381683ef44a3d70b3 NEO4J_TARBALL=neo4j-community-4.3.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 19:25:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.20-unix.tar.gz
# Mon, 07 Nov 2022 19:25:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 19:25:35 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Mon, 07 Nov 2022 19:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 19:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 19:25:52 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 19:25:52 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 19:25:52 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 19:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 19:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb308a8217347b6d723bff06f41605d1f28ad13d6900615736bce56e2bddc150`  
		Last Modified: Mon, 07 Nov 2022 19:27:42 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ca23000167bac40ad543e86fb6f97adc5ee34183e6d63657b8fd571587e7d4`  
		Last Modified: Mon, 07 Nov 2022 19:27:42 GMT  
		Size: 7.6 KB (7623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60118bf597968daff49197cadde156d7f25bfcd44d5bd005677c2cc29c83de74`  
		Last Modified: Mon, 07 Nov 2022 19:27:49 GMT  
		Size: 130.3 MB (130329674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3-community`

```console
$ docker pull neo4j@sha256:fee8b9b0f3ab31de53750a3d6dcaae551b6807d58ac60b0b3cb798873119c337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3-community` - linux; amd64

```console
$ docker pull neo4j@sha256:9baf075aaaeeafe1ded9bdbab40148610a0e53cec81aca1923e3e2cf214433a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.2 MB (360217041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8cc320674c8a4571f22723fbb5a8cee8085db6fcc4a3c49390fb15c8bb15da`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Mon, 07 Nov 2022 19:25:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1a006ae166e1fc3f51b0a846728979f01c5269334f78ea6381683ef44a3d70b3 NEO4J_TARBALL=neo4j-community-4.3.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 19:25:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.20-unix.tar.gz
# Mon, 07 Nov 2022 19:25:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 19:25:35 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Mon, 07 Nov 2022 19:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 19:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 19:25:52 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 19:25:52 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 19:25:52 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 19:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 19:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb308a8217347b6d723bff06f41605d1f28ad13d6900615736bce56e2bddc150`  
		Last Modified: Mon, 07 Nov 2022 19:27:42 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ca23000167bac40ad543e86fb6f97adc5ee34183e6d63657b8fd571587e7d4`  
		Last Modified: Mon, 07 Nov 2022 19:27:42 GMT  
		Size: 7.6 KB (7623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60118bf597968daff49197cadde156d7f25bfcd44d5bd005677c2cc29c83de74`  
		Last Modified: Mon, 07 Nov 2022 19:27:49 GMT  
		Size: 130.3 MB (130329674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3-enterprise`

```console
$ docker pull neo4j@sha256:a9ada1d37e9e3ebaca8952e2a87aad8940fd0816e8689ca319006f58c1a5f2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:0630aad4cfbde299afdf7669cdd2cfb99d4017b7751bb0373847897fef746196
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.7 MB (390687919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e69ff7dc53546e3bced8781c4053f4ac9439322759b5db0704169d7e8f51a24`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Mon, 07 Nov 2022 19:25:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3e53e774d810ea6c71642f4c233527e1b8a1aa2b916a166e67bf524934c5164d NEO4J_TARBALL=neo4j-enterprise-4.3.20-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 19:25:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.20-unix.tar.gz
# Mon, 07 Nov 2022 19:25:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 19:25:59 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Mon, 07 Nov 2022 19:26:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 19:26:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 19:26:18 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 19:26:18 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 19:26:18 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 19:26:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 19:26:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5eec5a8c463bf6b0b93f20ac78620d9bdcbc503d5d40ec2950d75a5ed642e2b`  
		Last Modified: Mon, 07 Nov 2022 19:28:04 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d900a51073f103a1ef91a454341d55a4a123c702cd4a1a353b971021b4fd71`  
		Last Modified: Mon, 07 Nov 2022 19:28:04 GMT  
		Size: 7.6 KB (7626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1d42b0e550468e935f2d5fd3e8b77304a61e53fe28d9a5290f60be41d42b58`  
		Last Modified: Mon, 07 Nov 2022 19:28:12 GMT  
		Size: 160.8 MB (160800554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.20`

```console
$ docker pull neo4j@sha256:fee8b9b0f3ab31de53750a3d6dcaae551b6807d58ac60b0b3cb798873119c337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.20` - linux; amd64

```console
$ docker pull neo4j@sha256:9baf075aaaeeafe1ded9bdbab40148610a0e53cec81aca1923e3e2cf214433a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.2 MB (360217041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8cc320674c8a4571f22723fbb5a8cee8085db6fcc4a3c49390fb15c8bb15da`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Mon, 07 Nov 2022 19:25:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1a006ae166e1fc3f51b0a846728979f01c5269334f78ea6381683ef44a3d70b3 NEO4J_TARBALL=neo4j-community-4.3.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 19:25:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.20-unix.tar.gz
# Mon, 07 Nov 2022 19:25:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 19:25:35 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Mon, 07 Nov 2022 19:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 19:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 19:25:52 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 19:25:52 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 19:25:52 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 19:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 19:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb308a8217347b6d723bff06f41605d1f28ad13d6900615736bce56e2bddc150`  
		Last Modified: Mon, 07 Nov 2022 19:27:42 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ca23000167bac40ad543e86fb6f97adc5ee34183e6d63657b8fd571587e7d4`  
		Last Modified: Mon, 07 Nov 2022 19:27:42 GMT  
		Size: 7.6 KB (7623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60118bf597968daff49197cadde156d7f25bfcd44d5bd005677c2cc29c83de74`  
		Last Modified: Mon, 07 Nov 2022 19:27:49 GMT  
		Size: 130.3 MB (130329674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.20-community`

```console
$ docker pull neo4j@sha256:fee8b9b0f3ab31de53750a3d6dcaae551b6807d58ac60b0b3cb798873119c337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.20-community` - linux; amd64

```console
$ docker pull neo4j@sha256:9baf075aaaeeafe1ded9bdbab40148610a0e53cec81aca1923e3e2cf214433a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.2 MB (360217041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8cc320674c8a4571f22723fbb5a8cee8085db6fcc4a3c49390fb15c8bb15da`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Mon, 07 Nov 2022 19:25:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1a006ae166e1fc3f51b0a846728979f01c5269334f78ea6381683ef44a3d70b3 NEO4J_TARBALL=neo4j-community-4.3.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 19:25:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.20-unix.tar.gz
# Mon, 07 Nov 2022 19:25:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 19:25:35 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Mon, 07 Nov 2022 19:25:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 19:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 19:25:52 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 19:25:52 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 19:25:52 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 19:25:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 19:25:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb308a8217347b6d723bff06f41605d1f28ad13d6900615736bce56e2bddc150`  
		Last Modified: Mon, 07 Nov 2022 19:27:42 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ca23000167bac40ad543e86fb6f97adc5ee34183e6d63657b8fd571587e7d4`  
		Last Modified: Mon, 07 Nov 2022 19:27:42 GMT  
		Size: 7.6 KB (7623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60118bf597968daff49197cadde156d7f25bfcd44d5bd005677c2cc29c83de74`  
		Last Modified: Mon, 07 Nov 2022 19:27:49 GMT  
		Size: 130.3 MB (130329674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.20-enterprise`

```console
$ docker pull neo4j@sha256:a9ada1d37e9e3ebaca8952e2a87aad8940fd0816e8689ca319006f58c1a5f2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.20-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:0630aad4cfbde299afdf7669cdd2cfb99d4017b7751bb0373847897fef746196
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.7 MB (390687919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e69ff7dc53546e3bced8781c4053f4ac9439322759b5db0704169d7e8f51a24`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Mon, 07 Nov 2022 19:25:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3e53e774d810ea6c71642f4c233527e1b8a1aa2b916a166e67bf524934c5164d NEO4J_TARBALL=neo4j-enterprise-4.3.20-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 19:25:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.20-unix.tar.gz
# Mon, 07 Nov 2022 19:25:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 19:25:59 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Mon, 07 Nov 2022 19:26:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 19:26:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 19:26:18 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 19:26:18 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 19:26:18 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 19:26:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 19:26:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5eec5a8c463bf6b0b93f20ac78620d9bdcbc503d5d40ec2950d75a5ed642e2b`  
		Last Modified: Mon, 07 Nov 2022 19:28:04 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d900a51073f103a1ef91a454341d55a4a123c702cd4a1a353b971021b4fd71`  
		Last Modified: Mon, 07 Nov 2022 19:28:04 GMT  
		Size: 7.6 KB (7626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1d42b0e550468e935f2d5fd3e8b77304a61e53fe28d9a5290f60be41d42b58`  
		Last Modified: Mon, 07 Nov 2022 19:28:12 GMT  
		Size: 160.8 MB (160800554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:101bdc97348fe9c2f357373c00ed409f362f250ec41fbe78a24d8e969ff08e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:a30733da33f58f933f90715597de35a5f2ab1f0a2e2152b2b68c4ba68b3c4ba5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.1 MB (365105179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df20d996599d98b762e2c0ad45151022e18be5121ad6fecbc8bf3b92ba23916`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Mon, 07 Nov 2022 19:24:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cf50b123f193bf438833ef769043bd472a284a6b4e9415a9985d7268f452d7e3 NEO4J_TARBALL=neo4j-community-4.4.13-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 19:24:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
# Mon, 07 Nov 2022 19:24:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 19:24:51 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Mon, 07 Nov 2022 19:25:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 19:25:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 19:25:10 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 19:25:10 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 19:25:10 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 19:25:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 19:25:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b765feaa97e554760b94f62b33239d92de60bfb2a9a60b2e88a95ae9d48b27`  
		Last Modified: Mon, 07 Nov 2022 19:26:58 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95da6ddf2628536accc2696951b7dcd72c27e276fd6ba2d1e33329042dc287cb`  
		Last Modified: Mon, 07 Nov 2022 19:26:58 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb245f163ab4925a34fcc5a99d5853fa31b506a261477ed3d0afa1ce92c0412`  
		Last Modified: Mon, 07 Nov 2022 19:27:06 GMT  
		Size: 135.2 MB (135217270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eb0cbeaeea818c9b951f23dcd5935e382d9593e661d5ddf3d6b222c7d1d39788
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360352207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be1d78efef2df0a425323d247554f36926860612b2096d5c792dbf6f36e4cd7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:12:49 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Mon, 07 Nov 2022 19:40:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cf50b123f193bf438833ef769043bd472a284a6b4e9415a9985d7268f452d7e3 NEO4J_TARBALL=neo4j-community-4.4.13-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 19:40:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
# Mon, 07 Nov 2022 19:40:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 19:40:35 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Mon, 07 Nov 2022 19:40:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 19:40:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 19:40:46 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 19:40:46 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 19:40:46 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 19:40:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 19:40:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb106e6b88c840d8bc916d39cbd7e76282f34fad97623abb4a385dbc33404ce`  
		Last Modified: Fri, 04 Nov 2022 23:23:35 GMT  
		Size: 195.2 MB (195201089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8d472e4af581173136f8930af6ec0379c895ae4f9055c5e789b70506fc50b9`  
		Last Modified: Mon, 07 Nov 2022 19:41:37 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3daada422a9710cc2eaf10cf278668d42a9bca8fff6d56bd51e29660622836d`  
		Last Modified: Mon, 07 Nov 2022 19:41:37 GMT  
		Size: 8.2 KB (8171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07db2bdf842dd18cc768758c09347f56998f9dad223c65e61c9eeee7b87b2c40`  
		Last Modified: Mon, 07 Nov 2022 19:41:43 GMT  
		Size: 135.1 MB (135075153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:101bdc97348fe9c2f357373c00ed409f362f250ec41fbe78a24d8e969ff08e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a30733da33f58f933f90715597de35a5f2ab1f0a2e2152b2b68c4ba68b3c4ba5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.1 MB (365105179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df20d996599d98b762e2c0ad45151022e18be5121ad6fecbc8bf3b92ba23916`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Mon, 07 Nov 2022 19:24:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cf50b123f193bf438833ef769043bd472a284a6b4e9415a9985d7268f452d7e3 NEO4J_TARBALL=neo4j-community-4.4.13-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 19:24:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
# Mon, 07 Nov 2022 19:24:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 19:24:51 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Mon, 07 Nov 2022 19:25:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 19:25:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 19:25:10 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 19:25:10 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 19:25:10 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 19:25:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 19:25:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b765feaa97e554760b94f62b33239d92de60bfb2a9a60b2e88a95ae9d48b27`  
		Last Modified: Mon, 07 Nov 2022 19:26:58 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95da6ddf2628536accc2696951b7dcd72c27e276fd6ba2d1e33329042dc287cb`  
		Last Modified: Mon, 07 Nov 2022 19:26:58 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb245f163ab4925a34fcc5a99d5853fa31b506a261477ed3d0afa1ce92c0412`  
		Last Modified: Mon, 07 Nov 2022 19:27:06 GMT  
		Size: 135.2 MB (135217270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eb0cbeaeea818c9b951f23dcd5935e382d9593e661d5ddf3d6b222c7d1d39788
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360352207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be1d78efef2df0a425323d247554f36926860612b2096d5c792dbf6f36e4cd7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:12:49 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Mon, 07 Nov 2022 19:40:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cf50b123f193bf438833ef769043bd472a284a6b4e9415a9985d7268f452d7e3 NEO4J_TARBALL=neo4j-community-4.4.13-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 19:40:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
# Mon, 07 Nov 2022 19:40:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 19:40:35 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Mon, 07 Nov 2022 19:40:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 19:40:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 19:40:46 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 19:40:46 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 19:40:46 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 19:40:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 19:40:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb106e6b88c840d8bc916d39cbd7e76282f34fad97623abb4a385dbc33404ce`  
		Last Modified: Fri, 04 Nov 2022 23:23:35 GMT  
		Size: 195.2 MB (195201089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8d472e4af581173136f8930af6ec0379c895ae4f9055c5e789b70506fc50b9`  
		Last Modified: Mon, 07 Nov 2022 19:41:37 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3daada422a9710cc2eaf10cf278668d42a9bca8fff6d56bd51e29660622836d`  
		Last Modified: Mon, 07 Nov 2022 19:41:37 GMT  
		Size: 8.2 KB (8171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07db2bdf842dd18cc768758c09347f56998f9dad223c65e61c9eeee7b87b2c40`  
		Last Modified: Mon, 07 Nov 2022 19:41:43 GMT  
		Size: 135.1 MB (135075153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:4d11099aa903febe5c7b1e6e5bcce24f4d852af993ba9d4e405de104ad3d25b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:51c57888494a4b29b9d276b2e25b07ff486cae25de578bcd118e9826484ffe5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.3 MB (460296432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b3fe022d0ecac26bc3c94ebc206b3ad7d3c2bc95992e464855753adab8ee6b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Mon, 07 Nov 2022 19:25:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f8ae7ee71fb1a7f6d5c549af2456ffa377623fbce3208194a2ee317f524d584 NEO4J_TARBALL=neo4j-enterprise-4.4.13-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 19:25:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.13-unix.tar.gz
# Mon, 07 Nov 2022 19:25:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.13-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 19:25:15 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Mon, 07 Nov 2022 19:25:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.13-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 19:25:30 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 19:25:30 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 19:25:30 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 19:25:31 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 19:25:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 19:25:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a58740ba1d754216b2a37aba19e4bafa6828a438f2946435e6708fb1c1ff047`  
		Last Modified: Mon, 07 Nov 2022 19:27:21 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7cef73c62a6d8fb73997cccaf981a0b6be7aeee85b619ee8d0de83524eb0f8`  
		Last Modified: Mon, 07 Nov 2022 19:27:21 GMT  
		Size: 8.2 KB (8169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4af22fab20d15fde1ab639378860bed58fcc885a6a7a0704b836eab1b0ac4dc`  
		Last Modified: Mon, 07 Nov 2022 19:27:32 GMT  
		Size: 230.4 MB (230408514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7bc1763d8eb7877201de31d0d8fb569542d0d09967e94338712236f6903bbf52
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.5 MB (455543517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750aa1d0d79e7233a4ca3a5d427d0927ae33f1de830f6fcd138e2f101995dd8a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:12:49 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Mon, 07 Nov 2022 19:40:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f8ae7ee71fb1a7f6d5c549af2456ffa377623fbce3208194a2ee317f524d584 NEO4J_TARBALL=neo4j-enterprise-4.4.13-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 19:40:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.13-unix.tar.gz
# Mon, 07 Nov 2022 19:40:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.13-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 19:40:51 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Mon, 07 Nov 2022 19:41:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.13-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 19:41:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 19:41:04 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 19:41:04 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 19:41:05 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 19:41:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 19:41:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb106e6b88c840d8bc916d39cbd7e76282f34fad97623abb4a385dbc33404ce`  
		Last Modified: Fri, 04 Nov 2022 23:23:35 GMT  
		Size: 195.2 MB (195201089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a4e3b7b1c1272b3c54b0d6f54a16cfc85e38aef8d0dd1f87245a5b3955e2c9`  
		Last Modified: Mon, 07 Nov 2022 19:41:59 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d465f6a2fdbccee0029634a170d505ad47432db1558945a4e817eefd9e36f9c2`  
		Last Modified: Mon, 07 Nov 2022 19:41:59 GMT  
		Size: 8.2 KB (8170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e729f0ff0f2e7e2d60f971ab0c6e57d5b498ff8c6716d71bc351cc25060fe9`  
		Last Modified: Mon, 07 Nov 2022 19:42:10 GMT  
		Size: 230.3 MB (230266460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.13`

```console
$ docker pull neo4j@sha256:101bdc97348fe9c2f357373c00ed409f362f250ec41fbe78a24d8e969ff08e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.13` - linux; amd64

```console
$ docker pull neo4j@sha256:a30733da33f58f933f90715597de35a5f2ab1f0a2e2152b2b68c4ba68b3c4ba5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.1 MB (365105179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df20d996599d98b762e2c0ad45151022e18be5121ad6fecbc8bf3b92ba23916`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Mon, 07 Nov 2022 19:24:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cf50b123f193bf438833ef769043bd472a284a6b4e9415a9985d7268f452d7e3 NEO4J_TARBALL=neo4j-community-4.4.13-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 19:24:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
# Mon, 07 Nov 2022 19:24:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 19:24:51 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Mon, 07 Nov 2022 19:25:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 19:25:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 19:25:10 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 19:25:10 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 19:25:10 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 19:25:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 19:25:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b765feaa97e554760b94f62b33239d92de60bfb2a9a60b2e88a95ae9d48b27`  
		Last Modified: Mon, 07 Nov 2022 19:26:58 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95da6ddf2628536accc2696951b7dcd72c27e276fd6ba2d1e33329042dc287cb`  
		Last Modified: Mon, 07 Nov 2022 19:26:58 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb245f163ab4925a34fcc5a99d5853fa31b506a261477ed3d0afa1ce92c0412`  
		Last Modified: Mon, 07 Nov 2022 19:27:06 GMT  
		Size: 135.2 MB (135217270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.13` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eb0cbeaeea818c9b951f23dcd5935e382d9593e661d5ddf3d6b222c7d1d39788
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360352207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be1d78efef2df0a425323d247554f36926860612b2096d5c792dbf6f36e4cd7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:12:49 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Mon, 07 Nov 2022 19:40:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cf50b123f193bf438833ef769043bd472a284a6b4e9415a9985d7268f452d7e3 NEO4J_TARBALL=neo4j-community-4.4.13-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 19:40:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
# Mon, 07 Nov 2022 19:40:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 19:40:35 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Mon, 07 Nov 2022 19:40:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 19:40:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 19:40:46 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 19:40:46 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 19:40:46 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 19:40:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 19:40:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb106e6b88c840d8bc916d39cbd7e76282f34fad97623abb4a385dbc33404ce`  
		Last Modified: Fri, 04 Nov 2022 23:23:35 GMT  
		Size: 195.2 MB (195201089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8d472e4af581173136f8930af6ec0379c895ae4f9055c5e789b70506fc50b9`  
		Last Modified: Mon, 07 Nov 2022 19:41:37 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3daada422a9710cc2eaf10cf278668d42a9bca8fff6d56bd51e29660622836d`  
		Last Modified: Mon, 07 Nov 2022 19:41:37 GMT  
		Size: 8.2 KB (8171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07db2bdf842dd18cc768758c09347f56998f9dad223c65e61c9eeee7b87b2c40`  
		Last Modified: Mon, 07 Nov 2022 19:41:43 GMT  
		Size: 135.1 MB (135075153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.13-community`

```console
$ docker pull neo4j@sha256:101bdc97348fe9c2f357373c00ed409f362f250ec41fbe78a24d8e969ff08e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.13-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a30733da33f58f933f90715597de35a5f2ab1f0a2e2152b2b68c4ba68b3c4ba5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.1 MB (365105179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df20d996599d98b762e2c0ad45151022e18be5121ad6fecbc8bf3b92ba23916`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Mon, 07 Nov 2022 19:24:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cf50b123f193bf438833ef769043bd472a284a6b4e9415a9985d7268f452d7e3 NEO4J_TARBALL=neo4j-community-4.4.13-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 19:24:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
# Mon, 07 Nov 2022 19:24:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 19:24:51 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Mon, 07 Nov 2022 19:25:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 19:25:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 19:25:10 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 19:25:10 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 19:25:10 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 19:25:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 19:25:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b765feaa97e554760b94f62b33239d92de60bfb2a9a60b2e88a95ae9d48b27`  
		Last Modified: Mon, 07 Nov 2022 19:26:58 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95da6ddf2628536accc2696951b7dcd72c27e276fd6ba2d1e33329042dc287cb`  
		Last Modified: Mon, 07 Nov 2022 19:26:58 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb245f163ab4925a34fcc5a99d5853fa31b506a261477ed3d0afa1ce92c0412`  
		Last Modified: Mon, 07 Nov 2022 19:27:06 GMT  
		Size: 135.2 MB (135217270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.13-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:eb0cbeaeea818c9b951f23dcd5935e382d9593e661d5ddf3d6b222c7d1d39788
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360352207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be1d78efef2df0a425323d247554f36926860612b2096d5c792dbf6f36e4cd7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:12:49 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Mon, 07 Nov 2022 19:40:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cf50b123f193bf438833ef769043bd472a284a6b4e9415a9985d7268f452d7e3 NEO4J_TARBALL=neo4j-community-4.4.13-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 19:40:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
# Mon, 07 Nov 2022 19:40:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 19:40:35 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Mon, 07 Nov 2022 19:40:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.13-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 19:40:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 19:40:46 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 19:40:46 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 19:40:46 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 19:40:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 19:40:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb106e6b88c840d8bc916d39cbd7e76282f34fad97623abb4a385dbc33404ce`  
		Last Modified: Fri, 04 Nov 2022 23:23:35 GMT  
		Size: 195.2 MB (195201089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8d472e4af581173136f8930af6ec0379c895ae4f9055c5e789b70506fc50b9`  
		Last Modified: Mon, 07 Nov 2022 19:41:37 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3daada422a9710cc2eaf10cf278668d42a9bca8fff6d56bd51e29660622836d`  
		Last Modified: Mon, 07 Nov 2022 19:41:37 GMT  
		Size: 8.2 KB (8171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07db2bdf842dd18cc768758c09347f56998f9dad223c65e61c9eeee7b87b2c40`  
		Last Modified: Mon, 07 Nov 2022 19:41:43 GMT  
		Size: 135.1 MB (135075153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.13-enterprise`

```console
$ docker pull neo4j@sha256:4d11099aa903febe5c7b1e6e5bcce24f4d852af993ba9d4e405de104ad3d25b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.13-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:51c57888494a4b29b9d276b2e25b07ff486cae25de578bcd118e9826484ffe5a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.3 MB (460296432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b3fe022d0ecac26bc3c94ebc206b3ad7d3c2bc95992e464855753adab8ee6b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Mon, 07 Nov 2022 19:25:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f8ae7ee71fb1a7f6d5c549af2456ffa377623fbce3208194a2ee317f524d584 NEO4J_TARBALL=neo4j-enterprise-4.4.13-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 19:25:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.13-unix.tar.gz
# Mon, 07 Nov 2022 19:25:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.13-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 19:25:15 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Mon, 07 Nov 2022 19:25:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.13-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 19:25:30 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 19:25:30 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 19:25:30 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 19:25:31 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 19:25:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 19:25:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a58740ba1d754216b2a37aba19e4bafa6828a438f2946435e6708fb1c1ff047`  
		Last Modified: Mon, 07 Nov 2022 19:27:21 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7cef73c62a6d8fb73997cccaf981a0b6be7aeee85b619ee8d0de83524eb0f8`  
		Last Modified: Mon, 07 Nov 2022 19:27:21 GMT  
		Size: 8.2 KB (8169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4af22fab20d15fde1ab639378860bed58fcc885a6a7a0704b836eab1b0ac4dc`  
		Last Modified: Mon, 07 Nov 2022 19:27:32 GMT  
		Size: 230.4 MB (230408514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.13-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7bc1763d8eb7877201de31d0d8fb569542d0d09967e94338712236f6903bbf52
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.5 MB (455543517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750aa1d0d79e7233a4ca3a5d427d0927ae33f1de830f6fcd138e2f101995dd8a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:12:49 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Mon, 07 Nov 2022 19:40:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f8ae7ee71fb1a7f6d5c549af2456ffa377623fbce3208194a2ee317f524d584 NEO4J_TARBALL=neo4j-enterprise-4.4.13-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 19:40:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.13-unix.tar.gz
# Mon, 07 Nov 2022 19:40:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.13-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 19:40:51 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Mon, 07 Nov 2022 19:41:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.13-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 19:41:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 19:41:04 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 19:41:04 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 19:41:05 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 19:41:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 19:41:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb106e6b88c840d8bc916d39cbd7e76282f34fad97623abb4a385dbc33404ce`  
		Last Modified: Fri, 04 Nov 2022 23:23:35 GMT  
		Size: 195.2 MB (195201089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a4e3b7b1c1272b3c54b0d6f54a16cfc85e38aef8d0dd1f87245a5b3955e2c9`  
		Last Modified: Mon, 07 Nov 2022 19:41:59 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d465f6a2fdbccee0029634a170d505ad47432db1558945a4e817eefd9e36f9c2`  
		Last Modified: Mon, 07 Nov 2022 19:41:59 GMT  
		Size: 8.2 KB (8170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e729f0ff0f2e7e2d60f971ab0c6e57d5b498ff8c6716d71bc351cc25060fe9`  
		Last Modified: Mon, 07 Nov 2022 19:42:10 GMT  
		Size: 230.3 MB (230266460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:589f6b099edcab2848f30899317af61547c2bc36777a66ecf4513ab8a258b4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad88ceb9cced6dc2bb686e060eb2fc68c580a5c82943f1c361ef6a23c099018
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334571402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8fabaef285bc934b646db7981529d3257b2dbd071d0efc166a764f0a05e9a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 20:48:08 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:42:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:42:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:42:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:42:04 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:42:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:42:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:42:16 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:42:16 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:42:16 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:42:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:42:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2d9967bfe9b338d34c1d6b115d688a7c4c9b111a5ea71ceb27421142a7f12b`  
		Last Modified: Mon, 07 Nov 2022 20:57:59 GMT  
		Size: 192.4 MB (192431266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca65b8a2c6678ed5001a523f60b53a78d05bdeafa47afb4159afb57a753d06bc`  
		Last Modified: Mon, 07 Nov 2022 21:43:14 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79ac708f0d7f66d87f165b4cbab59bf15f1e0a9331b05fa459a174e54deb409`  
		Last Modified: Mon, 07 Nov 2022 21:43:14 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbba578ea91813db3207c2be4512eb25b066646974c23a7f6ffb52ec6d0f57e`  
		Last Modified: Mon, 07 Nov 2022 21:43:20 GMT  
		Size: 110.7 MB (110708609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:db984633260a4dcebd2a947b897486e106a59219a926e1edef3ca02f39ce459d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.9 MB (331856654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ae93e09f723d1ce12b8b30075ec388bdd475c3cc75a32ceb3100855e3bd8d5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 21:03:54 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:39:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:39:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:39:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:39:22 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:39:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:39:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:39:31 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:39:31 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:39:31 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:39:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:39:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da08ea5cf75b951398d57ee8bc9c95f4a6a9ffdd4548e791b7ac3a9ea4c9900a`  
		Last Modified: Mon, 07 Nov 2022 21:12:03 GMT  
		Size: 191.2 MB (191215226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78489ea6d327966723e32b2c92b0a25b093bf7fc19d40d6ed0ccba9df1671e59`  
		Last Modified: Mon, 07 Nov 2022 21:40:22 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7fa9e5679baf03c909f45e99134562a0043cdac2d992a0f15f75752052263e`  
		Last Modified: Mon, 07 Nov 2022 21:40:22 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624eb837b81cf0ad6c6b061765b8aec39fb37d7492c2f91d999d6d8fa39931f5`  
		Last Modified: Mon, 07 Nov 2022 21:40:27 GMT  
		Size: 110.6 MB (110566002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:589f6b099edcab2848f30899317af61547c2bc36777a66ecf4513ab8a258b4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad88ceb9cced6dc2bb686e060eb2fc68c580a5c82943f1c361ef6a23c099018
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334571402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8fabaef285bc934b646db7981529d3257b2dbd071d0efc166a764f0a05e9a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 20:48:08 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:42:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:42:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:42:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:42:04 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:42:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:42:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:42:16 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:42:16 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:42:16 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:42:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:42:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2d9967bfe9b338d34c1d6b115d688a7c4c9b111a5ea71ceb27421142a7f12b`  
		Last Modified: Mon, 07 Nov 2022 20:57:59 GMT  
		Size: 192.4 MB (192431266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca65b8a2c6678ed5001a523f60b53a78d05bdeafa47afb4159afb57a753d06bc`  
		Last Modified: Mon, 07 Nov 2022 21:43:14 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79ac708f0d7f66d87f165b4cbab59bf15f1e0a9331b05fa459a174e54deb409`  
		Last Modified: Mon, 07 Nov 2022 21:43:14 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbba578ea91813db3207c2be4512eb25b066646974c23a7f6ffb52ec6d0f57e`  
		Last Modified: Mon, 07 Nov 2022 21:43:20 GMT  
		Size: 110.7 MB (110708609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:db984633260a4dcebd2a947b897486e106a59219a926e1edef3ca02f39ce459d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.9 MB (331856654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ae93e09f723d1ce12b8b30075ec388bdd475c3cc75a32ceb3100855e3bd8d5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 21:03:54 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:39:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:39:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:39:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:39:22 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:39:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:39:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:39:31 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:39:31 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:39:31 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:39:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:39:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da08ea5cf75b951398d57ee8bc9c95f4a6a9ffdd4548e791b7ac3a9ea4c9900a`  
		Last Modified: Mon, 07 Nov 2022 21:12:03 GMT  
		Size: 191.2 MB (191215226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78489ea6d327966723e32b2c92b0a25b093bf7fc19d40d6ed0ccba9df1671e59`  
		Last Modified: Mon, 07 Nov 2022 21:40:22 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7fa9e5679baf03c909f45e99134562a0043cdac2d992a0f15f75752052263e`  
		Last Modified: Mon, 07 Nov 2022 21:40:22 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624eb837b81cf0ad6c6b061765b8aec39fb37d7492c2f91d999d6d8fa39931f5`  
		Last Modified: Mon, 07 Nov 2022 21:40:27 GMT  
		Size: 110.6 MB (110566002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:9a4bcf00ee9014a9ff0b708a3c1030ecb09bb23d8d7522b5fe6f2b88a05fb7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:20b7411918a707659786a1a770d5c8c275565d85d0cada635fade57cf575ab83
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.2 MB (430159743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75672eebe80dbbdaeaff4717d949e0277218793afaf2d8c655fc59634edb3c70`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 20:48:08 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:42:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:42:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:42:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:42:21 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:42:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:42:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:42:36 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:42:36 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:42:36 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:42:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:42:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2d9967bfe9b338d34c1d6b115d688a7c4c9b111a5ea71ceb27421142a7f12b`  
		Last Modified: Mon, 07 Nov 2022 20:57:59 GMT  
		Size: 192.4 MB (192431266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e8565cfe49966c982867a5621e5eaf2dacc4051ede76f2d5fa1c05cc4663e8`  
		Last Modified: Mon, 07 Nov 2022 21:43:45 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a8f35af07dcaed5768cc7f8c4ef833434b4cf18877f9b9b2b829dd76db0a6e`  
		Last Modified: Mon, 07 Nov 2022 21:43:45 GMT  
		Size: 7.6 KB (7631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bef8af0d744b267d17da627ab840c060bc69874505af56002b0e06e1e65abe`  
		Last Modified: Mon, 07 Nov 2022 21:43:55 GMT  
		Size: 206.3 MB (206296947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:63b00a9e963c031cad10716e42ac91ba44aa05241d49480b00ad6a9ee3b9c1c6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.4 MB (427444123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e58c75c545a73f3f586b558acda7045154e84771fd0182d6754c6440d00d025`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 21:03:54 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:39:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:39:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:39:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:39:36 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:39:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:39:54 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:39:54 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:39:54 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:39:54 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:39:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:39:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da08ea5cf75b951398d57ee8bc9c95f4a6a9ffdd4548e791b7ac3a9ea4c9900a`  
		Last Modified: Mon, 07 Nov 2022 21:12:03 GMT  
		Size: 191.2 MB (191215226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a178c84172e1ce76780f08f6343145c0bcdc38eec775c69b6637fcb0be1d393`  
		Last Modified: Mon, 07 Nov 2022 21:40:49 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61a5e1cbd196598c089048696990a1e5f2c180f24cb8c95a97eecfbfc538831`  
		Last Modified: Mon, 07 Nov 2022 21:40:49 GMT  
		Size: 7.6 KB (7629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084b6431edc5985ae0e1d28b4a14112bd2c2b910312a545f0e41991d94b9ab06`  
		Last Modified: Mon, 07 Nov 2022 21:40:57 GMT  
		Size: 206.2 MB (206153470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.1`

```console
$ docker pull neo4j@sha256:589f6b099edcab2848f30899317af61547c2bc36777a66ecf4513ab8a258b4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.1` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad88ceb9cced6dc2bb686e060eb2fc68c580a5c82943f1c361ef6a23c099018
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334571402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8fabaef285bc934b646db7981529d3257b2dbd071d0efc166a764f0a05e9a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 20:48:08 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:42:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:42:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:42:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:42:04 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:42:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:42:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:42:16 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:42:16 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:42:16 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:42:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:42:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2d9967bfe9b338d34c1d6b115d688a7c4c9b111a5ea71ceb27421142a7f12b`  
		Last Modified: Mon, 07 Nov 2022 20:57:59 GMT  
		Size: 192.4 MB (192431266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca65b8a2c6678ed5001a523f60b53a78d05bdeafa47afb4159afb57a753d06bc`  
		Last Modified: Mon, 07 Nov 2022 21:43:14 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79ac708f0d7f66d87f165b4cbab59bf15f1e0a9331b05fa459a174e54deb409`  
		Last Modified: Mon, 07 Nov 2022 21:43:14 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbba578ea91813db3207c2be4512eb25b066646974c23a7f6ffb52ec6d0f57e`  
		Last Modified: Mon, 07 Nov 2022 21:43:20 GMT  
		Size: 110.7 MB (110708609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.1` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:db984633260a4dcebd2a947b897486e106a59219a926e1edef3ca02f39ce459d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.9 MB (331856654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ae93e09f723d1ce12b8b30075ec388bdd475c3cc75a32ceb3100855e3bd8d5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 21:03:54 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:39:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:39:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:39:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:39:22 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:39:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:39:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:39:31 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:39:31 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:39:31 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:39:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:39:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da08ea5cf75b951398d57ee8bc9c95f4a6a9ffdd4548e791b7ac3a9ea4c9900a`  
		Last Modified: Mon, 07 Nov 2022 21:12:03 GMT  
		Size: 191.2 MB (191215226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78489ea6d327966723e32b2c92b0a25b093bf7fc19d40d6ed0ccba9df1671e59`  
		Last Modified: Mon, 07 Nov 2022 21:40:22 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7fa9e5679baf03c909f45e99134562a0043cdac2d992a0f15f75752052263e`  
		Last Modified: Mon, 07 Nov 2022 21:40:22 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624eb837b81cf0ad6c6b061765b8aec39fb37d7492c2f91d999d6d8fa39931f5`  
		Last Modified: Mon, 07 Nov 2022 21:40:27 GMT  
		Size: 110.6 MB (110566002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.1-enterprise`

```console
$ docker pull neo4j@sha256:9a4bcf00ee9014a9ff0b708a3c1030ecb09bb23d8d7522b5fe6f2b88a05fb7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.1-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:20b7411918a707659786a1a770d5c8c275565d85d0cada635fade57cf575ab83
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.2 MB (430159743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75672eebe80dbbdaeaff4717d949e0277218793afaf2d8c655fc59634edb3c70`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 20:48:08 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:42:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:42:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:42:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:42:21 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:42:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:42:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:42:36 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:42:36 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:42:36 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:42:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:42:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2d9967bfe9b338d34c1d6b115d688a7c4c9b111a5ea71ceb27421142a7f12b`  
		Last Modified: Mon, 07 Nov 2022 20:57:59 GMT  
		Size: 192.4 MB (192431266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e8565cfe49966c982867a5621e5eaf2dacc4051ede76f2d5fa1c05cc4663e8`  
		Last Modified: Mon, 07 Nov 2022 21:43:45 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a8f35af07dcaed5768cc7f8c4ef833434b4cf18877f9b9b2b829dd76db0a6e`  
		Last Modified: Mon, 07 Nov 2022 21:43:45 GMT  
		Size: 7.6 KB (7631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bef8af0d744b267d17da627ab840c060bc69874505af56002b0e06e1e65abe`  
		Last Modified: Mon, 07 Nov 2022 21:43:55 GMT  
		Size: 206.3 MB (206296947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.1-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:63b00a9e963c031cad10716e42ac91ba44aa05241d49480b00ad6a9ee3b9c1c6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.4 MB (427444123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e58c75c545a73f3f586b558acda7045154e84771fd0182d6754c6440d00d025`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 21:03:54 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:39:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:39:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:39:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:39:36 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:39:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:39:54 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:39:54 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:39:54 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:39:54 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:39:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:39:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da08ea5cf75b951398d57ee8bc9c95f4a6a9ffdd4548e791b7ac3a9ea4c9900a`  
		Last Modified: Mon, 07 Nov 2022 21:12:03 GMT  
		Size: 191.2 MB (191215226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a178c84172e1ce76780f08f6343145c0bcdc38eec775c69b6637fcb0be1d393`  
		Last Modified: Mon, 07 Nov 2022 21:40:49 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61a5e1cbd196598c089048696990a1e5f2c180f24cb8c95a97eecfbfc538831`  
		Last Modified: Mon, 07 Nov 2022 21:40:49 GMT  
		Size: 7.6 KB (7629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084b6431edc5985ae0e1d28b4a14112bd2c2b910312a545f0e41991d94b9ab06`  
		Last Modified: Mon, 07 Nov 2022 21:40:57 GMT  
		Size: 206.2 MB (206153470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.1.0`

```console
$ docker pull neo4j@sha256:589f6b099edcab2848f30899317af61547c2bc36777a66ecf4513ab8a258b4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.1.0` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad88ceb9cced6dc2bb686e060eb2fc68c580a5c82943f1c361ef6a23c099018
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334571402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8fabaef285bc934b646db7981529d3257b2dbd071d0efc166a764f0a05e9a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 20:48:08 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:42:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:42:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:42:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:42:04 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:42:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:42:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:42:16 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:42:16 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:42:16 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:42:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:42:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2d9967bfe9b338d34c1d6b115d688a7c4c9b111a5ea71ceb27421142a7f12b`  
		Last Modified: Mon, 07 Nov 2022 20:57:59 GMT  
		Size: 192.4 MB (192431266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca65b8a2c6678ed5001a523f60b53a78d05bdeafa47afb4159afb57a753d06bc`  
		Last Modified: Mon, 07 Nov 2022 21:43:14 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79ac708f0d7f66d87f165b4cbab59bf15f1e0a9331b05fa459a174e54deb409`  
		Last Modified: Mon, 07 Nov 2022 21:43:14 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbba578ea91813db3207c2be4512eb25b066646974c23a7f6ffb52ec6d0f57e`  
		Last Modified: Mon, 07 Nov 2022 21:43:20 GMT  
		Size: 110.7 MB (110708609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.1.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:db984633260a4dcebd2a947b897486e106a59219a926e1edef3ca02f39ce459d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.9 MB (331856654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ae93e09f723d1ce12b8b30075ec388bdd475c3cc75a32ceb3100855e3bd8d5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 21:03:54 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:39:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:39:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:39:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:39:22 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:39:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:39:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:39:31 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:39:31 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:39:31 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:39:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:39:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da08ea5cf75b951398d57ee8bc9c95f4a6a9ffdd4548e791b7ac3a9ea4c9900a`  
		Last Modified: Mon, 07 Nov 2022 21:12:03 GMT  
		Size: 191.2 MB (191215226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78489ea6d327966723e32b2c92b0a25b093bf7fc19d40d6ed0ccba9df1671e59`  
		Last Modified: Mon, 07 Nov 2022 21:40:22 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7fa9e5679baf03c909f45e99134562a0043cdac2d992a0f15f75752052263e`  
		Last Modified: Mon, 07 Nov 2022 21:40:22 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624eb837b81cf0ad6c6b061765b8aec39fb37d7492c2f91d999d6d8fa39931f5`  
		Last Modified: Mon, 07 Nov 2022 21:40:27 GMT  
		Size: 110.6 MB (110566002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.1.0-community`

```console
$ docker pull neo4j@sha256:589f6b099edcab2848f30899317af61547c2bc36777a66ecf4513ab8a258b4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.1.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad88ceb9cced6dc2bb686e060eb2fc68c580a5c82943f1c361ef6a23c099018
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334571402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8fabaef285bc934b646db7981529d3257b2dbd071d0efc166a764f0a05e9a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 20:48:08 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:42:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:42:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:42:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:42:04 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:42:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:42:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:42:16 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:42:16 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:42:16 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:42:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:42:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2d9967bfe9b338d34c1d6b115d688a7c4c9b111a5ea71ceb27421142a7f12b`  
		Last Modified: Mon, 07 Nov 2022 20:57:59 GMT  
		Size: 192.4 MB (192431266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca65b8a2c6678ed5001a523f60b53a78d05bdeafa47afb4159afb57a753d06bc`  
		Last Modified: Mon, 07 Nov 2022 21:43:14 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79ac708f0d7f66d87f165b4cbab59bf15f1e0a9331b05fa459a174e54deb409`  
		Last Modified: Mon, 07 Nov 2022 21:43:14 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbba578ea91813db3207c2be4512eb25b066646974c23a7f6ffb52ec6d0f57e`  
		Last Modified: Mon, 07 Nov 2022 21:43:20 GMT  
		Size: 110.7 MB (110708609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.1.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:db984633260a4dcebd2a947b897486e106a59219a926e1edef3ca02f39ce459d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.9 MB (331856654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ae93e09f723d1ce12b8b30075ec388bdd475c3cc75a32ceb3100855e3bd8d5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 21:03:54 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:39:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:39:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:39:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:39:22 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:39:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:39:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:39:31 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:39:31 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:39:31 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:39:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:39:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da08ea5cf75b951398d57ee8bc9c95f4a6a9ffdd4548e791b7ac3a9ea4c9900a`  
		Last Modified: Mon, 07 Nov 2022 21:12:03 GMT  
		Size: 191.2 MB (191215226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78489ea6d327966723e32b2c92b0a25b093bf7fc19d40d6ed0ccba9df1671e59`  
		Last Modified: Mon, 07 Nov 2022 21:40:22 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7fa9e5679baf03c909f45e99134562a0043cdac2d992a0f15f75752052263e`  
		Last Modified: Mon, 07 Nov 2022 21:40:22 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624eb837b81cf0ad6c6b061765b8aec39fb37d7492c2f91d999d6d8fa39931f5`  
		Last Modified: Mon, 07 Nov 2022 21:40:27 GMT  
		Size: 110.6 MB (110566002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.1.0-enterprise`

```console
$ docker pull neo4j@sha256:9a4bcf00ee9014a9ff0b708a3c1030ecb09bb23d8d7522b5fe6f2b88a05fb7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.1.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:20b7411918a707659786a1a770d5c8c275565d85d0cada635fade57cf575ab83
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.2 MB (430159743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75672eebe80dbbdaeaff4717d949e0277218793afaf2d8c655fc59634edb3c70`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 20:48:08 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:42:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:42:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:42:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:42:21 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:42:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:42:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:42:36 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:42:36 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:42:36 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:42:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:42:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2d9967bfe9b338d34c1d6b115d688a7c4c9b111a5ea71ceb27421142a7f12b`  
		Last Modified: Mon, 07 Nov 2022 20:57:59 GMT  
		Size: 192.4 MB (192431266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e8565cfe49966c982867a5621e5eaf2dacc4051ede76f2d5fa1c05cc4663e8`  
		Last Modified: Mon, 07 Nov 2022 21:43:45 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a8f35af07dcaed5768cc7f8c4ef833434b4cf18877f9b9b2b829dd76db0a6e`  
		Last Modified: Mon, 07 Nov 2022 21:43:45 GMT  
		Size: 7.6 KB (7631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bef8af0d744b267d17da627ab840c060bc69874505af56002b0e06e1e65abe`  
		Last Modified: Mon, 07 Nov 2022 21:43:55 GMT  
		Size: 206.3 MB (206296947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.1.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:63b00a9e963c031cad10716e42ac91ba44aa05241d49480b00ad6a9ee3b9c1c6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.4 MB (427444123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e58c75c545a73f3f586b558acda7045154e84771fd0182d6754c6440d00d025`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 21:03:54 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:39:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:39:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:39:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:39:36 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:39:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:39:54 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:39:54 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:39:54 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:39:54 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:39:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:39:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da08ea5cf75b951398d57ee8bc9c95f4a6a9ffdd4548e791b7ac3a9ea4c9900a`  
		Last Modified: Mon, 07 Nov 2022 21:12:03 GMT  
		Size: 191.2 MB (191215226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a178c84172e1ce76780f08f6343145c0bcdc38eec775c69b6637fcb0be1d393`  
		Last Modified: Mon, 07 Nov 2022 21:40:49 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61a5e1cbd196598c089048696990a1e5f2c180f24cb8c95a97eecfbfc538831`  
		Last Modified: Mon, 07 Nov 2022 21:40:49 GMT  
		Size: 7.6 KB (7629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084b6431edc5985ae0e1d28b4a14112bd2c2b910312a545f0e41991d94b9ab06`  
		Last Modified: Mon, 07 Nov 2022 21:40:57 GMT  
		Size: 206.2 MB (206153470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:589f6b099edcab2848f30899317af61547c2bc36777a66ecf4513ab8a258b4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad88ceb9cced6dc2bb686e060eb2fc68c580a5c82943f1c361ef6a23c099018
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334571402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8fabaef285bc934b646db7981529d3257b2dbd071d0efc166a764f0a05e9a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 20:48:08 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:42:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:42:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:42:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:42:04 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:42:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:42:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:42:16 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:42:16 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:42:16 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:42:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:42:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2d9967bfe9b338d34c1d6b115d688a7c4c9b111a5ea71ceb27421142a7f12b`  
		Last Modified: Mon, 07 Nov 2022 20:57:59 GMT  
		Size: 192.4 MB (192431266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca65b8a2c6678ed5001a523f60b53a78d05bdeafa47afb4159afb57a753d06bc`  
		Last Modified: Mon, 07 Nov 2022 21:43:14 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79ac708f0d7f66d87f165b4cbab59bf15f1e0a9331b05fa459a174e54deb409`  
		Last Modified: Mon, 07 Nov 2022 21:43:14 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbba578ea91813db3207c2be4512eb25b066646974c23a7f6ffb52ec6d0f57e`  
		Last Modified: Mon, 07 Nov 2022 21:43:20 GMT  
		Size: 110.7 MB (110708609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:db984633260a4dcebd2a947b897486e106a59219a926e1edef3ca02f39ce459d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.9 MB (331856654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ae93e09f723d1ce12b8b30075ec388bdd475c3cc75a32ceb3100855e3bd8d5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 21:03:54 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:39:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:39:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:39:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:39:22 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:39:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:39:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:39:31 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:39:31 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:39:31 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:39:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:39:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da08ea5cf75b951398d57ee8bc9c95f4a6a9ffdd4548e791b7ac3a9ea4c9900a`  
		Last Modified: Mon, 07 Nov 2022 21:12:03 GMT  
		Size: 191.2 MB (191215226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78489ea6d327966723e32b2c92b0a25b093bf7fc19d40d6ed0ccba9df1671e59`  
		Last Modified: Mon, 07 Nov 2022 21:40:22 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7fa9e5679baf03c909f45e99134562a0043cdac2d992a0f15f75752052263e`  
		Last Modified: Mon, 07 Nov 2022 21:40:22 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624eb837b81cf0ad6c6b061765b8aec39fb37d7492c2f91d999d6d8fa39931f5`  
		Last Modified: Mon, 07 Nov 2022 21:40:27 GMT  
		Size: 110.6 MB (110566002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:9a4bcf00ee9014a9ff0b708a3c1030ecb09bb23d8d7522b5fe6f2b88a05fb7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:20b7411918a707659786a1a770d5c8c275565d85d0cada635fade57cf575ab83
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.2 MB (430159743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75672eebe80dbbdaeaff4717d949e0277218793afaf2d8c655fc59634edb3c70`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 20:48:08 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:42:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:42:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:42:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:42:21 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:42:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:42:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:42:36 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:42:36 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:42:36 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:42:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:42:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2d9967bfe9b338d34c1d6b115d688a7c4c9b111a5ea71ceb27421142a7f12b`  
		Last Modified: Mon, 07 Nov 2022 20:57:59 GMT  
		Size: 192.4 MB (192431266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e8565cfe49966c982867a5621e5eaf2dacc4051ede76f2d5fa1c05cc4663e8`  
		Last Modified: Mon, 07 Nov 2022 21:43:45 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a8f35af07dcaed5768cc7f8c4ef833434b4cf18877f9b9b2b829dd76db0a6e`  
		Last Modified: Mon, 07 Nov 2022 21:43:45 GMT  
		Size: 7.6 KB (7631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bef8af0d744b267d17da627ab840c060bc69874505af56002b0e06e1e65abe`  
		Last Modified: Mon, 07 Nov 2022 21:43:55 GMT  
		Size: 206.3 MB (206296947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:63b00a9e963c031cad10716e42ac91ba44aa05241d49480b00ad6a9ee3b9c1c6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.4 MB (427444123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e58c75c545a73f3f586b558acda7045154e84771fd0182d6754c6440d00d025`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 21:03:54 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:39:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:39:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:39:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:39:36 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:39:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:39:54 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:39:54 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:39:54 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:39:54 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:39:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:39:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da08ea5cf75b951398d57ee8bc9c95f4a6a9ffdd4548e791b7ac3a9ea4c9900a`  
		Last Modified: Mon, 07 Nov 2022 21:12:03 GMT  
		Size: 191.2 MB (191215226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a178c84172e1ce76780f08f6343145c0bcdc38eec775c69b6637fcb0be1d393`  
		Last Modified: Mon, 07 Nov 2022 21:40:49 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61a5e1cbd196598c089048696990a1e5f2c180f24cb8c95a97eecfbfc538831`  
		Last Modified: Mon, 07 Nov 2022 21:40:49 GMT  
		Size: 7.6 KB (7629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084b6431edc5985ae0e1d28b4a14112bd2c2b910312a545f0e41991d94b9ab06`  
		Last Modified: Mon, 07 Nov 2022 21:40:57 GMT  
		Size: 206.2 MB (206153470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:589f6b099edcab2848f30899317af61547c2bc36777a66ecf4513ab8a258b4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad88ceb9cced6dc2bb686e060eb2fc68c580a5c82943f1c361ef6a23c099018
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334571402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8fabaef285bc934b646db7981529d3257b2dbd071d0efc166a764f0a05e9a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 20:48:08 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:42:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:42:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:42:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:42:04 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:42:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:42:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:42:16 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:42:16 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:42:16 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:42:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:42:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2d9967bfe9b338d34c1d6b115d688a7c4c9b111a5ea71ceb27421142a7f12b`  
		Last Modified: Mon, 07 Nov 2022 20:57:59 GMT  
		Size: 192.4 MB (192431266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca65b8a2c6678ed5001a523f60b53a78d05bdeafa47afb4159afb57a753d06bc`  
		Last Modified: Mon, 07 Nov 2022 21:43:14 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79ac708f0d7f66d87f165b4cbab59bf15f1e0a9331b05fa459a174e54deb409`  
		Last Modified: Mon, 07 Nov 2022 21:43:14 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbba578ea91813db3207c2be4512eb25b066646974c23a7f6ffb52ec6d0f57e`  
		Last Modified: Mon, 07 Nov 2022 21:43:20 GMT  
		Size: 110.7 MB (110708609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:db984633260a4dcebd2a947b897486e106a59219a926e1edef3ca02f39ce459d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.9 MB (331856654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ae93e09f723d1ce12b8b30075ec388bdd475c3cc75a32ceb3100855e3bd8d5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 21:03:54 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:39:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 07 Nov 2022 21:39:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Mon, 07 Nov 2022 21:39:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 07 Nov 2022 21:39:22 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Mon, 07 Nov 2022 21:39:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 07 Nov 2022 21:39:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:39:31 GMT
WORKDIR /var/lib/neo4j
# Mon, 07 Nov 2022 21:39:31 GMT
VOLUME [/data /logs]
# Mon, 07 Nov 2022 21:39:31 GMT
EXPOSE 7473 7474 7687
# Mon, 07 Nov 2022 21:39:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 07 Nov 2022 21:39:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da08ea5cf75b951398d57ee8bc9c95f4a6a9ffdd4548e791b7ac3a9ea4c9900a`  
		Last Modified: Mon, 07 Nov 2022 21:12:03 GMT  
		Size: 191.2 MB (191215226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78489ea6d327966723e32b2c92b0a25b093bf7fc19d40d6ed0ccba9df1671e59`  
		Last Modified: Mon, 07 Nov 2022 21:40:22 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7fa9e5679baf03c909f45e99134562a0043cdac2d992a0f15f75752052263e`  
		Last Modified: Mon, 07 Nov 2022 21:40:22 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624eb837b81cf0ad6c6b061765b8aec39fb37d7492c2f91d999d6d8fa39931f5`  
		Last Modified: Mon, 07 Nov 2022 21:40:27 GMT  
		Size: 110.6 MB (110566002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
