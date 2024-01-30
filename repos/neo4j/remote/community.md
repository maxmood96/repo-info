## `neo4j:community`

```console
$ docker pull neo4j@sha256:a2a5761ff2b64dbb6994b565efb033b4e9f29593f1814a44f997af93c74c3d78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:02e94889bfdccda5e1df788bce318cf9e9e15f9a722d00f9d779a1a088868164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291729649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41a7d077c70ffc0ca470186c8d1fb350f9e7375cf69a909c67da15680649d55`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
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
	-	`sha256:6fdd164e574d382064d235142d8125a7b48b8e31a8802a873c97f35056c84646`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 144.9 MB (144892392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e640e178427e2744c87f3ff92c1088608d383624b5943e61ff6629ea9c5910e`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2271b1126d85db3ff847b53791c67519d0abc0fb4a588bc191bd77b7530cffae`  
		Last Modified: Mon, 29 Jan 2024 22:52:16 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b973a7341b7510b79b95255b12fec3855e3e98cadcb930f53126464c6fa99e3`  
		Last Modified: Mon, 29 Jan 2024 22:52:18 GMT  
		Size: 115.4 MB (115405978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:461308ea69c0d5dfae03f3a0d796b088cdb76a6917b8ba16edc8c303c857953d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0013396f551d23feea11f96887c99d3ff29f4ece4987e2b79a09eadefeb4be7b`

```dockerfile
```

-	Layers:
	-	`sha256:f83e9eb9e29b1f0010aa6df3cb6c83150148144448b8b01a672aaf7ab77a66da`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 2.5 MB (2470928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fede8b547207e15592e7077970bc02d38c4c4b40c4deb607a3d62f2a03c794`  
		Last Modified: Mon, 29 Jan 2024 22:52:15 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:36351791c1a1937ad0ed4126482dc8f7ec6e1493daee5844e0ae19bd8affbf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289166756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fafeab46b9cbe0e94960ff971b9dd8d1918ad711edfa00a05c59d5de08f92b8`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5de9518ceef86d3e87aeb513cb996f6f3f4dce11db5bb1d2308cab327deb9890 NEO4J_TARBALL=neo4j-community-5.16.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 Jan 2024 14:26:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 22 Jan 2024 14:26:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.16.0-unix.tar.gz
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
	-	`sha256:11b457c81b1800e6763c67b856b9a449491dcff861c99d29ba304855937936b1`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a3fc3c2079ad4759d043621ef8778c62c62c91cebcceec2854d28075c79d05`  
		Last Modified: Tue, 30 Jan 2024 01:00:05 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af8e5bf1888dfc5d9c528c259e2c147a74c04e2ec0bf68688ad53246585e81`  
		Last Modified: Tue, 30 Jan 2024 01:00:09 GMT  
		Size: 115.4 MB (115368992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5628740ac4f9529f9eb7b26fd5791ce1511c7e7cc281c7e7486e657c7b32294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42528782fbea9aa5a50494e586aaab6476bbdcd03c06e016764660d9f284292f`

```dockerfile
```

-	Layers:
	-	`sha256:8cff22d7206a582400976334ae97a91909135fd7932e63e2c72f35af7deed474`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 2.5 MB (2471278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:effd8cfe9897ba278413f817f7ffbebd7f691fecffe68ea92a51a756185f6767`  
		Last Modified: Tue, 30 Jan 2024 01:00:06 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json
