## `neo4j:2025-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:7fd8fa515d7adc338e998d2307ab3836b8493f09f0147720e530afb21e9681f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:3e8aabf8897fb8ba8682e4b54adc3a9176f5e58b7fb6639565538a00bc4cc7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.0 MB (528999546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a987dc7cd5f2afe98ae8ee0270b3ec683ea94ec8879ca28c6472b46ee8be6ab`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 19 Jun 2025 13:23:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Thu, 19 Jun 2025 13:23:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 19 Jun 2025 13:23:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=836097f43a9d33f986620f5ff6d7862f83623f6a74d7d828dbe2d694c39f98cd NEO4J_TARBALL=neo4j-enterprise-2025.05.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 19 Jun 2025 13:23:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.1-unix.tar.gz
# Thu, 19 Jun 2025 13:23:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Jun 2025 13:23:43 GMT
WORKDIR /var/lib/neo4j
# Thu, 19 Jun 2025 13:23:43 GMT
VOLUME [/data /logs]
# Thu, 19 Jun 2025 13:23:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 19 Jun 2025 13:23:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 19 Jun 2025 13:23:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf3e82515b5cb97676b7186f50de619d3323e08c1a5a17affb5d971f78c5e23`  
		Last Modified: Tue, 01 Jul 2025 05:50:13 GMT  
		Size: 157.6 MB (157634505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc247ffdb2e127e0630143776464d3fb5b415d7ca0f5aaabc0466943fb2956f`  
		Last Modified: Tue, 01 Jul 2025 02:27:57 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2ee62f90bbefb26375d07d028feb470a091dec6beb9507a6679308ed1d203e`  
		Last Modified: Tue, 01 Jul 2025 02:27:57 GMT  
		Size: 10.0 KB (9974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562eb1950b37a4147f8b91697a4c462612e0e08044cd3dd97f44ef7b1b717082`  
		Last Modified: Tue, 01 Jul 2025 05:50:58 GMT  
		Size: 341.1 MB (341095148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:729af8504b71771a5cb3476c4ca2f3ae4597548e99aca9f585b5f04cb64597b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4861202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862f95d4b470aa67b72c3b13d1614045ce137278ede7f61a7a5a9bfd47f61fd4`

```dockerfile
```

-	Layers:
	-	`sha256:504f2fa919e7b0060412cac0479f63b96bd9b401e8cef0ee21b8d3e038e3c649`  
		Last Modified: Tue, 01 Jul 2025 05:43:27 GMT  
		Size: 4.8 MB (4839501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a404f7e329ab813678da5cc5ad81bdccbbdee235de331223f74224c23f14d697`  
		Last Modified: Tue, 01 Jul 2025 05:43:28 GMT  
		Size: 21.7 KB (21701 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:870002662e07bd4320200024acdabf4b9d31c345ff29db5916d3e83ae37667cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.0 MB (525025766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb2b2612c7cdc26046920594c6de8fed74eb8fc3091db68cf25b139d8ad371f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Thu, 19 Jun 2025 13:23:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 19 Jun 2025 13:23:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=836097f43a9d33f986620f5ff6d7862f83623f6a74d7d828dbe2d694c39f98cd NEO4J_TARBALL=neo4j-enterprise-2025.05.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 19 Jun 2025 13:23:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.1-unix.tar.gz
# Thu, 19 Jun 2025 13:23:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Jun 2025 13:23:43 GMT
WORKDIR /var/lib/neo4j
# Thu, 19 Jun 2025 13:23:43 GMT
VOLUME [/data /logs]
# Thu, 19 Jun 2025 13:23:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 19 Jun 2025 13:23:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 19 Jun 2025 13:23:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a05b7675310ac1706c242efff47ecbf4b89d0e0e2b0670389c8f811b1f50b5e`  
		Last Modified: Fri, 20 Jun 2025 20:48:50 GMT  
		Size: 155.9 MB (155928824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9cfe852a13dd0960f3ef9bd9dac77da83fe7674c1a9f96878c888c8788d769`  
		Last Modified: Fri, 20 Jun 2025 18:35:21 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455524d0023dbfa738a25fa0f84e83f0fc1a52357aa8cdee0b9da9f6db2923f9`  
		Last Modified: Fri, 20 Jun 2025 18:35:21 GMT  
		Size: 10.0 KB (9977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae17b431c2aa7b63392474144ccacbd13c1aa59ff5fa5b14921677878ccd979`  
		Last Modified: Fri, 20 Jun 2025 21:03:03 GMT  
		Size: 340.3 MB (340338878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:a2379ba76f83ed532a2cfb90b60141d8be895320ba34b12278128decd5ca94c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4835224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa07469d3cb4124b55dea0546af1935e13e2692f77aeeeafd6c36a2ede06382`

```dockerfile
```

-	Layers:
	-	`sha256:dbd4e775be513cc18fe4e1302fb0e1561c1b5cc4251b27257eb04c4c28af9c66`  
		Last Modified: Fri, 20 Jun 2025 20:43:45 GMT  
		Size: 4.8 MB (4813330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:953bcd0204bba473190b6654193d811569950cdecf86984f18b2cd684caf383c`  
		Last Modified: Fri, 20 Jun 2025 20:43:45 GMT  
		Size: 21.9 KB (21894 bytes)  
		MIME: application/vnd.in-toto+json
