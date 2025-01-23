## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:7fd3e42060523f5ef3eb1cd0806a68bf29de2fb919f2ef920d0405de59312246
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:dcdcd562411ca7b38156ebed3e4dcec4ca0d4b4141eec585f75588f79447cf0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.2 MB (624222912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0385b289bf5d43af30000623d8da0a6334d71084f55e621aa688933c5abf6c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c8469db2dda82f16542b88fa42c694034a8d6eb65f1afb277e166bcd96346a`  
		Last Modified: Wed, 22 Jan 2025 19:39:20 GMT  
		Size: 144.5 MB (144536747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ea342b206999efc97b0548733f337a348f58d409a11b760838fa3a4a8325a2`  
		Last Modified: Wed, 22 Jan 2025 19:39:18 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8aedf9435870396729dfd6943036812bd7860b35c908e38587432d569f5922d`  
		Last Modified: Wed, 22 Jan 2025 19:39:18 GMT  
		Size: 10.0 KB (10035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bdb6068a0aec10efc7bb5c1df272e7d4b42f58564e2e3967b7a99af4297603`  
		Last Modified: Wed, 22 Jan 2025 19:39:25 GMT  
		Size: 449.4 MB (449419596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8a68ac0d12bfab5fde4d544d17d7ca5efda9ce3effc38af76d79da1b61064084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c32fce02ec8617a0a8440b20d4163027d34a7c580aa6c04043e41c2f7028c1`

```dockerfile
```

-	Layers:
	-	`sha256:5da674b1ae3d6f53865f37100e499f1f04beb05dc7371389f026795de7ec2e79`  
		Last Modified: Wed, 22 Jan 2025 19:39:18 GMT  
		Size: 3.5 MB (3538275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b647c4a570c9c9b8a7f48475054571f24c6c282e25b744ec61d80cec9e4ab9`  
		Last Modified: Wed, 22 Jan 2025 19:39:18 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ef9113a357b6175398cfb2b3e92d042b75c7be49ffbccc34e46b83b976462e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.5 MB (621505058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c397b3e70b112e72314b6a7dc79801831a2b56f64cc3eb9564137e8ec8226ed0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb02ee190e54be04764dda57106ad2732b4345d212e5d4cb8d68d9dd8039fe2`  
		Last Modified: Tue, 21 Jan 2025 20:23:33 GMT  
		Size: 143.4 MB (143361009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf3219f5f8a4af3cdbe4c430a18bbd331cea7a208e24b3d31335db62aa3ef3e`  
		Last Modified: Tue, 21 Jan 2025 20:25:03 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c86144cd5470bd2f3ec2929946ddea5a485547c701973b78ee9c21be4b378d4`  
		Last Modified: Tue, 21 Jan 2025 20:25:03 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2e8c5c07ead4b734ef5dfad8f94624c98e088918c6c762832b0b9a7c37cff2`  
		Last Modified: Tue, 21 Jan 2025 20:25:12 GMT  
		Size: 449.4 MB (449385214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:bc02fd3a4d3fae4e2c40354c8e7ac8a034655374be7b5669ac05185dd125a425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0449bea2a2e72b7e16a7cd3ed841161dde6ec5d5cb92fd86ff49c2ac3e74b356`

```dockerfile
```

-	Layers:
	-	`sha256:ee03a9458d62c7efb13285c463b7989dd722afbb7b6b69277444f5561b422f06`  
		Last Modified: Tue, 21 Jan 2025 20:25:04 GMT  
		Size: 3.5 MB (3537969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0294096bf6e09f6e6f179cd1be245e9736452b93bee9a70d9e4864fbb2ac5755`  
		Last Modified: Tue, 21 Jan 2025 20:25:03 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json
