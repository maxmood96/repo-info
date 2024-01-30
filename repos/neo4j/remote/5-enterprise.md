## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:a6cf066e12fa44f92d4998cb015137e0a221d696d6e4219a4a82cd862e9b0828
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:af6a3153f2fd3b7ae1dd5a300ec16868ce01b4f439198565ed0fbc4b7770c5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **547.7 MB (547747313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae560c39df85813e8bdcb9280d3789c254210e20899b5fef1a1e0ce7ec366701`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77833212e25fec8c89ffefaa57feb4b866f2295d9e9a9ebd440a904fb330e91a`  
		Last Modified: Mon, 29 Jan 2024 22:52:25 GMT  
		Size: 144.9 MB (144892412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c00b19fd07ccd282c75c97ccc07f77cdc3d0292055759afc5b96a756968e5ab`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d5dba03cda87e813ae34c407bc6098f18a0d949abb322458a9b98a87507664`  
		Last Modified: Mon, 29 Jan 2024 22:52:22 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b2f41c77192eda268eb031a937141977b65230d5875910333991118eee8a0a`  
		Last Modified: Mon, 29 Jan 2024 22:52:29 GMT  
		Size: 371.4 MB (371423625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3a099b5e38f44c81ce4d48840b028285c969364a1fcabe2d9d7d33720317804d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22707f2a029dd7b55d4cb8815941fc9fe5298242b9852d449de4bb6178acde4c`

```dockerfile
```

-	Layers:
	-	`sha256:eaa7a46aa23d3f5868ad4e07f4aa9e0cc8fe8c9338bf8c8bafc776cc9c35ba12`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 2.7 MB (2656206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b475692f548dc3c7aaddd666c8a7d8a3ef8a0bfa8eaa39e9c4fe161c9144c6`  
		Last Modified: Mon, 29 Jan 2024 22:52:23 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7317e1a955c352fcbf3330be440b853af8674660fd61fed941f01b5e22793525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.2 MB (545190884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd34a97f2ded79ffdc2bbf6a0b1a2b3875ecae2b92c6e559169a834ed95a3bd3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Mon, 22 Jan 2024 14:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jan 2024 14:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8f2e3719aa29e0542b2cae62bcbd8961bad3686bab5f2a546be681adb6b38746 NEO4J_TARBALL=neo4j-enterprise-5.16.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.16.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jan 2024 14:26:01 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
VOLUME [/data /logs]
# Mon, 22 Jan 2024 14:26:01 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 22 Jan 2024 14:26:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 Jan 2024 14:26:01 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e9a3857fa9c787c478b67599ad6e19f8c9b0301c9026e1eee6704f361c02a`  
		Last Modified: Tue, 30 Jan 2024 01:00:10 GMT  
		Size: 143.7 MB (143720399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f236b9f14053986036912d6cdfc5eb37714244b1d98ccb659b183a263712a`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bb491135f1fa074e6b583af09b6e260232cc162d11aa5079b941e9ade3b01f`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fdd5770ebea8c8ed064e97c32e441216ab6577d1cc62235b693d04a67c2791`  
		Last Modified: Tue, 30 Jan 2024 01:01:37 GMT  
		Size: 371.4 MB (371393127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:81f2e487104df991531092cf42da65e5d1214ee8e485d61f59261c00abba2cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2677047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d75a9c969713dcc0ac7ec7e447328a0d7733fa2a1de413a48fda57560e92d17`

```dockerfile
```

-	Layers:
	-	`sha256:c4d0a099b146c21c8ba110c91cd225082be5d0fc030539f72e33c589ddf00ca1`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 2.7 MB (2656540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5874394369b71ab4f00ab4ec58aa12b98ccd8244440056bf6b99eb3e0b32bd51`  
		Last Modified: Tue, 30 Jan 2024 01:01:28 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json
