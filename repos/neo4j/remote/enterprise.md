## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:b9a9c7c74297a0d23d54f87b17bae9a537257c5729d39d91c021b6ff6458f7a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:5505719bed6a3ce60de0e6941b622afef93af58db8f7fbf145213f24689f784e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.1 MB (518138753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:099b3436a0d269151e3b5a3fcf3426107ff1bc40c1e8e8f1099daac646482f38`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 21:39:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:39:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 21:39:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a47e20ec6bd7df9fd11781cba86264d530fd1f605cca817271ff7e5bbc7c3b4a NEO4J_TARBALL=neo4j-enterprise-2026.03.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 15 Apr 2026 21:39:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.03.1-unix.tar.gz
# Wed, 15 Apr 2026 21:39:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 15 Apr 2026 21:40:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.03.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 15 Apr 2026 21:40:06 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:40:06 GMT
WORKDIR /var/lib/neo4j
# Wed, 15 Apr 2026 21:40:06 GMT
VOLUME [/data /logs]
# Wed, 15 Apr 2026 21:40:06 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 15 Apr 2026 21:40:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:40:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c3adbd3c5bc63927fab129e6aea63e0edee67b95a91828b7951d7e2815261b`  
		Last Modified: Wed, 15 Apr 2026 21:40:35 GMT  
		Size: 92.3 MB (92256319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99300f882887c587be5fe682b9fd6a70700a88e500936bc2ace83561f48480b`  
		Last Modified: Wed, 15 Apr 2026 21:40:31 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57b5e4cd7e7c4c31e4d5eedd1ebf2de2f23111196cf291db8a34993e0504842`  
		Last Modified: Wed, 15 Apr 2026 21:40:41 GMT  
		Size: 396.1 MB (396096741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:c57ae4765e5934cb5e3a310c7f27b73ba4f8ff1ef0f7600b7ee28a3c538324f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4673084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52031eb783c06144f97f85a23fbc5373491bacd4cbc7c465ced4dce3acada72`

```dockerfile
```

-	Layers:
	-	`sha256:2d5c37bad361dcfc851965eabf65bacf4fb87d150754966e4a6a430ca4ac4adb`  
		Last Modified: Wed, 15 Apr 2026 21:40:31 GMT  
		Size: 4.7 MB (4653121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:983164fd3f99cefb5c43e9f5881878cced2dd27db8c491a80c576176d5861212`  
		Last Modified: Wed, 15 Apr 2026 21:40:31 GMT  
		Size: 20.0 KB (19963 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:61dde72df76ee43d52cbcecf9bbe2d565d6baa0bf4bcbfb146dbb7d5a9a0a69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.0 MB (516985017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9e7ebb5298b1d308830e604b6c1934db8416c18b7997a042b45f3ac3d2afe2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 21:51:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:51:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 21:51:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a47e20ec6bd7df9fd11781cba86264d530fd1f605cca817271ff7e5bbc7c3b4a NEO4J_TARBALL=neo4j-enterprise-2026.03.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 15 Apr 2026 21:51:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.03.1-unix.tar.gz
# Wed, 15 Apr 2026 21:51:31 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 15 Apr 2026 21:51:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.03.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 15 Apr 2026 21:51:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:51:58 GMT
WORKDIR /var/lib/neo4j
# Wed, 15 Apr 2026 21:51:58 GMT
VOLUME [/data /logs]
# Wed, 15 Apr 2026 21:51:58 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 15 Apr 2026 21:51:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:51:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a9f1dad33994091f096dabcc8eb7d973fa4b80a1396bd859fc5b1070239cb`  
		Last Modified: Wed, 15 Apr 2026 21:52:29 GMT  
		Size: 91.3 MB (91288275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431adefbd53fb3abdaef68bb2a230ca3143c3bcc3854e39c56826acba1e14370`  
		Last Modified: Wed, 15 Apr 2026 21:52:25 GMT  
		Size: 10.0 KB (10016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f5bca080b11a65266b599b06459604ba68cb7a004da1a0380f5a3d5d6f29ed`  
		Last Modified: Wed, 15 Apr 2026 21:52:34 GMT  
		Size: 395.5 MB (395548143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:bd349edf933da6b4ba457152072484d5f7f028f73c487aabb622c1c70e27df06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4667737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36319f3fe85e4478101d49a9d1e4e411f215d5c8f7a1c042a182f1e9f532f0c8`

```dockerfile
```

-	Layers:
	-	`sha256:8ede3b606e4ab021c5b4e293d719146ac0907874d42f15405eb17895a40dd815`  
		Last Modified: Wed, 15 Apr 2026 21:52:26 GMT  
		Size: 4.6 MB (4647596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2766dbbc8b9560ae4eec96a161671680bd153564af79907f59c50ac126282da8`  
		Last Modified: Wed, 15 Apr 2026 21:52:25 GMT  
		Size: 20.1 KB (20141 bytes)  
		MIME: application/vnd.in-toto+json
