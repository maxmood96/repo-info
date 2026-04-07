## `neo4j:5-enterprise-trixie`

```console
$ docker pull neo4j@sha256:b58dbfee63f92c6d900dbb87662303d448ca7bf238edf3204e8ca0b2a2156b9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:4b84111f32f74e521caf9e00e85c7c60e650a06244658626dfa55d9ae48c088d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **710.6 MB (710629879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce2b3f25e411975ad8ced68a907aeffe2574894662322ac5ef66dd7d7d72de6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:58:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 02:58:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0c97832ac9dd7172c2315c58b957c343644d4f50a863951976bb1b25ba291f5a NEO4J_TARBALL=neo4j-enterprise-5.26.24-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 07 Apr 2026 02:58:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.24-unix.tar.gz
# Tue, 07 Apr 2026 02:58:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 07 Apr 2026 02:58:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.24-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 07 Apr 2026 02:58:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:58:43 GMT
WORKDIR /var/lib/neo4j
# Tue, 07 Apr 2026 02:58:43 GMT
VOLUME [/data /logs]
# Tue, 07 Apr 2026 02:58:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 07 Apr 2026 02:58:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:58:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc254b2f52c3d5ac4a99d60430bd4f8da9394e31163c37c3f4292e6b13d92431`  
		Last Modified: Tue, 07 Apr 2026 02:59:18 GMT  
		Size: 157.9 MB (157857076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871fb4ecd3ec3ba91e3fd1e57ea167c9f9d44e7b31fc16fbe7a492e48e1f9757`  
		Last Modified: Tue, 07 Apr 2026 02:59:13 GMT  
		Size: 10.1 KB (10064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3309999902eccda4a7bfbe9be041b8a4226c64d5ba8dce57aedc7749629c0a24`  
		Last Modified: Tue, 07 Apr 2026 02:59:26 GMT  
		Size: 523.0 MB (522987067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:3c229d21c1dafe933b1575bc506e389221a800d037f46a76745d411a23eac21a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4679860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584db56cf6d0a069f08baa78dd8a8c38065c177f0281aa00030ec43ee6f7a873`

```dockerfile
```

-	Layers:
	-	`sha256:b6852332f83949ba34f16410bdf1623601a1fff04ba445f9feafb7be8f2a19ee`  
		Last Modified: Tue, 07 Apr 2026 02:59:14 GMT  
		Size: 4.7 MB (4660564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0624f452300781312b3f16a01619f4b2b6ac0a9cba33c9ded68c1888b1070428`  
		Last Modified: Tue, 07 Apr 2026 02:59:13 GMT  
		Size: 19.3 KB (19296 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:df341da2da0ebc81314d9f4cb7af748fe90125ceaf5aae188034112552b92cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.3 MB (708336836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1b48972284365d754d77ee096d690453ebf8e9fd8ddcd9b84a1222382f3200`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:11:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:11:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:11:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0c97832ac9dd7172c2315c58b957c343644d4f50a863951976bb1b25ba291f5a NEO4J_TARBALL=neo4j-enterprise-5.26.24-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 07 Apr 2026 03:11:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.24-unix.tar.gz
# Tue, 07 Apr 2026 03:11:06 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 07 Apr 2026 03:11:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.24-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 07 Apr 2026 03:11:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:11:35 GMT
WORKDIR /var/lib/neo4j
# Tue, 07 Apr 2026 03:11:35 GMT
VOLUME [/data /logs]
# Tue, 07 Apr 2026 03:11:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 07 Apr 2026 03:11:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 07 Apr 2026 03:11:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f28b6d4a43b2c895e78bfa8358d9a05d867adaff51768a5cf6a27b483bc70be`  
		Last Modified: Tue, 07 Apr 2026 03:12:13 GMT  
		Size: 156.1 MB (156133032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020b10f06870bdcdd90a7a989bd455d043192d16d588931892c2a932ac8a9241`  
		Last Modified: Tue, 07 Apr 2026 03:11:48 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a7c19d26ef3dc20dce9b21d05cdb2ddae5e74e9747a4a65f4adb90404997b9`  
		Last Modified: Tue, 07 Apr 2026 03:12:19 GMT  
		Size: 522.1 MB (522055161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:fcab1f79a19f21e2732e7fc309c59c83a3c7e5807e971d22a2bcb28408ceac73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4674469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc98517330489ae7b1474970aff34190a7fead7bb2c9350d7a9de56e30a74e63`

```dockerfile
```

-	Layers:
	-	`sha256:c68217255869c23906395ef66e47e594fae0b5a17e2cd902358e949dd15d01c8`  
		Last Modified: Tue, 07 Apr 2026 03:12:07 GMT  
		Size: 4.7 MB (4655018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eef59ee86f950bd3c1f96988440ffd4b8c794f5d89dc5748bc67a4736516ad5e`  
		Last Modified: Tue, 07 Apr 2026 03:12:07 GMT  
		Size: 19.5 KB (19451 bytes)  
		MIME: application/vnd.in-toto+json
