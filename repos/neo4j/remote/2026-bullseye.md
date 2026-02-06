## `neo4j:2026-bullseye`

```console
$ docker pull neo4j@sha256:cafca7faab7baf14708cdd8c462473d18979b9527c83454fc9fe304bcdba1a83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:bf669c3313abeb2c34470c7d4257d8c869a1ea76e5eac56792e1a8734d66eea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.7 MB (404700751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d1410464aa4cd09ea2b26e92a14f2846ff5a10386957245b44f2dde0a9b61b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 22:50:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:50:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 22:50:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=fd9376186034a84eeca384971b2e9e3e80f8e41166529843f49c48e390a48694 NEO4J_TARBALL=neo4j-community-2026.01.3-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 05 Feb 2026 22:50:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.3-unix.tar.gz
# Thu, 05 Feb 2026 22:50:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.3-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 05 Feb 2026 22:50:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 05 Feb 2026 22:50:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.3-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 05 Feb 2026 22:50:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:50:40 GMT
WORKDIR /var/lib/neo4j
# Thu, 05 Feb 2026 22:50:40 GMT
VOLUME [/data /logs]
# Thu, 05 Feb 2026 22:50:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 05 Feb 2026 22:50:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:50:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f488b3023a990ac6a2c674514857c1b2cb4f0218ed4df21e29bb0398720ac8f7`  
		Last Modified: Thu, 05 Feb 2026 22:51:10 GMT  
		Size: 157.9 MB (157857074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed51c4547f74421b7cfc1666da844ddc59c0d5297b366ce6fc444d950ffb9904`  
		Last Modified: Thu, 05 Feb 2026 22:51:03 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e05cf2d2fd5dafe2c247eb0a65cc81184e6d7b243d1a3d58c460ea9c86f032`  
		Last Modified: Thu, 05 Feb 2026 22:51:03 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aba0b9e58d9f3275b3611108327689645403509065c33b7e2f25671ca4a487a`  
		Last Modified: Thu, 05 Feb 2026 22:51:11 GMT  
		Size: 216.6 MB (216571330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:cdcd73014141b42f735e92722b3463c990d7e035ea612292ba55abc41c924c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4633279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3066f8d17e563f6d4c661f10ffd850726527bb615eb43be274d2a2cf0dd83b10`

```dockerfile
```

-	Layers:
	-	`sha256:42f9895f7a9e20d815dff8d1c7f531092b9c31ec66e5790206672e866f79dcb0`  
		Last Modified: Thu, 05 Feb 2026 22:51:03 GMT  
		Size: 4.6 MB (4611655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a49346c9b0f00627f18b0cd4db1a70709108c60f3a26ce1b77743f7fc3a57b8`  
		Last Modified: Thu, 05 Feb 2026 22:51:03 GMT  
		Size: 21.6 KB (21624 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d6e3d5a65f4c1c2dcb1484969dc3c34711b2d3f4f3e4ea1fefec886139824a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.7 MB (400706026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2767909738f678242425d8c042065c6c16ef457baff4f177bde4cec2b28bd3af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 22:50:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:50:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 22:50:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=fd9376186034a84eeca384971b2e9e3e80f8e41166529843f49c48e390a48694 NEO4J_TARBALL=neo4j-community-2026.01.3-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 05 Feb 2026 22:50:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.3-unix.tar.gz
# Thu, 05 Feb 2026 22:50:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.3-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 05 Feb 2026 22:50:23 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 05 Feb 2026 22:50:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.3-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 05 Feb 2026 22:50:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:50:42 GMT
WORKDIR /var/lib/neo4j
# Thu, 05 Feb 2026 22:50:42 GMT
VOLUME [/data /logs]
# Thu, 05 Feb 2026 22:50:42 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 05 Feb 2026 22:50:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:50:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814155c68d611111476d8bb0528e9e3b5bb2d879759534a025a33e335c22b71d`  
		Last Modified: Thu, 05 Feb 2026 22:51:10 GMT  
		Size: 156.1 MB (156133060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc4f4c492cd785c62121d93acaf92fc9ddb18b13e315ac2095c07d87d290e47`  
		Last Modified: Thu, 05 Feb 2026 22:51:03 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22b381ad4c90354f5d6d7e67012ddb303a093fc99066b8273f09c665decfa18`  
		Last Modified: Thu, 05 Feb 2026 22:51:03 GMT  
		Size: 10.2 KB (10190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d94d93733035543f6cf4cefa028fee6bd5f18e6a2e1e141ad8b62e7f4ef9094`  
		Last Modified: Thu, 05 Feb 2026 22:51:10 GMT  
		Size: 215.8 MB (215814437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:6696a6300d3caa93dde24abf7dd3a83d93c90792311f4db5a5eab77eccbbcee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4607301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a25a19ea2759deeb7b4c59a12c9f891ceaf605cfa1cb293d4a0f061c21ee78`

```dockerfile
```

-	Layers:
	-	`sha256:10736519a6c62648283c9cae5d0c16089545f9118d399aa298eccc06ff52d149`  
		Last Modified: Thu, 05 Feb 2026 22:51:04 GMT  
		Size: 4.6 MB (4585484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93c24ac18b5f856a9e71b199e64ca2523f5c5aaf98de82234aeb37d30a5c79d0`  
		Last Modified: Thu, 05 Feb 2026 22:51:03 GMT  
		Size: 21.8 KB (21817 bytes)  
		MIME: application/vnd.in-toto+json
