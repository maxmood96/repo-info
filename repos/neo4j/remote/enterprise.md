## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:8552defe4b2f5325389337291f1afc7e47caa19e371d44f76d934da92e87ca23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

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

### `neo4j:enterprise` - unknown; unknown

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

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cf5026562e6f9406be8ffc2c26158f853ba8e8b084bfb8706e9146b4bc05c3b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.2 MB (558176188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89c589c58578707f38d90c0fc3d139ca5c3bf4ef3d8a7e82e6a494215fb25f9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 12 Apr 2024 11:14:18 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
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
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f691d2d58221119fad973aeae6a1886a88548bc7d424785545c5fc7ed98516ed`  
		Last Modified: Thu, 02 May 2024 12:31:02 GMT  
		Size: 143.9 MB (143892696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df51f8b2dcf492004e096cfc367ccda30bded53cd0f28ddc858ef3a28f70fa0`  
		Last Modified: Thu, 02 May 2024 12:32:39 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbf66eb8b8b9a19225d5dab50f58fef9fcb055d20ef2fdce2d712c16478110d`  
		Last Modified: Thu, 02 May 2024 12:32:39 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be024d4dc51a78e3361d0fb6c1c62d6eb5a56fdf9ea0d13bdef4dd98248e7719`  
		Last Modified: Thu, 02 May 2024 12:32:48 GMT  
		Size: 384.2 MB (384182722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:964ccbd61c965606eb950043f33b4c4ca8580b9872c4c524a58d3a7d1dbc6485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec06a230f5052c0afb2e27bd0f7f64b5fc9a3ad67fcf1d98dae216f71b26f3b5`

```dockerfile
```

-	Layers:
	-	`sha256:8830e5ae5e41962e7946b5e0175a7735f8da8fa23aeea7c393b18f8087b4d4be`  
		Last Modified: Thu, 02 May 2024 12:32:40 GMT  
		Size: 3.1 MB (3127870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f2b4b358d82c1b4509a5f50d7a7e5bf13a1f7a4219a96716ebf1a2d97cb4057`  
		Last Modified: Thu, 02 May 2024 12:32:39 GMT  
		Size: 20.9 KB (20929 bytes)  
		MIME: application/vnd.in-toto+json
