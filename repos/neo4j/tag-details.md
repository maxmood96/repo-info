<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.27`](#neo4j4427)
-	[`neo4j:4.4.27-community`](#neo4j4427-community)
-	[`neo4j:4.4.27-enterprise`](#neo4j4427-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-bullseye`](#neo4j5-bullseye)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-community-bullseye`](#neo4j5-community-bullseye)
-	[`neo4j:5-community-ubi8`](#neo4j5-community-ubi8)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5-enterprise-bullseye`](#neo4j5-enterprise-bullseye)
-	[`neo4j:5-enterprise-ubi8`](#neo4j5-enterprise-ubi8)
-	[`neo4j:5-ubi8`](#neo4j5-ubi8)
-	[`neo4j:5.13`](#neo4j513)
-	[`neo4j:5.13-bullseye`](#neo4j513-bullseye)
-	[`neo4j:5.13-community`](#neo4j513-community)
-	[`neo4j:5.13-community-bullseye`](#neo4j513-community-bullseye)
-	[`neo4j:5.13-community-ubi8`](#neo4j513-community-ubi8)
-	[`neo4j:5.13-enterprise`](#neo4j513-enterprise)
-	[`neo4j:5.13-enterprise-bullseye`](#neo4j513-enterprise-bullseye)
-	[`neo4j:5.13-enterprise-ubi8`](#neo4j513-enterprise-ubi8)
-	[`neo4j:5.13-ubi8`](#neo4j513-ubi8)
-	[`neo4j:5.13.0`](#neo4j5130)
-	[`neo4j:5.13.0-bullseye`](#neo4j5130-bullseye)
-	[`neo4j:5.13.0-community`](#neo4j5130-community)
-	[`neo4j:5.13.0-community-bullseye`](#neo4j5130-community-bullseye)
-	[`neo4j:5.13.0-community-ubi8`](#neo4j5130-community-ubi8)
-	[`neo4j:5.13.0-enterprise`](#neo4j5130-enterprise)
-	[`neo4j:5.13.0-enterprise-bullseye`](#neo4j5130-enterprise-bullseye)
-	[`neo4j:5.13.0-enterprise-ubi8`](#neo4j5130-enterprise-ubi8)
-	[`neo4j:5.13.0-ubi8`](#neo4j5130-ubi8)
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
$ docker pull neo4j@sha256:0e593674d131841df7955d637c17a7f4e4622c2318a771e658b37f9f92c1c3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:605ed770d210979ed7626dcc0ae015d2b0a35d641e068017333f6ade0c955849
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298209808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981c2a6e767fbf788c3c2e6b48c0471e4b00fa74e5f4d97e2a9c0c58e9df5523`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:15:11 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:53:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f6eef5bcb224396393e67022c768c8fdb7a89bba6b926c622bc1093398f0ffcd NEO4J_TARBALL=neo4j-community-4.4.27-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:53:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
# Tue, 21 Nov 2023 19:53:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:53:10 GMT
COPY multi:6a59fb6c086225f45b1cdcf015360d89654939b0b18a918024f9ff44b0e3e0ff in /startup/ 
# Tue, 21 Nov 2023 19:53:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:53:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:53:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:53:21 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:53:21 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:53:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:53:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d18499daad2b8d9b0b9bdb87567af55fc240e281e74f93c4b5246c132b2723`  
		Last Modified: Tue, 21 Nov 2023 10:32:54 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2b4836a2560d3250bba50e014a852cdf49f32b8c4b22725a34aa7fc9d5fef6`  
		Last Modified: Tue, 21 Nov 2023 19:56:09 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cc0caaf2156fb44788795819b3d9a48253b598458000a135f4b2ed424e769d`  
		Last Modified: Tue, 21 Nov 2023 19:56:09 GMT  
		Size: 9.3 KB (9300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fb424c5109e04033ca2a5dbd83f6f43b1ac722950a514cb961b6863f6209b7`  
		Last Modified: Tue, 21 Nov 2023 19:56:15 GMT  
		Size: 121.5 MB (121512137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9e4c728ef21c2bfc12de52791a91ae29da1065884ac8a5309a4eb1e5db0709b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293483024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f1c4540c4c5d0de940d963613af18bd5e77f97f75467b67e5f8c936a719ab5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:27:44 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:03:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f6eef5bcb224396393e67022c768c8fdb7a89bba6b926c622bc1093398f0ffcd NEO4J_TARBALL=neo4j-community-4.4.27-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:03:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
# Tue, 21 Nov 2023 09:03:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:03:31 GMT
COPY multi:6a59fb6c086225f45b1cdcf015360d89654939b0b18a918024f9ff44b0e3e0ff in /startup/ 
# Tue, 21 Nov 2023 09:03:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:03:45 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:03:45 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:03:45 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:03:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:03:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f2af46f3972376700014e0c9774a8df2751034b3161a3d702c25eb208caad7`  
		Last Modified: Tue, 21 Nov 2023 07:43:54 GMT  
		Size: 142.0 MB (142001953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c6e88f22dcc928fffe1fc9644eaf0cda78ef4c8f6355d9ad8df50c4f6c3069`  
		Last Modified: Tue, 21 Nov 2023 09:05:52 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad7d099ac651269e37a67c5c9a956ee0b100508909424e7da45d3edd360ad47`  
		Last Modified: Tue, 21 Nov 2023 09:05:52 GMT  
		Size: 9.3 KB (9300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c828f96cc6fafff0ed21e259c36fa7c080a702a68b6eff41832a5f59406cbdcd`  
		Last Modified: Tue, 21 Nov 2023 09:05:57 GMT  
		Size: 121.4 MB (121403763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:0e593674d131841df7955d637c17a7f4e4622c2318a771e658b37f9f92c1c3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:605ed770d210979ed7626dcc0ae015d2b0a35d641e068017333f6ade0c955849
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298209808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981c2a6e767fbf788c3c2e6b48c0471e4b00fa74e5f4d97e2a9c0c58e9df5523`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:15:11 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:53:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f6eef5bcb224396393e67022c768c8fdb7a89bba6b926c622bc1093398f0ffcd NEO4J_TARBALL=neo4j-community-4.4.27-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:53:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
# Tue, 21 Nov 2023 19:53:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:53:10 GMT
COPY multi:6a59fb6c086225f45b1cdcf015360d89654939b0b18a918024f9ff44b0e3e0ff in /startup/ 
# Tue, 21 Nov 2023 19:53:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:53:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:53:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:53:21 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:53:21 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:53:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:53:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d18499daad2b8d9b0b9bdb87567af55fc240e281e74f93c4b5246c132b2723`  
		Last Modified: Tue, 21 Nov 2023 10:32:54 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2b4836a2560d3250bba50e014a852cdf49f32b8c4b22725a34aa7fc9d5fef6`  
		Last Modified: Tue, 21 Nov 2023 19:56:09 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cc0caaf2156fb44788795819b3d9a48253b598458000a135f4b2ed424e769d`  
		Last Modified: Tue, 21 Nov 2023 19:56:09 GMT  
		Size: 9.3 KB (9300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fb424c5109e04033ca2a5dbd83f6f43b1ac722950a514cb961b6863f6209b7`  
		Last Modified: Tue, 21 Nov 2023 19:56:15 GMT  
		Size: 121.5 MB (121512137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9e4c728ef21c2bfc12de52791a91ae29da1065884ac8a5309a4eb1e5db0709b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293483024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f1c4540c4c5d0de940d963613af18bd5e77f97f75467b67e5f8c936a719ab5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:27:44 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:03:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f6eef5bcb224396393e67022c768c8fdb7a89bba6b926c622bc1093398f0ffcd NEO4J_TARBALL=neo4j-community-4.4.27-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:03:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
# Tue, 21 Nov 2023 09:03:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:03:31 GMT
COPY multi:6a59fb6c086225f45b1cdcf015360d89654939b0b18a918024f9ff44b0e3e0ff in /startup/ 
# Tue, 21 Nov 2023 09:03:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:03:45 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:03:45 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:03:45 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:03:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:03:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f2af46f3972376700014e0c9774a8df2751034b3161a3d702c25eb208caad7`  
		Last Modified: Tue, 21 Nov 2023 07:43:54 GMT  
		Size: 142.0 MB (142001953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c6e88f22dcc928fffe1fc9644eaf0cda78ef4c8f6355d9ad8df50c4f6c3069`  
		Last Modified: Tue, 21 Nov 2023 09:05:52 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad7d099ac651269e37a67c5c9a956ee0b100508909424e7da45d3edd360ad47`  
		Last Modified: Tue, 21 Nov 2023 09:05:52 GMT  
		Size: 9.3 KB (9300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c828f96cc6fafff0ed21e259c36fa7c080a702a68b6eff41832a5f59406cbdcd`  
		Last Modified: Tue, 21 Nov 2023 09:05:57 GMT  
		Size: 121.4 MB (121403763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:750398067aff722afb530f4f4c90bbb34e8bfca2d2ecfbb9652e88b77fb83cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:6adfdc5cb4ee8cc5a543679bb943e80a8ccc5c3a25430360a5e09a4081336882
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.7 MB (402737865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed8f6ee8d4f229e8985b290b15ea9d849615afacf2e763d39f28d11681d31cd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:15:11 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:53:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e5b9d9cea72b676d384a4d71bec4d83c98084e0907d268475d48154a8b4ef0b4 NEO4J_TARBALL=neo4j-enterprise-4.4.27-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:53:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.27-unix.tar.gz
# Tue, 21 Nov 2023 19:53:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.27-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:53:27 GMT
COPY multi:6a59fb6c086225f45b1cdcf015360d89654939b0b18a918024f9ff44b0e3e0ff in /startup/ 
# Tue, 21 Nov 2023 19:53:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.27-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:53:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:53:41 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:53:41 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:53:41 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:53:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:53:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d18499daad2b8d9b0b9bdb87567af55fc240e281e74f93c4b5246c132b2723`  
		Last Modified: Tue, 21 Nov 2023 10:32:54 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efa65183835cff34731428738d32811c47f61a0305e119f145a23b8b74d76b5`  
		Last Modified: Tue, 21 Nov 2023 19:56:27 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66685cd5d35b837f29e6b10c836cd91199dd1143bf56512617f7526cf8a1191a`  
		Last Modified: Tue, 21 Nov 2023 19:56:27 GMT  
		Size: 9.3 KB (9300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7269c22710d5ef618565cd99735105b2bbe94cfaedf3ebdd30b4072d960121`  
		Last Modified: Tue, 21 Nov 2023 19:56:37 GMT  
		Size: 226.0 MB (226040202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:636e3c9f7705bf97ffab44590baef1ad62f764f677a83831df3b7de5051fc902
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.0 MB (398012213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310c21167a9308dd1bf2a23fe388838cdba62f6410ed0fdee2aaf25cb968b428`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:27:44 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:03:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e5b9d9cea72b676d384a4d71bec4d83c98084e0907d268475d48154a8b4ef0b4 NEO4J_TARBALL=neo4j-enterprise-4.4.27-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:03:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.27-unix.tar.gz
# Tue, 21 Nov 2023 09:03:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.27-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:03:50 GMT
COPY multi:6a59fb6c086225f45b1cdcf015360d89654939b0b18a918024f9ff44b0e3e0ff in /startup/ 
# Tue, 21 Nov 2023 09:04:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.27-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:04:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:04:10 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:04:10 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:04:10 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:04:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:04:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f2af46f3972376700014e0c9774a8df2751034b3161a3d702c25eb208caad7`  
		Last Modified: Tue, 21 Nov 2023 07:43:54 GMT  
		Size: 142.0 MB (142001953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f3946b4f487d9922a0eccf678dd8df6e8e1bb63359f25307f2dc6725e4bd46`  
		Last Modified: Tue, 21 Nov 2023 09:06:10 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5bb594acdefff6d841b363d374f74ee8d48c96e9d2569c2e9ae6f1ddcc337d`  
		Last Modified: Tue, 21 Nov 2023 09:06:10 GMT  
		Size: 9.3 KB (9296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7069e7943ea20f82d164b005461a230b8d1bb0323eb10c79ce3be4ed78c0a425`  
		Last Modified: Tue, 21 Nov 2023 09:06:18 GMT  
		Size: 225.9 MB (225932955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.27`

```console
$ docker pull neo4j@sha256:0e593674d131841df7955d637c17a7f4e4622c2318a771e658b37f9f92c1c3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.27` - linux; amd64

```console
$ docker pull neo4j@sha256:605ed770d210979ed7626dcc0ae015d2b0a35d641e068017333f6ade0c955849
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298209808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981c2a6e767fbf788c3c2e6b48c0471e4b00fa74e5f4d97e2a9c0c58e9df5523`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:15:11 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:53:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f6eef5bcb224396393e67022c768c8fdb7a89bba6b926c622bc1093398f0ffcd NEO4J_TARBALL=neo4j-community-4.4.27-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:53:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
# Tue, 21 Nov 2023 19:53:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:53:10 GMT
COPY multi:6a59fb6c086225f45b1cdcf015360d89654939b0b18a918024f9ff44b0e3e0ff in /startup/ 
# Tue, 21 Nov 2023 19:53:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:53:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:53:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:53:21 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:53:21 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:53:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:53:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d18499daad2b8d9b0b9bdb87567af55fc240e281e74f93c4b5246c132b2723`  
		Last Modified: Tue, 21 Nov 2023 10:32:54 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2b4836a2560d3250bba50e014a852cdf49f32b8c4b22725a34aa7fc9d5fef6`  
		Last Modified: Tue, 21 Nov 2023 19:56:09 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cc0caaf2156fb44788795819b3d9a48253b598458000a135f4b2ed424e769d`  
		Last Modified: Tue, 21 Nov 2023 19:56:09 GMT  
		Size: 9.3 KB (9300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fb424c5109e04033ca2a5dbd83f6f43b1ac722950a514cb961b6863f6209b7`  
		Last Modified: Tue, 21 Nov 2023 19:56:15 GMT  
		Size: 121.5 MB (121512137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.27` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9e4c728ef21c2bfc12de52791a91ae29da1065884ac8a5309a4eb1e5db0709b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293483024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f1c4540c4c5d0de940d963613af18bd5e77f97f75467b67e5f8c936a719ab5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:27:44 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:03:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f6eef5bcb224396393e67022c768c8fdb7a89bba6b926c622bc1093398f0ffcd NEO4J_TARBALL=neo4j-community-4.4.27-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:03:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
# Tue, 21 Nov 2023 09:03:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:03:31 GMT
COPY multi:6a59fb6c086225f45b1cdcf015360d89654939b0b18a918024f9ff44b0e3e0ff in /startup/ 
# Tue, 21 Nov 2023 09:03:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:03:45 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:03:45 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:03:45 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:03:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:03:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f2af46f3972376700014e0c9774a8df2751034b3161a3d702c25eb208caad7`  
		Last Modified: Tue, 21 Nov 2023 07:43:54 GMT  
		Size: 142.0 MB (142001953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c6e88f22dcc928fffe1fc9644eaf0cda78ef4c8f6355d9ad8df50c4f6c3069`  
		Last Modified: Tue, 21 Nov 2023 09:05:52 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad7d099ac651269e37a67c5c9a956ee0b100508909424e7da45d3edd360ad47`  
		Last Modified: Tue, 21 Nov 2023 09:05:52 GMT  
		Size: 9.3 KB (9300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c828f96cc6fafff0ed21e259c36fa7c080a702a68b6eff41832a5f59406cbdcd`  
		Last Modified: Tue, 21 Nov 2023 09:05:57 GMT  
		Size: 121.4 MB (121403763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.27-community`

```console
$ docker pull neo4j@sha256:0e593674d131841df7955d637c17a7f4e4622c2318a771e658b37f9f92c1c3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.27-community` - linux; amd64

```console
$ docker pull neo4j@sha256:605ed770d210979ed7626dcc0ae015d2b0a35d641e068017333f6ade0c955849
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298209808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981c2a6e767fbf788c3c2e6b48c0471e4b00fa74e5f4d97e2a9c0c58e9df5523`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:15:11 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:53:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f6eef5bcb224396393e67022c768c8fdb7a89bba6b926c622bc1093398f0ffcd NEO4J_TARBALL=neo4j-community-4.4.27-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:53:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
# Tue, 21 Nov 2023 19:53:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:53:10 GMT
COPY multi:6a59fb6c086225f45b1cdcf015360d89654939b0b18a918024f9ff44b0e3e0ff in /startup/ 
# Tue, 21 Nov 2023 19:53:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:53:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:53:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:53:21 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:53:21 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:53:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:53:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d18499daad2b8d9b0b9bdb87567af55fc240e281e74f93c4b5246c132b2723`  
		Last Modified: Tue, 21 Nov 2023 10:32:54 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2b4836a2560d3250bba50e014a852cdf49f32b8c4b22725a34aa7fc9d5fef6`  
		Last Modified: Tue, 21 Nov 2023 19:56:09 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cc0caaf2156fb44788795819b3d9a48253b598458000a135f4b2ed424e769d`  
		Last Modified: Tue, 21 Nov 2023 19:56:09 GMT  
		Size: 9.3 KB (9300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fb424c5109e04033ca2a5dbd83f6f43b1ac722950a514cb961b6863f6209b7`  
		Last Modified: Tue, 21 Nov 2023 19:56:15 GMT  
		Size: 121.5 MB (121512137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.27-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9e4c728ef21c2bfc12de52791a91ae29da1065884ac8a5309a4eb1e5db0709b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293483024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f1c4540c4c5d0de940d963613af18bd5e77f97f75467b67e5f8c936a719ab5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:27:44 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:03:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f6eef5bcb224396393e67022c768c8fdb7a89bba6b926c622bc1093398f0ffcd NEO4J_TARBALL=neo4j-community-4.4.27-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:03:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
# Tue, 21 Nov 2023 09:03:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:03:31 GMT
COPY multi:6a59fb6c086225f45b1cdcf015360d89654939b0b18a918024f9ff44b0e3e0ff in /startup/ 
# Tue, 21 Nov 2023 09:03:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.27-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:03:45 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:03:45 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:03:45 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:03:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:03:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f2af46f3972376700014e0c9774a8df2751034b3161a3d702c25eb208caad7`  
		Last Modified: Tue, 21 Nov 2023 07:43:54 GMT  
		Size: 142.0 MB (142001953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c6e88f22dcc928fffe1fc9644eaf0cda78ef4c8f6355d9ad8df50c4f6c3069`  
		Last Modified: Tue, 21 Nov 2023 09:05:52 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad7d099ac651269e37a67c5c9a956ee0b100508909424e7da45d3edd360ad47`  
		Last Modified: Tue, 21 Nov 2023 09:05:52 GMT  
		Size: 9.3 KB (9300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c828f96cc6fafff0ed21e259c36fa7c080a702a68b6eff41832a5f59406cbdcd`  
		Last Modified: Tue, 21 Nov 2023 09:05:57 GMT  
		Size: 121.4 MB (121403763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.27-enterprise`

```console
$ docker pull neo4j@sha256:750398067aff722afb530f4f4c90bbb34e8bfca2d2ecfbb9652e88b77fb83cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.27-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:6adfdc5cb4ee8cc5a543679bb943e80a8ccc5c3a25430360a5e09a4081336882
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.7 MB (402737865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed8f6ee8d4f229e8985b290b15ea9d849615afacf2e763d39f28d11681d31cd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:15:11 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:53:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e5b9d9cea72b676d384a4d71bec4d83c98084e0907d268475d48154a8b4ef0b4 NEO4J_TARBALL=neo4j-enterprise-4.4.27-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:53:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.27-unix.tar.gz
# Tue, 21 Nov 2023 19:53:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.27-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:53:27 GMT
COPY multi:6a59fb6c086225f45b1cdcf015360d89654939b0b18a918024f9ff44b0e3e0ff in /startup/ 
# Tue, 21 Nov 2023 19:53:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.27-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:53:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:53:41 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:53:41 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:53:41 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:53:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:53:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d18499daad2b8d9b0b9bdb87567af55fc240e281e74f93c4b5246c132b2723`  
		Last Modified: Tue, 21 Nov 2023 10:32:54 GMT  
		Size: 145.3 MB (145266683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efa65183835cff34731428738d32811c47f61a0305e119f145a23b8b74d76b5`  
		Last Modified: Tue, 21 Nov 2023 19:56:27 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66685cd5d35b837f29e6b10c836cd91199dd1143bf56512617f7526cf8a1191a`  
		Last Modified: Tue, 21 Nov 2023 19:56:27 GMT  
		Size: 9.3 KB (9300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7269c22710d5ef618565cd99735105b2bbe94cfaedf3ebdd30b4072d960121`  
		Last Modified: Tue, 21 Nov 2023 19:56:37 GMT  
		Size: 226.0 MB (226040202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.27-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:636e3c9f7705bf97ffab44590baef1ad62f764f677a83831df3b7de5051fc902
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.0 MB (398012213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310c21167a9308dd1bf2a23fe388838cdba62f6410ed0fdee2aaf25cb968b428`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:27:44 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:03:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e5b9d9cea72b676d384a4d71bec4d83c98084e0907d268475d48154a8b4ef0b4 NEO4J_TARBALL=neo4j-enterprise-4.4.27-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:03:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.27-unix.tar.gz
# Tue, 21 Nov 2023 09:03:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.27-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:03:50 GMT
COPY multi:6a59fb6c086225f45b1cdcf015360d89654939b0b18a918024f9ff44b0e3e0ff in /startup/ 
# Tue, 21 Nov 2023 09:04:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.27-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:04:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:04:10 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:04:10 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:04:10 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:04:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:04:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f2af46f3972376700014e0c9774a8df2751034b3161a3d702c25eb208caad7`  
		Last Modified: Tue, 21 Nov 2023 07:43:54 GMT  
		Size: 142.0 MB (142001953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f3946b4f487d9922a0eccf678dd8df6e8e1bb63359f25307f2dc6725e4bd46`  
		Last Modified: Tue, 21 Nov 2023 09:06:10 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5bb594acdefff6d841b363d374f74ee8d48c96e9d2569c2e9ae6f1ddcc337d`  
		Last Modified: Tue, 21 Nov 2023 09:06:10 GMT  
		Size: 9.3 KB (9296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7069e7943ea20f82d164b005461a230b8d1bb0323eb10c79ce3be4ed78c0a425`  
		Last Modified: Tue, 21 Nov 2023 09:06:18 GMT  
		Size: 225.9 MB (225932955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:6c6003e890c75c9136df06b9061afbbf9a70673711d2d9abc5937ca7f01abb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:1405b33f9d954b9962af09c3e8f8b69feb900cd917e7b24f9c3ca8d79dcf5dc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90fdf60dd2cdaa8631b8f2fe6906033728268064e21b9973ac341c2dce9bdd2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:21 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:52:37 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:52:37 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:52:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:52:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcf18532b0b5fe4037c5643568f1d179ff345d7055a7ac8a71d63d1358e919c`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024503fd6dce42f3b55a864c14a052cd01a6bc282c4bf992fee6ef4ba23cdf4`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79e7641645bdde609e308b0dc0cc7d3ed00f75229dfb351f7fdf838879ec17`  
		Last Modified: Tue, 21 Nov 2023 19:54:29 GMT  
		Size: 116.4 MB (116381803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4dfad0cf1fc9f49cd246d745c8e60de2655f5958cc9cf12c168ed9d89185412e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb3d9da9e8ef38511b9955ba39428d12508f08cfafd8120af33d7cb05c93a8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:02:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:02:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:02:50 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:02:50 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:02:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:02:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed5153b386f9e459da48369f426fafcc7640cc04e0a93a1b51328c28016de09`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac447c42fc4123607bbba8b0d6039aebd3f7398430097e791c6e733e6aef7e13`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584e8c85115b60c19fc0c86c9bc644df5aa9461a6c2d48b21b3d0a0a7fc436df`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 116.3 MB (116275156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:6c6003e890c75c9136df06b9061afbbf9a70673711d2d9abc5937ca7f01abb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1405b33f9d954b9962af09c3e8f8b69feb900cd917e7b24f9c3ca8d79dcf5dc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90fdf60dd2cdaa8631b8f2fe6906033728268064e21b9973ac341c2dce9bdd2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:21 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:52:37 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:52:37 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:52:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:52:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcf18532b0b5fe4037c5643568f1d179ff345d7055a7ac8a71d63d1358e919c`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024503fd6dce42f3b55a864c14a052cd01a6bc282c4bf992fee6ef4ba23cdf4`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79e7641645bdde609e308b0dc0cc7d3ed00f75229dfb351f7fdf838879ec17`  
		Last Modified: Tue, 21 Nov 2023 19:54:29 GMT  
		Size: 116.4 MB (116381803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4dfad0cf1fc9f49cd246d745c8e60de2655f5958cc9cf12c168ed9d89185412e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb3d9da9e8ef38511b9955ba39428d12508f08cfafd8120af33d7cb05c93a8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:02:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:02:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:02:50 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:02:50 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:02:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:02:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed5153b386f9e459da48369f426fafcc7640cc04e0a93a1b51328c28016de09`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac447c42fc4123607bbba8b0d6039aebd3f7398430097e791c6e733e6aef7e13`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584e8c85115b60c19fc0c86c9bc644df5aa9461a6c2d48b21b3d0a0a7fc436df`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 116.3 MB (116275156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:6c6003e890c75c9136df06b9061afbbf9a70673711d2d9abc5937ca7f01abb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:1405b33f9d954b9962af09c3e8f8b69feb900cd917e7b24f9c3ca8d79dcf5dc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90fdf60dd2cdaa8631b8f2fe6906033728268064e21b9973ac341c2dce9bdd2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:21 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:52:37 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:52:37 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:52:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:52:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcf18532b0b5fe4037c5643568f1d179ff345d7055a7ac8a71d63d1358e919c`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024503fd6dce42f3b55a864c14a052cd01a6bc282c4bf992fee6ef4ba23cdf4`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79e7641645bdde609e308b0dc0cc7d3ed00f75229dfb351f7fdf838879ec17`  
		Last Modified: Tue, 21 Nov 2023 19:54:29 GMT  
		Size: 116.4 MB (116381803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4dfad0cf1fc9f49cd246d745c8e60de2655f5958cc9cf12c168ed9d89185412e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb3d9da9e8ef38511b9955ba39428d12508f08cfafd8120af33d7cb05c93a8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:02:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:02:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:02:50 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:02:50 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:02:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:02:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed5153b386f9e459da48369f426fafcc7640cc04e0a93a1b51328c28016de09`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac447c42fc4123607bbba8b0d6039aebd3f7398430097e791c6e733e6aef7e13`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584e8c85115b60c19fc0c86c9bc644df5aa9461a6c2d48b21b3d0a0a7fc436df`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 116.3 MB (116275156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:6c6003e890c75c9136df06b9061afbbf9a70673711d2d9abc5937ca7f01abb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1405b33f9d954b9962af09c3e8f8b69feb900cd917e7b24f9c3ca8d79dcf5dc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90fdf60dd2cdaa8631b8f2fe6906033728268064e21b9973ac341c2dce9bdd2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:21 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:52:37 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:52:37 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:52:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:52:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcf18532b0b5fe4037c5643568f1d179ff345d7055a7ac8a71d63d1358e919c`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024503fd6dce42f3b55a864c14a052cd01a6bc282c4bf992fee6ef4ba23cdf4`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79e7641645bdde609e308b0dc0cc7d3ed00f75229dfb351f7fdf838879ec17`  
		Last Modified: Tue, 21 Nov 2023 19:54:29 GMT  
		Size: 116.4 MB (116381803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4dfad0cf1fc9f49cd246d745c8e60de2655f5958cc9cf12c168ed9d89185412e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb3d9da9e8ef38511b9955ba39428d12508f08cfafd8120af33d7cb05c93a8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:02:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:02:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:02:50 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:02:50 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:02:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:02:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed5153b386f9e459da48369f426fafcc7640cc04e0a93a1b51328c28016de09`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac447c42fc4123607bbba8b0d6039aebd3f7398430097e791c6e733e6aef7e13`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584e8c85115b60c19fc0c86c9bc644df5aa9461a6c2d48b21b3d0a0a7fc436df`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 116.3 MB (116275156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:7472e567239d6a2a3da0450135f18f439fb4fc1abe59c039c611bdf4681d8142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:ffa86c498495b1ed5c501db9ca22defa663573c996f73ceef3eb92cf06abf3b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303341461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc2bfb0891e8061604d52a1cc878b4170d149315006b25379f6299f1d63ff18`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Fri, 17 Nov 2023 04:07:36 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 04:07:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 04:07:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 04:07:37 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 04:07:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 04:07:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 04:07:41 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 04:07:41 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 04:07:41 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 04:07:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 04:07:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6252a3f696c27e59620b16d1002af23ef0a40c8379f9957e254e1c02b95be`  
		Last Modified: Fri, 17 Nov 2023 04:08:34 GMT  
		Size: 6.5 MB (6544950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d35315ff9cc6a58482ae3f04b4732bd85c1fb30a74b31bb68ea4efb7ac2a6c5`  
		Last Modified: Fri, 17 Nov 2023 04:08:33 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c1f45a0d680b445efacdae46d73f96fbee53649dd61e639f27c8ae65e04e9d`  
		Last Modified: Fri, 17 Nov 2023 04:08:40 GMT  
		Size: 112.6 MB (112571479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7828db1f899fd05a3a2fe026d47abb438cc26944b44ec03e2eca452ec6bbb755
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300449561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae5c1f7bcc0eef0555b1bc653a835c0742b9c591366d7364aefa9b7d867c237`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Fri, 17 Nov 2023 03:24:30 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 03:24:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 03:24:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 03:24:31 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 03:24:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 03:24:39 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 03:24:39 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 03:24:39 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 03:24:39 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 03:24:39 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 03:24:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a28d21be43245d925141d42098fe24b55b3e7bd4559cfd1cd9e91847c2dde`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 6.5 MB (6504026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc83fde0c0c3f7884cacc90c1c1ec1d4c0238afa611ce8d677c725acf33b51d`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ea211f3e78a618283203986e7ca5eee92d496eb81f936aafd33d22c1416ebb`  
		Last Modified: Fri, 17 Nov 2023 03:25:40 GMT  
		Size: 112.6 MB (112571515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:d02442781ac8eb24269962ae3b98d3d6c8f2c87bec04c9d493d38f0792aafcff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:a0a73992903a72392d1af2a83891ee4d0fae72ff107b5bf38cc99960dd461284
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564093527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa18f1a8990c2b44ded7f75640d04009d50c80fff83da25361406eb89ab729f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:41 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:59 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:53:00 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:53:00 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:53:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:53:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3cc9d3b549e34d2cb640568660d507b6bf5e6e04544338d0acbd3a61bea75f`  
		Last Modified: Tue, 21 Nov 2023 19:55:26 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4508e6f66f1395a0e42b885df9b3c30c60cd08dd8b06c922809e68f90a67827e`  
		Last Modified: Tue, 21 Nov 2023 19:55:26 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba7fc86877801886afc13370554e8aa83f85e4aa728d56bb6f9362288af09ea`  
		Last Modified: Tue, 21 Nov 2023 19:55:45 GMT  
		Size: 387.8 MB (387788526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9af44c40c5ba0c52c8fc3e74be80a141bf057ad7ce6456a1bdb3b78fdf891003
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.4 MB (561439235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898e64f4f1512971802863391144b7bb2ce8cdf3ff8452b79c345f252980d55e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:55 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:03:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:03:24 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:03:24 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:03:24 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:03:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:03:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed5118a32f8c2fe3869d9d1f74aef21fe22406e66b958cfc93783a179ed4742`  
		Last Modified: Tue, 21 Nov 2023 09:05:11 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c73e0a87bc638caf7d585b09b75e7ec3a733b2966c3671d5582fc16167bfffd`  
		Last Modified: Tue, 21 Nov 2023 09:05:11 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7cdd3753c6429fc0c39100f9f2889e868628f693f9fb4430bd6b0c5b887e44`  
		Last Modified: Tue, 21 Nov 2023 09:05:28 GMT  
		Size: 387.7 MB (387680091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:d02442781ac8eb24269962ae3b98d3d6c8f2c87bec04c9d493d38f0792aafcff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a0a73992903a72392d1af2a83891ee4d0fae72ff107b5bf38cc99960dd461284
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564093527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa18f1a8990c2b44ded7f75640d04009d50c80fff83da25361406eb89ab729f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:41 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:59 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:53:00 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:53:00 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:53:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:53:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3cc9d3b549e34d2cb640568660d507b6bf5e6e04544338d0acbd3a61bea75f`  
		Last Modified: Tue, 21 Nov 2023 19:55:26 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4508e6f66f1395a0e42b885df9b3c30c60cd08dd8b06c922809e68f90a67827e`  
		Last Modified: Tue, 21 Nov 2023 19:55:26 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba7fc86877801886afc13370554e8aa83f85e4aa728d56bb6f9362288af09ea`  
		Last Modified: Tue, 21 Nov 2023 19:55:45 GMT  
		Size: 387.8 MB (387788526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9af44c40c5ba0c52c8fc3e74be80a141bf057ad7ce6456a1bdb3b78fdf891003
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.4 MB (561439235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898e64f4f1512971802863391144b7bb2ce8cdf3ff8452b79c345f252980d55e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:55 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:03:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:03:24 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:03:24 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:03:24 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:03:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:03:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed5118a32f8c2fe3869d9d1f74aef21fe22406e66b958cfc93783a179ed4742`  
		Last Modified: Tue, 21 Nov 2023 09:05:11 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c73e0a87bc638caf7d585b09b75e7ec3a733b2966c3671d5582fc16167bfffd`  
		Last Modified: Tue, 21 Nov 2023 09:05:11 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7cdd3753c6429fc0c39100f9f2889e868628f693f9fb4430bd6b0c5b887e44`  
		Last Modified: Tue, 21 Nov 2023 09:05:28 GMT  
		Size: 387.7 MB (387680091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:a2a70251e1b3301223a12038044a77cb69d779d26de36636070629817ae14097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:fae3189d39d01bc069a01cfda97c2cd8bfd31e26b7f0ced74a4bd981dde162f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574748162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de61bb8b8729a83ea95dd5ed02687e79378aacc1f01ae7ff9b410733f638792d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Fri, 17 Nov 2023 04:07:36 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 04:07:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 04:07:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 04:07:45 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 04:07:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 04:07:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 04:07:58 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 04:07:58 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 04:07:59 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 04:07:59 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 04:07:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6252a3f696c27e59620b16d1002af23ef0a40c8379f9957e254e1c02b95be`  
		Last Modified: Fri, 17 Nov 2023 04:08:34 GMT  
		Size: 6.5 MB (6544950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75292d19b6ada0fcf335d32c496f9f7829bfbcd1f356b1bf5bc86ad9a9ac7962`  
		Last Modified: Fri, 17 Nov 2023 04:09:04 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d36c2caa4fefccc3fdce485e834a44f88157e4400a7c95c61a4a2bd5b20351`  
		Last Modified: Fri, 17 Nov 2023 04:09:19 GMT  
		Size: 384.0 MB (383978181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:51a1d4b0c1d0c87f687fb99f20d080e62c900be82e1360482b3c3d7a697d6a8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.9 MB (571856232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa097175b9839a4a175639fdbb1beaeb57c7fce54e3eab45d5d6448d81e9ccf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Fri, 17 Nov 2023 03:24:30 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 03:24:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 03:24:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 03:24:48 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 03:24:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 03:25:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 03:25:00 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 03:25:01 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 03:25:01 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 03:25:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 03:25:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a28d21be43245d925141d42098fe24b55b3e7bd4559cfd1cd9e91847c2dde`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 6.5 MB (6504026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8afe0f1f1a01988b2e5b24f9e1098e5cd45b2530f7dcf74d2f3d03965cb9470`  
		Last Modified: Fri, 17 Nov 2023 03:26:05 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a154f9e3b2395a9b9803f698016c62421aecbae7a191723ea7bf25cf6c19c794`  
		Last Modified: Fri, 17 Nov 2023 03:26:20 GMT  
		Size: 384.0 MB (383978188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:7472e567239d6a2a3da0450135f18f439fb4fc1abe59c039c611bdf4681d8142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:ffa86c498495b1ed5c501db9ca22defa663573c996f73ceef3eb92cf06abf3b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303341461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc2bfb0891e8061604d52a1cc878b4170d149315006b25379f6299f1d63ff18`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Fri, 17 Nov 2023 04:07:36 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 04:07:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 04:07:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 04:07:37 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 04:07:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 04:07:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 04:07:41 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 04:07:41 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 04:07:41 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 04:07:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 04:07:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6252a3f696c27e59620b16d1002af23ef0a40c8379f9957e254e1c02b95be`  
		Last Modified: Fri, 17 Nov 2023 04:08:34 GMT  
		Size: 6.5 MB (6544950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d35315ff9cc6a58482ae3f04b4732bd85c1fb30a74b31bb68ea4efb7ac2a6c5`  
		Last Modified: Fri, 17 Nov 2023 04:08:33 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c1f45a0d680b445efacdae46d73f96fbee53649dd61e639f27c8ae65e04e9d`  
		Last Modified: Fri, 17 Nov 2023 04:08:40 GMT  
		Size: 112.6 MB (112571479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7828db1f899fd05a3a2fe026d47abb438cc26944b44ec03e2eca452ec6bbb755
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300449561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae5c1f7bcc0eef0555b1bc653a835c0742b9c591366d7364aefa9b7d867c237`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Fri, 17 Nov 2023 03:24:30 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 03:24:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 03:24:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 03:24:31 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 03:24:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 03:24:39 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 03:24:39 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 03:24:39 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 03:24:39 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 03:24:39 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 03:24:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a28d21be43245d925141d42098fe24b55b3e7bd4559cfd1cd9e91847c2dde`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 6.5 MB (6504026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc83fde0c0c3f7884cacc90c1c1ec1d4c0238afa611ce8d677c725acf33b51d`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ea211f3e78a618283203986e7ca5eee92d496eb81f936aafd33d22c1416ebb`  
		Last Modified: Fri, 17 Nov 2023 03:25:40 GMT  
		Size: 112.6 MB (112571515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13`

```console
$ docker pull neo4j@sha256:6c6003e890c75c9136df06b9061afbbf9a70673711d2d9abc5937ca7f01abb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13` - linux; amd64

```console
$ docker pull neo4j@sha256:1405b33f9d954b9962af09c3e8f8b69feb900cd917e7b24f9c3ca8d79dcf5dc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90fdf60dd2cdaa8631b8f2fe6906033728268064e21b9973ac341c2dce9bdd2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:21 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:52:37 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:52:37 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:52:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:52:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcf18532b0b5fe4037c5643568f1d179ff345d7055a7ac8a71d63d1358e919c`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024503fd6dce42f3b55a864c14a052cd01a6bc282c4bf992fee6ef4ba23cdf4`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79e7641645bdde609e308b0dc0cc7d3ed00f75229dfb351f7fdf838879ec17`  
		Last Modified: Tue, 21 Nov 2023 19:54:29 GMT  
		Size: 116.4 MB (116381803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4dfad0cf1fc9f49cd246d745c8e60de2655f5958cc9cf12c168ed9d89185412e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb3d9da9e8ef38511b9955ba39428d12508f08cfafd8120af33d7cb05c93a8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:02:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:02:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:02:50 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:02:50 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:02:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:02:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed5153b386f9e459da48369f426fafcc7640cc04e0a93a1b51328c28016de09`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac447c42fc4123607bbba8b0d6039aebd3f7398430097e791c6e733e6aef7e13`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584e8c85115b60c19fc0c86c9bc644df5aa9461a6c2d48b21b3d0a0a7fc436df`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 116.3 MB (116275156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-bullseye`

```console
$ docker pull neo4j@sha256:6c6003e890c75c9136df06b9061afbbf9a70673711d2d9abc5937ca7f01abb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1405b33f9d954b9962af09c3e8f8b69feb900cd917e7b24f9c3ca8d79dcf5dc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90fdf60dd2cdaa8631b8f2fe6906033728268064e21b9973ac341c2dce9bdd2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:21 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:52:37 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:52:37 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:52:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:52:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcf18532b0b5fe4037c5643568f1d179ff345d7055a7ac8a71d63d1358e919c`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024503fd6dce42f3b55a864c14a052cd01a6bc282c4bf992fee6ef4ba23cdf4`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79e7641645bdde609e308b0dc0cc7d3ed00f75229dfb351f7fdf838879ec17`  
		Last Modified: Tue, 21 Nov 2023 19:54:29 GMT  
		Size: 116.4 MB (116381803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4dfad0cf1fc9f49cd246d745c8e60de2655f5958cc9cf12c168ed9d89185412e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb3d9da9e8ef38511b9955ba39428d12508f08cfafd8120af33d7cb05c93a8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:02:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:02:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:02:50 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:02:50 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:02:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:02:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed5153b386f9e459da48369f426fafcc7640cc04e0a93a1b51328c28016de09`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac447c42fc4123607bbba8b0d6039aebd3f7398430097e791c6e733e6aef7e13`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584e8c85115b60c19fc0c86c9bc644df5aa9461a6c2d48b21b3d0a0a7fc436df`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 116.3 MB (116275156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-community`

```console
$ docker pull neo4j@sha256:6c6003e890c75c9136df06b9061afbbf9a70673711d2d9abc5937ca7f01abb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-community` - linux; amd64

```console
$ docker pull neo4j@sha256:1405b33f9d954b9962af09c3e8f8b69feb900cd917e7b24f9c3ca8d79dcf5dc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90fdf60dd2cdaa8631b8f2fe6906033728268064e21b9973ac341c2dce9bdd2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:21 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:52:37 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:52:37 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:52:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:52:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcf18532b0b5fe4037c5643568f1d179ff345d7055a7ac8a71d63d1358e919c`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024503fd6dce42f3b55a864c14a052cd01a6bc282c4bf992fee6ef4ba23cdf4`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79e7641645bdde609e308b0dc0cc7d3ed00f75229dfb351f7fdf838879ec17`  
		Last Modified: Tue, 21 Nov 2023 19:54:29 GMT  
		Size: 116.4 MB (116381803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4dfad0cf1fc9f49cd246d745c8e60de2655f5958cc9cf12c168ed9d89185412e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb3d9da9e8ef38511b9955ba39428d12508f08cfafd8120af33d7cb05c93a8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:02:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:02:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:02:50 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:02:50 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:02:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:02:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed5153b386f9e459da48369f426fafcc7640cc04e0a93a1b51328c28016de09`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac447c42fc4123607bbba8b0d6039aebd3f7398430097e791c6e733e6aef7e13`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584e8c85115b60c19fc0c86c9bc644df5aa9461a6c2d48b21b3d0a0a7fc436df`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 116.3 MB (116275156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-community-bullseye`

```console
$ docker pull neo4j@sha256:6c6003e890c75c9136df06b9061afbbf9a70673711d2d9abc5937ca7f01abb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1405b33f9d954b9962af09c3e8f8b69feb900cd917e7b24f9c3ca8d79dcf5dc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90fdf60dd2cdaa8631b8f2fe6906033728268064e21b9973ac341c2dce9bdd2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:21 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:52:37 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:52:37 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:52:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:52:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcf18532b0b5fe4037c5643568f1d179ff345d7055a7ac8a71d63d1358e919c`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024503fd6dce42f3b55a864c14a052cd01a6bc282c4bf992fee6ef4ba23cdf4`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79e7641645bdde609e308b0dc0cc7d3ed00f75229dfb351f7fdf838879ec17`  
		Last Modified: Tue, 21 Nov 2023 19:54:29 GMT  
		Size: 116.4 MB (116381803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4dfad0cf1fc9f49cd246d745c8e60de2655f5958cc9cf12c168ed9d89185412e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb3d9da9e8ef38511b9955ba39428d12508f08cfafd8120af33d7cb05c93a8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:02:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:02:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:02:50 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:02:50 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:02:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:02:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed5153b386f9e459da48369f426fafcc7640cc04e0a93a1b51328c28016de09`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac447c42fc4123607bbba8b0d6039aebd3f7398430097e791c6e733e6aef7e13`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584e8c85115b60c19fc0c86c9bc644df5aa9461a6c2d48b21b3d0a0a7fc436df`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 116.3 MB (116275156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-community-ubi8`

```console
$ docker pull neo4j@sha256:7472e567239d6a2a3da0450135f18f439fb4fc1abe59c039c611bdf4681d8142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:ffa86c498495b1ed5c501db9ca22defa663573c996f73ceef3eb92cf06abf3b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303341461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc2bfb0891e8061604d52a1cc878b4170d149315006b25379f6299f1d63ff18`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Fri, 17 Nov 2023 04:07:36 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 04:07:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 04:07:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 04:07:37 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 04:07:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 04:07:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 04:07:41 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 04:07:41 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 04:07:41 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 04:07:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 04:07:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6252a3f696c27e59620b16d1002af23ef0a40c8379f9957e254e1c02b95be`  
		Last Modified: Fri, 17 Nov 2023 04:08:34 GMT  
		Size: 6.5 MB (6544950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d35315ff9cc6a58482ae3f04b4732bd85c1fb30a74b31bb68ea4efb7ac2a6c5`  
		Last Modified: Fri, 17 Nov 2023 04:08:33 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c1f45a0d680b445efacdae46d73f96fbee53649dd61e639f27c8ae65e04e9d`  
		Last Modified: Fri, 17 Nov 2023 04:08:40 GMT  
		Size: 112.6 MB (112571479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7828db1f899fd05a3a2fe026d47abb438cc26944b44ec03e2eca452ec6bbb755
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300449561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae5c1f7bcc0eef0555b1bc653a835c0742b9c591366d7364aefa9b7d867c237`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Fri, 17 Nov 2023 03:24:30 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 03:24:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 03:24:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 03:24:31 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 03:24:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 03:24:39 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 03:24:39 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 03:24:39 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 03:24:39 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 03:24:39 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 03:24:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a28d21be43245d925141d42098fe24b55b3e7bd4559cfd1cd9e91847c2dde`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 6.5 MB (6504026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc83fde0c0c3f7884cacc90c1c1ec1d4c0238afa611ce8d677c725acf33b51d`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ea211f3e78a618283203986e7ca5eee92d496eb81f936aafd33d22c1416ebb`  
		Last Modified: Fri, 17 Nov 2023 03:25:40 GMT  
		Size: 112.6 MB (112571515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-enterprise`

```console
$ docker pull neo4j@sha256:d02442781ac8eb24269962ae3b98d3d6c8f2c87bec04c9d493d38f0792aafcff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:a0a73992903a72392d1af2a83891ee4d0fae72ff107b5bf38cc99960dd461284
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564093527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa18f1a8990c2b44ded7f75640d04009d50c80fff83da25361406eb89ab729f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:41 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:59 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:53:00 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:53:00 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:53:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:53:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3cc9d3b549e34d2cb640568660d507b6bf5e6e04544338d0acbd3a61bea75f`  
		Last Modified: Tue, 21 Nov 2023 19:55:26 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4508e6f66f1395a0e42b885df9b3c30c60cd08dd8b06c922809e68f90a67827e`  
		Last Modified: Tue, 21 Nov 2023 19:55:26 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba7fc86877801886afc13370554e8aa83f85e4aa728d56bb6f9362288af09ea`  
		Last Modified: Tue, 21 Nov 2023 19:55:45 GMT  
		Size: 387.8 MB (387788526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9af44c40c5ba0c52c8fc3e74be80a141bf057ad7ce6456a1bdb3b78fdf891003
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.4 MB (561439235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898e64f4f1512971802863391144b7bb2ce8cdf3ff8452b79c345f252980d55e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:55 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:03:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:03:24 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:03:24 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:03:24 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:03:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:03:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed5118a32f8c2fe3869d9d1f74aef21fe22406e66b958cfc93783a179ed4742`  
		Last Modified: Tue, 21 Nov 2023 09:05:11 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c73e0a87bc638caf7d585b09b75e7ec3a733b2966c3671d5582fc16167bfffd`  
		Last Modified: Tue, 21 Nov 2023 09:05:11 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7cdd3753c6429fc0c39100f9f2889e868628f693f9fb4430bd6b0c5b887e44`  
		Last Modified: Tue, 21 Nov 2023 09:05:28 GMT  
		Size: 387.7 MB (387680091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:d02442781ac8eb24269962ae3b98d3d6c8f2c87bec04c9d493d38f0792aafcff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a0a73992903a72392d1af2a83891ee4d0fae72ff107b5bf38cc99960dd461284
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564093527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa18f1a8990c2b44ded7f75640d04009d50c80fff83da25361406eb89ab729f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:41 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:59 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:53:00 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:53:00 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:53:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:53:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3cc9d3b549e34d2cb640568660d507b6bf5e6e04544338d0acbd3a61bea75f`  
		Last Modified: Tue, 21 Nov 2023 19:55:26 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4508e6f66f1395a0e42b885df9b3c30c60cd08dd8b06c922809e68f90a67827e`  
		Last Modified: Tue, 21 Nov 2023 19:55:26 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba7fc86877801886afc13370554e8aa83f85e4aa728d56bb6f9362288af09ea`  
		Last Modified: Tue, 21 Nov 2023 19:55:45 GMT  
		Size: 387.8 MB (387788526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9af44c40c5ba0c52c8fc3e74be80a141bf057ad7ce6456a1bdb3b78fdf891003
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.4 MB (561439235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898e64f4f1512971802863391144b7bb2ce8cdf3ff8452b79c345f252980d55e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:55 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:03:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:03:24 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:03:24 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:03:24 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:03:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:03:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed5118a32f8c2fe3869d9d1f74aef21fe22406e66b958cfc93783a179ed4742`  
		Last Modified: Tue, 21 Nov 2023 09:05:11 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c73e0a87bc638caf7d585b09b75e7ec3a733b2966c3671d5582fc16167bfffd`  
		Last Modified: Tue, 21 Nov 2023 09:05:11 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7cdd3753c6429fc0c39100f9f2889e868628f693f9fb4430bd6b0c5b887e44`  
		Last Modified: Tue, 21 Nov 2023 09:05:28 GMT  
		Size: 387.7 MB (387680091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:a2a70251e1b3301223a12038044a77cb69d779d26de36636070629817ae14097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:fae3189d39d01bc069a01cfda97c2cd8bfd31e26b7f0ced74a4bd981dde162f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574748162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de61bb8b8729a83ea95dd5ed02687e79378aacc1f01ae7ff9b410733f638792d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Fri, 17 Nov 2023 04:07:36 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 04:07:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 04:07:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 04:07:45 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 04:07:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 04:07:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 04:07:58 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 04:07:58 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 04:07:59 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 04:07:59 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 04:07:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6252a3f696c27e59620b16d1002af23ef0a40c8379f9957e254e1c02b95be`  
		Last Modified: Fri, 17 Nov 2023 04:08:34 GMT  
		Size: 6.5 MB (6544950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75292d19b6ada0fcf335d32c496f9f7829bfbcd1f356b1bf5bc86ad9a9ac7962`  
		Last Modified: Fri, 17 Nov 2023 04:09:04 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d36c2caa4fefccc3fdce485e834a44f88157e4400a7c95c61a4a2bd5b20351`  
		Last Modified: Fri, 17 Nov 2023 04:09:19 GMT  
		Size: 384.0 MB (383978181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:51a1d4b0c1d0c87f687fb99f20d080e62c900be82e1360482b3c3d7a697d6a8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.9 MB (571856232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa097175b9839a4a175639fdbb1beaeb57c7fce54e3eab45d5d6448d81e9ccf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Fri, 17 Nov 2023 03:24:30 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 03:24:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 03:24:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 03:24:48 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 03:24:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 03:25:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 03:25:00 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 03:25:01 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 03:25:01 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 03:25:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 03:25:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a28d21be43245d925141d42098fe24b55b3e7bd4559cfd1cd9e91847c2dde`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 6.5 MB (6504026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8afe0f1f1a01988b2e5b24f9e1098e5cd45b2530f7dcf74d2f3d03965cb9470`  
		Last Modified: Fri, 17 Nov 2023 03:26:05 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a154f9e3b2395a9b9803f698016c62421aecbae7a191723ea7bf25cf6c19c794`  
		Last Modified: Fri, 17 Nov 2023 03:26:20 GMT  
		Size: 384.0 MB (383978188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-ubi8`

```console
$ docker pull neo4j@sha256:7472e567239d6a2a3da0450135f18f439fb4fc1abe59c039c611bdf4681d8142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:ffa86c498495b1ed5c501db9ca22defa663573c996f73ceef3eb92cf06abf3b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303341461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc2bfb0891e8061604d52a1cc878b4170d149315006b25379f6299f1d63ff18`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Fri, 17 Nov 2023 04:07:36 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 04:07:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 04:07:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 04:07:37 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 04:07:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 04:07:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 04:07:41 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 04:07:41 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 04:07:41 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 04:07:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 04:07:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6252a3f696c27e59620b16d1002af23ef0a40c8379f9957e254e1c02b95be`  
		Last Modified: Fri, 17 Nov 2023 04:08:34 GMT  
		Size: 6.5 MB (6544950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d35315ff9cc6a58482ae3f04b4732bd85c1fb30a74b31bb68ea4efb7ac2a6c5`  
		Last Modified: Fri, 17 Nov 2023 04:08:33 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c1f45a0d680b445efacdae46d73f96fbee53649dd61e639f27c8ae65e04e9d`  
		Last Modified: Fri, 17 Nov 2023 04:08:40 GMT  
		Size: 112.6 MB (112571479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7828db1f899fd05a3a2fe026d47abb438cc26944b44ec03e2eca452ec6bbb755
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300449561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae5c1f7bcc0eef0555b1bc653a835c0742b9c591366d7364aefa9b7d867c237`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Fri, 17 Nov 2023 03:24:30 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 03:24:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 03:24:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 03:24:31 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 03:24:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 03:24:39 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 03:24:39 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 03:24:39 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 03:24:39 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 03:24:39 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 03:24:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a28d21be43245d925141d42098fe24b55b3e7bd4559cfd1cd9e91847c2dde`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 6.5 MB (6504026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc83fde0c0c3f7884cacc90c1c1ec1d4c0238afa611ce8d677c725acf33b51d`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ea211f3e78a618283203986e7ca5eee92d496eb81f936aafd33d22c1416ebb`  
		Last Modified: Fri, 17 Nov 2023 03:25:40 GMT  
		Size: 112.6 MB (112571515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0`

```console
$ docker pull neo4j@sha256:6c6003e890c75c9136df06b9061afbbf9a70673711d2d9abc5937ca7f01abb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0` - linux; amd64

```console
$ docker pull neo4j@sha256:1405b33f9d954b9962af09c3e8f8b69feb900cd917e7b24f9c3ca8d79dcf5dc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90fdf60dd2cdaa8631b8f2fe6906033728268064e21b9973ac341c2dce9bdd2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:21 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:52:37 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:52:37 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:52:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:52:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcf18532b0b5fe4037c5643568f1d179ff345d7055a7ac8a71d63d1358e919c`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024503fd6dce42f3b55a864c14a052cd01a6bc282c4bf992fee6ef4ba23cdf4`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79e7641645bdde609e308b0dc0cc7d3ed00f75229dfb351f7fdf838879ec17`  
		Last Modified: Tue, 21 Nov 2023 19:54:29 GMT  
		Size: 116.4 MB (116381803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4dfad0cf1fc9f49cd246d745c8e60de2655f5958cc9cf12c168ed9d89185412e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb3d9da9e8ef38511b9955ba39428d12508f08cfafd8120af33d7cb05c93a8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:02:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:02:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:02:50 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:02:50 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:02:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:02:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed5153b386f9e459da48369f426fafcc7640cc04e0a93a1b51328c28016de09`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac447c42fc4123607bbba8b0d6039aebd3f7398430097e791c6e733e6aef7e13`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584e8c85115b60c19fc0c86c9bc644df5aa9461a6c2d48b21b3d0a0a7fc436df`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 116.3 MB (116275156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-bullseye`

```console
$ docker pull neo4j@sha256:6c6003e890c75c9136df06b9061afbbf9a70673711d2d9abc5937ca7f01abb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1405b33f9d954b9962af09c3e8f8b69feb900cd917e7b24f9c3ca8d79dcf5dc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90fdf60dd2cdaa8631b8f2fe6906033728268064e21b9973ac341c2dce9bdd2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:21 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:52:37 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:52:37 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:52:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:52:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcf18532b0b5fe4037c5643568f1d179ff345d7055a7ac8a71d63d1358e919c`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024503fd6dce42f3b55a864c14a052cd01a6bc282c4bf992fee6ef4ba23cdf4`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79e7641645bdde609e308b0dc0cc7d3ed00f75229dfb351f7fdf838879ec17`  
		Last Modified: Tue, 21 Nov 2023 19:54:29 GMT  
		Size: 116.4 MB (116381803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4dfad0cf1fc9f49cd246d745c8e60de2655f5958cc9cf12c168ed9d89185412e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb3d9da9e8ef38511b9955ba39428d12508f08cfafd8120af33d7cb05c93a8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:02:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:02:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:02:50 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:02:50 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:02:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:02:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed5153b386f9e459da48369f426fafcc7640cc04e0a93a1b51328c28016de09`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac447c42fc4123607bbba8b0d6039aebd3f7398430097e791c6e733e6aef7e13`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584e8c85115b60c19fc0c86c9bc644df5aa9461a6c2d48b21b3d0a0a7fc436df`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 116.3 MB (116275156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-community`

```console
$ docker pull neo4j@sha256:6c6003e890c75c9136df06b9061afbbf9a70673711d2d9abc5937ca7f01abb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:1405b33f9d954b9962af09c3e8f8b69feb900cd917e7b24f9c3ca8d79dcf5dc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90fdf60dd2cdaa8631b8f2fe6906033728268064e21b9973ac341c2dce9bdd2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:21 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:52:37 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:52:37 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:52:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:52:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcf18532b0b5fe4037c5643568f1d179ff345d7055a7ac8a71d63d1358e919c`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024503fd6dce42f3b55a864c14a052cd01a6bc282c4bf992fee6ef4ba23cdf4`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79e7641645bdde609e308b0dc0cc7d3ed00f75229dfb351f7fdf838879ec17`  
		Last Modified: Tue, 21 Nov 2023 19:54:29 GMT  
		Size: 116.4 MB (116381803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4dfad0cf1fc9f49cd246d745c8e60de2655f5958cc9cf12c168ed9d89185412e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb3d9da9e8ef38511b9955ba39428d12508f08cfafd8120af33d7cb05c93a8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:02:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:02:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:02:50 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:02:50 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:02:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:02:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed5153b386f9e459da48369f426fafcc7640cc04e0a93a1b51328c28016de09`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac447c42fc4123607bbba8b0d6039aebd3f7398430097e791c6e733e6aef7e13`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584e8c85115b60c19fc0c86c9bc644df5aa9461a6c2d48b21b3d0a0a7fc436df`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 116.3 MB (116275156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-community-bullseye`

```console
$ docker pull neo4j@sha256:6c6003e890c75c9136df06b9061afbbf9a70673711d2d9abc5937ca7f01abb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1405b33f9d954b9962af09c3e8f8b69feb900cd917e7b24f9c3ca8d79dcf5dc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90fdf60dd2cdaa8631b8f2fe6906033728268064e21b9973ac341c2dce9bdd2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:21 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:52:37 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:52:37 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:52:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:52:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcf18532b0b5fe4037c5643568f1d179ff345d7055a7ac8a71d63d1358e919c`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024503fd6dce42f3b55a864c14a052cd01a6bc282c4bf992fee6ef4ba23cdf4`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79e7641645bdde609e308b0dc0cc7d3ed00f75229dfb351f7fdf838879ec17`  
		Last Modified: Tue, 21 Nov 2023 19:54:29 GMT  
		Size: 116.4 MB (116381803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4dfad0cf1fc9f49cd246d745c8e60de2655f5958cc9cf12c168ed9d89185412e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb3d9da9e8ef38511b9955ba39428d12508f08cfafd8120af33d7cb05c93a8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:02:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:02:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:02:50 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:02:50 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:02:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:02:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed5153b386f9e459da48369f426fafcc7640cc04e0a93a1b51328c28016de09`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac447c42fc4123607bbba8b0d6039aebd3f7398430097e791c6e733e6aef7e13`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584e8c85115b60c19fc0c86c9bc644df5aa9461a6c2d48b21b3d0a0a7fc436df`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 116.3 MB (116275156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-community-ubi8`

```console
$ docker pull neo4j@sha256:7472e567239d6a2a3da0450135f18f439fb4fc1abe59c039c611bdf4681d8142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:ffa86c498495b1ed5c501db9ca22defa663573c996f73ceef3eb92cf06abf3b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303341461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc2bfb0891e8061604d52a1cc878b4170d149315006b25379f6299f1d63ff18`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Fri, 17 Nov 2023 04:07:36 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 04:07:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 04:07:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 04:07:37 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 04:07:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 04:07:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 04:07:41 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 04:07:41 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 04:07:41 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 04:07:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 04:07:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6252a3f696c27e59620b16d1002af23ef0a40c8379f9957e254e1c02b95be`  
		Last Modified: Fri, 17 Nov 2023 04:08:34 GMT  
		Size: 6.5 MB (6544950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d35315ff9cc6a58482ae3f04b4732bd85c1fb30a74b31bb68ea4efb7ac2a6c5`  
		Last Modified: Fri, 17 Nov 2023 04:08:33 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c1f45a0d680b445efacdae46d73f96fbee53649dd61e639f27c8ae65e04e9d`  
		Last Modified: Fri, 17 Nov 2023 04:08:40 GMT  
		Size: 112.6 MB (112571479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7828db1f899fd05a3a2fe026d47abb438cc26944b44ec03e2eca452ec6bbb755
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300449561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae5c1f7bcc0eef0555b1bc653a835c0742b9c591366d7364aefa9b7d867c237`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Fri, 17 Nov 2023 03:24:30 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 03:24:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 03:24:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 03:24:31 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 03:24:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 03:24:39 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 03:24:39 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 03:24:39 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 03:24:39 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 03:24:39 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 03:24:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a28d21be43245d925141d42098fe24b55b3e7bd4559cfd1cd9e91847c2dde`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 6.5 MB (6504026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc83fde0c0c3f7884cacc90c1c1ec1d4c0238afa611ce8d677c725acf33b51d`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ea211f3e78a618283203986e7ca5eee92d496eb81f936aafd33d22c1416ebb`  
		Last Modified: Fri, 17 Nov 2023 03:25:40 GMT  
		Size: 112.6 MB (112571515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-enterprise`

```console
$ docker pull neo4j@sha256:d02442781ac8eb24269962ae3b98d3d6c8f2c87bec04c9d493d38f0792aafcff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:a0a73992903a72392d1af2a83891ee4d0fae72ff107b5bf38cc99960dd461284
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564093527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa18f1a8990c2b44ded7f75640d04009d50c80fff83da25361406eb89ab729f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:41 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:59 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:53:00 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:53:00 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:53:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:53:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3cc9d3b549e34d2cb640568660d507b6bf5e6e04544338d0acbd3a61bea75f`  
		Last Modified: Tue, 21 Nov 2023 19:55:26 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4508e6f66f1395a0e42b885df9b3c30c60cd08dd8b06c922809e68f90a67827e`  
		Last Modified: Tue, 21 Nov 2023 19:55:26 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba7fc86877801886afc13370554e8aa83f85e4aa728d56bb6f9362288af09ea`  
		Last Modified: Tue, 21 Nov 2023 19:55:45 GMT  
		Size: 387.8 MB (387788526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9af44c40c5ba0c52c8fc3e74be80a141bf057ad7ce6456a1bdb3b78fdf891003
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.4 MB (561439235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898e64f4f1512971802863391144b7bb2ce8cdf3ff8452b79c345f252980d55e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:55 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:03:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:03:24 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:03:24 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:03:24 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:03:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:03:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed5118a32f8c2fe3869d9d1f74aef21fe22406e66b958cfc93783a179ed4742`  
		Last Modified: Tue, 21 Nov 2023 09:05:11 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c73e0a87bc638caf7d585b09b75e7ec3a733b2966c3671d5582fc16167bfffd`  
		Last Modified: Tue, 21 Nov 2023 09:05:11 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7cdd3753c6429fc0c39100f9f2889e868628f693f9fb4430bd6b0c5b887e44`  
		Last Modified: Tue, 21 Nov 2023 09:05:28 GMT  
		Size: 387.7 MB (387680091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:d02442781ac8eb24269962ae3b98d3d6c8f2c87bec04c9d493d38f0792aafcff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a0a73992903a72392d1af2a83891ee4d0fae72ff107b5bf38cc99960dd461284
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564093527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa18f1a8990c2b44ded7f75640d04009d50c80fff83da25361406eb89ab729f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:41 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:59 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:53:00 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:53:00 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:53:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:53:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3cc9d3b549e34d2cb640568660d507b6bf5e6e04544338d0acbd3a61bea75f`  
		Last Modified: Tue, 21 Nov 2023 19:55:26 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4508e6f66f1395a0e42b885df9b3c30c60cd08dd8b06c922809e68f90a67827e`  
		Last Modified: Tue, 21 Nov 2023 19:55:26 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba7fc86877801886afc13370554e8aa83f85e4aa728d56bb6f9362288af09ea`  
		Last Modified: Tue, 21 Nov 2023 19:55:45 GMT  
		Size: 387.8 MB (387788526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9af44c40c5ba0c52c8fc3e74be80a141bf057ad7ce6456a1bdb3b78fdf891003
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.4 MB (561439235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898e64f4f1512971802863391144b7bb2ce8cdf3ff8452b79c345f252980d55e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:55 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:03:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:03:24 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:03:24 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:03:24 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:03:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:03:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed5118a32f8c2fe3869d9d1f74aef21fe22406e66b958cfc93783a179ed4742`  
		Last Modified: Tue, 21 Nov 2023 09:05:11 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c73e0a87bc638caf7d585b09b75e7ec3a733b2966c3671d5582fc16167bfffd`  
		Last Modified: Tue, 21 Nov 2023 09:05:11 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7cdd3753c6429fc0c39100f9f2889e868628f693f9fb4430bd6b0c5b887e44`  
		Last Modified: Tue, 21 Nov 2023 09:05:28 GMT  
		Size: 387.7 MB (387680091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:a2a70251e1b3301223a12038044a77cb69d779d26de36636070629817ae14097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:fae3189d39d01bc069a01cfda97c2cd8bfd31e26b7f0ced74a4bd981dde162f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574748162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de61bb8b8729a83ea95dd5ed02687e79378aacc1f01ae7ff9b410733f638792d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Fri, 17 Nov 2023 04:07:36 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 04:07:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 04:07:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 04:07:45 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 04:07:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 04:07:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 04:07:58 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 04:07:58 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 04:07:59 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 04:07:59 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 04:07:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6252a3f696c27e59620b16d1002af23ef0a40c8379f9957e254e1c02b95be`  
		Last Modified: Fri, 17 Nov 2023 04:08:34 GMT  
		Size: 6.5 MB (6544950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75292d19b6ada0fcf335d32c496f9f7829bfbcd1f356b1bf5bc86ad9a9ac7962`  
		Last Modified: Fri, 17 Nov 2023 04:09:04 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d36c2caa4fefccc3fdce485e834a44f88157e4400a7c95c61a4a2bd5b20351`  
		Last Modified: Fri, 17 Nov 2023 04:09:19 GMT  
		Size: 384.0 MB (383978181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:51a1d4b0c1d0c87f687fb99f20d080e62c900be82e1360482b3c3d7a697d6a8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.9 MB (571856232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa097175b9839a4a175639fdbb1beaeb57c7fce54e3eab45d5d6448d81e9ccf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Fri, 17 Nov 2023 03:24:30 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 03:24:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 03:24:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 03:24:48 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 03:24:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 03:25:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 03:25:00 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 03:25:01 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 03:25:01 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 03:25:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 03:25:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a28d21be43245d925141d42098fe24b55b3e7bd4559cfd1cd9e91847c2dde`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 6.5 MB (6504026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8afe0f1f1a01988b2e5b24f9e1098e5cd45b2530f7dcf74d2f3d03965cb9470`  
		Last Modified: Fri, 17 Nov 2023 03:26:05 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a154f9e3b2395a9b9803f698016c62421aecbae7a191723ea7bf25cf6c19c794`  
		Last Modified: Fri, 17 Nov 2023 03:26:20 GMT  
		Size: 384.0 MB (383978188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-ubi8`

```console
$ docker pull neo4j@sha256:7472e567239d6a2a3da0450135f18f439fb4fc1abe59c039c611bdf4681d8142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:ffa86c498495b1ed5c501db9ca22defa663573c996f73ceef3eb92cf06abf3b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303341461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc2bfb0891e8061604d52a1cc878b4170d149315006b25379f6299f1d63ff18`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Fri, 17 Nov 2023 04:07:36 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 04:07:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 04:07:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 04:07:37 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 04:07:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 04:07:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 04:07:41 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 04:07:41 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 04:07:41 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 04:07:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 04:07:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6252a3f696c27e59620b16d1002af23ef0a40c8379f9957e254e1c02b95be`  
		Last Modified: Fri, 17 Nov 2023 04:08:34 GMT  
		Size: 6.5 MB (6544950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d35315ff9cc6a58482ae3f04b4732bd85c1fb30a74b31bb68ea4efb7ac2a6c5`  
		Last Modified: Fri, 17 Nov 2023 04:08:33 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c1f45a0d680b445efacdae46d73f96fbee53649dd61e639f27c8ae65e04e9d`  
		Last Modified: Fri, 17 Nov 2023 04:08:40 GMT  
		Size: 112.6 MB (112571479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7828db1f899fd05a3a2fe026d47abb438cc26944b44ec03e2eca452ec6bbb755
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300449561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae5c1f7bcc0eef0555b1bc653a835c0742b9c591366d7364aefa9b7d867c237`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Fri, 17 Nov 2023 03:24:30 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 03:24:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 03:24:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 03:24:31 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 03:24:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 03:24:39 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 03:24:39 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 03:24:39 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 03:24:39 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 03:24:39 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 03:24:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a28d21be43245d925141d42098fe24b55b3e7bd4559cfd1cd9e91847c2dde`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 6.5 MB (6504026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc83fde0c0c3f7884cacc90c1c1ec1d4c0238afa611ce8d677c725acf33b51d`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ea211f3e78a618283203986e7ca5eee92d496eb81f936aafd33d22c1416ebb`  
		Last Modified: Fri, 17 Nov 2023 03:25:40 GMT  
		Size: 112.6 MB (112571515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:6c6003e890c75c9136df06b9061afbbf9a70673711d2d9abc5937ca7f01abb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1405b33f9d954b9962af09c3e8f8b69feb900cd917e7b24f9c3ca8d79dcf5dc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90fdf60dd2cdaa8631b8f2fe6906033728268064e21b9973ac341c2dce9bdd2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:21 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:52:37 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:52:37 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:52:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:52:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcf18532b0b5fe4037c5643568f1d179ff345d7055a7ac8a71d63d1358e919c`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024503fd6dce42f3b55a864c14a052cd01a6bc282c4bf992fee6ef4ba23cdf4`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79e7641645bdde609e308b0dc0cc7d3ed00f75229dfb351f7fdf838879ec17`  
		Last Modified: Tue, 21 Nov 2023 19:54:29 GMT  
		Size: 116.4 MB (116381803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4dfad0cf1fc9f49cd246d745c8e60de2655f5958cc9cf12c168ed9d89185412e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb3d9da9e8ef38511b9955ba39428d12508f08cfafd8120af33d7cb05c93a8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:02:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:02:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:02:50 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:02:50 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:02:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:02:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed5153b386f9e459da48369f426fafcc7640cc04e0a93a1b51328c28016de09`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac447c42fc4123607bbba8b0d6039aebd3f7398430097e791c6e733e6aef7e13`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584e8c85115b60c19fc0c86c9bc644df5aa9461a6c2d48b21b3d0a0a7fc436df`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 116.3 MB (116275156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:6c6003e890c75c9136df06b9061afbbf9a70673711d2d9abc5937ca7f01abb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:1405b33f9d954b9962af09c3e8f8b69feb900cd917e7b24f9c3ca8d79dcf5dc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90fdf60dd2cdaa8631b8f2fe6906033728268064e21b9973ac341c2dce9bdd2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:21 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:52:37 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:52:37 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:52:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:52:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcf18532b0b5fe4037c5643568f1d179ff345d7055a7ac8a71d63d1358e919c`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024503fd6dce42f3b55a864c14a052cd01a6bc282c4bf992fee6ef4ba23cdf4`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79e7641645bdde609e308b0dc0cc7d3ed00f75229dfb351f7fdf838879ec17`  
		Last Modified: Tue, 21 Nov 2023 19:54:29 GMT  
		Size: 116.4 MB (116381803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4dfad0cf1fc9f49cd246d745c8e60de2655f5958cc9cf12c168ed9d89185412e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb3d9da9e8ef38511b9955ba39428d12508f08cfafd8120af33d7cb05c93a8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:02:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:02:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:02:50 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:02:50 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:02:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:02:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed5153b386f9e459da48369f426fafcc7640cc04e0a93a1b51328c28016de09`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac447c42fc4123607bbba8b0d6039aebd3f7398430097e791c6e733e6aef7e13`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584e8c85115b60c19fc0c86c9bc644df5aa9461a6c2d48b21b3d0a0a7fc436df`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 116.3 MB (116275156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:6c6003e890c75c9136df06b9061afbbf9a70673711d2d9abc5937ca7f01abb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1405b33f9d954b9962af09c3e8f8b69feb900cd917e7b24f9c3ca8d79dcf5dc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90fdf60dd2cdaa8631b8f2fe6906033728268064e21b9973ac341c2dce9bdd2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:21 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:52:37 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:52:37 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:52:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:52:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcf18532b0b5fe4037c5643568f1d179ff345d7055a7ac8a71d63d1358e919c`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024503fd6dce42f3b55a864c14a052cd01a6bc282c4bf992fee6ef4ba23cdf4`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79e7641645bdde609e308b0dc0cc7d3ed00f75229dfb351f7fdf838879ec17`  
		Last Modified: Tue, 21 Nov 2023 19:54:29 GMT  
		Size: 116.4 MB (116381803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4dfad0cf1fc9f49cd246d745c8e60de2655f5958cc9cf12c168ed9d89185412e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb3d9da9e8ef38511b9955ba39428d12508f08cfafd8120af33d7cb05c93a8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:02:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:02:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:02:50 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:02:50 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:02:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:02:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed5153b386f9e459da48369f426fafcc7640cc04e0a93a1b51328c28016de09`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac447c42fc4123607bbba8b0d6039aebd3f7398430097e791c6e733e6aef7e13`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584e8c85115b60c19fc0c86c9bc644df5aa9461a6c2d48b21b3d0a0a7fc436df`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 116.3 MB (116275156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:7472e567239d6a2a3da0450135f18f439fb4fc1abe59c039c611bdf4681d8142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:ffa86c498495b1ed5c501db9ca22defa663573c996f73ceef3eb92cf06abf3b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303341461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc2bfb0891e8061604d52a1cc878b4170d149315006b25379f6299f1d63ff18`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Fri, 17 Nov 2023 04:07:36 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 04:07:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 04:07:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 04:07:37 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 04:07:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 04:07:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 04:07:41 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 04:07:41 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 04:07:41 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 04:07:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 04:07:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6252a3f696c27e59620b16d1002af23ef0a40c8379f9957e254e1c02b95be`  
		Last Modified: Fri, 17 Nov 2023 04:08:34 GMT  
		Size: 6.5 MB (6544950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d35315ff9cc6a58482ae3f04b4732bd85c1fb30a74b31bb68ea4efb7ac2a6c5`  
		Last Modified: Fri, 17 Nov 2023 04:08:33 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c1f45a0d680b445efacdae46d73f96fbee53649dd61e639f27c8ae65e04e9d`  
		Last Modified: Fri, 17 Nov 2023 04:08:40 GMT  
		Size: 112.6 MB (112571479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7828db1f899fd05a3a2fe026d47abb438cc26944b44ec03e2eca452ec6bbb755
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300449561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae5c1f7bcc0eef0555b1bc653a835c0742b9c591366d7364aefa9b7d867c237`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Fri, 17 Nov 2023 03:24:30 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 03:24:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 03:24:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 03:24:31 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 03:24:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 03:24:39 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 03:24:39 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 03:24:39 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 03:24:39 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 03:24:39 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 03:24:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a28d21be43245d925141d42098fe24b55b3e7bd4559cfd1cd9e91847c2dde`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 6.5 MB (6504026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc83fde0c0c3f7884cacc90c1c1ec1d4c0238afa611ce8d677c725acf33b51d`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ea211f3e78a618283203986e7ca5eee92d496eb81f936aafd33d22c1416ebb`  
		Last Modified: Fri, 17 Nov 2023 03:25:40 GMT  
		Size: 112.6 MB (112571515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:d02442781ac8eb24269962ae3b98d3d6c8f2c87bec04c9d493d38f0792aafcff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:a0a73992903a72392d1af2a83891ee4d0fae72ff107b5bf38cc99960dd461284
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564093527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa18f1a8990c2b44ded7f75640d04009d50c80fff83da25361406eb89ab729f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:41 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:59 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:53:00 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:53:00 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:53:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:53:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3cc9d3b549e34d2cb640568660d507b6bf5e6e04544338d0acbd3a61bea75f`  
		Last Modified: Tue, 21 Nov 2023 19:55:26 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4508e6f66f1395a0e42b885df9b3c30c60cd08dd8b06c922809e68f90a67827e`  
		Last Modified: Tue, 21 Nov 2023 19:55:26 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba7fc86877801886afc13370554e8aa83f85e4aa728d56bb6f9362288af09ea`  
		Last Modified: Tue, 21 Nov 2023 19:55:45 GMT  
		Size: 387.8 MB (387788526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9af44c40c5ba0c52c8fc3e74be80a141bf057ad7ce6456a1bdb3b78fdf891003
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.4 MB (561439235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898e64f4f1512971802863391144b7bb2ce8cdf3ff8452b79c345f252980d55e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:55 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:03:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:03:24 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:03:24 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:03:24 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:03:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:03:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed5118a32f8c2fe3869d9d1f74aef21fe22406e66b958cfc93783a179ed4742`  
		Last Modified: Tue, 21 Nov 2023 09:05:11 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c73e0a87bc638caf7d585b09b75e7ec3a733b2966c3671d5582fc16167bfffd`  
		Last Modified: Tue, 21 Nov 2023 09:05:11 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7cdd3753c6429fc0c39100f9f2889e868628f693f9fb4430bd6b0c5b887e44`  
		Last Modified: Tue, 21 Nov 2023 09:05:28 GMT  
		Size: 387.7 MB (387680091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:d02442781ac8eb24269962ae3b98d3d6c8f2c87bec04c9d493d38f0792aafcff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a0a73992903a72392d1af2a83891ee4d0fae72ff107b5bf38cc99960dd461284
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.1 MB (564093527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa18f1a8990c2b44ded7f75640d04009d50c80fff83da25361406eb89ab729f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:41 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:59 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:53:00 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:53:00 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:53:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:53:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3cc9d3b549e34d2cb640568660d507b6bf5e6e04544338d0acbd3a61bea75f`  
		Last Modified: Tue, 21 Nov 2023 19:55:26 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4508e6f66f1395a0e42b885df9b3c30c60cd08dd8b06c922809e68f90a67827e`  
		Last Modified: Tue, 21 Nov 2023 19:55:26 GMT  
		Size: 9.4 KB (9418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba7fc86877801886afc13370554e8aa83f85e4aa728d56bb6f9362288af09ea`  
		Last Modified: Tue, 21 Nov 2023 19:55:45 GMT  
		Size: 387.8 MB (387788526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9af44c40c5ba0c52c8fc3e74be80a141bf057ad7ce6456a1bdb3b78fdf891003
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.4 MB (561439235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898e64f4f1512971802863391144b7bb2ce8cdf3ff8452b79c345f252980d55e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:55 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:03:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:03:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:03:24 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:03:24 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:03:24 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:03:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:03:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed5118a32f8c2fe3869d9d1f74aef21fe22406e66b958cfc93783a179ed4742`  
		Last Modified: Tue, 21 Nov 2023 09:05:11 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c73e0a87bc638caf7d585b09b75e7ec3a733b2966c3671d5582fc16167bfffd`  
		Last Modified: Tue, 21 Nov 2023 09:05:11 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7cdd3753c6429fc0c39100f9f2889e868628f693f9fb4430bd6b0c5b887e44`  
		Last Modified: Tue, 21 Nov 2023 09:05:28 GMT  
		Size: 387.7 MB (387680091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:a2a70251e1b3301223a12038044a77cb69d779d26de36636070629817ae14097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:fae3189d39d01bc069a01cfda97c2cd8bfd31e26b7f0ced74a4bd981dde162f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574748162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de61bb8b8729a83ea95dd5ed02687e79378aacc1f01ae7ff9b410733f638792d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Fri, 17 Nov 2023 04:07:36 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 04:07:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 04:07:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 04:07:45 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 04:07:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 04:07:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 04:07:58 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 04:07:58 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 04:07:59 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 04:07:59 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 04:07:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6252a3f696c27e59620b16d1002af23ef0a40c8379f9957e254e1c02b95be`  
		Last Modified: Fri, 17 Nov 2023 04:08:34 GMT  
		Size: 6.5 MB (6544950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75292d19b6ada0fcf335d32c496f9f7829bfbcd1f356b1bf5bc86ad9a9ac7962`  
		Last Modified: Fri, 17 Nov 2023 04:09:04 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d36c2caa4fefccc3fdce485e834a44f88157e4400a7c95c61a4a2bd5b20351`  
		Last Modified: Fri, 17 Nov 2023 04:09:19 GMT  
		Size: 384.0 MB (383978181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:51a1d4b0c1d0c87f687fb99f20d080e62c900be82e1360482b3c3d7a697d6a8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.9 MB (571856232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa097175b9839a4a175639fdbb1beaeb57c7fce54e3eab45d5d6448d81e9ccf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Fri, 17 Nov 2023 03:24:30 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 03:24:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 03:24:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 03:24:48 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 03:24:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 03:25:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 03:25:00 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 03:25:01 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 03:25:01 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 03:25:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 03:25:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a28d21be43245d925141d42098fe24b55b3e7bd4559cfd1cd9e91847c2dde`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 6.5 MB (6504026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8afe0f1f1a01988b2e5b24f9e1098e5cd45b2530f7dcf74d2f3d03965cb9470`  
		Last Modified: Fri, 17 Nov 2023 03:26:05 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a154f9e3b2395a9b9803f698016c62421aecbae7a191723ea7bf25cf6c19c794`  
		Last Modified: Fri, 17 Nov 2023 03:26:20 GMT  
		Size: 384.0 MB (383978188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:6c6003e890c75c9136df06b9061afbbf9a70673711d2d9abc5937ca7f01abb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:1405b33f9d954b9962af09c3e8f8b69feb900cd917e7b24f9c3ca8d79dcf5dc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292686809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90fdf60dd2cdaa8631b8f2fe6906033728268064e21b9973ac341c2dce9bdd2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:20:18 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 21 Nov 2023 19:52:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 19:52:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 19:52:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 19:52:21 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 19:52:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 19:52:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 19:52:37 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 19:52:37 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 19:52:37 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 19:52:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 19:52:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb2ec605bdd7c4e3e9ec3c1c017bc58abd1f4ed8d64e2f02df15eafab91eefe`  
		Last Modified: Tue, 21 Nov 2023 10:36:17 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcf18532b0b5fe4037c5643568f1d179ff345d7055a7ac8a71d63d1358e919c`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3024503fd6dce42f3b55a864c14a052cd01a6bc282c4bf992fee6ef4ba23cdf4`  
		Last Modified: Tue, 21 Nov 2023 19:54:09 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79e7641645bdde609e308b0dc0cc7d3ed00f75229dfb351f7fdf838879ec17`  
		Last Modified: Tue, 21 Nov 2023 19:54:29 GMT  
		Size: 116.4 MB (116381803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4dfad0cf1fc9f49cd246d745c8e60de2655f5958cc9cf12c168ed9d89185412e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290034299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb3d9da9e8ef38511b9955ba39428d12508f08cfafd8120af33d7cb05c93a8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:32:22 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 09:02:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 21 Nov 2023 09:02:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Tue, 21 Nov 2023 09:02:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 21 Nov 2023 09:02:39 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Tue, 21 Nov 2023 09:02:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:02:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 09:02:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 21 Nov 2023 09:02:50 GMT
VOLUME [/data /logs]
# Tue, 21 Nov 2023 09:02:50 GMT
EXPOSE 7473 7474 7687
# Tue, 21 Nov 2023 09:02:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 09:02:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774c3f8f337a80da224d5f4f5b5f609bc6ed9c008d2dca47113a0123d56da5dd`  
		Last Modified: Tue, 21 Nov 2023 07:47:17 GMT  
		Size: 143.7 MB (143681712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed5153b386f9e459da48369f426fafcc7640cc04e0a93a1b51328c28016de09`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac447c42fc4123607bbba8b0d6039aebd3f7398430097e791c6e733e6aef7e13`  
		Last Modified: Tue, 21 Nov 2023 09:04:33 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584e8c85115b60c19fc0c86c9bc644df5aa9461a6c2d48b21b3d0a0a7fc436df`  
		Last Modified: Tue, 21 Nov 2023 09:04:38 GMT  
		Size: 116.3 MB (116275156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:7472e567239d6a2a3da0450135f18f439fb4fc1abe59c039c611bdf4681d8142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:ffa86c498495b1ed5c501db9ca22defa663573c996f73ceef3eb92cf06abf3b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303341461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc2bfb0891e8061604d52a1cc878b4170d149315006b25379f6299f1d63ff18`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:53 GMT
ADD file:47589af4a3da87e21edebcff87ac699aa8818e369afb7b60c9a26f193942db3e in / 
# Wed, 01 Nov 2023 03:26:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:54 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:54 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:54 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:54 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:54 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:55 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:732950e4831bd3dbf3c279f66da444e65ecc2962a326463fc1748a7ef063d841 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:b361c9d04ed3cbb92e69fd3858c1b12aecbd2de1bf55967db6159058c4a49e12 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:26:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 04:07:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 04:07:24 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Fri, 17 Nov 2023 04:07:36 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 04:07:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 04:07:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 04:07:37 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 04:07:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 04:07:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 04:07:41 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 04:07:41 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 04:07:41 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 04:07:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 04:07:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4a3c904e5565efee16dbcb82838bbb64a39f8261e4531648bc591c528236c24`  
		Last Modified: Wed, 15 Nov 2023 18:35:34 GMT  
		Size: 39.3 MB (39341714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91150f8130a3a57fbbe53278b22e5e9633949a8d689508666a98dc178ffcf9d1`  
		Last Modified: Fri, 17 Nov 2023 04:08:45 GMT  
		Size: 144.9 MB (144873897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f6252a3f696c27e59620b16d1002af23ef0a40c8379f9957e254e1c02b95be`  
		Last Modified: Fri, 17 Nov 2023 04:08:34 GMT  
		Size: 6.5 MB (6544950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d35315ff9cc6a58482ae3f04b4732bd85c1fb30a74b31bb68ea4efb7ac2a6c5`  
		Last Modified: Fri, 17 Nov 2023 04:08:33 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c1f45a0d680b445efacdae46d73f96fbee53649dd61e639f27c8ae65e04e9d`  
		Last Modified: Fri, 17 Nov 2023 04:08:40 GMT  
		Size: 112.6 MB (112571479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7828db1f899fd05a3a2fe026d47abb438cc26944b44ec03e2eca452ec6bbb755
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300449561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae5c1f7bcc0eef0555b1bc653a835c0742b9c591366d7364aefa9b7d867c237`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Nov 2023 03:26:54 GMT
ADD file:2268389f6691723ff73eafb7f91e3fc2326d5d821040b1e7b1f16f6ca6a450c7 in / 
# Wed, 01 Nov 2023 03:26:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 01 Nov 2023 03:26:55 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 01 Nov 2023 03:26:55 GMT
ADD multi:1d8f8a6ff2fa00884e209245ce9248e4cee06aa7f27bdf4f90dc2edc3498c511 in /etc/yum.repos.d/ 
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 01 Nov 2023 03:26:55 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 01 Nov 2023 03:26:55 GMT
ENV container oci
# Wed, 01 Nov 2023 03:26:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 03:26:55 GMT
CMD ["/bin/bash"]
# Wed, 01 Nov 2023 03:26:56 GMT
RUN rm -rf /var/log/*
# Wed, 01 Nov 2023 03:26:56 GMT
LABEL release=1029
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:aa421ceadf9415f2c5b67b3b5d9a8543215bfc83157831e4d93bf5ac187a6549 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1029.json 
# Wed, 01 Nov 2023 03:26:57 GMT
ADD file:075dfdece656aa5ed8d1c9a45607ce60c4b2c2025f8cd0516d52cecf2e8331f0 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1029 
# Wed, 01 Nov 2023 03:26:57 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-11-01T03:17:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1029"
# Wed, 01 Nov 2023 03:26:58 GMT
RUN rm -f '/etc/yum.repos.d/repo-3b08a.repo' '/etc/yum.repos.d/repo-4c95e.repo'
# Wed, 01 Nov 2023 03:26:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 01 Nov 2023 03:27:01 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 17 Nov 2023 03:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 17 Nov 2023 03:24:10 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Fri, 17 Nov 2023 03:24:30 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Fri, 17 Nov 2023 03:24:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 17 Nov 2023 03:24:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Fri, 17 Nov 2023 03:24:31 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Fri, 17 Nov 2023 03:24:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Fri, 17 Nov 2023 03:24:39 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Nov 2023 03:24:39 GMT
WORKDIR /var/lib/neo4j
# Fri, 17 Nov 2023 03:24:39 GMT
VOLUME [/data /logs]
# Fri, 17 Nov 2023 03:24:39 GMT
EXPOSE 7473 7474 7687
# Fri, 17 Nov 2023 03:24:39 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 17 Nov 2023 03:24:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:efe07ddbececa05537c13805b89ed74cb770f1dde30ddcae0a6c60ccd010ea2f`  
		Last Modified: Wed, 15 Nov 2023 19:35:11 GMT  
		Size: 37.7 MB (37682884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d7ddbdda4bac772245a602caec768364b4dca54bac23e4fe092efbd401d40a`  
		Last Modified: Fri, 17 Nov 2023 03:25:45 GMT  
		Size: 143.7 MB (143681715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a28d21be43245d925141d42098fe24b55b3e7bd4559cfd1cd9e91847c2dde`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 6.5 MB (6504026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc83fde0c0c3f7884cacc90c1c1ec1d4c0238afa611ce8d677c725acf33b51d`  
		Last Modified: Fri, 17 Nov 2023 03:25:36 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ea211f3e78a618283203986e7ca5eee92d496eb81f936aafd33d22c1416ebb`  
		Last Modified: Fri, 17 Nov 2023 03:25:40 GMT  
		Size: 112.6 MB (112571515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
