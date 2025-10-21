## `neo4j:latest`

```console
$ docker pull neo4j@sha256:5b445304d1fd62347e7a71a314cca87ee0428458126e9dbba42191acc1dbc8d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:45729c7e3aac49f4e53591fbf5435fe8b4ef47a8d58f69c37c7f4e8bb0dff1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.3 MB (399302915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadab3ba9974b1fe10e9dc479bbc9c045adfa73b0a3f6ed0336336b77ceeadf5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 30 Sep 2025 13:19:30 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Tue, 30 Sep 2025 13:19:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Sep 2025 13:19:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=997928463c687a96433720610c3091969fd4d5f76f8a12d09a6149bddf65927a NEO4J_TARBALL=neo4j-community-2025.09.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 30 Sep 2025 13:19:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
# Tue, 30 Sep 2025 13:19:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Sep 2025 13:19:30 GMT
WORKDIR /var/lib/neo4j
# Tue, 30 Sep 2025 13:19:30 GMT
VOLUME [/data /logs]
# Tue, 30 Sep 2025 13:19:30 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 30 Sep 2025 13:19:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 13:19:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a523219352919b1b1c00ab8a8ec1e2a19e88135beba5d009c5d32cc964db4246`  
		Last Modified: Tue, 21 Oct 2025 01:46:16 GMT  
		Size: 157.8 MB (157804775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c411ff69e0b43e8df9ffbd8f2a313518ddd4637317ebf6a22122da609bd9f12`  
		Last Modified: Tue, 21 Oct 2025 01:46:23 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21246ad7d4780a828bd1c1250111032db2f761d43c68026449de0a43ae6fbe78`  
		Last Modified: Tue, 21 Oct 2025 01:46:23 GMT  
		Size: 10.0 KB (10019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d370e05914a9a8962878bd0e1ace262d6c11128d20f333a25ed35b891e573c14`  
		Last Modified: Tue, 21 Oct 2025 11:45:35 GMT  
		Size: 211.2 MB (211225884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:812f988b7eda6189016cbfa79b05a4e55ac0a57971ae38e4793b0a962130b065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4627779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc1331609c28de870644ef5caa4cf5297c83aaba4d0c40bfce2e3e90ad797fd`

```dockerfile
```

-	Layers:
	-	`sha256:048530d73ebc186b01b61628623706f4961e12758e76b30d226528147e2a3f69`  
		Last Modified: Tue, 21 Oct 2025 11:43:17 GMT  
		Size: 4.6 MB (4603670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c026a24b7b002785a8687ce2db8de6d1c5e807b1e381df55f36508d93d82169f`  
		Last Modified: Tue, 21 Oct 2025 11:43:18 GMT  
		Size: 24.1 KB (24109 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2f0369a88cb3a846a6578bf73dfea38343f06b59d6f7b96117f762247726c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.3 MB (395313068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3811837fe591b3ad02da152d3157517a408e7dde12cc6279212cac139e960381`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 30 Sep 2025 13:19:30 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Tue, 30 Sep 2025 13:19:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Sep 2025 13:19:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=997928463c687a96433720610c3091969fd4d5f76f8a12d09a6149bddf65927a NEO4J_TARBALL=neo4j-community-2025.09.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 30 Sep 2025 13:19:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
# Tue, 30 Sep 2025 13:19:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Sep 2025 13:19:30 GMT
WORKDIR /var/lib/neo4j
# Tue, 30 Sep 2025 13:19:30 GMT
VOLUME [/data /logs]
# Tue, 30 Sep 2025 13:19:30 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 30 Sep 2025 13:19:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 13:19:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c58427f0e485063420619bb5b5890b8de24bc0ca9e1890b5614e50166d3173`  
		Last Modified: Tue, 21 Oct 2025 08:45:48 GMT  
		Size: 156.1 MB (156081199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4b08912389b82d7975ce75b19766993dc3cd0e146d86ef463b4edb51c70db4`  
		Last Modified: Tue, 21 Oct 2025 02:36:43 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8bc76b617287b13f0cc5b5a93edccf0a2eaf64101321c564540359abb60286`  
		Last Modified: Tue, 21 Oct 2025 02:36:41 GMT  
		Size: 10.0 KB (10018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ed096c98df9d009543d201eaa8d243544ee08e22851b770e80d13af141b672`  
		Last Modified: Tue, 21 Oct 2025 08:46:25 GMT  
		Size: 210.5 MB (210469553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:e908417602590aa200aed1e9e27a6cec09e349b32c37d2b57be691c1a2b904af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4601992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3266276724925ae22308db90c7735c1ec793ac02d795ccaff3aaae944861e7d7`

```dockerfile
```

-	Layers:
	-	`sha256:38f542ce7c63575aa505c82b7a476d5113e55ebfeec4fcc867a00051062ef4f3`  
		Last Modified: Tue, 21 Oct 2025 08:43:20 GMT  
		Size: 4.6 MB (4577595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9aef8bfef7f1d12a24b869d6f706753cfa9a995cd215e4cee5e63afc1fba0b`  
		Last Modified: Tue, 21 Oct 2025 08:43:21 GMT  
		Size: 24.4 KB (24397 bytes)  
		MIME: application/vnd.in-toto+json
