## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:47c0b21f74594af79adbd5adfea985b6b76d59238f5220cdda3b2b13fd6fb2ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:6dfd328965503f2b1f689848c4c0a6e57a79b9a140884f514e7a153aca3851fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.1 MB (624054147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d176ab0f2881f586e7e41dccf90392b1f93555fe1c2ee97cc86185e8d2c36c5`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6d478c1e3f1cc2a8d29ebcec4e4793831d5174cb7d81c8461a329e7df70cda1a NEO4J_TARBALL=neo4j-enterprise-5.26.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 05 Feb 2025 10:07:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.2-unix.tar.gz
# Wed, 05 Feb 2025 10:07:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 05 Feb 2025 10:07:55 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 05 Feb 2025 10:07:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.2-unix.tar.gz
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
	-	`sha256:e7f1c6b8d172d296d0849bbb7c635b04bc667b9307de11c7f0b873b4e4b963b0`  
		Last Modified: Wed, 05 Feb 2025 19:28:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c559b21a2509235e079f0cdd9efb2bbce8348d433ed6e7db44628690718727`  
		Last Modified: Wed, 05 Feb 2025 19:28:42 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a301960c91109d9281c65f65ce5cc969712f5f67277d31fcaaf8d9653d3ec4b7`  
		Last Modified: Wed, 05 Feb 2025 19:28:49 GMT  
		Size: 449.2 MB (449221111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:0df7ae46e2bfb48063c22955d79350058223e810aafcc08b3290b87d514edb2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b5431c559777b3a0615dd3b60207fb5c8aa4a2be7e3e97a5eec3928d09377d`

```dockerfile
```

-	Layers:
	-	`sha256:60b557880f1ac5aa1a60354de849dfe773139763fe961843648ec316bb2ee184`  
		Last Modified: Wed, 05 Feb 2025 19:28:42 GMT  
		Size: 3.5 MB (3542858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de7eb497b2ad4a700acd87c8129f01af15d5665d3ce261ab7703d0b04c153bcd`  
		Last Modified: Wed, 05 Feb 2025 19:28:42 GMT  
		Size: 20.8 KB (20758 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cc0e6575bd80b771e5f4e57cf899d64782f75e8d3984a9269b96a0b21dd74855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.4 MB (621399393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fe59a078789abd6ba9fb563dcee747d69ca39af1e681c99f4b011c26a676e0`
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
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6d478c1e3f1cc2a8d29ebcec4e4793831d5174cb7d81c8461a329e7df70cda1a NEO4J_TARBALL=neo4j-enterprise-5.26.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 05 Feb 2025 10:07:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.2-unix.tar.gz
# Wed, 05 Feb 2025 10:07:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 05 Feb 2025 10:07:55 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 05 Feb 2025 10:07:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.2-unix.tar.gz
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
	-	`sha256:30c3097d322fdf08abaffa1868c7adfded02ca89b30f64c282bbafbea20a4a83`  
		Last Modified: Wed, 05 Feb 2025 19:35:21 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe46e4a867a3c6ab5a5562b14080e7763a5dee301616dd41bd2dd7088fc80ceb`  
		Last Modified: Wed, 05 Feb 2025 19:35:21 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ff1ef9634e8d0155593665177fdbe191b13a49415a91a4d346b3692ada1cb2`  
		Last Modified: Wed, 05 Feb 2025 19:35:31 GMT  
		Size: 449.2 MB (449185926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:6f9643dd74b6f9478657b6814b1ac209db9642b5f7e85a2fe5385a756729f336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979abcf9e26e0f75d0d9aeb12a0da9dcbd18e52bd331f35b43eab46d41dfe629`

```dockerfile
```

-	Layers:
	-	`sha256:f019f0e7d6d1cac2ab68212d23081078565019216f70a7046dbdc6937d4a5fed`  
		Last Modified: Wed, 05 Feb 2025 19:35:22 GMT  
		Size: 3.5 MB (3542528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfa0e9cd99259d76ecd1fda820d7e7a29d005645158f4e70b56174659b476461`  
		Last Modified: Wed, 05 Feb 2025 19:35:21 GMT  
		Size: 20.9 KB (20927 bytes)  
		MIME: application/vnd.in-toto+json
