## `neo4j:enterprise-trixie`

```console
$ docker pull neo4j@sha256:23917c4b53ac19367ce19c6dcf05dd125f8f6d663732239a894b8b02685c8504
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:6de0aa841bf3d003a1e07cd192c49aecf964564889376e515930d5d9e0bac728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.2 MB (515195014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0313cbabbe7cbfc9009c7a652e836ff3e528dcbe119f8f0194725ec0d3de4e2a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:57:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 02:57:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 02:57:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a47e20ec6bd7df9fd11781cba86264d530fd1f605cca817271ff7e5bbc7c3b4a NEO4J_TARBALL=neo4j-enterprise-2026.03.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 07 Apr 2026 02:57:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.03.1-unix.tar.gz
# Tue, 07 Apr 2026 02:57:52 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 07 Apr 2026 02:58:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.03.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 07 Apr 2026 02:58:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:58:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 07 Apr 2026 02:58:18 GMT
VOLUME [/data /logs]
# Tue, 07 Apr 2026 02:58:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 07 Apr 2026 02:58:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:58:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a694f1e15932153263c19815856c4b6263be9c5ee4a188bea8c3069ae87c908`  
		Last Modified: Tue, 07 Apr 2026 02:58:46 GMT  
		Size: 92.3 MB (92256277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1217d9ea4b3ada6a39028fd697ea7b84e2a3bdfa4235bf491cd79c380c8c766f`  
		Last Modified: Tue, 07 Apr 2026 02:58:43 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b85c72ac282e5b89b8f1b455e6c5b835650c73484b4aa254c5ce0968bba346`  
		Last Modified: Tue, 07 Apr 2026 02:58:52 GMT  
		Size: 393.2 MB (393153044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:da454c71466f3ce39fa1af65956aa402c6f845c6a18ffa784a9273819ad470a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4673083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296a11f65b7968636f94433bd492b8b4361cc103712e27df63fd69b692f90e91`

```dockerfile
```

-	Layers:
	-	`sha256:c33641c5e6b68da112038842f0bfd8cf60bf686147c23bb666cf6f25f3e20eb4`  
		Last Modified: Tue, 07 Apr 2026 02:58:43 GMT  
		Size: 4.7 MB (4653121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9f23ebe764c9536e337143c518fc2161230d54997a051716677d4184f1fa7ee`  
		Last Modified: Tue, 07 Apr 2026 02:58:43 GMT  
		Size: 20.0 KB (19962 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9f793b0bc208f8d1d21e0cc9d164501222fae45d2304c35ad5dc7e5917f3660f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.7 MB (513664010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09af400d42e00c915c81838c8561cc6bc1c36f6768d0d63a465f737070c28ae7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:10:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:10:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:10:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a47e20ec6bd7df9fd11781cba86264d530fd1f605cca817271ff7e5bbc7c3b4a NEO4J_TARBALL=neo4j-enterprise-2026.03.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 07 Apr 2026 03:10:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.03.1-unix.tar.gz
# Tue, 07 Apr 2026 03:10:52 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 07 Apr 2026 03:11:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.03.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 07 Apr 2026 03:11:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:11:19 GMT
WORKDIR /var/lib/neo4j
# Tue, 07 Apr 2026 03:11:19 GMT
VOLUME [/data /logs]
# Tue, 07 Apr 2026 03:11:19 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 07 Apr 2026 03:11:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 03:11:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce720478095fbdeaca2f1f2fcf749e301f31ee41c5cd98b3b706966f6b75736b`  
		Last Modified: Tue, 07 Apr 2026 03:11:50 GMT  
		Size: 91.3 MB (91288284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0430d4fa5f69933e3d8a29b10fd9b6b3d4e139b72e8728deae25a3e902781466`  
		Last Modified: Tue, 07 Apr 2026 03:11:46 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdc834e8d0efbb04e8a09a40a8f518b8188fa5539a3860d6913d184c340c771`  
		Last Modified: Tue, 07 Apr 2026 03:11:56 GMT  
		Size: 392.2 MB (392227122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:a99b4b597463747cb0fe19d2a8c175272f05ec73b6bb33c7e0b2cc34c172c4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4667737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88137e7ea03c3ebdc03c1dee40d65ab258e13cb9b408c38a6153883c5c10e48f`

```dockerfile
```

-	Layers:
	-	`sha256:3bd4714afff3c32448650aa709778bfba2249b9c83e0aa97830eff0dec43ebed`  
		Last Modified: Tue, 07 Apr 2026 03:11:47 GMT  
		Size: 4.6 MB (4647596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f54e6d3b3c0a356e13c76d48da582c441c477c527ae243c277037782ce3920d7`  
		Last Modified: Tue, 07 Apr 2026 03:11:46 GMT  
		Size: 20.1 KB (20141 bytes)  
		MIME: application/vnd.in-toto+json
