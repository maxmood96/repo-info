## `neo4j:2026-enterprise-trixie`

```console
$ docker pull neo4j@sha256:47ddd1e73be8bec8e97a05417722207045f1e50e991c3fa50d0a50f3e51ef6d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-enterprise-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:9999b73457bb74a1241873d97b35ceeb97034dace2f61a2cc605fb0109ab7e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **517.3 MB (517349649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd84e27c96206ba5713f7bccaf79c008fc70b33ead0619dbdbe4e9c9d8eefb99`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 00:44:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 00:44:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2507ce15c1410931cf81db4435c1e1e437d5a857f59db3f946697988a5263aeb NEO4J_TARBALL=neo4j-enterprise-2026.05.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 11 Jun 2026 00:44:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.05.0-unix.tar.gz
# Thu, 11 Jun 2026 00:44:29 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 11 Jun 2026 00:45:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.05.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 11 Jun 2026 00:45:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:45:07 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jun 2026 00:45:07 GMT
VOLUME [/data /logs]
# Thu, 11 Jun 2026 00:45:07 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 11 Jun 2026 00:45:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc62e6a66f5c629274454567fd8f3a8aeb2bf9ad16498255e79a129e4473986`  
		Last Modified: Thu, 11 Jun 2026 00:45:38 GMT  
		Size: 92.6 MB (92574589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c6480b330c00cc7140d828ab08495a92dccb5e430bcfde2fcf437a579f15d6`  
		Last Modified: Thu, 11 Jun 2026 00:45:34 GMT  
		Size: 10.0 KB (10015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf3db988d78a3df8b3e3b44aba8d703288d57a94e8abab726a4069a64184e89`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 395.0 MB (394979598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:36ef765175664c613aaa97be0173c4b0861a356ca4a49df27ae49dbf0c1f1691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4682046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63897dfd7487286228c4e3b20feb972962966b13fb1afc6ab1ed877d39124ed`

```dockerfile
```

-	Layers:
	-	`sha256:171856ff5e36ec2d049a254ee7f423a34a5059e0a7da0fa0b250446d8654a7c8`  
		Last Modified: Thu, 11 Jun 2026 00:45:34 GMT  
		Size: 4.7 MB (4661929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beeb3ad54dda4a14ed067a10452ba953a5580da1f9df9a75a10fd903bca1bdbd`  
		Last Modified: Thu, 11 Jun 2026 00:45:34 GMT  
		Size: 20.1 KB (20117 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-enterprise-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0660d0539991348b5bf76b90159f98cd0066485354a0245e2bb76de65c0f0d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.8 MB (515750780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd7887538b49db36fc226db48376252f332462426751e9b76ba17a66a7ff9b3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 00:46:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 00:46:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2507ce15c1410931cf81db4435c1e1e437d5a857f59db3f946697988a5263aeb NEO4J_TARBALL=neo4j-enterprise-2026.05.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 11 Jun 2026 00:46:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.05.0-unix.tar.gz
# Thu, 11 Jun 2026 00:46:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 11 Jun 2026 00:46:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.05.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 11 Jun 2026 00:46:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:46:45 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jun 2026 00:46:45 GMT
VOLUME [/data /logs]
# Thu, 11 Jun 2026 00:46:45 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 11 Jun 2026 00:46:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:46:45 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b60bc1b09aa39ba9e04f0e64648884d8bf69c71a830c509e9ef4e93c9cad620`  
		Last Modified: Thu, 11 Jun 2026 00:47:17 GMT  
		Size: 91.5 MB (91542261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77ff2becd0d536b28b6708467f9876bb92ce33ebbd0d65e0ccefde79630d3a4`  
		Last Modified: Thu, 11 Jun 2026 00:47:12 GMT  
		Size: 10.0 KB (10016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e301279661e5cebaf463b70c49248d5d806b33d33229906831c2a8bffa0658`  
		Last Modified: Thu, 11 Jun 2026 00:47:24 GMT  
		Size: 394.0 MB (394049941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:554ab685d9ca256cd6a60d3afd34d7890457d693a7f566aa58a3ed4d0f6d4505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4676691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b8462b63bdffb58adae87528568dbedcfeb8d7ce26734ab4b354a750697822`

```dockerfile
```

-	Layers:
	-	`sha256:22be9ea9a799ef35b024bbf4b28e38115092a315a5ef64c1aff4ea755a2df6a3`  
		Last Modified: Thu, 11 Jun 2026 00:47:12 GMT  
		Size: 4.7 MB (4656396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c876ee4966ed10993eca0ff540db2c38c07feb05d2d2b23333065fe807cb8f0e`  
		Last Modified: Thu, 11 Jun 2026 00:47:12 GMT  
		Size: 20.3 KB (20295 bytes)  
		MIME: application/vnd.in-toto+json
