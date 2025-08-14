## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:1bff40bc58ba12dc15ba2b366f0ddcfaf456f725c4271113e4b5a8e1f4f3cff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:3d72bbb8855f14b6cf8cf744e48940e0828ba466e83b0c5fe4cbf6733ebadf85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.9 MB (649858991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62580272d5c8dad2d42ad80683a3eec3436a091329162c4d93acf715484b22c3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 04 Aug 2025 08:17:16 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Mon, 04 Aug 2025 08:17:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 04 Aug 2025 08:17:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 04 Aug 2025 08:17:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ee7279cfca57e0441d277992daab5ffd02501a111dfce50c398da0ba6a2d9227 NEO4J_TARBALL=neo4j-enterprise-5.26.10-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 04 Aug 2025 08:17:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.10-unix.tar.gz
# Mon, 04 Aug 2025 08:17:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.10-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 04 Aug 2025 08:17:16 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 04 Aug 2025 08:17:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.10-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 04 Aug 2025 08:17:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 08:17:16 GMT
WORKDIR /var/lib/neo4j
# Mon, 04 Aug 2025 08:17:16 GMT
VOLUME [/data /logs]
# Mon, 04 Aug 2025 08:17:16 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 04 Aug 2025 08:17:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 04 Aug 2025 08:17:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6213a73a1db8073926eaded67593989d256acd23e7c5a9b719a3ec0bfdf2bb`  
		Last Modified: Tue, 12 Aug 2025 23:45:23 GMT  
		Size: 144.7 MB (144693312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be08b49978a9cee380a22f9ef9ff3976f1aee5f32c576be2e4bb85bd89407e0a`  
		Last Modified: Tue, 12 Aug 2025 21:25:35 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e813323b48313f2995b7a7233edfa5b112512d21548984b624cec697b8d766e`  
		Last Modified: Tue, 12 Aug 2025 21:25:36 GMT  
		Size: 10.0 KB (10030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c255ba658d40b2938c70adb034c28d75190d77fa8eb260926d6eb066930acbe`  
		Last Modified: Tue, 12 Aug 2025 23:46:00 GMT  
		Size: 474.9 MB (474895660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:fce4c1e722556f17273940c759be44ef432ffabd90fb48399b0ce5f01ac215d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4882110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c76ed5409eac246cff08f4b3d6ec4464228e6c540f1ea6a6b3711167e075bf9`

```dockerfile
```

-	Layers:
	-	`sha256:e211e9497989bd58289531224e7f29cb083993c9e758ecec0edf71aefc50ab03`  
		Last Modified: Tue, 12 Aug 2025 23:44:04 GMT  
		Size: 4.9 MB (4861082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d4d6533ef92c00a51dcffc6e8af8bb5c1fc6f643e64d9fa6e31410fd8093e36`  
		Last Modified: Tue, 12 Aug 2025 23:44:05 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bac64872e61f91450a70a36b8a248c561f92beaa7ae814e70110b602497d07d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.4 MB (646446140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4a69950a973362a1086590c4315eda0cb3c6fcb7dfec2b26364d7d1804d7b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 04 Aug 2025 08:17:16 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Mon, 04 Aug 2025 08:17:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 04 Aug 2025 08:17:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 04 Aug 2025 08:17:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ee7279cfca57e0441d277992daab5ffd02501a111dfce50c398da0ba6a2d9227 NEO4J_TARBALL=neo4j-enterprise-5.26.10-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 04 Aug 2025 08:17:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.10-unix.tar.gz
# Mon, 04 Aug 2025 08:17:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.10-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 04 Aug 2025 08:17:16 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 04 Aug 2025 08:17:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.10-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 04 Aug 2025 08:17:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 Aug 2025 08:17:16 GMT
WORKDIR /var/lib/neo4j
# Mon, 04 Aug 2025 08:17:16 GMT
VOLUME [/data /logs]
# Mon, 04 Aug 2025 08:17:16 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 04 Aug 2025 08:17:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 04 Aug 2025 08:17:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554132d4fbb3932b7e2b1bcec38abd85ae0c20704c81e7370c80cad692f6108c`  
		Last Modified: Wed, 13 Aug 2025 08:47:16 GMT  
		Size: 143.5 MB (143542152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3784601156146b5f8b1f065b6cc11f416ba0b32db6cdf3275d94a50d2b3963`  
		Last Modified: Wed, 13 Aug 2025 11:10:51 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d406fccb33b9cd9fdcf84a6b4eee638770293a1d0eec30fe25c33126573059`  
		Last Modified: Wed, 13 Aug 2025 11:10:50 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194cfa7fdaac91618f9345ee94f467fc96b6f104d41533a7c6dd53b7132f2be3`  
		Last Modified: Wed, 13 Aug 2025 11:11:56 GMT  
		Size: 474.1 MB (474139567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:7c9ac4505b340463265427cf7b7e7c9a382e067f9c3e09d6a2e29200951796b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4856084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741d3483d90c104adf029f9f1a789be950de1d127a21e77f2ec3d962f19903a6`

```dockerfile
```

-	Layers:
	-	`sha256:bc95defd2fc3391eca2fa24ee43d406e52698aa7e9af98fdd09a13bc4daffced`  
		Last Modified: Wed, 13 Aug 2025 08:44:08 GMT  
		Size: 4.8 MB (4834887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2281c73b2628a556bac8bd95f3ca848de80acc6adc5d5c2dee533759a06dd61f`  
		Last Modified: Wed, 13 Aug 2025 08:44:09 GMT  
		Size: 21.2 KB (21197 bytes)  
		MIME: application/vnd.in-toto+json
