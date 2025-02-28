## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:bc9381fa6e5f83c774efdd851e42494a8641a9c81e7cc0d470544f5ca4761af8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:03fc8da33ff5df2374b00934ec228748cc5ff3eea3ab9623c92abae692d42e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.5 MB (348476484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1113df41736d2e40dc64632522a4d36605708f782fc4256c440983ecab43cb5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Thu, 27 Feb 2025 14:20:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Feb 2025 14:20:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=95ec43f4502668d5f7ba3af8e0791d91b1cbd61f74133ef15d75068013bf1149 NEO4J_TARBALL=neo4j-community-2025.02.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 27 Feb 2025 14:20:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.02.0-unix.tar.gz
# Thu, 27 Feb 2025 14:20:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.02.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.02.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2025 14:20:06 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Feb 2025 14:20:06 GMT
VOLUME [/data /logs]
# Thu, 27 Feb 2025 14:20:06 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Feb 2025 14:20:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Feb 2025 14:20:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181c20c39eb3c95490a796756c249bc0b031d22a2b97bc5771dba68f16ef4df`  
		Last Modified: Fri, 28 Feb 2025 18:31:28 GMT  
		Size: 157.6 MB (157585892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6059a4a25ccd10b685c9d6fa40e772b698887eb3f0e9a564d6e08d1998137c`  
		Last Modified: Fri, 28 Feb 2025 18:31:25 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75774c36a6f8467933c357986d5503e6db1c80daa57de342e86cbf4bf628b38c`  
		Last Modified: Fri, 28 Feb 2025 18:31:25 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617430850f661f61869f94ce46a2d30333f3cc4bcb26a0bf831946eeb0b65704`  
		Last Modified: Fri, 28 Feb 2025 18:31:28 GMT  
		Size: 160.6 MB (160622762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:79e65b91317b0a818cd4bdac0b3600f42435f82b5874fa4754ef4e99df05a7c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3261533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0202d6286479ba6b7e1194bce59ff9620e3bcb871db2ef55960a378e7f1e3539`

```dockerfile
```

-	Layers:
	-	`sha256:c429b0add9f424c35e03ba466cb37b507cc428977ef3625440b8f14f5a6ece70`  
		Last Modified: Fri, 28 Feb 2025 18:31:25 GMT  
		Size: 3.2 MB (3237680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58c32bd5fb01ab846e37aa9ef522cfce570860617a70dd1406d47b66e0b06b92`  
		Last Modified: Fri, 28 Feb 2025 18:31:26 GMT  
		Size: 23.9 KB (23853 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a17d9772449df04bf30e0d6561918040e2fe6d525f0f31adbf9dd812a0438418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345203790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab93ed892373ef5c3b211019fbe8b5c86037f738aa43e1c03f60950d79ba591`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Thu, 27 Feb 2025 14:20:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Feb 2025 14:20:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=95ec43f4502668d5f7ba3af8e0791d91b1cbd61f74133ef15d75068013bf1149 NEO4J_TARBALL=neo4j-community-2025.02.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 27 Feb 2025 14:20:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.02.0-unix.tar.gz
# Thu, 27 Feb 2025 14:20:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.02.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.02.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2025 14:20:06 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Feb 2025 14:20:06 GMT
VOLUME [/data /logs]
# Thu, 27 Feb 2025 14:20:06 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Feb 2025 14:20:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Feb 2025 14:20:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b45bcdca7ffe879eb2c91c1ba7c5b68f5883aa9fee954f831d0b8624c4e031`  
		Last Modified: Fri, 28 Feb 2025 18:31:17 GMT  
		Size: 155.9 MB (155859251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4548176648bcae1ed128ecef9b1ebb7a47d6307ad572a54cf9f5a93d89a8e4e8`  
		Last Modified: Fri, 28 Feb 2025 18:31:14 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af62efa99c8f591476769249bf8d5f3d4ab1a0d4e2bff5b9039e00b6f7e4858`  
		Last Modified: Fri, 28 Feb 2025 18:31:14 GMT  
		Size: 10.0 KB (10025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb31d486231d27d1bd47654b1e2114a26cd832226d998b77ef7c2e033ef1d25`  
		Last Modified: Fri, 28 Feb 2025 18:31:18 GMT  
		Size: 160.6 MB (160584630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ccd69adc9c64cd95c812b8fc2c09588ce23545d6ce60346e9cff2e8de1be0085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3261613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26d40e326825d0380c02d7c039c79be095982490b53502db99fc5204ca0ed24`

```dockerfile
```

-	Layers:
	-	`sha256:e10efc9ccbfe93e0a4c76719530ed197898b962115de34e026c93d606af0ca76`  
		Last Modified: Fri, 28 Feb 2025 18:31:14 GMT  
		Size: 3.2 MB (3237470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d6cdd83be54886880f4f0f4745e74a201bbcf6062aaee01d3cc0c29d9ec545b`  
		Last Modified: Fri, 28 Feb 2025 18:31:14 GMT  
		Size: 24.1 KB (24143 bytes)  
		MIME: application/vnd.in-toto+json
