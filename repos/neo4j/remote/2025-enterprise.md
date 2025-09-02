## `neo4j:2025-enterprise`

```console
$ docker pull neo4j@sha256:bcc8c609dad08b856ca717278eb4c585ef9450e5fdee131e93cc058196abdde0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b6a614c72e4499589232cbe72aa7b1a79983c1c7ee409183dd88ee8d17e50600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.0 MB (530025228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0abad4368ca8d896e4ba4972d9057c95c9fb2ea81e8b0b19484bd6827dcb13`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Wed, 27 Aug 2025 14:31:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Aug 2025 14:31:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6818a98fca5044976e23935e9fc415aa080c9f36d4546274f7a8486cb8096d3c NEO4J_TARBALL=neo4j-enterprise-2025.08.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 27 Aug 2025 14:31:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.08.0-unix.tar.gz
# Wed, 27 Aug 2025 14:31:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.08.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.08.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 14:31:02 GMT
WORKDIR /var/lib/neo4j
# Wed, 27 Aug 2025 14:31:02 GMT
VOLUME [/data /logs]
# Wed, 27 Aug 2025 14:31:02 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 27 Aug 2025 14:31:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 27 Aug 2025 14:31:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22cd6df87a9cf7594b20acdc41e594510dfb82a3f61bb0d38cdd1b8a0ae37b0`  
		Last Modified: Tue, 02 Sep 2025 01:43:29 GMT  
		Size: 157.8 MB (157804774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41557dc7ebfa669ff9eb3c49183f42404046610920c94d9769e4068df8ba8f44`  
		Last Modified: Tue, 02 Sep 2025 00:56:47 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec3f29d8e47d48a49cbaaf19b043b9cbce353f65443e068af812f03ece2c04c`  
		Last Modified: Tue, 02 Sep 2025 00:56:47 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2b4bb525f4d5bed77afb014bc6646539e48c9beb80f88d8defa14f71f761e`  
		Last Modified: Tue, 02 Sep 2025 01:44:50 GMT  
		Size: 342.0 MB (341950446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:1daaee6b030d65c91a727a58036e7547fae9d46183dd923ee3f2076063afa664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4862633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87bace66d34114f8160a7a49c3cd4b7e2c89322b3966938ba84cc2804265412`

```dockerfile
```

-	Layers:
	-	`sha256:0666bebde27d16514ed6b05f2a0e3bcb3f34c7d9a7fc87c4c0d86aee3cfc410e`  
		Last Modified: Tue, 02 Sep 2025 02:43:24 GMT  
		Size: 4.8 MB (4840929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a81a42368503198bf96c6d836ef6f31ed83df48c2dea98a6e6a41a937c8471b`  
		Last Modified: Tue, 02 Sep 2025 02:43:25 GMT  
		Size: 21.7 KB (21704 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:87281eb7155fa3a6e60eba5ce68b2f71b5d7c2bfb03274e0f9ec87f7f0d31093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.0 MB (526039946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428f21e895866714b361c00ed5aa0ea9ad8d8f1f967d09f27cc9742f199380f7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Wed, 27 Aug 2025 14:31:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Aug 2025 14:31:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6818a98fca5044976e23935e9fc415aa080c9f36d4546274f7a8486cb8096d3c NEO4J_TARBALL=neo4j-enterprise-2025.08.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 27 Aug 2025 14:31:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.08.0-unix.tar.gz
# Wed, 27 Aug 2025 14:31:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.08.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.08.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 14:31:02 GMT
WORKDIR /var/lib/neo4j
# Wed, 27 Aug 2025 14:31:02 GMT
VOLUME [/data /logs]
# Wed, 27 Aug 2025 14:31:02 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 27 Aug 2025 14:31:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 27 Aug 2025 14:31:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2018a747c37989de117c5255ed9b90797d04cc50b7b51efd380710484b6be5df`  
		Last Modified: Tue, 19 Aug 2025 02:32:37 GMT  
		Size: 156.1 MB (156081251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0c143a8741306038160d96854ea790be91e30c9238a8bae844f49e13d90816`  
		Last Modified: Thu, 28 Aug 2025 16:44:41 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7e318e624aa1a00181ec24476bb24e5e98893451628a73f30b49d6740ff68b`  
		Last Modified: Thu, 28 Aug 2025 16:44:41 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265d757dc5159649c71bd7845d94298466141a474d6008af71ff71b66c300cb3`  
		Last Modified: Thu, 28 Aug 2025 18:26:23 GMT  
		Size: 341.2 MB (341194284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:362e9bf935789d4b0f39841ed729194fcfd513fe4bf91b4750e333c2bbd11a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4836655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b361fece2441366013ccf05eeff318b290d666a71e9d72e80b07a87b14f4ebd5`

```dockerfile
```

-	Layers:
	-	`sha256:3e1fd18df3e766bd538b1f52273a58386ad47140de0b3da382e328c261bd6308`  
		Last Modified: Thu, 28 Aug 2025 17:43:48 GMT  
		Size: 4.8 MB (4814758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21386cd6d67d286bf709ad6bd944fd9456fdfd6799e586c26e7348a66c22064c`  
		Last Modified: Thu, 28 Aug 2025 17:43:49 GMT  
		Size: 21.9 KB (21897 bytes)  
		MIME: application/vnd.in-toto+json
