## `neo4j:2025-community-bullseye`

```console
$ docker pull neo4j@sha256:e9be37e336d23876723a01c6ca1e494ca54522326ad7749b0b46c57d19fd6b8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a200d6b0ab5a1878d068eb840a9c7a9bc1af7034e73bda5602aef41eb4b8883f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348379800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac995c929f43b8908ca73a89483216406d9ec42c42a9344762de930c45b3118f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 05 Feb 2025 12:33:33 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Wed, 05 Feb 2025 12:33:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Feb 2025 12:33:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2fdf62479fcfb79e5e3c5d998fc3788c621842e596fa7fb01918d492722ccfa5 NEO4J_TARBALL=neo4j-community-2025.01.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 05 Feb 2025 12:33:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.01.0-unix.tar.gz
# Wed, 05 Feb 2025 12:33:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.01.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.01.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 12:33:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 05 Feb 2025 12:33:33 GMT
VOLUME [/data /logs]
# Wed, 05 Feb 2025 12:33:33 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 05 Feb 2025 12:33:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 05 Feb 2025 12:33:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d8076a8653641eb87d9525ac6dbb915ca7bea330c045f8996453ab4214b39c`  
		Last Modified: Tue, 25 Feb 2025 02:26:51 GMT  
		Size: 157.6 MB (157585883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f58c68262f591ef62fdfab874bb08c7f54ee6dd12399f5160570783b181f25`  
		Last Modified: Tue, 25 Feb 2025 02:26:50 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b668f66bc8adee87b1c450ee57bef6e9ac3175b4291d552f5171d1ca5d08bc40`  
		Last Modified: Tue, 25 Feb 2025 02:26:49 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b68e6702834336cc63211a716356012ca65c62f2c69f6b30d78eb136a693cf8`  
		Last Modified: Tue, 25 Feb 2025 02:26:52 GMT  
		Size: 160.5 MB (160526087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0cd96960e99ca9abb6be07499732dc795c782ea7de3ed1832ce3904b439812a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3286f78745ec28135f314bff1002867df7a08668a87950faa80ed581faaeb989`

```dockerfile
```

-	Layers:
	-	`sha256:75f136c3e5c0ab4a0145889ebfcf68feca93176b6f70367dd757c155508243ab`  
		Last Modified: Tue, 25 Feb 2025 02:26:49 GMT  
		Size: 3.2 MB (3239635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99b9ebc7674779c0a3d1b68f3b23cc366cbc7a01ef11b5d8b23a18addd61e631`  
		Last Modified: Tue, 25 Feb 2025 02:26:49 GMT  
		Size: 23.9 KB (23854 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c507a923cb7fc31d2ac8251879799c2b378b81455fa53a0244c4bc41a273cf1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345108173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54adeb150f31ec95a75da9141d3938d155f300d0263bfe739c9bcb5eaceb890`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 05 Feb 2025 12:33:33 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Wed, 05 Feb 2025 12:33:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Feb 2025 12:33:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2fdf62479fcfb79e5e3c5d998fc3788c621842e596fa7fb01918d492722ccfa5 NEO4J_TARBALL=neo4j-community-2025.01.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 05 Feb 2025 12:33:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.01.0-unix.tar.gz
# Wed, 05 Feb 2025 12:33:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.01.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.01.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 05 Feb 2025 12:33:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Feb 2025 12:33:33 GMT
WORKDIR /var/lib/neo4j
# Wed, 05 Feb 2025 12:33:33 GMT
VOLUME [/data /logs]
# Wed, 05 Feb 2025 12:33:33 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 05 Feb 2025 12:33:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 05 Feb 2025 12:33:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5cb53fd16883fcaa413ae72b30f381d319c6f223b5292d219d695c8cca9147`  
		Last Modified: Tue, 25 Feb 2025 06:04:36 GMT  
		Size: 155.9 MB (155859256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3b48bb9c4b8fc3c2225a756efa3eb6151db832aeb25c9feb1fa6c7a738a693`  
		Last Modified: Tue, 25 Feb 2025 06:04:31 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b373b650adcee2709c18c851c3cd96390f1e5b56ab58ee54be80c6346c1fd`  
		Last Modified: Tue, 25 Feb 2025 06:04:32 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2b043e950d952ef00c42e8c1df5132df94c6a3dfb094a439870d7e0d1a2bc9`  
		Last Modified: Tue, 25 Feb 2025 06:04:37 GMT  
		Size: 160.5 MB (160488998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:a9b50e49902cbd368adc55057b467c3182e26b5c3d8d33d30c668fae23e70a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c3cc3523c957d5309bda9c9a5e026d0b9692ea9c412342b58649a56617e8e0`

```dockerfile
```

-	Layers:
	-	`sha256:5c1f5485e0c77c3d6635d883dc10a603441873e124de0411a2ef9d51b9eeafd6`  
		Last Modified: Tue, 25 Feb 2025 06:04:32 GMT  
		Size: 3.2 MB (3239425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e6981fe606c5fe85c57a19ab5fafea8b71be062e3d9a17af604a826bb8cee5f`  
		Last Modified: Tue, 25 Feb 2025 06:04:31 GMT  
		Size: 24.1 KB (24143 bytes)  
		MIME: application/vnd.in-toto+json
