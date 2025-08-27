## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:8df67fe1b58596b85a6089daa7fd59b0b22b181fd2b6ab5b78401d7fb99a1d9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:ec404d3ca11d93a5b63457210b41f5c85d71c79ea2f9838a44c4b501c977cba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.1 MB (651103295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7451eb5232b75ff5e33a3cc64411e955f24bf3f7d6e0e3890f4252d33cdd2541`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 15:09:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 15:09:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 15:09:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e9e59dc26810399e15679dffe292975db5c947058a57345cff7433f48f67734c NEO4J_TARBALL=neo4j-enterprise-5.26.11-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 26 Aug 2025 15:09:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.11-unix.tar.gz
# Tue, 26 Aug 2025 15:09:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 26 Aug 2025 15:09:07 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 26 Aug 2025 15:09:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.11-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 26 Aug 2025 15:09:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 15:09:07 GMT
WORKDIR /var/lib/neo4j
# Tue, 26 Aug 2025 15:09:07 GMT
VOLUME [/data /logs]
# Tue, 26 Aug 2025 15:09:07 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 26 Aug 2025 15:09:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 26 Aug 2025 15:09:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d0db72cf99c3ecdf2b3efa671eed5d3514af35721909ea1abdd24c4a5a9c42`  
		Last Modified: Wed, 27 Aug 2025 17:44:06 GMT  
		Size: 144.7 MB (144693264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e171dc085aa8f93805ca71a79917c55a8879f93a09c5272606c4fbb30a7e281c`  
		Last Modified: Wed, 27 Aug 2025 17:07:37 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc31a14365daeb139182fda140e4143d7b506afda84dfd5f911c2836f5c3b94`  
		Last Modified: Wed, 27 Aug 2025 17:07:37 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa68e2dd7b82265fabb464ea213f3c17dc343cf9681403664044667e44edf422`  
		Last Modified: Wed, 27 Aug 2025 17:45:04 GMT  
		Size: 476.1 MB (476139981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:33449bb904313027ff61dc6aad37b4ca910a7b89b5ec10de5e68812d4c21ce5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4875982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9563235ab105a8eabe78c1f2c6379132a557417dc595bda66692b4007ba25b8b`

```dockerfile
```

-	Layers:
	-	`sha256:9a93b7e838e13b33496ad2fc9be73e10b367d6111f75425afc0e0ea3b4faac28`  
		Last Modified: Wed, 27 Aug 2025 17:43:57 GMT  
		Size: 4.9 MB (4854954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d0cc8c769d1d3ba7ad1912e3e0d765d9a43190bb283449d3794d4ca38f85421`  
		Last Modified: Wed, 27 Aug 2025 17:43:58 GMT  
		Size: 21.0 KB (21028 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6ed6cc9249e51e3c4ae46f0c43d357d791a98183cd9f0a9df80a9e380b41e688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.7 MB (647690728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71842d4ec90af6294002a9bb2c128b96afbc52098b4bce57d3e7db3bac0f37dd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 15:09:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 15:09:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 15:09:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e9e59dc26810399e15679dffe292975db5c947058a57345cff7433f48f67734c NEO4J_TARBALL=neo4j-enterprise-5.26.11-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 26 Aug 2025 15:09:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.11-unix.tar.gz
# Tue, 26 Aug 2025 15:09:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.11-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 26 Aug 2025 15:09:07 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 26 Aug 2025 15:09:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.11-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 26 Aug 2025 15:09:07 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 15:09:07 GMT
WORKDIR /var/lib/neo4j
# Tue, 26 Aug 2025 15:09:07 GMT
VOLUME [/data /logs]
# Tue, 26 Aug 2025 15:09:07 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 26 Aug 2025 15:09:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 26 Aug 2025 15:09:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3ae6e888f8d80755e7324ad970040abde4815c597db4a9f05cfdd6ecbe241c`  
		Last Modified: Tue, 19 Aug 2025 03:47:44 GMT  
		Size: 143.5 MB (143542102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71008a436838976be593ece4da23c269db5079e13b5136ae3c1bf376111361d`  
		Last Modified: Wed, 27 Aug 2025 17:09:55 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df38e7cd25c3e694beff926cb96a17ff162e03d10ccda275c83bb731e50d0c61`  
		Last Modified: Wed, 27 Aug 2025 17:09:56 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6ad78890d183da862372aa22f2f8ef7d43bec90d9c8ef282e91eaebffe10b8`  
		Last Modified: Wed, 27 Aug 2025 21:12:05 GMT  
		Size: 475.4 MB (475384173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:ff607e5181b8b444575458bcc9608c1f397aabaae8db5679ff9caafd2647e9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4849956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224ba97c2b02f4a25cccf094c0d4ba32faac52799ec9d733d05d83ca4ac0567c`

```dockerfile
```

-	Layers:
	-	`sha256:b860c0e7cf13d20c76d8bbd30e314024a0c6fa160401ca80f934575e1cf7ef05`  
		Last Modified: Wed, 27 Aug 2025 20:43:49 GMT  
		Size: 4.8 MB (4828759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e7b4bd65ac97a3f26948382c6b2232b67e25856961a11a3f4b16bbad46b1c64`  
		Last Modified: Wed, 27 Aug 2025 20:43:50 GMT  
		Size: 21.2 KB (21197 bytes)  
		MIME: application/vnd.in-toto+json
