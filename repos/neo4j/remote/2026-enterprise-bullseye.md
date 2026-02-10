## `neo4j:2026-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:d4db3967b84f44105802d6d092a16e0be2833899d7572d7f2f4a09143a809bbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:6ea57b261757a0143d828164cb711cce44f055c52add5aa99e828068fd1b673f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.6 MB (553558012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170bb6ec6b7bed65eefc63afcb948218ea9efa13356e67cf03cc3501f744aacf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 10 Feb 2026 19:19:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 10 Feb 2026 19:19:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 10 Feb 2026 19:19:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a2435d9ec6f9a18eb9616c1a1319caa8b7040f38b8c20c73ef3467e607d06bf NEO4J_TARBALL=neo4j-enterprise-2026.01.4-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 10 Feb 2026 19:19:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
# Tue, 10 Feb 2026 19:19:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 10 Feb 2026 19:19:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 10 Feb 2026 19:19:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 10 Feb 2026 19:19:32 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 19:19:32 GMT
WORKDIR /var/lib/neo4j
# Tue, 10 Feb 2026 19:19:32 GMT
VOLUME [/data /logs]
# Tue, 10 Feb 2026 19:19:32 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 10 Feb 2026 19:19:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 10 Feb 2026 19:19:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641fc09b58be22401ca1ff3abb3e8a63d8d6aed1f982628fa0dc39877a25f433`  
		Last Modified: Tue, 10 Feb 2026 19:20:04 GMT  
		Size: 157.9 MB (157857076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3314f95f3d8fad8119aa7a57f3c7d43b7cbcc1fcff98fec5bbbaec4dbdeca9`  
		Last Modified: Tue, 10 Feb 2026 19:19:59 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1addabc7b207ce5c0db9dbb7541006f5508444d0d8f05442f3988b3ad4d83fe`  
		Last Modified: Tue, 10 Feb 2026 19:19:58 GMT  
		Size: 10.2 KB (10188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bd631963d1b7bdb0a0c5a260fcb7444e186b6951dc033ada77c82dffeb6f01`  
		Last Modified: Tue, 10 Feb 2026 19:20:08 GMT  
		Size: 365.4 MB (365428590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:233fd5fe73ce048531fe397198a5607e2d6045abe15f92412de98d2571d05979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4875924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796c73913238601267720bb3b305eb18f24ba4ed7895e846d976edc89f5961df`

```dockerfile
```

-	Layers:
	-	`sha256:d5346127667ae78215c194c3eb937259390c0dc7e30e62346abe692a792d9109`  
		Last Modified: Tue, 10 Feb 2026 19:19:59 GMT  
		Size: 4.9 MB (4855525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a9b6011f41d9cb462369fe43e58ac50f50827906eb19f48c5907fc461f187c8`  
		Last Modified: Tue, 10 Feb 2026 19:19:59 GMT  
		Size: 20.4 KB (20399 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:77b29f2b64736d6e2c8407110f1f6bbbfcac5d76b79913a3240af6a9aaefed10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.6 MB (549564998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce51ef186e840ac7364795d0eef2ebc31e1f40c759f6c04c15c1df93782ee861`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 10 Feb 2026 19:19:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 10 Feb 2026 19:19:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 10 Feb 2026 19:19:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a2435d9ec6f9a18eb9616c1a1319caa8b7040f38b8c20c73ef3467e607d06bf NEO4J_TARBALL=neo4j-enterprise-2026.01.4-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 10 Feb 2026 19:19:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
# Tue, 10 Feb 2026 19:19:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 10 Feb 2026 19:19:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 10 Feb 2026 19:19:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 10 Feb 2026 19:19:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Feb 2026 19:19:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 10 Feb 2026 19:19:40 GMT
VOLUME [/data /logs]
# Tue, 10 Feb 2026 19:19:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 10 Feb 2026 19:19:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 10 Feb 2026 19:19:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d367928254b3b9a8165892dbaee1775ec9b35a11335920a1da7c94ddbb076de7`  
		Last Modified: Tue, 10 Feb 2026 19:20:13 GMT  
		Size: 156.1 MB (156133091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0baa0f5a967a2f30644543a62cf7037b527d7352a69e42ad80d784179c675b96`  
		Last Modified: Tue, 10 Feb 2026 19:20:06 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a29041d9c9174eb0d00a25c368ca79afacfee4837c05948470e011eb4183839`  
		Last Modified: Tue, 10 Feb 2026 19:20:06 GMT  
		Size: 10.2 KB (10188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a28e684a073d5078cd9bfecff282599c8d76f9d97b7b0505cba54caa1ffdb2`  
		Last Modified: Tue, 10 Feb 2026 19:20:17 GMT  
		Size: 364.7 MB (364673378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d295a9c3a2ca585ec858ec618714ddb9c6500434de43b7341f37687af3e97933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4849850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cff4937f38c1d549b03184e2071c63336b5e7014715a679001db2e6c3b43d7`

```dockerfile
```

-	Layers:
	-	`sha256:eeaab2decd6188e1aad4ebaccf8aa9c390cc3cce5d52ffcaf23ea4980493adb6`  
		Last Modified: Tue, 10 Feb 2026 19:20:07 GMT  
		Size: 4.8 MB (4829306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea72f86969384eba44a5f9dc5f417f94d96a9a8221678d02ed2e399e35f2bd7a`  
		Last Modified: Tue, 10 Feb 2026 19:20:06 GMT  
		Size: 20.5 KB (20544 bytes)  
		MIME: application/vnd.in-toto+json
