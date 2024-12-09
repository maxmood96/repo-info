## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:1d436532c2047cc428182167744b0ae07c59c1eb9d894af5e594a5ae05fe8e1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:02633a43403034a5afb4100d7247ec2d079033e3160bc4d1cfd14c082fccf04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336709103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56fc1cd06f8d3d98493ca3c766abd99ae31b54fb93fcb24691686206ae3abaa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
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
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7c3bf219b42e1f7dc7a54f62d871e89aa54d602f02deb175836f67e361e49`  
		Last Modified: Mon, 09 Dec 2024 19:30:20 GMT  
		Size: 144.5 MB (144536717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c967aced981bbbe9e9b3d4dddfb2d60224f18967729394899c95bc3a6357e684`  
		Last Modified: Mon, 09 Dec 2024 19:30:19 GMT  
		Size: 161.9 MB (161905837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:eaace86f18640e810d24bbdab603f2058f728d8e5974e7d14770c1e6e8966255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef28ecd4a7406d0c80948ea86e709b97d2b02eb82e589e1f0ea34ace060a`

```dockerfile
```

-	Layers:
	-	`sha256:5e46689ef7f40097b9be730733bdb2b9303d95869d0da0ee79972fa4318d3b9a`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.2 MB (3240036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf07a126391c6e133a1b609452158e657752952f664d2f38f26a731e6b7cbb69`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:28b2390c4dc319f6c3079cf689347fc46a07952be528a89ba7398592df8fa536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315200080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313ad5378f72b900be490874e2d9a9f20582eb5efda43d7d2ac30e13eed4ed6a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4f7fdfab7981c1fd1ce39b349e6d2283d10dcdfcc3a26cdfaec40e92c2f974`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f45aef30b574f2766fa472920f01b410f5ce42f2abaf1e7ad36071d2ce4e0b`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a5984a007343e4980cef2a376e94f816e0f476d5ba2ce5a7c5ba4d16513562`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.1 MB (143080277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3094943aea8f9bc29afdf481ceed9a6790568472d2c0cd93d8d075f217bc5cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3262501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a648ee22f153335283ee2269f8b880b1831c2531435101b2c211b83f92612000`

```dockerfile
```

-	Layers:
	-	`sha256:12bafcaeb8940310546c17937b3a1f821c7ec053efd59d8557d573cbb90e9c95`  
		Last Modified: Tue, 03 Dec 2024 13:58:16 GMT  
		Size: 3.2 MB (3238459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1251aff1ae04b8aac0ad07793e7d21a39b29b2e5795fa6a4d27d6e0c398b85a`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json
