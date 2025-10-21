## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:9c54f48a35069af1ec7843d851d285035b8436f8cf95bfa7127fff1c72edaa3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:4c0c47daaf5ab90922d947ab58f449c6ec58ab7608e3b729f237d92325c40cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.2 MB (667215750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b4c3483acc482cad02e4b6991669b729148cad126075effed538af66a46cda`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Mon, 20 Oct 2025 12:38:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Oct 2025 12:38:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Oct 2025 12:38:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=aae26711bb6daf26070ce9ab3f1beecbb1eff2066352a4ed3ee64eb7e3b09a24 NEO4J_TARBALL=neo4j-enterprise-5.26.14-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Oct 2025 12:38:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.14-unix.tar.gz
# Mon, 20 Oct 2025 12:38:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.14-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Oct 2025 12:38:37 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Oct 2025 12:38:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.14-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Oct 2025 12:38:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 12:38:37 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Oct 2025 12:38:37 GMT
VOLUME [/data /logs]
# Mon, 20 Oct 2025 12:38:37 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Oct 2025 12:38:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Oct 2025 12:38:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46bbcbf9790fb31c874797a296ef271fb9758e678daea89463604ed6b1cee6a`  
		Last Modified: Mon, 20 Oct 2025 23:11:33 GMT  
		Size: 144.7 MB (144693312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d75a8ec2b730ae1395a653e76cc8986d56f2c68c9db918ac0ca0564b31d969`  
		Last Modified: Mon, 20 Oct 2025 21:32:37 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7816c47b63e65a70f3057c31a866f8c516c2b4dc321ccf6125ca695ade0e5e6e`  
		Last Modified: Mon, 20 Oct 2025 21:32:37 GMT  
		Size: 10.1 KB (10056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602074510df7e6ca21d34717f9347b4ea09ab83ea7f3de3f197872e9ed4e9bbf`  
		Last Modified: Mon, 20 Oct 2025 23:11:46 GMT  
		Size: 492.3 MB (492250149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b67877b08f98c0b3577fca2e9b7b6989bdf5dd3e74f0f7d5e9470e51b2edb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4865777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f613d83499e646484413917ef91c078d867d0f3a27b30641b0d0779e08c431c`

```dockerfile
```

-	Layers:
	-	`sha256:9eaab26d4e313f8af4f851ef69d4a9389765c6ef5cc4bb07434e259d2ae625aa`  
		Last Modified: Mon, 20 Oct 2025 23:43:56 GMT  
		Size: 4.8 MB (4844749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3e6fa18380e5ccb48a90a8400f3d644d3a64fb54572a7520625ca8376c574ad`  
		Last Modified: Mon, 20 Oct 2025 23:43:57 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0a6e5fd268affe132ac5c65b3e288d83c68c24e404001c17bc1cdcecfc504128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.8 MB (663798520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0249708b7045d5ed79942936848ef70217272084b17c269b56cc1217b2481281`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Mon, 20 Oct 2025 12:38:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Oct 2025 12:38:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Oct 2025 12:38:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=aae26711bb6daf26070ce9ab3f1beecbb1eff2066352a4ed3ee64eb7e3b09a24 NEO4J_TARBALL=neo4j-enterprise-5.26.14-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Oct 2025 12:38:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.14-unix.tar.gz
# Mon, 20 Oct 2025 12:38:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.14-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Oct 2025 12:38:37 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Oct 2025 12:38:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.14-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Oct 2025 12:38:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 12:38:37 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Oct 2025 12:38:37 GMT
VOLUME [/data /logs]
# Mon, 20 Oct 2025 12:38:37 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Oct 2025 12:38:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Oct 2025 12:38:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc93cfbec22b275040b347c2492f6027ac2f14b58f823aef49a1ec5e84303e9`  
		Last Modified: Mon, 20 Oct 2025 21:33:06 GMT  
		Size: 143.5 MB (143542164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ff0e4ea5f35c43b69b2342a588583bec79f41ed50ad0583254fe061c1dac59`  
		Last Modified: Mon, 20 Oct 2025 21:33:20 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2524ea99c855a24705d38040c82659ddfefa58ebe346918982fe49752079985`  
		Last Modified: Mon, 20 Oct 2025 21:33:20 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab20c8048ee14ba8ff940d9247ba01308920b88325d4e23e7fc6b50cf69d8ed5`  
		Last Modified: Mon, 20 Oct 2025 21:33:14 GMT  
		Size: 491.5 MB (491493969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b12046968d2c52487d25f02ac5c8fe1d625f44b812c352b73aa42755bfd5b2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4839751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6c57fcc5e07405526cef8ae9fcc5b0ba03864bab87e70bac66688ec2e0dca4`

```dockerfile
```

-	Layers:
	-	`sha256:6d7063ee36b929fd08e4dc36707a663f53c784e8bb2ba37cbc7cb8115011fa3a`  
		Last Modified: Mon, 20 Oct 2025 23:44:02 GMT  
		Size: 4.8 MB (4818554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60f6d77f3ef074bdd2f79c70654b630f54b8c060efb69ee764c8e3b72b598448`  
		Last Modified: Mon, 20 Oct 2025 23:44:03 GMT  
		Size: 21.2 KB (21197 bytes)  
		MIME: application/vnd.in-toto+json
