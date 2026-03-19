## `neo4j:5-enterprise-trixie`

```console
$ docker pull neo4j@sha256:f094c50a424105ec2115df3f2fafc44dafa57f9e08f84c136ec034e017d08976
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:3fdad3cb3730afe255e2d994b296e0f93ffb2d0ae2fde7cac8f6b64c1799ff30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.3 MB (708277259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5cd3edf3fe0c9bc04f1cee5ee85f41f7c61320f4b7afd7ae49749dfc4f4ee7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Wed, 18 Mar 2026 23:12:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Mar 2026 23:12:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 18 Mar 2026 23:12:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b45d9ede6bd79ced9ec6f9efbedd1b098e9553439fddf8c74cdf96f968fb1520 NEO4J_TARBALL=neo4j-enterprise-5.26.23-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 18 Mar 2026 23:12:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.23-unix.tar.gz
# Wed, 18 Mar 2026 23:12:00 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 18 Mar 2026 23:12:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.23-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 18 Mar 2026 23:12:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Mar 2026 23:12:31 GMT
WORKDIR /var/lib/neo4j
# Wed, 18 Mar 2026 23:12:31 GMT
VOLUME [/data /logs]
# Wed, 18 Mar 2026 23:12:31 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 18 Mar 2026 23:12:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 18 Mar 2026 23:12:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f295b69243b167a12e8f2ef5597478b18e04f81e81daed38d47f19b3c0c3c210`  
		Last Modified: Wed, 18 Mar 2026 23:13:06 GMT  
		Size: 157.9 MB (157857112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e18326ec3337a3a844d5f905a117ad766a5e217ed1004b2a58e97279f69e72f`  
		Last Modified: Wed, 18 Mar 2026 23:13:00 GMT  
		Size: 10.1 KB (10058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa740e60eb652ba8d4f8e0bfa832843f4e8d4f9b79443dd56f249377eb9a9c8`  
		Last Modified: Wed, 18 Mar 2026 23:13:12 GMT  
		Size: 520.6 MB (520634557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:a90ee1bc2eef8e45b14f3e882656fec388c6c4e058e52284e3b197b8760b631f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4673693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27a97ffa7144660266fbf2226e0a817ee4c8659cd029663c0bb1601cbacf26a`

```dockerfile
```

-	Layers:
	-	`sha256:17fd8d4546a475285337f1c34559aba6b5db73668bb4ed3c98b05292c339c350`  
		Last Modified: Wed, 18 Mar 2026 23:13:01 GMT  
		Size: 4.7 MB (4654396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f931fb4e29c3bdc500f046c935c6703289155f1c28e1760c2778fad54ad60b89`  
		Last Modified: Wed, 18 Mar 2026 23:13:00 GMT  
		Size: 19.3 KB (19297 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e18199ecfe766e1632d29cc7eb1d755d5ef9eec41684e11f8b85d05e4f2bb356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.0 MB (705985490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cfd4d604c27ea59cabe147aa89bc751c29f7770681c363a8f4aca6f1c65308e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Wed, 18 Mar 2026 23:11:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Mar 2026 23:11:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 18 Mar 2026 23:11:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b45d9ede6bd79ced9ec6f9efbedd1b098e9553439fddf8c74cdf96f968fb1520 NEO4J_TARBALL=neo4j-enterprise-5.26.23-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 18 Mar 2026 23:11:32 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.23-unix.tar.gz
# Wed, 18 Mar 2026 23:11:32 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 18 Mar 2026 23:12:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.23-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 18 Mar 2026 23:12:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Mar 2026 23:12:18 GMT
WORKDIR /var/lib/neo4j
# Wed, 18 Mar 2026 23:12:18 GMT
VOLUME [/data /logs]
# Wed, 18 Mar 2026 23:12:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 18 Mar 2026 23:12:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 18 Mar 2026 23:12:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4cf576851c1af1d234b041ec56e15efade90729af12bfe17a30db3a195d675`  
		Last Modified: Wed, 18 Mar 2026 23:12:55 GMT  
		Size: 156.1 MB (156133067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbd9ad484e5adab1f77d82d22be5bba412556df74ae8a136469a0b30f8f5d82`  
		Last Modified: Wed, 18 Mar 2026 23:12:49 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c5052dd9db0909a8c46644e6de176df37695010f7f7fb0f376ff6b6827c1dc`  
		Last Modified: Wed, 18 Mar 2026 23:13:02 GMT  
		Size: 519.7 MB (519703912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e7a5a660c6890ee72096a4d49681ba2e425a8e3365caf931ec342ab80d48f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4668300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d0de7250b2d9cb7aa1f3342887a47962563271e5fe98a260da44da94de2fd0`

```dockerfile
```

-	Layers:
	-	`sha256:0859ca973f47abbd8afd8acd9282a7a124d1bb45886d989159ab00a800efdb40`  
		Last Modified: Wed, 18 Mar 2026 23:12:50 GMT  
		Size: 4.6 MB (4648850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174313820c7bd821bfa9c40905e3946c3c05fd72155f6f6e9a9e9e21692ffb63`  
		Last Modified: Wed, 18 Mar 2026 23:12:49 GMT  
		Size: 19.4 KB (19450 bytes)  
		MIME: application/vnd.in-toto+json
