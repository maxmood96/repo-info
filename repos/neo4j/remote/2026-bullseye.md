## `neo4j:2026-bullseye`

```console
$ docker pull neo4j@sha256:9621a63dcd2b6effcb34d0e2eac00d6548cf83dbe75a17f9a2aba1c35357f75e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:60689f156485d137816e22621b2fecde7645b79c61b568f9d41f4df26541634d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.7 MB (404669431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b18679f09985727d6225b797d4e0334a6300d57b3cff04bf7aa5b8f23e9ce6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Wed, 04 Feb 2026 21:10:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Feb 2026 21:10:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Feb 2026 21:10:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=fd9376186034a84eeca384971b2e9e3e80f8e41166529843f49c48e390a48694 NEO4J_TARBALL=neo4j-community-2026.01.3-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 04 Feb 2026 21:10:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.3-unix.tar.gz
# Wed, 04 Feb 2026 21:10:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.3-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 04 Feb 2026 21:10:09 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 04 Feb 2026 21:10:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.3-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 04 Feb 2026 21:10:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 21:10:29 GMT
WORKDIR /var/lib/neo4j
# Wed, 04 Feb 2026 21:10:29 GMT
VOLUME [/data /logs]
# Wed, 04 Feb 2026 21:10:29 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 04 Feb 2026 21:10:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 21:10:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a6e80b7b48803f41a265d420bf6a5829a959ad106dde588f761d91e79ae903`  
		Last Modified: Wed, 04 Feb 2026 21:10:54 GMT  
		Size: 157.8 MB (157826034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7f6d70f0b69f58aae2fb9a84713c15553e8924266cdc5011ae82798c4e919f`  
		Last Modified: Wed, 04 Feb 2026 21:10:48 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d733d08a421e745e32b1c11cf4306c896c056246cb57c4800eafcc378fcec7`  
		Last Modified: Wed, 04 Feb 2026 21:10:48 GMT  
		Size: 10.2 KB (10190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd0dc6309c9fd3898f74e3bb30ad5e4faf044d9ee359f4c5da050c342a286fc`  
		Last Modified: Wed, 04 Feb 2026 21:10:55 GMT  
		Size: 216.6 MB (216571050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c6f2e826b0f5e16ea57a740c32a143b9ed9169de7cf5dbfc0609b1fd0322f003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4633277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da6f6b11268d8350104ac8f1b5f7f1b8777c1e5c5557446e200afa5417e5874`

```dockerfile
```

-	Layers:
	-	`sha256:96b19f14a1df3a58ffc3b0bafb1476c359d776c0a75dbb8b4c9ded870b643c70`  
		Last Modified: Wed, 04 Feb 2026 21:10:48 GMT  
		Size: 4.6 MB (4611653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10f95c4123eae436145b86fd1bc926ca4a2f08e58a13f2786bf7f8c42625586c`  
		Last Modified: Wed, 04 Feb 2026 21:10:48 GMT  
		Size: 21.6 KB (21624 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3906f9abacca0e7f7f3651349321c74cbc5b111e3cf2f81f1287a0a6ba686807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.7 MB (400680553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a1cc1a279c38df35d091f076e69f73537bd96a2c416dd6fcdda67585ca78b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Wed, 04 Feb 2026 21:08:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Feb 2026 21:08:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Feb 2026 21:08:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=fd9376186034a84eeca384971b2e9e3e80f8e41166529843f49c48e390a48694 NEO4J_TARBALL=neo4j-community-2026.01.3-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 04 Feb 2026 21:08:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.3-unix.tar.gz
# Wed, 04 Feb 2026 21:08:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.3-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 04 Feb 2026 21:08:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 04 Feb 2026 21:08:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.3-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 04 Feb 2026 21:08:38 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 21:08:38 GMT
WORKDIR /var/lib/neo4j
# Wed, 04 Feb 2026 21:08:38 GMT
VOLUME [/data /logs]
# Wed, 04 Feb 2026 21:08:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 04 Feb 2026 21:08:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 21:08:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67702c678c31d3c3f8dbc675850d5a7abef6f4dfff1589573d59703216dcd449`  
		Last Modified: Wed, 04 Feb 2026 21:09:06 GMT  
		Size: 156.1 MB (156107672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2cf23b2e2ad403c61adaa90ecdc83e2c9d14feb8f20c5aed3c49aa3db8904f`  
		Last Modified: Wed, 04 Feb 2026 21:09:00 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64caa3c5b8777e558407fed9004ba33ba187fe5619e17db91a9815581d98f43f`  
		Last Modified: Wed, 04 Feb 2026 21:09:00 GMT  
		Size: 10.2 KB (10191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789722e9f7cedc1cfc8742726186107ba8c15bf2218d5a4938f34228b343696e`  
		Last Modified: Wed, 04 Feb 2026 21:09:13 GMT  
		Size: 215.8 MB (215814340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8b1c8f46d5c27f9ac89632f3ab54bfd6b5047f45f086e315e63a2f462d0782b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4607298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adece6bdc5bffd43b236e56c7bff7567143ca0d604fb63f02bee27c920294d75`

```dockerfile
```

-	Layers:
	-	`sha256:e3321841b3b223bbdef17a82eb829a1f4af7ff2f5bc664b39bf5e80682fe32e5`  
		Last Modified: Wed, 04 Feb 2026 21:09:00 GMT  
		Size: 4.6 MB (4585482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60eb8351f1382b552a78c6354da8b1feebf92c19541d12feee5dd4c5bab70df2`  
		Last Modified: Wed, 04 Feb 2026 21:09:00 GMT  
		Size: 21.8 KB (21816 bytes)  
		MIME: application/vnd.in-toto+json
