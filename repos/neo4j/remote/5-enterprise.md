## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:0f62dff65da35575a8696d7c1c0c9bd9e19db108fdf9a28f247a12932ba78e30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:e49d2969e9308236eee516a338ac8c3edf8b6d4e98355c06e99fa8ce9c914892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.7 MB (667735109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d22f1ba6b1630313b0579823aaaf8c3816d421d72a5a8b8899327d9d020d11`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 23:11:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Nov 2025 23:11:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 05 Nov 2025 23:11:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ff006f997021433017e5e768f83f963f8c181531fafbcffebd53b8f6a585bf96 NEO4J_TARBALL=neo4j-enterprise-5.26.16-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 05 Nov 2025 23:11:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.16-unix.tar.gz
# Wed, 05 Nov 2025 23:11:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 05 Nov 2025 23:11:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 05 Nov 2025 23:11:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.16-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 05 Nov 2025 23:11:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 23:11:48 GMT
WORKDIR /var/lib/neo4j
# Wed, 05 Nov 2025 23:11:48 GMT
VOLUME [/data /logs]
# Wed, 05 Nov 2025 23:11:48 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 05 Nov 2025 23:11:48 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 05 Nov 2025 23:11:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05210f25e489c5746fb2b437966c01773dd8909d0e544b70739049a3501a0d9`  
		Last Modified: Thu, 06 Nov 2025 00:48:35 GMT  
		Size: 144.7 MB (144693306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3eeeb829c71d23da69d82abfcddc97e40d01748de89286debf52ce1453ca8aa`  
		Last Modified: Wed, 05 Nov 2025 23:12:46 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bac771c756473f32aed19f88e7f86d701d266226dc30d1518e99435c2bd9c9a`  
		Last Modified: Wed, 05 Nov 2025 23:12:46 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc73fad0959f7dbc110e6448b41ffab1e52d4ec95bd800b2019a041c82bf3c0`  
		Last Modified: Thu, 06 Nov 2025 00:48:37 GMT  
		Size: 492.8 MB (492769274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:a5cb6aec550479cd6f11ddab0e0807b8bf692808b5057317648d97676b3930fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4864203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8c2948b834a76c9fcb7dded82f032ab7fcb1b18113884a2f1e6bfee4a95117`

```dockerfile
```

-	Layers:
	-	`sha256:c4ab26ae6052f241e42d36eb5c28f42c1f7ff74d678094cdff86cee929107a30`  
		Last Modified: Thu, 06 Nov 2025 00:43:55 GMT  
		Size: 4.8 MB (4843218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbf60c49dfcb109beb8ff275e8c3392773b483133642f166f385b8fb46aa8a12`  
		Last Modified: Thu, 06 Nov 2025 00:43:56 GMT  
		Size: 21.0 KB (20985 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e4dd9220f6c6dc00d11d36b473f7800cb6f2c464df16d05adbfb2b4bf707435f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.3 MB (664318406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7fc4f95bd9e14a82dca9bd04e60ddf4a9a3406b572056a8ddd90b9b5915465`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 23:10:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Nov 2025 23:10:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 05 Nov 2025 23:10:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ff006f997021433017e5e768f83f963f8c181531fafbcffebd53b8f6a585bf96 NEO4J_TARBALL=neo4j-enterprise-5.26.16-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 05 Nov 2025 23:10:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.16-unix.tar.gz
# Wed, 05 Nov 2025 23:10:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 05 Nov 2025 23:10:54 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 05 Nov 2025 23:11:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.16-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 05 Nov 2025 23:11:32 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 23:11:32 GMT
WORKDIR /var/lib/neo4j
# Wed, 05 Nov 2025 23:11:32 GMT
VOLUME [/data /logs]
# Wed, 05 Nov 2025 23:11:32 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 05 Nov 2025 23:11:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 05 Nov 2025 23:11:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7becb92ff11e6281ead84954b18a2ab2ceff09979b7a7eced8ff4357b3586549`  
		Last Modified: Thu, 06 Nov 2025 00:50:48 GMT  
		Size: 143.5 MB (143542093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14e9969754256e0edb10cb63e5aa53b9378fef2296793e71253ff7405a6540b`  
		Last Modified: Wed, 05 Nov 2025 23:12:28 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d63337f0fb54df730d0c7f38c629926acb9b9d173d2d4ed22ae4f01790735f`  
		Last Modified: Wed, 05 Nov 2025 23:12:28 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8af55a82b3a50b5091c1aaf0b7ae902ee2f9ff9f58f0ea0b8d07886fd48d9c`  
		Last Modified: Thu, 06 Nov 2025 00:51:16 GMT  
		Size: 492.0 MB (492013800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:fa76aaa7674f4a845c2d5c317e863376d4b0a5414ce0df6858bfa4934cab78ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4838177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f96eebc3ad6fd2187e2755a6a1e081cf5be2343d4181dbe3c05706f4fcf577c`

```dockerfile
```

-	Layers:
	-	`sha256:86ba82f18f9ea54ddcaab19c9d30c1f5dc64815e4e8d03cd9da2535c0ae5c95e`  
		Last Modified: Thu, 06 Nov 2025 00:44:03 GMT  
		Size: 4.8 MB (4817023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ed9c21e9ff4be8f1d100b857d3fdef7c9dfeb0ebbcd7c94f227554c10d96df2`  
		Last Modified: Thu, 06 Nov 2025 00:44:03 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json
