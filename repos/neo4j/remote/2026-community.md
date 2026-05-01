## `neo4j:2026-community`

```console
$ docker pull neo4j@sha256:447781490e26e4858443ba3d9977778f9a78264bcf5a57728c85f565347e663f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-community` - linux; amd64

```console
$ docker pull neo4j@sha256:2f5ebaa8038ee5252577b1c20f99f237950217921e5d384e8c5eb6a5cfe4f869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.6 MB (368611243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633840537d1cada397353d074390feebec4aaa900270f41847b3c50ddded94f0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Thu, 30 Apr 2026 23:44:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:44:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:44:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=fd750466b1247c0d1ef09a84c614f7e045793b30dfa277148e8da71646598820 NEO4J_TARBALL=neo4j-community-2026.04.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 30 Apr 2026 23:44:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
# Thu, 30 Apr 2026 23:44:23 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 30 Apr 2026 23:44:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 30 Apr 2026 23:44:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:44:48 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Apr 2026 23:44:48 GMT
VOLUME [/data /logs]
# Thu, 30 Apr 2026 23:44:48 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 30 Apr 2026 23:44:48 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:44:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fa583666b63cb5ee3990ce1dbbcbb791bad2d5df9dd68e795467140ac1e503`  
		Last Modified: Thu, 30 Apr 2026 23:45:13 GMT  
		Size: 92.6 MB (92574598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbcc0d331f9628ba385dc21de2316feaf63235d8fa3a3fee043857dba813be6`  
		Last Modified: Thu, 30 Apr 2026 23:45:09 GMT  
		Size: 10.0 KB (10019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0261e425c30964b453ea1750731d2c2534cc61b0a84d756000459b9406f0a1af`  
		Last Modified: Thu, 30 Apr 2026 23:45:16 GMT  
		Size: 246.2 MB (246246420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:cabac502706b924d69da13f2ae2321d8e3abc38f08c90038fa940454604ca86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe55c6049bb5138900eedee14d55a77857214508cf48ff36cac575651a669be2`

```dockerfile
```

-	Layers:
	-	`sha256:df71849c8833c656adab424ec2b94e27421e1aad63b2cf463f1545648127150c`  
		Last Modified: Thu, 30 Apr 2026 23:45:09 GMT  
		Size: 4.4 MB (4359959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d77be108e5d6de65423b88b523216d054437d9d61a2fdd2955d0ea4000f821a`  
		Last Modified: Thu, 30 Apr 2026 23:45:09 GMT  
		Size: 22.4 KB (22355 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ba629b36de208cf2ad747364a2ee2e62ef9b792858195194e910da0b6d32e5fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.0 MB (367009846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfbb4ff6545ae3d6847fe19205093face86f3ae8ccb6b9824b520dec041c74c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Thu, 30 Apr 2026 23:49:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:49:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:49:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=fd750466b1247c0d1ef09a84c614f7e045793b30dfa277148e8da71646598820 NEO4J_TARBALL=neo4j-community-2026.04.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 30 Apr 2026 23:49:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
# Thu, 30 Apr 2026 23:49:27 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 30 Apr 2026 23:49:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 30 Apr 2026 23:49:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:49:51 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Apr 2026 23:49:51 GMT
VOLUME [/data /logs]
# Thu, 30 Apr 2026 23:49:51 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 30 Apr 2026 23:49:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 30 Apr 2026 23:49:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3813829e6b2e2b8ba8ac8c750a6365167fe7fda46427c870985fd184a2643b`  
		Last Modified: Thu, 30 Apr 2026 23:50:16 GMT  
		Size: 91.5 MB (91542288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae95f45bc016903d305f7190000576d4ef7f096f3cec8acc26df37d25ad446de`  
		Last Modified: Thu, 30 Apr 2026 23:50:12 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce3949bde005fc7fa70946e8c3105866aec3f8e078e0a89e31c6703688735be`  
		Last Modified: Thu, 30 Apr 2026 23:50:19 GMT  
		Size: 245.3 MB (245313899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:51bce38edfaad920020b5cdc04faaaea2cde0a53eb8fc0f9e3f9678fa080968b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4377159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81dc24a9dbcba9d96dafb4830955bb7191a4edb11b488a183939d89afb7d770`

```dockerfile
```

-	Layers:
	-	`sha256:317775bba5eaed64f22dd85d55ef31793eeda50736423eafdd97c7cc677c9336`  
		Last Modified: Thu, 30 Apr 2026 23:50:13 GMT  
		Size: 4.4 MB (4354530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3407682ef4f42c59b5f9a8b5c20dc14f0d07f6fc0c203199df6b25114d89704f`  
		Last Modified: Thu, 30 Apr 2026 23:50:13 GMT  
		Size: 22.6 KB (22629 bytes)  
		MIME: application/vnd.in-toto+json
