## `neo4j:5-enterprise-trixie`

```console
$ docker pull neo4j@sha256:0f4ab99cde6cfc71f7a268b93e4db8fb64c22faaef7a8a0df19483bd17e8f858
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:72ac5f9ce7138098f1ffb52a2c1abd4fd0eb124accb84ec1a967d17207bba325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.1 MB (695089069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f44908ef099bd6442cc203d31cdeb2edc8d442abcbe042ff4e8579275c6591`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:26:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:26:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:26:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e417825ffda8b405de7bb7b45788d3810ff270fbe09b7ddc12fb2a6a09de737d NEO4J_TARBALL=neo4j-enterprise-5.26.26-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 19 May 2026 23:26:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.26-unix.tar.gz
# Tue, 19 May 2026 23:26:16 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 19 May 2026 23:26:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.26-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 19 May 2026 23:26:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:26:57 GMT
WORKDIR /var/lib/neo4j
# Tue, 19 May 2026 23:26:57 GMT
VOLUME [/data /logs]
# Tue, 19 May 2026 23:26:57 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 19 May 2026 23:26:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:26:57 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c613b9171b8444545cb084d81fb72164978a9cd0ac22db51847c0f03d7c46559`  
		Last Modified: Tue, 19 May 2026 23:27:32 GMT  
		Size: 158.2 MB (158166943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2008912f29a68177c11dc1b8862040fee7be8b9ba571a94b65015f9dc5714c3`  
		Last Modified: Tue, 19 May 2026 23:27:26 GMT  
		Size: 10.1 KB (10058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3233d96d7ce886bbd7c9df79b645ee32505b6ae73e7acf179daef3ae0651fb`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 507.1 MB (507132110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:05beaf514a1e2151d3a058626bbc1f072bc5bb614ee4514571802b360362b0cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4671499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc55810563b2a7bde7b4d56fe08e6ea7a19d6dba42d9d334dc1722d154f1bb2f`

```dockerfile
```

-	Layers:
	-	`sha256:e39fc0d73358689f417a5dd172e791450231aaa193dcd7580b6ad0f289826ebc`  
		Last Modified: Tue, 19 May 2026 23:27:27 GMT  
		Size: 4.7 MB (4652048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20333f9d2993f57cf4ddca1f792649286a159de39b01250817e339088590ce0e`  
		Last Modified: Tue, 19 May 2026 23:27:26 GMT  
		Size: 19.5 KB (19451 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3872d0d7f1c327090b08a9c444bf6edaf170bd76ee852a052e5b841cb4683923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.8 MB (692816684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676244759697219b75d9b4463cd86452b78bec652dd35103bc440e0e9de7be7c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:29:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:29:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:29:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e417825ffda8b405de7bb7b45788d3810ff270fbe09b7ddc12fb2a6a09de737d NEO4J_TARBALL=neo4j-enterprise-5.26.26-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 19 May 2026 23:29:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.26-unix.tar.gz
# Tue, 19 May 2026 23:29:54 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 19 May 2026 23:30:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.26-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 19 May 2026 23:30:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:30:24 GMT
WORKDIR /var/lib/neo4j
# Tue, 19 May 2026 23:30:24 GMT
VOLUME [/data /logs]
# Tue, 19 May 2026 23:30:24 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 19 May 2026 23:30:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:30:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaefe7fef97464ca5aea32c07c0ee1e6b105e9d61ccc530c3da54463c57655a`  
		Last Modified: Tue, 19 May 2026 23:31:02 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7deee8c51140b9f81e46b8fa6c6edafa15636930c4428a4faa77eee5901d44`  
		Last Modified: Tue, 19 May 2026 23:30:55 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec048cb0e870433cc390c47504090ad5f9fa1267c558861888484b9d8498268`  
		Last Modified: Tue, 19 May 2026 23:31:11 GMT  
		Size: 506.2 MB (506203347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:d838d515c2919520d2a5d152c10f09edc348a2bdb04f43b5aa82e574cde35c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4666099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395212f27b81a38efc6f98be36198b54e9f7a4186efa473560e0bc55a82bb73d`

```dockerfile
```

-	Layers:
	-	`sha256:77ee66f36560df6d5ec0b6a3e984a6d689fb218f6dc446fb243a43cb327ab824`  
		Last Modified: Tue, 19 May 2026 23:30:55 GMT  
		Size: 4.6 MB (4646494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a758133b67584fca83846a4dff408737e822496be921de9913cf8f0fba9282b`  
		Last Modified: Tue, 19 May 2026 23:30:55 GMT  
		Size: 19.6 KB (19605 bytes)  
		MIME: application/vnd.in-toto+json
