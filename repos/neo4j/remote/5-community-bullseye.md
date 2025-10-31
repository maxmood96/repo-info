## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:2cd259494d695bc726515685715e9d88776eb60456410020d392601738254cf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:e6ef56dcbc5bb73a333339860a744ba3c49aae03b6ac1a5a90d7a85dcf3db4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 MB (305750628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d624e13f07aeb436b26403261b74eee3ea5b2577b0dd9095f8a0b8e3a77c2e6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 20:49:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Oct 2025 20:49:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Oct 2025 20:49:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4ae618c5d781fa73560aaf001da49b502989ebd00c593ba80d3331d0b0c8aad3 NEO4J_TARBALL=neo4j-community-5.26.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 30 Oct 2025 20:49:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.15-unix.tar.gz
# Thu, 30 Oct 2025 20:49:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 30 Oct 2025 20:49:56 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 30 Oct 2025 20:50:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.15-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 30 Oct 2025 20:50:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 20:50:18 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Oct 2025 20:50:18 GMT
VOLUME [/data /logs]
# Thu, 30 Oct 2025 20:50:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 30 Oct 2025 20:50:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 30 Oct 2025 20:50:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aba188c4461707a5cb65724674b318212ad55d90f3115e49738eed9e1883af3`  
		Last Modified: Thu, 30 Oct 2025 23:44:50 GMT  
		Size: 144.7 MB (144693321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfb75c211393fbd853c1aa9e06444c4340271010fbc22f53bc2eb5ece6e0a1e`  
		Last Modified: Thu, 30 Oct 2025 20:50:46 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df77151e38bbd06f94e36c7cec1cd2773232baa1ed9527c82439e2539c3bc15e`  
		Last Modified: Thu, 30 Oct 2025 20:50:46 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622dd870770a8048dce3cb5707a51dbdb22c4aad7590d1d8d7d6556cde0f7284`  
		Last Modified: Thu, 30 Oct 2025 23:44:46 GMT  
		Size: 130.8 MB (130785008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5ef3c933cd9fe5d43ac9d64e415ceaef1a03f28c6b4145cc950b13caa0616e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d997ee834cb09ca6072a3af0c4325c1e0a836af2b77442494b1e5ce0caf9a604`

```dockerfile
```

-	Layers:
	-	`sha256:be4c7f4ca31726210fff53b527019bb496ba4830ebe77221d23b96acf1ecff0c`  
		Last Modified: Thu, 30 Oct 2025 23:44:37 GMT  
		Size: 4.5 MB (4482984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:860a4dc900897ab21a0712e51b6d6049177e6f6a24e01bf5cc475439d585f2d6`  
		Last Modified: Thu, 30 Oct 2025 23:44:38 GMT  
		Size: 22.8 KB (22765 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d658c771b8483ef1dc3f69b1b97c1597f7b7c43e7fead932ca22426a7f820d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302333064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebe3fc8257556a2243fc40089007daad69ba140a1812ae94f140e35657a3ce8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Thu, 30 Oct 2025 20:50:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Oct 2025 20:50:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Oct 2025 20:50:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4ae618c5d781fa73560aaf001da49b502989ebd00c593ba80d3331d0b0c8aad3 NEO4J_TARBALL=neo4j-community-5.26.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 30 Oct 2025 20:50:50 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.15-unix.tar.gz
# Thu, 30 Oct 2025 20:50:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 30 Oct 2025 20:50:50 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 30 Oct 2025 20:51:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.15-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 30 Oct 2025 20:51:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Oct 2025 20:51:07 GMT
WORKDIR /var/lib/neo4j
# Thu, 30 Oct 2025 20:51:07 GMT
VOLUME [/data /logs]
# Thu, 30 Oct 2025 20:51:07 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 30 Oct 2025 20:51:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 30 Oct 2025 20:51:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04f6c1253e1eebbf2726dc355260b3fb35803848fbc96b9ed50d1f7a4dc25d8`  
		Last Modified: Thu, 30 Oct 2025 21:09:25 GMT  
		Size: 143.5 MB (143542115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f43586789212e1079256bbeace621b518f795c68e4edead64743bf3374a8c0`  
		Last Modified: Thu, 30 Oct 2025 20:51:35 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4132ae4c9c2cc0f0098d9ebc4582e34b53cfbdccc3aba19ccbb53a69e946468`  
		Last Modified: Thu, 30 Oct 2025 20:51:35 GMT  
		Size: 10.1 KB (10059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b883b8dae807378b8f45a06c40ea2174008a20df8340ebc8508218ec54c91f`  
		Last Modified: Thu, 30 Oct 2025 23:45:48 GMT  
		Size: 130.0 MB (130028588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:f69ae918328ab3644a9fd50666152ed65eb74ec5d48d179f6c08e355b3203699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4479868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f906fe1d637f9029433d9c6f69193dc7b46b1734fdda873f53a6887e15713bc`

```dockerfile
```

-	Layers:
	-	`sha256:3069d1c250164c51117b389bf32d1779459ceb07303c780e4fafba0885990809`  
		Last Modified: Thu, 30 Oct 2025 23:44:44 GMT  
		Size: 4.5 MB (4456861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f510f2124d9360de740bad9eff14be8dab6f0581822ac4eb9a71cc948fceb59d`  
		Last Modified: Thu, 30 Oct 2025 23:44:45 GMT  
		Size: 23.0 KB (23007 bytes)  
		MIME: application/vnd.in-toto+json
