## `neo4j:5-trixie`

```console
$ docker pull neo4j@sha256:5a240d74b0bf507048cceb24a718dc98a5403afaeb5e6395ad1e367fb5aabf06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:e478a735e8ec2dbd6f4f838cadb96ba9b7d221d483e79cb9871be52e17966d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355577127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da20d33550a230bf881414acfd87a382fe0078a1c7f98fe4cbe4947288b9b46b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 00:44:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5e752081e2863febf3d2f11fab31e1a3185e1ea7bb5e0bcf7d8e516ddbec5349 NEO4J_TARBALL=neo4j-community-5.26.27-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 11 Jun 2026 00:44:47 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.27-unix.tar.gz
# Thu, 11 Jun 2026 00:44:48 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 11 Jun 2026 00:45:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.27-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 11 Jun 2026 00:45:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:45:08 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jun 2026 00:45:08 GMT
VOLUME [/data /logs]
# Thu, 11 Jun 2026 00:45:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 11 Jun 2026 00:45:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1350f728cccb5e4acd702a6a28a27fecaa06affa2f9968ceb793a2ad9e6068`  
		Last Modified: Thu, 11 Jun 2026 00:45:35 GMT  
		Size: 158.2 MB (158166942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5488ca61c58ea3c2877a6e735e1de11de37d52ffb0fd7c98ae8cd40e441d08`  
		Last Modified: Thu, 11 Jun 2026 00:45:28 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98c4c5537a52eb48954acc88be043e8ecf7a0dc64923595b1aa70561060c0bc`  
		Last Modified: Thu, 11 Jun 2026 00:45:35 GMT  
		Size: 167.6 MB (167614676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:0d9c216e414e56717d24044b98f5bd18196bb89782336985bfb38e3870d3d546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c511935b435a650888af9b14411035d6c74a1895c50e57f965f505c0e5711152`

```dockerfile
```

-	Layers:
	-	`sha256:0e1567e174dd4ddd345e45d4b03391a8e52af0345ffefa3b24641cfc7320d6a5`  
		Last Modified: Thu, 11 Jun 2026 00:45:29 GMT  
		Size: 4.3 MB (4291176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16b7951d93f9c1f1636a96083c65a508c08db6bf53eea1125813c8c271fac8d6`  
		Last Modified: Thu, 11 Jun 2026 00:45:28 GMT  
		Size: 21.2 KB (21223 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:073ae3c57dcc4402cfaed1c4fc237d0136642960528034bc1f9940bba43eda0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.3 MB (353307565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aeab9326cfcde9271aaed1c409b35e8faa21de6d50b826ddb31ec680290fb52`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 00:46:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 00:46:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5e752081e2863febf3d2f11fab31e1a3185e1ea7bb5e0bcf7d8e516ddbec5349 NEO4J_TARBALL=neo4j-community-5.26.27-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 11 Jun 2026 00:46:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.27-unix.tar.gz
# Thu, 11 Jun 2026 00:46:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 11 Jun 2026 00:46:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.27-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 11 Jun 2026 00:46:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:46:41 GMT
WORKDIR /var/lib/neo4j
# Thu, 11 Jun 2026 00:46:41 GMT
VOLUME [/data /logs]
# Thu, 11 Jun 2026 00:46:41 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 11 Jun 2026 00:46:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:46:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f500c1abf82dfbfddc3bba6a79f4de675793f9866cf3bbdc9b81ba96eb25ba`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a93c4d927aa800dd57cb72a42bb01dea3a7ff2d038e9a183651ab8b78b390d`  
		Last Modified: Thu, 11 Jun 2026 00:47:00 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410e54d213501f9cc9f7e69bff4842dd2b656d2bde5199f2b0f2ce52cbe031cc`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 166.7 MB (166687619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:9522a95f94bd223c8c5149bb5dc49e11dff3cebe647f312b27a3faec63833527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4307142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fdf0aaf34a36d394438022c80de20159d26d51120ad1c049a1d3d9731a85fe5`

```dockerfile
```

-	Layers:
	-	`sha256:68d03dd17a5238300f548ecc6cb7ebc5f372159bc38bc07b3fda2979e038ccd7`  
		Last Modified: Thu, 11 Jun 2026 00:47:00 GMT  
		Size: 4.3 MB (4285694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b0e246c1a4bfa8cc1c095fd103ee9610cc5d60cfe0155d5f0f85f8ee05c1624`  
		Last Modified: Thu, 11 Jun 2026 00:46:59 GMT  
		Size: 21.4 KB (21448 bytes)  
		MIME: application/vnd.in-toto+json
