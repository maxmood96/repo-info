## `neo4j:2026-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:29d9e80326ba153c5659ef7fec6782c240d9abe958ce56e52a1b00d1b6fb2a78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:834e87279721ef0b24a2d76f7f6d4d0d3517944c14702cab4f508b0ca67266bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.6 MB (553554323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b17a9347e36c0283a72a8b0eebcf7a1bc2d331590529382e643740e04eb12e1e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 22:50:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:50:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 22:50:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3326a905d4accc1bdd224923a6d30c9a498bbd0fb7b43e87983aec29734c367d NEO4J_TARBALL=neo4j-enterprise-2026.01.3-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 05 Feb 2026 22:50:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
# Thu, 05 Feb 2026 22:50:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 05 Feb 2026 22:50:24 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 05 Feb 2026 22:50:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 05 Feb 2026 22:50:47 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:50:48 GMT
WORKDIR /var/lib/neo4j
# Thu, 05 Feb 2026 22:50:48 GMT
VOLUME [/data /logs]
# Thu, 05 Feb 2026 22:50:48 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 05 Feb 2026 22:50:48 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:50:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedcfaa7b96cf7ac176b25af0a29dba4319470ecab522a1709d851a8e29f11f3`  
		Last Modified: Thu, 05 Feb 2026 22:51:05 GMT  
		Size: 157.9 MB (157857090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d4a451a74588426c36cdf632844a8114cfe8d37d4c9d9a12ad31c4aab2322d`  
		Last Modified: Thu, 05 Feb 2026 22:51:15 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730c2d2e61263fcd613e9e8686216fde7e59f1cc4e39e27de61fe32fe22a3e12`  
		Last Modified: Thu, 05 Feb 2026 22:51:15 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569811c2c78ce0f55017cfe8008fa39a522c453c71f9720924bad756244243e2`  
		Last Modified: Thu, 05 Feb 2026 22:51:22 GMT  
		Size: 365.4 MB (365424891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:de97ae1828e68aa321624afa23c2e0ca7c9db24fa2b694227db4b7fd854d5564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4875921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922e52cdbc5b88ae2c11de23078fd1daf53fb4b69ff58e0db0b988701182b810`

```dockerfile
```

-	Layers:
	-	`sha256:6b92b0783369679b7cbfa2a20c7c7b627f250d687f39b9d270c9c65dcb9e7527`  
		Last Modified: Thu, 05 Feb 2026 22:51:15 GMT  
		Size: 4.9 MB (4855525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6723f56fbbace91d57b190dd2481d99c778604388acdc421f8b5b50bd1040259`  
		Last Modified: Thu, 05 Feb 2026 22:51:15 GMT  
		Size: 20.4 KB (20396 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d27bf0b7c41fbd93047a63aa7673c15328acc855934303c5eaeca22369fe31a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.6 MB (549561934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04bcda5ec609137d9feba2b0fd1f51b860f9c0a3a715122bec92a5df6ae3fa24`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 22:50:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:50:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 22:50:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3326a905d4accc1bdd224923a6d30c9a498bbd0fb7b43e87983aec29734c367d NEO4J_TARBALL=neo4j-enterprise-2026.01.3-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 05 Feb 2026 22:50:23 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
# Thu, 05 Feb 2026 22:50:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 05 Feb 2026 22:50:23 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 05 Feb 2026 22:50:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.3-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 05 Feb 2026 22:50:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:50:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 05 Feb 2026 22:50:46 GMT
VOLUME [/data /logs]
# Thu, 05 Feb 2026 22:50:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 05 Feb 2026 22:50:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:50:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e988328ecdafe875f4abda2797efe461b11507c3526bba5b941a7aacf81f100d`  
		Last Modified: Thu, 05 Feb 2026 22:51:17 GMT  
		Size: 156.1 MB (156133048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc4f4c492cd785c62121d93acaf92fc9ddb18b13e315ac2095c07d87d290e47`  
		Last Modified: Thu, 05 Feb 2026 22:51:03 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5279f97cd16aa3e80380a91487ad42a26d30193cbe821e920ba1c7642335027c`  
		Last Modified: Thu, 05 Feb 2026 22:51:12 GMT  
		Size: 10.2 KB (10188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ea8fcb5308ba35609525d4d6aa73048cc3931aa49f1cf82737780a301c9e79`  
		Last Modified: Thu, 05 Feb 2026 22:51:20 GMT  
		Size: 364.7 MB (364670359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:548693fffa74498c2708eed6a411c37bc797e5703a9abe8ccb531e3fb6070aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4849849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7023d5762082b1dbe87f76e53bb0b8f9b997d49e20acf40065f87af49193d7b1`

```dockerfile
```

-	Layers:
	-	`sha256:1a37026bb74249c5441f10b0889ca6582ba2efddeb1147ec3e65be7c2f891152`  
		Last Modified: Thu, 05 Feb 2026 22:51:12 GMT  
		Size: 4.8 MB (4829306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95f0246c027ba620d49aab71e16929bf19d77924493a6368ae9a7170ff8ac3b0`  
		Last Modified: Thu, 05 Feb 2026 22:51:12 GMT  
		Size: 20.5 KB (20543 bytes)  
		MIME: application/vnd.in-toto+json
