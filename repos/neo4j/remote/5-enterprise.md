## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:292bc4d59071b61bf1a3e6919e24a70057360a1d180d63e3a146948def96cadf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:837ad317e3a6f6917f63fb7f1f8cffbfcc90372b81017aa544b90f2215661371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.9 MB (666935929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd18748b479f1590a4560ce7bfcdbb221204676ca10a3bfb3f10777d25eb54bf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Mon, 06 Oct 2025 07:06:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Oct 2025 07:06:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=379c3771ab55d7c9c62cfb52c5ca47d19452e042951560a73e3bc3ba2b13e5e4 NEO4J_TARBALL=neo4j-enterprise-5.26.13-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 06 Oct 2025 07:06:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.13-unix.tar.gz
# Mon, 06 Oct 2025 07:06:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.13-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.13-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 07:06:58 GMT
WORKDIR /var/lib/neo4j
# Mon, 06 Oct 2025 07:06:58 GMT
VOLUME [/data /logs]
# Mon, 06 Oct 2025 07:06:58 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 06 Oct 2025 07:06:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 07:06:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95580ce183e93b566e7b495e9f2bbe789b41ed6cf5c2c616b4fc5f55db9b963d`  
		Last Modified: Mon, 06 Oct 2025 19:23:04 GMT  
		Size: 144.7 MB (144693573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ce46f9f7a420f5e2806d6fea520fb5aa94fb1b5b8db76e6009092cbd425497`  
		Last Modified: Mon, 06 Oct 2025 19:23:19 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217eb3bdfbce5b9649471128b8058bf176f19919a69d0b92fe02e79ced3e3428`  
		Last Modified: Mon, 06 Oct 2025 19:23:19 GMT  
		Size: 10.1 KB (10059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8017d3945d08dd6b9721033b17af3ff7979f9ba8f1ec35ca5f76035812e59c4b`  
		Last Modified: Mon, 06 Oct 2025 19:23:12 GMT  
		Size: 492.0 MB (491970061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:2a9f89063cd55ccfdeff81e3178ff449283079dbeeec602d672e089b74867d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4876518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99a69db1f7b8d608babed89d0e20300afe69773b70286272bb54640b34ec522`

```dockerfile
```

-	Layers:
	-	`sha256:9ae250815249ea2ff48a434ae56b62a769d1c99f156e8665c7b6a581688cdcc3`  
		Last Modified: Mon, 06 Oct 2025 20:43:59 GMT  
		Size: 4.9 MB (4855490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d2b0be4531ac7a4c1736fd617b512f86ab51c668581f4173e9c542e48f1ef35`  
		Last Modified: Mon, 06 Oct 2025 20:44:00 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f36adc7ce11e56edc18164b7c6679230c87358cb5fdca23dc1c33227040087ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.5 MB (663519699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517519904f13b3e00f5b19c1e45dc6e6c6b6cc1f0b0f9b5393e3800bb5c7a808`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Mon, 06 Oct 2025 07:06:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Oct 2025 07:06:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=379c3771ab55d7c9c62cfb52c5ca47d19452e042951560a73e3bc3ba2b13e5e4 NEO4J_TARBALL=neo4j-enterprise-5.26.13-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 06 Oct 2025 07:06:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.13-unix.tar.gz
# Mon, 06 Oct 2025 07:06:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.13-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.13-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 06 Oct 2025 07:06:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 07:06:58 GMT
WORKDIR /var/lib/neo4j
# Mon, 06 Oct 2025 07:06:58 GMT
VOLUME [/data /logs]
# Mon, 06 Oct 2025 07:06:58 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 06 Oct 2025 07:06:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 07:06:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0fd85d34e635c966ef32b093e4695c78854f248ef21a50c00e9b146b986ec5`  
		Last Modified: Mon, 06 Oct 2025 19:23:09 GMT  
		Size: 143.5 MB (143542205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf41d2ee7c6ea5873a1e2da99a7c982f8ce87b7380f739e6d185816c41f10c2`  
		Last Modified: Mon, 06 Oct 2025 19:23:22 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7deb960d50c4403c93a86c93dc92255d8141b01e13a2edf7a2642dc6818456d`  
		Last Modified: Mon, 06 Oct 2025 19:23:22 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c077fc70274ece0b9fbb6755982f6adc270e16b4cfc54f1312f31f9263474821`  
		Last Modified: Mon, 06 Oct 2025 19:23:15 GMT  
		Size: 491.2 MB (491215107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:c6fcce951ab0982969d643e00337ba87b8f560dd685b49d6bcda5db7fc649ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4850492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e513ef5bcafe70c18c0b438441bb6a845435d42a7e5414ff690fda1ea37c7a`

```dockerfile
```

-	Layers:
	-	`sha256:36ac1f5dcf34ad08251f02a131e420c987273ad48b2cc6215d64db75dc8f3462`  
		Last Modified: Mon, 06 Oct 2025 20:44:05 GMT  
		Size: 4.8 MB (4829295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b562a363d64e32a318a7433036bf183850016967ba4522b21665cfbf4179478`  
		Last Modified: Mon, 06 Oct 2025 20:44:06 GMT  
		Size: 21.2 KB (21197 bytes)  
		MIME: application/vnd.in-toto+json
