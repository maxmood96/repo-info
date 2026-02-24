## `neo4j:community-trixie`

```console
$ docker pull neo4j@sha256:657e0b601f09da7ef1bd51eebfe3758c3123eb362249767d8476500c95ea810e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:95c49bcdcf4120585652a1e095dffcd0928b2a4e3cb930e70f70c88c5de46cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.4 MB (341397678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a50074257406b8459385132abf69065bad04bc0be797fcf5c93dc0dfe83c49a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:24:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:24:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f026977b1559a9a5e796faf6b0d3da3ecf8fae4d2bfb3a3c01ce9980f8010de2 NEO4J_TARBALL=neo4j-community-2026.01.4-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 24 Feb 2026 19:24:56 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.4-unix.tar.gz
# Tue, 24 Feb 2026 19:24:56 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 24 Feb 2026 19:25:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.4-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 24 Feb 2026 19:25:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:25:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Feb 2026 19:25:21 GMT
VOLUME [/data /logs]
# Tue, 24 Feb 2026 19:25:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 24 Feb 2026 19:25:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:25:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03112f55b45dff0b2a5b8a9275f8f156021f0217fc4622ba52f78cab15b50e4c`  
		Last Modified: Tue, 24 Feb 2026 19:25:46 GMT  
		Size: 92.3 MB (92256315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cc0068ff7c7064e10ccfd26a7d8939bfbe0660554fb8a2851516b3ad9c31f8`  
		Last Modified: Tue, 24 Feb 2026 19:25:42 GMT  
		Size: 10.0 KB (10018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6985154fdd0d14d23f600ade07f5c44c192a4ff8cfbb47eb2117c4d949a09830`  
		Last Modified: Tue, 24 Feb 2026 19:25:48 GMT  
		Size: 219.4 MB (219352681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:c53f3840dd0d5d2ce40be569a00d048066db364e9b58308354b3a9d4c0443519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4409765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23c88f75537760b8d1f379e3a4bd5a8557cf47c214ea96d9f02e19980dba4ff`

```dockerfile
```

-	Layers:
	-	`sha256:077d72da18245c192ecd8316653cd316dff48b264295fbe02c93e6cea6e161ec`  
		Last Modified: Tue, 24 Feb 2026 19:25:42 GMT  
		Size: 4.4 MB (4387410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8b6bd11cb0c9d55430c7007b3e26f4b5e6290daabf6536106f5f23811de0d46`  
		Last Modified: Tue, 24 Feb 2026 19:25:42 GMT  
		Size: 22.4 KB (22355 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f28031b6a329fd2b51603bbb3267a8ba40ffa59b5b2b73e7135fec8a6d37e302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.9 MB (339856331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425ef73801a6534a635859d6f322b8af6b200a47d5cb665c0ec520a2c018baa5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:29:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:29:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:29:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f026977b1559a9a5e796faf6b0d3da3ecf8fae4d2bfb3a3c01ce9980f8010de2 NEO4J_TARBALL=neo4j-community-2026.01.4-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 24 Feb 2026 19:29:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.4-unix.tar.gz
# Tue, 24 Feb 2026 19:29:38 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 24 Feb 2026 19:30:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.4-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 24 Feb 2026 19:30:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:30:03 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Feb 2026 19:30:03 GMT
VOLUME [/data /logs]
# Tue, 24 Feb 2026 19:30:03 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 24 Feb 2026 19:30:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:30:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd8ca5259505d743cc41c01de9671c7f6d6c0f831080b84a28ac6c5c52b39b8`  
		Last Modified: Tue, 24 Feb 2026 19:30:28 GMT  
		Size: 91.3 MB (91288290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063f7a45a9815579b2716141570a82ed72759e100567f8cc6e6152d843884a89`  
		Last Modified: Tue, 24 Feb 2026 19:30:24 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c161d1b33b233e636bd99b32599c6849d3344d89a1eff0063e6767294265333`  
		Last Modified: Tue, 24 Feb 2026 19:30:30 GMT  
		Size: 218.4 MB (218417890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:aed96b941a190166fbe68f949fd28fdfb8a1a88976f043e2aec0734ae8149dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4404609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb6d65c09c047fcf624f4a0132e6abcdfc727313c13c379f27a08a5880d702e`

```dockerfile
```

-	Layers:
	-	`sha256:1613ffeeee028b21f409f6249e051b56e1d9f8ae9ca26134912cff699692757f`  
		Last Modified: Tue, 24 Feb 2026 19:30:25 GMT  
		Size: 4.4 MB (4381981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b364e7ba8ee36697399dec5f6851e3de1ff02d76698a58e7b063a6c42e84735`  
		Last Modified: Tue, 24 Feb 2026 19:30:24 GMT  
		Size: 22.6 KB (22628 bytes)  
		MIME: application/vnd.in-toto+json
