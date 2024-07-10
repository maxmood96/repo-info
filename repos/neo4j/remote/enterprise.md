## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:ba2b323bce8373519a86a03a813c4efefa448cf3d65b0908e64ab817c10265f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:418a574219584da03717b1064090afb6a2fef0c925c76e625fa608824be19350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.4 MB (589365163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f9959cf5bee6cf4d64be50ee3364f2e76d7d1e36c29cecaca52a987466c1750`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9850004735377a931bafa0889f753ec5cf73cd6760b43971ab774024584241f1 NEO4J_TARBALL=neo4j-enterprise-5.21.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d1b83553e4a03d82e118bcd494bb14b21d56d3058dad54513aa56e0936f0d0`  
		Last Modified: Tue, 09 Jul 2024 18:59:02 GMT  
		Size: 145.1 MB (145095124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3db6b858c4859a04e8cc8e048f7c8c974946fbba6e60c712169038d5ca03720`  
		Last Modified: Tue, 09 Jul 2024 18:59:00 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe73a7b538165dfb160db8cfbdb707460bb01851cbb0b1a7818488bc23f12eb`  
		Last Modified: Tue, 09 Jul 2024 18:59:00 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120c6f5b9587bd120aa39f4025071fc00e77aa26502936773e958dc75fe12f89`  
		Last Modified: Tue, 09 Jul 2024 18:59:06 GMT  
		Size: 412.8 MB (412834261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:04dbf2626eb0f72f7a7f095ea5b0762c26f6aa0c60c3d4ba0d348278fb200791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be74cd4ca625ba4193512c23ad712485ef229c7774dfad1c1982e322f54f0b5d`

```dockerfile
```

-	Layers:
	-	`sha256:2e6ab85112e85b0388512a4ef56d01df3bd12875cad1f74905263c0c1b85ab86`  
		Last Modified: Tue, 09 Jul 2024 18:59:00 GMT  
		Size: 3.2 MB (3188082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37e39f3552ddcb8296b5adb27d929fc5b09e8b7361dbc5203556811188171093`  
		Last Modified: Tue, 09 Jul 2024 18:59:00 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c16f6edf08a2a6d9082a266659626a2c1a943e5ded2d202b76b00a974dc0a0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586774715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43fb7aa8c8437f216e0f34b4c9c7afc9b49a883fb6e1515e5f2b432b5b88e6f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9850004735377a931bafa0889f753ec5cf73cd6760b43971ab774024584241f1 NEO4J_TARBALL=neo4j-enterprise-5.21.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597e193394a16e7ce4f7319f265eb4490e90781352261c19ce610805e4db1d9e`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab12acc287d76f7ee208891bf35d50474ef788d26c99d013d705ab4e4b6e52b`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60fc92950c63e0570a22a3c93548bbf86519afcb11354c0f86d73ad269d5a17`  
		Last Modified: Tue, 09 Jul 2024 19:39:38 GMT  
		Size: 412.8 MB (412798793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:fc6ef7512d3e9cbe1095837fd751001d3b5fe4e85e1b691a23371396cd66db44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf741080bc44fe0b7220172f01f086c918fad2dc889918f935ac214a65bcd576`

```dockerfile
```

-	Layers:
	-	`sha256:40eac872f4ca581a51573364af436cbbbb85d33a3285d9eb9da982b08c61732c`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 3.2 MB (3188393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44b1734c8c05490e3e5f8cae58ce3093774c756ee923760bfe51998554ba3807`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 21.6 KB (21561 bytes)  
		MIME: application/vnd.in-toto+json
