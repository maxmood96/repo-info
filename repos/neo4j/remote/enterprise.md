## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:e6f60e0a6cb5babdac51ffb295a011170f79769e0a15626d9865a5afdd058713
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

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

### `neo4j:enterprise` - unknown; unknown

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

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a5cb56c71f77039061546004dd7c79a8c128f511db39265150e2c19925bd8ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.7 MB (621669691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d61fe54e8fd69461bc2ada4f1992dda84534d6e0981fa200d409ef3c37abe2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b45bcdca7ffe879eb2c91c1ba7c5b68f5883aa9fee954f831d0b8624c4e031`  
		Last Modified: Fri, 28 Feb 2025 18:31:17 GMT  
		Size: 155.9 MB (155859251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02407f14adde6fff7477b57c7a02a937d9639e676b786faa877c581244478bca`  
		Last Modified: Fri, 28 Feb 2025 18:32:33 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c465ac5196507619d54f0325daf8441e5d3953aa449781bfe109d805a7691c9f`  
		Last Modified: Fri, 28 Feb 2025 18:32:33 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a82a09efe2e8458ccc707040d7687364d566c470cfd106fc0f8c1a6fe183ab0`  
		Last Modified: Fri, 28 Feb 2025 18:32:42 GMT  
		Size: 437.1 MB (437050522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e554ce49df8b3a5bb16f84c4702ef9f7f96178472e4c46a18c79ebe67796ba4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58936c7c62a0fd182972de1ab233f64efcda3559e99dcfa247621944b356f5dd`

```dockerfile
```

-	Layers:
	-	`sha256:21938ff4307b793f720a07b10ae98f3d6c2278c142461315c1fedd5f3005cecc`  
		Last Modified: Fri, 28 Feb 2025 18:32:33 GMT  
		Size: 3.5 MB (3529617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a84dd7300171b1b3f54243cb9de77e70fc60ee110035c16699490934029840`  
		Last Modified: Fri, 28 Feb 2025 18:32:33 GMT  
		Size: 21.6 KB (21642 bytes)  
		MIME: application/vnd.in-toto+json
