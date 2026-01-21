## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:58f064e2f8ce7b6a790704cb576e5792a06f1a30ef2c10589a1dda8ead74d768
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a57e737f280d028c09df616ecb075659e7ac6267737411615b5519a7d698d715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.5 MB (668499106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8746145861a98e67ffc4deb0fa73ab9ce323768be0a7ddc2dd976039cbc3f77`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 00:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 00:38:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 00:38:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4090c59d7959304579e5725902d3c1cf0c5ffc5852da6e68d2f0cdd4e84bc3f2 NEO4J_TARBALL=neo4j-enterprise-5.26.19-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 16 Jan 2026 00:38:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.19-unix.tar.gz
# Fri, 16 Jan 2026 00:38:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 16 Jan 2026 00:38:48 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 16 Jan 2026 00:39:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.19-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 16 Jan 2026 00:39:15 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 00:39:15 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jan 2026 00:39:15 GMT
VOLUME [/data /logs]
# Fri, 16 Jan 2026 00:39:15 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 16 Jan 2026 00:39:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 00:39:15 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766b5a51319239db2e62d2d93f88c9bda644e4d98ad4b32531a2126e5d9a9a69`  
		Last Modified: Fri, 16 Jan 2026 00:39:49 GMT  
		Size: 144.8 MB (144847971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e679949712117e57d26a0585f367aeb3089d3005a6952191fc6ccca2b13add2`  
		Last Modified: Fri, 16 Jan 2026 00:39:44 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb47fab7a08b8ab32ebf3f0d90bb596429e653e568c0fc50512a43977ad5840`  
		Last Modified: Fri, 16 Jan 2026 00:40:01 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e451c8fe79346484a6c0c79f5caeda9c6562d6121309008d57fe94a2a6e2ce82`  
		Last Modified: Fri, 16 Jan 2026 00:39:56 GMT  
		Size: 493.4 MB (493378712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2282a97002f0ced654d763ab89b8638572bd843fd7073a991a287b4501eb91a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4868197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a165efe2b79c3c8b4783b417ce29b2d6f35d9681e73949732561d5f46e46f036`

```dockerfile
```

-	Layers:
	-	`sha256:f887a299bc53803bd57067b7a84549b49d22d740c2ba9d811bd5c766648537fe`  
		Last Modified: Fri, 16 Jan 2026 03:45:00 GMT  
		Size: 4.8 MB (4847212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b36d03cd5735cdeab644724da84775feae8614ecdefe4c16bdb9d101f753ea6f`  
		Last Modified: Fri, 16 Jan 2026 00:39:45 GMT  
		Size: 21.0 KB (20985 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3fb247e6eb8132167a66b9ec13d061e269501595bb68e007c8e51f29d7891f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.1 MB (665065055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5cc31f80db1fb4ba4c93300486bb3ab5ca92a49c40ac4d8f39f6eafe2e4755`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 00:41:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 00:41:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 00:41:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4090c59d7959304579e5725902d3c1cf0c5ffc5852da6e68d2f0cdd4e84bc3f2 NEO4J_TARBALL=neo4j-enterprise-5.26.19-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 16 Jan 2026 00:41:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.19-unix.tar.gz
# Fri, 16 Jan 2026 00:41:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 16 Jan 2026 00:41:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 16 Jan 2026 00:41:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.19-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 16 Jan 2026 00:41:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 00:41:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jan 2026 00:41:36 GMT
VOLUME [/data /logs]
# Fri, 16 Jan 2026 00:41:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 16 Jan 2026 00:41:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 00:41:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a5fc1c780c6255e1c74e20b6363b45e8353e32823653e6ea0c3d41b6004989`  
		Last Modified: Fri, 16 Jan 2026 00:42:33 GMT  
		Size: 143.7 MB (143679930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4f454851b5ba7e8430a0f7f68e014ee873298b98eadba1d826d4a9441befda`  
		Last Modified: Fri, 16 Jan 2026 00:42:07 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff0968ae446b381c4e67387be0f37b67b916d920582d670545db984e054acd4`  
		Last Modified: Fri, 16 Jan 2026 00:42:22 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8ef92c8ad96e687afacf9240db3a91b4a6b723001f679624b41864cf6a16`  
		Last Modified: Fri, 16 Jan 2026 00:42:50 GMT  
		Size: 492.6 MB (492622646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:18c43a84f43804903e2e509295997e7d5f8467792331198c8536deabe37e7ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4842171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744bf27148bd0cd7ad0768ac2ac21d036d8fd58f876692971074d5943a178559`

```dockerfile
```

-	Layers:
	-	`sha256:8aafeb81787d80921cfacf00c15f2977b9f2ab945180daa71eaa2c271af639be`  
		Last Modified: Fri, 16 Jan 2026 03:45:06 GMT  
		Size: 4.8 MB (4821017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f8c18ce960da76e71b4883c1b085aea257a89cccb3df786e8b0c6492f051141`  
		Last Modified: Fri, 16 Jan 2026 00:42:07 GMT  
		Size: 21.2 KB (21154 bytes)  
		MIME: application/vnd.in-toto+json
