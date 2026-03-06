## `neo4j:community-trixie`

```console
$ docker pull neo4j@sha256:7bbe414ef4c1e1184284b2f4dcb19fb8c7e03126b540a77907b2e4d07014b4af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:5d1e3786f2b2ea094792eea96bf77041d0678b46680fbcf7552a4a6def6821a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.6 MB (384590631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:135aabcff3123242140805ed583d6ed9e15073d54df45d11f47f2fec57d3b649`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 18:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Mar 2026 18:21:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Mar 2026 18:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e95626e21348a30109799a44639c2169bc24e27e1a1371972ff2583c3d8493c NEO4J_TARBALL=neo4j-community-2026.02.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 06 Mar 2026 18:21:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.2-unix.tar.gz
# Fri, 06 Mar 2026 18:21:59 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 06 Mar 2026 18:22:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.2-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 06 Mar 2026 18:22:32 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 18:22:32 GMT
WORKDIR /var/lib/neo4j
# Fri, 06 Mar 2026 18:22:32 GMT
VOLUME [/data /logs]
# Fri, 06 Mar 2026 18:22:32 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 06 Mar 2026 18:22:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 06 Mar 2026 18:22:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32303d1841b246b5f3248ef156b44edc750c67d53f015ec9baa800b73391b39c`  
		Last Modified: Fri, 06 Mar 2026 18:22:57 GMT  
		Size: 92.3 MB (92256315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110041cf81119275200c3c80e54b8adb242213afa597b3150d8292d9762a8cdb`  
		Last Modified: Fri, 06 Mar 2026 18:22:53 GMT  
		Size: 10.0 KB (10014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3791b25a58e33a29a35408faa97df64d7d3943b13836d1a33bccd7da4c63b7`  
		Last Modified: Fri, 06 Mar 2026 18:23:00 GMT  
		Size: 262.5 MB (262545638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:01d66a418f539d467bf56993977d46f66d9ed6e1f29162ee6e7c0a3bbcb24635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4400761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a868bd26f398499ea59d489a8b8ebde6ab66c48a721664e8f7aa9c9f4a82a32b`

```dockerfile
```

-	Layers:
	-	`sha256:cd020ab360b8de0ace557bae9ba2b250393a71965b9e73269c918a562b571038`  
		Last Modified: Fri, 06 Mar 2026 18:22:54 GMT  
		Size: 4.4 MB (4378407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a837623f5b860f2cc6b306c1310e7dced7969a9fd995406f2d1632500ef2b551`  
		Last Modified: Fri, 06 Mar 2026 18:22:53 GMT  
		Size: 22.4 KB (22354 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc37752df9c4f15584b503d797d2cfd681093fc8c209a201e7187c13622366e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383053037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13de9a9598dccc960468f1f85a7248a9af702e1439d776d1ab16aac3c6915465`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 18:24:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Mar 2026 18:24:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Mar 2026 18:24:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e95626e21348a30109799a44639c2169bc24e27e1a1371972ff2583c3d8493c NEO4J_TARBALL=neo4j-community-2026.02.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 06 Mar 2026 18:24:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.2-unix.tar.gz
# Fri, 06 Mar 2026 18:24:10 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 06 Mar 2026 18:24:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.02.2-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 06 Mar 2026 18:24:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 18:24:35 GMT
WORKDIR /var/lib/neo4j
# Fri, 06 Mar 2026 18:24:35 GMT
VOLUME [/data /logs]
# Fri, 06 Mar 2026 18:24:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 06 Mar 2026 18:24:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 06 Mar 2026 18:24:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91692a29f7f8992a7942da6de9876a9c64e5f4a8acaf777264a1a2ccfb634f2f`  
		Last Modified: Fri, 06 Mar 2026 18:25:01 GMT  
		Size: 91.3 MB (91288290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df1c223c67457d5caba6e4a82b24e210f95fc556998bd564e3ffb2717a3a3d1`  
		Last Modified: Fri, 06 Mar 2026 18:24:56 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38d1ace37953e4b28ee415dc6acb230d0444336d745c2f58079904728bf1aa9`  
		Last Modified: Fri, 06 Mar 2026 18:25:03 GMT  
		Size: 261.6 MB (261614596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:ada41dceef61310052ca724dab4186b69cf093089b9619d0197088eebf8ca8c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4395607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d8ef45cf3b99c2fd37e67e9a1e8c9e8bc3f9f5cd1aeddad9d5241dcca7d2e8`

```dockerfile
```

-	Layers:
	-	`sha256:860b6aa528e09c2c3bb55231289919cd9636a14f690ff6f1236e9be79fef3587`  
		Last Modified: Fri, 06 Mar 2026 18:24:57 GMT  
		Size: 4.4 MB (4372978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:262809c323689b4385b8e80aaedd5e8a4f23a25173cbb84248a3e4d9601df15d`  
		Last Modified: Fri, 06 Mar 2026 18:24:57 GMT  
		Size: 22.6 KB (22629 bytes)  
		MIME: application/vnd.in-toto+json
