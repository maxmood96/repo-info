## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:c3e7f7491d0807081f35105183cd94f2c3670c770e899ccdb674a1efd80534c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:239052cf244db11d46e94cd6f19fb8f872053005f5c573c3ad22da656ef83d40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339684863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4d337b0e4d756ba9f6aad8da811a40edad4be7190a33c047fdb1c9e769c2e93`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Apr 2023 20:09:11 GMT
COPY dir:097a611561277927a8e367a60640ce12877b7a6373689dec24d5cfb76f99c807 in /opt/java/openjdk 
# Wed, 26 Apr 2023 23:04:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e13e94d8c8730f9525f30f98821ade79b349af1697d7ac94a8c3cc8b0273b734 NEO4J_TARBALL=neo4j-community-5.7.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 26 Apr 2023 23:04:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
# Wed, 26 Apr 2023 23:04:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 26 Apr 2023 23:04:10 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Wed, 26 Apr 2023 23:04:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Apr 2023 23:04:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 23:04:22 GMT
WORKDIR /var/lib/neo4j
# Wed, 26 Apr 2023 23:04:22 GMT
VOLUME [/data /logs]
# Wed, 26 Apr 2023 23:04:22 GMT
EXPOSE 7473 7474 7687
# Wed, 26 Apr 2023 23:04:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 26 Apr 2023 23:04:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3dca630898b65b3e3d97ffce265d16549a24facef0348fd8a6d8d5aee0493b3`  
		Last Modified: Wed, 26 Apr 2023 20:24:23 GMT  
		Size: 192.6 MB (192580428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32afad0266c5803624d5b4c47e109eb8d119463a5852079be3be2cff297d0554`  
		Last Modified: Wed, 26 Apr 2023 23:05:31 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7bb8bb021d620689e3020e8541a8d04126164cec4845a5094b311e79ff0904f`  
		Last Modified: Wed, 26 Apr 2023 23:05:31 GMT  
		Size: 8.8 KB (8769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5e887c054981c5032f22462900a7b701380746421009661f9b39c9b17815c8`  
		Last Modified: Wed, 26 Apr 2023 23:05:37 GMT  
		Size: 115.7 MB (115673577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9de981c249476aed2d470bd0a64c6c95ad6abb4f30eca2bcd7f7b529b82cd5fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.0 MB (336992978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911bc4820ee3b1ebdf4b195296330d3d68653b046cdd332f811cfa4a5ee20a30`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Apr 2023 20:43:30 GMT
COPY dir:d3d9f08d06fd1214b20f5d901cee398f498773bedf69f0d3cc795772967cfe44 in /opt/java/openjdk 
# Wed, 26 Apr 2023 21:27:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e13e94d8c8730f9525f30f98821ade79b349af1697d7ac94a8c3cc8b0273b734 NEO4J_TARBALL=neo4j-community-5.7.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 26 Apr 2023 21:27:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
# Wed, 26 Apr 2023 21:27:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 26 Apr 2023 21:27:45 GMT
COPY multi:231d2413caca967db6cb3937a1975c89c8f725750a4c6cb2893820fb868a6427 in /startup/ 
# Wed, 26 Apr 2023 21:27:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.7.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Apr 2023 21:27:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 21:27:59 GMT
WORKDIR /var/lib/neo4j
# Wed, 26 Apr 2023 21:27:59 GMT
VOLUME [/data /logs]
# Wed, 26 Apr 2023 21:28:00 GMT
EXPOSE 7473 7474 7687
# Wed, 26 Apr 2023 21:28:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 26 Apr 2023 21:28:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583bb3029fa1410e5fe69cb8c1d3ec8b162189c224628b2cfd41d97a9456f302`  
		Last Modified: Wed, 26 Apr 2023 20:55:49 GMT  
		Size: 191.4 MB (191387717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f22869964797c26a880d19258a72293d0bb501248977a1636458a29cb0fba2e`  
		Last Modified: Wed, 26 Apr 2023 21:29:19 GMT  
		Size: 3.9 KB (3891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870e2644b69ccd34825e7c1df21335c57df205040882fdfb32df7f90fb50adf9`  
		Last Modified: Wed, 26 Apr 2023 21:29:19 GMT  
		Size: 8.8 KB (8770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00c5cb17f5c2b02cb670db33650af90684c6ff5d9f0883f070ff8596491e02c`  
		Last Modified: Wed, 26 Apr 2023 21:29:23 GMT  
		Size: 115.5 MB (115528774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
