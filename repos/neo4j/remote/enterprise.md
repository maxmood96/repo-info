## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:14ec9ffe2099d3e733f8bd7d7f6a110785446959ebf5c72411069ba90d3336ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:7b6eab5e7d4da8bacd6009fa6220795182a6531492a074cb38b19730ca5eab40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.3 MB (547268943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9734d0a3bf4b3140692f9bd9de438804bab3fd076c20923a2f0f2840014c380`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Fri, 19 Dec 2025 18:36:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Dec 2025 18:36:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Dec 2025 18:36:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=22fe6ea9bb332e5a1250b0fd1c226539e0a4babec699e0b1e7d2aa5043f65e05 NEO4J_TARBALL=neo4j-enterprise-2025.11.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 19 Dec 2025 18:36:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.11.2-unix.tar.gz
# Fri, 19 Dec 2025 18:36:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.11.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 19 Dec 2025 18:36:16 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 19 Dec 2025 18:36:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.11.2-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 19 Dec 2025 18:36:39 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Dec 2025 18:36:39 GMT
WORKDIR /var/lib/neo4j
# Fri, 19 Dec 2025 18:36:39 GMT
VOLUME [/data /logs]
# Fri, 19 Dec 2025 18:36:39 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 19 Dec 2025 18:36:39 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:36:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d04f1684544ad313e78c07ba6c4a45f5c61fcb19af79bd41ec6246819daabe`  
		Last Modified: Fri, 19 Dec 2025 18:37:36 GMT  
		Size: 157.8 MB (157825976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832567e008ccf355f838642f5b610d041d4984863aed1c97a9e35beb64447eef`  
		Last Modified: Fri, 19 Dec 2025 18:37:19 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d742e35fd72c5446f8522a13f77d57f62708542395378959f0c71482bd87776e`  
		Last Modified: Fri, 19 Dec 2025 18:37:19 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4950c4f1ab223aae31e937d15f725a4dc861dea7cc38ac106889af597447f02`  
		Last Modified: Fri, 19 Dec 2025 18:37:43 GMT  
		Size: 359.2 MB (359170610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3009fc1390dfde4947f21d74d87d6c2989bd4ce8f3caa0c0c6f2ec199fe4fdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4868421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9002905ab57de9ef2e8e7e739d70ade76f3f0c1c4eb87c988f7840a43e014a41`

```dockerfile
```

-	Layers:
	-	`sha256:770e324c19da72e50be057e6f7032e64a864400c316f45e99fe9dcacf843e57f`  
		Last Modified: Fri, 19 Dec 2025 21:43:43 GMT  
		Size: 4.8 MB (4846760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa803d19de1a33ba7ef2bc794269adfe29aa089e5f284f8f742c9f25a339df60`  
		Last Modified: Fri, 19 Dec 2025 21:43:44 GMT  
		Size: 21.7 KB (21661 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b00798034514c09442e4300855483798844d06839709bc66349633bb2cecb067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.3 MB (543285105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f910a9e7be46ee0bca5d7cc08a34873dc017085bac602dd63c9b91db9c827b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Fri, 19 Dec 2025 18:36:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Dec 2025 18:36:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Dec 2025 18:36:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=22fe6ea9bb332e5a1250b0fd1c226539e0a4babec699e0b1e7d2aa5043f65e05 NEO4J_TARBALL=neo4j-enterprise-2025.11.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 19 Dec 2025 18:36:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.11.2-unix.tar.gz
# Fri, 19 Dec 2025 18:36:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.11.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 19 Dec 2025 18:36:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 19 Dec 2025 18:36:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.11.2-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 19 Dec 2025 18:36:39 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Dec 2025 18:36:39 GMT
WORKDIR /var/lib/neo4j
# Fri, 19 Dec 2025 18:36:39 GMT
VOLUME [/data /logs]
# Fri, 19 Dec 2025 18:36:39 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 19 Dec 2025 18:36:39 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 19 Dec 2025 18:36:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c4f78650cd5e69994166a3a455e68435b87812cc2588785b085f3667138bdb`  
		Last Modified: Fri, 19 Dec 2025 18:37:42 GMT  
		Size: 156.1 MB (156107580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdeea9ecac9851c41326010de19dc876f1e1d37b6dcc96b666dfbc89bcaf101`  
		Last Modified: Fri, 19 Dec 2025 18:37:20 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f799de91bcfe3bee212e3ae15e8a81cebb51244cb5e9c7f3d8084de926316980`  
		Last Modified: Fri, 19 Dec 2025 18:37:21 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1e15502a64c9c1b8ae6f46cf4cc037a08effb5fa572fbada48f19c34ceac55`  
		Last Modified: Fri, 19 Dec 2025 18:37:46 GMT  
		Size: 358.4 MB (358415123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:38008f8ef388cf4281c3bf339ea47bfec2898ac6c9283ace0b32df1524f98e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4842441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8a083cedce2a50d8dd48302ce53f08c16966276263af0d3ccead20ee2e196d`

```dockerfile
```

-	Layers:
	-	`sha256:7aebaed8a20910c498eb4915f96be46b8b5fe84126f8e9b95722438b92b3fcfd`  
		Last Modified: Fri, 19 Dec 2025 21:43:52 GMT  
		Size: 4.8 MB (4820589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f10bf27930eda4f5557c5912145c639a31d344daca0d26de406c701551dd0fcd`  
		Last Modified: Fri, 19 Dec 2025 21:43:53 GMT  
		Size: 21.9 KB (21852 bytes)  
		MIME: application/vnd.in-toto+json
