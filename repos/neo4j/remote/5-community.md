## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:88283acc200072a6ef46a63076251ee3955bb69a5b2310d3e6b627338b18fa35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:41eee4658ee0c967bc2143c7cc7c9df1ef90537cdbdaba3f0146433396140763
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291017418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dab1df079a98c656d3bc66f1c35b7b2c83ce34af0b5105f157a04ab2a3c98af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 07:35:48 GMT
COPY dir:e13dbcd57950f4d4d23f4aba8428b6fbbf838d8f4801d32a25e344d37d33c37e in /opt/java/openjdk 
# Sat, 02 Dec 2023 07:35:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54cdf068887eb9371105999992ae874473b8378f6df06cf16b32a4aa36bc586f NEO4J_TARBALL=neo4j-community-5.14.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 02 Dec 2023 07:35:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
# Sat, 02 Dec 2023 07:35:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 02 Dec 2023 07:35:50 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Sat, 02 Dec 2023 07:36:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.14.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Sat, 02 Dec 2023 07:36:27 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 07:36:27 GMT
WORKDIR /var/lib/neo4j
# Sat, 02 Dec 2023 07:36:27 GMT
VOLUME [/data /logs]
# Sat, 02 Dec 2023 07:36:27 GMT
EXPOSE 7473 7474 7687
# Sat, 02 Dec 2023 07:36:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 02 Dec 2023 07:36:27 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4929994d0853caabbfd68ce7ab07e3af7c0e483db2f66881247df513f25c95`  
		Last Modified: Sat, 02 Dec 2023 07:40:56 GMT  
		Size: 144.9 MB (144873901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f3ecc48715aeb33d07ff8f2a12520a7885ae8e9147478778aae095a3e216a4`  
		Last Modified: Sat, 02 Dec 2023 07:40:45 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa60e85d7a3b94ffab28b8f416014d61152878632a12989076913d064867a2b`  
		Last Modified: Sat, 02 Dec 2023 07:40:45 GMT  
		Size: 9.5 KB (9489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a8534eac41907811ec184f29ea4383a6b98a1bfcc38ebb7c1ad4e3000021b8`  
		Last Modified: Sat, 02 Dec 2023 07:40:51 GMT  
		Size: 114.7 MB (114712340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f28741ec0e2bc6b4beffbf32026b11311b0c8cfbd24069893bf16ab741c88fa9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289274766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b49430bb9c8b01aa5087b38d91c3060bfd7be63cb69ebd4dfa7e33975acaa00`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 08:54:33 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Fri, 15 Dec 2023 19:53:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0090ee5fd8ca5718ced107d5e7a7803919f55b970c3e7acad83bf88292a2361f NEO4J_TARBALL=neo4j-community-5.15.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 15 Dec 2023 19:53:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
# Fri, 15 Dec 2023 19:53:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 15 Dec 2023 19:53:44 GMT
COPY multi:8fee13a85b98996afa1dd437b17591f4356f4c453ab9a107827f32427bb071da in /startup/ 
# Fri, 15 Dec 2023 19:54:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.15.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec
# Fri, 15 Dec 2023 19:54:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Dec 2023 19:54:12 GMT
WORKDIR /var/lib/neo4j
# Fri, 15 Dec 2023 19:54:12 GMT
VOLUME [/data /logs]
# Fri, 15 Dec 2023 19:54:12 GMT
EXPOSE 7473 7474 7687
# Fri, 15 Dec 2023 19:54:12 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 15 Dec 2023 19:54:12 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d93fb72555944d51d7e18e85dbba1405725af6fa11dc155f20ab3dc455df52`  
		Last Modified: Sat, 02 Dec 2023 09:08:50 GMT  
		Size: 143.7 MB (143681749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d231bc995d177519536f3394d00334e961ba4ce52b39a4de4e5655ac3265e9f4`  
		Last Modified: Fri, 15 Dec 2023 19:57:41 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdfd6cc00534f53f3ba3907fc83af82d3a122113ac12e9bfc194a82cd46fa9`  
		Last Modified: Fri, 15 Dec 2023 19:57:42 GMT  
		Size: 9.5 KB (9488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5a282811d905ae461208da4adbc648e78d0515e819bb2ae9d88c5c7534f8d9`  
		Last Modified: Fri, 15 Dec 2023 19:57:46 GMT  
		Size: 115.5 MB (115515518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
