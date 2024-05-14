## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:c2ed309acf79c14739b3cc3fd153b56bde4bba20b58bc0e1626cdfcd921e6482
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b43f065d67483415c00825cc7767b8d2fc26659acf320f6b1da3f59bdb479ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.8 MB (560761162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219325ad96c5293dd79dea4ead4a14b2e762b91519a01c989b8d90181f9b11ac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b824ce77ad68cafa05918acda4f34755c4fa7d142c1927e5d9616e01937952`  
		Last Modified: Tue, 14 May 2024 02:56:53 GMT  
		Size: 145.1 MB (145094994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd42b842950d86f4442c1dfcf8c7a250094f9080ee48715269b0a3283058da3`  
		Last Modified: Tue, 14 May 2024 02:56:51 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8dbe65f8123adc8ac1eec137ec82627612d54b897e25fae92714599be09f24`  
		Last Modified: Tue, 14 May 2024 02:56:51 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bd421edfc09c3359c7e5da140e5b03e6b228a145590838f4b93cc2f1f5db5f`  
		Last Modified: Tue, 14 May 2024 02:56:57 GMT  
		Size: 384.2 MB (384218832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:8ef5415132a46e38eafabf662e55d9cfbdc93cf3611e2c38ae70ae5c2922bf76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b036717d5c4ef4a3a75ce941dfdc0e55ed581137efb60f9970b0e5fae5e0477`

```dockerfile
```

-	Layers:
	-	`sha256:6188b22b1b2e55c48cdba6c484258debc801ff4984dd6aaf9d1731b4cccefb2a`  
		Last Modified: Tue, 14 May 2024 02:56:51 GMT  
		Size: 3.1 MB (3127650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e63019109b90ca587b26830733520d1fcdc01f47ee802edc68f09892adecbfa7`  
		Last Modified: Tue, 14 May 2024 02:56:51 GMT  
		Size: 21.9 KB (21896 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:dd27168936e5d5bd077870731d3c4580a7e2a1f2a273ad212fc9c3aa3f59178a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.2 MB (558175765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7702e2d0b50fccd511b427eb9336b8eae6491b3e2a563a2031f7cef311a229`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6602bdd08a78b210f56434605dbd1dd60a73e5b0823d7e96a65b39e84477d7`  
		Last Modified: Tue, 14 May 2024 17:54:13 GMT  
		Size: 3.9 KB (3874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843623d688fc8b8489257965f61b7489de9fd5a1d738aae59b5db6c7295cbad5`  
		Last Modified: Tue, 14 May 2024 17:54:12 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53f80a4199e1fd49b13460eb24c045db4fee5d0eab561b41458e2ac95d2b27d`  
		Last Modified: Tue, 14 May 2024 17:54:23 GMT  
		Size: 384.2 MB (384182637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:8a545f1a454b0d4d629627a8a5911b6cb800d98fc00199405b9e34af06d0d382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c80492d16541cbc269a485f100fdd27451094ee7b37868b7db68b83b84d7c4`

```dockerfile
```

-	Layers:
	-	`sha256:d813a06730fb1dc0c51b25362eea0388a4974497c60a6ba1cad227c41129f5b8`  
		Last Modified: Tue, 14 May 2024 17:54:13 GMT  
		Size: 3.1 MB (3127876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700fdb379067d8534052b86280126fd359f2116aacfacae3ba00d3ed9ff43e09`  
		Last Modified: Tue, 14 May 2024 17:54:12 GMT  
		Size: 20.9 KB (20927 bytes)  
		MIME: application/vnd.in-toto+json
