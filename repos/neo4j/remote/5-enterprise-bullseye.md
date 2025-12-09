## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:d3bb8f13a08d181c07d45246c77ae5a47a66fad5858b77fc375ff5dc888d87f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2372822af03ee0d82b32f961a15ac3e4e4da4e939703531d5278aeaeaa7f6154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.6 MB (671614437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:117da781eaab67eb675d65ae907769f7cd36cb274d4a4943bfdf458396acb8ad`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:12:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:12:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:12:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9f3d954467e43681210a4541df73dae563d4f960273333b4b6db788313ef4096 NEO4J_TARBALL=neo4j-enterprise-5.26.18-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 08 Dec 2025 23:12:11 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.18-unix.tar.gz
# Mon, 08 Dec 2025 23:12:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 08 Dec 2025 23:12:11 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 08 Dec 2025 23:12:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.18-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 08 Dec 2025 23:12:38 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:12:38 GMT
WORKDIR /var/lib/neo4j
# Mon, 08 Dec 2025 23:12:38 GMT
VOLUME [/data /logs]
# Mon, 08 Dec 2025 23:12:38 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 08 Dec 2025 23:12:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:12:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f298ae32b382f589b5faee77cba5c204d2ece18202e863d91bc0c5cf8efd9b6c`  
		Last Modified: Tue, 09 Dec 2025 03:48:57 GMT  
		Size: 144.8 MB (144847947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3203b03da6078eebf562cdb159609374b35754b096955cb29c4b10bbdb12940b`  
		Last Modified: Mon, 08 Dec 2025 23:13:25 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5879a90d9643fe1028734a16c0650a170289e6dae55b39cd6f156ef9011c7e94`  
		Last Modified: Mon, 08 Dec 2025 23:13:25 GMT  
		Size: 10.1 KB (10058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4295ae19d4380c8f96411c3667a55cdee9527cb64afe7b4652cb862ed7d1e6`  
		Last Modified: Mon, 08 Dec 2025 23:13:51 GMT  
		Size: 496.5 MB (496494101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8b68c370c36b24ec0fdd92ac4414cccced62a13036e0c717f49cd5b19f2ccc2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4869447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3645bc3bf28fbfad87a62dd368771268c1741dc7d0b9f37114b6e2ea666c785`

```dockerfile
```

-	Layers:
	-	`sha256:c23ca6da272f3625cddc871f7d773c2fc2aac1713051c0368f093ec75299e984`  
		Last Modified: Tue, 09 Dec 2025 03:44:46 GMT  
		Size: 4.8 MB (4848462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:480809464398c600c0d455fad0cb982c5a45673e7ed5883f2afc315aa83e4997`  
		Last Modified: Tue, 09 Dec 2025 03:44:46 GMT  
		Size: 21.0 KB (20985 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2e9b8a60a1201d512bb479fe133d30f1c992c5fd635491d4d175d2b5fbb0e9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.2 MB (668180007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f313cd23b178d796dbdb14a5f4e8879326d2619aec9da476451d315e6de72c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:15:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:15:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:15:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9f3d954467e43681210a4541df73dae563d4f960273333b4b6db788313ef4096 NEO4J_TARBALL=neo4j-enterprise-5.26.18-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 08 Dec 2025 23:15:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.18-unix.tar.gz
# Mon, 08 Dec 2025 23:15:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 08 Dec 2025 23:15:30 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 08 Dec 2025 23:15:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.18-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 08 Dec 2025 23:15:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:15:55 GMT
WORKDIR /var/lib/neo4j
# Mon, 08 Dec 2025 23:15:55 GMT
VOLUME [/data /logs]
# Mon, 08 Dec 2025 23:15:55 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 08 Dec 2025 23:15:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:15:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8b81a1896ea694ba81a15bcd83297fe0033ebdd739e9d4448b86795b0165de`  
		Last Modified: Mon, 08 Dec 2025 23:17:01 GMT  
		Size: 143.7 MB (143679919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395400b69eef4b92d60daa2009faea160b7d08cb15157e31c13108ed0de61953`  
		Last Modified: Mon, 08 Dec 2025 23:16:47 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b71e4b945e819138778fe67a563138965f96a250b543a1adb0726645cb8bfd`  
		Last Modified: Mon, 08 Dec 2025 23:16:47 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e7ae8c437e021ddc93cd4c81f67fd506c6ccb435f7f2346d43e9c84a7c6384`  
		Last Modified: Mon, 08 Dec 2025 23:17:26 GMT  
		Size: 495.7 MB (495737651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:16811f2514d1ffe44f5aeb8857d7aba1ea01701b54f3fb04caffe1f41cc768ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4843421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce64403d6a71069919b52f64909b401a3103086ef069dad0709a467d96797056`

```dockerfile
```

-	Layers:
	-	`sha256:e3399d7d81b6d8572928f873eb1263d27e964953b51afcebd2b959f989041139`  
		Last Modified: Tue, 09 Dec 2025 03:44:51 GMT  
		Size: 4.8 MB (4822267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c2eb1d3daac2b520fec88a2f68d930c169c295b4e9e5b213997af0e234d2996`  
		Last Modified: Tue, 09 Dec 2025 03:44:52 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json
