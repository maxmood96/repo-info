## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:4106bc0defc2ddd4f9de1a992f1b35217a090f740bb72ecee79aacf3d0a78b9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:0c9a60cc659c92601dc0393388abcf6fb42deb053c01bbe49846265c3f565265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.0 MB (355956294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc613cb8be78056e964b1f9c11716b8e6846779c2954db5f510102848d7a7bd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 27 May 2025 16:09:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 16:09:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 27 May 2025 16:09:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0c73f9f06e4720950db49acfb27dc4e7359b8ebd2630810ba3b209e1d269bae2 NEO4J_TARBALL=neo4j-community-5.26.7-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 27 May 2025 16:09:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.7-unix.tar.gz
# Tue, 27 May 2025 16:09:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.7-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 27 May 2025 16:09:55 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 27 May 2025 16:09:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.7-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 27 May 2025 16:09:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 16:09:55 GMT
WORKDIR /var/lib/neo4j
# Tue, 27 May 2025 16:09:55 GMT
VOLUME [/data /logs]
# Tue, 27 May 2025 16:09:55 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 27 May 2025 16:09:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 27 May 2025 16:09:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df31920a92b5d4959492353d3401be816ab8bdae1d6e2a4c52937bfa89a3534`  
		Last Modified: Tue, 03 Jun 2025 05:13:52 GMT  
		Size: 144.6 MB (144635024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3401f02e355d978b7b2c61f15f70368e7c258c3cdc8e809f194552a30907e7`  
		Last Modified: Tue, 03 Jun 2025 05:13:48 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037b48bd741ce655279cd8d7e0353747b9cd773c5b431d89763dada4e6515da8`  
		Last Modified: Tue, 03 Jun 2025 05:13:48 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37f109aa91458341a7166490f808373de68cb48824914bc5ba9a0b624341f17`  
		Last Modified: Tue, 03 Jun 2025 05:13:52 GMT  
		Size: 181.1 MB (181051431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:c28f3ebfb7539f47a1ec1d9f8781ffb807468e5d392a9bc469f3be651a1bcec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4447750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de01a481c466619ea7d6dd3f6f4ccb5d043c86f90073834d06ba0608b3df2376`

```dockerfile
```

-	Layers:
	-	`sha256:b21c93df4d641b7aa774f498bc11958e48a42e834108abff2645412defd84095`  
		Last Modified: Tue, 03 Jun 2025 05:13:48 GMT  
		Size: 4.4 MB (4424960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cdcd95653f4845e23d3ab2a4a673e938d68b254494f04a4f46b458f14187e03`  
		Last Modified: Tue, 03 Jun 2025 05:13:48 GMT  
		Size: 22.8 KB (22790 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7b4faf7a9ef59eba0b21b046312be76bb712120b136676e1975d855241376c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.8 MB (351785134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0284eade0f6ac96e91c69d3f6add6d48dfc3c2f7aed5863182654b045a691477`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 27 May 2025 16:09:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 27 May 2025 16:09:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 27 May 2025 16:09:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0c73f9f06e4720950db49acfb27dc4e7359b8ebd2630810ba3b209e1d269bae2 NEO4J_TARBALL=neo4j-community-5.26.7-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 27 May 2025 16:09:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.7-unix.tar.gz
# Tue, 27 May 2025 16:09:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.7-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 27 May 2025 16:09:55 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 27 May 2025 16:09:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.7-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 27 May 2025 16:09:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 May 2025 16:09:55 GMT
WORKDIR /var/lib/neo4j
# Tue, 27 May 2025 16:09:55 GMT
VOLUME [/data /logs]
# Tue, 27 May 2025 16:09:55 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 27 May 2025 16:09:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 27 May 2025 16:09:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Wed, 21 May 2025 22:28:28 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d42e8bebe42abc72f8a99347a686e6bcc371f4b39b9d2f706177fdfa30ce72`  
		Last Modified: Tue, 27 May 2025 21:52:52 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9710b8f3f7bac26dcc32573bba3e0d8c6a478bb80ef71b53aba1a2eb41fe0f89`  
		Last Modified: Tue, 27 May 2025 21:52:48 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd41b470b488c84abcf9dd318d776d0ff9d178781f39ce90dc8c8664a6751bf`  
		Last Modified: Tue, 27 May 2025 21:52:48 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc565351c727fcfcf0d11d7b270a36169f67f50b9aa1d8db7f6da5c964d1dce5`  
		Last Modified: Tue, 27 May 2025 21:52:52 GMT  
		Size: 179.5 MB (179512319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:e7adc7a3b41f6caaeabf3a1da20980d47c51325e874d948ec74c18144af8cb0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4421867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd73577c9b1ad325e0ed1bfcb7ddd2bd064ccdcf00f02898e68960416b8cc38`

```dockerfile
```

-	Layers:
	-	`sha256:c130954a338433f1f8830c86476ca07b4d46a9b868014485fb84edbdadc6ae36`  
		Last Modified: Tue, 27 May 2025 21:52:48 GMT  
		Size: 4.4 MB (4398837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9be714feb6a31d53fc3a9ed97e65c4e4efdff41f7d4b07f9d20b5b0ffbb90317`  
		Last Modified: Tue, 27 May 2025 21:52:48 GMT  
		Size: 23.0 KB (23030 bytes)  
		MIME: application/vnd.in-toto+json
