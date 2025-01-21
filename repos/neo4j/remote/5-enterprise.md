## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:f5e4065b3215b9dccd3e17baf7732a6f901b7460b5e8275ad7c3d0df3037636f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:083202a0c06d4dab2890fc1b2b70891b8e163ba5e07c0c9a44c29d8207dd0f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.2 MB (624222843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d87a786b323848336e306f33c3804bb6a122180399066f543ae4aa4f0135d6b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4be83292b9a10a068ad80562a911dd4ac05fef1c33867521b85d470bf7775df`  
		Last Modified: Tue, 21 Jan 2025 19:29:11 GMT  
		Size: 144.5 MB (144536708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a039e3407d645b3af8f0cc775d42d0275a0ebffcf54190773ef705e7d94700`  
		Last Modified: Tue, 21 Jan 2025 19:29:09 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41f6679e199c646e8a782d279478b91577656dbd48f581bc7b8558576d7158f`  
		Last Modified: Tue, 21 Jan 2025 19:29:09 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abdae9594e0aabaf722c84b47cb0d9651db37e29be529af9ac9c179984f2950`  
		Last Modified: Tue, 21 Jan 2025 19:29:15 GMT  
		Size: 449.4 MB (449419567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:dd24d61585aa05d84e9522294c2662ae6f322d96c856c510565cea993d098374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a70776dc22dbe671a8a20410f77f89f359613c2e825ab47b059a9d53683e39f`

```dockerfile
```

-	Layers:
	-	`sha256:8b1d4b714a2d19b7bc5377aaf329f637493c77e4ed776eded2813eef2a840697`  
		Last Modified: Tue, 21 Jan 2025 19:29:09 GMT  
		Size: 3.5 MB (3538275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a32220fc8d80c14e35f86a3276d29e4da030fee9915630ab9a57e1dc2a1e07b`  
		Last Modified: Tue, 21 Jan 2025 19:29:09 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:89a3d33c11cbf7fccd30c8271337a917ee7dc9df6c7bfd8d4341cb8acd18a240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.7 MB (621734113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c963bfc842817d7182a404ff133895b61cd6bce8758ce946ee4b374e2266fb74`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a9fea114fbd00c11c58a44e09fa8c34763301d9e52a1a548e04722af721c49`  
		Last Modified: Tue, 14 Jan 2025 07:25:10 GMT  
		Size: 143.4 MB (143360959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebe9a8a677620e6cd17af7c158f13ccbc27660e1e7e6eebdd3c2134e2a1d82b`  
		Last Modified: Tue, 14 Jan 2025 07:26:28 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcc170c82c071aa7adc3d73f71a7ce747b2528ab6b4bc88bad8c9b84250a239`  
		Last Modified: Tue, 14 Jan 2025 07:26:28 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d49baa815fb7c78c5bfe51b8ef4ed7dce75afbd932b920d9aef59b12912e823`  
		Last Modified: Tue, 14 Jan 2025 07:26:39 GMT  
		Size: 449.6 MB (449614311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:4fa503165d996c3c6639f8f11d4b704d948409ee8a18b615fb060c7754477a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c408e06ca104d701efda6dfc97b55c1c0dde4da589e6c03b6fc94e9500eb59`

```dockerfile
```

-	Layers:
	-	`sha256:79c9428f38f0fb06b1bc644cfdb150f1e755c94357dce58a5e8d7bbbb8d8cea3`  
		Last Modified: Tue, 14 Jan 2025 07:26:28 GMT  
		Size: 3.5 MB (3537969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8d9c2f82a0c670a3866a4652f29e3fb4d60e04b7ae57c55a49fb8d8ed98a2c`  
		Last Modified: Tue, 14 Jan 2025 07:26:28 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json
