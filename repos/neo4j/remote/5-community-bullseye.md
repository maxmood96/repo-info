## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:f2e960f4057ca770d203d746605d6b111da34043329b35c95cc4e473405f4928
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:c289368a308dd856e113b5651db6a37137f4fe806e37eb909bcde97d07e4bd9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.1 MB (338065118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0808d288adafd2ceb883621be04d3518e22c0e5efaac4bc05f524bdd173c86b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Wed, 05 Feb 2025 10:07:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Feb 2025 10:07:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 05 Feb 2025 10:07:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=95dde4f8092b9dffb57f74248ef6579bc36d6418c07ba7c513d9c95a36f44518 NEO4J_TARBALL=neo4j-community-5.26.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 05 Feb 2025 10:07:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.2-unix.tar.gz
# Wed, 05 Feb 2025 10:07:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 05 Feb 2025 10:07:55 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 05 Feb 2025 10:07:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 05 Feb 2025 10:07:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 10:07:55 GMT
WORKDIR /var/lib/neo4j
# Wed, 05 Feb 2025 10:07:55 GMT
VOLUME [/data /logs]
# Wed, 05 Feb 2025 10:07:55 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 05 Feb 2025 10:07:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 05 Feb 2025 10:07:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81b1e546d85dd8ba4135a5ed62039b018d71c9d3e6dc015d1cec4ca48d1b8aa`  
		Last Modified: Wed, 05 Feb 2025 19:28:22 GMT  
		Size: 144.6 MB (144566549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3651794f2114411b7c5e9dd9c972599d115afa6005a6f7399364ffd602aa3c9f`  
		Last Modified: Wed, 05 Feb 2025 19:28:18 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3648a96820d39b900cb3cc84f23bfb3a1b06b82dad17232691f022416ab0a8`  
		Last Modified: Wed, 05 Feb 2025 19:28:18 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f6d5893baa5c1bc6777e9bff247635f3c764e7742a41781484afebfbd473ee`  
		Last Modified: Wed, 05 Feb 2025 19:28:22 GMT  
		Size: 163.2 MB (163232083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3c7ee24e225a8cb4579262245323680e2f590f7814ab57f57eda764d323cd5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3255806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ff679b64862e48cbc6cb980c099a8afbf3bcf03e5e739b5e68db091ecdeab3`

```dockerfile
```

-	Layers:
	-	`sha256:4562647b4293f333cde7a7581bf25d3e6e83b30922e6e674bee699b41d42a22f`  
		Last Modified: Wed, 05 Feb 2025 19:28:18 GMT  
		Size: 3.2 MB (3233271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:953c38dfd0061c196c57e00a3883b0c6f63b319e3569f64d7ca15bcc8a587192`  
		Last Modified: Wed, 05 Feb 2025 19:28:18 GMT  
		Size: 22.5 KB (22535 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1ac01bfd404c391c23d94a4b21cfc5d0a8ec378923fe78c43df15efd09387f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.4 MB (335404404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d3ff0a360b837fcf7870b37a78b7a8b76a6612e89a585e6fa8e62c333322a8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Wed, 05 Feb 2025 10:07:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Feb 2025 10:07:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 05 Feb 2025 10:07:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=95dde4f8092b9dffb57f74248ef6579bc36d6418c07ba7c513d9c95a36f44518 NEO4J_TARBALL=neo4j-community-5.26.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 05 Feb 2025 10:07:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.2-unix.tar.gz
# Wed, 05 Feb 2025 10:07:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 05 Feb 2025 10:07:55 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 05 Feb 2025 10:07:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 05 Feb 2025 10:07:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 10:07:55 GMT
WORKDIR /var/lib/neo4j
# Wed, 05 Feb 2025 10:07:55 GMT
VOLUME [/data /logs]
# Wed, 05 Feb 2025 10:07:55 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 05 Feb 2025 10:07:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 05 Feb 2025 10:07:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348ff9ac1b37388eb3a2a2be1629fee6895100908a9151629f94915c2adee8bb`  
		Last Modified: Tue, 04 Feb 2025 21:13:28 GMT  
		Size: 143.5 MB (143454729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c600c1387fcaa381fcf0c0aab1445e85255372fb38aa3038c91d85a0b0dc964e`  
		Last Modified: Wed, 05 Feb 2025 19:33:54 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661e983a30edf0b78d9e1cbefef3a8fb0cc62f48bba133f835f2ce83b9cd4dac`  
		Last Modified: Wed, 05 Feb 2025 19:33:54 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e22b6398a4a8986ed645c47162c2910b8363fa65acab1cd91c7c5d0a060f4a5`  
		Last Modified: Wed, 05 Feb 2025 19:33:58 GMT  
		Size: 163.2 MB (163190940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:569ceeae2863df87d93c65b8a895dcc03a2bdd94863c13c6c7630cfbeff82109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3255789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35c79d9d8d40ecfe9c39a0b85c41003ee0997961af7fd6ad7f197b29b7d31b3`

```dockerfile
```

-	Layers:
	-	`sha256:562b6dd84d92767acb670a88b0fede4e4e4c63c70bdb915c258f088df9cc11e5`  
		Last Modified: Wed, 05 Feb 2025 19:33:55 GMT  
		Size: 3.2 MB (3233013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1045c39d51658a3d16ad77cac46be89ff2d4060419c81683d6b8242d23522e42`  
		Last Modified: Wed, 05 Feb 2025 19:33:54 GMT  
		Size: 22.8 KB (22776 bytes)  
		MIME: application/vnd.in-toto+json
