## `neo4j:2025-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:770b3c4822e7e06915a34a384680624ecd5f5a279cad4cf0505746b72a48b4cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d90d6a858281090e1f4c198c6c10e28bb18d22cc0ac0ed1e3e5b4709bcba300e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.4 MB (529431048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50188d71e9f848e6f651210ab1d60f3bf889436e2f4b725130d6edf47093748`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Jun 2025 10:48:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Tue, 03 Jun 2025 10:48:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 10:48:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=20c1d8a43608aa943885c80d2b496b25aa51126f605a0c0e5b8399424da6aff4 NEO4J_TARBALL=neo4j-enterprise-2025.05.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Jun 2025 10:48:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.0-unix.tar.gz
# Tue, 03 Jun 2025 10:48:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:48:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Jun 2025 10:48:21 GMT
VOLUME [/data /logs]
# Tue, 03 Jun 2025 10:48:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Jun 2025 10:48:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Jun 2025 10:48:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81aa7e7f1fb42d43470866ba7e7aaa57730fc6fe3d6b5e3addb47d2ed380f9e2`  
		Last Modified: Wed, 11 Jun 2025 03:00:29 GMT  
		Size: 157.6 MB (157634503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f078f54dd01ea0ffd19a6c0c4cf41e6602d7b2143265423ea5c5c6571083b5c4`  
		Last Modified: Tue, 10 Jun 2025 23:39:57 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6866a6a6f91f9b4c90fb2bab8509bf98bb2971dd16796d3df336a8294156a36b`  
		Last Modified: Tue, 10 Jun 2025 23:39:57 GMT  
		Size: 10.0 KB (9979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db86b90447fef71557e06ad82e8bd5d43208167ac40484a78cafc5ff17cc44`  
		Last Modified: Wed, 11 Jun 2025 03:01:26 GMT  
		Size: 341.5 MB (341526633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:04ec2c54fd69fcf8439525621e4630f18789a042f2905e1c6cca7436f0c961f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4862499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc40d84da121af7d3234b326373537f6bb1ce1d6effa821832256081f19f2619`

```dockerfile
```

-	Layers:
	-	`sha256:651cdfeeb8c18186cfed5501dacc422863e11960a872d53120f7d62de1124200`  
		Last Modified: Wed, 11 Jun 2025 02:43:27 GMT  
		Size: 4.8 MB (4840798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e213b08300b740be01133d8bd28ed8f612d2efed05d80e22fe04f4a2dfa442`  
		Last Modified: Wed, 11 Jun 2025 02:43:28 GMT  
		Size: 21.7 KB (21701 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:32c1ae2f4e585244131ad48a15480de8aa79372362389412eef65d8b32631151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.5 MB (525457542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8cbba3f6490d87399d96a9b17dc5c4c76b64df7325589490874f3f84410152`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Jun 2025 10:48:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Tue, 03 Jun 2025 10:48:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 10:48:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=20c1d8a43608aa943885c80d2b496b25aa51126f605a0c0e5b8399424da6aff4 NEO4J_TARBALL=neo4j-enterprise-2025.05.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Jun 2025 10:48:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.0-unix.tar.gz
# Tue, 03 Jun 2025 10:48:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Jun 2025 10:48:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 10:48:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Jun 2025 10:48:21 GMT
VOLUME [/data /logs]
# Tue, 03 Jun 2025 10:48:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Jun 2025 10:48:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Jun 2025 10:48:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6234ac02f2dcc239c9056925c661110c694e5f2e647658c2af946ab8e8e50b`  
		Last Modified: Wed, 11 Jun 2025 05:48:57 GMT  
		Size: 155.9 MB (155928823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c219c8fc5848c886b9e6ab2dfd0b54bedf8e5eaaad27f9e1cefdeeb61dbcb5af`  
		Last Modified: Wed, 11 Jun 2025 03:26:19 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24021a5696c32127ebb53be4e212bb595a85bd19d923d7540684590c9756c62`  
		Last Modified: Wed, 11 Jun 2025 03:26:19 GMT  
		Size: 10.0 KB (9979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b792ce1bb9b856d4ae7b57ec60644ec504475ea7965e7cc47901321c5d50787`  
		Last Modified: Wed, 11 Jun 2025 05:51:48 GMT  
		Size: 340.8 MB (340770657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:72c71c06f21942d9e0fe89d394999e4c0d996a71312892c95a4c313778c98302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4836521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0345b0e5825e8fa5fedbee1788dab5a649beb2a938a0a4e1de489c1dd86b340c`

```dockerfile
```

-	Layers:
	-	`sha256:cf30083d1e986097e50ffdbdef709cf89f9d0751893403ce4ac8da13412aa411`  
		Last Modified: Wed, 11 Jun 2025 05:43:28 GMT  
		Size: 4.8 MB (4814627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cd9a4395ceafb787141e63f33a556b11e00eb38dcbb1d88c8dd858d5cfb6c1`  
		Last Modified: Wed, 11 Jun 2025 05:43:29 GMT  
		Size: 21.9 KB (21894 bytes)  
		MIME: application/vnd.in-toto+json
