## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:d5339fa6af8aa5ba74d62ff121f5283c5f91b4044e02b4f8bfb1c25ec28e6a9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:6940266a04149bebaf4035b85881e06dcc0db56d4306c7422658e38d4b97e0ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.9 MB (624932781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8439159c6f0f13bde0a76691c58bd3e705e510ac0dfdb22b3bc0d8ca1b3218fc`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Feb 2025 14:20:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Thu, 27 Feb 2025 14:20:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Feb 2025 14:20:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d4323822935d7677ae5a12dd5638a1ed7012c190b6dd93913640ac2fda30501f NEO4J_TARBALL=neo4j-enterprise-2025.02.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 27 Feb 2025 14:20:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.02.0-unix.tar.gz
# Thu, 27 Feb 2025 14:20:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.02.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.02.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2025 14:20:06 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Feb 2025 14:20:06 GMT
VOLUME [/data /logs]
# Thu, 27 Feb 2025 14:20:06 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Feb 2025 14:20:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Feb 2025 14:20:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f45477448bf364e21defb7070b14a16fdf70f3097bc3510d724a9869ebfb74`  
		Last Modified: Mon, 17 Mar 2025 23:15:32 GMT  
		Size: 157.6 MB (157585923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d41f3c1e263be15bc24e672be969dd4c6fff571c56bc9db287e618f55356554`  
		Last Modified: Mon, 17 Mar 2025 23:15:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b48d4a95f9f9d0ef6cf1280a8eb1af7b61faf2fbd178858adf0dafb077cd36`  
		Last Modified: Mon, 17 Mar 2025 23:15:30 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fb1d4132006cd110a07709d5fc78b25be9061f90a7ad1160b58dab04af5827`  
		Last Modified: Mon, 17 Mar 2025 23:15:36 GMT  
		Size: 437.1 MB (437079127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:27ca716dd7a15e7db09df549ecd25d79f17f26bff35f42840c3fefa4e5228091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b2fdf2cb8b3cbc84be8a03869e3b237e3a06096eb60df294c954a1a98f239b`

```dockerfile
```

-	Layers:
	-	`sha256:c5749d0b2a4e0c32e2779b64b7de49c9fb96fdef1d78eaad5e5410b1864d5ca7`  
		Last Modified: Mon, 17 Mar 2025 23:15:30 GMT  
		Size: 3.5 MB (3529923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c2f1f5a2ed7c74eea61b6883c855c42a3149663ce8e9b7cc126ece0f0357b9e`  
		Last Modified: Mon, 17 Mar 2025 23:15:30 GMT  
		Size: 21.4 KB (21449 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b7205c01af7e90b92941dfc5c2b3cc3aae43dd4b3c9977dcbd95a7863e33b7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.7 MB (621669448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c78d2e059d732133ca24c85f59ba2eda6a3771553c1a92b70373b9934556e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Feb 2025 14:20:06 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Thu, 27 Feb 2025 14:20:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Feb 2025 14:20:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d4323822935d7677ae5a12dd5638a1ed7012c190b6dd93913640ac2fda30501f NEO4J_TARBALL=neo4j-enterprise-2025.02.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 27 Feb 2025 14:20:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.02.0-unix.tar.gz
# Thu, 27 Feb 2025 14:20:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.02.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.02.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Feb 2025 14:20:06 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Feb 2025 14:20:06 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Feb 2025 14:20:06 GMT
VOLUME [/data /logs]
# Thu, 27 Feb 2025 14:20:06 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Feb 2025 14:20:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Feb 2025 14:20:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b944b2358a5a7ab6f38260a8331507c0b05ceb8f17b4c303253b790f49755487`  
		Last Modified: Mon, 17 Mar 2025 23:45:31 GMT  
		Size: 155.9 MB (155859248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bbc84e11bd5f4bae7d8ed2b5b87e37a4d643e74542a40bbd42ed6a966160c1`  
		Last Modified: Tue, 18 Mar 2025 03:53:11 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69eddc1b20d7d78d1ac72785380a1ec2ff5ce4edb09ba1d6ea59ddabc0996a9a`  
		Last Modified: Tue, 18 Mar 2025 03:53:11 GMT  
		Size: 10.0 KB (10025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e080933f51813ce337ef02809f3f5d654ab70cd6e196c3ced448059ffa13cf2`  
		Last Modified: Tue, 18 Mar 2025 03:53:22 GMT  
		Size: 437.1 MB (437050352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9d3c1df04452dfa0251201647e0cc85ab2e4077304ce696a6d888f026200a15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655c38db524f74870294257dafd43e0682087caf41ea4bad1db9ab8fdab90fce`

```dockerfile
```

-	Layers:
	-	`sha256:e53c152b73690ef8d4bf4659247f2564110aa725482636d8fb3ef70404a709c6`  
		Last Modified: Tue, 18 Mar 2025 03:53:12 GMT  
		Size: 3.5 MB (3529617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a4d444738227b83a2004a4953474b34c0c33a430b129d6a1098e836c29f4c9`  
		Last Modified: Tue, 18 Mar 2025 03:53:11 GMT  
		Size: 21.6 KB (21642 bytes)  
		MIME: application/vnd.in-toto+json
