<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.22`](#neo4j4422)
-	[`neo4j:4.4.22-community`](#neo4j4422-community)
-	[`neo4j:4.4.22-enterprise`](#neo4j4422-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5.9`](#neo4j59)
-	[`neo4j:5.9-community`](#neo4j59-community)
-	[`neo4j:5.9-enterprise`](#neo4j59-enterprise)
-	[`neo4j:5.9.0`](#neo4j590)
-	[`neo4j:5.9.0-community`](#neo4j590-community)
-	[`neo4j:5.9.0-enterprise`](#neo4j590-enterprise)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:latest`](#neo4jlatest)

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:8cb49c332a62ef9e0767a8e596501e4d99f544bb3f31e8e72ed8888b24b30fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:364162f9d0cabcfb8fc89eecce25eeb223a2e69166fa7285e0aa2b6380d04839
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348437804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50381ff28061eb19f94537c3ee600ebe2157615075a8c7b308a3f041079723a8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:20:25 GMT
COPY dir:8166f0419dcb1797526932f102a2cde39418897507eef5904ae1b596b03e4941 in /opt/java/openjdk 
# Tue, 27 Jun 2023 19:21:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a4a150531e421f7bd24a00b3cfb8d923b898035f2ac987c68ead7d69ef321b06 NEO4J_TARBALL=neo4j-community-4.4.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 27 Jun 2023 19:21:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
# Tue, 27 Jun 2023 19:21:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 27 Jun 2023 19:21:13 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Tue, 27 Jun 2023 19:21:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jun 2023 19:21:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jun 2023 19:21:34 GMT
WORKDIR /var/lib/neo4j
# Tue, 27 Jun 2023 19:21:34 GMT
VOLUME [/data /logs]
# Tue, 27 Jun 2023 19:21:34 GMT
EXPOSE 7473 7474 7687
# Tue, 27 Jun 2023 19:21:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 27 Jun 2023 19:21:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce9cee97ba9b79deb50a75bd84ddae8d819deb99b5745e620764e192c07b86b`  
		Last Modified: Fri, 16 Jun 2023 05:22:45 GMT  
		Size: 198.5 MB (198549374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5df2ef9f1bf63362eb88ccf438942a5b114f4d0daa037c35b52de19b0bef33`  
		Last Modified: Tue, 27 Jun 2023 19:22:20 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36596c2a344e397e28d3514acae48f9dff96817de0600eaf08eabcdb4b153730`  
		Last Modified: Tue, 27 Jun 2023 19:22:20 GMT  
		Size: 9.3 KB (9325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68663ce90262938cac23bf7beadd58f0f11b23d6c68093957e8a9830b84ca98f`  
		Last Modified: Tue, 27 Jun 2023 19:22:26 GMT  
		Size: 118.5 MB (118457837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0bd5c788f5bcefb559ea421f817147ae97e150b2d4a3e357fec15c6f109db582
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.8 MB (343751784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3f46b3f22be2c2a71de1805a81006eec2cd572e16265009b360b5daa8fb817`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:35:19 GMT
COPY dir:e9846f499a157c7a78a7ddb1d6b9ebc67065c65b65eb611ad6978501e8452ab7 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:35:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a4a150531e421f7bd24a00b3cfb8d923b898035f2ac987c68ead7d69ef321b06 NEO4J_TARBALL=neo4j-community-4.4.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:35:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
# Tue, 04 Jul 2023 06:35:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:35:24 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Tue, 04 Jul 2023 06:35:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:35:38 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:35:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:35:39 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:35:39 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:35:39 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:35:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fccefcb482635b3259449981a784fc2012a529dac3559c916400e0c1558529`  
		Last Modified: Tue, 04 Jul 2023 06:37:25 GMT  
		Size: 195.3 MB (195324205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97973f720365351bb1affd42f5b336dab6f3f77029b84df579d53ef7eb5467a`  
		Last Modified: Tue, 04 Jul 2023 06:37:14 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef5344b0adba04a5da63e6fa7b7b4b78d1e41aaf532ac6e64169feb1c160680`  
		Last Modified: Tue, 04 Jul 2023 06:37:14 GMT  
		Size: 9.3 KB (9327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544d9b78c5f43953f3e27950c8a04dab4b295dda8095a6c8bfda44221f1c818f`  
		Last Modified: Tue, 04 Jul 2023 06:37:18 GMT  
		Size: 118.4 MB (118351410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:8cb49c332a62ef9e0767a8e596501e4d99f544bb3f31e8e72ed8888b24b30fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:364162f9d0cabcfb8fc89eecce25eeb223a2e69166fa7285e0aa2b6380d04839
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348437804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50381ff28061eb19f94537c3ee600ebe2157615075a8c7b308a3f041079723a8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:20:25 GMT
COPY dir:8166f0419dcb1797526932f102a2cde39418897507eef5904ae1b596b03e4941 in /opt/java/openjdk 
# Tue, 27 Jun 2023 19:21:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a4a150531e421f7bd24a00b3cfb8d923b898035f2ac987c68ead7d69ef321b06 NEO4J_TARBALL=neo4j-community-4.4.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 27 Jun 2023 19:21:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
# Tue, 27 Jun 2023 19:21:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 27 Jun 2023 19:21:13 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Tue, 27 Jun 2023 19:21:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jun 2023 19:21:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jun 2023 19:21:34 GMT
WORKDIR /var/lib/neo4j
# Tue, 27 Jun 2023 19:21:34 GMT
VOLUME [/data /logs]
# Tue, 27 Jun 2023 19:21:34 GMT
EXPOSE 7473 7474 7687
# Tue, 27 Jun 2023 19:21:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 27 Jun 2023 19:21:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce9cee97ba9b79deb50a75bd84ddae8d819deb99b5745e620764e192c07b86b`  
		Last Modified: Fri, 16 Jun 2023 05:22:45 GMT  
		Size: 198.5 MB (198549374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5df2ef9f1bf63362eb88ccf438942a5b114f4d0daa037c35b52de19b0bef33`  
		Last Modified: Tue, 27 Jun 2023 19:22:20 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36596c2a344e397e28d3514acae48f9dff96817de0600eaf08eabcdb4b153730`  
		Last Modified: Tue, 27 Jun 2023 19:22:20 GMT  
		Size: 9.3 KB (9325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68663ce90262938cac23bf7beadd58f0f11b23d6c68093957e8a9830b84ca98f`  
		Last Modified: Tue, 27 Jun 2023 19:22:26 GMT  
		Size: 118.5 MB (118457837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0bd5c788f5bcefb559ea421f817147ae97e150b2d4a3e357fec15c6f109db582
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.8 MB (343751784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3f46b3f22be2c2a71de1805a81006eec2cd572e16265009b360b5daa8fb817`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:35:19 GMT
COPY dir:e9846f499a157c7a78a7ddb1d6b9ebc67065c65b65eb611ad6978501e8452ab7 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:35:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a4a150531e421f7bd24a00b3cfb8d923b898035f2ac987c68ead7d69ef321b06 NEO4J_TARBALL=neo4j-community-4.4.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:35:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
# Tue, 04 Jul 2023 06:35:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:35:24 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Tue, 04 Jul 2023 06:35:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:35:38 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:35:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:35:39 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:35:39 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:35:39 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:35:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fccefcb482635b3259449981a784fc2012a529dac3559c916400e0c1558529`  
		Last Modified: Tue, 04 Jul 2023 06:37:25 GMT  
		Size: 195.3 MB (195324205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97973f720365351bb1affd42f5b336dab6f3f77029b84df579d53ef7eb5467a`  
		Last Modified: Tue, 04 Jul 2023 06:37:14 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef5344b0adba04a5da63e6fa7b7b4b78d1e41aaf532ac6e64169feb1c160680`  
		Last Modified: Tue, 04 Jul 2023 06:37:14 GMT  
		Size: 9.3 KB (9327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544d9b78c5f43953f3e27950c8a04dab4b295dda8095a6c8bfda44221f1c818f`  
		Last Modified: Tue, 04 Jul 2023 06:37:18 GMT  
		Size: 118.4 MB (118351410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:13a5a7e130412ce6b4e60e06eb8322e7a58ad87ed0f3a62ca2bef2fc6bbad907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:424b7814250f256f68c7306ce1dab15e7cd63347df85bb4a9fb53dc24c5f1914
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.8 MB (447761997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7df46eb5e243503fdf2e1ac7840f33001b381df52347fe515dee42467d04ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:20:25 GMT
COPY dir:8166f0419dcb1797526932f102a2cde39418897507eef5904ae1b596b03e4941 in /opt/java/openjdk 
# Tue, 27 Jun 2023 19:21:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ec49ac0f429a7e05ab21e48c8bc6273274c82df6f75221b85cec0c53a51ef840 NEO4J_TARBALL=neo4j-enterprise-4.4.22-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 27 Jun 2023 19:21:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.22-unix.tar.gz
# Tue, 27 Jun 2023 19:21:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 27 Jun 2023 19:21:41 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Tue, 27 Jun 2023 19:21:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jun 2023 19:21:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jun 2023 19:21:55 GMT
WORKDIR /var/lib/neo4j
# Tue, 27 Jun 2023 19:21:55 GMT
VOLUME [/data /logs]
# Tue, 27 Jun 2023 19:21:56 GMT
EXPOSE 7473 7474 7687
# Tue, 27 Jun 2023 19:21:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 27 Jun 2023 19:21:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce9cee97ba9b79deb50a75bd84ddae8d819deb99b5745e620764e192c07b86b`  
		Last Modified: Fri, 16 Jun 2023 05:22:45 GMT  
		Size: 198.5 MB (198549374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927451cb9e4df6751d462580fafb06533e5646ac17d7238223345a351ffcfd71`  
		Last Modified: Tue, 27 Jun 2023 19:22:38 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7275d4adc31ca7ab39775315dfd357db9c55de9bf96e07a7d0b85fbfa11ef9da`  
		Last Modified: Tue, 27 Jun 2023 19:22:38 GMT  
		Size: 9.3 KB (9323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cb8d02d9f7ecbf7ef87fab58f750150738bbd9eba86289b1f1fe251160f7db`  
		Last Modified: Tue, 27 Jun 2023 19:22:48 GMT  
		Size: 217.8 MB (217782034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6b113164787c72acb401288cc539a2c63e89d77c19b7b34bede60aee492b039f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.1 MB (443074102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d35c8b2d8322767d72d1b0ac2cb53d3af201760e97732b0d38fa09e81c0d6bf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:35:19 GMT
COPY dir:e9846f499a157c7a78a7ddb1d6b9ebc67065c65b65eb611ad6978501e8452ab7 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:35:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ec49ac0f429a7e05ab21e48c8bc6273274c82df6f75221b85cec0c53a51ef840 NEO4J_TARBALL=neo4j-enterprise-4.4.22-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:35:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.22-unix.tar.gz
# Tue, 04 Jul 2023 06:35:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:35:45 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Tue, 04 Jul 2023 06:36:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:36:06 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:36:06 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:36:06 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:36:06 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:36:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:36:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fccefcb482635b3259449981a784fc2012a529dac3559c916400e0c1558529`  
		Last Modified: Tue, 04 Jul 2023 06:37:25 GMT  
		Size: 195.3 MB (195324205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835e3da3584541f879967b51d01d72f998910e7ce61a1e8b2b2c90f90cfeb12c`  
		Last Modified: Tue, 04 Jul 2023 06:37:36 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e024cb6cf7ad1f191de432829ecaf90718ee764c6714a481b7cc124b955377`  
		Last Modified: Tue, 04 Jul 2023 06:37:36 GMT  
		Size: 9.3 KB (9325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489287abfe63d498bca83f108d8f16fe6d934c0beb71a0446669965b19117cb7`  
		Last Modified: Tue, 04 Jul 2023 06:37:44 GMT  
		Size: 217.7 MB (217673731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.22`

```console
$ docker pull neo4j@sha256:8cb49c332a62ef9e0767a8e596501e4d99f544bb3f31e8e72ed8888b24b30fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.22` - linux; amd64

```console
$ docker pull neo4j@sha256:364162f9d0cabcfb8fc89eecce25eeb223a2e69166fa7285e0aa2b6380d04839
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348437804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50381ff28061eb19f94537c3ee600ebe2157615075a8c7b308a3f041079723a8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:20:25 GMT
COPY dir:8166f0419dcb1797526932f102a2cde39418897507eef5904ae1b596b03e4941 in /opt/java/openjdk 
# Tue, 27 Jun 2023 19:21:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a4a150531e421f7bd24a00b3cfb8d923b898035f2ac987c68ead7d69ef321b06 NEO4J_TARBALL=neo4j-community-4.4.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 27 Jun 2023 19:21:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
# Tue, 27 Jun 2023 19:21:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 27 Jun 2023 19:21:13 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Tue, 27 Jun 2023 19:21:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jun 2023 19:21:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jun 2023 19:21:34 GMT
WORKDIR /var/lib/neo4j
# Tue, 27 Jun 2023 19:21:34 GMT
VOLUME [/data /logs]
# Tue, 27 Jun 2023 19:21:34 GMT
EXPOSE 7473 7474 7687
# Tue, 27 Jun 2023 19:21:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 27 Jun 2023 19:21:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce9cee97ba9b79deb50a75bd84ddae8d819deb99b5745e620764e192c07b86b`  
		Last Modified: Fri, 16 Jun 2023 05:22:45 GMT  
		Size: 198.5 MB (198549374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5df2ef9f1bf63362eb88ccf438942a5b114f4d0daa037c35b52de19b0bef33`  
		Last Modified: Tue, 27 Jun 2023 19:22:20 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36596c2a344e397e28d3514acae48f9dff96817de0600eaf08eabcdb4b153730`  
		Last Modified: Tue, 27 Jun 2023 19:22:20 GMT  
		Size: 9.3 KB (9325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68663ce90262938cac23bf7beadd58f0f11b23d6c68093957e8a9830b84ca98f`  
		Last Modified: Tue, 27 Jun 2023 19:22:26 GMT  
		Size: 118.5 MB (118457837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.22` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0bd5c788f5bcefb559ea421f817147ae97e150b2d4a3e357fec15c6f109db582
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.8 MB (343751784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3f46b3f22be2c2a71de1805a81006eec2cd572e16265009b360b5daa8fb817`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:35:19 GMT
COPY dir:e9846f499a157c7a78a7ddb1d6b9ebc67065c65b65eb611ad6978501e8452ab7 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:35:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a4a150531e421f7bd24a00b3cfb8d923b898035f2ac987c68ead7d69ef321b06 NEO4J_TARBALL=neo4j-community-4.4.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:35:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
# Tue, 04 Jul 2023 06:35:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:35:24 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Tue, 04 Jul 2023 06:35:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:35:38 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:35:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:35:39 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:35:39 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:35:39 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:35:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fccefcb482635b3259449981a784fc2012a529dac3559c916400e0c1558529`  
		Last Modified: Tue, 04 Jul 2023 06:37:25 GMT  
		Size: 195.3 MB (195324205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97973f720365351bb1affd42f5b336dab6f3f77029b84df579d53ef7eb5467a`  
		Last Modified: Tue, 04 Jul 2023 06:37:14 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef5344b0adba04a5da63e6fa7b7b4b78d1e41aaf532ac6e64169feb1c160680`  
		Last Modified: Tue, 04 Jul 2023 06:37:14 GMT  
		Size: 9.3 KB (9327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544d9b78c5f43953f3e27950c8a04dab4b295dda8095a6c8bfda44221f1c818f`  
		Last Modified: Tue, 04 Jul 2023 06:37:18 GMT  
		Size: 118.4 MB (118351410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.22-community`

```console
$ docker pull neo4j@sha256:8cb49c332a62ef9e0767a8e596501e4d99f544bb3f31e8e72ed8888b24b30fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.22-community` - linux; amd64

```console
$ docker pull neo4j@sha256:364162f9d0cabcfb8fc89eecce25eeb223a2e69166fa7285e0aa2b6380d04839
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348437804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50381ff28061eb19f94537c3ee600ebe2157615075a8c7b308a3f041079723a8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:20:25 GMT
COPY dir:8166f0419dcb1797526932f102a2cde39418897507eef5904ae1b596b03e4941 in /opt/java/openjdk 
# Tue, 27 Jun 2023 19:21:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a4a150531e421f7bd24a00b3cfb8d923b898035f2ac987c68ead7d69ef321b06 NEO4J_TARBALL=neo4j-community-4.4.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 27 Jun 2023 19:21:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
# Tue, 27 Jun 2023 19:21:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 27 Jun 2023 19:21:13 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Tue, 27 Jun 2023 19:21:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jun 2023 19:21:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jun 2023 19:21:34 GMT
WORKDIR /var/lib/neo4j
# Tue, 27 Jun 2023 19:21:34 GMT
VOLUME [/data /logs]
# Tue, 27 Jun 2023 19:21:34 GMT
EXPOSE 7473 7474 7687
# Tue, 27 Jun 2023 19:21:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 27 Jun 2023 19:21:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce9cee97ba9b79deb50a75bd84ddae8d819deb99b5745e620764e192c07b86b`  
		Last Modified: Fri, 16 Jun 2023 05:22:45 GMT  
		Size: 198.5 MB (198549374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5df2ef9f1bf63362eb88ccf438942a5b114f4d0daa037c35b52de19b0bef33`  
		Last Modified: Tue, 27 Jun 2023 19:22:20 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36596c2a344e397e28d3514acae48f9dff96817de0600eaf08eabcdb4b153730`  
		Last Modified: Tue, 27 Jun 2023 19:22:20 GMT  
		Size: 9.3 KB (9325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68663ce90262938cac23bf7beadd58f0f11b23d6c68093957e8a9830b84ca98f`  
		Last Modified: Tue, 27 Jun 2023 19:22:26 GMT  
		Size: 118.5 MB (118457837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.22-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0bd5c788f5bcefb559ea421f817147ae97e150b2d4a3e357fec15c6f109db582
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.8 MB (343751784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3f46b3f22be2c2a71de1805a81006eec2cd572e16265009b360b5daa8fb817`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:35:19 GMT
COPY dir:e9846f499a157c7a78a7ddb1d6b9ebc67065c65b65eb611ad6978501e8452ab7 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:35:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a4a150531e421f7bd24a00b3cfb8d923b898035f2ac987c68ead7d69ef321b06 NEO4J_TARBALL=neo4j-community-4.4.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:35:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
# Tue, 04 Jul 2023 06:35:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:35:24 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Tue, 04 Jul 2023 06:35:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:35:38 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:35:38 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:35:39 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:35:39 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:35:39 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:35:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fccefcb482635b3259449981a784fc2012a529dac3559c916400e0c1558529`  
		Last Modified: Tue, 04 Jul 2023 06:37:25 GMT  
		Size: 195.3 MB (195324205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97973f720365351bb1affd42f5b336dab6f3f77029b84df579d53ef7eb5467a`  
		Last Modified: Tue, 04 Jul 2023 06:37:14 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef5344b0adba04a5da63e6fa7b7b4b78d1e41aaf532ac6e64169feb1c160680`  
		Last Modified: Tue, 04 Jul 2023 06:37:14 GMT  
		Size: 9.3 KB (9327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544d9b78c5f43953f3e27950c8a04dab4b295dda8095a6c8bfda44221f1c818f`  
		Last Modified: Tue, 04 Jul 2023 06:37:18 GMT  
		Size: 118.4 MB (118351410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.22-enterprise`

```console
$ docker pull neo4j@sha256:13a5a7e130412ce6b4e60e06eb8322e7a58ad87ed0f3a62ca2bef2fc6bbad907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.22-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:424b7814250f256f68c7306ce1dab15e7cd63347df85bb4a9fb53dc24c5f1914
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.8 MB (447761997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7df46eb5e243503fdf2e1ac7840f33001b381df52347fe515dee42467d04ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:20:25 GMT
COPY dir:8166f0419dcb1797526932f102a2cde39418897507eef5904ae1b596b03e4941 in /opt/java/openjdk 
# Tue, 27 Jun 2023 19:21:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ec49ac0f429a7e05ab21e48c8bc6273274c82df6f75221b85cec0c53a51ef840 NEO4J_TARBALL=neo4j-enterprise-4.4.22-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 27 Jun 2023 19:21:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.22-unix.tar.gz
# Tue, 27 Jun 2023 19:21:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 27 Jun 2023 19:21:41 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Tue, 27 Jun 2023 19:21:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jun 2023 19:21:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jun 2023 19:21:55 GMT
WORKDIR /var/lib/neo4j
# Tue, 27 Jun 2023 19:21:55 GMT
VOLUME [/data /logs]
# Tue, 27 Jun 2023 19:21:56 GMT
EXPOSE 7473 7474 7687
# Tue, 27 Jun 2023 19:21:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 27 Jun 2023 19:21:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce9cee97ba9b79deb50a75bd84ddae8d819deb99b5745e620764e192c07b86b`  
		Last Modified: Fri, 16 Jun 2023 05:22:45 GMT  
		Size: 198.5 MB (198549374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927451cb9e4df6751d462580fafb06533e5646ac17d7238223345a351ffcfd71`  
		Last Modified: Tue, 27 Jun 2023 19:22:38 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7275d4adc31ca7ab39775315dfd357db9c55de9bf96e07a7d0b85fbfa11ef9da`  
		Last Modified: Tue, 27 Jun 2023 19:22:38 GMT  
		Size: 9.3 KB (9323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cb8d02d9f7ecbf7ef87fab58f750150738bbd9eba86289b1f1fe251160f7db`  
		Last Modified: Tue, 27 Jun 2023 19:22:48 GMT  
		Size: 217.8 MB (217782034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.22-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6b113164787c72acb401288cc539a2c63e89d77c19b7b34bede60aee492b039f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **443.1 MB (443074102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d35c8b2d8322767d72d1b0ac2cb53d3af201760e97732b0d38fa09e81c0d6bf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:35:19 GMT
COPY dir:e9846f499a157c7a78a7ddb1d6b9ebc67065c65b65eb611ad6978501e8452ab7 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:35:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ec49ac0f429a7e05ab21e48c8bc6273274c82df6f75221b85cec0c53a51ef840 NEO4J_TARBALL=neo4j-enterprise-4.4.22-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:35:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.22-unix.tar.gz
# Tue, 04 Jul 2023 06:35:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:35:45 GMT
COPY multi:269f2bb89a34e8e23b4028baf2582795a6378669e17bfcf98f4ae14c2de48e0b in /startup/ 
# Tue, 04 Jul 2023 06:36:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:36:06 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:36:06 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:36:06 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:36:06 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:36:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:36:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fccefcb482635b3259449981a784fc2012a529dac3559c916400e0c1558529`  
		Last Modified: Tue, 04 Jul 2023 06:37:25 GMT  
		Size: 195.3 MB (195324205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835e3da3584541f879967b51d01d72f998910e7ce61a1e8b2b2c90f90cfeb12c`  
		Last Modified: Tue, 04 Jul 2023 06:37:36 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e024cb6cf7ad1f191de432829ecaf90718ee764c6714a481b7cc124b955377`  
		Last Modified: Tue, 04 Jul 2023 06:37:36 GMT  
		Size: 9.3 KB (9325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489287abfe63d498bca83f108d8f16fe6d934c0beb71a0446669965b19117cb7`  
		Last Modified: Tue, 04 Jul 2023 06:37:44 GMT  
		Size: 217.7 MB (217673731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:95de8dc67e16abc946a16d385bba05080f06f7590170d58f788d179ce5d8621e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:fa8f71d6091bc76419f571acd04d30fd654642c7f834e5d671f637303611425d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339764660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246f3b226b168f5342e28e71b7502c2fe6bf1d2afe536b7694ce2cb9cd99c25`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:19:27 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:30 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:19:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:19:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:19:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:19:50 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:19:50 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:19:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:19:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16587156d6d664ce45c78f53fd4abf3903d66718d37c56e9d942121e5a5c2298`  
		Last Modified: Fri, 16 Jun 2023 05:21:41 GMT  
		Size: 192.6 MB (192580339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf092e6a4075a792e6cfdfa941697da3110c57b3eed1a6514ac06fb653fcd446`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 3.9 KB (3853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e8789f08f62ffed6acd775d54345f8ffdcc301329b64e9c9b676d8782c8ae`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b62bb6d5e4ab5cd0b4e67117c58f65929c22d74141894345bac35d9df4bf77`  
		Last Modified: Fri, 16 Jun 2023 05:21:34 GMT  
		Size: 115.8 MB (115753684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ab9c060c7ff61a54b35a7b38fc09f4cb143f210c2c7711c04d19802b0b97f10f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337110137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2aa94390a4d91363d5896f5f9c83921b57d038fa1fefc849bf32f4c662ab5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:34:28 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:34:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:34:32 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Tue, 04 Jul 2023 06:34:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:34:33 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Tue, 04 Jul 2023 06:34:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:34:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:34:48 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:34:49 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:34:49 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:34:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:34:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275827ff61a5cc842494b7c486dc8fd020f878ff693af5f57969cf5f7481a0d0`  
		Last Modified: Tue, 04 Jul 2023 06:36:29 GMT  
		Size: 191.4 MB (191387687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31bbf0eb561b1650f22e928cbeccb17872671effa64cad96c568923c773c5e1`  
		Last Modified: Tue, 04 Jul 2023 06:36:18 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7602e07641dac1311b8a2427efdb849b9749894a1a9ed64979931ed3d6f03bdc`  
		Last Modified: Tue, 04 Jul 2023 06:36:18 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925b08e9954cc34ec2861c0b6ea5ade09ae1a9361db08e6c22d2c5eba5010b65`  
		Last Modified: Tue, 04 Jul 2023 06:36:23 GMT  
		Size: 115.6 MB (115646236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:95de8dc67e16abc946a16d385bba05080f06f7590170d58f788d179ce5d8621e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:fa8f71d6091bc76419f571acd04d30fd654642c7f834e5d671f637303611425d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339764660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246f3b226b168f5342e28e71b7502c2fe6bf1d2afe536b7694ce2cb9cd99c25`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:19:27 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:30 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:19:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:19:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:19:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:19:50 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:19:50 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:19:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:19:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16587156d6d664ce45c78f53fd4abf3903d66718d37c56e9d942121e5a5c2298`  
		Last Modified: Fri, 16 Jun 2023 05:21:41 GMT  
		Size: 192.6 MB (192580339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf092e6a4075a792e6cfdfa941697da3110c57b3eed1a6514ac06fb653fcd446`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 3.9 KB (3853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e8789f08f62ffed6acd775d54345f8ffdcc301329b64e9c9b676d8782c8ae`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b62bb6d5e4ab5cd0b4e67117c58f65929c22d74141894345bac35d9df4bf77`  
		Last Modified: Fri, 16 Jun 2023 05:21:34 GMT  
		Size: 115.8 MB (115753684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ab9c060c7ff61a54b35a7b38fc09f4cb143f210c2c7711c04d19802b0b97f10f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337110137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2aa94390a4d91363d5896f5f9c83921b57d038fa1fefc849bf32f4c662ab5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:34:28 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:34:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:34:32 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Tue, 04 Jul 2023 06:34:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:34:33 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Tue, 04 Jul 2023 06:34:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:34:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:34:48 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:34:49 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:34:49 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:34:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:34:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275827ff61a5cc842494b7c486dc8fd020f878ff693af5f57969cf5f7481a0d0`  
		Last Modified: Tue, 04 Jul 2023 06:36:29 GMT  
		Size: 191.4 MB (191387687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31bbf0eb561b1650f22e928cbeccb17872671effa64cad96c568923c773c5e1`  
		Last Modified: Tue, 04 Jul 2023 06:36:18 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7602e07641dac1311b8a2427efdb849b9749894a1a9ed64979931ed3d6f03bdc`  
		Last Modified: Tue, 04 Jul 2023 06:36:18 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925b08e9954cc34ec2861c0b6ea5ade09ae1a9361db08e6c22d2c5eba5010b65`  
		Last Modified: Tue, 04 Jul 2023 06:36:23 GMT  
		Size: 115.6 MB (115646236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:2eca6bc1d822cbcab980141695125300a92cecf26346740349684e67f13292fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:631f6f6c38f7f4ec8c242c835170dd208889b6ff1d1974cd91c0befd909abd57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.7 MB (617745683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5355d4b7934f264f871f69865b91102fe63a65413e2e8fd09238b57a3c35c3c1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:19:27 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:19:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=978819870e976f903ecfb68a8e22ee5ea498779ee14a0c4d9f0f98fc29230ccb NEO4J_TARBALL=neo4j-enterprise-5.9.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:58 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:20:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:20:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:20:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:20:18 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:20:18 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:20:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:20:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16587156d6d664ce45c78f53fd4abf3903d66718d37c56e9d942121e5a5c2298`  
		Last Modified: Fri, 16 Jun 2023 05:21:41 GMT  
		Size: 192.6 MB (192580339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfeefc867edcf7d51cc01312e1d1db4f53976bc6bbc672ee592afe405e904eb4`  
		Last Modified: Fri, 16 Jun 2023 05:22:00 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e2c974f3c0a61eb19c39c57031e709c5175b072d83a0adad056aedeab6a702`  
		Last Modified: Fri, 16 Jun 2023 05:22:00 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90970750e9471bcf7f345847d4ca2adec9d10d0f5f0df02b0c8d1cd0b4b0d5c3`  
		Last Modified: Fri, 16 Jun 2023 05:22:16 GMT  
		Size: 393.7 MB (393734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:34ccc1bd75af18944b35db27f14a3747b099d89c062ebbae6d1ce13b4c3afd1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.1 MB (615092882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a0584d04469afc9b6f9b5dabf6d8c470fa180ae3aeb3b7a28fd24a8ae6e59e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:34:28 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:34:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=978819870e976f903ecfb68a8e22ee5ea498779ee14a0c4d9f0f98fc29230ccb NEO4J_TARBALL=neo4j-enterprise-5.9.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:34:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
# Tue, 04 Jul 2023 06:34:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:34:54 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Tue, 04 Jul 2023 06:35:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:35:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:35:13 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:35:13 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:35:14 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:35:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:35:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275827ff61a5cc842494b7c486dc8fd020f878ff693af5f57969cf5f7481a0d0`  
		Last Modified: Tue, 04 Jul 2023 06:36:29 GMT  
		Size: 191.4 MB (191387687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd0804164ff5a7a8bac70caaa09e39349c9e0dbb8baef6d0ff03058ca910cac`  
		Last Modified: Tue, 04 Jul 2023 06:36:48 GMT  
		Size: 3.9 KB (3892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a8710006fb7822fddd6ed807ef02ffd3ec563cea959c37a3bf53fca4f7d956`  
		Last Modified: Tue, 04 Jul 2023 06:36:49 GMT  
		Size: 9.4 KB (9370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38a745a710edaf1eadcb2d76e64bd6030fb941963f87a919d7e899aaee490fa`  
		Last Modified: Tue, 04 Jul 2023 06:37:02 GMT  
		Size: 393.6 MB (393628976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.9`

```console
$ docker pull neo4j@sha256:95de8dc67e16abc946a16d385bba05080f06f7590170d58f788d179ce5d8621e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.9` - linux; amd64

```console
$ docker pull neo4j@sha256:fa8f71d6091bc76419f571acd04d30fd654642c7f834e5d671f637303611425d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339764660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246f3b226b168f5342e28e71b7502c2fe6bf1d2afe536b7694ce2cb9cd99c25`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:19:27 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:30 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:19:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:19:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:19:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:19:50 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:19:50 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:19:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:19:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16587156d6d664ce45c78f53fd4abf3903d66718d37c56e9d942121e5a5c2298`  
		Last Modified: Fri, 16 Jun 2023 05:21:41 GMT  
		Size: 192.6 MB (192580339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf092e6a4075a792e6cfdfa941697da3110c57b3eed1a6514ac06fb653fcd446`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 3.9 KB (3853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e8789f08f62ffed6acd775d54345f8ffdcc301329b64e9c9b676d8782c8ae`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b62bb6d5e4ab5cd0b4e67117c58f65929c22d74141894345bac35d9df4bf77`  
		Last Modified: Fri, 16 Jun 2023 05:21:34 GMT  
		Size: 115.8 MB (115753684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ab9c060c7ff61a54b35a7b38fc09f4cb143f210c2c7711c04d19802b0b97f10f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337110137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2aa94390a4d91363d5896f5f9c83921b57d038fa1fefc849bf32f4c662ab5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:34:28 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:34:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:34:32 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Tue, 04 Jul 2023 06:34:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:34:33 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Tue, 04 Jul 2023 06:34:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:34:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:34:48 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:34:49 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:34:49 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:34:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:34:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275827ff61a5cc842494b7c486dc8fd020f878ff693af5f57969cf5f7481a0d0`  
		Last Modified: Tue, 04 Jul 2023 06:36:29 GMT  
		Size: 191.4 MB (191387687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31bbf0eb561b1650f22e928cbeccb17872671effa64cad96c568923c773c5e1`  
		Last Modified: Tue, 04 Jul 2023 06:36:18 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7602e07641dac1311b8a2427efdb849b9749894a1a9ed64979931ed3d6f03bdc`  
		Last Modified: Tue, 04 Jul 2023 06:36:18 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925b08e9954cc34ec2861c0b6ea5ade09ae1a9361db08e6c22d2c5eba5010b65`  
		Last Modified: Tue, 04 Jul 2023 06:36:23 GMT  
		Size: 115.6 MB (115646236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.9-community`

```console
$ docker pull neo4j@sha256:95de8dc67e16abc946a16d385bba05080f06f7590170d58f788d179ce5d8621e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.9-community` - linux; amd64

```console
$ docker pull neo4j@sha256:fa8f71d6091bc76419f571acd04d30fd654642c7f834e5d671f637303611425d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339764660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246f3b226b168f5342e28e71b7502c2fe6bf1d2afe536b7694ce2cb9cd99c25`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:19:27 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:30 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:19:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:19:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:19:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:19:50 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:19:50 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:19:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:19:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16587156d6d664ce45c78f53fd4abf3903d66718d37c56e9d942121e5a5c2298`  
		Last Modified: Fri, 16 Jun 2023 05:21:41 GMT  
		Size: 192.6 MB (192580339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf092e6a4075a792e6cfdfa941697da3110c57b3eed1a6514ac06fb653fcd446`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 3.9 KB (3853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e8789f08f62ffed6acd775d54345f8ffdcc301329b64e9c9b676d8782c8ae`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b62bb6d5e4ab5cd0b4e67117c58f65929c22d74141894345bac35d9df4bf77`  
		Last Modified: Fri, 16 Jun 2023 05:21:34 GMT  
		Size: 115.8 MB (115753684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.9-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ab9c060c7ff61a54b35a7b38fc09f4cb143f210c2c7711c04d19802b0b97f10f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337110137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2aa94390a4d91363d5896f5f9c83921b57d038fa1fefc849bf32f4c662ab5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:34:28 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:34:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:34:32 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Tue, 04 Jul 2023 06:34:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:34:33 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Tue, 04 Jul 2023 06:34:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:34:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:34:48 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:34:49 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:34:49 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:34:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:34:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275827ff61a5cc842494b7c486dc8fd020f878ff693af5f57969cf5f7481a0d0`  
		Last Modified: Tue, 04 Jul 2023 06:36:29 GMT  
		Size: 191.4 MB (191387687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31bbf0eb561b1650f22e928cbeccb17872671effa64cad96c568923c773c5e1`  
		Last Modified: Tue, 04 Jul 2023 06:36:18 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7602e07641dac1311b8a2427efdb849b9749894a1a9ed64979931ed3d6f03bdc`  
		Last Modified: Tue, 04 Jul 2023 06:36:18 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925b08e9954cc34ec2861c0b6ea5ade09ae1a9361db08e6c22d2c5eba5010b65`  
		Last Modified: Tue, 04 Jul 2023 06:36:23 GMT  
		Size: 115.6 MB (115646236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.9-enterprise`

```console
$ docker pull neo4j@sha256:2eca6bc1d822cbcab980141695125300a92cecf26346740349684e67f13292fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.9-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:631f6f6c38f7f4ec8c242c835170dd208889b6ff1d1974cd91c0befd909abd57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.7 MB (617745683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5355d4b7934f264f871f69865b91102fe63a65413e2e8fd09238b57a3c35c3c1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:19:27 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:19:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=978819870e976f903ecfb68a8e22ee5ea498779ee14a0c4d9f0f98fc29230ccb NEO4J_TARBALL=neo4j-enterprise-5.9.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:58 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:20:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:20:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:20:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:20:18 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:20:18 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:20:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:20:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16587156d6d664ce45c78f53fd4abf3903d66718d37c56e9d942121e5a5c2298`  
		Last Modified: Fri, 16 Jun 2023 05:21:41 GMT  
		Size: 192.6 MB (192580339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfeefc867edcf7d51cc01312e1d1db4f53976bc6bbc672ee592afe405e904eb4`  
		Last Modified: Fri, 16 Jun 2023 05:22:00 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e2c974f3c0a61eb19c39c57031e709c5175b072d83a0adad056aedeab6a702`  
		Last Modified: Fri, 16 Jun 2023 05:22:00 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90970750e9471bcf7f345847d4ca2adec9d10d0f5f0df02b0c8d1cd0b4b0d5c3`  
		Last Modified: Fri, 16 Jun 2023 05:22:16 GMT  
		Size: 393.7 MB (393734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.9-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:34ccc1bd75af18944b35db27f14a3747b099d89c062ebbae6d1ce13b4c3afd1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.1 MB (615092882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a0584d04469afc9b6f9b5dabf6d8c470fa180ae3aeb3b7a28fd24a8ae6e59e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:34:28 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:34:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=978819870e976f903ecfb68a8e22ee5ea498779ee14a0c4d9f0f98fc29230ccb NEO4J_TARBALL=neo4j-enterprise-5.9.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:34:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
# Tue, 04 Jul 2023 06:34:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:34:54 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Tue, 04 Jul 2023 06:35:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:35:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:35:13 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:35:13 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:35:14 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:35:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:35:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275827ff61a5cc842494b7c486dc8fd020f878ff693af5f57969cf5f7481a0d0`  
		Last Modified: Tue, 04 Jul 2023 06:36:29 GMT  
		Size: 191.4 MB (191387687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd0804164ff5a7a8bac70caaa09e39349c9e0dbb8baef6d0ff03058ca910cac`  
		Last Modified: Tue, 04 Jul 2023 06:36:48 GMT  
		Size: 3.9 KB (3892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a8710006fb7822fddd6ed807ef02ffd3ec563cea959c37a3bf53fca4f7d956`  
		Last Modified: Tue, 04 Jul 2023 06:36:49 GMT  
		Size: 9.4 KB (9370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38a745a710edaf1eadcb2d76e64bd6030fb941963f87a919d7e899aaee490fa`  
		Last Modified: Tue, 04 Jul 2023 06:37:02 GMT  
		Size: 393.6 MB (393628976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.9.0`

```console
$ docker pull neo4j@sha256:95de8dc67e16abc946a16d385bba05080f06f7590170d58f788d179ce5d8621e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.9.0` - linux; amd64

```console
$ docker pull neo4j@sha256:fa8f71d6091bc76419f571acd04d30fd654642c7f834e5d671f637303611425d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339764660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246f3b226b168f5342e28e71b7502c2fe6bf1d2afe536b7694ce2cb9cd99c25`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:19:27 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:30 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:19:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:19:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:19:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:19:50 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:19:50 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:19:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:19:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16587156d6d664ce45c78f53fd4abf3903d66718d37c56e9d942121e5a5c2298`  
		Last Modified: Fri, 16 Jun 2023 05:21:41 GMT  
		Size: 192.6 MB (192580339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf092e6a4075a792e6cfdfa941697da3110c57b3eed1a6514ac06fb653fcd446`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 3.9 KB (3853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e8789f08f62ffed6acd775d54345f8ffdcc301329b64e9c9b676d8782c8ae`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b62bb6d5e4ab5cd0b4e67117c58f65929c22d74141894345bac35d9df4bf77`  
		Last Modified: Fri, 16 Jun 2023 05:21:34 GMT  
		Size: 115.8 MB (115753684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.9.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ab9c060c7ff61a54b35a7b38fc09f4cb143f210c2c7711c04d19802b0b97f10f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337110137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2aa94390a4d91363d5896f5f9c83921b57d038fa1fefc849bf32f4c662ab5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:34:28 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:34:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:34:32 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Tue, 04 Jul 2023 06:34:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:34:33 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Tue, 04 Jul 2023 06:34:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:34:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:34:48 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:34:49 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:34:49 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:34:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:34:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275827ff61a5cc842494b7c486dc8fd020f878ff693af5f57969cf5f7481a0d0`  
		Last Modified: Tue, 04 Jul 2023 06:36:29 GMT  
		Size: 191.4 MB (191387687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31bbf0eb561b1650f22e928cbeccb17872671effa64cad96c568923c773c5e1`  
		Last Modified: Tue, 04 Jul 2023 06:36:18 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7602e07641dac1311b8a2427efdb849b9749894a1a9ed64979931ed3d6f03bdc`  
		Last Modified: Tue, 04 Jul 2023 06:36:18 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925b08e9954cc34ec2861c0b6ea5ade09ae1a9361db08e6c22d2c5eba5010b65`  
		Last Modified: Tue, 04 Jul 2023 06:36:23 GMT  
		Size: 115.6 MB (115646236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.9.0-community`

```console
$ docker pull neo4j@sha256:95de8dc67e16abc946a16d385bba05080f06f7590170d58f788d179ce5d8621e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.9.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:fa8f71d6091bc76419f571acd04d30fd654642c7f834e5d671f637303611425d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339764660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246f3b226b168f5342e28e71b7502c2fe6bf1d2afe536b7694ce2cb9cd99c25`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:19:27 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:30 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:19:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:19:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:19:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:19:50 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:19:50 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:19:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:19:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16587156d6d664ce45c78f53fd4abf3903d66718d37c56e9d942121e5a5c2298`  
		Last Modified: Fri, 16 Jun 2023 05:21:41 GMT  
		Size: 192.6 MB (192580339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf092e6a4075a792e6cfdfa941697da3110c57b3eed1a6514ac06fb653fcd446`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 3.9 KB (3853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e8789f08f62ffed6acd775d54345f8ffdcc301329b64e9c9b676d8782c8ae`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b62bb6d5e4ab5cd0b4e67117c58f65929c22d74141894345bac35d9df4bf77`  
		Last Modified: Fri, 16 Jun 2023 05:21:34 GMT  
		Size: 115.8 MB (115753684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.9.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ab9c060c7ff61a54b35a7b38fc09f4cb143f210c2c7711c04d19802b0b97f10f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337110137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2aa94390a4d91363d5896f5f9c83921b57d038fa1fefc849bf32f4c662ab5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:34:28 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:34:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:34:32 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Tue, 04 Jul 2023 06:34:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:34:33 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Tue, 04 Jul 2023 06:34:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:34:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:34:48 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:34:49 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:34:49 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:34:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:34:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275827ff61a5cc842494b7c486dc8fd020f878ff693af5f57969cf5f7481a0d0`  
		Last Modified: Tue, 04 Jul 2023 06:36:29 GMT  
		Size: 191.4 MB (191387687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31bbf0eb561b1650f22e928cbeccb17872671effa64cad96c568923c773c5e1`  
		Last Modified: Tue, 04 Jul 2023 06:36:18 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7602e07641dac1311b8a2427efdb849b9749894a1a9ed64979931ed3d6f03bdc`  
		Last Modified: Tue, 04 Jul 2023 06:36:18 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925b08e9954cc34ec2861c0b6ea5ade09ae1a9361db08e6c22d2c5eba5010b65`  
		Last Modified: Tue, 04 Jul 2023 06:36:23 GMT  
		Size: 115.6 MB (115646236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.9.0-enterprise`

```console
$ docker pull neo4j@sha256:2eca6bc1d822cbcab980141695125300a92cecf26346740349684e67f13292fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.9.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:631f6f6c38f7f4ec8c242c835170dd208889b6ff1d1974cd91c0befd909abd57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.7 MB (617745683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5355d4b7934f264f871f69865b91102fe63a65413e2e8fd09238b57a3c35c3c1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:19:27 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:19:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=978819870e976f903ecfb68a8e22ee5ea498779ee14a0c4d9f0f98fc29230ccb NEO4J_TARBALL=neo4j-enterprise-5.9.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:58 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:20:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:20:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:20:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:20:18 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:20:18 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:20:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:20:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16587156d6d664ce45c78f53fd4abf3903d66718d37c56e9d942121e5a5c2298`  
		Last Modified: Fri, 16 Jun 2023 05:21:41 GMT  
		Size: 192.6 MB (192580339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfeefc867edcf7d51cc01312e1d1db4f53976bc6bbc672ee592afe405e904eb4`  
		Last Modified: Fri, 16 Jun 2023 05:22:00 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e2c974f3c0a61eb19c39c57031e709c5175b072d83a0adad056aedeab6a702`  
		Last Modified: Fri, 16 Jun 2023 05:22:00 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90970750e9471bcf7f345847d4ca2adec9d10d0f5f0df02b0c8d1cd0b4b0d5c3`  
		Last Modified: Fri, 16 Jun 2023 05:22:16 GMT  
		Size: 393.7 MB (393734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.9.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:34ccc1bd75af18944b35db27f14a3747b099d89c062ebbae6d1ce13b4c3afd1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.1 MB (615092882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a0584d04469afc9b6f9b5dabf6d8c470fa180ae3aeb3b7a28fd24a8ae6e59e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:34:28 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:34:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=978819870e976f903ecfb68a8e22ee5ea498779ee14a0c4d9f0f98fc29230ccb NEO4J_TARBALL=neo4j-enterprise-5.9.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:34:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
# Tue, 04 Jul 2023 06:34:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:34:54 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Tue, 04 Jul 2023 06:35:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:35:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:35:13 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:35:13 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:35:14 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:35:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:35:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275827ff61a5cc842494b7c486dc8fd020f878ff693af5f57969cf5f7481a0d0`  
		Last Modified: Tue, 04 Jul 2023 06:36:29 GMT  
		Size: 191.4 MB (191387687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd0804164ff5a7a8bac70caaa09e39349c9e0dbb8baef6d0ff03058ca910cac`  
		Last Modified: Tue, 04 Jul 2023 06:36:48 GMT  
		Size: 3.9 KB (3892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a8710006fb7822fddd6ed807ef02ffd3ec563cea959c37a3bf53fca4f7d956`  
		Last Modified: Tue, 04 Jul 2023 06:36:49 GMT  
		Size: 9.4 KB (9370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38a745a710edaf1eadcb2d76e64bd6030fb941963f87a919d7e899aaee490fa`  
		Last Modified: Tue, 04 Jul 2023 06:37:02 GMT  
		Size: 393.6 MB (393628976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:95de8dc67e16abc946a16d385bba05080f06f7590170d58f788d179ce5d8621e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:fa8f71d6091bc76419f571acd04d30fd654642c7f834e5d671f637303611425d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339764660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246f3b226b168f5342e28e71b7502c2fe6bf1d2afe536b7694ce2cb9cd99c25`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:19:27 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:30 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:19:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:19:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:19:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:19:50 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:19:50 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:19:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:19:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16587156d6d664ce45c78f53fd4abf3903d66718d37c56e9d942121e5a5c2298`  
		Last Modified: Fri, 16 Jun 2023 05:21:41 GMT  
		Size: 192.6 MB (192580339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf092e6a4075a792e6cfdfa941697da3110c57b3eed1a6514ac06fb653fcd446`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 3.9 KB (3853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e8789f08f62ffed6acd775d54345f8ffdcc301329b64e9c9b676d8782c8ae`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b62bb6d5e4ab5cd0b4e67117c58f65929c22d74141894345bac35d9df4bf77`  
		Last Modified: Fri, 16 Jun 2023 05:21:34 GMT  
		Size: 115.8 MB (115753684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ab9c060c7ff61a54b35a7b38fc09f4cb143f210c2c7711c04d19802b0b97f10f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337110137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2aa94390a4d91363d5896f5f9c83921b57d038fa1fefc849bf32f4c662ab5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:34:28 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:34:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:34:32 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Tue, 04 Jul 2023 06:34:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:34:33 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Tue, 04 Jul 2023 06:34:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:34:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:34:48 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:34:49 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:34:49 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:34:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:34:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275827ff61a5cc842494b7c486dc8fd020f878ff693af5f57969cf5f7481a0d0`  
		Last Modified: Tue, 04 Jul 2023 06:36:29 GMT  
		Size: 191.4 MB (191387687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31bbf0eb561b1650f22e928cbeccb17872671effa64cad96c568923c773c5e1`  
		Last Modified: Tue, 04 Jul 2023 06:36:18 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7602e07641dac1311b8a2427efdb849b9749894a1a9ed64979931ed3d6f03bdc`  
		Last Modified: Tue, 04 Jul 2023 06:36:18 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925b08e9954cc34ec2861c0b6ea5ade09ae1a9361db08e6c22d2c5eba5010b65`  
		Last Modified: Tue, 04 Jul 2023 06:36:23 GMT  
		Size: 115.6 MB (115646236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:2eca6bc1d822cbcab980141695125300a92cecf26346740349684e67f13292fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:631f6f6c38f7f4ec8c242c835170dd208889b6ff1d1974cd91c0befd909abd57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.7 MB (617745683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5355d4b7934f264f871f69865b91102fe63a65413e2e8fd09238b57a3c35c3c1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:19:27 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:19:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=978819870e976f903ecfb68a8e22ee5ea498779ee14a0c4d9f0f98fc29230ccb NEO4J_TARBALL=neo4j-enterprise-5.9.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:57 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:58 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:20:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:20:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:20:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:20:18 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:20:18 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:20:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:20:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16587156d6d664ce45c78f53fd4abf3903d66718d37c56e9d942121e5a5c2298`  
		Last Modified: Fri, 16 Jun 2023 05:21:41 GMT  
		Size: 192.6 MB (192580339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfeefc867edcf7d51cc01312e1d1db4f53976bc6bbc672ee592afe405e904eb4`  
		Last Modified: Fri, 16 Jun 2023 05:22:00 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e2c974f3c0a61eb19c39c57031e709c5175b072d83a0adad056aedeab6a702`  
		Last Modified: Fri, 16 Jun 2023 05:22:00 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90970750e9471bcf7f345847d4ca2adec9d10d0f5f0df02b0c8d1cd0b4b0d5c3`  
		Last Modified: Fri, 16 Jun 2023 05:22:16 GMT  
		Size: 393.7 MB (393734706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:34ccc1bd75af18944b35db27f14a3747b099d89c062ebbae6d1ce13b4c3afd1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.1 MB (615092882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a0584d04469afc9b6f9b5dabf6d8c470fa180ae3aeb3b7a28fd24a8ae6e59e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:34:28 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:34:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=978819870e976f903ecfb68a8e22ee5ea498779ee14a0c4d9f0f98fc29230ccb NEO4J_TARBALL=neo4j-enterprise-5.9.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:34:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
# Tue, 04 Jul 2023 06:34:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:34:54 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Tue, 04 Jul 2023 06:35:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:35:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:35:13 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:35:13 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:35:14 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:35:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:35:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275827ff61a5cc842494b7c486dc8fd020f878ff693af5f57969cf5f7481a0d0`  
		Last Modified: Tue, 04 Jul 2023 06:36:29 GMT  
		Size: 191.4 MB (191387687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd0804164ff5a7a8bac70caaa09e39349c9e0dbb8baef6d0ff03058ca910cac`  
		Last Modified: Tue, 04 Jul 2023 06:36:48 GMT  
		Size: 3.9 KB (3892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a8710006fb7822fddd6ed807ef02ffd3ec563cea959c37a3bf53fca4f7d956`  
		Last Modified: Tue, 04 Jul 2023 06:36:49 GMT  
		Size: 9.4 KB (9370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38a745a710edaf1eadcb2d76e64bd6030fb941963f87a919d7e899aaee490fa`  
		Last Modified: Tue, 04 Jul 2023 06:37:02 GMT  
		Size: 393.6 MB (393628976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:95de8dc67e16abc946a16d385bba05080f06f7590170d58f788d179ce5d8621e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:fa8f71d6091bc76419f571acd04d30fd654642c7f834e5d671f637303611425d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339764660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b246f3b226b168f5342e28e71b7502c2fe6bf1d2afe536b7694ce2cb9cd99c25`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jun 2023 23:21:07 GMT
ADD file:5ab44909c2983e19ab6596e7e4ee9ad80e48afeb9dfe0e7224afdae7cafd25ef in / 
# Mon, 12 Jun 2023 23:21:08 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:44:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 05:19:27 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Fri, 16 Jun 2023 05:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 16 Jun 2023 05:19:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Fri, 16 Jun 2023 05:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 16 Jun 2023 05:19:30 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Fri, 16 Jun 2023 05:19:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 05:19:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 05:19:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jun 2023 05:19:50 GMT
VOLUME [/data /logs]
# Fri, 16 Jun 2023 05:19:50 GMT
EXPOSE 7473 7474 7687
# Fri, 16 Jun 2023 05:19:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:19:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:759700526b7894aa9c150feb2ebfcd00cf06d2890df739e71555edcfd13669e3`  
		Last Modified: Mon, 12 Jun 2023 23:26:30 GMT  
		Size: 31.4 MB (31417410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16587156d6d664ce45c78f53fd4abf3903d66718d37c56e9d942121e5a5c2298`  
		Last Modified: Fri, 16 Jun 2023 05:21:41 GMT  
		Size: 192.6 MB (192580339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf092e6a4075a792e6cfdfa941697da3110c57b3eed1a6514ac06fb653fcd446`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 3.9 KB (3853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158e8789f08f62ffed6acd775d54345f8ffdcc301329b64e9c9b676d8782c8ae`  
		Last Modified: Fri, 16 Jun 2023 05:21:28 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b62bb6d5e4ab5cd0b4e67117c58f65929c22d74141894345bac35d9df4bf77`  
		Last Modified: Fri, 16 Jun 2023 05:21:34 GMT  
		Size: 115.8 MB (115753684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ab9c060c7ff61a54b35a7b38fc09f4cb143f210c2c7711c04d19802b0b97f10f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337110137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2aa94390a4d91363d5896f5f9c83921b57d038fa1fefc849bf32f4c662ab5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:34:28 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:34:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5c8774afac24e8a43d1de94d7b200ed6ad27f51b6ab7802bc325f5d27992930a NEO4J_TARBALL=neo4j-community-5.9.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 04 Jul 2023 06:34:32 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
# Tue, 04 Jul 2023 06:34:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 04 Jul 2023 06:34:33 GMT
COPY multi:5d29fd3ffa43989bd2f4a4674bb74cea0fc3d966076b29cc72e8b59442142704 in /startup/ 
# Tue, 04 Jul 2023 06:34:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.9.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:34:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:34:48 GMT
WORKDIR /var/lib/neo4j
# Tue, 04 Jul 2023 06:34:49 GMT
VOLUME [/data /logs]
# Tue, 04 Jul 2023 06:34:49 GMT
EXPOSE 7473 7474 7687
# Tue, 04 Jul 2023 06:34:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 04 Jul 2023 06:34:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275827ff61a5cc842494b7c486dc8fd020f878ff693af5f57969cf5f7481a0d0`  
		Last Modified: Tue, 04 Jul 2023 06:36:29 GMT  
		Size: 191.4 MB (191387687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31bbf0eb561b1650f22e928cbeccb17872671effa64cad96c568923c773c5e1`  
		Last Modified: Tue, 04 Jul 2023 06:36:18 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7602e07641dac1311b8a2427efdb849b9749894a1a9ed64979931ed3d6f03bdc`  
		Last Modified: Tue, 04 Jul 2023 06:36:18 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925b08e9954cc34ec2861c0b6ea5ade09ae1a9361db08e6c22d2c5eba5010b65`  
		Last Modified: Tue, 04 Jul 2023 06:36:23 GMT  
		Size: 115.6 MB (115646236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
