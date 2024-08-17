## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:c1289d495039617b05726fabc7cb00d9b2693e19c20f02ab0bcf746c155e7162
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:800f03ae433838b8d33a297354994ea758c82b85106d62e5347e7939b86fe1b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.1 MB (589093543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2052d23f5d77e9f205ad3c7b34b978d9427fe6f58b15c9f148ea3b54a2bf5145`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 Jul 2024 13:55:16 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 23 Jul 2024 13:55:16 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 13:55:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Jul 2024 13:55:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=458511394ae55681856acfe6e457dcc09fcdd2a26373a523cef9424adee871d8 NEO4J_TARBALL=neo4j-enterprise-5.22.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 23 Jul 2024 13:55:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.22.0-unix.tar.gz
# Tue, 23 Jul 2024 13:55:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.22.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.22.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 13:55:16 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 Jul 2024 13:55:16 GMT
VOLUME [/data /logs]
# Tue, 23 Jul 2024 13:55:16 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 23 Jul 2024 13:55:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 Jul 2024 13:55:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074f2ad3d164c210043f47ff16f1740b373fbb630dc22f33b59d678429d9dc34`  
		Last Modified: Sat, 17 Aug 2024 02:02:37 GMT  
		Size: 145.2 MB (145164843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4811295d5243bdfdac6e485faaff24c8ac3e5e4a81e7602099625e5b8de8da67`  
		Last Modified: Sat, 17 Aug 2024 02:02:34 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a5bbd69d583211d8652f74dca5f6c4d13a2ed4991baa350ff007b67ae56881`  
		Last Modified: Sat, 17 Aug 2024 02:02:34 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41379f9b1f5f4f6c4311c369353c8045257fda8cfac3f7e5d3d99bd61de0d5e8`  
		Last Modified: Sat, 17 Aug 2024 02:02:44 GMT  
		Size: 412.5 MB (412486916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:788fbf90452702de2b9fd424a30a9dc647edcf23de8f4f8a3e6efeee64bad7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f995567742382399889ff41d8438c620e29f8e8f72cf032afe6cc8e318850ec4`

```dockerfile
```

-	Layers:
	-	`sha256:4dfa66e0f797c861026954d1a7b1ffbbea4cce776b4564091109a7bdef9d8b9d`  
		Last Modified: Sat, 17 Aug 2024 02:02:34 GMT  
		Size: 3.3 MB (3278022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e964c90c8ccaebef5d31a031b3ebbfbc53016c7d630c2e0a129f7f99dcf74cbe`  
		Last Modified: Sat, 17 Aug 2024 02:02:34 GMT  
		Size: 21.0 KB (21015 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:237024c153874c50977a6bc114067918723bb70d256aade6adde7feb86829006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.5 MB (586500170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2cc591907fc0c7619202b171b9ca7fc934f777f45ed5feaad08d3af216eb32`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 Jul 2024 13:55:16 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Tue, 23 Jul 2024 13:55:16 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 13:55:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Jul 2024 13:55:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=458511394ae55681856acfe6e457dcc09fcdd2a26373a523cef9424adee871d8 NEO4J_TARBALL=neo4j-enterprise-5.22.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 23 Jul 2024 13:55:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.22.0-unix.tar.gz
# Tue, 23 Jul 2024 13:55:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.22.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.22.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 23 Jul 2024 13:55:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 13:55:16 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 Jul 2024 13:55:16 GMT
VOLUME [/data /logs]
# Tue, 23 Jul 2024 13:55:16 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 23 Jul 2024 13:55:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 Jul 2024 13:55:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c229b6d4698a9454e9c62693654360cc097801af308b176ca82da1b9fb41517`  
		Last Modified: Sat, 17 Aug 2024 06:14:12 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec04d17222bf745de3ed6f5ffaf7a1a7e07ff1c09bfe7c9348fc590368e490d`  
		Last Modified: Sat, 17 Aug 2024 07:37:25 GMT  
		Size: 3.9 KB (3876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1504d664b81293277228f682c8792cbfb101380c8c14830a7fab7a577a7962`  
		Last Modified: Sat, 17 Aug 2024 07:37:25 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd0fa11dd30642d0f2a495913b670c22adecc338f53576be84059b7f5563fdd`  
		Last Modified: Sat, 17 Aug 2024 07:37:34 GMT  
		Size: 412.5 MB (412451076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:c011b935f6f4142b050b1fa4e60315f5f5ca1d2333dbcd9016e50223b7663618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e85c66b153119036febaf773560207fcbd44f4402c96a54baca147d02dd7ab4`

```dockerfile
```

-	Layers:
	-	`sha256:911b590eba4932b395e703516646b1abd4cf9f391c2824aada6a1a2e0a00e92b`  
		Last Modified: Sat, 17 Aug 2024 07:37:26 GMT  
		Size: 3.3 MB (3278333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b54dd3b664f600fcd798a492694d35e0d637ad872554646a31b4ebacdcbb57ed`  
		Last Modified: Sat, 17 Aug 2024 07:37:25 GMT  
		Size: 21.6 KB (21616 bytes)  
		MIME: application/vnd.in-toto+json
