## `neo4j:2025-enterprise`

```console
$ docker pull neo4j@sha256:3406874fedd454815a9e43bf7fa9baf784cd0fd9f0a1d8ffe29345f4262f460b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8b82ef5622bd12d2fc31f26b43087ec43fbad8d5201978411871e520cff8646d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.1 MB (538102104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0fe5ba6e1072cfb0d89153b9a0d5af7c4338020c1e4b3e51dca9fd4d301496`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Tue, 30 Sep 2025 13:19:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Sep 2025 13:19:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0b81f4601987925d0a7a844b4206fc75fefb8cd989bc95b00f1ecbf38afc3e4f NEO4J_TARBALL=neo4j-enterprise-2025.09.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 30 Sep 2025 13:19:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
# Tue, 30 Sep 2025 13:19:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Sep 2025 13:19:30 GMT
WORKDIR /var/lib/neo4j
# Tue, 30 Sep 2025 13:19:30 GMT
VOLUME [/data /logs]
# Tue, 30 Sep 2025 13:19:30 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 30 Sep 2025 13:19:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 13:19:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7507357fe38e7d3b283eff120d6e87f796cbaa3f51a0a650ed55d01c8c3a22b4`  
		Last Modified: Fri, 10 Oct 2025 05:44:38 GMT  
		Size: 157.8 MB (157804763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec493187f00b62b958a65f9cc38b1104b684ac0d0530a2612fba6a1d6d0aeba5`  
		Last Modified: Thu, 09 Oct 2025 23:01:25 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cf0e5f871249437920568a5b8dad918456410b405768ac833f8c64915b568a`  
		Last Modified: Thu, 09 Oct 2025 23:01:25 GMT  
		Size: 10.0 KB (10019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a2290632074ae3348e2368e0ce2ce49e534779735621e3b8aabb47e3539f3f`  
		Last Modified: Fri, 10 Oct 2025 05:45:41 GMT  
		Size: 350.0 MB (350025087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:da24e985ec021643716e8ac1313a51100aad594b7cff6887dd22369784ad9b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4868377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a326e6d1ac92cb07bc43ea3aaddcb81bbe614041f1453df819a1102eb143745f`

```dockerfile
```

-	Layers:
	-	`sha256:e9987349e931670a7b74811fd9f31e7d3db60402006fd4a217536dcd148aad2f`  
		Last Modified: Fri, 10 Oct 2025 05:43:36 GMT  
		Size: 4.8 MB (4846673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cd0087c94cb0a8166c76813d3980e40d3cd7d7a4a17458d7b7ba414ba9d7f3`  
		Last Modified: Fri, 10 Oct 2025 05:43:37 GMT  
		Size: 21.7 KB (21704 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:08a5fa8b241897a1900ee4cecb2d1502fe294b243bf119a42c6eba220cf8df8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.1 MB (534112654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef56b3ddc7eb026a02ed0f315b70af7b5d98e5754452b71a96d709ce30f79243`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Tue, 30 Sep 2025 13:19:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Sep 2025 13:19:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0b81f4601987925d0a7a844b4206fc75fefb8cd989bc95b00f1ecbf38afc3e4f NEO4J_TARBALL=neo4j-enterprise-2025.09.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 30 Sep 2025 13:19:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
# Tue, 30 Sep 2025 13:19:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.09.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 30 Sep 2025 13:19:30 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Sep 2025 13:19:30 GMT
WORKDIR /var/lib/neo4j
# Tue, 30 Sep 2025 13:19:30 GMT
VOLUME [/data /logs]
# Tue, 30 Sep 2025 13:19:30 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 30 Sep 2025 13:19:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 30 Sep 2025 13:19:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740f30b54e86a7cf13f163467afe1fea0fc70490f42545cf12f1ed8991ecec2d`  
		Last Modified: Fri, 10 Oct 2025 05:55:13 GMT  
		Size: 156.1 MB (156081207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90af19a3b31ee51c60d8392a53b36928d6cbeb3d70c5ae62d83007def5964c4`  
		Last Modified: Thu, 09 Oct 2025 22:19:32 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ee40af9ee1bbef9088cd0688767873b3a5600d287b6ad59f0b9168d29ff875`  
		Last Modified: Thu, 09 Oct 2025 22:19:31 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4b2127e26a33c82ad706d6b90a4f2d3d4f206313bcec48609f875bc1c54e6d`  
		Last Modified: Fri, 10 Oct 2025 05:55:53 GMT  
		Size: 349.3 MB (349269102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:1623d9b162c5b5c998662a9008427092bc622a5f405c676486b6f00708720241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4842399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cd623845e3621884a905fdb0de6ab02c77d6bcb53904f96921156546ea4801`

```dockerfile
```

-	Layers:
	-	`sha256:2bba93cb5cae410b4a8627a41cc2b03c8459c2371bad8fbcb5fb94aa16a85e25`  
		Last Modified: Fri, 10 Oct 2025 05:43:41 GMT  
		Size: 4.8 MB (4820502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44986a564f38f46d6f27f80385f63552dff307d85edab875eec6e5cbbe63f0bb`  
		Last Modified: Fri, 10 Oct 2025 05:43:42 GMT  
		Size: 21.9 KB (21897 bytes)  
		MIME: application/vnd.in-toto+json
