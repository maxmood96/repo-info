## `neo4j:latest`

```console
$ docker pull neo4j@sha256:66218a899c92379207f140cefdb642c2e4be34b37f77248abe0e6c72e7f6fee1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:509cfbdd9512e2fe608aef4aed6e675ce6bbe1f93cfe1588fb265181a7774fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.7 MB (391692985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522ec08f96e3fce57419eaecc42a6aa3943bee29542aa6ba1095d968f3fcff43`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Aug 2025 14:31:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Wed, 27 Aug 2025 14:31:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Aug 2025 14:31:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cce5d0d88c05635692a8db86cde299861ff8fd71271e034fc633080bb09d9c59 NEO4J_TARBALL=neo4j-community-2025.08.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 27 Aug 2025 14:31:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.08.0-unix.tar.gz
# Wed, 27 Aug 2025 14:31:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.08.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.08.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 14:31:02 GMT
WORKDIR /var/lib/neo4j
# Wed, 27 Aug 2025 14:31:02 GMT
VOLUME [/data /logs]
# Wed, 27 Aug 2025 14:31:02 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 27 Aug 2025 14:31:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 27 Aug 2025 14:31:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef1ec4fd4531b64554fe821503d7b6c01bf95423b8aad892ee9f364ee284639`  
		Last Modified: Mon, 08 Sep 2025 23:45:34 GMT  
		Size: 157.8 MB (157804808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb100e1903413a3eab768cc7a23488ed9a90880fadfca14aa075989efc54d04`  
		Last Modified: Mon, 08 Sep 2025 21:51:15 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e1e43f0ed8d81be2179d6b080a1f5ef722eb0f5b6ec2c619934213c3887179`  
		Last Modified: Mon, 08 Sep 2025 21:51:20 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae11238180e4cd5420f1b84010d959dbf698042d64c1726056ce89cd3253cdef`  
		Last Modified: Mon, 08 Sep 2025 23:45:33 GMT  
		Size: 203.6 MB (203618220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:a4cfa4789c7b4d5b70605a156538a3c706c2a404c3346c1c410adda64d407d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4624931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa0c6072add71bcf2af9f86125eab9e9cdcfe0e7b1e36e17e3e88364ca68681`

```dockerfile
```

-	Layers:
	-	`sha256:133525def385fc060b4092e82cfdfbad216b6032eddc10939b48a91b8ac0ebe9`  
		Last Modified: Mon, 08 Sep 2025 23:43:20 GMT  
		Size: 4.6 MB (4600822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09f3eb94171355c8e7dd0f4b95c166e26eaaeecc41c118e3015686b5d9fe9272`  
		Last Modified: Mon, 08 Sep 2025 23:43:21 GMT  
		Size: 24.1 KB (24109 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4f562ee8d044a94039c570805ee89d50a90f1fc8899234d7db9dd37cc996166e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.7 MB (387707933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0a4c39b1477827c13a7632ed58d0bae307f65e71e51a5cff4cf2935f9be998`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Aug 2025 14:31:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Wed, 27 Aug 2025 14:31:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Aug 2025 14:31:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cce5d0d88c05635692a8db86cde299861ff8fd71271e034fc633080bb09d9c59 NEO4J_TARBALL=neo4j-community-2025.08.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 27 Aug 2025 14:31:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.08.0-unix.tar.gz
# Wed, 27 Aug 2025 14:31:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.08.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.08.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 14:31:02 GMT
WORKDIR /var/lib/neo4j
# Wed, 27 Aug 2025 14:31:02 GMT
VOLUME [/data /logs]
# Wed, 27 Aug 2025 14:31:02 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 27 Aug 2025 14:31:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 27 Aug 2025 14:31:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1c2c39a2f9b63f51255bb40620bffbbc66324b911a74269054b571a4bc7449`  
		Last Modified: Mon, 08 Sep 2025 23:43:48 GMT  
		Size: 156.1 MB (156081188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6232aa87cf26dc0d32b8a863413f7ce20ed7aae406dd2d7d39aec732a872c3`  
		Last Modified: Mon, 08 Sep 2025 22:08:10 GMT  
		Size: 3.9 KB (3871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04705c25390f14c89f303d4af2bba916e474d288ec4f89e2cb27c7efb116095e`  
		Last Modified: Mon, 08 Sep 2025 22:08:14 GMT  
		Size: 10.0 KB (10022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a69ecf46364e52f63e540aa0f04e22957a614de7f9737aa937aaae3f4c7989`  
		Last Modified: Mon, 08 Sep 2025 23:46:13 GMT  
		Size: 202.9 MB (202862363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:282c8e9ade1adf430a09529e4d43590842164aa383f45317bb99edccf094e07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4599145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51209b6ef16d37f8731f109d56b2c18fd1c72c2b35477055e416fc1cd67a8d76`

```dockerfile
```

-	Layers:
	-	`sha256:22e1a1b6ff3705a37c2b881fe9e60d5f04692c6e0616362d4632e0ab65e8fde4`  
		Last Modified: Mon, 08 Sep 2025 23:43:25 GMT  
		Size: 4.6 MB (4574747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3bd54d714cea2f7e90bcefe3243797549a2cd79ec7498271b13330409b0e3a5`  
		Last Modified: Mon, 08 Sep 2025 23:43:26 GMT  
		Size: 24.4 KB (24398 bytes)  
		MIME: application/vnd.in-toto+json
