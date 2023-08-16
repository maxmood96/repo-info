## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:67d8248d43b018202649914ce1f32e5e8769cf35086dddcdf6c1f34cbd159a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:0a6b680f256e74e1d4da1c6dd848c7347c0499ea82c616c7b6645ecf04c4e505
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.7 MB (574730694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f57457ff0c63cf2a4ae5e931021e57929fd69edbacfe2ce2428c6decbd716e2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 01:33:03 GMT
COPY dir:8ea3eea47bd8b9d37ce2403b2d64b2cdc0fec836a119c10ec3e4ff0bcca8bb4d in /opt/java/openjdk 
# Wed, 16 Aug 2023 09:14:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 16 Aug 2023 09:14:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Wed, 16 Aug 2023 09:14:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 16 Aug 2023 09:14:59 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Wed, 16 Aug 2023 09:15:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 09:15:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 09:15:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 16 Aug 2023 09:15:18 GMT
VOLUME [/data /logs]
# Wed, 16 Aug 2023 09:15:18 GMT
EXPOSE 7473 7474 7687
# Wed, 16 Aug 2023 09:15:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 16 Aug 2023 09:15:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e3c34f08976bd478d8cdd805c9120ba7dd2aeacd5c4f019c318b1b43d14a5e`  
		Last Modified: Wed, 16 Aug 2023 01:42:50 GMT  
		Size: 144.8 MB (144773799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1696b3564c7ca8f5dd4fabd89c46a0158479e813ad0afe0f5086dbf4b59fc0`  
		Last Modified: Wed, 16 Aug 2023 09:17:08 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6f0f522763a27494b0510e34887d8674851c38e662e383eb33499d4b547a0d`  
		Last Modified: Wed, 16 Aug 2023 09:17:07 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17650464d0d9cbfbb82dad9f4b95434356d0867cc5a5f270f73434dda3e3c39a`  
		Last Modified: Wed, 16 Aug 2023 09:17:24 GMT  
		Size: 398.5 MB (398526009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ef00cdc553e58483ecdddf848b2398a50ab02968adb84069f329ee9e41d15fad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.0 MB (572031843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7a6acf0f4a55f11a16afbd51dd7400bacf5a73435572ba0e956b4f2553998e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 01:51:38 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Wed, 16 Aug 2023 03:46:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3d387334532ff35c6114343fadea68657f0c600665daa5af75fce96c087c6ddc NEO4J_TARBALL=neo4j-enterprise-5.10.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 16 Aug 2023 03:46:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
# Wed, 16 Aug 2023 03:46:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 16 Aug 2023 03:46:04 GMT
COPY multi:d939a3d156891be9a8e359f0c5c2adbad24c093f1ca53494ce82d0acd2b2613d in /startup/ 
# Wed, 16 Aug 2023 03:46:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.10.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:46:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 03:46:34 GMT
WORKDIR /var/lib/neo4j
# Wed, 16 Aug 2023 03:46:34 GMT
VOLUME [/data /logs]
# Wed, 16 Aug 2023 03:46:34 GMT
EXPOSE 7473 7474 7687
# Wed, 16 Aug 2023 03:46:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 16 Aug 2023 03:46:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f16cbfa1489dec25027e54a744e2466b26edafb5b673ee5516b7f9ca7b77d19`  
		Last Modified: Wed, 16 Aug 2023 01:59:37 GMT  
		Size: 143.5 MB (143538046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2377fe355272285d4397f2572e8c38c4c7c8bbbf961ae12db66a8e55b3ce3`  
		Last Modified: Wed, 16 Aug 2023 03:48:16 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a5f580d2976a991a8eb0e2f91c35186ee121f3cfa194a5701aecda1f8a47a9`  
		Last Modified: Wed, 16 Aug 2023 03:48:15 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5a390e78d05efc74a129940a46bd24f89839b18bbafad9e59a6d7755e4f55a`  
		Last Modified: Wed, 16 Aug 2023 03:48:30 GMT  
		Size: 398.4 MB (398417742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
